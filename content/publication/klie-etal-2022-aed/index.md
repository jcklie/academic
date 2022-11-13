---
# Documentation: https://wowchemy.com/docs/managing-content/

title: 'Annotation Error Detection: Analyzing the Past and Present for a More Coherent
  Future'
subtitle: ''
summary: ''
authors:
- Jan-Christoph Klie
- Bonnie Webber
- Iryna Gurevych
tags: []
categories: []
date: '2022-11-01'
lastmod: 2022-11-13T11:34:26+01:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: '2022-11-13T10:34:26.380540Z'
publication_types:
- '2'
abstract: Annotated data is an essential ingredient in natural language processing
  for training and evaluating machine learning models. It is therefore very desirable
  for the annotations to be of high quality. Recent work, however, has shown that
  several popular datasets contain a surprising number of annotation errors or inconsistencies.
  To alleviate this issue, many methods for annotation error detection have been devised
  over the years. While researchers show that their approaches work well on their
  newly introduced datasets, they rarely compare their methods to previous work or
  on the same datasets. This raises strong concerns on methods’ general performance
  and makes it difficult to asses their strengths and weaknesses. We therefore reimplement
  18 methods for detecting potential annotation errors and evaluate them on 9 English
  datasets for text classification as well as token and span labeling. In addition,
  we define a uniform evaluation setup including a new formalization of the annotation
  error detection task, evaluation protocol and general best practices. To facilitate
  future research and reproducibility, we release our datasets and implementations
  in an easy-to-use and open source software package.
publication: '*Computational Linguistics*'
doi: 10.1162/coli_a_00464
links:
- name: URL
  url: https://doi.org/10.1162/coli_a_00464
---
