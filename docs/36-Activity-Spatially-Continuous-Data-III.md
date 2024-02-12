# Activity 17: Spatially Continuous Data III

*NOTE*: The source files for this book are available with companion package [{isdas}](https://paezha.github.io/isdas/). The source files are in Rmarkdown format and packed as templates. These files allow you execute code within the notebook, so that you can work interactively with the notes. 

## Practice questions

Answer the following questions:

1. What is a correlogram?
2. What is the relationship between the autocovariance and the semivariance?
3. Describe the elements of a semivariogram.
4. Why is it important to consider the number of pairs used in the calculation of the semivariance?

## Learning objectives

In this activity, you will:

1. Calculate and plot empirical semivariograms.
2. Estimate and plot theoretical semivariograms.
3. Discuss the results of variographic analysis.

## Suggested reading

- Bailey TC and Gatrell AC [-@Bailey1995] Interactive Spatial Data Analysis, Chapters 5 and 6. Longman: Essex.
- Bivand RS, Pebesma E, and Gomez-Rubio V [-@Bivand2008] Applied Spatial Data Analysis with R, Chapter 8. Springer: New York.
- Brunsdon C and Comber L [-@Brunsdon2015R] An Introduction to R for Spatial Analysis and Mapping, Chapter 6, Sections 6.7 and 6.8. Sage: Los Angeles.
- Isaaks EH and Srivastava RM  [-@Isaaks1989applied] An Introduction to Applied Geostatistics, Chapter 7. Oxford University Press: Oxford.
- O'Sullivan D and Unwin D [-@Osullivan2010] Geographic Information Analysis, 2nd Edition, Chapters 9 and 10. John Wiley & Sons: New Jersey.

## Preliminaries

As usual, please remember to start with a new session of `R` or at least use the command `rm` (for "remove") to clear the workspace, followed by a list of items to be removed. To clear the workspace from _all_ objects, do the following:

```r
rm(list = ls())
```

Note that `ls()` lists all objects currently on the workspace.

Load the libraries you will use in this activity (load other packages as appropriate). 

```r
library(isdas)
library(gstat)
library(sf)
library(spdep)
library(tidyverse)
```

Load dataset:

```r
data("aquifer")
```

Convert to a simple features object:

```r
aquifer.sf <- st_as_sf(aquifer, coords = c("X", "Y"))
```

The data is a set of piezometric head (watertable pressure) observations of the Wolfcamp Aquifer in Texas (https://en.wikipedia.org/wiki/Hydraulic_head). Measures of pressure can be used to infer the flow of underground water, since water flows from high to low pressure areas.

These data were collected to evaluate potential flow of contamination related to a high level toxic waste repository in Texas. The Deaf Smith county site in Texas was one of three potential sites proposed for this repository. Beneath the site is a deep brine aquifer known as the Wolfcamp aquifer that may serve as a conduit of contamination leaking from the repository.

The data set consists of 85 georeferenced measurements of piezometric head. Possible applications of interpolation are to determine sites at risk and to quantify uncertainty of the interpolated surface, to evaluate the best locations for monitoring stations.

## Activity

**NOTE**: Activities include technical "how to" tasks/questions. Usually, these ask you to practice using the software to organize data, create plots, and so on in support of analysis and interpretation. The second type of questions ask you to activate your brainware and to think geographically and statistically.

::: {.infobox .software data-latex="{software}"}
**Activity Part I**
:::

1. Obtain and plot the empirical semivariogram for the head in the Wolfcamp Aquifer dataset.

2. Fit a trend surface of your choice to the Aquifer data set (i.e., polynomial). Then, estimate the residuals and plot an empirical semivariogram using these residuals. How would you interpret this empirical semivariogram of residuals?

3. From the residual semivariogram estimated in Question 2, fit and plot a theoretical semivariogram model for the residual semivariogram. 

::: {.infobox .brainware data-latex="{brainware}"}
**Activity Part II**
:::

4. What is your interpretation of the semivariograms above?

5. How would you use the information provided by the variographic analysis above to improve your predictions (spatially interpolated values) of the field?
