---
title: "Using pacman::p_load()"
subtitle: 
excerpt: "A convenient way to load and install packages"
date: 2024-03-12
author: "Nicholas Vietto"
draft: false
layout: single
---

Loading and installing multiple packages can take up time and space at the beginning of your scripts, especially if you're new to R and still getting familiar with what each package does.  

For example, the beginning of my homework assignments in my second semester of Advance Statistics would often look like this:

<br>

``` r
# install.packages("")

library(haven)
library(tidyr)
library(readr)
library(dplyr)
library(ggplot2)
library(tigerstats)
library(lattice)
library(grid)
library(mosaic)
library(pastecs)
library(car)
library (multcomp)
library(granova)
library(polycor)
library(yarrr)


``` 

<br>

Which not only looks silly but also takes a significant amount of time to install each individually. 


But there is an easy solution to this problem - the pacman package. 

<br>

``` r
# first install 

install.packages("pacman")

```

<br>

Since some packages have multiple functions we can use the :: operator to specify the specific function we are calling within the package.This is good to know in cases where packages have similar dependencies and loading them together can potentially mask functions.

<br>


 
``` r
# load and install your libraries

pacman::p_load(tidyverse, haven, tigerstats, lattice, grid, mosaic, pastecs, car, multcomp, granova, polycor, yarrr)

```

<br>

This looks way better AND it installs the packages (even multiple) you don't have. So you can skip the install.packages("haven") and library (haven) lingo.

For more information on the pacman functions check out the [documentation](https://cran.r-project.org/web/packages/pacman/readme/README.html).

<br>







