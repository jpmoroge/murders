Report on Gun Murders
================
Rafael Irizarry
2020-08-14

## Introduction

This is a report on 2010 gun murder rates obtained from FBI reports. The
original data was obtained from [this Wikipedia
page](https://en.wikipedia.org/wiki/Murder_in_the_United_States_by_state).

We are going to use the following library:

``` r
library(tidyverse)
```

    ## -- Attaching packages ------------------------------------------------------------------------------ tidyverse 1.3.0 --

    ## v ggplot2 3.3.2     v purrr   0.3.4
    ## v tibble  3.0.3     v dplyr   1.0.0
    ## v tidyr   1.1.0     v stringr 1.4.0
    ## v readr   1.3.1     v forcats 0.5.0

    ## -- Conflicts --------------------------------------------------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

and load the data we already wrangled:

``` r
load("rda/murders.rda")
```

### Sample variable reuse

Here 51 rows are compared

## Murders data summary

    ##     state               abb                      region     population      
    ##  Length:51          Length:51          North Central:12   Min.   :  563626  
    ##  Class :character   Class :character   Northeast    : 9   1st Qu.: 1696962  
    ##  Mode  :character   Mode  :character   South        :17   Median : 4339367  
    ##                                        West         :13   Mean   : 6075769  
    ##                                                           3rd Qu.: 6636084  
    ##                                                           Max.   :37253956  
    ##      total             rate        
    ##  Min.   :   2.0   Min.   : 0.3196  
    ##  1st Qu.:  24.5   1st Qu.: 1.2526  
    ##  Median :  97.0   Median : 2.6871  
    ##  Mean   : 184.4   Mean   : 2.7791  
    ##  3rd Qu.: 268.0   3rd Qu.: 3.3861  
    ##  Max.   :1257.0   Max.   :16.4528

## Murder rate by state

We note the large state to state variability by generating a barplot
showing the murder rate by state:

![](report_files/figure-gfm/murder-rate-by-state-1.png)<!-- -->
