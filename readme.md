# Lue ensin / First

*Read* the `malliopas.tex`.  If you are not to develop this class, use download button, not clone.

*Lue* ensin `malliopas.tex`.  Se auttaa sinua oppimaan LaTeXin ja kandi/gradupohjan käyttöä.
Jos et aio kehittää LaTeX-luokkaa eteenpäin, käytä yllä olevaa latausnapikkaa, älä turhaan kloonaa projektia.

Wiki tuossa vasemmalla tulee myöhemmin sisältämään hyödyllistä tietoa latexin ja tutkielmapohjan käytöstä.

Wiki on the left will contain useful information.

# Tarvittavat ohjelmistot / Software you'll need:
* Joku LaTeX-toteutus, esim: / A LaTeX driver program such as:
  - `lualatex`
  - `xelatex`
  - `pdflatex`
* `biber`  kirjallisuusviitteiden hallintaan / bibliography processing backend
* Joitain LaTeX-paketteja / Various LaTeX packages

Nämä löytyvät yleensä LaTeX-järjestelmästä kuten \
[TeX Live](https://www.tug.org/texlive/) \
or a similar TeX distribution usually includes these.

# Dokumentin tuottaminen / Build automatically

Dokumentin voi tex-lähdetiedostosta tuottaa ja esikatsella automaattisesti komennolla

```
latexmk -pvc somefile
```

is used to watch the your tex file and continually compile it with preview.

See [`man latexmk`](https://manpages.org/latexmk) for how to configure the
driver program and PDF viewer.

Komennolla [`man latexmk`](https://manpages.org/latexmk) voit lukea lisää
ohjeita `latexmk`-ohjelman käytöstä ja konfiguroinnista.


# Dokumentin tuottaminen käsin / Manual build:

```
$ latex somefile.tex
$ biber somefile # if somefile.bib is your bibliography
$ latex somefile.tex
$ latex somefile.tex
```
