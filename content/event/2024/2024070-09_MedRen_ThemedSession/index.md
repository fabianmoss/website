---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "After Digitization: Computational Modeling and Analysis of Medieval Chant"
event: Medieval and Renaissance Music Conference 2024
event_url: https://www.medren2024.com/
location: Universidad de Granada
address:
  street:
  city: Granada, Spain
  region:
  postcode:
  country:
summary: Our themed session presents three projects with this ambition in mind. We showcase examples of computational modeling for chant analysis and report the gains and losses obtained during our interdisciplinary discussions.
abstract: | 
  Decades of digitization work have provided massive amounts of computer-readable chant encodings that endow scholars with unprecedented access and querying opportunities. Drawing on these digital treasure troves, recent years have witnessed the rapid development and application of computational models for chant analysis, promising to move past mere access, but rather to aid in answering musicological research questions or even inspire novel insights. Here, computational models are understood as explicit representations of scholars’ sometimes implicit domain knowledge and assumptions, e.g., about provenances or datings of sources, while at the same time offering means to incorporate notions of uncertainty and ambiguity that are so characteristic for this repertoire from a distant past. This scientific practice then turns out to be a natural continuation of the scholarly activity to draw inferences from the sparse historical record in the light of contextual knowledge. At the same time, this entails that computational approaches lacking sensitivity to the complexities surrounding historical sources are blind at best and that true interdisciplinary conversations are indispensable. Our themed session presents three projects with this ambition in mind. We showcase examples of computational modeling for chant analysis and report the gains and losses obtained during our interdisciplinary discussions.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: 2024-07-06T20:50:32+01:00
date_end: 2024-07-06T20:50:32+01:00
all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2024-03-20T20:50:32+01:00

authors: [Tim Eipert, admin, John Ashley Burgoyne, Bas Cornelissen, Jan Hajič, Vojtěch Lanz, Hana Vlhová-Wörner, Andreas Haug, Charles Atkinson]
tags: []

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

## Gregorian Chant Melody Segmentation: Centonization vs Bayesian Methods

_Vojtěch Lanz, Jan Hajič jr. & Charles Atkinson_

Gregorian melodies have been observed to re-use melodic segments, especially within modes. Such segments would have allowed for more efficient memorization. Segmentations have also led to better assignment of melodies to mode than music-theoretical methods. We model chant melody from this perspective of efficient memorization. Using only antiphon and responsory melodies themselves, we apply nonparametric Bayesian models to infer their optimal segmentations. These provide yet better mode classification results, and provide empirical evidence that modality is more determinative for the beginnings and ends of melodies, but they also suggest that surface-level segmentation is not an appropriate model of chant melody.


## Reconstructing the Formation of Trope Traditions through Network Models 

_Tim Eipert, Fabian C. Moss & Hana Vlhóva-Wörner_

The trope element catalogs of the edition project Corpus Troporum provide an essential insight into chant transmission. The catalogs reveal how the chant community created new melodies in a time when a closed collection of unchangeable sacred chant was used in liturgy. Modeling this catalog data as a graph enables us to re-evaluate existing scholarship in the light of our data: Do the shifting boundaries of the Carolingian Empire influence the melodies’ origin and the formation of melodic traditions? Can we estimate the origin date by combining statistical models and expert knowledge?

## The helping hand: A computational perspective on Guidonian solmisation

_Bas Cornelissen, Ashley Burgoyne & Andreas Haug_

For centuries, medieval singers were trained to navigate a musical space of overlapping hexachords using their hands: using Guidonian solmisation. A sequence of solmisation syllables may, therefore, come closer to how Medieval singers conceived chant than a modern transcription does. This project asks a simple question: can we automatically derive a good ‘solmisation’ for a given chant melody? Addressing this question requires a formal description of Guidonian solmisation, and the sorts of strategies one can use to produce solmizations. We hope that such a computational perspective on solmisation can contribute to our understanding of solmisation, and to musical representations that more closely align with historical conceptions.

## "I have a dream": Future projects in computer-aided chant research

_Charles M. Atkinson_

This session presents three examples of current projects involving digitization and computational analysis. My paper, however, focuses on the first word of the session title: "After". I envision three large-scale projects involving expanded computational resources that would be of great benefit to chant scholars: 1. Virtual reconstruction of liturgical manuscripts from the myriad fragments that have been and continue to be discovered. 2. Developing tools to compare Western and Eastern chant (including Byzantine, Georgian, and other traditions) allowing reciprocal text and music searches between symbol and content among all notated sources. 3. Creating a universal index of music-theoretical diagrams in all notated traditions (e.g. ancient Greek, Arabic, Chinese) showing both diagrams and the texts they illustrate.
