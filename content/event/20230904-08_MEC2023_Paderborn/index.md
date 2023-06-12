---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Music-Text Interlinking as a Challenge for Digital Encodings of Music-Theoretical Writings"
event: "Encoding Cultures - Joint MEC and TEI conference 2023"
event_url: https://teimec2023.uni-paderborn.de/
location: Paderborn, Germany
address:
  street:
  city:
  region:
  postcode:
  country:
summary:
abstract: |
  Music-theoretical writings are often multimodal, in the sense that they may contain textual as well as musical elements, and even diagrams or images. These different modalities are moreover frequently related to one another. This can happen, for instance, when specific music examples are provided to illustrate music-theoretical concepts that are discussed in the text, or when certain passages from “real” compositions are analyzed or commented on. In addition, it can occur that musical characters and symbols such as notes, rests, or clefs, are not separated from but rather embedded within the textual flow. In general, multimodalities of text and notated music can also be found in numerous other types of sources, such as textbooks, newspapers, journals, and letters, but with a remarkable density and variety in music-critical or music-theoretical treatises.

  It has been demonstrated that text-music-linking can operate very effectively on a presentational level for text that repeatedly and explicitly refers to sections of a piece of music in standard notation.[1] Yet, another challenge for digital encoding are symbols for harmonic or other analyses that are idiosyncratic to only one or a few sources but not common enough to be considered by current music encoding standards and guidelines. This tightly-knit texture of musical and textual interdependence renders music-theoretical treatises a prime case study for digital encodings of documents that partake in both domains. A successful multimodal encoding with effective bidirectional interlinking (music to text and text to music) would moreover facilitate subsequent computational analyses, such as querying for specific terms and concepts or named-entity recognition across documents.

  Our contribution presents such a case, namely a corpus of selected 19th-century German music monographs encoded in TEI and Kern (convertible into MEI).[2] The selection was based on the relevance of the texts for the so-called harmonic dualism, a topic of at times heated debate.[3-5] Rather than discussing the content of these works, we here focus on the challenges posed through interlinkage of music and text in TEI/MEI encoded documents. While the basic scenario will consist in references between TEI and MEI portions, text is often part of musical notation itself, which would require text-music linking only within MEI. On the basis of various examples from the corpus, we demonstrate current encoding challenges, and propose and discuss several directions towards their resolution.

  - [1] Klaus Rettinghaus: Digitale und kritische Edition der 24 Probstücke der Ober-Classe aus Johann Matthesons Großer Generalbass-Schule, http://probstuecke-digital.de/.
  - [2] Text corpus: https://github.com/DCMLab/ddd/tree/main/data and music examples: https://osf.io/qm9z5/.
  - [3] Cfr. »Digitizing the Dualism Debate« (2021), https://dcmlab.github.io/ddd/.
  - [4] Jorgenson, D. (1963). A Résumé of Harmonic Dualism. Music & Letters, 44(1), 31–42. 
  - [5] Snyder, J. L. (1980). Harmonic Dualism and the Origin of the Minor Triad. Indiana Theory Review, 4(1), 45–78.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: 2023-09-04T12:01:52+02:00
date_end: 2023-09-08T12:01:52+02:00
all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2023-06-11T12:01:52+02:00

authors: [Torsten Roeder, Maik Köster, admin]
tags: [digital humanities]

# Is this a featured event? (true/false)
featured: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

# Optional filename of your slides within your event's folder or a URL.
url_slides:

url_code:
url_pdf:
url_video:

# Markdown Slides (optional).
#   Associate this event with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
