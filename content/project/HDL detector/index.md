---
title: Sizing HDL particles on TEM images
summary: Measure HDL particle sizes using YOLOv7 object detector
tags:
  - Python
  - Neural network
date: "2024-01-10T00:00:00Z"

# Optional external URL for project (replaces project detail page).
# external_link: https://zivkoviclab.shinyapps.io/case_study_mg/

# image:
#   caption: Photo by Toa Heftiba on Unsplash
#   focal_point: Smart

links:
  - icon: code
    icon_pack: fas
    name: Tutorial
    url: https://colab.research.google.com/drive/1Fcne-E3Ykiq-qYkkyXADWhJaMJtPfBs1?usp=sharing
url_code: 'https://github.com/zivkovic-lab/yolov7_HDL_detector'
url_pdf: ''
url_slides: ''
url_video: ''


# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

High-density lipoproteins (HDLs) are nanosized (7 – 15 nm) particles released by the liver, small intestine, and other minor tissues in the body. Conventional image analysis software can be challenged by various image quality issues and can be unpredictable. Here we implemented the yolov7 convolutional neural network for HDL imaging using TEM and particle measurement.