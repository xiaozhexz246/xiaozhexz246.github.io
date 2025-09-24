---
title: 'Explanation-Inspired Transferable Adversarial Attacks with Layer-Wise Increment Decomposition'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Yiyuan Chen
  - Wenze Shao

# Author notes (optional)
author_notes:
  - ''
  - ''
  - 'Corresponding author'

date: '2025-09-24T12:26:00Z'

# Schedule page publish date (NOT publication's date).
publishDate: '2025-07-24T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *International Conference On Intelligent Computing 2025*
publication_short: In *ICIC2025*

abstract: Adversarial attacks have gained significant attention in the context of neural network security. In the realm of black-box attacks, feature-level attack methods have substantially enhanced the transferability of adversarial examples. Nevertheless, existing approaches for assessing feature importance exhibit certain weaknesses. In this paper, an explanation method termed Layer-wise Increment Decomposition (LID) for calculating neuron relevance is firstly revisited by further combining it with SoftMax Gradient-LRP (SG-LRP) and Integrated Gradients (IG), making it a more robust and precise tool for guiding adversarial attacks. Building upon this foundation and drawing inspiration from existing intermediate-layer attacks, an alternative transferable attacking loss is proposed by naively adapting the LID-based neuron relevance for intermediate layers. By further incorporating sophisticated numerical schemes for the LID-induced loss, we enhance the transferability of adversarial examples. A series of experiments conducted on both normal and defense models demonstrate that the proposed approach either outperforms or achieves comparable transferability to state-of-the-art methods.

# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - Computer Vision
  - Addversarial Attack
  - Explainability
  

# Display this page in the Featured widget?
featured: true

# Standard identifiers for auto-linking
hugoblox:
  ids:
    doi: 10.1007/978-981-96-9872-1_6

# Custom links
links:
  - type: pdf
    url: './paper.pdf'
  # - type: code
  #   url: https://github.com/HugoBlox/hugo-blox-builder
  - type: dataset
    url: https://image-net.org/
  # - type: slides
  #   url: https://www.slideshare.net/
  - type: source
    url: https://link.springer.com/chapter/10.1007/978-981-96-9872-1_6
  # - type: video
  #   url: https://youtube.com

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

{{% callout note %}}
Click the _Cite_ button above to cite this work using **bibtex**.
{{% /callout %}}

<!-- {{% callout note %}}
Create your slides in Markdown - click the _Slides_ button to check out the example.
{{% /callout %}} -->

<!-- Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->
To view the full text, please visit the [paper](https://link.springer.com/chapter/10.1007/978-981-96-9872-1_6).
