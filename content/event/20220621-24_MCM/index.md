---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "midiVerto: A Web Application to Visualize Tonality in Real Time"
event: Mathematics and Computation in Music (MCM 2022)
event_url: http://mcm2022.org/
location: Atlanta, USA
address:
  street:
  city:
  region:
  postcode:
  country:
summary: This paper presents a web application for visualizing the tonality of a piece of music---the organization of its chords and scales---at a high level of abstraction and with coordinated playback.
abstract: |
  This paper presents a web application for visualizing the tonality of a piece of music---the organization of its chords and scales---at a high level of abstraction and with coordinated playback.
  The application applies the discrete Fourier transform to the pitch-class domain of a user-specified segmentation of a MIDI file and visualizes the Fourier coefficients' trajectories.
  Since the coefficients indicate different musical properties, such as harmonic function, triadicity, and diatonicity, the application isolates aspects of a piece's tonality and shows their development in time.
  The aim of the application is to bridge a gap between mathematical music theory, musicology, and the general public by making the discrete Fourier transform as applied to the pitch-class domain accessible without requiring advanced mathematical knowledge or programming skills up front.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: 2022-06-21 #T12:06:24+01:00
date_end: 2022-06-24 #T12:06:24+01:00
all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2022-06-21T08:06:24+01:00

authors: [Daniel Harasim, Giovanni Affatato, admin]
tags: [Web application, Visualization, Discrete Fourier transform, Tonality, MIDI]

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

url_code: https://dcmlab.github.io/midiVERTO/
url_pdf:
url_video: https://www.youtube.com/watch?v=VHamnm1F3nc/

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
projects: [music-theory, digital-humanities]
---
