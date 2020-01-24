# LaTeX-Template für die Nordakademie-Transferleistungen

Struktur des LaTeX-Projekts:

- **/drawings** für Zeichnungen
- **/images** für Bilddateien
- **/sections** für den eigentlichen Inhalt der Arbeit

Die Kapitel sind in eigene Dateien im Ordner **/sections** ausgelagert, um die Hauptdatei **main.tex** übersichtlich zu halten.

Als LaTeX-Umgebung verwende ich TeX Live (https://www.tug.org/texlive/).

Als Editor verwende ich TeXMaker (http://www.xm1math.net/texmaker/). Hierbei muss der Bib(la)tex-Befehl angepasst werden zu _biber %_.

"Schnelles Übersetzen" muss dabei immer auf der **main.tex** ausgeführt werden und auf _"PdfLaTeX + Bib(la)tex + PdfLaTeX (x2) + PDF anzeigen"_ gestellt sein in den Einstellungen.

Falls benötigt, hier noch ein kleines LaTeX-Cheatsheet: https://wch.github.io/latexsheet/latexsheet-a4.pdf

Wie das LaTeX-Dokument am Ende aussehen könnte, kann man in **main.pdf** sehen.

Anleitung für die Nutzung von Visual Studio Code (https://code.visualstudio.com/) als Editor:

Benötigte Plugins:

- **LaTeX Workshop** (https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
- **LaTeX Utilities** (https://marketplace.visualstudio.com/items?itemName=tecosaur.latex-utilities)

Konfiguration (für TeX Live):
'''
{
"workbench.iconTheme": "vscode-icons",
"workbench.colorTheme": "Visual Studio Light",
"workbench.startupEditor": "newUntitledFile",
"terminal.integrated.fontFamily": "'MesloLGL Nerd Font Mono'",
"editor.formatOnSave": true,
"vsicons.dontShowNewVersionMessage": true,
"latex-workshop.message.update.show": false,
"latex-workshop.view.pdf.viewer": "tab",
"diffEditor.renderSideBySide": false,
"editor.wordWrap": "on",
"latex-workshop.latex.build.clearLog.everyRecipeStep.enabled": false,
"latex-workshop.latex.autoClean.run": "onBuilt",
"latex-workshop.latex.clean.fileTypes": [
"*.aux",
"*.bbl",
"*.blg",
"*.idx",
"*.ind",
"*.lof",
"*.lot",
"*.out",
"*.toc",
"*.acn",
"*.acr",
"*.alg",
"*.glg",
"*.glo",
"*.gls",
"*.fls",
"*.log",
"*.fdb_latexmk",
"*.snm",
"*.synctex(busy)",
"*.synctex.gz(busy)",
"*.nav",
"*.bak",
"*.bcf",
"*.run.xml",
"*.log"
],
"latex-workshop.latex.rootFile.useSubFile": false,
"latex-workshop.latex.recipe.default": "first",
"latex-workshop.latex.recipes": [
{
"name": "Build PDF with Biber",
"tools": [
"pdflatex",
"biber",
"pdflatex",
"pdflatex"
]
},
{
"name": "latexmk 🔃",
"tools": [
"latexmk"
]
},
{
"name": "latexmk (latexmkrc)",
"tools": [
"latexmk_rconly"
]
},
{
"name": "latexmk (lualatex)",
"tools": [
"lualatexmk"
]
},
{
"name": "pdflatex ➞ bibtex ➞ pdflatex × 2",
"tools": [
"pdflatex",
"bibtex",
"pdflatex",
"pdflatex"
]
}
],
"files.autoSaveDelay": 10000,
"editor.wordBasedSuggestions": false,
"latex-workshop.latex.tools": [
{
"name": "latexmk",
"command": "latexmk",
"args": [
"-synctex=1",
"-interaction=nonstopmode",
"-file-line-error",
"-pdf",
"-outdir=%OUTDIR%",
"%DOC%"
],
"env": {}
},
{
"name": "lualatexmk",
"command": "latexmk",
"args": [
"-synctex=1",
"-interaction=nonstopmode",
"-file-line-error",
"-lualatex",
"-outdir=%OUTDIR%",
"%DOC%"
],
"env": {}
},
{
"name": "latexmk_rconly",
"command": "latexmk",
"args": [
"%DOC%"
],
"env": {}
},
{
"name": "pdflatex",
"command": "pdflatex",
"args": [
"-synctex=1",
"-interaction=nonstopmode",
"-file-line-error",
"%DOC%"
],
"env": {}
},
{
"name": "bibtex",
"command": "bibtex",
"args": [
"%DOCFILE%"
],
"env": {}
},
{
"name": "biber",
"command": "biber",
"args": [
"%DOCFILE%"
],
"env": {}
}
]
}
'''
