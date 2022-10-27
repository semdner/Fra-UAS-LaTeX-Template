# Frankfurt University of Applied Sciences: LaTeX Template
A LaTeX template for scientific essays based on [Handreichung: Wissenschafftliche Arbeiten](https://www.yumpu.com/de/document/read/31685236/handreichung-wissenschaftliche-arbeiten-elearning-der-fh-) by Prof. Dr. Alexandra Caspari for Frankfurt University of Applied Sciences.

### Project Structure

To use this template, download this repository. The `README.md` file can be deleted because the actual LaTeX template is contained in the `src` folder. Replace the `src` folder name with any name, such as the name of your essay. The structure of `src` the the following

```
/src
  main.tex
  main.pdf
  /sections
     titlepage.tex
  /graphics
```

The file`main.tex` contains the document structure as well as references to all section of the essay. The pdf-file `main.pdf` is the generated pdf (your essay). It will be overwritten everytime you generate the document new. The folder `sections` contains your individual sections. (By default it contains the file `example.tex` which can be deleted. The reference to this file must be removed in the `main.tex`). Your sections can be included in the main file.(see the `include section` section under `Usage` down below). The folder `graphics` contains images you want to add in your text.

### Document Structure

#### Paper and Page Orientation

<u>Format:</u>

DIN A4, one-sided

<u>Margins</u>

- left: 3cm
- right: 2cm (2.5 if no header is used)
- top: 2.5cm
- bottom: 2cm

#### Font and Typesetting

<u>Font:</u> 

Computer Modern (Handreichung: Wissenschaftliche Arbeiten recommends Times New Roman)

<u>Font-Size:</u>

12pt

<u>Line-Spacing:</u>

Default line spacing of LaTeX was used (Handreichung: Wissenschaftliche Arbeiten recommends 1.5 lines which is equivalent to 18pt)

<u>Line Alignment:</u>

Justified

#### Footnotes

The footnote settings have been left at the LaTeX default settings, as they correlate with the specifications from Handreichung: Wissenschaftliche Arbeiten, with the exception of the font.

### Usage

<u>Include Sections:</u>

Sections can be added under `src/sections` as `.tex` files. To include them in your document open `main.tex` and use the `\include` command.

```tex
\begin{document} % specifies begin of document
% ...

\include{sections/titlepage.tex} the titlepage

\tableofcontents % generates a table of contents of the sections down below

\include{sections/yourfile.tex}

%...
\begin{document} % specified end of document
```

<u>Code Blocks:</u>

```tex
\begin{lstlisting}[language=YourLanguage]
% your code here
\end{lstlisting}
```

In the `main.tex` colors, line numbers and other settings can be changed.

<u>Footnotes:</u>

Footnotes can be added to the the text via `\footnote{footnote content}`. By default, latex uses a size of 10pt, generates it in single lines and numbers it across the document.

<u>Word Highlighting:</u>

- *cursive*: emphasis on individual words
- simple quotation marks: highlighting of special words or single specific terms
- **bold**: emphasis on individual words (should be avoided)
- S p a c e d  W r i t i n g, CAPITALIZATION and <u>underlining</u> and should be avoided.









