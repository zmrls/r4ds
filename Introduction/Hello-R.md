Hello R
================
Zach Morales
7/20/2021

### Installing required packages

The below block of code installs the packages that will be used
throughout the book.

``` r
install.packages(c("tidyverse", "nycflights13", "gapminder", "Lahman"))
```

### Loading packages

If packages have been installed, you can load them with the following.

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

``` r
library(nycflights13)
library(gapminder)
library(Lahman)
```

### Running R code

Example of simple arithmetic.

``` r
1 + 2
```

    ## [1] 3

### Constructing a reprex

A good minimal reproducible example makes it easier for other people to
help you, and often you’ll figure out the problem yourself in the course
of making it.

1.  Load packages at the top of the script (and ensure they are all
    updated to the latest version).
2.  Use `dput()` to generate the R code needed to recreate a dataset and
    try to find the smallest subset of your data that still reveals the
    problem.
    -   Run `dput(dataset)`.
    -   Copy the output.
    -   In the reprex type `dataset <-` then paste the copied code.
3.  Ensure that your code is easy for others to read (use spaces, ensure
    variables names are concise/informative, use comments to indicate
    where the problems lies, remove everything not related to the
    problem). Shorter code is easier to understand and easier to fix.
4.  Ensure you actually have a reprex by starting a fresh R session and
    copying/pasting the script in.
