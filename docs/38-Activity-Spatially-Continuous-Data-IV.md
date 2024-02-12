# Activity 18: Spatially Continuous Data IV

*NOTE*: The source files for this book are available with companion package [{isdas}](https://paezha.github.io/isdas/). The source files are in Rmarkdown format and packed as templates. These files allow you execute code within the notebook, so that you can work interactively with the notes. 

## Practice questions

Answer the following questions:

1. What does "Best" in BLUP mean?
2. What is the advantage of kriging over other interpolation approaches?
3. How is the the autocovariance used to produce optimal predictions?

## Learning objectives

In this activity, you will:

1. Conduct variograpic analysis.

2. Use kriging to interpolate a field. 

## Suggested reading

- Bailey TC and Gatrell AC [-@Bailey1995] Interactive Spatial Data Analysis, Chapters 5 and 6. Longman: Essex.
- Bivand RS, Pebesma E, and Gomez-Rubio V [-@Bivand2008] Applied Spatial Data Analysis with R, Chapter 8. Springer: New York.
- Brunsdon C and Comber L [-@Brunsdon2015R] An Introduction to R for Spatial Analysis and Mapping, Chapter 6, Sections 6.7 and 6.8. Sage: Los Angeles.
- Isaaks EH and Srivastava RM  [-@Isaaks1989applied] An Introduction to Applied Geostatistics, Chapter 12. Oxford University Press: Oxford.
- O'Sullivan D and Unwin D [-@Osullivan2010] Geographic Information Analysis, 2nd Edition, Chapters 9 and 10. John Wiley & Sons: New Jersey.

## Preliminaries

Restart `R` to begin work with a new session, or at least clear the working space to ensure that you do not have extraneous items there when you begin your work. The command in R to clear the workspace is `rm` (for "remove"), followed by a list of items to be removed. To clear the workspace from _all_ objects, do the following:

```r
rm(list = ls())
```

Note that `ls()` lists all objects currently on the workspace.

Load the libraries you will use in this activity (load other packages as appropriate). 

```r
library(isdas)
library(gstat)
library(sf)
library(tidyverse)
library(stars)
```

Load dataset:

```r
data("aquifer")
```

The data is a set of piezometric head (watertable pressure) observations of the Wolfcamp Aquifer in Texas (https://en.wikipedia.org/wiki/Hydraulic_head). Measures of pressure can be used to infer the flow of underground water, since water flows from high to low pressure areas.

These data were collected to evaluate potential flow of contamination related to a high level toxic waste repository in Texas. The Deaf Smith county site in Texas was one of three potential sites proposed for this repository. Beneath the site is a deep brine aquifer known as the Wolfcamp aquifer that may serve as a conduit of contamination leaking from the repository.

The data set consists of 85 georeferenced measurements of piezometric head. Possible applications of interpolation are to determine sites at risk and to quantify uncertainty of the interpolated surface, to evaluate the best locations for monitoring stations.

Convert to a `SpatialPointsDataFrame`:

```r
aquifer.sf <- aquifer |>
  st_as_sf(coords = c("X", "Y"),
           remove = FALSE)
```

## Activity

::: {.infobox .caution data-latex="{caution}"}
**Capstone Activity**

This is a capstone activity where you can work free-style
on a data set of your choice, and put in practice what you
have learned with respect to the analysis of spatially continuous/
field data.
:::

1. Partner with a fellow student to analyze the dataset provided.

2. Use kriging to interpolate the underlying field. Justify your modeling choices.

3. Discuss your results.

4. Imagine that you had to compare different modeling approaches (e.g., kriging, IDW). Propose a protocol to decide which method is more accurate. 
