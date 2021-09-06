---
title: (Not) Eating The Elephant
author: Laura Thomas
date: '2021-08-18'
categories:
  - webdev
tags:
  - blogdown
  - github
  - learning
  - rstudio
DisableComments: no
draft: true
---

I built my first website when I was 13 from the public library's computer in basic HTML on Angelfire. After that I was commissioned to build websites for two local restaurants and a florist. It was fun.

Flash forward 20-some years... Building this website - less fun. Gotta be honest, I beat my head against the wall one long weekend trying to make all the pieces work together. I knew HTML & CSS. I knew my way around R, RStudio, RMarkdown, the Tidyverse. But this was a whole new ballgame. Especially because at the time I didn't know how to interact with Git and GitHub. I'd never heard of [Netlify](https://www.netlify.com/). I had parked a domain a long time ago but was never really compelled or confident enough to share anything. But after walking/crawling through [Blogdown](https://bookdown.org/yihui/blogdown/) and lots of Googling, I did it!

Some things I learned along the way...

### **Stage, Commit (with message), then Push:**
Git and GitHub took some getting used to. I mean, now it's all fine and great but figuring out the right order and commands and abbreviations was more confusing than I expected. I'm used to jumping in and picking up online platforms right away, figuring it out as I go, but this was different. It wasn't until I walked step by step through [Happy Git and GitHub for the useR](https://happygitwithr.com/) that things started making sense.  

### **Using `message = FALSE` in the code chunk settings:** 
When I was typing up my first project walk-through, I was annoyed because after the libraries chunk ran I would get this:

```r
library(tidyverse)
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
Which is really annoying and cluttered up my post. Then when I was perusing the [RMarkdown Cheatsheet](https://github.com/rstudio/cheatsheets/raw/master/rmarkdown.pdf) looking for something else, I came across the list for all the code chunk options, including `message`. I added `message=FALSE` into my libraries code chunk options and then...

```r
library(tidyverse)
```
Voila! No notes about it attaching packages or conflicts! Cleaner output for sharing. Win. 
