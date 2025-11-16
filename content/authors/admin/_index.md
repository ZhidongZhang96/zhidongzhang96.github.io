---
# Display name
title: 张志东

# Name pronunciation (optional)
name_pronunciation: 'Zhāng Zhì Dōng'

# Full name (for SEO)
first_name: Zhidong
last_name: Zhang

# Pronouns (optional)
pronouns: he/him

# Status emoji
status:
  icon: 🚀

# Is this the primary user of the site?
superuser: true

# Highlight the author in author lists? (true/false)
highlight_name: true

# Role/position/tagline
role: Master Student

# Organizations/Affiliations to display in Biography blox
organizations:
  - name: University of Tübingen
    url: https://www.uni-tuebingen.de/

# Social network links
# Need to use another icon? Simply download the SVG icon to your `assets/media/icons/` folder.
profiles:
  - icon: at-symbol
    url: 'mailto:zhidong.zhang96@foxmail.com'
    label: E-mail Me
  - icon: brands/x
    url: https://twitter.com/ZhangZhidong
  - icon: brands/github
    url: https://github.com/ZhidongZhang96
  - icon: brands/linkedin
    url: https://www.linkedin.com/in/zhidong-zhang-136a94311/
  - icon: academicons/google-scholar
    url: https://scholar.google.com/citations?user=weFOAukAAAAJ
  - icon: academicons/orcid
    url: https://orcid.org/0009-0004-7009-3369

interests:
  - Computational Neuroscience
  - Artificial Intelligence
  - Memory and Learning

education:
  - area: MS Computational Neuroscience
    institution: University of Tübingen
    icon: ""
    date_start: 2025-10-01
    date_end: 2027-10-01 
    # summary: |
    #   GPA: 4.0/4.0

    #   Specialized in machine learning and robotics.
  - area: BEng Software Engineering
    institution: Wuhan University
    icon: "" # whu-logo.svg
    date_start: 2021-09-01
    date_end: 2025-06-30
    summary: |
      GPA: 3.73/4.0

      Courses included:
      - Advanced Mathmatics, Discrete Mathematics, Linear Algebra, Probability & Statistics.
      - Data Structures, Computer Organization, Operating Syustems, Database Systems, Computer Networks.
      - Machine Learning
  # - area: PhD Computer Science (AI Focus)
  #   institution: Stanford University
  #   icon: ""
  #   date_start: 2015-09-01
  #   date_end: 2019-06-30
  #   summary: |
  #     Thesis on _Scaling Laws for Neural Language Models_. Supervised by Prof. Andrew Ng. Published 5 papers in NeurIPS and ICML, with 2 best paper awards.
  #   button:
  #     text: 'Read Thesis'
  #     url: 'https://example.com/thesis.pdf'


work:
  - position: RNN Analysis on Same-Different Task 
    company_name: Chinese University of Hong Kong
    company_url: ''
    company_logo: ''
    date_start: 2024-09-01
    date_end: 2024-11-01
    summary: |2-
      Advisor: [Dr. Xiangbin Teng](https://www.psy.cuhk.edu.hk/index.php/component/sppagebuilder/?view=page&id=558)
      - **Model Training**: Trained RNNs on the same-different task under varying noise levels by neurogym, optimizing the code for readability and extensibility.
      - **Model Analysis**: Analyzed normalized averages and principal components (PCA) of RNN hidden states, performed linear fitting of activities at different time points to stimuli values, and analyzed the temporal scope.
  - position: Large Model Based Crossmodal Chinese Poetry Creation
    company_name: School of Computer Science, Wuhan University
    company_url: 'https://cs.whu.edu.cn/'
    company_logo: ''
    date_start: 2024-07-01
    date_end: 2024-10-01
    summary: |2-
      Advisor: [Dr. Weiping Zhu](https://cs.whu.edu.cn/info/1019/2920.htm)
      - **System Development**: Led the development of modules supporting cross-modal text and image inputs, enhancing iterative optimization mechanisms.
      - **System Evaluation**: Evaluated poem quality across different input modalities and optimization on three poem sets.
  - position: Data Analysis on Forward Flow Task
    company_name: NKLCNL, Beijing Normal University
    company_url: ''
    company_logo: ''
    date_start: 2024-04-01
    date_end: 2024-06-01
    summary: |2-
      Advisor: [Prof. Yunzhe Liu](https://brain.bnu.edu.cn/kytd/jsyjy/Ljs/18e25c12984e48eb966932924b9b76c7.htm)
      - **Data Prepocessing**: Pre-processed word data for forward flow tasks, inserting seed words, removing duplicates, and generating embeddings.
      - **Correlation Analysis**: Analyzed the correlation between participants’ scale scores and statistical indicators, including sequence length, embedding similarity, optimality divergence, semantic distance range, and “forward flow”.

  # - position: AI Research Intern
  #   company_name: OpenAI
  #   company_url: 'https://openai.com/'
  #   icon: ''
  #   date_start: 2019-06-01
  #   date_end: 2019-12-31
  #   summary: |
  #     Worked on GPT-3 scaling. Co-authored paper on prompt engineering.

# Skills
# Add your own SVG icons to `assets/media/icons/`
skills:
  - name: Technical Skills
    items:
      - name: Python
        description: ''
        percent: 80
        icon: code-bracket
      - name: Machine Learning
        description: ''
        percent: 80
        icon: chart-bar
  - name: Hobbies
    color: '#eeac02'
    color_border: '#f0bf23'
    items:
      - name: Hiking
        description: ''
        percent: 60
        icon: person-simple-walk
      - name: Reading
        description: ''
        percent: 60
        icon: book-open

languages:
  - name: Chinese (Mandarin)
    percent: 100
  - name: English
    percent: 50

# Awards.
#   Add/remove as many awards below as you like.
#   Only `title`, `awarder`, and `date` are required.
#   Begin multi-line `summary` with YAML's `|` or `|2-` multi-line prefix and indent 2 spaces below.
awards:
  - title: 'Student of Computational Neuroscience'
    url: https://compneuro.neuromatch.io
    certificate_url: https://portal.neuromatchacademy.org/certificate/d83ba21d-39f6-4a09-a00f-15e6efa22bcd
    date: '2024-07-27'
    awarder: NeuroMatch Academy
    icon: custom/nma-dark
    summary: |
      I studied the foundational concept of computational neuroscience through active learning in groups.
      The curriculum spans most areas of computational neuroscience, including Machine Learning, Dynamical Systems, Stochastic Processes, and how to model. To finish the course, I worked with partners on the project [The Working Memory Capacity of RNN]({{< relref "projects/working-memory-capacity-of-rnn/" >}}).

  # - title: Best Paper Award
  #   url: https://neurips.cc/
  #   date: '2022-12-01'
  #   awarder: NeurIPS
  #   icon: hero/trophy
  #   summary: |
  #     Awarded for groundbreaking work on efficient training of large models.
  # - title: AI Innovation Grant
  #   url: https://www.nsf.gov/
  #   date: '2021-06-15'
  #   awarder: National Science Foundation
  #   icon: hero/currency-dollar
  #   summary: |
  #     $500,000 grant for research in ethical AI development.
  # - title: Outstanding PhD Thesis
  #   url: https://www.stanford.edu/
  #   date: '2019-06-30'
  #   awarder: Stanford University
  #   icon: hero/academic-cap
  #   summary: |
  #     Recognized for contributions to scaling laws in deep learning.
---


Zhidong Zhang (**张志东**) is a master student in Computational Neuroscience at University of Tübingen. He obtained his bachelor's degree in Software Engineering from Wuhan University in 2025. 

I am fascinated by the complexity of human brain cognition (e.g. working memory, decision-making, learning, and emotion), and I look forward to working at the intersection of neuroscience and computer science to advance our understanding of biological and artificial intelligence.
