Examples in R
================
Ricardo Lacerda
2019-07-07

Loading libraries

``` r
library(tidyverse)
library(scales)
```

Creating dataframe with 100 randoms prices.

``` r
set.seed(0)
df <- tibble(price=runif(100,min=10000,max=50000))
```

Ploting a percent histogram:

``` r
df %>%
  ggplot(aes(price)) +  
  geom_histogram(aes(y = stat(width*density)),
                 breaks=seq(10000,50000,2500),fill="blue",color="black") +
  scale_y_continuous(labels = percent_format()) +
  labs(y="percentage")
```

![](README_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

Loading libraries

``` r
library(tidyverse)
library(tidyverse)
```

Creating a ggplot

``` r
  ggplot(data = mpg) +  
  geom_point(mapping= aes(x = displ,y = hwy))
```

![](README_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->
