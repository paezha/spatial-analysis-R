
<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- IMPORTANT: DO NOT KNIT WITH KNIT BUTTON. INSTEAD USE THIS:
     rmarkdown::render('README.Rmd', output_format = 'github_document', output_file = 'README.md') 
-->

# An Introduction to Spatial Data Analysis and Statistics: A Course in R

<!-- badges: start -->

[![GitHub all
contributors](https://img.shields.io/github/contributors/paezha/spatial-analysis-r?color=2b9348)](https://github.com/paezha/spatial-analysis-r/graphs/contributors)
\[![GitHub commit
activity](https://img.shields.io/github/commit-activity/y/paezha/spatial-analysis-r)
[![Launch Rstudio
Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/paezha/spatial-analysis-r/main?urlpath=rstudio)
[![DOI](https://zenodo.org/badge/391072865.svg)](https://zenodo.org/badge/latestdoi/391072865)
<!-- badges: end -->

## Introduction

This repository hosts the code underlying the book *An Introduction to
Spatial Data Analysis and Statistics: A Course in R*, by [Antonio
Paez](https://www.science.mcmaster.ca/ees/component/comprofiler/userprofile/paezha.html):

> Paez A (2021). An Introduction to Spatial Data Analysis and
> Statistics: A Course in R. McMaster Invisible Press. ISBN:
> 978-1-7778515-0-7

The book is free to read online at
<https://paezha.github.io/spatial-analysis-r>.

## Resources for Students and Instructors

### Presentation slides

I have created a set of presentation slides in mentimeter for each
substantive chapter in the book. I use these as mini-lectures in a
[flipped classroom](https://en.wikipedia.org/wiki/Flipped_classroom)
format in my course, but they can be used as a template for creating
longer presentations or lectures.

| Chapter | Mentimeter Slides | Static pdf file |
|----|----|----|
| Chapter 3 | [Introduction to Mapping](https://www.mentimeter.com/s/de73cd678c3af6b487f2f06eee44cad7/966186ab94da/edit) | pdf |
| Chapter 5 | [Mapping in `R` Continued](https://www.mentimeter.com/s/0fbd2c03bf23a9da5fbac902278644fe/ee9058215205/edit) | pdf |
| Chapter 7 | [Maps as Processes](https://www.mentimeter.com/s/59484637c743e96b6810c5e48b2cf405/d1152a9e811c/edit) | pdf |
| Chapter 9 | [Point Pattern Analysis I](https://www.mentimeter.com/s/2db531a235490f7d66a0077f2c4f0930/df1cd6ccccbb/edit) | pdf |
| Chapter 11 | [Point Pattern Analysis II](https://www.mentimeter.com/s/100f17f481ed1f28dd98112492533ba6/389b8ed12832/edit) | pdf |
| Chapter 13 | [Point Pattern Analysis III](https://www.mentimeter.com/s/8495ddf8551f0083017726a9f68cfa5b/4e5c29e8c78e/edit) | pdf |
| Chapter 15 | [Point Pattern Analysis IV](https://www.mentimeter.com/s/587258400bd04521b52585f27296a799/57f84401a6a6/edit) | pdf |
| Chapter 17 | [Point Pattern Analysis V](https://www.mentimeter.com/s/fe385c8dbd256f2645507290f579b15c/2056e80d53e4/edit) | pdf |
| Chapter 19 | [Area Data I](https://www.mentimeter.com/s/cab8fcae7e9b2cd1f447f79b5349dd23/d939ca4b33e9/edit) | pdf |
| Chapter 21 | [Area Data II](https://www.mentimeter.com/s/c8442809151f00d4ac7e4a300bdf707a/20932ed527b6/edit) | pdf |
| Chapter 23 | [Area Data III](https://www.mentimeter.com/s/175ee004df6fb9452837023e02b2960b/96666c58d803/edit) | pdf |
| Chapter 25 | [Area Data IV](https://www.mentimeter.com/s/516dae79f2558cd948da3de61b1c2b54/b7bb868b80d0/edit) | pdf |
| Chapter 27 | [Area Data V](https://www.mentimeter.com/s/32ee96ef3aaf83559b779f3fb88fc209/341e94b74b69/edit) | pdf |
| Chapter 29 | [Area Data VI](https://www.mentimeter.com/s/13eade97c82235b94c73d6dec6ef34a7/10a4634c3a9d/edit) | pdf |
| Chapter 31 | [Spatially Continuous Data I](https://www.mentimeter.com/s/57b95c57c9a4b75e91d91adb8b6e5faa/330c2ca0d567/edit) | pdf |
| Chapter 33 | [Spatially Continuous Data II](https://www.mentimeter.com/s/b40aa86207d96711a40c73397bd36d08/f8248b9e8ecd/edit) | pdf |
| Chapter 35 | [Spatially Continuous Data III](https://www.mentimeter.com/s/d651523809c79353767df82bc7ba4d2f/d8e42a7811ed/edit) | pdf |
| Chapter 37 | [Spatially Continuous Data IV](https://www.mentimeter.com/s/78b3ec0313be43abe9995fe4c3447dd2/07a125804a15/edit) | pdf |

### Template repository for projects

I created a [template
repository](https://github.com/paezha/ES4GA3-Sample-Repository) to help
students get started with the use of GitHub and R Markdown for
collaborative work on term projects. In my own course adoption of this
workflow is completely optional. Not every student/group has the
inclination/time to adopt this approach, but those who do produce very
professional-looking reports and learn valuable skills.

### Examples of projects

These are examples of projects completed in this course:

- [Examining the Relationships Between Socioeconomic Variables and
  Particulate Air Pollution in the Toronto Metropolitan
  Area](https://github.com/paezha/Air-Pollution-Correlates-4GA3)  
- [Evaluating Effects of Population Demographics on Access to Sexual
  Health Care: A Toronto Case
  Study](https://github.com/paezha/Sexual-Health-Clinics-4GA3)  
- [Investigating Socio-Economic Disparities in the Damages Caused by
  Hurricane Katrina and Hurricane Rita in Southern Louisiana
  Counties](https://github.com/paezha/Hurricane-Damage-Lousiana-4GA3)  
- [The Effects of Income and Unemployment on Crime in
  Toronto](https://github.com/paezha/Crime-in-Toronto-4GA3)

## Contributing

An advantage of an Open Educational Resource compared to traditional
publishing (besides it being free!) is that it is a live, ongoing
project, for as long as anyone cares for it. If you are using this
resource, I would encourage you to contribute to improve it, by:

- suggesting improvements to the text, e.g. clarifying unclear
  sentences, fixing typos (see guidance from [Yihui
  Xie](https://yihui.name/en/2013/06/fix-typo-in-documentation/));
- proposing changes to the code, e.g. to do things in a more efficient
  way; and
- making requests to develop content (see the project’s [issue
  tracker](https://github.com/paezha/spatial-analysis-r/issues)).

<!-- Need to check what the style is
See [our-style.md](https://github.com/Robinlovelace/geocompr/blob/master/our-style.md) for the book's style.
&#10;-->

Many thanks to all contributors to the book so far via GitHub (this list
will update automatically): [soukhova](https://github.com/soukhova),
[Robinlovelace](https://github.com/Robinlovelace).

<!-- Need to figure out what this is
During the project we aim to contribute 'upstream' to the packages that make geocomputation with R possible.
This impact is recorded in [`our-impact.csv`](https://github.com/Robinlovelace/geocompr/blob/master/our-impact.csv).
-->
<!--
## Reproducing the book
&#10;To ease reproducibility, we created the `geocompkg` package.
Installing it from GitHub will install all the R packages needed build the book (you will a computer with necessary [system dependencies](https://github.com/r-spatial/sf#installing) and the [**remotes**](https://github.com/r-lib/remotes/) package installed):
&#10;
&#10;``` r
install.packages("remotes")
remotes::install_github("geocompr/geocompkg")
```
&#10;You need a recent version of the GDAL, GEOS, PROJ and UDUNITS libraries installed for this to work on Mac and Linux. See the **sf** package's [README](https://github.com/r-spatial/sf) for information on that.
&#10;Once the dependencies have been installed you should be able to build and view a local version the book with:
&#10;
``` r
bookdown::render_book("index.Rmd") # to build the book
browseURL("_book/index.html") # to view it
```
&#10;<!-- The code associated with each chapter is saved in the `code/chapters/` folder. -->
<!-- `source("code/chapters/07-transport.R")` runs run the code chunks in chapter 7, for example. -->
<!-- These R scripts are generated with the follow command which wraps `knitr::purl()`: -->
<!--
## The book in binder
&#10;I think I got the binder to work.
&#10;[![Launch Rstudio Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/paezha/spatial-analysis-r/main?urlpath=rstudio)
&#10;For many people the quickest way to get started with Geocomputation with R is in your web browser via Binder.
To see an interactive RStudio Server instance click on the following button, which will open [mybinder.org](https://mybinder.org/v2/gh/robinlovelace/geocompr/master?urlpath=rstudio) with an R installation that has all the dependencies needed to reproduce the book:
&#10;#You can also have a play with the repo in RStudio Cloud by clicking on this link (requires log-in):
&#10;
## The book in a Docker container
&#10;TODO
<!--
To ease reproducibility we have made Docker images available, at [geocompr/geocompr](https://hub.docker.com/r/geocompr/geocompr/) on DockerHub.
These images allow you to explore Geocomputation with R in a virtual machine that has up-to-date dependencies.
&#10;After you have [installed docker](https://www.docker.com/community-edition#/download) and set-it up on [your computer](https://docs.docker.com/install/linux/linux-postinstall/) you can start RStudio Server without a password (see the [Rocker project](https://www.rocker-project.org/use/managing_users/) for info on how to add a password and other security steps for public-facing servers):
&#10;```sh
docker run -p 8787:8787 -e DISABLE_AUTH=TRUE geocompr/geocompr
```
&#10;If it worked you should be able to open-up RStudio server by opening a browser and navigating to
http://localhost:8787/ resulting in an up-to-date version of R and RStudio running in a container.
&#10;Start a plain R session running:
&#10;```sh
docker run -it geocompr/geocompr R
```
&#10;See the [geocompr/docker](https://github.com/geocompr/docker#geocomputation-with-r-in-docker) repo for details, including how to share volumes between your computer and the Docker image, for using geographic R packages on your own data and for information on available tags.
&#10;## Reproducing this README
&#10;TODO
&#10;<!--
&#10;To reduce the book's dependencies, scripts to be run infrequently to generate input for the book are run on creation of this README.
&#10;The additional packages required for this can be installed as follows:
&#10;
``` r
source("code/extra-pkgs.R")
```
&#10;With these additional dependencies installed, you should be able to run the following scripts, which create content for the book, that we've removed from the main book build to reduce package dependencies and the book's build time:
&#10;
``` r
source("code/cranlogs.R")
source("code/sf-revdep.R")
source("code/08-urban-animation.R")
source("code/08-map-pkgs.R")
```
&#10;Note: the `.Rproj` file is configured to build a website not a single page.
To reproduce this [README](https://github.com/Robinlovelace/geocompr/blob/master/README.Rmd) use the following command:
&#10;
``` r
rmarkdown::render("README.Rmd", output_format = "github_document", output_file = "README.md")
```
&#10;
&#10;
&#10;<!-- ## Book statistics -->
<!-- An indication of the book's progress over time is illustrated below (to be updated roughly every week as the book progresses). -->
<!--
&#10;
&#10;
&#10;
<!-- Book statistics: estimated number of pages per chapter over time. -->
<!--
## Citations
-->
<!--
TODO
&#10;To cite packages used in this book we use code from [Efficient R Programming](https://csgillespie.github.io/efficientR/):
&#10;
``` r
# geocompkg:::generate_citations()
```
&#10;This generates .bib and .csv files containing the packages.
The current of packages used can be read-in as follows:
&#10;
``` r
#pkg_df = readr::read_csv("extdata/package_list.csv")
```
&#10;Other citations are stored online using Zotero.
&#10;If you would like to add to the references, please use Zotero, join the [open group](https://www.zotero.org/groups/418217/energy-and-transport) add your citation to the open [geocompr library](https://www.zotero.org/groups/418217/energy-and-transport/items/collectionKey/9K6FRP6N).
&#10;We use the following citation key format:
&#10;```
[auth:lower]_[veryshorttitle:lower]_[year]
```
&#10;This can be set from inside Zotero desktop with the Better Bibtex plugin installed (see [github.com/retorquere/zotero-better-bibtex](https://github.com/retorquere/zotero-better-bibtex)) by selecting the following menu options (with the shortcut `Alt+E` followed by `N`), and as illustrated in the figure below:
&#10;```
Edit > Preferences > Better Bibtex
```
&#10;![](figures/zotero-settings.png)
&#10;Zotero settings: these are useful if you want to add references.
&#10;We use Zotero because it is a powerful open source reference manager that integrates well with the **citr** package.
As described in the GitHub repo [Robinlovelace/rmarkdown-citr-demo](https://github.com/Robinlovelace/rmarkdown-citr-demo).
&#10;## References
&#10;
``` r
# remotes::install_github("gadenbuie/regexplain")
# regexplain::regexplain_file("extdata/package_list.csv")
#pattern = " \\[[^\\}]*\\]" # perl=TRUE
#pkg_df$Title = gsub(pattern = pattern, replacement = "", x = pkg_df$Title, perl = TRUE)
#knitr::kable(pkg_df)
```
&#10;-->
