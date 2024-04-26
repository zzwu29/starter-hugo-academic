---
title: "A novel factor graph framework for tightly coupled GNSS/INS integration with carrier-phase ambiguity resolution"
authors:
- Zhiheng Shen
- Xingxing Li
- Xuanbin Wang
- admin
- Xin Li
- Yuxuan Zhou
- Shengyu Li

author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2024-04-23T00:00:00Z"
doi: "10.1109/TITS.2024.3387466"

# Schedule page publish date (NOT publication's date).
publishDate: "2024-04-23T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Intelligent Transportation Systems (Early Access)"
publication_short: ""

abstract: Accurate position, velocity and orientation are essential for the autonomous navigation of unmanned vehicles. The integration of GNSS and INS that can deliver continuous navigation states is widely used for intelligent vehicle systems. In this paper, we propose a tightly coupled GNSS/INS positioning framework with carrier-phase ambiguity resolution based on factor graph optimization (FGO). In this approach, a sliding window optimizer is employed to fuse the multi-GNSS pseudorange and carrier-phase observations with inertial measurements. The same ambiguity within the window is considered as a state node, and the constraint on the ambiguity is continuously preserved by marginalization. To further improve the accuracy and reliability of precise positioning, the carrier-phase ambiguity resolution is introduced to the FGO-based GNSS/INS framework. When the vehicle is detected to be stationary, a zero-velocity constraint and an attitude invariant constraint will be imposed. Several experimental results indicate that the proposed method can accomplish the centimeter-level position estimation performance with beyond 90% positioning availability (horizontal < 10 cm and vertical < 10 cm) and outperforms the current state-of-the-art filter-based tightly coupled method.

# Summary. An optional shortened abstract.
summary: 

tags:
- GNSS
- sensor fusion
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://doi.org/10.1109/TITS.2024.3387466'
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
