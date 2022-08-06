# LaTeX Template

This repo contains the boilerplate for creating a new LaTeX document.

## Settings

I use VSCode with [Latex Workshop made by James Yu](https://github.com/James-Yu/LaTeX-Workshop).

The settings I use is:

```json
{
  "latex-workshop.view.pdf.viewer": "tab",
  "latex-workshop.latex.autoClean.run": "onBuilt",
  "[latex]": {
    "editor.defaultFormatter": "James-Yu.latex-workshop"
  },
  "latex-workshop.message.error.show": false,
  "latex-workshop.message.warning.show": false,
  "latex-workshop.latex.outDir": "%DIR%",
  "latex-workshop.latex.clean.fileTypes": [
    "*.aux",
    "*.log",
    "*.synctex.gz",
    "*.toc",
    "*.run.xml",
    "*.blg",
    "*.bbl"
  ],
  "latex-workshop.latex.option.maxPrintLine.enabled": false,
  "latex-workshop.latex.clean.subfolder.enabled": true,
  "latex-workshop.latex.recipes": [
    {
      "name": "pdflatex ➞ bibtex ➞ pdflatex × 2",
      "tools": ["pdflatex", "bibtex", "pdflatex", "pdflatex"]
    }
  ],
  "latex-workshop.latex.tools": [
    {
      "name": "pdflatex",
      "command": "pdflatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        // "--aux-directory=.aux",
        "%DOC%"
      ],
      "env": {}
    },
    {
      "name": "bibtex",
      "command": "bibtex",
      "args": ["%DOCFILE%"],
      "env": {}
    }
  ]
}
```
