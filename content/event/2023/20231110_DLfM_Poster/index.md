---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Communities in Medieval Troper Networks are Shaped by Carolingian Politics"
event: Digital Libraries for Musicology
event_url: https://dlfm.web.ox.ac.uk/
location: Biblioteca del Conservatorio di Milano
address:
  street:
  city:
  region:
  postcode:
  country:
summary:
abstract: |
  For medieval musicology, one main question in studying tropes of the mass is how individual tropes spread regionally, and how different manuscripts group together based on shared trope elements. Often, a clear split between an Anglo-French style and a Germanic repertoire is observed. Here, we present a new dataset and analyze it using a network model. The data is derived from volumes of Corpus Troporum (CT), which contains thousands of trope elements from different medieval European manuscripts, so-called tropers. The trope element synopses of the chants for the main feasts Christmas and Easter, as well as the feasts of the Saints were digitized, in part relying on optical character recognition (OCR). 

  Using this novel dataset, we create a network model in order to better understand how different manuscripts relate to one another, based on their shared content. We generalize the similarity metrics used in a previous study and construct a monopartite graph using the networkx Python library. In our model, nodes represent tropers and are mapped to their geographical locations of origin according to CT. 

  Since our goal is to analyze troper groups that might represent different traditions, we employ an unsupervised community detection algorithm to partition the graph. The regional groups we found might be tied to the political situation when the tropes were first created: The separation of the Carolingian empire into three different zones in 943 a.D. Interestingly, not all found communities are regionally close, demonstrating that geographical distance is not always the most important factor. 

  Our poster shows how network analysis and visualization can reveal patterns in concordance data. These patterns can further be related to and potentially explained by prior scholarship. The poster prominently features a central visualization, displaying the network of manuscripts and their similarities, from which the hypothesis can also be traced: The grouping, which is discernible from the data using community detection algorithms, aligns with the divisions of the Carolingian empire post-943. We further provide information about means of accessing the data to reproduce our results.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: 2023-11-10T13:20:00+02:00
date_end: 2023-11-10T16:10:00+02:00
all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2023-10-25T10:34:04+02:00

authors: [Tim Eipert, admin]
tags: [Digital Musicology, network models, medieval chant, community detection]

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
