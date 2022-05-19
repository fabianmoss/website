---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Towards a Unified Model of Chords in Western Harmony"
authors: [Johannes Hentschel, admin, Andrew McLeod, Markus Neuwirth, Martin Rohrmeier]
date: 2022-05-19T12:15:00+01:00
doi: "10.17613/4crx-fr36"

# Schedule page publish date (NOT publication's date).
publishDate: 2021-07-19T14:15:00+01:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Music Encoding Conference Proceedings 2021"
publication_short: "MEC Proceedings 2021"

abstract: | 
  Chord-based harmony is an important aspect of many types of Western music, across genres,
  regions, and historical eras. However, the consistent representation and comparison of harmony
  across a wide range of styles (e.g. classical music, Jazz, Rock, or Pop) is a challenging task.
  Moreover, even within a single musical style, multiple theories of harmony may exist, each
  relying on its own (possibly implicit) assumptions and leading to harmonic analyses with a
  distinct focus (e.g. on the root of a chord vs. its bass note) or representation (e.g. spelled vs.
  enharmonic pitch classes). Cross-stylistic comparisons (as well as comparisons within a single
  style involving multiple annotation systems) are therefore even more difficult, particularly in a
  large-scale computational setting that requires a common overarching representation. To
  address these problems, we propose a model which allows for the representation of chords at
  multiple levels of abstraction: from chord realizations on the score level (if available), to
  pitch-class collections (including a potential application of different equivalences, such as
  enharmonic or octave equivalence), to pitch- and chord-level functions and higher-order
  abstractions. Importantly, our proposed model is also well-defined for theories which do not
  specify information at each level of abstraction (e.g., some theories make no claims about
  harmonic function), representing only those harmonic properties that are included and inducing
  others where possible (e.g., deriving scale degrees from root and key information). Our model
  thus represents an important step towards a unified representation of harmony and its various
  applications.

# Summary. An optional shortened abstract.
summary: ""

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: https://hcommons.org/deposits/item/hc:46003/ #https://apmcleod.github.io/pdf/mec-chord-model.pdf
url_code: https://github.com/DCMLab/chord-model
url_dataset:
url_poster:
url_project: https://www.epfl.ch/labs/dcml/projects/distant-listening/
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
projects: [music-theory, digital-humanities]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
