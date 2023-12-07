---
title: Integrate C++ and Python in programming
subtitle: "Hybrid Programming"

# Summary for listings and search engines
summary: "Hybrid Programming"

# Link this post with a project
projects: []

# Date published
date: '2023-11-05T00:00:00Z'

# Date updated
lastmod: '2023-12-07T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
tags: 
  - tool
  - programming
categories:
  - research
---

## CMake

You should include python directory in CMakeLists.txt as

```cmake
find_path(Third_python_ROOT       HINTS "${Third_python_ROOT}"        "$ENV{Third_python_ROOT}            ")
......
include_directories(${Third_python_ROOT}/include)
......
target_link_libraries(${PROJECT_NAME} ${Third_python_ROOT}/libs/python39.lib) # python 3.9 as an example
```

## Modify .h and .cpp file

You should include python header file in your header file as

```c++
#include <Python.h>
```

and here is an example of init

```c++
// init
Py_Initialize();
if (!Py_IsInitialized())
    return;

// an example to run python command as a string
PyRun_SimpleString("import sys"); 

// an example to set python parameters
pyParams = PyDict_New();
//mind: Py_BuildValue 's' will automatically add " at beginning and end, so "\"" + ... + "\"" will result wrong !!!
PyDict_SetItemString(pyParams, "weights_path", Py_BuildValue("s", string(weights_path).c_str())); //string
PyDict_SetItemString(pyParams, "H", Py_BuildValue("i", H)); //int
PyDict_SetItemString(pyParams, "conf_thresh", Py_BuildValue("d", conf_thresh)); //double or float
PyDict_SetItemString(pyParams, "cuda", Py_True); //bool

// init threads
PyEval_InitThreads();
PyEval_ReleaseThread(PyThreadState_Get());
```

and here is an example of run a function

```c++
PyGILState_STATE state;
state = PyGILState_Ensure();

pModule = PyImport_ImportModule("...");  // ... is python file name
pFunc = PyObject_GetAttrString(pModule, "......"); // ...... is the function name in file ...

if (pModule && PyCallable_Check(pFunc))
{
    PyObject* pArgs = PyTuple_New(1);
    PyTuple_SetItem(pArgs, 0, pyParams);
    PyObject* pReturn = PyEval_CallObject(pFunc, pArgs);
    if (pReturn)
    {
        PyArrayObject* fea = (PyArrayObject*)pReturn;
        
        // ---------- add here ---------- 

        Py_DECREF(fea);
    }
    else {
        cout << "python not valid return! error!" << endl;
    }
}
```

and you should close the python module once you do not need
```c++
Py_Finalize();
```

## Interact with numpy I/O parameters

You should include numpy directory in CMakeLists.txt as

```cmake
include_directories(${Third_python_ROOT}/Lib/site-packages/numpy/core/include)
```

You should include numpy header file in your header file as

```c++
#include <numpy/arrayobject.h>
```

An example to receive the numpy return

```c++
if (pModule && PyCallable_Check(pFunc))
{
    PyObject* pArgs = PyTuple_New(1);
    PyTuple_SetItem(pArgs, 0, pyParams);
    PyObject* pReturn = PyEval_CallObject(pFunc, pArgs);
    if (pReturn)
    {
        PyArrayObject* fea = (PyArrayObject*)pReturn;

        // -------------------- 
        int fea_row = fea->dimensions[0], fea_col = fea->dimensions[1];
        for (int idx_col = 0; idx_col < fea_col; idx_col++) {
            double x = 0.0, y = 0.0, z = 0;
            for (int idx_row = 0; idx_row < 2; idx_row++) {
                if (idx_row == 0)
                {
                    x = *(double*)(fea->data + idx_row * fea->strides[0] + idx_col * fea->strides[1]);
                }
                if (idx_row == 1)
                {
                    y = *(double*)(fea->data + idx_row * fea->strides[0] + idx_col * fea->strides[1]);
                    z = *(double*)(fea->data + 2 * fea->strides[0] + idx_col * fea->strides[1]);
                    n_pts.push_back(cv::Point2f(x, y));
                    add_feature_num = add_feature_num + 1;
                }
            }
        }
        // -------------------- 

        Py_DECREF(fea);
    }
    else {
        cout << "python not valid return! error!" << endl;
    }
}
```

## Reference Link

https://blog.csdn.net/qq_25005909/article/details/79092315