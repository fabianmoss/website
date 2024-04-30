---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Medieval Chant Lineages Unlocked: Leveraging Optical Music Recognition for Phylogenetic Analysis of Gregorian Proper"
event: "ECHOES conference 'Digital Technologies Applied to Music Research: Methodologies, Projects and Challenges'"
event_url: https://sites.google.com/fcsh.unl.pt/elsadeluca/echoes-conference
location: Universidade Nova de Lisboa
address:
  street:
  city: Lisbon
  region:
  postcode:
  country: Portugal
summary:
abstract: | 
  The Graduale Synopticum edition project, led by Harald Buchinger at Regensburg University from 2015-2018, has pioneered bringing the essential Gregorian chant propers to the forefront of musicological research through a synoptic presentation of early manuscript readings. While it successfully digitized textual variants and metadata, melody synopses are manually transcribed and image-based, preventing algorithmic analyses, e.g. to compare the melodies computationally. We address this gap using OMMR4all, a tool developed at the University of Würzburg, by transcribing the melodic variants in computer-readable form. OMMR4all employs a comprehensive automatic pipeline encompassing essential steps, including staff line detection, layout recognition, symbol detection, text detection, and syllable assignment.
  Leveraging deep learning techniques as the primary methodology, each pipeline step is meticulously crafted to ensure accuracy and efficiency. Additionally,  post-processing algorithms, enriched with musicological background knowledge, are employed to combine results from individual steps and enhance overall transcription quality.
  While the tool was initially developed for the automatic transcription of handwritten diastematic notations, it is particularly suitable for the types used in editions that mimic square notation, where the graphical representation of a neume does not differ. The pipeline was adapted for the Graduale Synopticum dataset to incorporate additional background information, such as existing lyrics and texts, and support a unique layout structure. The pipeline output consists of fully transcribed documents, where the melody, lyrics, and syllable note assignments have been extracted. 
  The dataset holds excellent potential for researching medieval chants, as the manuscripts depict some of the earliest notated versions. The issue with later manuscripts is the alignment of melodies to subsequent external theoretical models, which is why the early manuscripts may come closest to the original forms of the melodies. Here, we apply a phylogenetic model to the dataset to infer the degree of variance in the chants across manuscripts. With a network of such phylogenetic trees, we ultimately aim to uncover insights into the transmission of the manuscripts.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: 2024-06-27T08:03:22+01:00
date_end: 2024-06-29T08:03:22+01:00
all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2024-03-15T08:03:22+01:00

authors: [Tim Eipert, Alexander Hartelt, admin, Frank Puppe]
tags: [Optical Music Recognition, Digital Analysis of Chant, Phylogenetic Inference]

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
