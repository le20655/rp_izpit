# Računalniški praktikum - Podrobna priprava na izpit

## 1. VISUAL STUDIO CODE

### Delo z datotečnim sistemom
- **Odpiranje map/projektov**: File > Open Folder (Ctrl+K Ctrl+O)
- **Ustvarjanje datotek**: Klik na ikono "New File" v Explorer ali Ctrl+N
- **Shranjevanje**: Ctrl+S (posamezna datoteka), Ctrl+K S (vse datoteke)
- **Preklapljanje med datotekami**: Ctrl+Tab

### Paleta ukazov
- **Odpiranje palete**: Ctrl+Shift+P ali F1
- Omogoča dostop do vseh ukazov brez uporabe miške
- Primer uporabe: "Transform to Uppercase", "Sort Lines Ascending"

### Bližnjice na tipkovnici

**Osnovno urejanje:**
- Ctrl+C: kopiraj
- Ctrl+X: izreži
- Ctrl+V: prilepi
- Ctrl+Z: razveljavi
- Ctrl+Shift+Z: uveljavi
- Ctrl+/: komentiraj/odkomentiraj vrstico

**Izbiranje:**
- Ctrl+A: izberi vse
- Shift+puščice: razširi izbor
- Ctrl+L: izberi celotno vrstico

### Hitro premikanje

**Med besedami:**
- Ctrl+puščica levo/desno: skok med besedami
- Ctrl+Shift+puščica: izberi do naslednje besede

**Na začetek/konec vrstice:**
- Home: začetek vrstice
- End: konec vrstice
- Ctrl+Home: začetek dokumenta
- Ctrl+End: konec dokumenta

**Po vrsticah:**
- Ctrl+G: skok na določeno vrstico (vneseš številko)
- Ctrl+P: hitro iskanje datotek

### Iskanje in zamenjava

**V trenutni datoteki:**
- Ctrl+F: iskanje
- Ctrl+H: zamenjava
- F3 ali Enter: naslednja pojavitev
- Shift+F3: prejšnja pojavitev
- Alt+Enter: izberi vse pojavitve

**V celotnem projektu:**
- Ctrl+Shift+F: iskanje v projektih
- Ctrl+Shift+H: zamenjava v projektih
- Lahko uporabiš regex (klik na ikono .*)

**Praktični primeri:**
- Najdi vse `.png` datoteke: uporabi `*.png` v iskanju
- Zamenjaj `%` z `\section`: Ctrl+H, vpiši `%` in `\section`

### Več kurzorjev

**Dodajanje z miško:**
- Alt+klik: doda kurzor na položaj klika
- Uporabno za urejanje več vrstic naenkrat

**Razširitev na sosednje vrstice:**
- Ctrl+Alt+puščica gor/dol: dodaj kurzor na zgornjo/spodnjo vrstico
- Lahko urediš več vrstic sočasno

**Na pojavitve besede:**
- Ctrl+D: izberi naslednjo pojavitev besede pod kurzorjem
- Ctrl+Shift+L: izberi vse pojavitve besede
- Primer: izberi "TODO", pritisni Ctrl+Shift+L, zapiši "DONE"

### Urejanje vrstic

**Podvajanje:**
- Shift+Alt+puščica gor/dol: podvoji vrstico gor/dol
- Ctrl+Shift+D: podvoji vrstico (alternativa)

**Premikanje:**
- Alt+puščica gor/dol: premakni vrstico gor/dol

**Zamikanje:**
- Tab: zamakni desno
- Shift+Tab: zamakni levo
- Ctrl+] / Ctrl+[: zamakni izbor desno/levo

**Komentiranje:**
- Ctrl+/: vklopni/izklopni komentiranje (// v večini jezikov)
- Shift+Alt+A: blokovski komentar (/* */ v večini jezikov)

---

## 2. HTML

### Struktura HTML dokumenta

```html
<!DOCTYPE html>
<html>
<head>
    <title>Naslov strani</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Vsebina dokumenta -->
</body>
</html>
```

### Glava dokumenta

**`<!DOCTYPE html>`**
- Deklaracija tipa dokumenta
- Pove brskalniku, da gre za HTML5 dokument
- Vedno prva vrstica v HTML datoteki

**`<html>`**
- Korenski element HTML dokumenta
- Vsebuje celoten dokument

**`<head>`**
- Glava dokumenta
- Vsebuje metapodatke (informacije o dokumentu)
- Ni vidna na strani

**`<title>`**
- Naslov dokumenta
- Prikazan v zavihku brskalnika
- Primer: `<title>Moja spletna stran</title>`

**`<link>`**
- Povezava na zunanje vire (CSS, ikone, ...)
- Primer: `<link rel="stylesheet" href="oblikovanje.css">`
- `rel` določa relacijo (relationship)
- `href` je pot do datoteke

**`<meta>`**
- Metapodatki o dokumentu
- `<meta charset="UTF-8">` določa kodiranje znakov
- UTF-8 podpira šumnike in posebne znake

### Struktura dokumenta

**`<!--...-->`**
- HTML komentar
- Ni viden na strani
- Primer: `<!-- To je komentar -->`

**`<body>`**
- Telo dokumenta
- Vsebuje vso vidno vsebino strani

**`<div>`**
- Generični vsebnik (division)
- Uporaben za skupinsko oblikovanje elementov
- Primer: `<div class="container">...</div>`

**`<h1>`, `<h2>`, ... `<h6>`**
- Naslovi različnih ravni
- `<h1>` je največji (glavni naslov)
- `<h6>` je najmanjši
- Primer: `<h1>Glavni naslov</h1>`

### Oblikovanje vsebine

**`<a>`**
- Povezava (anchor)
- `href` atribut določa cilj
- Primeri:
  - `<a href="https://www.wikipedia.org">Wikipedia</a>`
  - `<a href="#razdelek">Skok na razdelek</a>` (notranja povezava)
  - `<a href="dokument.pdf">Prenesi PDF</a>`

**`<blockquote>`**
- Daljši citat iz drugega vira
- Primer: `<blockquote>To je citat.</blockquote>`

**`<br>`**
- Prelom vrstice (break)
- Samozapirajoča značka
- Primer: `Prva vrstica<br>Druga vrstica`

**`<code>`**
- Koda (kratek odsek)
- Monospace pisava
- Primer: `Uporabi funkcijo <code>printf()</code>`

**`<em>`**
- Poudarek (emphasis)
- Običajno prikazano kot ležeče
- Primer: `<em>pomembno</em>`

**`<hr>`**
- Horizontalna črta (horizontal rule)
- Samozapirajoča značka
- Uporablja se za ločevanje vsebin

**`<img>`**
- Slika (image)
- Samozapirajoča značka
- Primer: `<img src="slika.jpg" alt="Opis slike">`
- `src`: pot do slike
- `alt`: alternativen tekst (dostopnost)

**`<kbd>`**
- Tipka na tipkovnici (keyboard)
- Primer: `Pritisni <kbd>Ctrl</kbd>+<kbd>C</kbd>`

**`<p>`**
- Odstavek (paragraph)
- Primer: `<p>To je odstavek besedila.</p>`

**`<pre>`**
- Predformatirano besedilo (preformatted)
- Ohrani presledke in nove vrstice
- Uporabno za kodo
```html
<pre>
def funkcija():
    return True
</pre>
```

**`<small>`**
- Manjše besedilo
- Primer: `<small>Drobni tisk</small>`

**`<span>`**
- Generični vsebnik za vrstično vsebino
- Za oblikovanje dela besedila
- Primer: `<span class="rdeče">Pomembno</span>`

**`<strong>`**
- Močan poudarek
- Običajno prikazano krepko
- Primer: `<strong>zelo pomembno</strong>`

### Seznami

**`<ul>` - Neurejen seznam (unordered list)**
```html
<ul>
    <li>Prvi element</li>
    <li>Drugi element</li>
</ul>
```
- Prikazan s kroglicami

**`<ol>` - Urejen seznam (ordered list)**
```html
<ol>
    <li>Prvi korak</li>
    <li>Drugi korak</li>
</ol>
```
- Prikazan z številkami

**`<li>` - Element seznama (list item)**
- Uporablja se znotraj `<ul>` ali `<ol>`

**`<dl>`, `<dt>`, `<dd>` - Seznam definicij**
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
</dl>
```
- `<dl>`: definition list
- `<dt>`: definition term (izraz)
- `<dd>`: definition description (opis)

### Tabele

```html
<table>
    <thead>
        <tr>
            <th>Stolpec 1</th>
            <th>Stolpec 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Podatek 1</td>
            <td>Podatek 2</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Noga 1</td>
            <td>Noga 2</td>
        </tr>
    </tfoot>
</table>
```

**`<table>`** - Tabela
**`<thead>`** - Glava tabele (table head)
**`<tbody>`** - Telo tabele (table body)
**`<tfoot>`** - Noga tabele (table foot)
**`<tr>`** - Vrstica tabele (table row)
**`<th>`** - Celica glave (table header)
**`<td>`** - Celica s podatki (table data)

### Splošni atributi

**`id`**
- Unikaten identifikator elementa
- Primer: `<div id="glava">...</div>`
- Za sklicevanje: `<a href="#glava">Pojdi na glavo</a>`

**`class`**
- Razred elementa (lahko več elementov ima isti razred)
- Primer: `<p class="pomembno">...</p>`
- Za CSS: `.pomembno { color: red; }`

---

## 3. CSS

### Osnovni izbiralci

**Po znački:**
```css
p {
    color: blue;
}
```
- Izbere vse `<p>` elemente

**Po razredu:**
```css
.pomembno {
    font-weight: bold;
}
```
- Izbere vse elemente z `class="pomembno"`
- Začne se s piko (.)

**Po identifikatorju:**
```css
#glava {
    background-color: gray;
}
```
- Izbere element z `id="glava"`
- Začne se z lojtrco (#)

**Univerzalni izbiralec:**
```css
* {
    margin: 0;
    padding: 0;
}
```
- Izbere vse elemente

### Sestavljeni izbiralci

**Potomci (descendants):**
```css
table a {
    color: red;
}
```
- Izbere vse `<a>` elemente znotraj `<table>`
- Ne glede na globino

**Disjunkcija (vejica):**
```css
h1, h2, h3 {
    font-family: Arial;
}
```
- Izbere vse `<h1>`, `<h2>` IN `<h3>` elemente

**Konjunkcija (brez presledka):**
```css
p.pomembno {
    background-color: yellow;
}
```
- Izbere `<p>` elemente, ki imajo `class="pomembno"`

### Izbiralci atributov

**Obstoj atributa:**
```css
[href] {
    text-decoration: underline;
}
```
- Izbere vse elemente z atributom `href`

**Točna vrednost:**
```css
[type="text"] {
    border: 1px solid black;
}
```
- Izbere elemente z `type="text"`

### Psevdo-razredi

**`:hover`**
```css
a:hover {
    color: red;
}
```
- Aktivira se, ko miška lebdi nad elementom

**`:nth-child(even)` / `:nth-child(odd)`**
```css
tr:nth-child(even) {
    background-color: #f2f2f2;
}
```
- `even`: sodi elementi (2, 4, 6, ...)
- `odd`: lihi elementi (1, 3, 5, ...)

**`:last-child`**
```css
li:last-child {
    border-bottom: none;
}
```
- Izbere zadnji element med sorojenci

**`:first-child`**
```css
p:first-child {
    margin-top: 0;
}
```
- Izbere prvi element med sorojenci

### Lastnosti za dimenzije

**`width` / `height`**
```css
img {
    width: 400px;
    height: 300px;
}
```
- Širina in višina elementa

### Škatlasti model (Box Model)

```
+---------------------------+
|        margin             |
|  +---------------------+  |
|  |     border          |  |
|  |  +---------------+  |  |
|  |  |   padding     |  |  |
|  |  |  +---------+  |  |  |
|  |  |  | content |  |  |  |
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

**`margin`**
- Prostor zunaj obrobe
- `margin: 10px;` (vsi robovi)
- `margin-top`, `margin-right`, `margin-bottom`, `margin-left`

**`padding`**
- Prostor znotraj obrobe
- `padding: 10px;` (vsi robovi)
- `padding-top`, `padding-right`, `padding-bottom`, `padding-left`

**`border`**
- Obroba elementa
- `border: 2px solid black;` (debelina slog barva)
- `border-top`, `border-right`, `border-bottom`, `border-left`
- Slogi: `solid`, `dashed`, `dotted`, `double`

### Oblikovanje besedila

**`color`**
```css
p { color: red; }
```
- Barva besedila

**`font-size`**
```css
h1 { font-size: 24px; }
```
- Velikost pisave

**`font-weight`**
```css
strong { font-weight: bold; }
```
- Debelina pisave: `normal`, `bold`, `100-900`

**`text-align`**
```css
h1 { text-align: center; }
```
- Poravnava: `left`, `center`, `right`, `justify`

### Druge lastnosti

**`background-color`**
```css
body { background-color: #f0f0f0; }
```
- Barva ozadja

**`float`**
```css
img { float: left; }
```
- Element "plava" levo ali desno
- Vrednosti: `left`, `right`, `none`

### Barve

**Po imenu:**
```css
color: red;
color: blue;
color: lightgray;
```

**Heksadecimalno:**
```css
color: #FF0000; /* rdeča */
color: #00FF00; /* zelena */
color: #0000FF; /* modra */
```

**RGB:**
```css
color: rgb(255, 0, 0); /* rdeča */
background-color: rgba(255, 0, 0, 0.5); /* rdeča s 50% prosojnostjo */
```

### Merske enote

**Točke (pixels):**
```css
width: 400px;
font-size: 16px;
```

**Em:**
```css
font-size: 2em; /* 2x velikost starševskega elementa */
```

**Odstotki:**
```css
width: 50%; /* 50% širine starševskega elementa */
```

---

## 4. LaTeX

### Struktura dokumenta

```latex
\documentclass[a4paper,12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[slovene]{babel}
\usepackage[T1]{fontenc}

\title{Naslov dokumenta}
\author{Ime Priimek}
\date{\today}

\begin{document}

\maketitle

\begin{abstract}
Povzetek dokumenta.
\end{abstract}

\tableofcontents

\section{Uvod}
Besedilo...

\end{document}
```

### Preambula

**`\documentclass`**
```latex
\documentclass[a4paper,12pt]{article}
```
- Določa razred dokumenta
- Možnosti: `article`, `beamer`, `book`, `report`
- Parametri: `a4paper`, `10pt`, `11pt`, `12pt`, `14pt`

**Paketi za slovenščino:**
```latex
\usepackage[utf8]{inputenc}      % kodiranje
\usepackage[slovene]{babel}      % slovenski jezik
\usepackage[T1]{fontenc}         % pisave
```

**Pomembni paketi:**
```latex
\usepackage{amsmath}      % matematika
\usepackage{amssymb}      % matematični simboli
\usepackage{amsthm}       % okolja za trditve
\usepackage{hyperref}     % hiperpovezave
\usepackage{booktabs}     % lepše tabele
\usepackage{graphicx}     % slike
\usepackage{tikz}         % risanje
\usepackage{pgfplots}     % grafi
```

**`\newcommand`**
```latex
\newcommand{\p}{\mathbb{P}}
```
- Definira nov ukaz
- `\p` bo postal `\mathbb{P}`

**`\newtheorem`**
```latex
\theoremstyle{definition}
\newtheorem{definicija}{Definicija}
\newtheorem{algoritem}{Algoritem}

\theoremstyle{plain}
\newtheorem{izrek}{Izrek}
```
- Definira nova okolja za trditve
- Slogi: `plain`, `definition`, `remark`

### Vsebina dokumenta

**Naslov:**
```latex
\title{Naslov dokumenta}
\author{Ime Priimek}
\date{\today}          % ali \date{25. januar 2025}
\maketitle             % izpiše naslov
```

**Povzetek in kazalo:**
```latex
\begin{abstract}
Kratek povzetek vsebine dokumenta.
\end{abstract}

\tableofcontents  % kazalo
```

**Vključitev datotek:**
```latex
\input{poglavje1.tex}
```
- Vključi vsebino druge datoteke

### Razdelki

```latex
\section{Naslov razdelka}
\subsection{Naslov podrazdelka}
\subsubsection{Naslov podpodrazdelka}
```
- Avtomatsko oštevilčeni
- Za neoštevilčene: `\section*{Naslov}`

### Oblikovanje besedila

```latex
\emph{poudarjeno}         % poudarek (ležeče)
\textbf{krepko}           % krepko
\textit{ležeče}           % ležeče
\texttt{monospace}        % pisava pisalnega stroja
\verb|print("hello")|     % dobesedno (ne interpretira LaTeX)
\url{https://...}         % URL naslov
```

**Poravnava:**
```latex
\noindent                 % brez zamika
\centering                % centriranje (v okolju)

\begin{center}
Centriran tekst.
\end{center}
```

**Dobesedno besedilo:**
```latex
\begin{verbatim}
def funkcija():
    return True
\end{verbatim}
```

### Seznami

**Neurejen seznam:**
```latex
\begin{itemize}
    \item Prvi element
    \item Drugi element
\end{itemize}
```

**Urejen seznam:**
```latex
\begin{enumerate}
    \item Prvi korak
    \item Drugi korak
\end{enumerate}
```

**Gnezdeni seznami:**
```latex
\begin{itemize}
    \item Prvi nivo
    \begin{itemize}
        \item Drugi nivo
    \end{itemize}
\end{itemize}
```

### Tabele

**Osnovna tabela:**
```latex
\begin{table}[h]
\centering
\begin{tabular}{|l|c|r|}
\hline
Levo & Center & Desno \\
\hline
a & b & c \\
d & e & f \\
\hline
\end{tabular}
\caption{Opis tabele}
\label{tab:primer}
\end{table}
```

**Specifikacija stolpcev:**
- `l`: levo poravnano
- `c`: centrirano
- `r`: desno poravnano
- `|`: navpična črta

**Črte v tabelah:**
```latex
\hline                    % vodoravna črta
\toprule                  % zgornja črta (booktabs)
\midrule                  % srednja črta (booktabs)
\bottomrule               % spodnja črta (booktabs)
```

**Spajanje stolpcev:**
```latex
\multicolumn{2}{c}{Naslov}  % 2 stolpca, centrirano
```

### Slike

**Vključitev slike:**
```latex
\begin{figure}[h]
\centering
\includegraphics[width=0.5\textwidth]{slika.png}
\caption{Opis slike}
\label{fig:primer}
\end{figure}
```

**Parametri položaja:**
- `h`: here (tukaj)
- `t`: top (na vrhu)
- `b`: bottom (na dnu)
- `p`: page (na svoji strani)

**Več slik skupaj:**
```latex
\begin{figure}[h]
\centering
\begin{subfigure}[b]{0.4\textwidth}
    \includegraphics[width=\textwidth]{slika1.png}
    \caption{Prva slika}
    \label{fig:prva}
\end{subfigure}
\begin{subfigure}[b]{0.4\textwidth}
    \includegraphics[width=\textwidth]{slika2.png}
    \caption{Druga slika}
    \label{fig:druga}
\end{subfigure}
\caption{Skupni naslov}
\end{figure}
```

### Sklici

```latex
\label{eq:formula}        % označi element
\ref{eq:formula}          % sklicuj se na številko
\eqref{eq:formula}        % sklicuj se na enačbo (v oklepajih)
\pageref{eq:formula}      % številka strani
```

### Citati

```latex
\cite{kljuc}              % citat
\nocite{kljuc}            % citat brez reference v tekstu
\bibliographystyle{plain} % stil bibliografije
\bibliography{viri}       % vključi .bib datoteko
```

### Beamer (predstavitve)

**Osnovna struktura:**
```latex
\documentclass{beamer}
\usetheme{Berlin}

\begin{document}

\begin{frame}
\titlepage
\end{frame}

\begin{frame}{Naslov okvirja}
Vsebina...
\end{frame}

\end{document}
```

**Teme:**
- `Berlin`, `Madrid`, `Copenhagen`, `Warsaw`, ...

**Bloki:**
```latex
\begin{block}{Naslov bloka}
Vsebina bloka.
\end{block}

\begin{exampleblock}{Primer}
Primer vsebine.
\end{exampleblock}

\begin{alertblock}{Opozorilo}
Pomembna informacija!
\end{alertblock}
```

**Postopno odkrivanje:**
```latex
\pause                    % premor

\onslide<2>{Prikaže se na 2. koraku}
\only<3>{Prikaže se samo na 3. koraku}

\begin{itemize}[<+->]     % postopno odkrivanje
    \item Prvi
    \item Drugi
    \item Tretji
\end{itemize}
```

**Stolpci:**
```latex
\begin{columns}
\column{0.5\textwidth}
Levi stolpec

\column{0.5\textwidth}
Desni stolpec
\end{columns}
```

### Matematika

**Vrstični način:**
```latex
Formula $a^2 + b^2 = c^2$ v besedilu.
\(E = mc^2\) alternativna sintaksa.
```

**Prikazni način:**
```latex
\[
    \int_0^\infty e^{-x} dx = 1
\]
```

**Matematični simboli:**
```latex
\alpha, \beta, \gamma     % grške črke
\infty                    % neskončno
\sum_{i=1}^n              % vsota
\int_a^b                  % integral
\lim_{x \to 0}            % limita
\frac{a}{b}               % ulomek
\sqrt{x}                  % koren
\binom{n}{k}              % binomski simbol
\leq, \geq                % ≤, ≥
\in, \notin               % ∈, ∉
\emptyset                 % prazna množica
\mathbb{R}, \mathbb{N}    % množice
\forall, \exists          % ∀, ∃
```

**Funkcije:**
```latex
\sin x, \cos x, \tan x
\log x, \ln x, \exp x
\lim_{x \to 0} f(x)
```
- NE piši samo `sin`, ampak `\sin`!

**Prikazna okolja:**
```latex
\begin{equation}
E = mc^2
\label{eq:einstein}
\end{equation}

\begin{align}
a &= b + c \\
  &= d + e
\end{align}

\begin{multline}
Zelo dolga enačba = \\
ki se nadaljuje na drugi vrstici
\end{multline}
```
- Za neoštevilčene: `equation*`, `align*`, `multline*`

**Cases (po kosih definirana funkcija):**
```latex
\[
f(x) = \begin{cases}
x^2 & \text{če } x \geq 0 \\
-x  & \text{če } x < 0
\end{cases}
\]
```

**Matrike:**
```latex
\begin{pmatrix}         % okrogli oklepaji
a & b \\
c & d
\end{pmatrix}

\begin{bmatrix}         % oglati oklepaji
a & b \\
c & d
\end{bmatrix}

\begin{vmatrix}         % determinanta
a & b \\
c & d
\end{vmatrix}
```

**Pisave v matematiki:**
```latex
\mathbb{R}              % blackboard bold (množice)
\mathcal{F}             % kaligrafija
\mathsf{ABC}            % sans-serif
\mathtt{text}           % typewriter
\mathrm{log}            % roman (funkcije)
\text{besedilo}         % besedilo v matematiki
```

**Pomembno:**
- Prazna množica: `\emptyset`, NE `\phi`
- Element: `\in`, NE `\epsilon`
- Enakosti: poravnaj z `&=`

---

## 5. EXCEL

### Uvoz CSV datotek

**Postopek:**
1. Data > Get Data > From File > From Text/CSV
2. Izberi datoteko
3. Nastavi:
   - **File Origin**: UTF-8
   - **Delimiter**: 
     - `;` (podpičje) za slovenske CSV
     - `,` (vejica) za angleške CSV
   - **Data Type Detection**: Based on entire dataset
4. Load

**Decimalni separator:**
- Slovenski CSV: vejica (3,14)
- Angleški CSV: pika (3.14)
- Excel mora pravilno prepoznati!

### Osnovne formule

**Seštevanje:**
```
=SUM(A1:A10)            % vsota od A1 do A10
=A1+A2+A3               % direktno seštevanje
```

**Povprečje:**
```
=AVERAGE(B1:B10)
```

**Pogojni stavki:**
```
=IF(A1>100, "Veliko", "Malo")
=IF(A1>100, "Veliko", IF(A1>50, "Srednje", "Malo"))
```

**Štetje:**
```
=COUNT(A1:A10)          % šteje številke
=COUNTA(A1:A10)         % šteje neprazne celice
```

**Matematične operacije:**
```
=A1*B1                  % množenje
=A1/B1                  % deljenje
=A1^2                   % potenca
=SQRT(A1)               % koren
```

**Funkcija MONTH:**
```
=MONTH(A1)              % izloči mesec iz datuma
```
- Če je v A1 datum "15.3.2024", vrne 3

### Formatiranje celic

**Število decimalk:**
1. Izberi celice
2. Home > Number > Increase/Decrease Decimal
3. Ali: Format Cells > Number > Decimal places

**Valute:**
1. Home > Number > Currency
2. Izberi simbol (€, $, ...)

**Odstotki:**
1. Home > Number > Percentage
2. Avtomatično pomnoži z 100 in doda %

**Drugo:**
- Date: za datume
- Text: za besedilo (Excel ne interpretira kot številke)

### Tabele

**Ustvarjanje tabele:**
1. Izberi podatke
2. Insert > Table (ali Ctrl+T)
3. Potrdi, da ima prva vrstica glave

**Prednosti tabel:**
- Avtomatsko filtriranje
- Enostavno dodajanje formul
- Lepo oblikovanje
- Strukturirane reference: `=[@Cena]*[@Količina]`

### Pogojno oblikovanje

**Osnovni postopek:**
1. Izberi celice
2. Home > Conditional Formatting

**Vrednosti nad/pod mejo:**
- Highlight Cells Rules > Greater Than... (100, zelena)
- Highlight Cells Rules > Less Than... (50, rdeča)

**Barvne lestvice:**
- Color Scales > izberite barvno shemo
- Nižje vrednosti ena barva, višje druga

**Ikone:**
- Icon Sets > puščice, semaforji, ...

### Vrtilne tabele (Pivot Tables)

**Ustvarjanje:**
1. Izberi podatke
2. Insert > PivotTable
3. Izberi, kam jo postaviti (nov list ali obstoječi)

**Konfiguracija:**
- **Rows**: kaj bo v vrsticah (npr. Mesec)
- **Columns**: kaj bo v stolpcih (npr. Regija)
- **Values**: katere vrednosti računamo (npr. Povprečje prodaje)
  - Klikni na vrednost > Value Field Settings > izberite funkcijo (Sum, Average, Count, ...)

**Primer:**
- Vrstice: Mesec
- Stolpci: Regija
- Vrednosti: Average of Prodaja
- Rezultat: povprečna prodaja po regijah in mesecih

---

## 6. MATHEMATICA

### Osnove

**Matematične operacije:**
```mathematica
2 + 3                   (* seštevanje *)
5 - 2                   (* odštevanje *)
3 * 4                   (* množenje *)
10 / 2                  (* deljenje *)
2^3                     (* potenciranje *)
Sqrt[16]                (* koren *)
```

**Grške črke:**
- Vpiši `\alpha` in pritisni Esc: α
- `\beta`: β
- `\gamma`: γ
- `\pi`: π
- itd.

**Posebni znaki:**
- Potenca: Ctrl+6 (ali ^)
- Subscript: Ctrl+- 
- Fraction: Ctrl+/

### Spremenljivke in funkcije

**Shranjevanje vrednosti:**
```mathematica
x = 5
y = 10
z = x + y               (* z = 15 *)
```

**Definiranje funkcij:**
```mathematica
f[x_] := x^2 + 1
f[3]                    (* vrne 10 *)

g[x_, y_] := x^2 + y^2
g[3, 4]                 (* vrne 25 *)
```
- Podčrtaj `_` označuje parameter!
- `:=` za definicijo, `=` za vrednost

### Barve spremenljivk

- **Črna**: definirana vrednost (npr. `x = 5`)
- **Zelena**: vezana spremenljivka (parameter funkcije)
- **Modra**: neznan simbol (še ni definiran)

Če dobite napako, preverite barve!

### Dokumentacija

**Poizvedba:**
```mathematica
?Plot                   (* pomoč za funkcijo Plot *)
??Plot                  (* več podrobnosti *)
```

### Čiščenje spremenljivk

**Pomembno pred vsako nalogo:**
```mathematica
ClearAll[x, y, z, f, g]
```
- Počisti vse definicije
- Prepreči napake zaradi starih vrednosti

### Preoblikovanje izrazov

**Razširjanje:**
```mathematica
Expand[(x + 1)^3]
(* vrne x^3 + 3x^2 + 3x + 1 *)
```

**Faktorizacija:**
```mathematica
Factor[x^2 - 1]
(* vrne (x-1)(x+1) *)
```

**Poenostavljanje:**
```mathematica
Simplify[Sin[x]^2 + Cos[x]^2]
(* vrne 1 *)
```

### Vsote in limite

**Vsota:**
```mathematica
Sum[i^2, {i, 1, 10}]    (* 1^2 + 2^2 + ... + 10^2 *)
Sum[1/n^2, {n, 1, Infinity}]  (* neskončna vsota *)
```

**Limita:**
```mathematica
Limit[Sin[x]/x, x -> 0]
(* vrne 1 *)

Limit[(1 + 1/n)^n, n -> Infinity]
(* vrne E *)
```

### Odvodi in integrali

**Odvod:**
```mathematica
D[x^3, x]               (* 3x^2 *)
D[Sin[x], x]            (* Cos[x] *)
D[x^2 * y^3, x]         (* 2xy^3 *)
D[x^2 * y^3, y]         (* 3x^2*y^2 *)
```

**Integral:**
```mathematica
Integrate[x^2, x]       (* nedoločeni: x^3/3 *)
Integrate[x^2, {x, 0, 1}]  (* določeni: 1/3 *)
Integrate[E^(-x^2), {x, -Infinity, Infinity}]  (* Sqrt[Pi] *)
```

### Reševanje enačb

**Simbolno:**
```mathematica
Solve[x^2 - 5x + 6 == 0, x]
(* vrne {{x -> 2}, {x -> 3}} *)

Solve[{x + y == 5, x - y == 1}, {x, y}]
(* sistem enačb *)
```

**Numerično:**
```mathematica
NSolve[x^5 - x - 1 == 0, x]
(* numerične rešitve *)
```

**Poenostavljanje sistemov:**
```mathematica
Reduce[x^2 - 4 > 0, x]
(* vrne x < -2 || x > 2 *)

Reduce[{x > 0, y > 0, x + y < 10}, {x, y}]
```

**Iskanje ničel:**
```mathematica
FindRoot[Cos[x] == x, {x, 0}]
(* numerično poišče ničlo blizu 0 *)
```

### Risanje grafov

**Navaden graf:**
```mathematica
Plot[Sin[x], {x, 0, 2 Pi}]
Plot[{Sin[x], Cos[x]}, {x, 0, 2 Pi}]  (* več funkcij *)
```

**Parametrični graf:**
```mathematica
ParametricPlot[{Cos[t], Sin[t]}, {t, 0, 2 Pi}]
(* riše krog *)
```

**Nivojnice:**
```mathematica
ContourPlot[x^2 + y^2, {x, -2, 2}, {y, -2, 2}]
```

**Področja:**
```mathematica
RegionPlot[x^2 + y^2 < 1, {x, -2, 2}, {y, -2, 2}]
(* obarva notranjost kroga *)
```

**3D graf:**
```mathematica
Plot3D[Sin[x] * Cos[y], {x, 0, 2 Pi}, {y, 0, 2 Pi}]
```

**Opcije za grafe:**
```mathematica
Plot[Sin[x], {x, 0, 2 Pi},
  PlotLabel -> "Sinus",
  AxesLabel -> {"x", "y"},
  PlotStyle -> Red
]
```

---

## PRAKTIČNI NASVETI ZA IZPIT

### Organizacija dela

1. **Preberi VSA navodila** pred začetkom
2. **Preveri datoteke** - ali imaš vse?
3. **Ustvari mapo** za izpit, vse shranjuj noter
4. **Delaj po vrsti**, a ne obsedi pri težki nalogi
5. **Sproti shranjuj** (Ctrl+S vsake 2 minuti)
6. **Na koncu:** vse stisni v PriimekIme.zip

### Visual Studio Code

- Uporabi paleto ukazov (Ctrl+Shift+P) za hitre transformacije
- Več kurzorjev: Ctrl+D za iste besede
- Iskanje in zamenjava: Ctrl+H za globalne zamenjave
- Ne pozabi na Regex možnost pri iskanju

### HTML & CSS

- Vedno preveri, ali si vključil CSS: `<link rel="stylesheet" href="...">` 
- UTF-8: `<meta charset="UTF-8">`
- Ne pozabi na `alt` atribut pri slikah
- ID je unikaten, class ni
- Preveri črkovanje razredov in ID-jev!

### LaTeX

- Vedno začni s ClearAll
- Preveri kodiranje: `utf8`, `slovene`, `T1`
- Paketi: naloži samo tiste, ki jih rabiš
- Preveri razliko: `$...# Računalniški praktikum - Podrobna priprava na izpit

## 1. VISUAL STUDIO CODE

### Delo z datotečnim sistemom
- **Odpiranje map/projektov**: File > Open Folder (Ctrl+K Ctrl+O)
- **Ustvarjanje datotek**: Klik na ikono "New File" v Explorer ali Ctrl+N
- **Shranjevanje**: Ctrl+S (posamezna datoteka), Ctrl+K S (vse datoteke)
- **Preklapljanje med datotekami**: Ctrl+Tab

### Paleta ukazov
- **Odpiranje palete**: Ctrl+Shift+P ali F1
- Omogoča dostop do vseh ukazov brez uporabe miške
- Primer uporabe: "Transform to Uppercase", "Sort Lines Ascending"

### Bližnjice na tipkovnici

**Osnovno urejanje:**
- Ctrl+C: kopiraj
- Ctrl+X: izreži
- Ctrl+V: prilepi
- Ctrl+Z: razveljavi
- Ctrl+Shift+Z: uveljavi
- Ctrl+/: komentiraj/odkomentiraj vrstico

**Izbiranje:**
- Ctrl+A: izberi vse
- Shift+puščice: razširi izbor
- Ctrl+L: izberi celotno vrstico

### Hitro premikanje

**Med besedami:**
- Ctrl+puščica levo/desno: skok med besedami
- Ctrl+Shift+puščica: izberi do naslednje besede

**Na začetek/konec vrstice:**
- Home: začetek vrstice
- End: konec vrstice
- Ctrl+Home: začetek dokumenta
- Ctrl+End: konec dokumenta

**Po vrsticah:**
- Ctrl+G: skok na določeno vrstico (vneseš številko)
- Ctrl+P: hitro iskanje datotek

### Iskanje in zamenjava

**V trenutni datoteki:**
- Ctrl+F: iskanje
- Ctrl+H: zamenjava
- F3 ali Enter: naslednja pojavitev
- Shift+F3: prejšnja pojavitev
- Alt+Enter: izberi vse pojavitve

**V celotnem projektu:**
- Ctrl+Shift+F: iskanje v projektih
- Ctrl+Shift+H: zamenjava v projektih
- Lahko uporabiš regex (klik na ikono .*)

**Praktični primeri:**
- Najdi vse `.png` datoteke: uporabi `*.png` v iskanju
- Zamenjaj `%` z `\section`: Ctrl+H, vpiši `%` in `\section`

### Več kurzorjev

**Dodajanje z miško:**
- Alt+klik: doda kurzor na položaj klika
- Uporabno za urejanje več vrstic naenkrat

**Razširitev na sosednje vrstice:**
- Ctrl+Alt+puščica gor/dol: dodaj kurzor na zgornjo/spodnjo vrstico
- Lahko urediš več vrstic sočasno

**Na pojavitve besede:**
- Ctrl+D: izberi naslednjo pojavitev besede pod kurzorjem
- Ctrl+Shift+L: izberi vse pojavitve besede
- Primer: izberi "TODO", pritisni Ctrl+Shift+L, zapiši "DONE"

### Urejanje vrstic

**Podvajanje:**
- Shift+Alt+puščica gor/dol: podvoji vrstico gor/dol
- Ctrl+Shift+D: podvoji vrstico (alternativa)

**Premikanje:**
- Alt+puščica gor/dol: premakni vrstico gor/dol

**Zamikanje:**
- Tab: zamakni desno
- Shift+Tab: zamakni levo
- Ctrl+] / Ctrl+[: zamakni izbor desno/levo

**Komentiranje:**
- Ctrl+/: vklopni/izklopni komentiranje (// v večini jezikov)
- Shift+Alt+A: blokovski komentar (/* */ v večini jezikov)

---

## 2. HTML

### Struktura HTML dokumenta

```html
<!DOCTYPE html>
<html>
<head>
    <title>Naslov strani</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Vsebina dokumenta -->
</body>
</html>
```

### Glava dokumenta

**`<!DOCTYPE html>`**
- Deklaracija tipa dokumenta
- Pove brskalniku, da gre za HTML5 dokument
- Vedno prva vrstica v HTML datoteki

**`<html>`**
- Korenski element HTML dokumenta
- Vsebuje celoten dokument

**`<head>`**
- Glava dokumenta
- Vsebuje metapodatke (informacije o dokumentu)
- Ni vidna na strani

**`<title>`**
- Naslov dokumenta
- Prikazan v zavihku brskalnika
- Primer: `<title>Moja spletna stran</title>`

**`<link>`**
- Povezava na zunanje vire (CSS, ikone, ...)
- Primer: `<link rel="stylesheet" href="oblikovanje.css">`
- `rel` določa relacijo (relationship)
- `href` je pot do datoteke

**`<meta>`**
- Metapodatki o dokumentu
- `<meta charset="UTF-8">` določa kodiranje znakov
- UTF-8 podpira šumnike in posebne znake

### Struktura dokumenta

**`<!--...-->`**
- HTML komentar
- Ni viden na strani
- Primer: `<!-- To je komentar -->`

**`<body>`**
- Telo dokumenta
- Vsebuje vso vidno vsebino strani

**`<div>`**
- Generični vsebnik (division)
- Uporaben za skupinsko oblikovanje elementov
- Primer: `<div class="container">...</div>`

**`<h1>`, `<h2>`, ... `<h6>`**
- Naslovi različnih ravni
- `<h1>` je največji (glavni naslov)
- `<h6>` je najmanjši
- Primer: `<h1>Glavni naslov</h1>`

### Oblikovanje vsebine

**`<a>`**
- Povezava (anchor)
- `href` atribut določa cilj
- Primeri:
  - `<a href="https://www.wikipedia.org">Wikipedia</a>`
  - `<a href="#razdelek">Skok na razdelek</a>` (notranja povezava)
  - `<a href="dokument.pdf">Prenesi PDF</a>`

**`<blockquote>`**
- Daljši citat iz drugega vira
- Primer: `<blockquote>To je citat.</blockquote>`

**`<br>`**
- Prelom vrstice (break)
- Samozapirajoča značka
- Primer: `Prva vrstica<br>Druga vrstica`

**`<code>`**
- Koda (kratek odsek)
- Monospace pisava
- Primer: `Uporabi funkcijo <code>printf()</code>`

**`<em>`**
- Poudarek (emphasis)
- Običajno prikazano kot ležeče
- Primer: `<em>pomembno</em>`

**`<hr>`**
- Horizontalna črta (horizontal rule)
- Samozapirajoča značka
- Uporablja se za ločevanje vsebin

**`<img>`**
- Slika (image)
- Samozapirajoča značka
- Primer: `<img src="slika.jpg" alt="Opis slike">`
- `src`: pot do slike
- `alt`: alternativen tekst (dostopnost)

**`<kbd>`**
- Tipka na tipkovnici (keyboard)
- Primer: `Pritisni <kbd>Ctrl</kbd>+<kbd>C</kbd>`

**`<p>`**
- Odstavek (paragraph)
- Primer: `<p>To je odstavek besedila.</p>`

**`<pre>`**
- Predformatirano besedilo (preformatted)
- Ohrani presledke in nove vrstice
- Uporabno za kodo
```html
<pre>
def funkcija():
    return True
</pre>
```

**`<small>`**
- Manjše besedilo
- Primer: `<small>Drobni tisk</small>`

**`<span>`**
- Generični vsebnik za vrstično vsebino
- Za oblikovanje dela besedila
- Primer: `<span class="rdeče">Pomembno</span>`

**`<strong>`**
- Močan poudarek
- Običajno prikazano krepko
- Primer: `<strong>zelo pomembno</strong>`

### Seznami

**`<ul>` - Neurejen seznam (unordered list)**
```html
<ul>
    <li>Prvi element</li>
    <li>Drugi element</li>
</ul>
```
- Prikazan s kroglicami

**`<ol>` - Urejen seznam (ordered list)**
```html
<ol>
    <li>Prvi korak</li>
    <li>Drugi korak</li>
</ol>
```
- Prikazan z številkami

**`<li>` - Element seznama (list item)**
- Uporablja se znotraj `<ul>` ali `<ol>`

**`<dl>`, `<dt>`, `<dd>` - Seznam definicij**
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
</dl>
```
- `<dl>`: definition list
- `<dt>`: definition term (izraz)
- `<dd>`: definition description (opis)

### Tabele

```html
<table>
    <thead>
        <tr>
            <th>Stolpec 1</th>
            <th>Stolpec 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Podatek 1</td>
            <td>Podatek 2</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Noga 1</td>
            <td>Noga 2</td>
        </tr>
    </tfoot>
</table>
```

**`<table>`** - Tabela
**`<thead>`** - Glava tabele (table head)
**`<tbody>`** - Telo tabele (table body)
**`<tfoot>`** - Noga tabele (table foot)
**`<tr>`** - Vrstica tabele (table row)
**`<th>`** - Celica glave (table header)
**`<td>`** - Celica s podatki (table data)

### Splošni atributi

**`id`**
- Unikaten identifikator elementa
- Primer: `<div id="glava">...</div>`
- Za sklicevanje: `<a href="#glava">Pojdi na glavo</a>`

**`class`**
- Razred elementa (lahko več elementov ima isti razred)
- Primer: `<p class="pomembno">...</p>`
- Za CSS: `.pomembno { color: red; }`

---

## 3. CSS

### Osnovni izbiralci

**Po znački:**
```css
p {
    color: blue;
}
```
- Izbere vse `<p>` elemente

**Po razredu:**
```css
.pomembno {
    font-weight: bold;
}
```
- Izbere vse elemente z `class="pomembno"`
- Začne se s piko (.)

**Po identifikatorju:**
```css
#glava {
    background-color: gray;
}
```
- Izbere element z `id="glava"`
- Začne se z lojtrco (#)

**Univerzalni izbiralec:**
```css
* {
    margin: 0;
    padding: 0;
}
```
- Izbere vse elemente

### Sestavljeni izbiralci

**Potomci (descendants):**
```css
table a {
    color: red;
}
```
- Izbere vse `<a>` elemente znotraj `<table>`
- Ne glede na globino

**Disjunkcija (vejica):**
```css
h1, h2, h3 {
    font-family: Arial;
}
```
- Izbere vse `<h1>`, `<h2>` IN `<h3>` elemente

**Konjunkcija (brez presledka):**
```css
p.pomembno {
    background-color: yellow;
}
```
- Izbere `<p>` elemente, ki imajo `class="pomembno"`

### Izbiralci atributov

**Obstoj atributa:**
```css
[href] {
    text-decoration: underline;
}
```
- Izbere vse elemente z atributom `href`

**Točna vrednost:**
```css
[type="text"] {
    border: 1px solid black;
}
```
- Izbere elemente z `type="text"`

### Psevdo-razredi

**`:hover`**
```css
a:hover {
    color: red;
}
```
- Aktivira se, ko miška lebdi nad elementom

**`:nth-child(even)` / `:nth-child(odd)`**
```css
tr:nth-child(even) {
    background-color: #f2f2f2;
}
```
- `even`: sodi elementi (2, 4, 6, ...)
- `odd`: lihi elementi (1, 3, 5, ...)

**`:last-child`**
```css
li:last-child {
    border-bottom: none;
}
```
- Izbere zadnji element med sorojenci

**`:first-child`**
```css
p:first-child {
    margin-top: 0;
}
```
- Izbere prvi element med sorojenci

### Lastnosti za dimenzije

**`width` / `height`**
```css
img {
    width: 400px;
    height: 300px;
}
```
- Širina in višina elementa

### Škatlasti model (Box Model)

```
+---------------------------+
|        margin             |
|  +---------------------+  |
|  |     border          |  |
|  |  +---------------+  |  |
|  |  |   padding     |  |  |
|  |  |  +---------+  |  |  |
|  |  |  | content |  |  |  |
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

**`margin`**
- Prostor zunaj obrobe
- `margin: 10px;` (vsi robovi)
- `margin-top`, `margin-right`, `margin-bottom`, `margin-left`

**`padding`**
- Prostor znotraj obrobe
- `padding: 10px;` (vsi robovi)
- `padding-top`, `padding-right`, `padding-bottom`, `padding-left`

**`border`**
- Obroba elementa
- `border: 2px solid black;` (debelina slog barva)
- `border-top`, `border-right`, `border-bottom`, `border-left`
- Slogi: `solid`, `dashed`, `dotted`, `double`

### Oblikovanje besedila

**`color`**
```css
p { color: red; }
```
- Barva besedila

**`font-size`**
```css
h1 { font-size: 24px; }
```
- Velikost pisave

**`font-weight`**
```css
strong { font-weight: bold; }
```
- Debelina pisave: `normal`, `bold`, `100-900`

**`text-align`**
```css
h1 { text-align: center; }
```
- Poravnava: `left`, `center`, `right`, `justify`

### Druge lastnosti

**`background-color`**
```css
body { background-color: #f0f0f0; }
```
- Barva ozadja

**`float`**
```css
img { float: left; }
```
- Element "plava" levo ali desno
- Vrednosti: `left`, `right`, `none`

### Barve

**Po imenu:**
```css
color: red;
color: blue;
color: lightgray;
```

**Heksadecimalno:**
```css
color: #FF0000; /* rdeča */
color: #00FF00; /* zelena */
color: #0000FF; /* modra */
```

**RGB:**
```css
color: rgb(255, 0, 0); /* rdeča */
background-color: rgba(255, 0, 0, 0.5); /* rdeča s 50% prosojnostjo */
```

### Merske enote

**Točke (pixels):**
```css
width: 400px;
font-size: 16px;
```

**Em:**
```css
font-size: 2em; /* 2x velikost starševskega elementa */
```

**Odstotki:**
```css
width: 50%; /* 50% širine starševskega elementa */
```

---

## 4. LaTeX

### Struktura dokumenta

```latex
\documentclass[a4paper,12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[slovene]{babel}
\usepackage[T1]{fontenc}

\title{Naslov dokumenta}
\author{Ime Priimek}
\date{\today}

\begin{document}

\maketitle

\begin{abstract}
Povzetek dokumenta.
\end{abstract}

\tableofcontents

\section{Uvod}
Besedilo...

\end{document}
```

### Preambula

**`\documentclass`**
```latex
\documentclass[a4paper,12pt]{article}
```
- Določa razred dokumenta
- Možnosti: `article`, `beamer`, `book`, `report`
- Parametri: `a4paper`, `10pt`, `11pt`, `12pt`, `14pt`

**Paketi za slovenščino:**
```latex
\usepackage[utf8]{inputenc}      % kodiranje
\usepackage[slovene]{babel}      % slovenski jezik
\usepackage[T1]{fontenc}         % pisave
```

**Pomembni paketi:**
```latex
\usepackage{amsmath}      % matematika
\usepackage{amssymb}      % matematični simboli
\usepackage{amsthm}       % okolja za trditve
\usepackage{hyperref}     % hiperpovezave
\usepackage{booktabs}     % lepše tabele
\usepackage{graphicx}     % slike
\usepackage{tikz}         % risanje
\usepackage{pgfplots}     % grafi
```

**`\newcommand`**
```latex
\newcommand{\p}{\mathbb{P}}
```
- Definira nov ukaz
- `\p` bo postal `\mathbb{P}`

**`\newtheorem`**
```latex
\theoremstyle{definition}
\newtheorem{definicija}{Definicija}
\newtheorem{algoritem}{Algoritem}

\theoremstyle{plain}
\newtheorem{izrek}{Izrek}
```
- Definira nova okolja za trditve
- Slogi: `plain`, `definition`, `remark`

### Vsebina dokumenta

**Naslov:**
```latex
\title{Naslov dokumenta}
\author{Ime Priimek}
\date{\today}          % ali \date{25. januar 2025}
\maketitle             % izpiše naslov
```

**Povzetek in kazalo:**
```latex
\begin{abstract}
Kratek povzetek vsebine dokumenta.
\end{abstract}

\tableofcontents  % kazalo
```

**Vključitev datotek:**
```latex
\input{poglavje1.tex}
```
- Vključi vsebino druge datoteke

### Razdelki

```latex
\section{Naslov razdelka}
\subsection{Naslov podrazdelka}
\subsubsection{Naslov podpodrazdelka}
```
- Avtomatsko oštevilčeni
- Za neoštevilčene: `\section*{Naslov}`

### Oblikovanje besedila

```latex
\emph{poudarjeno}         % poudarek (ležeče)
\textbf{krepko}           % krepko
\textit{ležeče}           % ležeče
\texttt{monospace}        % pisava pisalnega stroja
\verb|print("hello")|     % dobesedno (ne interpretira LaTeX)
\url{https://...}         % URL naslov
```

**Poravnava:**
```latex
\noindent                 % brez zamika
\centering                % centriranje (v okolju)

\begin{center}
Centriran tekst.
\end{center}
```

**Dobesedno besedilo:**
```latex
\begin{verbatim}
def funkcija():
    return True
\end{verbatim}
```

### Seznami

**Neurejen seznam:**
```latex
\begin{itemize}
    \item Prvi element
    \item Drugi element
\end{itemize}
```

**Urejen seznam:**
```latex
\begin{enumerate}
    \item Prvi korak
    \item Drugi korak
\end{enumerate}
```

**Gnezdeni seznami:**
```latex
\begin{itemize}
    \item Prvi nivo
    \begin{itemize}
        \item Drugi nivo
    \end{itemize}
\end{itemize}
```

### Tabele

**Osnovna tabela:**
```latex
\begin{table}[h]
\centering
\begin{tabular}{|l|c|r|}
\hline
Levo & Center & Desno \\
\hline
a & b & c \\
d & e & f \\
\hline
\end{tabular}
\caption{Opis tabele}
\label{tab:primer}
\end{table}
```

**Specifikacija stolpcev:**
- `l`: levo poravnano
- `c`: centrirano
- `r`: desno poravnano
- `|`: navpična črta

**Črte v tabelah:**
```latex
\hline                    % vodoravna črta
\toprule                  % zgornja črta (booktabs)
\midrule                  % srednja črta (booktabs)
\bottomrule               % spodnja črta (booktabs)
```

**Spajanje stolpcev:**
```latex
\multicolumn{2}{c}{Naslov}  % 2 stolpca, centrirano
```

### Slike

**Vključitev slike:**
```latex
\begin{figure}[h]
\centering
\includegraphics[width=0.5\textwidth]{slika.png}
\caption{Opis slike}
\label{fig:primer}
\end{figure}
```

**Parametri položaja:**
- `h`: here (tukaj)
- `t`: top (na vrhu)
- `b`: bottom (na dnu)
- `p`: page (na svoji strani)

**Več slik skupaj:**
```latex
\begin{figure}[h]
\centering
\begin{subfigure}[b]{0.4\textwidth}
    \includegraphics[width=\textwidth]{slika1.png}
    \caption{Prva slika}
    \label{fig:prva}
\end{subfigure}
\begin{subfigure}[b]{0.4\textwidth}
    \includegraphics[width=\textwidth]{slika2.png}
    \caption{Druga slika}
    \label{fig:druga}
\end{subfigure}
\caption{Skupni naslov}
\end{figure}
```

### Sklici

```latex
\label{eq:formula}        % označi element
\ref{eq:formula}          % sklicuj se na številko
\eqref{eq:formula}        % sklicuj se na enačbo (v oklepajih)
\pageref{eq:formula}      % številka strani
```

### Citati

```latex
\cite{kljuc}              % citat
\nocite{kljuc}            % citat brez reference v tekstu
\bibliographystyle{plain} % stil bibliografije
\bibliography{viri}       % vključi .bib datoteko
```

### Beamer (predstavitve)

**Osnovna struktura:**
```latex
\documentclass{beamer}
\usetheme{Berlin}

\begin{document}

\begin{frame}
\titlepage
\end{frame}

\begin{frame}{Naslov okvirja}
Vsebina...
\end{frame}

\end{document}
```

**Teme:**
- `Berlin`, `Madrid`, `Copenhagen`, `Warsaw`, ...

**Bloki:**
```latex
\begin{block}{Naslov bloka}
Vsebina bloka.
\end{block}

\begin{exampleblock}{Primer}
Primer vsebine.
\end{exampleblock}

\begin{alertblock}{Opozorilo}
Pomembna informacija!
\end{alertblock}
```

**Postopno odkrivanje:**
```latex
\pause                    % premor

\onslide<2>{Prikaže se na 2. koraku}
\only<3>{Prikaže se samo na 3. koraku}

\begin{itemize}[<+->]     % postopno odkrivanje
    \item Prvi
    \item Drugi
    \item Tretji
\end{itemize}
```

**Stolpci:**
```latex
\begin{columns}
\column{0.5\textwidth}
Levi stolpec

\column{0.5\textwidth}
Desni stolpec
\end{columns}
```

### Matematika

**Vrstični način:**
```latex
Formula $a^2 + b^2 = c^2$ v besedilu.
\(E = mc^2\) alternativna sintaksa.
```

**Prikazni način:**
```latex
\[
    \int_0^\infty e^{-x} dx = 1
\]
```

**Matematični simboli:**
```latex
\alpha, \beta, \gamma     % grške črke
\infty                    % neskončno
\sum_{i=1}^n              % vsota
\int_a^b                  % integral
\lim_{x \to 0}            % limita
\frac{a}{b}               % ulomek
\sqrt{x}                  % koren
\binom{n}{k}              % binomski simbol
\leq, \geq                % ≤, ≥
\in, \notin               % ∈, ∉
\emptyset                 % prazna množica
\mathbb{R}, \mathbb{N}    % množice
\forall, \exists          % ∀, ∃
```

**Funkcije:**
```latex
\sin x, \cos x, \tan x
\log x, \ln x, \exp x
\lim_{x \to 0} f(x)
```
- NE piši samo `sin`, ampak `\sin`!

**Prikazna okolja:**
```latex
\begin{equation}
E = mc^2
\label{eq:einstein}
\end{equation}

\begin{align}
a &= b + c \\
  &= d + e
\end{align}

\begin{multline}
Zelo dolga enačba = \\
ki se nadaljuje na drugi vrstici
\end{multline}
```
- Za neoštevilčene: `equation*`, `align*`, `multline*`

**Cases (po kosih definirana funkcija):**
```latex
\[
f(x) = \begin{cases}
x^2 & \text{če } x \geq 0 \\
-x  & \text{če } x < 0
\end{cases}
\]
```

**Matrike:**
```latex
\begin{pmatrix}         % okrogli oklepaji
a & b \\
c & d
\end{pmatrix}

\begin{bmatrix}         % oglati oklepaji
a & b \\
c & d
\end{bmatrix}

\begin{vmatrix}         % determinanta
a & b \\
c & d
\end{vmatrix}
```

**Pisave v matematiki:**
```latex
\mathbb{R}              % blackboard bold (množice)
\mathcal{F}             % kaligrafija
\mathsf{ABC}            % sans-serif
\mathtt{text}           % typewriter
\mathrm{log}            % roman (funkcije)
\text{besedilo}         % besedilo v matematiki
```

**Pomembno:**
- Prazna množica: `\emptyset`, NE `\phi`
- Element: `\in`, NE `\epsilon`
- Enakosti: poravnaj z `&=`

---

## 5. EXCEL

### Uvoz CSV datotek

**Postopek:**
1. Data > Get Data > From File > From Text/CSV
2. Izberi datoteko
3. Nastavi:
   - **File Origin**: UTF-8
   - **Delimiter**: 
     - `;` (podpičje) za slovenske CSV
     - `,` (vejica) za angleške CSV
   - **Data Type Detection**: Based on entire dataset
4. Load

**Decimalni separator:**
- Slovenski CSV: vejica (3,14)
- Angleški CSV: pika (3.14)
- Excel mora pravilno prepoznati!

### Osnovne formule

**Seštevanje:**
```
=SUM(A1:A10)            % vsota od A1 do A10
=A1+A2+A3               % direktno seštevanje
```

**Povprečje:**
```
=AVERAGE(B1:B10)
```

**Pogojni stavki:**
```
=IF(A1>100, "Veliko", "Malo")
=IF(A1>100, "Veliko", IF(A1>50, "Srednje", "Malo"))
```

 (vrstično) vs `\[...\]` (prikazno)
- Ne pozabi na `\maketitle` po definiciji naslova
- Label DAJ, ne pozabi REF-a

### Excel

- UTF-8 kodiranje pri uvozu CSV
- Pazi na decimalne vejice/pike
- Tabele: Ctrl+T
- Pogojno oblikovanje: Home > Conditional Formatting
- Vrtilne tabele: preveri, da so vsi podatki izbrani

### Mathematica

- **VEDNO** ClearAll na začetku vsake celice
- Podčrtaj pri definiciji funkcij: `f[x_]`
- `:=` za funkcije, `=` za vrednosti
- Preveri barve: črna (OK), modra (ni definirano)
- Shift+Enter za evaluacijo celice

### Pogosti napaki

❌ **HTML:** Pozabljen `</tag>` zapirajoči element
✅ Preveri, da so vsi pari odprti in zaprti

❌ **CSS:** Pozabljena `{` ali `}` ali `;`
✅ Vsaka deklaracija se konča s podpičjem

❌ **LaTeX:** `\usepackge` namesto `\usepackage`
✅ Pozor na tipkarske napake v ukazih!

❌ **Excel:** Formula se ne posodobi
✅ Pritisni F9 za osvežitev ali Ctrl+Alt+F9

❌ **Mathematica:** `f[x]` namesto `f[x_]`
✅ Podčrtaj označuje parameter!

### Časovna razporeditev (120 min)

- HTML/CSS (20 točk): ~25 min
- LaTeX (36 točk): ~45 min
- Excel (12 točk): ~15 min
- Mathematica (32 točk): ~30 min
- Oddaja in preverjanje: 5 min

**Rezerva:** Ne rabijo ti biti točne minute, ampak imej občutek za čas!

### Pred oddajo

✅ Preveri imena datotek  
✅ Preveri, da so vse datoteke v mapi  
✅ Odpri ZIP in preveri vsebino  
✅ Ime arhiva: **PriimekIme.zip** (brez šumnikov!)  
✅ Oddaj na spletno učilnico  

**SREČNO NA IZPITU!** 🍀