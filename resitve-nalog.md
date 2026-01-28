# Rešitve nalog iz 1. izpita - Januar 2025

## 1. naloga - HTML in CSS (20 točk)

### 1.1 Naslov dokumenta in vključitev CSS (4 točke)

V `dokument.html`, v razdelku `<head>`:

```html
<head>
    <meta charset="UTF-8">
    <title>Finančni derivati</title>
    <link rel="stylesheet" href="oblikovanje.css">
</head>
```

### 1.2 Oštevilčen seznam s povezavo (4 točke)

V razdelku "Kazalo":

```html
<h2>Kazalo</h2>
<ol>
    <li><a href="#financni-derivati">Finančni derivati</a></li>
    <li>Zgodovina</li>
    <li>Primeri derivatov</li>
</ol>
```

### 1.3 Povezava na Wikipedijo in slika (4 točke)

V razdelku "Finančni derivati":

```html
<h2 id="financni-derivati">Finančni derivati</h2>
<p>Finančni derivati so finančni instrumenti, katerih vrednost je odvisna od vrednosti osnovnega sredstva. Primeri derivatov so terminske pogodbe, opcije in zamenjave.</p>
<p>Več o finančnih derivatih lahko preberete <a href="https://en.wikipedia.org/wiki/Derivative_(finance)">na Wikipediji</a>.</p>
<div class="slika">
    <img src="stocks.jpg" alt="Finančni derivati">
</div>
```

### 1.4 Popravljena tabela (4 točke)

```html
<h2>Primeri derivatov</h2>
<table>
    <thead>
        <tr>
            <th>Vrsta</th>
            <th>Opis</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Terminska pogodba</td>
            <td>Pogodba za nakup ali prodajo osnovnega sredstva po vnaprej določeni ceni.</td>
        </tr>
        <tr>
            <td>Opcija</td>
            <td>Pravica (ne obveznost) za nakup ali prodajo osnovnega sredstva po določeni ceni.</td>
        </tr>
    </tbody>
</table>
```

### 1.5 CSS stili (4 točke)

V `oblikovanje.css` dodajte:

```css
th {
    background-color: #e9ecef;
    font-weight: bold;
}

.slika {
    border: 1px solid #ccc;
    padding: 0.5em;
    margin: 0 auto;
    background-color: #eee;
    width: 400px;
}
```

---

## 2. naloga - LaTeX (36 točk)

### 2.1 Glava dokumenta (6 točk)

```latex
\title{Dinamika demokratskih izborov}
\author{Matej Rojec}
\date{2.2.2025}

\begin{document}

\maketitle

\begin{abstract}
Esej obravnava Galamov model in njegove dinamike \cite{galam2015stubbornness, galam2016trump, galam2020tipping}. 
Predstavi osnovni model, njegove razširitve ter poudari njegovo uporabnost pri 
analizi dinamike mnenj v sistemih, ki jih zaznamujejo pomembni dogodki in predsodki. 
Analizirane so dinamike modela, razširitve pa naslavljajo njegove omejitve in 
povečujejo uporabnost. Obravnavan je primer volitev Donalda Trumpa leta 2016, 
ki ponazarja uporabnost modela.
\end{abstract}
```

### 2.2 Literatura (6 točk)

Na koncu dokumenta pred `\end{document}`:

```latex
\bibliographystyle{plain}
\bibliography{viri}
```

Datoteka `viri.bib` je že pripravljena z vsemi potrebnimi viri.

### 2.3 AMS okolje algoritem (6 točk)

V preambuli:

```latex
\theoremstyle{definition}
\newtheorem{algoritem}{Algoritem}
```

V dokumentu namesto komentarjev:

```latex
\begin{algoritem}
Galamov model deluje skozi tri ključne korake, ki se iterativno ponavljajo:   

\begin{enumerate}
\item Agenti se naključno razporedijo v skupine velikosti od 1 do največ 5 ali 6.

\item V vsaki skupini se uvede lokalno pravilo večine. Pri izenačenju mnenj se mnenje $A$ posodobi z 
verjetnostjo $k$, mnenje $B$ pa z verjetnostjo $(1-k)$, kar je odvisno od predsodkov v skupini.

\item Vsi agenti se premešajo in postopek se ponovi.
\end{enumerate}
\end{algoritem}
```

### 2.4 Ukaz \p (6 točk)

V preambuli:

```latex
\newcommand{\p}{\mathbb{P}}
```

Zamenjava v dokumentu (vrstica 63):

```latex
\( p_n := \sum_{r=1}^{L} a_r \p_r(p_{n-1}) \),
kjer je $L$ največja velikost skupine, $a_r$ delež skupin velikosti $r$, $\p_r$ pa verjetnost, 
da skupina s $r$ agenti podpira izbiro $A$.

Verjetnost $\p_r$ je izražena kot:
```

### 2.5 Enačba z okoljem cases (6 točk)

```latex
\begin{equation}
\label{eq:gl}
\p_{r}(p_{n-1}) = 
\begin{cases}
    \sum_{m=\frac{r+1}{2}}^r \binom{r}{m} p_{n-1}^m (1-p_{n-1})^{r-m} 
    & \text{za lihe } r, \\
    \sum_{m=\frac{r}{2} + 1}^r \binom{r}{m} p_{n-1}^m (1-p_{n-1})^{r-m} + k\cdot \binom{r}{\frac{r}{2}} p_{n-1}^\frac{r}{2} (1-p_{n-1})^\frac{r}{2}
    & \text{za sode } r.
\end{cases}
\end{equation}
```

Sklic v besedilu (vrstica 76):

```latex
Verjetnost $\p_r$ je izražena kot v enačbi~\eqref{eq:gl}.
```

ali:

```latex
Verjetnost $\p_r$ je izražena v enačbi~(\ref{eq:gl}).
```

### 2.6 Slike z subfigure (6 točk)

V preambuli potrebujete paket `subfigure` (že vključen).

V dokumentu (namesto komentarjev vrstica 83-94):

```latex
Za dodatno analizo je na sliki~\ref{fig:graphs} prikazana verjetnost $p_n$ 
kot funkcija prejšnje verjetnosti $p_{n-1}$ za različne vrednosti $r$ pri $k=1$.

\begin{figure}[ht!]
    \centering
    \subfigure[Trenutna verjetnost $p_n$ kot funkcija prejšnje verjetnosti $p_{n-1}$ za $k = 1$ in $r = 3$ v intervalu $p_{n-1} \in (0, 1)$.]{
        \includegraphics[width=0.4\textwidth]{r3.png}
        \label{fig:r3}
    }
    \hfill
    \subfigure[Trenutna verjetnost $p_n$ kot funkcija prejšnje verjetnosti $p_{n-1}$ za $k = 1$ in $r = 4$ v intervalu $p_{n-1} \in (0, 1)$.]{
        \includegraphics[width=0.4\textwidth]{r4.png}
        \label{fig:r4}
    }
    \caption{Primerjava verjetnostnih prehodov}
    \label{fig:graphs}
\end{figure}
```

**Alternativna rešitev z `subcaption`** (če uporabljate modernejši pristop):

```latex
\begin{figure}[ht!]
    \centering
    \begin{subfigure}{0.45\textwidth}
        \includegraphics[width=\textwidth]{r3.png}
        \caption{Trenutna verjetnost $p_n$ kot funkcija prejšnje verjetnosti $p_{n-1}$ za $k = 1$ in $r = 3$ v intervalu $p_{n-1} \in (0, 1)$.}
        \label{fig:r3}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.45\textwidth}
        \includegraphics[width=\textwidth]{r4.png}
        \caption{Trenutna verjetnost $p_n$ kot funkcija prejšnje verjetnosti $p_{n-1}$ za $k = 1$ in $r = 4$ v intervalu $p_{n-1} \in (0, 1)$.}
        \label{fig:r4}
    \end{subfigure}
    \caption{Primerjava verjetnostnih prehodov}
    \label{fig:graphs}
\end{figure}
```

---

## 3. naloga - Excel (12 točk)

### 3.1 Uvoz podatkov in dodajanje stolpca Mesec (4 točke)

1. Odprite Excel
2. Podatki → Iz besedila/CSV → izberite `vhodni-podatki-sl.csv` (ali `-en.csv`)
3. Nastavitve:
   - Za slovensko verzijo: Ločilo = **podpičje** (`;`), Decimalna vejica = **vejica** (`,`)
   - Za angleško verzijo: Ločilo = **vejica** (`,`), Decimalna vejica = **pika** (`.`)
   - Kodiranje: **UTF-8** (65001)
4. Kliknite "Naloži"
5. Vrinite nov stolpec pred stolpec "Datum":
   - Desni klik na stolpec B → "Vstavi"
6. V celico B1 napišite: `Mesec`
7. V celico B2 napišite formulo: `=MONTH(C2)`
8. Formulo kopirajte navzdol do konca podatkov (povlecite ali dvojni klik na modro kvadratek)

### 3.2 Stolpec Prodaja s pogojnim barvanjem (4 točke)

1. V celico F1 napišite: `Prodaja`
2. V celico F2 napišite formulo: `=D2*E2`
3. Formulo kopirajte navzdol do konca podatkov
4. Izberite celice F2:F1082 (vsi podatki v stolpcu Prodaja)
5. Domov → Pogojno oblikovanje → Nova pravila:
   
   **Pravilo 1 (zeleno za >100):**
   - Izberite "Oblikuj samo celice, ki vsebujejo"
   - Pogoj: "Vrednost celice" "večja od" `100`
   - Oblikovanje: Zelena barva ozadja
   
   **Pravilo 2 (rdeče za <50):**
   - Izberite "Oblikuj samo celice, ki vsebujejo"
   - Pogoj: "Vrednost celice" "manjša od" `50`
   - Oblikovanje: Rdeča barva ozadja

**Alternativno (hitrejša metoda):**
- Izberite stolpec F (samo podatke brez glave)
- Domov → Pogojno oblikovanje → Pravila označevanja celic:
  - "Večje od" → vnesite `100` → izberite "Zeleno polnilo z zelenim besedilom"
  - "Manjše od" → vnesite `50` → izberite "Svetlo rdeče polnilo z rdečim besedilom"

### 3.3 Vrtilna tabela (4 točke)

1. Izberite katerokoli celico v tabeli s podatki
2. Vstavi → Vrtilna tabela → OK (nova delovna tabla)
3. Nastavitve vrtilne tabele:
   - **Vrstice:** Povlecite "Mesec" v polje "Vrstice"
   - **Stolpci:** Povlecite "Regija" v polje "Stolpci"
   - **Vrednosti:** Povlecite "Prodaja" v polje "Vrednosti"
   - Kliknite na "Vsota od Prodaja" → Nastavitve polja vrednosti → izberite **"Povprečje"**
4. Rezultat:
   - Vrstice: Meseci 1, 2, 3
   - Stolpci: Celje, Nova Gorica, Ptuj, Škofja Loka
   - Vrednosti: Povprečna prodaja za vsako kombinacijo

**Pričakovani rezultat** (približno):

| Mesec | Celje | Nova Gorica | Ptuj | Škofja Loka | Skupaj |
|-------|-------|-------------|------|-------------|--------|
| 1 | ~19402 | ~17642 | ~18260 | ~17474 | ~72778 |
| 2 | ~16205 | ~18020 | ~18885 | ~17550 | ~70661 |
| 3 | ~19411 | ~19572 | ~18848 | ~18822 | ~76653 |
| **Skupaj** | ~55019 | ~55234 | ~55992 | ~53846 | ~220091 |

**Opomba:** Če povprečje ne deluje pravilno, preverite:
- Da ste res izbrali "Povprečje" namesto "Vsota"
- Da so vrednosti v stolpcu Prodaja številske (ne tekstovne)

---

## 4. naloga - Mathematica (32 točk)

Za to nalogo potrebujete odpreti `mathematica.nb` ali `mathematica_en.nb` zvezek in slediti navodilom v njem.

### Tipični koraki pri Mathematica nalogah:

1. **Uvoz podatkov:**
   ```mathematica
   data = Import["pot/do/datoteke.csv"]
   ```

2. **Definicija funkcij:**
   ```mathematica
   f[x_, y_] := x^2 + y^2
   ```

3. **Uporaba vgrajenih funkcij:**
   ```mathematica
   ? FunctionName  (* Pomoč *)
   Expand[expr]
   Simplify[expr]
   Solve[equation, x]
   ```

4. **Risanje grafov:**
   ```mathematica
   Plot[f[x], {x, 0, 10}]
   Plot3D[f[x, y], {x, -2, 2}, {y, -2, 2}]
   ```

5. **Čiščenje spremenljivk:**
   ```mathematica
   ClearAll[x, y, f, g]
   ```

---

## Dodatne opombe

### Oddaja rešitev

1. Prepričajte se, da imate vse datoteke:
   - `dokument.html`
   - `oblikovanje.css`
   - `dokument.tex`
   - `dokument.pdf` (kompilirano)
   - `prodaja.xlsx`
   - `mathematica.nb` (z rešenimi nalogami)

2. Stisnite vse v **ZIP arhiv** z imenom `PriimekIme.zip` (brez šumnikov)

3. Oddajte na spletno učilnico

### Preverjanje pred oddajo

- [ ] HTML se pravilno prikaže v brskalniku
- [ ] CSS stili so pravilno uporabljeni
- [ ] LaTeX dokument se uspešno kompilira v PDF
- [ ] PDF vsebuje literaturo in pravilne sklice
- [ ] Excel vsebuje formule (ne samo vrednosti)
- [ ] Vrtilna tabela prikazuje pravilne podatke
- [ ] Mathematica zvezek se izvaja brez napak

### Pogosta vprašanja

**Q: Kako kompiram LaTeX z BibTeX?**
```bash
pdflatex dokument.tex
bibtex dokument
pdflatex dokument.tex
pdflatex dokument.tex
```

**Q: Excel ne prikaže pravilnih decimalnih vejic/pik?**
A: Preverite nastavitve uvoza in uporabite pravilno verzijo CSV datoteke (sl/en).

**Q: Subfigure ne deluje?**
A: Poskusite uporabiti paket `subcaption` namesto `subfigure` ali preverite, da imate pravilno sintakso.

**Q: Vrtilna tabela prikazuje vsoto namesto povprečja?**
A: Kliknite na polje v Vrednostih → Nastavitve polja vrednosti → Povprečje.

---

## Časovna razporeditev (priporočilo)

- **1. naloga (HTML/CSS):** 25 minut
- **2. naloga (LaTeX):** 50 minut
- **3. naloga (Excel):** 20 minut
- **4. naloga (Mathematica):** 25 minut
- **Rezerva in oddaja:** 10 minut

**Skupaj:** 130 minut (izpit traja 120 minut + čas za oddajo)
