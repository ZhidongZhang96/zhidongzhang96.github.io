---
# Display this page in the Featured widget?
featured: true

title: 'Large Model Based Crossmodal Chinese Poetry Creation'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - L. Yang
  - admin
  - K. Niu
  - S. Pan
  - W. Zhu
  - C. Ma

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'

date: '2024-10-04T00:00:00Z'

# Schedule page publish date (NOT publication's date).
publishDate: '2024-03-24T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference'] # article

# Publication name and optional abbreviated publication name.
publication: In *2024 IEEE Smart World Congress* (SWC)
publication_short: In *2024 IEEE SWC*

abstract: Generating Chinese poetry is a complex task with significant potential for large models. However, most current systems only support single-model of input and the output lacks interpretability. This paper proposes a large model based system that supports cross-modal input of text and image, provides interpretable annotations for generated Chinese poems, and sup- ports multiple rounds of iterative optimization. First, it analyzes images with CLIP and MiniGPT-4 and generates descriptive text from analysis with ERNIE-4.0. Then, it generates Chinese ancient poems from the input text and descriptive text by ERNIE-4.0, using our devised prompts based on CRISPE. Finally, it evaluates and then optimizes the created poems with prompts based on few-shot. Preliminary evaluations have validated the efficacy of our poetry scoring criteria and demonstrated the superior performance of the system when utilizing the conjunction of text and imagery as cross-modal inputs.

# Summary. An optional shortened abstract.
summary: A poetry generation system that supported cross-modal input of text and image, provided interpretable annotations for generated Chinese poems, and supported multiple rounds of iterative optimization.

tags:
  - Large Language Models


hugoblox:
  ids:
    doi: 10.1109/SWC62898.2024.00034

# Custom links
links:
  # - type: pdf
  #   url: ""
  # - type: code
  #   url: https://github.com/HugoBlox/hugo-blox-builder
  # - type: dataset
  #   url: https://github.com/HugoBlox/hugo-blox-builder
  - type: slides
    url: uploads/slides/CrossModalPoetryCreation.pdf
  # - type: source
  #   url: https://github.com/HugoBlox/hugo-blox-builder
  # - type: video
  #   url: https://youtube.com

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'System Structure'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []
  # - LargeModeldBasedCrossmodalChinesePoetryCreation

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: "" #slides
---


<!-- > [!NOTE]
> Click the _Cite_ button above to demo the feature to enable visitors to import publication metadata into their reference management software.

> [!NOTE]
> Create your slides in Markdown - click the _Slides_ button to check out the example.

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->

