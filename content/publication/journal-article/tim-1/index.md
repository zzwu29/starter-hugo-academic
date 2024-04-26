---
title: "Precise and robust IMU-centric vehicle navigation via tightly integrating multiple homogeneous GNSS terminals"
authors:
- Zhiheng Shen
- Xingxing Li
- Xin Li
- Zhili Xu
- admin
- Yuxuan Zhou

author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2023-11-29T00:00:00Z"
doi: "10.1109/TIM.2023.3336725"

# Schedule page publish date (NOT publication's date).
publishDate: "2023-11-29T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Instrumentation and Measurement, vol. 73, pp. 1-14, 2023, Art no. 9501214"
publication_short: ""

abstract: In the realm of signal interference mitigation and precise attitude estimation, the utilization of multiple homogeneous Global Navigation Satellite System (GNSS) antennas/ terminals has demonstrated notable advantages. However, the potential benefits of homogeneous sensor fusion for enhancing position estimation have been relatively unexplored. In this paper, we propose a tightly coupled precise point positioning (PPP)/INS vehicle navigation algorithm without base stations, which can integrate an arbitrary number of homogeneous GNSS terminals with the aim of improving position estimation and speeding up system recovery from interference. Specifically, for the measurement representation, the original pseudorange and carrier-phase observations from all GNSS terminals are tightly incorporated with the IMU data to enable optimal state estimation. On the other hand, we exploit the known geometry between terminals and the spatially atmospheric correlation of observations to compress the states, thus to accelerate system convergence. Furthermore interestingly, since each GNSS terminal is peer-to-peer rather than master-slave in the proposed IMU-centric system, it enables a seamless operation without switching even in the event of an unexpected GNSS terminal failure. Real-world experiments have demonstrated that the proposed system can achieve a root mean square error (RMSE) of approximately 0.3 m for horizontal position estimation, and 92.24% availability at a 0.5 m boundary, outperforming the prevailing methods in terms of position estimation, state convergence and performance in extreme scenarios.

# Summary. An optional shortened abstract.
summary: 

tags:
- GNSS
- sensor fusion
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://doi.org/10.1109/TIM.2023.3336725'
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
