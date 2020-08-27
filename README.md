# masterfrontpage
The LaTeX package `masterfrontpage` is used to generate official front pages
for master's theses at the Department of Mathematics at the University of Oslo.

The cover illustration is a section of the root system of the exceptional [Lie group E8](https://en.wikipedia.org/wiki/E8_(mathematics)).

[![Link to example PDF](https://i.imgur.com/FSEEyTN.png)](https://www.duo.uio.no/bitstream/handle/10852/51942/Helso-master.pdf)

## Title page
The package `masterfrontpage` collects information from the commands 
* `\author{...}`,
* `\title{...}`,
* `\subtitle{...}`.

The front page itself is produced with the command `\masterfrontpage`.
It is optional to use `\subtitle{...}`.

Use one of the package options `LongTitle` or `ExtraLongTitle`
if there is not enough room for your title.

If the layout comes out wrong the first time,
then recompile.

## Colophon
Following the title page,
`masterfrontpage` prints a short text with information about your study programme
and the scope of the thesis.
The programme is specified with one of the package options
* `MAT` — *Mathematics*, Mathematics;
* `MFA` — *Mathematics for applications*, Mathematics;
* `MEK` — *Mechanics*, Mechanics;
* `FFR` — *Finance, Insurance and Risk*, Stochastic Modelling, Statistics and Risk Analysis;
* `STK` — *Statistics*, Stochastic Modelling, Statistics and Risk Analysis;
* `DS` — *Data Science*, Data Science;
* `CSMEK` — *Mechanics*, Computational Science;
* `AMRA` — *Applied Mathematics and Risk Analysis*, Computational Science;
* `LEKMAT` — *Mathematics*, Lektorprogrammet;
* `LEKMEK` — *Mechanics*, Lektorprogrammet;
* `OLDFFR` — *Finance, Insurance and Risk*, Modelling and Data Analysis (Discontinued);
* `SDATA` — *Statistics and Data Analysis*, Modelling and Data Analysis (Discontinued);
* `CS` — *Computational Science*, Computational Science and Engineering (Discontinued);
* `OLDMEK` — *Mechanics*, Computational Science and Engineering (Discontinued).

The discontinued study programmes no longer accept new students;
they are not discontinued by `masterfrontpage`.

The scope of the thesis in terms of credits
is specified with one of the package options `30` or `60`.

## Print or web edition
By default,
`masterfrontpage` will produce a front page fitted for viewing on a screen.
When printing at the University Print Centre (Reprosentralen),
a card stock rim will be added,
which steals some of the left margin.
In order to compensate for this,
we recommend using the option `print` before submitting the file for printing.
This shifts the logo, seal and text to the right.

## Language
Choice of language will influence the university's logo,
the words "Master's Thesis" and the colophon.
Language is preferably given as a document class option.
The package recognises the following language options:
`american`, `english`, `UKenglish`, `USenglish`, `norsk` and `nynorsk`.
If none of these are given,
`english` is chosen by default.

## Date
The date can if necessary be overwritten
with the TeX primitives `\year = yyyy` and `\month = mm`
before `masterfrontpage` is imported.

## Compiler
If compiling with `xelatex`,
the white banner will not be transparent.
Both `pdflatex` and `lualatex` work.

## Example
```latex
\documentclass[a4paper]{memoir}

\usepackage[AMRA, 30]{masterfrontpage}

\title{Title}
\subtitle{Optional subtitle}
\author{Author's name}

\begin{document}
    \masterfrontpage
\end{document}
```
