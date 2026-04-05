# UMBC LaTeX Poster Template

A clean, modern, and customizable LaTeX **beamerposter** template designed for academic posters at the University of Maryland, Baltimore County (UMBC). This template is inspired by [Rylan Schaeffer](https://rylanschaeffer.github.io/)'s [Stanford LaTeX Poster Template](https://github.com/RylanSchaeffer/Stanford-LaTeX-Poster-Template) and adapted to align with UMBC branding and presentation standards, adhering to the [UMBC Brand and Style Guide](https://styleguide.umbc.edu/).

Accessible on [Overleaf](https://www.overleaf.com/read/dmwdjvpbspcs#f175ae)  
(**Note:** On Overleaf, set the compiler to **XeLaTeX** or **LuaLaTeX** via *Menu → Settings → Compiler*.)

---

## ✨ Features

- 🎓 **UMBC-branded design** aligned with official university guidelines  
- 🎯 **Adheres to the UMBC Style Guide** (colors, typography, and layout principles)  
- 🧩 **Modular structure** for easy editing and reuse  
- 🎨 **Clean and professional layout** suitable for research presentations  
- ⚡ **Minimal setup** — get started quickly with LaTeX  
- 📐 **Beamerposter-based**, making it flexible and widely supported  
- 🔧 Easily customizable for:
  - Different departments  
  - Conferences and symposiums  
  - Personal branding tweaks  

---

## 📸 Preview

![](poster_pic.png)

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/johnlmbui/UMBC-LaTeX-Poster-Template.git
cd UMBC-LaTeX-Poster-Template
```

### 2. Open the template
Edit the 'main.tex' file to add your content:
- Title
- Authors and affiliations
- Sections (Introduction, Methods, Results, etc.)

### 3. Compile the poster
You can compile using:
- Overleaf (recommended for beginners)
- Local LaTeX installation:
```bash
xelatex poster.tex
```

---

🧱 Project Structure

.
├── main.tex                # Main poster file
├── beamercolorthemeumbc.sty # Custom UMBC color theme
├── umbc_logos/                   # UMBC logos and graphics
└── README.md

---

## 🎨 Color Themes (see `demos/`)

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

## 🎛️ Changing the Theme Color

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

- Additional combinations are available in the file.

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for improvements, feel free to open an issue or submit a pull request.

Thank you in advance 🙂
