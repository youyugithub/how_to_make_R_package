# how_to_make_R_package
how_to_make_R_package

## Method 1: Using RStudio

In Rstudio:
File -> New Project... -> New Directory -> R package/R package using Rcpp

Then: Put functions in the folders [R] and [src]

Then: Rename src/Makevars and scr/Makevars.win to be src/Makevars_discard scr/Makevars_discard.win
(Probably only necessary in MacOS)

Finally: Shift + Command + B to build package (or Build -> Build Source Pacakge)

## Method 2: Using package "usethis"

```
library(usethis)

path<-".................."
create_package(path)

usethis::create_package("abc")
usethis::use_roxygen_md()
usethis::use_rcpp()
usethis::use_rcpp_armadillo()
```

## Method 3: Using package "devtools" (now obsolete)

```
library(devtools)

WD <- '~/Desktop'
setwd(WD)

devtools::create("GatorPKG") 
WD2 <- '~/Desktop/GatorPKG'
setwd(WD2)

devtools::document()
devtools::use_rcpp()
devtools::build()
devtools::install()
```
