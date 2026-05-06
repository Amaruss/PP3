# PP3

## Ziel
In dieser Übung untersuchen wir, wie wir textbasierte Informationen von unserem Terminal aus verarbeiten, rendern und anzeigen.
Auch die Grundlagen der Softwareentwicklung sind die Verwaltung mit den Konzepten der programmtechnischen Textverarbeitung. 
Wir werden verschiedene Artefakte mit vier verschiedenen generieren _Beschreibung sprechen_. 
Nach dieser Übung sollen Sie selbst entscheid können, wollen Sie welche Verben und ein grundlegender Verständnis dafür haben, wie sie funktionieren sollen.

**Wichtig:** Beginnen Sie zu Beginnen einer Stoppuhr und arbeiten Sie 90 Minuten lang unterbrechen. Sobald die Zeit auf Grund ist, halten Sie sofort an und denken Sie den Punkt, an dem Sie innehalten mussten.

---

## Workflow
Merken Sie sich den Standard-Workflow. 
Im Zweifelsfall noch einmal suchen [PP1](https://github.com/MaxClerkwell/PP1)

1. **Gabel** Das Repository
2. **Andern und Commit** Ihre Lösung
3. **Senden Sie Ihren Link zur Übervorbereitung**

Wenn Sie nicht mehr kommen, wenden Sie die [Github-Diskussionen zu diesem Repository](https://github.com/MaxClerkwell/PP3/discussions)!

## Aufgaben

### Voraussetzungen: Linux, SSH und vim 
> Diese Aufgabe ist nicht Teil der gemessenen Zeit innerhalb dieser praktischen Übung!

Mittlere Wege sollen Sie hineits Zugriff auf einem lokalen Linux-Rechner haben. 
Ob es sich um einen Raspberry Pi, einen Desktop-PC oder ein Paravirtualisiertes WSL-System auf Ihrem Windows-Computer handelt handelt, macht keine Unterschied.
Wenn Sie sich nicht sicher sind, wie Sie sich anmelden sollen, können Sie [Schauen Sie sich diese Video-Tutorial an](https://www.youtube.com/watch?v=Z0ggeNzEhzY).
Stellen Sie sicher, dass Sie mit der Nutzung Ihres Datisystems gut vertraut sind `CD`, `ls`, `Katze`, `mkdir` und `rm`, sowie das Navigieren durch Textdateien mit `vim`, indem wir die `vimtutor` Du hättest bis zum Ende fertig sein sollen [PP2](https://github.com/MaxClerkwell/PP2).

---

### Aufgabe 1: SVG
Das skalierbare Vektorgrafikformat ist eine hohe gewandte Beschreibung für Diagramm. 
Sie werden diese Dateiformat wahrscheinlich würrend Ihr gemeinsamer beruflicher Laufbahn und Ihre Studienmittel wenden, daher mögen wir diese Format hier entdecken.

Wie bei Schreibsprachen über, handelt es sich bei dem eigentlichen Inhalt um eine normale Textdatei, die von einer speziellen Rendering-Software auf der Anzeige gerendert wird. 
Im Fall von SVG ist die Software, die das eigene Bild rendert, in viele andere Tools wie Browser oder Bildsoftware einbett. 

Eine SVG-Datei ist eine XML-basierte Textdatei, die zweidimensionalen Vektorgrafiken schreiben. 
Die Grundstruktur einer SVG-Datei umfast folgen Komponenten:

#### XML-Erklärung

```xml
<?XML-Version="1.0" Kodierung="UTF-8"?>
```

Diese optionale Zeit wird in der Datumsausgabe XML-Version und Zeichenkodierung angezeigt.

#### SVG-Wurzelelement

```xml
<svg xmlns="http://www.w3.org/2000/svg"
     version="1.1"
     width="800mm" height="600mm"
     viewBox="-400 -300 800 600">
  <!-- SVG content goes here -->
</svg>
```

##### Attributes:

- `xmlns`: Defines the XML namespace for SVG elements.
- `version`: Specifies the SVG version being used.
- `width` and `height`: Set the dimensions of the SVG canvas.
- `viewBox`: Establishes the coordinate system and aspect ratio.

#### Optional Metadata Elements

Within the `<svg>` element, you can include metadata to provide additional information about the SVG content:

```xml
<title>Title of the SVG</title>
<desc>Description or alternative text for the content.</desc>
```

- `<title>`: Provides a title for the SVG, which can improve accessibility.
- `<desc>`: Offers a description of the SVG content, also aiding accessibility.

#### Graphical Elements

Inside the `<svg>` element, you can define various graphical elements such as:

- `<rect>`: Draws rectangles.
- `<circle>`: Draws circles.
- `<path>`: Defines complex shapes.
- `<text>`: Adds text elements.

Each of these elements can have attributes to define their appearance and position.

#### Example

```xml
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg"
     version="1.1"
     width="800mm" height="600mm"
     viewBox="-400 -300 800 600">
  <title>Sample SVG</title>
  <desc>A simple example of an SVG file structure.</desc>
  <rect x="10" y="10" width="100" height="50" fill="blue" />
</svg>
```

This example creates an SVG canvas with a blue rectangle positioned at (10,10) with a width of 100 units and a height of 50 units.

For more detailed information on SVG structure and elements, you can refer to the [W3C SVG 2 Specification](https://www.w3.org/TR/SVG2/struct.html).

**Install vim on your local machine and open a new file, called `example.svg`. Write the SVG-code to include a straight line, a circle and a rectangle. When done, use your browser to open the file.**

<details>
    <summary>Your SVG Code</summary>
    <code>
    ......
    </code>
</details>

### Task 2: Markdown
You have already discovered _markdown_ in these `README.md` files. 
It is an easy and lightweight syntax, to instruct a display software to render text in a given way.

**Answer the following questions:**

<details>
    <summary>How does prepending hashes (<code>#</code>) affect the display?</summary>
    ......
</details>
<details>
    <summary>How do you mark italic or bold font?</summary>
    <code>
    ......
    </code>
</details>
<details>
    <summary>Which different ways are there to generate listings and tables?</summary>
    <code>
    ......
    </code>
</details>

### Task 3: LaTeX
While markdown is great for light-weight rendering text within a limited context such as a browser or phone, when it comes to more complex and professional rendering, the `LaTeX` toolset is the standard for creating `.pdf` files. 
`LaTeX` is usually not rendered _on the fly_, meaning while it is being displayed. 
A special software which we call _compiler_ is used to generate a parametrized documents. 
If you are running a local WSL, make sure to install `texlive-full` before continuing with the next steps. 
This may take up to 30 minutes, since it's a large software package. 
To check whether the installation was sucessful, run `pdflatex --version`.
The output should look something like this:
```sh
user@machine:~$ pdflatex --version
pdfTeX 3.141592653-2.6-1.40.25 (TeX Live 2023/Debian)
kpathsea version 6.3.5
Copyright 2023 Han The Thanh (pdfTeX) et al.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the pdfTeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the pdfTeX source.
Primary author of pdfTeX: Han The Thanh (pdfTeX) et al.
Compiled with libpng 1.6.43; using libpng 1.6.43
Compiled with zlib 1.3; using zlib 1.3
Compiled with xpdf version 4.04
```
If you are using the lecture-server, make sure to visit the [SCP tutorial](https://github.com/STEMgraph/301394c2-6efb-4677-aaff-47091fb8145d) first. 
Otherwise, you might have a hard time opening the generated `.pdf`-document.

Create a new directory on the linux machine that texlive is installed at, navigate into it and open a file with the name `main.tex`.
Simply copy the following text into it:
```tex
\documentclass{article}             % Sets the document class to "article"
\usepackage[utf8]{inputenc}         % Allows you to use UTF-8 input encoding

\title{Minimal LaTeX Project}       % Sets your document title
\author{Your Name}                  % Sets your name as the author
\date{\today}                       % Sets the date to the day you compile

\begin{document}                    % Begins the document content

\maketitle                          % Generates the title using the above information

Hello, world!                       % This is where your content goes

\end{document}                      % Ends the document
```
Save and close the document. 
Now run the following command to create a `.pdf`-file from it:
```sh
pdflatex -jobname=example.pdf main.tex
```
After it finishes, us `ls` to inspect the directory. 

**Answer the following questions:**

<details>
    <summary>Which files were generated by the LaTeX compiler?</summary>
    ......
</details>

<details>
    <summary>How do you change the name of the pdf-file?</summary>
    ......
</details>

### Task 4: Displaying your pdf
1) If you worked on the lecture-machine, use the `scp` command to copy your `.pdf`-file to your desktop. There you can display it with every regular `.pdf`-viewer
2) If you worked in the WSL: run `sudo apt install xpdf -y` to install the `xpdf`-viewer. Run `xpdf <your pdf path>` to open the document.

**Answer the following questions:**

<details>
    <summary>What changes in your pdf, if you change the documentclass to <code>book</code></summary>
    ......
</details>
<details>
    <summary>What changes in your pdf, if you add <code>\section{Intro}</code> after <code>\maketitle</code></summary>
    ......
</details>


### Task 5: 
If you are running on a Windows machine, make sure to install `vim` for Windows from the [official `vim` repository](https://github.com/vim/vim-win32-installer/releases).
Scroll down until you see the _Assets_ and use the `_64.exe` or `_x86.exe`, depending on your system. 
If you run MacOS or Linux natively, make sure you have `vim` installed via your package-manager. 

Open a terminal-session and create a new directory within your users home-directory called `html`.
Use `vim` to open a new file within it called: `index.html`.

Copy the following text into it:
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Minimal HTML Example</title>
  </head>
  <body>
    <p>Hello, world!</p>
  </body>
</html>
```
Depending on your system, run the following command to open the rendered file:
Windows:
```sh
start index.html
```
MacOS
```sh
open index.html
```
Linux
```sh
xdg-open index.html
```
If you are running in WSL, make sure to install the `w3m` browser before by executing `sudo apt install w3m -y`.


**Answer the following questions:**
<details>
  <summary>What happens if you exchange the <code>&lt;p&gt;&lt;/p&gt;</code> for <code>&lt;h1&gt;&lt;/h1&gt;</code>?</summary>
  ...
</details>

<details>
    <summary>How can you generate a listing of items?</summary>
    <code>
    ......
    </code>
</details>

<details>
    <summary>How can you create a table in this document?</summary>
    <code>
    ......
    </code>
</details>


---

**Remember:** Stop working after 90 minutes and record where you stopped!
