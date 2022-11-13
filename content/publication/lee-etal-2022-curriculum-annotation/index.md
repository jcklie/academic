---
# Documentation: https://wowchemy.com/docs/managing-content/

title: Annotation Curricula to Implicitly Train Non-Expert Annotators
subtitle: ''
summary: ''
authors:
- Ji-Ung Lee
- Jan-Christoph Klie
- Iryna Gurevych
tags: []
categories: []
date: '2022-06-01'
lastmod: 2022-11-13T11:34:27+01:00
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
publishDate: '2022-11-13T10:34:26.955656Z'
publication_types:
- '2'
abstract: Annotation studies often require annotators to familiarize themselves with
  the task, its annotation scheme, and the data domain. This can be overwhelming in
  the beginning, mentally taxing, and induce errors into the resulting annotations;
  especially in citizen science or crowdsourcing scenarios where domain expertise
  is not required. To alleviate these issues, this work proposes annotation curricula,
  a novel approach to implicitly train annotators. The goal is to gradually introduce
  annotators into the task by ordering instances to be annotated according to a learning
  curriculum. To do so, this work formalizes annotation curricula for sentence- and
  paragraph-level annotation tasks, defines an ordering strategy, and identifies well-performing
  heuristics and interactively trained models on three existing English datasets.
  Finally, we provide a proof of concept for annotation curricula in a carefully designed
  user study with 40 voluntary participants who are asked to identify the most fitting
  misconception for English tweets about the Covid-19 pandemic. The results indicate
  that using a simple heuristic to order instances can already significantly reduce
  the total annotation time while preserving a high annotation quality. Annotation
  curricula thus can be a promising research direction to improve data collection.
  To facilitate future research—for instance, to adapt annotation curricula to specific
  tasks and expert annotation scenarios—all code and data from the user study consisting
  of 2,400 annotations is made available.1
publication: '*Computational Linguistics*'
doi: 10.1162/coli_a_00436
links:
- name: URL
  url: https://doi.org/10.1162/coli_a_00436
---
