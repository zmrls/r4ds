Data Visualization
================
Zach Morales
7/20/2021

### ggplot2

Visualizations are centered around the tidyverse package `ggplot2`.
Install a package once, load it every time you start a new R session.
Load tidyverse (including ggplot2) using:

``` r
library(tidyverse)
```

    ## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --

    ## v ggplot2 3.3.5     v purrr   0.3.4
    ## v tibble  3.1.2     v dplyr   1.0.7
    ## v tidyr   1.1.3     v stringr 1.4.0
    ## v readr   1.4.0     v forcats 0.5.1

    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

### First Steps

First look at a data frame (rectangular collection of variables
(columns) and observations (rows).

``` r
mpg
```

    ## # A tibble: 234 x 11
    ##    manufacturer model    displ  year   cyl trans   drv     cty   hwy fl    class
    ##    <chr>        <chr>    <dbl> <int> <int> <chr>   <chr> <int> <int> <chr> <chr>
    ##  1 audi         a4         1.8  1999     4 auto(l~ f        18    29 p     comp~
    ##  2 audi         a4         1.8  1999     4 manual~ f        21    29 p     comp~
    ##  3 audi         a4         2    2008     4 manual~ f        20    31 p     comp~
    ##  4 audi         a4         2    2008     4 auto(a~ f        21    30 p     comp~
    ##  5 audi         a4         2.8  1999     6 auto(l~ f        16    26 p     comp~
    ##  6 audi         a4         2.8  1999     6 manual~ f        18    26 p     comp~
    ##  7 audi         a4         3.1  2008     6 auto(a~ f        18    27 p     comp~
    ##  8 audi         a4 quat~   1.8  1999     4 manual~ 4        18    26 p     comp~
    ##  9 audi         a4 quat~   1.8  1999     4 auto(l~ 4        16    25 p     comp~
    ## 10 audi         a4 quat~   2    2008     4 manual~ 4        20    28 p     comp~
    ## # ... with 224 more rows

Create a plot showing `hwy` (fuel efficiency on the highway in mpg) as a
function of `displ` (engine size in liters). We can use this data to
answer a question: Do cars with big engines use more fuel than cars with
small engines? It is important to make answer precise detailing the
relationship between engine size and fuel efficiency. Best to use
keywords such as **positive**, **negative**, **linear**, **nonlinear**.

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = displ, y = hwy))
```

![](Data-Visualization_files/figure-gfm/mpg%20plot1-1.png)<!-- -->

From the plot, I would say there is a **negative** relationship between
engine size and fuel efficiency. Typically, smaller engines provide
greater fuel efficiency.

##### Basic ggplot template

``` r
ggplot(data = <DATA>) + 
  <GEOM_FUNCTION>(mapping = aes(<MAPPINGS>))
```

-   `ggplot()` creates a coordinate system, layers are added to this.
    -   `ggplot(data = mpg)` first parameter for ggplot is the dataset
        to be used in the graph. This line of code along will only
        create an empty graph.
    -   `geom_point()` complete the graph by adding one or more layers
        to `ggplot()`. `geom_point()` is an example of one of the layers
        that can be added to the graph which creates a scatter plot.
        -   Each geom function takes a mapping parameter. This defines
            how variables in the dataset are mapped to visual
            properties. This mapping is done with `aes()`.
