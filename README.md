# LaTeX-Template für die Nordakademie-Transferleistungen

## Struktur des LaTeX-Projekts:

- **/drawings** für Zeichnungen
- **/images** für Bilddateien
- **/sections** für den eigentlichen Inhalt der Arbeit

Die Kapitel sind in eigene Dateien im Ordner **/sections** ausgelagert, um die Hauptdatei **main.tex** übersichtlich zu halten.

## LaTeX-Umgebung

Als LaTeX-Umgebung verwende ich TeX Live (https://www.tug.org/texlive/).

## Editor

### TeXMaker

Als Editor verwende ich TeXMaker (http://www.xm1math.net/texmaker/). Hierbei muss der Bib(la)tex-Befehl angepasst werden zu _biber %_.

"Schnelles Übersetzen" muss dabei immer auf der **main.tex** ausgeführt werden und auf _"PdfLaTeX + Bib(la)tex + PdfLaTeX (x2) + PDF anzeigen"_ gestellt sein in den Einstellungen.

### Visual Studio Code

Anleitung für die Nutzung von Visual Studio Code (https://code.visualstudio.com/) als Editor:

Benötigte Plugins:

- **LaTeX Workshop** (https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
- **LaTeX Utilities** (https://marketplace.visualstudio.com/items?itemName=tecosaur.latex-utilities)
- **Settings Sync** (für das Importieren meiner Settings) (https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

Meine Settings für Visual Studio Code: https://gist.github.com/simondose1012/1c8d67a1215e6ef4751c427f4c6ad6bb

## Nutzung von Draw.io

- Am besten die Desktop-Version nutzen: https://github.com/jgraph/drawio-desktop/releases
- Die .drawio-Dateien am besten unter `/drawings/drawio` speichern
- Unter `/drawings/drawio` die Zeichnungen als cropped PDF speichern, dies kann auch mit folgendem Script (unter Linux) automatisiert werden:
  ```
  /usr/bin/find ./drawings/drawio -name *.drawio -exec rm -f {}.pdf \; -exec /usr/local/bin/draw.io --crop -x -o {}.pdf {} \;
  ```

## Cheat Sheet

Falls benötigt, hier noch ein kleines LaTeX-Cheatsheet: https://wch.github.io/latexsheet/latexsheet-a4.pdf
