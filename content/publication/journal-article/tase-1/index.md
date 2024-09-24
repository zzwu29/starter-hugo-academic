---
title: "Accurate and capable GNSS-inertial-visual vehicle navigation via tightly coupled multiple homogeneous sensors"
authors:
- Zhiheng Shen
- Xingxing Li
- Yuxuan Zhou
- Shengyu Li
- admin
- Xuanbin Wang

author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2024-07-05T00:00:00Z"
doi: "10.1109/TASE.2024.3422081"

# Schedule page publish date (NOT publication's date).
publishDate: "2024-07-05T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Automation Science and Engineering, (Early Access)"
publication_short: ""

abstract: Continuous and reliable estimation of navigation states is of paramount importance in ensuring the safe operation of intelligent vehicles. The conventional global navigation satellite system (GNSS)-Inertial-Visual navigation systems have demonstrated the capability to achieve locally accurate and globally drift-free pose estimation. However, challenges such as frequent satellite signal interference, limited visual features, and sudden sensor failures can severely degrade performance or even lead to complete system collapse when utilizing minimal sensor configurations. For this reason, we propose a novel and globally drift-free tightly coupled (TC) system that can integrate any number of GNSS, inertial measurement units (IMUs), and cameras to enable accurate and robust vehicle navigation. Specifically, a stacked state estimator centered on the IMU is designed to fuse information from all sensors at the raw measurement level. The pseudorange and carrier phase measurements from all GNSS terminals are directly correlated with the core IMU, ensuring accurate and fast positioning of the system in a global frame. The feature measurements from multiple independent cameras are also used to update the states by exploiting inter-epoch geometric constraints. In addition, the multiple homogeneous IMUs can not only further improve the state estimation of the system by imposing rigid constraints on the core IMU, but also switch over in time for smooth state estimation when the core IMU are faulty. We comprehensively evaluate the state estimation accuracy and robustness of the proposed approach through a series of in-vehicle experiments and simulation experiments in real urban scenarios. The results indicate that the proposed system can achieve 93.2% availability with a horizontal position error less than 0.5 m and 97.8% availability with a heading error less than 0.2 deg in typical urban environments, significantly outperforming both conventional and state-of-the-art approaches. Note to Practitioners —This study focuses on the tight integration of multiple homogeneous and heterogeneous sensors with the goal of addressing frequent interference and degradation challenges in wide-area vehicle navigation applications. We propose a general-purpose GNSS-Inertial-Visual tight coupled framework capable of integrating any number of GNSS, IMUs, and cameras at the raw measurement level. It maximizes the use of as much sensor information as possible to achieve accurate and robust state estimation and is resilient to anomalous measurements and sensor unavailability. This solution holds practical and effective for autonomous vehicles that are now commonly equipped with multiple sensors.

# Summary. An optional shortened abstract.
summary: 

tags:
- GNSS
- sensor fusion
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://doi.org/10.1109/TASE.2024.3422081'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---

<!-- {{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://wowchemy.com/docs/content/writing-markdown-latex/). -->
