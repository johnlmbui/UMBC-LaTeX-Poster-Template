# UMBC LaTeX Poster Template

Accessible on [Overleaf](https://www.overleaf.com/read/dmwdjvpbspcs#f175ae) (**Note:** On Overleaf, set the compiler to XeLatex or LuaLaTeX by going to Settings > Compiler).

![](poster_pic.png)

## 8 Colors (see `demos/`)

### Primary

Gold, Black

<p align="middle">
  <img align="top" src="demos/Gold.png" width="45%" />
  <img align="top" src="demos/Black.png" width="45%" />
</p>

### Secondary

Teal, Red

<p align="middle">
  <img align="top" src="demos/Teal.png" width="45%" />
  <img align="top" src="demos/Red.png" width="45%" />
</p>

Light Gray, Dark Gray

<p align="middle">
  <img align="top" src="demos/Light_Gray.png" width="45%" />
  <img align="top" src="demos/Dark_Gray.png" width="45%" />
</p>

White, Brown

<p align="middle">
  <img align="top" src="demos/White.png" width="45%" />
  <img align="top" src="demos/Brown.png" width="45%" />
</p>

## Changing Theme Color

Go to `beamerthemestanford.sty` and change the `headline` color by (un)commenting the [relevant lines](https://github.com/johnlmbui/UMBC-LaTeX-Poster-Template/blob/master/beamercolorthemeumbc.sty#L54-61):

- Black Text, Gold Banner: `\setbeamercolor{headline}{bg=umbcgold,fg=black}`,
- Gold Text, Black Banner: `\setbeamercolor{headline}{bg=black,fg=umbcgold}`,
- White Text, Teal Banner: `\setbeamercolor{headline}{bg=umbcaokteal,fg=white}`,
- and so on.

## Contributing

Contributions are more than welcome! If you have a way to improve this poster, please pay it forward by opening a pull request and I'll add your improvement(s)

Thank you in advance :)
