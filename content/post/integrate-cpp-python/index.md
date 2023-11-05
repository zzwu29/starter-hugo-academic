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
lastmod: '2023-11-05T00:00:00Z'

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
target_link_libraries(${PROJECT_NAME} ${Third_python_ROOT}/libs/python39.lib)
```

## .h or .hpp file

You should include python header file in your header file as

```c++
#include <Python.h>
```

and here is an example of simple usage

```c++
Py_Initialize();

// as your code in .py file
PyRun_SimpleString("......"); 
// as your code in command line
PyRun_SimpleString("import os");
PyRun_SimpleString("os.system(\"......\")");

Py_Finalize();
```