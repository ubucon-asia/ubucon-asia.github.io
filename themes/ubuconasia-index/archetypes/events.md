---
title: "{{ replace .Name "-" " " | title }}" # Name of the event
date: {{ .Date }} # When this content published
eventStartsAt: {{ .Date }} # When the event starts
eventEndsAt: {{ .Date }} # When the event ends
summary: "Description of the event in a few sentences."
link: "https://xxxx.ubucon.asia" # Event website url
image: "" # Event logo path
location: "" # City and Country (e.g. Seoul, South Korea)
venue: "" # Event venue (e.g. JustCo Tower)
draft: true # If true, this content will be hidden on website
---

Detailed description of the event (in markdown format)