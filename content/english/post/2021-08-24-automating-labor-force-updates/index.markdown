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



```r
library(tidyverse) # because obviously
```

```
## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --
```

```
## v ggplot2 3.3.5     v purrr   0.3.4
## v tibble  3.1.3     v dplyr   1.0.7
## v tidyr   1.1.3     v stringr 1.4.0
## v readr   2.0.1     v forcats 0.5.1
```

```
## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
## x dplyr::filter() masks stats::filter()
## x dplyr::lag()    masks stats::lag()
```

```r
library(blscrapeR) # as of 8/2021, not currently on CRAN, so download from GitHub
library(googlesheets4)
```
