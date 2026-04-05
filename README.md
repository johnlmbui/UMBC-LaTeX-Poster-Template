# UMBC LaTeX Poster Template

![](poster_pic.png)

**Note:** If using Overleaf, make sure to set the compiler to XeLatex or LuaLaTeX (Menu in the top left > Settings > Compiler).

## 8 Available Colors (see `demos/`)

### Primary

Gold, Black:

<p align="middle">
  <img align="top" src="demos/Gold.png" width="45%" />
  <img align="top" src="demos/Black.png" width="45%" />
</p>

### Secondary

Teal, Red:

<p align="middle">
  <img align="top" src="demos/Teal.png" width="45%" />
  <img align="top" src="demos/Red.png" width="45%" />
</p>

Light Gray, Dark Gray:

<p align="middle">
  <img align="top" src="demos/Light Gray.png" width="45%" />
  <img align="top" src="demos/Dark Gray.png" width="45%" />
</p>

White, Brown:

<p align="middle">
  <img align="top" src="demos/White.png" width="45%" />
  <img align="top" src="demos/Brown.png" width="45%" />
</p>


To change the color, go to `beamerthemestanford.sty` and change the `headline` color by (un)commenting the [relevant lines](https://github.com/RylanSchaeffer/Stanford-LaTeX-Poster-Template/blob/master/beamercolorthemestanford.sty#L44-L47):

- Black Text, Gold Banner: `\setbeamercolor{headline}{bg=umbcgold,fg=black}`
- Gold Text, Black Banner: `\setbeamercolor{headline}{bg=black,fg=umbcgold}`
- White Text, Teal Banner: `\setbeamercolor{headline}{bg=umbcaokteal,fg=white}`
- and so on.

## Contributing

Contributions are more than welcome! If you have a way to improve this poster, please pay it forward by opening a pull request and I'll add your improvement(s)

Thank you in advance :)
