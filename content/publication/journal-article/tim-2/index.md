---
title: "A failure-resistant, lightweight, and tightly coupled GNSS/INS/vision vehicle integration for complex urban environments"
authors:
- admin
- Xingxing Li
- Zhiheng Shen
- Zhili Xu
- Shengyu Li
- Yuxuan Zhou
- Xin Li

author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2024-05-29T00:00:00Z"
doi: "10.1109/TIM.2024.3406814"

# Schedule page publish date (NOT publication's date).
publishDate: "2024-05-29T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Instrumentation and Measurement, vol. 73, pp. 1-13, 2024, Art no. 9510613"
publication_short: ""

abstract: Accurate ego-motion estimation is the foundation for autonomous vehicle navigation in complex urban environments. In multisensor fusion schemes, in addition to environment-related degradations, sensor measurements sometimes fail, which may have an unpredictable impact on navigation performance. To make the vehicle sensor system resistant to different types of failures, we propose a failure-resistant and lightweight multisensor fusion method, in which pseudorange and carrier phase from multiple global navigation satellite system (GNSS) constellations, sparse visual features from a monocular camera, and records from multiple low-cost micro-electromechanical system (MEMS) inertial measurement units (IMUs) are integrated at the measurement level by a sliding-window tightly coupled filter. Furthermore, considering the possibilities of the high-rate IMUs recovering from failures, we propose a flexible strategy to fully utilize all available IMU measurements without frequent reinitializations. To verify the proposed method, we perform extensive evaluations under different sensor failures (e.g., GNSS short-term blocking and long-term failures, image failures, and complex IMU failures and recoveries). The results show that our method outperforms conventional approaches that include only a single IMU and merely focus on sensor degradation, and resists various types of sensor failures. Despite initializing under a harsh environment and experiencing complex sensor failures, velocity and yaw estimations are significantly improved while a submeter 3-D positioning can be achieved in approximately 80% of the challenging scenario. For complex IMU failure and recovery records, our method can fully utilize all available IMU measurements and seamlessly switch between the base and auxiliary IMUs to recover trajectories that approximate the ground truth.

# Summary. An optional shortened abstract.
summary: 

tags:
- GNSS
- sensor fusion
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://doi.org/10.1109/TIM.2024.3406814'
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
