# First

Read the malliopas.tex.  If you are not to develop this class, use download button, not clone.

Lue ensin malliopas.tex.  Se auttaa sinua oppimaan LaTeXin ja kandi/gradupohjan käyttöä.
Jos et aio kehittää LaTeX-luokkaa eteenpäin, käytä yllä olevaa latausnapikkaa, älä turhaan kloonaa projektia.

Wiki tuossa vasemmalla tulee myöhemmin sisältämään hyödyllistä tietoa latexin ja tutkielmapohjan käytöstä.

# Software you'll need:
* A LaTeX driver program such as `lualatex` or `xelatex` (recommended) or else
  the older `pdflatex`
* The `biber` bibliography processing backend
* Various LaTeX packages

These are all included in a TeX distribution such as [TeX
Live](https://www.tug.org/texlive/).

# Build using `latexmk`

Simply use the following to watch the your tex file and continually compile it with preview:

```
latexmk -pvc somefile
```

See [`man latexmk`](https://manpages.org/latexmk) for how to configure the
driver program and PDF viewer.

# Manual build:

```
$ latex somefile.tex
$ biber somefile # if somefile.bib is your bibliography
$ latex somefile.tex
$ latex somefile.tex
```
