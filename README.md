# Frankfurt University of Applied Sciences: LaTeX Template

This LaTeX paper template is intended for students and researchers of the Frankfurt University of Applied Sciences who wish to write essays in LaTeX. It includes two folders, `src_de` for the German version and `src_eng` for the English version. The document structure is partly based on [Handreichung: Wissenschafftliche Arbeiten](https://www.yumpu.com/de/document/read/31685236/handreichung-wissenschaftliche-arbeiten-elearning-der-fh-) by Prof. Dr. Alexandra Caspari for students of Frankfurt University of Applied Sciences.

## Project Structure

To use this template, download this repository. The `README.md` file can be deleted because the actual LaTeX template is contained in the `src` folder. Replace the `src` folder name with any name, such as the name of your essay. The structure of `src` the the following:

```bash
├── src_de
│   ├── graphics
│   ├── sections
│   │   └── 0_information
│   │       ├── abstract.tex
│   │       ├── declaration_of_authorship.tex
│   │       └── titlepage.tex
│   ├── main.tex
│   ├── references.bib
│   └── main.pdf
└── src_eng
    ├── graphics
    ├── sections
    │   └── 0_information
    │       ├── abstract.tex
    │       ├── declaration_of_authorship.tex
    │       └── titlepage.tex
    ├── main.tex
    ├── references.bib
    └── main.pdf
```

`src_de` and `src_eng`:
- `graphics`: Insert your graphics and figures here 
- `sections`: This folder contains sections of the paper. Add your sections here.
  - `0_information`: This subfolder contains general files for the paper.
    - `abstract.tex`: Replace the dummy text with your abstract.
    - `declaration_of_authorship.tex`: Contains the declaration of authorship. Replace your name here.
    - `titlepage.tex`: Replace the course information, personal information, title and subtitle.
- `main.tex`: This is the main file for inserting text and sections.
- `references.bib`: Insert your references here file contains the references for the paper using BibTeX.
- `main.pdf`: The final generated PDF file.

## Usage

Clone this repository to your local machine. Navigate to either the `src_de` or `src_eng` folder, depending on which language you prefer to write your paper in. Use a LaTeX editor to modify the files as necessary. Compile the main.tex file to generate the final PDF document.


**Include Sections:**

Sections can be added under `src/sections` as `.tex` files. It is recommended to create a subfolder for each section you create and place subsections in it. Here an example:

```css
└── sections
    ├── 0_information
    │   ├── abstract.tex
    │   ├── declaration_of_authorship.tex
    │   └── titlepage.tex
    └── 1_section_example
        ├── 1_subsection.tex
        ├── 2_subsection.tex
        └── 3_subsection.tex
```

To include them in your document open `main.tex` and use the `\include` or `\input` command. The markers `%=== Your Text ===%` and `%=================%` where set. Place your sections within those markers.

```tex
\begin{document} % specifies begin of document
% ...

%=== Your Text ===%

\include{sections/1_section/1_subsection.tex}

\include{sections/1_section/2_subsection.tex}

\include{sections/1_section/3_subsection.tex}

%=================%

%...
\begin{document} % specified end of document
```

**Code Blocks:**

To add code predefined listings are included. Here an example usage:

```tex
\begin{lstlisting}[language=programming_language]
% your code here
\end{lstlisting}
```

In the `main.tex` colors, line numbers and other settings can be changed. 

**Recommended Word Highlighting:**

- *cursive*: emphasis on individual words
- **bold**: emphasis on individual words (should be avoided)
- S p a c e d  W r i t i n g, CAPITALIZATION and <u>underlining</u> should be avoided.

## Contribution

Contributions are welcome to improve this template. Please fork this repository and submit a pull request with your changes. 

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.