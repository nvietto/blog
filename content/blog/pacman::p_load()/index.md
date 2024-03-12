---
title: "Using pacman::p_load()"
subtitle: "A convenient way to load and install packages"
excerpt: "A convenient way to load and install packages"
date: 2024-03-12
author: "Nicholas Vietto"
draft: false
layout: single
---
 
 
 
Loading and installing multiple packages can take up time and space at the beginning of your scripts. This is especially true when you're just starting out in R and you don't really understand what each package does. 



For example, the beginning of my homework assignments in my second semester of Advance Statistics would often look like this:

``` r

library(haven)
library(tidyr)
library(foreign)
library(readr)
library(dplyr)
library(ggplot2)
library(tigerstats)
library(lattice)
library(grid)
library(mosaic)
library(pastecs)


``` 


Which not only looks silly but also takes a significant amount of time to install each individually. BUT there is an easy solution to this problem - the pacman package. 



``` r

# first install 
install.packages("pacman")

# Now you can use pacman::p_load


```

Quick note: 

Since some packages have multiple functions we can use the :: operator to specify the specific function we are calling within the package. 

package::functionname
 
 
 
 ``` r
 
 pacman::p_load(tidyverse, tigerstats, lattice, grid, mosaic, car, multcomp)
 
 ```
 
This looks way better AND it installs the packages (even multiple) you don't have. So you can skip the install.package("tidyverse") and library (tidyverse) lingo.




Hopefully this saves you a bit of time. 


References: 

https://www.rdocumentation.org/packages/pacman/versions/0.5.1


