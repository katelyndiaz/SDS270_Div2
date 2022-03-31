
<!-- README.md is generated from README.Rmd. Please edit that file -->

# ggArtsyR

<!-- badges: start -->
<!-- badges: end -->

### Overview

At this point in its development, the ggArtsyR package works with
`ggplot2()` to add an additional color palette to the user’s repertoire.
This is the goghColors dataset, which contains the RGB codes of colors
picked from Van Gogh paintings. It also has a function that work
alongside `ggplot2()` to create more interesting data visualizations and
add contextual information to the user’s plots. This main function is
`RectangleFiller()`, which divides data visualizations into colored
quadrants, improving the readability of graphs.

### Usage example

``` r
#is there a way to make it so that this part of the code is not visible in the final visible readme? 
# I think we only want to show usage of the function/dataset if possible
library(dplyr)
#> 
#> Attaching package: 'dplyr'
#> The following objects are masked from 'package:stats':
#> 
#>     filter, lag
#> The following objects are masked from 'package:base':
#> 
#>     intersect, setdiff, setequal, union
library(ggplot2)
plotOne <- ggplot(starwars, aes(x = mass, y = height)) +
  geom_point() +
  scale_x_continuous()

# Commented out because of error halting knit
# RectangleFiller(plotOne,)
```

### Installation instructions

Get the development version from GitHub:

``` r
# Install remotes if needed:
# install.packages("remotes")
# next line commented out because it does not work and halts knitting
# remotes::install_github("katelyndiaz/SDS270_Div2")
```

You’ll still need to render `README.Rmd` regularly, to keep `README.md`
up-to-date. `devtools::build_readme()` is handy for this. You could also
use GitHub Actions to re-render `README.Rmd` every time you push. An
example workflow can be found here:
<https://github.com/r-lib/actions/tree/v1/examples>.
