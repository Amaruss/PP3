# PP3

## Goal
In this exercise, we will explore how to handle, render and display text-based information from our terminal.
As ancient as this may seem, the foundation of effective software engineering is a familiarity with the concepts of programmatic text-processing. 
We will generate different artifacts using four different _description-languages_. 
After this exercise, you should be able to decide for yourselves, when to use which and have a fundamental understanding of how they are supposed to work.

**Important:** Start a stopwatch when you begin and work uninterruptedly for 90 minutes. Once time is up, stop immediately and document the point where you had to pause.

---

## Workflow
Remember the standard workflow. 
If in doubt, revisit [PP1](https://github.com/MaxClerkwell/PP1)

1. **Fork** the repository
2. **Modify and Commit** your solution
3. **Submit your link for Review**

If you get stuck, use the [Github-Discussions of this Repository](https://github.com/MaxClerkwell/PP3/discussions)!

## Tasks

### Prerequisits: Linux, SSH and vim 
> This task is not part of the measured time within this practical exercise!

By now you should already have access to one local linux machine. 
Whether this is a Raspberry Pi, a Desktop-PC or a WSL para-virtualized system on your Windows computer doesn't make any difference.
If you are unsure about how to log in, you can [check out this video tutorial](https://www.youtube.com/watch?v=Z0ggeNzEhzY).
Make sure, that you are wellversed in utilizing your filesystem with `cd`, `ls`, `cat`, `mkdir` and `rm`, as well as navigating through textfiles with `vim`, by revisiting the `vimtutor` you should've finished by the end of [PP2](https://github.com/MaxClerkwell/PP2).

---

### Task 1: SVG
The scalable-vector-graphics format is a commonly used description language for diagrams. 
You will probably use this file format throughout your professional career and your studies multiple times, therefore we want to explore this format here.

As usual for description languages, the actual content is a regular textfile, that get's rendered on display by a sepecific rendering software. 
In case of SVG, the software that renders the actual picture is embedded in a lot of other tools, such as browsers, or image software. 

An SVG file is an XML-based text file that describes two-dimensional vector graphics. 
The basic structure of an SVG file includes the following components:

#### XML Declaration

```xml
<?xml version="1.0" encoding="UTF-8"?>
```

Diese optionale Zeile deklariert die in der Datei verwendete XML-Version und Zeichenkodierung.

#### SVG-Wurzelelement

```xml
<svg xmlns="http://www.w3.org/2000/svg"
 Version="1.1"
 Breite="800 mm" Höhe="600 mm"
 viewBox="-400 -300 800 600">
 <!-- SVG-Inhalte kommen hierhin -->
</svg>
```

##### Attribute:

- `xmlns`: Definiert den XML-Namespace für SVG-Elemente.
- `Version`: Gibt die verwendete SVG-Version an.
- `Breite` und `Höhe`: Legen Sie die Abmessungen der SVG-Leinwand fest.
- `Ansichtsfeld`: Legt das Koordinatensystem und das Seitenverhältnis fest.

#### Optionale Metadatenelemente

Innerhalb der `<svg>` Element können Sie Metadaten einfügen, um zusätzliche Informationen zum SVG-Inhalt bereitzustellen:

```xml
<title>Titel des SVG</title>
<desc>Beschreibung oder Alternativtext zum Inhalt.</desc>
```

- `<Titel>`: Bietet einen Titel für das SVG, der die Zugänglichkeit verbessern kann.
- `<Beschreibung>`: Bietet eine Beschreibung des SVG-Inhalts und unterstützt so auch die Zugänglichkeit.

#### Grafische Elemente

Im Inneren der `<svg>` Element, Sie können verschiedene grafische Elemente definieren, wie zum Beispiel:`<svg>` Element, Sie können verschiedene grafische Elemente definieren, wie zum Beispiel:

- `<rechteck>`: Zeichnet Rechtecke.
- `<Kreis>`: Zeichnet Kreise.
- `<Pfad>`: Definiert komplexe Formen.
- `<text>`: Für Texte Elemente hinzu.

Jedes dieser Elemente kann Attribut haben, um sein Aussehen und seine Position zu definieren.

#### Spiel

```xml
<?XML-Version="1.0" Kodierung="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg"
 Version="1.1"
 Breite="800 mm" Höhe="600 mm"
 viewBox="-400 -300 800 600">
 <title>Beispiel-SVG</title>
 <desc>Ein einfaches Beispiel einer SVG-Dateistruktur.</desc>
 <rect x="10" y="10" Breite="100" Höhe="50" Füllung="blau" />
</svg>
```

Dieses Beispiel stellt eine SVG-Leinwand mit einem blauen Rechteck dar, das bei (10,10) positioniert ist, mit einer Breite von 100 Einheiten und einer Höhe von 50 Einheiten.

Ausführende Informationen zur SVG-Struktur und den SVG-Elementen finden Sie im [W3C SVG 2 Spezifikation](https://www.w3.org/TR/SVG2/struct.html).

 XML-ErklärungInstallieren Sie vim auf Ihrem lokalen Computer und öffnen Sie eine neue Datei namens `Beispiel.svg`. Schreiben Sie den SVG-Code so, dass er eine gerade Linie, einen Kreis und einen Rechteck enthält. Wenn Sie fertig sind, können Sie die Datei mit Ihrem Browser.**

Hier ist Mein **Code:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg"
     version="1.1"
     width="12cm" height="4cm"
     viewBox="0 0 1200 400">
  <title>Sample SVG</title>
  <desc>A simple example of an SVG file structure.</desc>
  <rect x="1" y="1" width="1198" height="398" fill="none" storke="blue" stroke-width="2"/>
  <line x1="500" y1="300" x2="700" y2="100" stroke-width="15"  />
  <circle cx="600" cy="200" r="100" fill="red" stroke="none" stroke-width="10" />
</svg>
```


### Aufgabe 2: Markdown
Du hast es schon entdeckt _Markdown_ in Diesen `README.md` Datteln. 
Es handelt sich um eine einfache und leichte Syntax, um eine Anzeigesoftware anzuweisen, Text auf einer besten Weise darzustellen.

**Beantworten Sie die folgenden Fragen:**

<Details>
    <Zusammenfassung>Wie funktioniert das Voranstellen von Hashes (<Code>#</Code>) die Anzeige Bienenflussen?</Zusammenfassung>
    Das Voranstellen von Hashes (#) erzeugt in Markdown Überschriften. Je mehr Hashes verwendet werden, desto kleiner beziehungsweise niedriger ist die Überschrift.
Beispiele:
# Überschrift 1
## Überschrift 2
### Überschrift 3
#### Überschrift 4
</Details>
<Details>
    <Zusammenfassung>Wie markiert man kursive oder fette gedruckte Schrift?</Zusammenfassung>
    Kursive Schrift wird mit einem Stern * oder Unterstrich _ markiert. Fettgedruckte Schrift wird mit zwei Sternen ** oder zwei Unterstrichen __ markiert.

Beispiele:

*kursiv*
_kursiv_

**fett**
__fett__

***fett und kursiv***
</Details>
<Details>
    <Zusammenfassung>Welche verschiedenen Möglichkeiten geben es, Einträge und Tabellen zu generieren?</Zusammenfassung>
    Einträge können als ungeordnete oder geordnete Listen erstellt werden. Ungeordnete Listen nutzen -, * oder +. Geordnete Listen verwenden Zahlen. Tabellen werden mit | und --- erstellt.

Beispiele:

- Eintrag 1
- Eintrag 2

1. Erstes Element
2. Zweites Element

| Name | Alter |
|------|------|
| Anna | 21 |
| Max | 25 |
</Details>

### Aufgabe 3: LaTeX
Während Markdown sich hervorragend für die leichte Textwiedergabe in einem erweiterten Kontext wie einem Browser oder Telefon selbst, ist bei Komplexerer und Professioneller Wiedergabe die `LaTeX` Werkzeugsatz ist der Standard für die Gründung `. . . . .pdf` Datteln. 
`LaTeX` Wird normalerweise nicht gerendert _im Handumdrehen_, auch würrend der Anzeige. 
Eine spezielle Software, die wir nennen _Compiler_ wird verwendet, um parametrisierte Dokumente zu generieren. 
Wenn Sie eine lokale WSL übernehmen, stellen Sie sicher, dass Sie installieren `texlive-voll` vor Sie mit den nächsten Schritten fortfahren. 
Dies kann bis zu 30 Minuten dauern, da es sich um ein großes Softwarepaket handelt. 
Um zu überprüfen, ob die Installation erfolreich war, für Sie `pdflatex --version`.
Die Ausgabe soll ungezügelt so aussehen:
```Scheiße
user@machine:~$ pdflatex --version
pdfTeX 3.141592653-2.6-1.40.25 (TeX Live 2023/Debian)
kpathsea Version 6.3.5
Copyright 2023 Han The Thanh (pdfTeX) et al.
Es gibt KEINE Garantie. Die Weiterverbreitung dieser Software erfolgt
unter den Bedingungen des pdfTeX-Urheberrechts und
Die Lesser GNU General Public License.
Weitere Informationen zu diesen Angelegenheiten finden Sie in der Datei
Genanntes KOPIEREN und die pdfTeX-Quelle.
Hauptautor von pdfTeX: Han The Thanh (pdfTeX) et al.
Kompiliert mit libpng 1.6.43; unter Verwaltung von libpng 1.6.43
Kompiliert mit zlib 1.3; mit zlib 1.3
Kompiliert mit xpdf Version 4.04
```
Wenn Sie den Vorlesungsserver wenden, suchen Sie sie unbedingt den [SCP-Tutorial](https://github.com/STEMgraph/301394c2-6efb-4677-aaff-47091fb8145d) Erste. 
Andernfalls kann es sein, dass er gefallen ist, das Generierte zu öffnen `. . . .pdf`- Dokumentieren.

Erste Sie ein neues Verzeichnis auf dem Linux-Rechner, auf dem texlive installiert ist, navigieren Sie hinein und können Sie eine Datei mit dem Namen `main.tex`.
Koppeln Sie einfach folgen Text hinein:
```tex
\documentclass{article} % Setzt die Dokumentklasse auf "article"
\usepackage[utf8]{inputenc} % Verarbeitung der Verwaltung der UTF-8-Eingangskodierung

\title{Minimal LaTeX Project} % Legt Ihren Dokumenttitel fest
\author{Ihr Name} % Legt Ihren Namen als Autor fest
\date{\today} % Legt das Datum auf den Tag fest, an dem Sie kompilieren

\begin{document} % Beginne mit dem Dokumentinhalt

\maketitle % Generiert den Titel unter Werbung der eigenen allgemeinen Informationen

Hallo Welt! % Hierhin gehen Ihre Inhalation

\end{document} % Beendet das Dokument
```
Speicher und Schichten Sie das Dokument. 
Für Sie nun den folgenden Befehl aus, um eine zu ersten `. . . . . . .pdf`- Dattel-Daraus:
```
pdflatex -jobname=example.pdf main.tex
```
Nachdem es fertig ist, `ls` um das Verzeichnis zu überprüfen. 

**Beantworten Sie die folgenden Fragen:**

*Welche Daten wurden vom LaTeX-Compiler generiert?*


Der LaTeX-Compiler erzeugt mehrere Dateien. Neben der PDF-Datei werden auch Hilfsdateien erstellt, die für die Kompilierung benötigt werden. Typischerweise entstehen folgende Dateien:
example.pdf → das fertige PDF-Dokument
main.log → Protokolldatei mit Informationen und Fehlermeldungen
main.aux → Hilfsdatei für Referenzen und Verzeichnisse
Je nach Dokument können noch weitere Dateien entstehen.

*Wie ist der Name der PDF-Datei?*

Der Name der PDF-Datei lautet:
example.pdf
Der Name entsteht durch den Parameter:
-jobname=example.pdf
im Befehl:
pdflatex -jobname=example.pdf main.tex

### Aufgabe 4: Anhang Ihres PDFs
1) Wenn Sie an der Vorlesungsmaschine arbeiten haben, wenden Sie die `scp` Befehl zum Kopieren Ihrer `. . . . .pdf Stop working after 90 minutes and record where you stopped!- Datum auf Ihrem Desktop. Dort können Sie es mit jedem regulären anzeigen `. . . . . .pdf Hören Sie nach 90 Minuten auf zu arbeiten und zeichnen Sie auf, wo Sie aufgehört haben!-Zuschauer
2) Wenn Sie in der WSL arbeiten haben: laufen `sudo apt install xpdf -y` um die zu installieren `xpdf`-Zuschauer. Ausführer `xpdf <Ihr PDF-Pfad>` um das Dokument zu öffnen.

**Beantworten Sie die folgenden Fragen:**

1. **War sich in Ihrem PDF geändert, wenn Sie die Dokumentklasse ändern in `book`?**
   Wenn die Dokumentklasse von `article` zu `book` geändert wird, verändert sich das Layout des Dokuments. Das Dokument wirkt mehr wie ein Buch: Kapitel (`\chapter`) können verwendet werden, Seitenumbrüche werden anders gesetzt und die Formatierung der Überschriften verändert sich.

---

2. **Was hat sich in Ihrem PDF geändert, wenn Sie `\section{Einleitung}` nach `\maketitle` hinzufügen?**
   Es wird eine neue Abschnittsüberschrift mit dem Namen „Einleitung“ erzeugt. Diese erscheint unter dem Titel des Dokuments und strukturiert den Inhalt.

Beispiel:

```latex id="a7u4r9"
\maketitle
\section{Einleitung}
```

### Aufgabe 5: 
Wenn Sie auf einem Windows-Computer laufen, stellen Sie sicher, dass Sie installieren `vim` für Windows aus dem [Büroell `vim` Repository](https://github.com/vim/vim-win32-installer/releases).
Scrollen Sie nach bis, bis Sie das sehen _Vermögenswerte_ und Wenden Sie sterben `_64.exe` Oder `_x86.exe`, abhängig von Ihrem System. 
Wenn Sie MacOS oder Linux nativ ausfürhren, stellen Sie sicher, dass Sie dies getan haben `vim` Über Ihren Paketmanager installiert. 

Öffnen Sie eine Terminalsitzung und erste Sie ein neues Verzeichnis im Home-Verzeichnis Ihre Nutzers mit dem Namen `HTML`.
Wenden `vim` um darin eine neue Datei mit dem Namen zu öffnen: `index.html`.

Kopieren Sie den folgenden Text hinein:
```HTML
<!DOCTYPE html>
<html>
 <Kopf>
 <meta charset="UTF-8">
 <title>Minimales HTML-Beispiel</title>
 </Kopf>
 <Körper>
 <p>Hallo Welt!</p>
 </Körper>
</html>
```
Für Sie sind Sie nach System den folgenden Befehlen aus, um die gerenderten Termine zu kaufen:
Windows:
```Scheiße
index.html starten
```
MacOS
```Scheiße
Index.html öffnen
```
Linux
```Scheiße
xdg-open index.html
```
Wenn Sie in WSL laufen, stellen Sie sicher, dass Sie das installieren `w3m` Browser vorher durch Ausgaben `sudo apt install w3m -y`.


**Beantworten Sie die folgenden Fragen:**
1. **Was passiert, wenn Sie `<p></p>` durch `<h1></h1>` ersetzen?**
   Der Text wird nicht mehr als normaler Absatz dargestellt, sondern als große Hauptüberschrift.

Beispiel:

```html id="91v7a3"
<h1>Hallo Welt!</h1>
```

---

2. **Wie können Sie eine Auflistung von Artikeln erzeugen?**

Mit HTML-Listen:

```html id="7pr5h2"
<ul>
  <li>Artikel 1</li>
  <li>Artikel 2</li>
  <li>Artikel 3</li>
</ul>
```

* `<ul>` erzeugt eine ungeordnete Liste
* `<li>` erzeugt einzelne Listeneinträge

---

3. **Wie können Sie in diesem Dokument eine Tabelle erzeugen?**

Mit den HTML-Tags `<table>`, `<tr>` und `<td>`:

```html id="x1m5ka"
<table border="1">
  <tr>
    <td>Name</td>
    <td>Alter</td>
  </tr>
  <tr>
    <td>Anna</td>
    <td>21</td>
  </tr>
</table>
```
---
**Denken Sie an Daran:** Hören Sie nach 90 Minuten auf zu arbeiten und zeichen Sie auf, wo Sie aufgehört haben!
