
# Data and Code: Evaluation of the "take time to think" safer gambling message: a randomised, online experimental study

<!-- badges: start -->
<!-- badges: end -->

This repository consists of data and code for the manuscript 'Evaluation of the "take time to think" safer gambling message: a randomised, online experimental study' by Newall, Hayes, Singmann, Weiss-Cohen, Ludvig, and Walasek.

The code to reproduce the analysis is contained in the [RMarkdown file](https://rmarkdown.rstudio.com/) `ttt_analysis.Rmd`. Running the code requires that the `data` folder containing the data is in the same folder as `ttt_analysis.Rmd`.

Compiling (or "knitting") this RMarkdown document produces the output file `ttt_analysis.html` which contains numerical results and figures. Compiling also creates the results figures as files in folder `figures` as well as saves the Bayesian MCMC chains as a binary `R` file in folder `model_fits`. Both of these folders are created during compilation in case they do not yet exist.

To ensure computational reproducibility, the code uses the [`checkpoint`](https://cran.r-project.org/package=checkpoint) package. This makes sure that `R` package versions from a specific checkpoint date (2022-04-10) are used. Sometimes running checkpoint from within `RMarkdown` can fail. In this case, running the following `R` code once **before** compiling the RMarkdown document will install the required packages. Please note that the working directory of the `R` session needs to be set to the directory (see `getwd()` and `setwd()`) in which the `ttt_analysis.Rmd` file is (and in which ideally no further `R` files should be as `checkpoint` will install all packages found in the folder in which it is run.)



```r
install.packages("checkpoint")
library("checkpoint")
create_checkpoint("2022-04-10")
```


