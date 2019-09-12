Sample
================

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that
includes both content as well as the output of any embedded R code
chunks within the document. You can embed an R code chunk like this:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Including Plots

You can also embed plots, for example:

![](Template_RMD-Sample_files/figure-gfm/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.

I’m an R Markdown document\!

# Section 1

Here’s a **code chunk** that samples from a *normal distribution*:

``` r
samp = rnorm(100)
length(samp)
```

    ## [1] 100

# Section 2

I can take the mean of the sample, too\! The mean is -0.1457712.

library(tidyverse)

## set seed to ensure reproducibility

set.seed(1234)

## define data frame containing x and y

plot\_df = tibble( x = rnorm(1000, sd = .5), y = 1 + 2 \* x +
rnorm(1000) )

## histogram of x

ggplot(plot\_df, aes(x = x)) + geom\_histogram()

## scatterplot of x and y

ggplot(plot\_df, aes(x = x, y = y)) + geom\_point()
