---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Echos (mode) classification in heirmologic corpora of Byzantine music"
event: Medieval and Renaissance Music Conference 2024
event_url: https://www.medren2024.com/
location: Universidad de Granada
address:
  street:
  city: Granada, Spain
  region:
  postcode:
  country:
summary: "Taking a Byzantine music dataset with 400 music pieces from three music sources, we perform computational classifications into echos using three content features: pitches, intervals, and Byzantine signs (called voiced units, which represent melodic movement)"
abstract: | 
  As modal music, Byzantine music groups its pieces into eight modes called _echoi_. Analogous to other modal systems, echos classification is neither unique nor universal, and it remains an open question on what grounds classifications have been made historically. Taking a Byzantine music dataset with 400 music pieces from three music sources, we perform computational classifications into echos using three content features: pitches, intervals, and Byzantine signs (called voiced units, which represent melodic movement). Furthermore, we extract phrase groupings and the distribution of voiced units into syllables. As in prior work, this research confirms that the choice of patterns' length affects the results. Inspired by Cornelissen et al.'s research (2020), we repeat the classification for n-syllables, which present better performance. We use tf–idf frequency for the creation of the models, bootstrap sampling to limit the impact of outliers on the results, and two classifiers (k-nearest neighbour and random forests) for cross-checking. We examine the validity of definitions and observations of the historical theory of Byzantine music, by repeating the classification with a modified training set derived through carefully selected elimination strategies. We observe (a) high accuracy in the classification with the full dataset, (b) the n-syllables perform better than n-grams for pitch and voiced unit attributes, and (c) pitch has the greatest impact on the echos identification, as expected. Finally, we discuss the results in relation to the historical theory of Byzantine music and the corresponding works on Gregorian music.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: 2024-07-06T20:50:32+01:00
date_end: 2024-07-06T20:50:32+01:00
all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2024-03-20T20:50:32+01:00

authors: [Polykarpos Polykarpidis, Dionysios Kalofonos, admin, Christina Anagnostopoulou]
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
