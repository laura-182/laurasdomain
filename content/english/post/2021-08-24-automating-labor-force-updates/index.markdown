---
title: Automating Labor Force Updates
author: Laura Thomas
date: '2021-08-24'
categories:
  - R
  - laborforce
tags:
  - blscraper
  - datastudio
DisableComments: no
---




Monthly labor force and unemployment data are the most requested metrics both internally and externally. It was top of my list for automating after I learned R. Thankfully [blscrapeR](https://github.com/keberwein/blscrapeR) takes care of most of the hard work to get the data from the BLS website. I already was storing my data in a Google Sheet, so [googlesheets4](https://googlesheets4.tidyverse.org/) was an awesome discovery to allow me to move the data out of RStudio and into my existing data structure.

### Getting some basics out of the way...


```r
library(tidyverse) # because obviously
library(blscrapeR) # as of 8/2021, not currently on CRAN, so download from GitHub
library(googlesheets4) # you'll need a google account

# file with account information including gmail address and google sheet URL
source("~/R/laurasdomain/content/english/post/2021-08-24-automating-labor-force-updates/data/_config.R") 

gs4_auth(email = gmail) # authorize access to Google Sheets
```

### Let's talk about BLS.

The most popular one is the unemployment rate. For now, I'll save you the lecture on how it's more complicated than the news makes it out to be, but it's [down here](#unemploymentrate) for the record.




### Why the unemployment rate is more complicated than everyone makes it out to be. {#unemploymentrate}

Haven't had time to write the lecture yet. It will go here. Lucky you.
