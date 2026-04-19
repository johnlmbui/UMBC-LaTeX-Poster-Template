# UMBC LaTeX Poster Template
A modern LaTeX `beamerposter` template designed for research posters at the University of Maryland, Baltimore County (UMBC). This template is inspired by [Rylan Schaeffer](https://rylanschaeffer.github.io/)'s [Stanford LaTeX Poster Template](https://github.com/RylanSchaeffer/Stanford-LaTeX-Poster-Template).

---

## Poster Preview
![](poster.png)

---

## Features
- Preconfigured themes, fonts, and logos aligned with the [UMBC Brand and Style Guide](https://styleguide.umbc.edu/)
  - Also easily customizable to fit your needs. The world (or at least this poster) is your oyster!
- Works out-of-the-box with minimal setup
- Compatible with [Overleaf](https://www.overleaf.com/read/dmwdjvpbspcs#f175ae) and local LaTeX environments, including:
  - [TeXstudio](https://www.texstudio.org/)
  - [VS Code](https://code.visualstudio.com/)
  - [MacTeX](https://www.tug.org/mactex/) (macOS)

---

## Quick Start
1. Download ZIP, or [clone the repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
2. Open `main.tex` to edit contents
3. Set compiler to **XeLaTex** or **LuaLaTeX** on Overleaf (Menu -> Settings -> Compiler) or whatever your favorite editor is, and compile

---

## Main Project Structure

```md
.
├── fonts/                     # Avenir font family files
├── umbc_logos/                # UMBC logos and graphics
├── beamercolorthemeumbc.sty   # UMBC color theme
├── beamerthemeavenirnext.sty  # Avenir Next font theme (UMBC standard)
├── beamerthemegemini.sty      # Gemini, default font theme
├── main.tex                   # Main poster file
└── poster.bib                 # Bibliography/references
```

---

## Color Themes Preview (see `demos/`)

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

## Changing Theme Color
To modify the color theme, open `beamercolorthemeumbc.sty` and adjust the `headline` color by (un)commenting the desired configuration:

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
- Additional color combinations can be defined in the file by adding or redefining RGB values:
```latex
\definecolor{color_name}{RGB}{RRR, GGG, BBB}
```

---

## The Avenir Font Family

**Avenir Next** is the primary font used in UMBC publications. It is not included in standard TeX distributions and must be installed separately. The `fonts/` directory contains:

- `Avenir.ttc`
- `Avenir Next.ttc`
- `Avenir Next Condensed.ttc`

Refer to this [Overleaf documentation](https://www.overleaf.com/learn/latex/Questions/I_have_a_custom_font_I%27d_like_to_load_to_my_document._How_can_I_do_this%3F) for guidance on loading custom fonts, but you may use any LaTeX editor or setup you prefer.

## Changing the Font

This project uses `beamerthemegemini.sty` by default (forked from https://github.com/anishathalye/gemini).

To use Avenir Next, update `main.tex` by changing `\usetheme{gemini}` to `\usetheme{avenirnext}`.

Font installation varies by operating system. Refer to the appropriate instructions below or system-specific documentation for installing custom fonts:

#### macOS
These font files are typically preinstalled and available through *Font Book*.

#### Windows 10/11
Open *Font settings* and drag the font files into the window to install them.

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

This code block is from the style file `beamerthemeavenirnext.sty`, which sets the font to Avenir Next. You are encouraged to edit existing style files or add your own.
---

## Contributions
If you have suggestions for improvement, you're more than welcome to open an issue or submit a pull request!
