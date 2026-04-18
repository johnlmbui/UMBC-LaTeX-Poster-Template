# UMBC LaTeX Poster Template
A modern LaTeX `beamerposter` template designed for research posters at the University of Maryland, Baltimore County (UMBC). This template is inspired by [Rylan Schaeffer](https://rylanschaeffer.github.io/)'s [Stanford LaTeX Poster Template](https://github.com/RylanSchaeffer/Stanford-LaTeX-Poster-Template).

Accessible on [Overleaf](https://www.overleaf.com/read/dmwdjvpbspcs#f175ae) (**Note:** On Overleaf, set the compiler to `XeLaTeX` or `LuaLaTeX` via *Menu -> Settings -> Compiler*).

---

## Features
- Themes (school colors, font style) aligned with the [UMBC Brand and Style Guide](https://styleguide.umbc.edu/)
- Built on the `beamerposter` class and fully customizable.
- Simple setup (compatible with Overleaf and local LaTeX editors)

---

## Poster Preview
![](poster.png)

---

## Setup Steps
### 1. Getting Started
You can access the project files in two ways: downloading and cloning. You can learn about cloning repositories [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).

To download, simply go to _$\color{green}{<> Code}$ -> Download ZIP_

```bash
git clone https://github.com/johnlmbui/UMBC-LaTeX-Poster-Template.git
cd UMBC-LaTeX-Poster-Template
```
### 2. Editing
Edit the main contents of your poster on `main.tex`.

### 3. Compiling
You can compile on Overleaf or whatever your favorite LaTeX editor is.

---

## Project Structure

```text
.
├── demos/                     # Examples of compiled posters
├── umbc_logos/                # UMBC logos and graphics
├── beamercolorthemeumbc.sty   # UMBC-themed colors
├── beamerthemeavenirnext.sty  # Avenir font files
├── beamerthemegemini.sty      # Gemini, a beamerposter theme (https://github.com/anishathalye/gemini/tree/master)
├── main.tex                   # Main poster file
├── poster.bib                 # Bibliography/references
└── README.md                  # What you're reading right now
```

---

## Theme Colors Preview (see `demos/`)

### Primary
Gold, Black
<p align="middle"> <img src="demos/Gold.png" width="45%" /> <img src="demos/Black.png" width="45%" /> </p>

### Secondary
Teal, Red
<p align="middle"> <img src="demos/Teal.png" width="45%" /> <img src="demos/Red.png" width="45%" /> </p>
Light Gray, Dark Gray
<p align="middle"> <img src="demos/Light_Gray.png" width="45%" /> <img src="demos/Dark_Gray.png" width="45%" /> </p>
White, Brown
<p align="middle"> <img src="demos/White.png" width="45%" /> <img src="demos/Brown.png" width="45%" /> </p>

---

## Changing the Theme Color
Navigate to `beamercolorthemeumbc.sty` and modify the `headline` color by (un)commenting the relevant lines:

- Gold Banner, Black Text:
```latex
\setbeamercolor{headline}{bg=umbcgold,fg=black}
```
- Black Banner, Gold Text:
```latex
\setbeamercolor{headline}{bg=black,fg=umbcgold}
```
- Teal Banner, White Text:
```latex
\setbeamercolor{headline}{bg=umbcaokteal,fg=white}
```
- And other combinations that are available in the file.

---

## Changing the Font
There exist fonts that are not readily available in standard TeX packages, and therefore must be installed separately. There is [Overleaf documentation](https://www.overleaf.com/learn/latex/Questions/I_have_a_custom_font_I%27d_like_to_load_to_my_document._How_can_I_do_this%3F) on how to load custom font files, but feel free to use different editors or configurations. I personally use [MacTeX](https://www.tug.org/mactex/) for macOS and [TeXstudio](https://www.texstudio.org/) for Windows. This project defaults to using the `beamerthemegemini.sty`, as it is forked from https://github.com/anishathalye/gemini and is intended to work “out of the box.”

### The Avenir Font Family
**Avenir Next** is the primary font used in UMBC publications. Therein  `fonts/` contains three `.ttc` files:
- `Avenir.ttc`
- `Avenir Next.ttc`
- `Avenir Next Condensed.ttc`

#### macOS
These font files come preinstalled in Font Book. In `main.tex`, change `\usetheme{gemini}` to `\usetheme{avenirnext}`.
#### Windows 10/11
Open Font settings and drag the font files into its window to install them. Then follow the same step above.
#### Linux 
I am less familiar with the exact steps for Linux, but there are many guides and resources available online. You are encouraged to look up instructions specific to your distribution.


### How `beamertheme[font_name].sty` Works
```latex
% ====================
% Fonts
% ====================

\newfontfamily\AvenirNext{Avenir Next}[Ligatures=TeX]

\usefonttheme{professionalfonts}

\setsansfont{Avenir Next}[
  Ligatures=TeX,
  UprightFont    = {Avenir Next Regular},
  ItalicFont     = {Avenir Next Italic},
  BoldFont       = {Avenir Next Bold},
  BoldItalicFont = {Avenir Next Bold Italic}
]

\setbeamerfont{headline}{family=\AvenirNext}
\setbeamerfont{headline title}{size=\Huge,series=\bfseries}
\setbeamerfont{headline author}{size=\Large}
\setbeamerfont{headline institute}{size=\normalsize}
\setbeamerfont{block title}{family=\AvenirNext,size=\large,series=\bfseries}
\setbeamerfont{heading}{family=\AvenirNext,series=\bfseries}
\setbeamerfont{caption}{size=\small}
\setbeamerfont{footline}{family=\AvenirNext,size=\normalsize}

```
This code block is from the style file `beamerthemeavenirnext.sty`, which sets the font to Avenir Next. You are encouraged to edit existing style files or add your own. The world is your oyster.

---

## Contributions
If you have suggestions for improvement, you're more than welcome to open an issue or submit a pull request!
