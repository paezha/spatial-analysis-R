# Activity 11: Area Data III

*NOTE*: The source files for this book are available with companion package [{isdas}](https://paezha.github.io/isdas/). The source files are in Rmarkdown format and packed as templates. These files allow you execute code within the notebook, so that you can work interactively with the notes. 

## Practice questions

Answer the following questions:

1. What does the 45 degree line in the scatterplot of spatial moving averages indicate?
2. What is the effect of centering a variable around the mean?
3. In your own words, describe the phenomenon of spatial autocorrelation.
4. What is the null hypothesis in the test of autocorrelation based on Moran's I?

## Learning objectives

In this activity, you will:

1. Calculate Moran's I coefficient of autocorrelation for area data.
2. Create Moran's scatterplots.
2. Examine the results of the tests/scatterplots for further insights.
3. Think about ways to decide whether a landscape is random when working with area data.

## Suggested reading

O'Sullivan D and Unwin D (2010) Geographic Information Analysis, 2nd Edition, Chapter 7. John Wiley & Sons: New Jersey.

## Preliminaries

Restart your `R` session or at least make sure that the working space is clean when you begin your work. The command in `R` to clear the workspace is `rm` (for "remove"), followed by a list of items to be removed. To clear the workspace from _all_ objects, do the following:

``` r
rm(list = ls())
```

Note that `ls()` lists all objects currently on the workspace.

Load the libraries you will use in this activity. 

In addition to `tidyverse`, you will need `sf`, a package that implements simple features in R (you can learn about `sf` [here](https://cran.r-project.org/web/packages/sf/vignettes/sf1.html)) and `spdep`, a package that implements several spatial statistical methods (you can learn more about it [here](https://cran.r-project.org/web/packages/spdep/index.html)):

``` r
library(isdas)
library(sf)
library(spdep)
library(tidyverse)
```

Begin by loading the data that you will use in this activity:

``` r
data(Hamilton_CT)
```

This is a `sf` object with census tracts and selected demographic variables for the Hamilton CMA in Canada.

You can obtain new (calculated) variables as follows. For instance, to obtain the proportion of residents who are between 20 and 34 years old, and between 35 and 49:

``` r
Hamilton_CT <- mutate(Hamilton_CT, Prop20to34 = (AGE_20_TO_24 + AGE_25_TO_29 + AGE_30_TO_34)/POPULATION, Prop35to49 = (AGE_35_TO_39 + AGE_40_TO_44 + AGE_45_TO_49)/POPULATION)
```

You are now ready for the next activity.

## Activity

**NOTE**: Activities include technical "how to" tasks/questions. Usually, these ask you to practice using the software to organize data, create plots, and so on in support of analysis and interpretation. The second type of questions ask you to activate your brainware and to think geographically and statistically.

::: {.infobox .software data-latex="{software}"}
**Activity Part I**
:::

1. Create a spatial weights matrix for the census tracts in the Hamilton CMA.

2. Use `moran.test` to test the following variables for spatial autocorrelation: proportion of the population who are 20 to 34 years old, 35 to 49 years old, 50 to 65 years old, and 65 and older.

3. Use `moran.plot()` to create Moran's scatterplots to complement your tests of spatial autocorrelation.

::: {.infobox .brainware data-latex="{brainware}"}
**Activity Part II**
:::

4. How confident are you deciding whether the variables under analysis are not spatially random? What can you say regarding the relative strength of the spatial pattern of these variables?

5. Show a fellow student the Moran's scatterplots you created in Question 3. What can you tell about the spatial pattern based on these scatterplots? Create choropleth maps for the variables. If the spatial pattern is not random, what kind of process might have led to the patterns you observe? 

6. The scatterplots created using `moran.plot` include some observations that are labeled with their id and a different symbol. Why do you think these observations are highlighted in such a way?
