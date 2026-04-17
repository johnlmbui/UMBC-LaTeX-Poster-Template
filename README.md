# UMBC LaTeX Poster Template
A modern LaTeX `beamerposter` template designed for research posters at the University of Maryland, Baltimore County (UMBC). This template is inspired by [Rylan Schaeffer](https://rylanschaeffer.github.io/)'s [Stanford LaTeX Poster Template](https://github.com/RylanSchaeffer/Stanford-LaTeX-Poster-Template).

Accessible on [Overleaf](https://www.overleaf.com/read/dmwdjvpbspcs#f175ae) (**Note:** On Overleaf, set the compiler to `XeLaTeX` or `LuaLaTeX` via *Menu -> Settings -> Compiler*).

---

## Features
- Color themes and layout components aligned with the [UMBC Brand and Style Guide](https://styleguide.umbc.edu/)
  - 
- Built on the `beamerposter` class
- Modular structure for easy editing and customization (e.g., departments, conferences, personal use)
- Simple setup (compatible with Overleaf and local LaTeX)

---

## Poster Preview
![](poster.png)

---

## How to Get Started
### 1. Clone the repository
```bash
git clone https://github.com/johnlmbui/UMBC-LaTeX-Poster-Template.git
cd UMBC-LaTeX-Poster-Template
```
### 2. Open the template
Edit the `main.tex` file to add your content:
- Title
- Authors and affiliations
- Sections (Introduction, Methods, Results, etc.)
### 3. Compile the poster
You can compile using:
- Overleaf
- Local LaTeX installation:
```bash
xelatex main.tex
```

---

## Project Structure

```text
.
├── demos/                     # Examples of compiled posters
├── umbc_logos/                # UMBC logos and graphics
├── beamercolorthemeumbc.sty   # UMBC-themed colors
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

## Changing the Font (Avenir Next)
**Note:** Avenir Next is the primary font used in UMBC publications; however, it is not available in standard TeX packages and must be installed separately. This may also require using different editors or configurations. I personally use [MacTeX](https://www.tug.org/mactex/) for macOS and [TeXstudio](https://www.texstudio.org/) for Windows, but feel free to explore alternatives such as VS Code or other editors. This project defaults to using the `beamerthemegemini.sty`, as it is forked from https://github.com/anishathalye/gemini and is intended to work “out of the box.”

### `fonts/`
Contains three `.ttc` files:
- `Avenir.ttc`
- `Avenir Next.ttc`
- `Avenir Next Condensed.ttc`

### macOS
These fonts are already preinstalled in Font Book. In `main.tex`, change `\usetheme{gemini}` to `\usetheme{avenirnext}`.
### Windows 10/11
Open Font settings and drag the font files into the window to install them. Then follow the same step above.
### Linux 
I am less familiar with the exact steps for Linux, but there are many guides and resources available online. You are encouraged to look up instructions specific to your distribution.

Customization and documentation can also extend to other fonts that are not included in standard LaTeX packages, depending on your system and setup.

---

## Contributions
If you have suggestions for improvement, you're more than welcome to open an issue or submit a pull request!
