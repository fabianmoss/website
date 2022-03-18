---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Wavescapes: A visual hierarchical analysis of tonality using the discrete Fourier transform"
authors: [Cédric Viaccoz, Daniel Harasim, admin, Martin Rohrmeier]
date: 2022-01-17T09:26:05+01:00
doi: "10.1177/10298649211034906"

# Schedule page publish date (NOT publication's date).
publishDate: 2022-01-17T09:26:05+01:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Musicae Scientiae"
publication_short: ""

abstract: "Many structural aspects of music, such as tonality, can be expressed using hierarchical representations. In music analysis, so-called keyscapes can be used to map a key estimate (e.g., C major, F minor) to each subsection of a piece of music, thus providing an intuitive visual representation of its tonality, in particular of the hierarchical organization of local and global keys. However, that approach is limited in that the mapping relies on assumptions that are specific to common-practice tonality, such as the existence of 24 major and minor keys. This limitation can be circumvented by applying the discrete Fourier transform (DFT) to the tonal space. The DFT does not rely on style-specific theoretical assumptions but only presupposes an encoding of the music as pitch classes in 12-tone equal temperament. We introduce wavescapes, a novel visualization method for tonal hierarchies that combines the visual representation of keyscapes with music analysis based on the DFT. Since wavescapes produce visual analyses deterministically, a number of potential subjective biases are removed. By concentrating on one or more Fourier coefficients, the role of the analyst is thus focused on the interpretation and contextualization of the results. We illustrate the usefulness of this method for computational music theory by analyzing eight compositions from different historical epochs and composers (Josquin, Bach, Liszt, Chopin, Scriabin, Webern, Coltrane, Ligeti) in terms of the phase and magnitude of several Fourier coefficients. We also provide a Python library that allows such visualizations to be easily generated for any piece of music for which a symbolic score or audio recording is available."

# Summary. An optional shortened abstract.
summary: "We introduce wavescapes, a novel visualization method for tonal hierarchies that combines the visual representation of keyscapes with music analysis based on the discrete Fourier transformation (DFT) and illustrate it by analyzing compositions by Josquin, Bach, Liszt, Chopin, Scriabin, Webern, Coltrane, and Ligeti."

tags: [Discrete Fourier transform, music analysis, keyscapes, tonal hierarchy, visualization]
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
url_code:
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
  focal_point: "Center"
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: [music-theory]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
