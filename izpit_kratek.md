# Računalniški praktikum - HITRA REFERENCA

## VISUAL STUDIO CODE

### Bližnjice
- **Ctrl+Shift+P**: paleta ukazov
- **Ctrl+F** / **Ctrl+H**: iskanje / zamenjava
- **Ctrl+Shift+F** / **Ctrl+Shift+H**: iskanje/zamenjava v projektu
- **Alt+klik**: dodaj kurzor
- **Ctrl+D**: izberi naslednjo pojavitev besede
- **Ctrl+Shift+L**: izberi vse pojavitve
- **Alt+↑/↓**: premakni vrstico
- **Shift+Alt+↑/↓**: podvoji vrstico
- **Ctrl+/**: komentiraj
- **Ctrl+Home/End**: na začetek/konec dokumenta
- **Home/End**: na začetek/konec vrstice

---

## HTML

### Osnovna struktura
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Naslov</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- vsebina -->
</body>
</html>
```

### Pomembne značke
- **Glave**: `<h1>` do `<h6>`
- **Odstavek**: `<p>`
- **Povezava**: `<a href="url">besedilo</a>`
- **Slika**: `<img src="pot" alt="opis">`
- **Div/span**: `<div>`, `<span>`
- **Krepko/ležeče**: `<strong>`, `<em>`
- **Seznami**: `<ul>/<ol>` z `<li>`
- **Tabela**: `<table>`, `<tr>`, `<th>`, `<td>`
- **Komentar**: `<!-- komentar -->`

### Atributi
- `id="unikaten-id"` - za en element
- `class="razred"` - za več elementov

---

## CSS

### Izbiralci
```css
p { }              /* značka */
.razred { }        /* razred */
#id { }            /* ID */
* { }              /* vsi elementi */
table a { }        /* potomci */
h1, h2 { }         /* več elementov */
p.razred { }       /* p z razredom */
[href] { }         /* z atributom */
tr:nth-child(even) { }  /* sode vrstice */
a:hover { }        /* ob lebdenju */
```

### Pomembne lastnosti
```css
/* Dimenzije */
width: 400px;
height: 300px;

/* Škatlasti model */
margin: 10px;
padding: 10px;
border: 2px solid black;

/* Besedilo */
color: red;
font-size: 16px;
font-weight: bold;
text-align: center;

/* Ozadje */
background-color: #f0f0f0;
```

### Barve
- Ime: `red`, `blue`
- Hex: `#FF0000`
- RGB: `rgb(255, 0, 0)`, `rgba(255, 0, 0, 0.5)`

### Enote
- `px` (točke), `em` (relativno), `%` (odstotki)

---

## LaTeX

### Preambula
```latex
\documentclass[a4paper,12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[slovene]{babel}
\usepackage[T1]{fontenc}
\usepackage{amsmath,amssymb,amsthm}
\usepackage{graphicx,hyperref,booktabs}

\newcommand{\p}{\mathbb{P}}

\theoremstyle{definition}
\newtheorem{definicija}{Definicija}
```

### Dokument
```latex
\begin{document}
\title{Naslov}
\author{Avtor}
\date{\today}
\maketitle

\begin{abstract}
Povzetek
\end{abstract}

\tableofcontents
\section{Razdelek}
\end{document}
```

### Matematika
```latex
$a^2 + b^2$            % vrstično
\[a^2 + b^2\]          % prikazno

\frac{a}{b}            % ulomek
\sqrt{x}               % koren
\sum_{i=1}^n           % vsota
\int_0^1 f(x) dx       % integral

\sin, \cos, \log       % funkcije (NE sin!)
\alpha, \beta          % grške črke
\mathbb{R}             % množice
\in, \emptyset         % ∈, ∅
```

### Okolja
```latex
\begin{itemize}
\item Element
\end{itemize}

\begin{equation}
E = mc^2
\label{eq:e}
\end{equation}

\begin{cases}
x & x \geq 0 \\
-x & x < 0
\end{cases}

\begin{tabular}{|l|c|r|}
\hline
a & b & c \\
\hline
\end{tabular}
```

### Slike
```latex
\begin{figure}[h]
\centering
\includegraphics[width=0.5\textwidth]{slika.png}
\caption{Opis}
\label{fig:sl}
\end{figure}
```

### Sklici in citati
```latex
\label{key}
\ref{key}, \eqref{key}
\cite{key}
\bibliography{viri}
\bibliographystyle{plain}
```

### Beamer
```latex
\documentclass{beamer}
\usetheme{Berlin}

\begin{frame}{Naslov}
\begin{block}{Blok}
Vsebina
\end{block}
\pause
\end{frame}

\begin{itemize}[<+->]
\item Se
\item Postopno
\item Odkriva
\end{itemize}
```

---

## EXCEL

### Uvoz CSV
- Data > From Text/CSV
- UTF-8 kodiranje
- Delimiter: `;` (SL) ali `,` (EN)

### Formule
```
=SUM(A1:A10)           % vsota
=AVERAGE(A1:A10)       % povprečje
=IF(A1>100,"Da","Ne")  % pogoj
=MONTH(A1)             % mesec iz datuma
=A1*B1                 % množenje
```

### Pogojno oblikovanje
- Home > Conditional Formatting
- Highlight Cells Rules > Greater/Less Than
- Color Scales

### Vrtilne tabele
- Insert > PivotTable
- Rows: vrstice (npr. Mesec)
- Columns: stolpci (npr. Regija)
- Values: vrednosti (npr. Average Prodaje)

---

## MATHEMATICA

### Osnove
```mathematica
ClearAll[x, y, f]      (* VEDNO na začetku! *)

x = 5                  (* vrednost *)
f[x_] := x^2          (* funkcija *)

Expand[(x+1)^2]        (* razširi *)
Factor[x^2-1]          (* faktoriziraj *)
Simplify[expr]         (* poenostavi *)
```

### Izračuni
```mathematica
Sum[i^2, {i,1,10}]              (* vsota *)
Limit[Sin[x]/x, x->0]           (* limita *)
D[x^3, x]                       (* odvod *)
Integrate[x^2, x]               (* integral *)
Integrate[x^2, {x,0,1}]         (* določeni *)
```

### Enačbe
```mathematica
Solve[x^2-5x+6==0, x]           (* simbolno *)
NSolve[x^5-x-1==0, x]           (* numerično *)
Reduce[x^2>4, x]                (* neenačbe *)
FindRoot[Cos[x]==x, {x,0}]      (* ničle *)
```

### Grafi
```mathematica
Plot[Sin[x], {x,0,2Pi}]
ParametricPlot[{Cos[t],Sin[t]}, {t,0,2Pi}]
ContourPlot[x^2+y^2, {x,-2,2}, {y,-2,2}]
RegionPlot[x^2+y^2<1, {x,-2,2}, {y,-2,2}]
Plot3D[Sin[x]Cos[y], {x,0,2Pi}, {y,0,2Pi}]
```

### Grške črke
- `ESC alpha ESC` → α
- `ESC beta ESC` → β
- `ESC pi ESC` → π

### Barve spremenljivk
- **Črna**: definirano
- **Zelena**: parameter
- **Modra**: nedoločeno (napaka!)

---

## PREPOVEDANO NA IZPITU

❌ Git  
❌ Regularni izrazi  
❌ TikZ risanje (samo `\input`)  
❌ Vizualno oblikovanje (barve, fonti) v Excelu  
❌ INDEX, MATCH v Excelu  
❌ Manipulate v Mathematici  

---

## HITRI NASVETI

### Pred izpitom
✅ Preveri osebni dokument in študentsko  
✅ Izklopi telefon (v torbo!)  
✅ Odpri spletno učilnico  
✅ Preveri, da imaš vse datoteke  

### Med izpitom
✅ **Sproti shranjuj** (Ctrl+S na 2 min)  
✅ Ne obsedi pri težki nalogi  
✅ Preveri imena datotek  
✅ Uporabljaj ClearAll (Mathematica)  
✅ Preveri barve spremenljivk (Mathematica)  

### Pred oddajo
✅ Stisni vse v **PriimekIme.zip** (brez šumnikov!)  
✅ Preveri vsebino ZIP-a  
✅ Oddaj na učilnico  
✅ Počakaj na dovoljenje za vstajanje  

---

## ČASOVNA RAZPOREDITEV (120 min)

| Naloga | Točke | Čas |
|--------|-------|-----|
| HTML/CSS | 20 | ~25 min |
| LaTeX | 36 | ~45 min |
| Excel | 12 | ~15 min |
| Mathematica | 32 | ~30 min |
| Oddaja | - | 5 min |

---

## POGOSTI NAPAKE

| ❌ Napaka | ✅ Pravilno |
|----------|-----------|
| HTML neparnične značke | Vsaka `<tag>` rabi `</tag>` |
| CSS pozabljen `;` | Vsaka lastnost konča s `;` |
| LaTeX `sin` | Uporabi `\sin` |
| LaTeX `\phi` za ∅ | Uporabi `\emptyset` |
| Excel pozabljen $ | `$A$1` za absolutno referenco |
| Mathematica `f[x]` | Uporabi `f[x_]` s podčrtajem |
| Mathematica `=` za funkcijo | Uporabi `:=` za definicijo |

---

**SREČNO! 🍀**