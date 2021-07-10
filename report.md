---
title: "Fake Analysis Report"
author: Ali Ben Gator
date: "2021-06-17"
output:
  prettydoc::html_pretty:
    theme: architect
    toc: true
  html_document: 
    toc: true
  pdf_document: default
---


## Creating Dummy Text

First, I created some dummy text via

```r
library(tidyverse)
library(stringi)
set.seed(123)
stri_rand_lipsum(1)
```


## Dealing With Formatting

The output from thos functions can be easily formated like so:

**Lorem ipsum dolor sit amet, sollicitudin duis maecenas habitasse ultrices aenean tempus.** Volutpat id, non natoque ad, commodo suscipit sed risus, facilisis mauris aliquam, a. **Non leo leo, sapien non eu a quam.** Nunc vivamus in, `purus ultricies` ac suspendisse at. Eu quisque fames sapien consequat et nisl nunc, `viverra est mattis` mattis posuere. [Purus quisque auctor aenean sed risus mauris ante nisi](https://www.youtube.com/watch?v=dQw4w9WgXcQ). Ligula ac vitae lacinia. Magna aliquet et mi cubilia per. Hendrerit amet eu ullamcorper turpis ultrices aliquam.^[This is an amazing footnote containing another [Link](https://yards.albert-rapp.de/) ]

Also, one can transform the text into lists sentence by sentence

* Lorem ipsum dolor sit amet, sollicitudin duis maecenas habitasse ultrices aenean tempus.
* Volutpat id, non natoque ad, commodo suscipit sed risus, facilisis mauris aliquam, a.
* Non leo leo, sapien non eu a quam.
* Nunc vivamus in, purus ultricies ac suspendisse at.
* Eu quisque fames sapien consequat et nisl nunc, viverra est mattis mattis posuere.
* Purus quisque auctor aenean sed risus mauris ante nisi.
* Ligula ac vitae lacinia. Magna aliquet et mi cubilia per.
* Hendrerit amet eu ullamcorper turpis ultrices aliquam.

1. Lorem ipsum dolor sit amet, sollicitudin duis maecenas habitasse ultrices aenean tempus.
1. Volutpat id, non natoque ad, commodo suscipit sed risus, facilisis mauris aliquam, a.
1. Non leo leo, sapien non eu a quam.
1. Nunc vivamus in, purus ultricies ac suspendisse at.
1. Eu quisque fames sapien consequat et nisl nunc, viverra est mattis mattis posuere.
1. Purus quisque auctor aenean sed risus mauris ante nisi.
1. Ligula ac vitae lacinia. Magna aliquet et mi cubilia per.
1. Hendrerit amet eu ullamcorper turpis ultrices aliquam.


# Tables

The first 10 rows and first 5 columns of `ggplot2::mpg` are displayed in this fancy table:


```
## Error in library(kableExtra): there is no package called 'kableExtra'
```

```
## Error in ggplot2::mpg[1:10, 1:5] %>% knitr::kable() %>% kable_classic(full_width = F) %>% : could not find function "%>%"
```


# Plots

Finally, I created this helpful plot.


```r
nycflights13::flights %>% 
  na.omit() %>% 
  filter(dep_delay > 0) %>% 
  ggplot(aes(x = dep_delay)) +
  geom_histogram() + 
  scale_x_log10()
```

Also, I did this using the following code:


```r
nycflights13::flights %>% 
  na.omit() %>% 
  filter(dep_delay > 0) %>% 
  ggplot(aes(x = dep_delay)) +
  geom_histogram() + 
  scale_x_log10()
```
