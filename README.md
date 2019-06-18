# how_to_make_R_package
how_to_make_R_package

## Method 1: Using RStudio

In Rstudio:
File -> New Project... -> New Directory -> R package/R package using Rcpp

Then: Put functions in the folders [R] and [src]

Then: Rename src/Makevars and scr/Makevars.win to be src/Makevars_discard scr/Makevars_discard.win
(Probably only necessary in MacOS)

Finally: Shift + Command + B to build package (or Build -> Build Source Pacakge)

## Method 2: Using 
