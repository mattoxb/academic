---
title: "Improv: Live Coding for Robot Motion Design"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- Alexandra Q. Nilles
- Chase Gladish
- admin
- Amy LaViers
#- Sam Kamin

# Author notes (optional)
#author_notes:
#- "Equal contribution"
#- "Equal contribution"

date: "2018-06-28T00:00:00Z"
doi: "10.1145/3212721.3212882"

# Schedule page publish date (NOT publication's date).
publishDate: "2018-06-28T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In Proceedings of the 2018 International Conference on Movement and Computing
publication_short: MOCO'18

abstract:  []

# Summary. An optional shortened abstract.
summary:  []

tags: []

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: https://example.org

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
#image:
#  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
#  focal_point: ""
#  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []
# - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

Often, people such as educators, artists, and researchers wish to quickly
generate robot motion. However, current toolchains for programming robots can
be difficult to learn, especially for people without technical training. This
paper presents the Improv system, a programming language for high-level
description of robot motion with immediate visualization of the resulting
motion on a physical or simulated robot. Improv includes a "live coding"
wrapper for ROS ("Robot Operating System", an open-source robot software
framework which is widely used in academia and industry, and integrated with
many commercially available robots). Commands in Improv are compiled to ROS
messages. The language is inspired by choreographic techniques, and allows the
user to compose and transform movements in space and time. In this paper, we
present our work on Improv so far, as well as the design decisions made
throughout its creation.
