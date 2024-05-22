# Lue ensin / First

[![en](https://img.shields.io/badge/lang-en-red.svg)](README.en.md)
[![es](https://img.shields.io/badge/lang-es-yellow.svg)](README.es.md)

*Lue* ensin `malliopas.tex`.  Se auttaa sinua oppimaan LaTeXin ja kandi/gradupohjan käyttöä.
Jos et aio kehittää LaTeX-luokkaa eteenpäin, käytä yllä olevaa latausnapikkaa, älä turhaan kloonaa projektia.

Start off by reading `enthesis.tex`, which includes various information on using this template, LaTeX, and writing a thesis in general.
If you are not to developing this class, you can use the download button instead of cloning.

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

# Accessibility / Saavutettavuus

Making content accessible [is part of the law in Finland](https://www.finlex.fi/fi/laki/alkup/2019/20190306).
One of the most prominent e-print repositories, arXiv, [recommends making LaTeX documents by exporting to HTML](https://info.arxiv.org/about/accessible_HTML.html).
However, the JYU Open Science Center has chosen not to support this approach.
According [to their guidance](https://openscience.jyu.fi/en/thesis-tutorial/bachelors-masters-thesis/publishing-your-thesis/thesis-accessibility), they have chosen to support tagged PDF, a which has only more recently received widespread support in PDFs.
LaTeX support for tagged PDF is still experimental.
However, if you have access to a new enough version of LaTeX (TeXLive 2024+) you can compile and follow the instructions in `accessibility.tex` to add these features to your document.

Sisällön saavutettavuuden varmistaminen [on osa Suomen lakia] (https://www.finlex.fi/fi/laki/alkup/2019/20190306).
Yksi tunnetuimmista sähköisen tulostuksen arkistoista, arXiv, [suosittelee LaTeX-dokumenttien tekemistä viemällä ne HTML-muotoon](https://info.arxiv.org/about/accessible_HTML.html).
JYU Open Science Center ei kuitenkaan ole päättänyt tukea tätä lähestymistapaa.
[Ohjeidensa mukaan](https://openscience.jyu.fi/en/thesis-tutorial/bachelors-masters-thesis/publishing-your-thesis/thesis-accessibility) he ovat päättäneet tukea tagged PDF:ää, joka on vasta viime aikoina saanut laajaa tukea PDF-tiedostoissa.
LaTeXin tuki tagged PDF:lle on vielä kokeellinen.
Jos sinulla on kuitenkin käytössäsi tarpeeksi uusi LaTeX-versio, (TeXLive 2024+) voit kääntää sen ja lisätä nämä ominaisuudet dokumenttiisi noudattamalla `accessibility.texissä` annettuja ohjeita.

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
