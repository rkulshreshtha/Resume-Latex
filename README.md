# Resume in LaTeX

This repository contains my resume written in LaTeX (`rkulshreshtha_resume.tex`).

## How to Compile to PDF

The resume uses the `fontspec` package to load the system font **Arial**, which means it requires a Unicode-aware LaTeX engine like **XeLaTeX**, **LuaLaTeX**, or **Tectonic** rather than standard `pdflatex`.

### Option 1: Using XeLaTeX (Standard TeX Live / MacTeX)
If you have a standard LaTeX distribution installed, you can compile the resume from the terminal by running:

```bash
xelatex rkulshreshtha_resume.tex
```
*(You may need to run this command twice to ensure the layout and hyperlinks are fully resolved.)*

### Option 2: Using Tectonic (Fastest Setup)
[Tectonic](https://tectonic-typesetting.github.io/) is a modern, self-contained LaTeX engine that downloads required packages on the fly. 

If you are on macOS, you can install it via Homebrew:
```bash
brew install tectonic
```

Then, simply run:
```bash
tectonic rkulshreshtha_resume.tex
```
This will automatically handle all package dependencies and output the compiled `rkulshreshtha_resume.pdf` file.
