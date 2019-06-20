# How to make an R package

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

Ref: https://usethis.r-lib.org/

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

Ref: https://knausb.github.io/2017/09/a-minimal-rcpp-and-roxygen2-package/

## Workable Makevars file for mac

```
CXX_STD = CXX11
PKG_LIBS = $(LAPACK_LIBS) $(BLAS_LIBS) $(FLIBS)
```
