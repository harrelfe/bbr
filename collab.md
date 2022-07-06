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

  
