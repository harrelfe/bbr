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
In what follows `chapterbasename` usually refers to the prefix of
`.qmd` in the chapter's file name.

* Figures

   ```{r}
   #| label: fig-chapterbasename-figurelabel
   #| fig-cap: "This is a long caption for the figure ..."
   #| fig-scap: "This is a short caption for the table of figures ..."
   #| fig-height: (inches)
   #| fig-width: (inches)
   ... base, ggplot2, or plotly graphic commands ...
   ```
   
* Section label: `## ... {#sec-chapterbasename-sectionname}`
* Drill-down collapsed text:

```
::: {.callout-note collapse="true"}
. . . .

:::
```

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
. . . stuff here . . .
(blank line)
:::
(blank line)
```


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

# Compilation
It's probably best to compile individual chapters and not recompile
the whole book.  E.g. use from the command line `quarto render
chaptername.qmd` or click on `Render` in `RStudio`.  If recompiling
the chapter changed or added figures, the table if figures will need
to be updated by running `quarto render figures.qmd`.

The resulting `html` files will be in the `_book` directory underneath
the `bbr` directory.  The `.gitignore` files in `bbr` will keep these
from being put on `Github`.  To update the web site `hbiostat.org/bbr`
Frank will have to compile changed chapters on his machine, which he
will do when others change and commit chapter `.qmd` files.

