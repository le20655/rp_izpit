# 🎯 Primeri nalog za izpit - Računalniški praktikum

## ⭐ LEGENDA

**🟨 RUMENI OKVIR** = BISTVENO ZNANJE (skoraj zagotovo na izpitu, dovolj za 50%+)

**🟦 MODER OKVIR** = Naloga

**🟩 ZELEN OKVIR** = Rešitev

**⬜ SIV OKVIR** = Naprednejše/specifično znanje

---

# 1. HTML & CSS (20 točk, ~25 min)

## ⭐ BISTVENO - HTML Osnove

**TO MORA BITI NA PAMET:**

- `<!DOCTYPE html>` - vedno prva vrstica
- `<meta charset="UTF-8">` - kodiranje
- `<title>Naslov</title>` - naslov v zavihku
- `<link rel="stylesheet" href="style.css">` - vključitev CSS
- `<a href="url">besedilo</a>` - povezava
- `<img src="slika.jpg" alt="opis">` - slika
- `<ul><li>...</li></ul>` - seznam
- `id` vs `class`

---

## 🟦 Naloga 1.1 (4 točke)

V datoteki `dokument.html`:

1. V glavi dokumenta določite naslov dokumenta na "Finančni derivati"
2. Vključite datoteko z oblikovanjem `oblikovanje.css`

---

## 🟩 Rešitev 1.1

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Finančni derivati</title>
    <link rel="stylesheet" href="oblikovanje.css">
</head>
<body>
    <!-- vsebina -->
</body>
</html>
```

**Pogosti napaki:**
- ❌ Pozabljen `<meta charset="UTF-8">`
- ❌ Napačna pot v href (npr. `href="css/oblikovanje.css"` če je datoteka v isti mapi)

---

## 🟦 Naloga 1.2 (4 točke)

Naredite oštevilčen seznam s tremi elementi. Prvi element naj vsebuje povezavo na razdelek z id="derivati".

Elementi seznama (že v komentarjih): Finančni derivati, Primeri, Povzetek

---

## 🟩 Rešitev 1.2

```html
<h2>Kazalo</h2>
<ol>
    <li><a href="#derivati">Finančni derivati</a></li>
    <li>Primeri</li>
    <li>Povzetek</li>
</ol>

<!-- Kasneje v dokumentu -->
<div id="derivati">
    <h2>Finančni derivati</h2>
    <!-- vsebina -->
</div>
```

**Ključne točke:**
- ✓ `<ol>` za oštevilčen seznam (NE `<ul>`!)
- ✓ `href="#derivati"` - lojtra (#) za interno povezavo
- ✓ ID mora biti enak v href in na elementu

---

## 🟦 Naloga 1.3 (4 točke)

V razdelku dodajte:

1. Besedilo "na Wikipediji" naj bo povezava na https://sl.wikipedia.org/wiki/Derivat
2. Na koncu razdelka dodajte div z razredom "slika"
3. V ta div vključite sliko `stocks.jpg`

---

## 🟩 Rešitev 1.3

```html
<div id="derivati">
    <h2>Finančni derivati</h2>
    <p>Več informacij najdete 
       <a href="https://sl.wikipedia.org/wiki/Derivat">na Wikipediji</a>.
    </p>
    
    <div class="slika">
        <img src="stocks.jpg" alt="Finančni trgi">
    </div>
</div>
```

**Pomembno:**
- ✓ Polna URL povezava (s `https://`)
- ✓ `class="slika"` (NE `id="slika"` - class za oblikovanje!)
- ✓ `alt` atribut pri sliki (vedno!)

---

## ⭐ BISTVENO - CSS Izbiralci

**TO MORA BITI NA PAMET:**

- `p { }` - vse značke p
- `.razred { }` - vsi z class="razred"
- `#id { }` - element z id="id"
- `table a { }` - vsi a znotraj table
- `tr:nth-child(even) { }` - sode vrstice
- `a:hover { }` - ob lebdenju

---

## 🟦 Naloga 1.4 (4 točke)

V datoteki `oblikovanje.css` dodajte izbiralec za celice v glavi tabele (`th`), ki naj določi:

- Ozadje barve #e9ecef
- Pisavo na krepko

---

## 🟩 Rešitev 1.4

```css
th {
    background-color: #e9ecef;
    font-weight: bold;
}
```

**Alternativa (če imaš samo eno tabelo):**

```css
table th {
    background-color: #e9ecef;
    font-weight: bold;
}
```

---

## 🟦 Naloga 1.5 (4 točke)

Dopolnite izbiralec za razred `slika`, da bo širina 400px.

Že v datoteki je:

```css
.slika {
    /* dopolni */
}
```

---

## 🟩 Rešitev 1.5

```css
.slika {
    width: 400px;
}
```

**Če bi hoteli tudi centrirati sliko:**

```css
.slika {
    width: 400px;
    text-align: center;
}

.slika img {
    max-width: 100%;
}
```

---

## ⬜ Naprednejše - CSS specifično

**Naloga:** Vsem povezavam v tabeli dodajte ozadje #bada55 in odstranite podčrtavo.

**Rešitev:**

```css
table a {
    background-color: #bada55;
    text-decoration: none;
}
```

**Naloga:** Sode vrstice tabele naj imajo ozadje rgba(225, 127, 74, 0.15).

**Rešitev:**

```css
tr:nth-child(even) {
    background-color: rgba(225, 127, 74, 0.15);
}
```

---

# 2. LaTeX (36 točk, ~45 min)

## ⭐ BISTVENO - LaTeX Preambula

**TO MORA BITI NA PAMET:**

```latex
\documentclass[a4paper,12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[slovene]{babel}
\usepackage[T1]{fontenc}
\usepackage{amsmath}
\usepackage{graphicx}

\title{Naslov}
\author{Ime Priimek}
\date{\today}

\begin{document}
\maketitle
\end{document}
```

---

## 🟦 Naloga 2.1 (6 točk)

Pripravite glavo dokumenta z:

- Naslov: "Black-Scholesov model"
- Avtor: "Janez Novak"
- Datum: današnji datum
- Povzetek: "V tem dokumentu obravnavamo osnove Black-Scholesovega modela."

---

## 🟩 Rešitev 2.1

```latex
\documentclass[a4paper,12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[slovene]{babel}
\usepackage[T1]{fontenc}

\title{Black-Scholesov model}
\author{Janez Novak}
\date{\today}

\begin{document}

\maketitle

\begin{abstract}
V tem dokumentu obravnavamo osnove Black-Scholesovega modela.
\end{abstract}

\end{document}
```

**Pogosti napaki:**
- ❌ Pozabljen `\maketitle` (naslov se ne izpiše!)
- ❌ Povzetek pred `\maketitle` (mora biti za!)

---

## ⭐ BISTVENO - Citati in literatura

**TO MORA BITI NA PAMET:**

```latex
% V besedilu
Kot navaja \cite{black1973}...

% Na koncu dokumenta (pred \end{document})
\bibliographystyle{plain}
\bibliography{viri}
```

---

## 🟦 Naloga 2.2 (6 točk)

V povzetku dodajte sklic na literaturo s ključem `black1973` (ključ je v komentarju). Uporabite priloženo datoteko `viri.bib` in na koncu dokumenta izdelajte seznam literature s stilom `plain`.

---

## 🟩 Rešitev 2.2

```latex
\begin{abstract}
V tem dokumentu obravnavamo osnove Black-Scholesovega modela \cite{black1973}.
\end{abstract}

\section{Uvod}
% ... vsebina ...

% Na koncu dokumenta
\bibliographystyle{plain}
\bibliography{viri}

\end{document}
```

**Pomembno:**
- ✓ `\cite{kljuc}` tam, kjer citirate
- ✓ `\bibliographystyle{plain}` PRED `\bibliography`
- ✓ `\bibliography{viri}` brez .bib končnice!

---

## ⭐ BISTVENO - Nova okolja

**TO MORA BITI NA PAMET:**

```latex
% V preambuli
\usepackage{amsthm}
\theoremstyle{definition}
\newtheorem{definicija}{Definicija}

% V dokumentu
\begin{definicija}
Vsebina definicije.
\end{definicija}
```

---

## 🟦 Naloga 2.3 (6 točk)

Definirajte novo AMS okolje `algoritem` s slogom `definition` in ga uporabite.

---

## 🟩 Rešitev 2.3

```latex
% V preambuli (za \begin{document})
\usepackage{amsthm}
\theoremstyle{definition}
\newtheorem{algoritem}{Algoritem}

% V dokumentu
\begin{algoritem}
Monte Carlo metoda za izračun cene opcije:
\begin{enumerate}
    \item Generiraj naključne poti
    \item Izračunaj izplačila
    \item Povpreči rezultate
\end{enumerate}
\end{algoritem}
```

---

## ⭐ BISTVENO - Novi ukazi

**TO MORA BITI NA PAMET:**

```latex
% V preambuli
\newcommand{\p}{\mathbb{P}}

% V dokumentu
Pod verjetnostno mero $\p$ velja...
```

---

## 🟦 Naloga 2.4 (6 točk)

Definirajte ukaz `\p`, ki izpiše ℙ (verjetnostna mera). V dokumentu so pojavitve `\mathbb{P}\mathbb{P}\mathbb{P}` - zamenjajte jih z uporabo ukaza `\p`.

---

## 🟩 Rešitev 2.4

```latex
% V preambuli
\newcommand{\p}{\mathbb{P}}

% V dokumentu - PREJ:
Pod verjetnostno mero $\mathbb{P}\mathbb{P}\mathbb{P}$ velja...

% V dokumentu - POTEM:
Pod verjetnostno mero $\p\p\p$ velja...
```

**Uporabi VS Code:**
- Ctrl+H (zamenjava)
- Najdi: `\mathbb{P}`
- Zamenjaj: `\p`
- Replace All

---

## ⭐ BISTVENO - Matematika (cases)

**TO MORA BITI NA PAMET:**

```latex
\[
f(x) = \begin{cases}
x^2 & \text{če } x \geq 0 \\
0 & \text{sicer}
\end{cases}
\]
```

---

## 🟦 Naloga 2.5 (6 točk)

Oblikujte naslednjo enačbo z okoljem `cases`:

```
C(S,t) = { S - K    če S > K
         { 0        sicer
```

Dodajte oznako `eq:call` in se nanjo skličite v naslednjem odstavku (nadomestite ??).

---

## 🟩 Rešitev 2.5

```latex
\[
C(S,t) = \begin{cases}
S - K & \text{če } S > K \\
0 & \text{sicer}
\end{cases}
\label{eq:call}
\]

Enačba \eqref{eq:call} opisuje izplačilo call opcije ob dospetju.
```

**Pomembno:**
- ✓ `\text{...}` za besedilo v matematiki
- ✓ `\\` za novo vrstico (NE samo `\`!)
- ✓ `&` pred pogojem za poravnavo
- ✓ `\eqref{eq:call}` za sklicevanje na enačbo (ne `\ref`!)

---

## 🟦 Naloga 2.6 (6 točk)

Vključite dve sliki `graf1.png` in `graf2.png` v eno figuro z uporabo `subfigure`. Vsaka slika naj bo široka `0.4\textwidth`. Dodajte oznaki `fig:graf1` in `fig:graf2` ter se nanju skličite v besedilu (nadomestite ??).

---

## 🟩 Rešitev 2.6

```latex
% V preambuli
\usepackage{graphicx}
\usepackage{subcaption}

% V besedilu
Na slikah \ref{fig:graf1} in \ref{fig:graf2} so prikazani rezultati.

\begin{figure}[h]
\centering
\begin{subfigure}[b]{0.4\textwidth}
    \includegraphics[width=\textwidth]{graf1.png}
    \caption{Prvi graf}
    \label{fig:graf1}
\end{subfigure}
\hfill
\begin{subfigure}[b]{0.4\textwidth}
    \includegraphics[width=\textwidth]{graf2.png}
    \caption{Drugi graf}
    \label{fig:graf2}
\end{subfigure}
\caption{Primerjava grafov}
\end{figure}
```

**Ključne točke:**
- ✓ Vsak `subfigure` ima svoj `\caption` in `\label`
- ✓ `\hfill` med slikami za razporeditev
- ✓ `width=\textwidth` znotraj subfigure (ne absolutno!)

---

## ⬜ Naprednejše - LaTeX specifično

**Tabele z booktabs:**

```latex
\usepackage{booktabs}

\begin{table}[h]
\centering
\begin{tabular}{lcc}
\toprule
Opcija & Strike & Cena \\
\midrule
Call & 100 & 5.50 \\
Put & 100 & 4.20 \\
\bottomrule
\end{tabular}
\caption{Cene opcij}
\end{table}
```

**Matematika - align:**

```latex
\begin{align}
V &= S_0 \cdot N(d_1) - K e^{-rT} N(d_2) \\
d_1 &= \frac{\ln(S_0/K) + (r + \sigma^2/2)T}{\sigma\sqrt{T}}
\end{align}
```

---

# 3. Excel (12 točk, ~15 min)

## ⭐ BISTVENO - Excel Osnove

**TO MORA BITI NA PAMET:**

- **Uvoz CSV**: Data > From Text/CSV, UTF-8, ločilo `;` ali `,`
- **Formule**: `=SUM(A1:A10)`, `=AVERAGE(A1:A10)`, `=IF(A1>100,"Da","Ne")`
- **MONTH**: `=MONTH(A1)` - izloči mesec iz datuma
- **Pogojno oblikovanje**: Home > Conditional Formatting > Greater/Less Than
- **Vrtilna tabela**: Insert > PivotTable

---

## 🟦 Naloga 3.1 (4 točke)

Uvozite podatke iz datoteke:
- `vhodni-podatki-sl.csv`: decimalne vejice, ločilo podpičje, UTF-8

Pred stolpec "Datum" vrinite nov stolpec z imenom "Mesec" in v njem izračunajte številko meseca prodaje.

---

## 🟩 Rešitev 3.1

**1. Uvoz CSV:**

1. Data > Get Data > From File > From Text/CSV
2. Izberi `vhodni-podatki-sl.csv`
3. Nastavi:
   - File Origin: **65001: Unicode (UTF-8)**
   - Delimiter: **Semicolon** (podpičje)
   - Data Type Detection: Based on entire dataset
4. Load

**2. Dodaj stolpec Mesec:**

1. Desni klik na glavo stolpca "Datum" > Insert > Insert Columns to the Left
2. Preimenuj stolpec v "Mesec"
3. V prvo celico pod glavo vpiši: `=MONTH(B2)` (če je Datum v stolpcu B)
4. Kopiraj formulo navzdol (potegni za ročico ali dvojni klik)

**Rezultat:**

| Mesec | Datum      | Izdelek | Količina |
|-------|------------|---------|----------|
| 1     | 15.1.2024  | A       | 10       |
| 1     | 20.1.2024  | B       | 5        |
| 2     | 5.2.2024   | A       | 8        |

---

## 🟦 Naloga 3.2 (4 točke)

Dodajte stolpec "Prodaja" in v njem izračunajte produkt količine in cene na enoto. Na stolpcu uporabite pogojno barvanje:

- Prodaja > 100: zeleno
- Prodaja < 50: rdeče

---

## 🟩 Rešitev 3.2

**1. Dodaj stolpec Prodaja:**

1. V prvi prosti stolpec zapiši glavo: "Prodaja"
2. V prvo celico pod glavo: `=C2*D2` (Količina × Cena)
3. Kopiraj formulo navzdol

**2. Pogojno barvanje:**

1. Izberi stolpec Prodaja (celice s podatki, ne glava)
2. Home > Conditional Formatting > Highlight Cells Rules > Greater Than...
3. Vpiši 100, izberi zeleno barvo (Green Fill with Dark Green Text)
4. Ponovno: Conditional Formatting > Highlight Cells Rules > Less Than...
5. Vpiši 50, izberi rdeče barvo (Light Red Fill with Dark Red Text)

**Rezultat:**

| Količina | Cena | Prodaja |
|----------|------|---------|
| 10       | 12   | **120** (zeleno) |
| 3        | 15   | **45** (rdeče)   |
| 8        | 10   | 80      |

---

## ⭐ BISTVENO - Vrtilne tabele

**VEDNO PRIDE NA IZPIT!**

Vrtilna tabela = Povzetek podatkov

- **Rows**: kaj je v vrsticah (npr. Mesec)
- **Columns**: kaj je v stolpcih (npr. Regija)
- **Values**: katere vrednosti računamo (npr. Average Prodaje)

---

## 🟦 Naloga 3.3 (4 točke)

Ustvarite vrtilno tabelo, ki bo izpisala **povprečno prodajo** za vsako regijo (po stolpcih) in mesec (po vrsticah).

---

## 🟩 Rešitev 3.3

1. Klikni kjerkoli v podatkih
2. Insert > PivotTable
3. Izberi "New Worksheet"
4. OK
5. V PivotTable Fields (desno):
   - Povleci "Mesec" v **Rows**
   - Povleci "Regija" v **Columns**
   - Povleci "Prodaja" v **Values**
6. Klikni na "Sum of Prodaja" v Values > Value Field Settings
7. Spremeni na **Average**
8. OK

**Rezultat:**

| Mesec | Ljubljana | Maribor | Koper |
|-------|-----------|---------|-------|
| 1     | 85.50     | 92.30   | 78.20 |
| 2     | 91.20     | 88.70   | 95.40 |
| 3     | 87.60     | 94.10   | 82.30 |

---

## ⬜ Naprednejše - Excel specifično

**Pogojno oblikovanje z barvno lestvico:**

1. Izberi celice
2. Conditional Formatting > Color Scales
3. Izberi shemo (npr. Green-Yellow-Red)

**Absolutne reference:**

```
=A1*$B$1    % B1 se ne bo spremenila pri kopiranju
=SUM($A$1:$A$10)  % območje se ne bo spremenilo
```

---

# 4. Mathematica (32 točk, ~30 min)

## ⭐ BISTVENO - Mathematica Osnove

**TO MORA BITI NA PAMET:**

```mathematica
ClearAll[x, y, f]     (* VEDNO na začetku! *)

x = 5                 (* vrednost *)
f[x_] := x^2         (* funkcija - PODČRTAJ! *)

Expand[(x+1)^2]       (* razširi *)
Simplify[expr]        (* poenostavi *)
D[x^3, x]            (* odvod *)
Integrate[x^2, x]     (* integral *)
Solve[x^2==4, x]      (* reši enačbo *)
Plot[Sin[x], {x,0,2Pi}]  (* graf *)
```

---

## 🟦 Naloga 4.1 (8 točk)

Definirajte funkcijo Black-Scholesovega modela za ceno call opcije:

```
C[S_, K_, r_, σ_, T_] = S*N[d1] - K*Exp[-r*T]*N[d2]
kjer:
d1 = (Log[S/K] + (r + σ²/2)*T) / (σ*Sqrt[T])
d2 = d1 - σ*Sqrt[T]
N[x] = CDF[NormalDistribution[0,1], x]
```

Izračunajte ceno za: S=100, K=95, r=0.05, σ=0.2, T=1

---

## 🟩 Rešitev 4.1

```mathematica
ClearAll[C, d1, d2, S, K, r, σ, T]

(* Definicija funkcij *)
d1[S_, K_, r_, σ_, T_] := (Log[S/K] + (r + σ^2/2)*T)/(σ*Sqrt[T])

d2[S_, K_, r_, σ_, T_] := d1[S, K, r, σ, T] - σ*Sqrt[T]

C[S_, K_, r_, σ_, T_] := 
  S*CDF[NormalDistribution[0,1], d1[S, K, r, σ, T]] - 
  K*Exp[-r*T]*CDF[NormalDistribution[0,1], d2[S, K, r, σ, T]]

(* Izračun *)
C[100, 95, 0.05, 0.2, 1]

(* Rezultat: približno 10.45 *)
```

**Ključne točke:**
- ✓ **PODČRTAJ** pri parametrih: `S_`, `K_`, ...
- ✓ `ClearAll` na začetku!
- ✓ `Log` je naravni logaritem (ln)
- ✓ `Exp` za e^x
- ✓ `CDF[NormalDistribution[0,1], x]` za N(x)

---

## ⭐ BISTVENO - Reševanje enačb

**TO MORA BITI NA PAMET:**

```mathematica
Solve[x^2 - 5x + 6 == 0, x]        (* simbolno *)
NSolve[x^5 - x - 1 == 0, x]        (* numerično *)
FindRoot[Cos[x] == x, {x, 0}]      (* ničla blizu 0 *)
```

---

## 🟦 Naloga 4.2 (8 točk)

Rešite enačbo za implicitno volatilnost. Dana je cena call opcije C=10, poiščite σ, da bo:

```
C[100, 95, 0.05, σ, 1] == 10
```

Uporabite `FindRoot` z začetnim približkom σ=0.2

---

## 🟩 Rešitev 4.2

```mathematica
(* Že imamo definirano funkcijo C iz prejšnje naloge *)

(* Poiščemo σ *)
FindRoot[C[100, 95, 0.05, σ, 1] == 10, {σ, 0.2}]

(* Rezultat: {σ -> 0.192...} *)

(* Shranimo rezultat *)
implicitnaVolatilnost = σ /. FindRoot[C[100, 95, 0.05, σ, 1] == 10, {σ, 0.2}]

(* Preverimo *)
C[100, 95, 0.05, implicitnaVolatilnost, 1]
(* Mora biti približno 10 *)
```

**Pomembno:**
- ✓ `==` za enačbo (NE samo `=`!)
- ✓ `/.` (ReplaceAll) za substitucijo rešitve
- ✓ Začetni približek mora biti razumen (σ > 0)

---

## 🟦 Naloga 4.3 (8 točk)

Narišite graf funkcije C[S, 95, 0.05, 0.2, 1] za S od 80 do 120. Dodajte horizontalno črto pri C=10.

---

## 🟩 Rešitev 4.3

```mathematica
Plot[
  {C[S, 95, 0.05, 0.2, 1], 10},
  {S, 80, 120},
  PlotLabel -> "Cena call opcije",
  AxesLabel -> {"Cena delnice S", "Cena opcije C"},
  PlotLegends -> {"Black-Scholes", "Tržna cena"},
  PlotStyle -> {Blue, {Red, Dashed}}
]
```

**Alternativa brez legend:**

```mathematica
Plot[
  {C[S, 95, 0.05, 0.2, 1], 10},
  {S, 80, 120}
]
```

---

## 🟦 Naloga 4.4 (8 točk)

Izračunajte delta hedging razmerje (delta) kot odvod cene opcije po ceni delnice. Uporabite numerični odvod za S=100, K=95, r=0.05, σ=0.2, T=1.

---

## 🟩 Rešitev 4.4

```mathematica
(* Metoda 1: Simbolni odvod *)
delta[S_, K_, r_, σ_, T_] := D[C[s, K, r, σ, T], s] /. s -> S

delta[100, 95, 0.05, 0.2, 1]

(* Metoda 2: Numerični odvod (enostavneje) *)
ND[C[S, 95, 0.05, 0.2, 1], S, 100]

(* Metoda 3: Direktno iz formule *)
deltaBS[S_, K_, r_, σ_, T_] := CDF[NormalDistribution[0,1], d1[S, K, r, σ, T]]

deltaBS[100, 95, 0.05, 0.2, 1]

(* Rezultat: približno 0.69 - kupi 0.69 delnice na opcijo *)
```

**Interpretacija:** Delta 0.69 pomeni, da za hedging ene call opcije potrebujemo 0.69 delnice.

---

## ⬜ Naprednejše - Mathematica specifično

**Monte Carlo simulacija:**

```mathematica
ClearAll[simulirajCeno, S0, K, r, σ, T, n]

S0 = 100; K = 95; r = 0.05; σ = 0.2; T = 1; n = 10000;

(* Generiraj končne cene *)
ST = S0 * Exp[(r - σ^2/2)*T + σ*Sqrt[T]*RandomVariate[NormalDistribution[], n]];

(* Izplačila *)
payoffs = Max[ST - K, 0];

(* Diskontirano povprečje *)
cenaMC = Exp[-r*T] * Mean[payoffs]

(* Primerjaj z BS *)
C[S0, K, r, σ