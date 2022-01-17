---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Discovering Tonal Profiles with Latent Dirichlet Allocation"
authors: [admin, Martin Rohrmeier]
date: 2021-12-13T08:47:13+01:00
doi: "10.1177/20592043211048827"

# Schedule page publish date (NOT publication's date).
publishDate: 2021-12-13T08:47:13+01:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Music & Science, _4_, 1-15"
publication_short: ""

abstract: "Music analysis, in particular harmonic analysis, is concerned with the way pitches are organized in pieces of music, and a range of empirical applications have been developed, for example, for chord recognition or key finding. Naturally, these approaches rely on some operationalization of the concepts they aim to investigate. In this study, we take a complementary approach and discover latent tonal structures in an unsupervised manner. We use the topic model Latent Dirichlet Allocation and apply it to a large historical corpus of musical pieces from the Western classical tradition. This method conceives topics as distributions of pitch classes without assuming a priori that they correspond to either chords, keys, or other harmonic phenomena. To illustrate the generative process assumed by the model, we create an artificial corpus with arbitrary parameter settings and compare the sampled pieces to real compositions. The results we obtain by applying the topic model to the musical corpus show that the inferred topics have music-theoretically meaningful interpretations. In particular, topics cover contiguous segments on the line of fifths and mostly correspond to diatonic sets. Moreover, tracing the prominence of topics over the course of music history over ∼600 years reflects changes in the ways pitch classes are employed in musical compositions and reveals particularly strong changes at the transition from common-practice to extended tonality in the 19th century."

# Summary. An optional shortened abstract.
summary: "In this study, we use the Latent Dirichlet Allocation (LDA) topic model to discover tonal structures in a corpus of more than 2000 musical pieces from large historical range (ca. 600 years). and that the inferred topics have music-theoretically meaningful interpretations."

tags: [Topic modelling, Latent Dirichlet Allocation, tonal pitch classes, tonality, corpus studies]
categories: []
featured: false  

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf:
url_code: https://github.com/DCMLab/lda_tpcs
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: [music-theory, corpus-studies]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
