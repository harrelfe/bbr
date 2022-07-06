# Figure Captions

`_quarto.yml` specifies that captions are placed in the margins.  This
works well except when specifying `yaml` in specific chunks that makes
multiple columns of graphics.  These may appear as multiple rows, and
if you use sub captions they will appear in the margin instead of
under each panel.  So `fig-cap-location` in a chunk is ignored if
`margin` is specified in the book-wide `yaml`.  See
[this](https://github.com/quarto-dev/quarto-cli/discussions/1172) for
more information.

This problem will be fixed in `Quarto` 1.1 around 2022-08.  Then the
following figures can be improved using subcaptions:
* reg: 10.5 10.6
* ancova: 13.4, 13.5
* info: 18.2

# General To-Do

