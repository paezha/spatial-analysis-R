# Activity 9: Area Data I

*NOTE*: The source files for this book are available with companion package [{isdas}](https://paezha.github.io/isdas/). The source files are in Rmarkdown format and packed as templates. These files allow you execute code within the notebook, so that you can work interactively with the notes. 

## Practice questions

Answer the following questions:

1. What is a key difference between area data and point data?
2. What is a choropleth map?
3. What is a cartogram?
4. What are the advantages and disadvantages of these mapping techniques?

## Learning objectives

In this activity, you will:

1. Create choroplet maps using census data.
2. Think about possible underlying process that could explain the pattern.
3. Think about ways to decide whether a landscape is random when working with area data.

## Suggested reading

O'Sullivan D and Unwin D (2010) Geographic Information Analysis, 2nd Edition, Chapter 7. John Wiley & Sons: New Jersey.

## Preliminaries

To start with a clean session restart the application or enter `command/ctrl + shift + F10`. A weaker alternative to this is to _only_ purge user-created objects from memory with the `R` command `rm` (for "remove"), followed by a list of items to be removed. This way at least the working space is clear of extraneous items when you begin your work:

``` r
rm(list = ls())
```

Note that `ls()` lists all objects currently on the workspace.

Load the libraries you will use in this activity. 

In addition to `tidyverse`, you will need `sf`, a package that implements simple features in R (you can learn more about this package [here](https://cran.r-project.org/web/packages/sf/vignettes/sf1.html)):

``` r
library(tidyverse)
library(sf)
library(cartogram)
library(isdas)
```

In the practice that preceded this activity, you learned about the area data and visualization techniques for area data.

Begin by loading the data that you will use in this activity:

``` r
data("Hamilton_CT")
```

This is an `sf` object with census tracts and selected demographic variables for the Hamilton CMA in Canada.

You can obtain new (calculated) variables as follows. For instance, to obtain the proportion of residents who are between 20 and 34 years old, and between 35 and 49:

``` r
Hamilton_CT <- Hamilton_CT |>
  mutate(Prop20to34 = (AGE_20_TO_24 + 
                         AGE_25_TO_29 + 
                         AGE_30_TO_34)/POPULATION, 
         Prop35to49 = (AGE_35_TO_39 + 
                         AGE_40_TO_44 + 
                         AGE_45_TO_49)/POPULATION)
```

You are ready for the next activity.

## Activity

**NOTE**: Activities include technical "how to" tasks/questions. Usually, these ask you to practice using the software to organize data, create plots, and so on in support of analysis and interpretation. The second type of questions ask you to activate your brainware and to think geographically and statistically.

::: {.infobox .software data-latex="{software}"}
**Activity Part I**
:::

1. Create choropleth maps for the proportion of the population who are 20 to 34 years old, 35 to 49 years old, 50 to 65 years old, and 65 and older.

2. Create cartograms for the proportion of the population who are 20 to 34 years old, 35 to 49 years old, 50 to 65 years old, and 65 and older.

3. Choose one of the maps you made in Question 1 or Question 2 and prepare to change the scheme and colors of this map to obtain 3 new maps. One map should have 2 classes/colors, another should have 5 classes/colors, and another should have 10 classes/colors. You can check different color palettes [in the documentation of {ggplot2}](https://ggplot2.tidyverse.org/reference/scale_brewer.html). Which scheme is more informative? What colors looked better to you?

::: {.infobox .brainware data-latex="{brainware}"}
**Activity Part II**
:::

4. Show your maps to a fellow student. What patterns do you notice in the distribution of population by age in Hamilton? Do you think the distribution of the population by age is random, or not random?

5. Devise a rule or a type of benchmark you could use to decide whether the pattern observed in a choropleth map is random. Discuss how this rule/benchmark would work. 
