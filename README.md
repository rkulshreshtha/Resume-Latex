# Resume in LaTeX

This repository contains my resume source files written in LaTeX, configured with automated compilation via GitHub Actions.

---

## Resume Variants & Downloads

The compiled PDFs for all versions are automatically generated and maintained in the [`resume`](https://github.com/rkulshreshtha/Resume-Latex/tree/resume) branch:

| Variant | Source TeX File | Description | Download PDF |
| :--- | :--- | :--- | :--- |
| **Master Resume** | [`rkulshreshtha_resume.tex`](rkulshreshtha_resume.tex) | Master comprehensive resume used with AI & job descriptions to generate role-tailored CVs | [Download PDF](https://github.com/rkulshreshtha/Resume-Latex/raw/resume/rkulshreshtha_resume.pdf) |
| **EM (1-Page, Relocation)** | [`rkulshreshtha_resume_EM_1page.tex`](rkulshreshtha_resume_EM_1page.tex) | 1-page CV targeting Engineering Manager roles (includes open to relocation info at the top) | [Download PDF](https://github.com/rkulshreshtha/Resume-Latex/raw/resume/rkulshreshtha_resume_EM_1page.pdf) |
| **EM (2-Page, Relocation)** | [`rkulshreshtha_resume_EM_2page.tex`](rkulshreshtha_resume_EM_2page.tex) | 2-page CV targeting Engineering Manager roles (includes open to relocation info at the top) | [Download PDF](https://github.com/rkulshreshtha/Resume-Latex/raw/resume/rkulshreshtha_resume_EM_2page.pdf) |
| **EM (1-Page, BLR)** | [`rkulshreshtha_resume_EM_1page_BLR.tex`](rkulshreshtha_resume_EM_1page_BLR.tex) | 1-page CV targeting Engineering Manager roles in Bangalore (BLR only, no relocation info) | [Download PDF](https://github.com/rkulshreshtha/Resume-Latex/raw/resume/rkulshreshtha_resume_EM_1page_BLR.pdf) |
| **EM (2-Page, BLR)** | [`rkulshreshtha_resume_EM_2page_BLR.tex`](rkulshreshtha_resume_EM_2page_BLR.tex) | 2-page CV targeting Engineering Manager roles in Bangalore (BLR only, no relocation info) | [Download PDF](https://github.com/rkulshreshtha/Resume-Latex/raw/resume/rkulshreshtha_resume_EM_2page_BLR.pdf) |

---

## How to Compile Locally

These resumes use the `fontspec` package to load the system font **Arial**, requiring a Unicode-aware LaTeX engine such as **XeLaTeX**, **LuaLaTeX**, or **Tectonic** rather than standard `pdflatex`.

### Option 1: Using XeLaTeX (Standard TeX Live / MacTeX)
Run the following from your terminal (running twice ensures hyperlinks and layout alignment are fully resolved):

```bash
xelatex <filename>.tex
xelatex <filename>.tex
```

Example:
```bash
xelatex rkulshreshtha_resume.tex
```

### Option 2: Using Tectonic (Fastest Setup)
[Tectonic](https://tectonic-typesetting.github.io/) is a modern, self-contained LaTeX engine that downloads required packages on the fly.

On macOS:
```bash
brew install tectonic
```

Then compile any variant:
```bash
tectonic <filename>.tex
```

Example:
```bash
tectonic rkulshreshtha_resume.tex
```

---

## Automated Compilation (GitHub Actions)

This repository includes a GitHub Actions CI/CD pipeline (`.github/workflows/compile-resume.yml`):

- **Trigger:** Whenever changes are pushed to any file matching `rkulshreshtha_resume*.tex` on the `main` branch.
- **Compilation:** Compiles all matching `.tex` files using XeLaTeX with Microsoft TrueType fonts installed.
- **Deployment:** Automatically pushes all resulting PDFs to the dedicated [`resume`](https://github.com/rkulshreshtha/Resume-Latex/tree/resume) branch, keeping your `main` branch clean and preserving version history for each PDF.
