# Types of New Material

## Changes to Commit Straight to Github
* Corrections and clarifications
* New topic in existing chapter
* New drill-down material that defaults to be collapsed

## Changes to Discuss First
* New chapter
* New material that makes it logical to convert old material to
  drill-down collapsed text

# Conventions to Follow
* Drill-down collapsed text:

```
::: {.callout-note collapse="true"}
. . . .

:::
```

* Section label: `... {#sec-chapterfilenameprefix-sectionname}`
* Figure label: `#| label: fig-chapterfilenameprefix-figname}`

# New Bibliographic References
* Send the link to the publication to Frank who will add to Zotero
  then download into an updated harrelfe.bib

# Overall Suggestions
* Make ample use of `mermaid` diagrams to illustrate concepts, using
  the `Quarto` built-in markdown for `mermaid` as seen in `index.qmd`
* Make ample use of marginal notes.  Small notes that don't need to
  show any code or formatted output are best created using `[... note
  ...]{.aside}` whereas longer notes or ones requiring formatting are
  best produced with:
  
```
::: {.column-margin}
. . .

:::


# R Packages Needed
To be able to run all the examples in the entire book you will need to
install the following R packages:

* Hmisc
* rms
* data.table
* gpplot2
* mvtnorm (for corr.qmd)
* lattice (for descript.qmd, info.qmd)
* brms (htest.qmd, prop.qmd)
* pwr (htest.qmd)
* nlme (serial.qmd)
* rmsb (serial.qmd)
* kableExtra

Don't use `tidyverse` (e.g., `dplyr`) in any R code.  It is messy and has too many
dependencies, and sometimes conflicts with `Hmisc`.
