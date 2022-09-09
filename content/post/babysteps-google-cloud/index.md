---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Baby steps towards working with Google Cloud"
subtitle: "A little documentation of my journey"
summary: "In this post, I document how I learned to work with Google Cloud services"
authors: [admin]
tags: []
categories: []
date: 2022-05-03T10:54:58+02:00
lastmod: 2022-05-03T10:54:58+02:00
featured: false
draft: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

## Preparations

First, I had to sign up at [https://console.cloud.google.com/](https://console.cloud.google.com/),
and give them my credit card details (to confirm I am human, well...)

The main interface is the [Concole](https://console.cloud.google.com/) (or dashboard).
The documentation is [here](https://cloud.google.com/bigquery/docs/quickstarts/query-public-dataset-console?_ga=2.109019018.-963495020.1651566990).

## Data set 

The [Public Patents Dataset](https://console.cloud.google.com/bigquery?p=patents-public-data&d=patents&page=dataset&project=online-teaching-271009) will be the main resource for this project.

Not sure yet whether we analyze and build the models on the platform or whether we script it 
(which would be better for reproducibility).