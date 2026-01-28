# LaTeX: Definiranje ukazov, operatorjev in zapis virov

## 1. Ukaz `\newcommand`

Ukaz `\newcommand` se uporablja za definiranje novih ukazov v LaTeX-u. Definira se v preambuli dokumenta.

### Osnovna sintaksa

```latex
\newcommand{\iméukaza}{definicija}
```

**Primeri:**

```latex
\newcommand{\R}{\mathbb{R}}           % Real numbers
\newcommand{\N}{\mathbb{N}}           % Natural numbers
\newcommand{\p}{\mathbb{P}}           % Probability symbol P
\newcommand{\bs}{\backslash}          % Backslash
```

**Uporaba:**
```latex
Naj bo $x \in \R$ realno število.
Verjetnost $\p(A)$ je pozitivna.
```

### Ukazi s parametri

```latex
\newcommand{\iméukaza}[število-parametrov]{definicija z #1, #2, ...}
```

**Primeri:**

```latex
\newcommand{\norm}[1]{\|#1\|}                    % Norma
\newcommand{\abs}[1]{|#1|}                       % Absolutna vrednost
\newcommand{\set}[1]{\{#1\}}                     % Množica
\newcommand{\inner}[2]{\langle #1, #2 \rangle}  % Skalarni produkt
\newcommand{\frac}[2]{\dfrac{#1}{#2}}           % Ulomek (lahko tudi overwrite)
```

**Uporaba:**
```latex
Naj bo $\norm{x} = 5$ in $\abs{-3} = 3$.
Množica $\set{1, 2, 3}$ je končna.
Skalarni produkt $\inner{v}{w}$ je definiran.
```

### Ukazi z neobveznimi parametri

```latex
\newcommand{\iméukaza}[število-parametrov][privzeta-vrednost]{definicija}
```

**Primeri:**

```latex
\newcommand{\derivative}[2][x]{\frac{d #2}{d #1}}
\newcommand{\integral}[2][x]{\int #2 \, d#1}
```

**Uporaba:**
```latex
$\derivative{f}$          % rezultat: df/dx (privzeto)
$\derivative[t]{s}$       % rezultat: ds/dt
$\integral{x^2}$          % rezultat: ∫x² dx
$\integral[t]{t^3}$       % rezultat: ∫t³ dt
```

### Kompleksnejši primeri

```latex
% Vektor s puščico
\newcommand{\vect}[1]{\overrightarrow{#1}}

% Matrična transpozicija
\newcommand{\trans}[1]{#1^{\mathsf{T}}}

% Oznaka za end of proof
\newcommand{\qed}{\hfill $\square$}

% Parcialani odvod
\newcommand{\pder}[2]{\frac{\partial #1}{\partial #2}}

% Funkcija z domeno in kodomeno
\newcommand{\func}[3]{#1 \colon #2 \to #3}
```

---

## 2. Ukaz `\DeclareMathOperator`

Ukaz `\DeclareMathOperator` se uporablja za definiranje novih matematičnih operatorjev. Zahteva paket `amsmath`.

### Osnovna sintaksa

```latex
\usepackage{amsmath}
\DeclareMathOperator{\iméoperatorja}{besedilo}
```

**Primeri:**

```latex
\DeclareMathOperator{\diag}{diag}
\DeclareMathOperator{\trace}{tr}
\DeclareMathOperator{\rank}{rank}
\DeclareMathOperator{\sgn}{sgn}
\DeclareMathOperator{\Ker}{Ker}
\DeclareMathOperator{\Im}{Im}
```

**Uporaba:**
```latex
$\diag(A)$ je diagonala matrike $A$.
$\trace(A) = \sum_{i} a_{ii}$
$\rank(A) \leq \min(m,n)$
```

### Razlika med `\DeclareMathOperator` in običajnim tekstom

**Napačno (brez deklaracije):**
```latex
$log(x)$ ali $\text{log}(x)$    % Slabo! Razmik ni pravilen
```

**Pravilno:**
```latex
\DeclareMathOperator{\Log}{log}
$\Log(x)$                        % Dobro! Pravilen razmik
```

ali uporabite vgrajene operatorje:
```latex
$\log(x), \sin(x), \cos(x), \lim_{x \to 0}$
```

### Operatorji z limitami: `\DeclareMathOperator*`

Za operatorje, ki imajo limite nad in pod seboj (kot `\lim`, `\max`, `\min`), uporabite `\DeclareMathOperator*`.

```latex
\DeclareMathOperator*{\argmax}{arg\,max}
\DeclareMathOperator*{\argmin}{arg\,min}
\DeclareMathOperator*{\esssup}{ess\,sup}
```

**Uporaba:**
```latex
% V prikaznem načinu (display mode):
\[
    x^* = \argmax_{x \in \mathbb{R}} f(x)
\]

% V vrstičnem načinu (inline mode):
Naj bo $x^* = \argmax_{x} f(x)$ optimalna vrednost.
```

### Primerjava: `\DeclareMathOperator` vs `\newcommand`

| Vidik | `\DeclareMathOperator` | `\newcommand` |
|-------|------------------------|---------------|
| Namen | Matematični operatorji | Splošni ukazi |
| Razmik | Avtomatsko pravilno | Ročna kontrola potrebna |
| Pisava | Vedno roman (navadna) | Poljubna |
| Limite | Podpora z `*` različico | Ročna implementacija |

**Primeri:**

```latex
% SLABO (z newcommand):
\newcommand{\diag}{\text{diag}}
$\diag(A)$    % razmik ni optimalen

% DOBRO (z DeclareMathOperator):
\DeclareMathOperator{\diag}{diag}
$\diag(A)$    % pravilni razmiki
```

---

## 3. Zapis virov in literatura (BibTeX)

### Struktura BibTeX datoteke

BibTeX datoteka (`.bib`) vsebuje bibliografske podatke v strukturiranem formatu:

```bibtex
@tip{ključ,
    polje1 = {vrednost1},
    polje2 = {vrednost2},
    ...
}
```

### Vrste virov (tipi)

| Tip | Uporaba | Obvezna polja |
|-----|---------|---------------|
| `@article` | Članek v reviji | author, title, journal, year |
| `@book` | Knjiga | author/editor, title, publisher, year |
| `@inproceedings` | Članek v zborniku | author, title, booktitle, year |
| `@phdthesis` | Doktorska disertacija | author, title, school, year |
| `@mastersthesis` | Magistrsko delo | author, title, school, year |
| `@techreport` | Tehnično poročilo | author, title, institution, year |
| `@misc` | Ostalo (npr. spletne strani) | author/title (vsaj eno) |

### Pogosto uporabljena polja

| Polje | Opis | Primer |
|-------|------|--------|
| `author` | Avtorji | `"Priimek, Ime and Priimek2, Ime2"` |
| `title` | Naslov dela | `"The Art of Computer Programming"` |
| `year` | Leto izdaje | `2023` |
| `journal` | Revija (za članke) | `"Nature"` |
| `volume` | Letnik | `42` |
| `number` | Številka | `3` |
| `pages` | Strani | `123--145` ali `123-145` |
| `booktitle` | Naslov zbornika | `"Proceedings of ICML 2023"` |
| `publisher` | Založba | `"Springer"` |
| `editor` | Urednik | `"Smith, John"` |
| `school` | Univerza (za diplome) | `"MIT"` |
| `institution` | Institucija | `"Stanford University"` |
| `url` | Spletni naslov | `"https://example.com"` |
| `note` | Dodatne opombe | `"Dostopno na: ..."` |
| `month` | Mesec | `jan`, `feb`, ..., ali `"January"` |

### Primeri BibTeX vnosov

#### Članek v reviji (`@article`)

```bibtex
@article{einstein1905,
    author = {Einstein, Albert},
    title = {On the electrodynamics of moving bodies},
    journal = {Annalen der Physik},
    year = {1905},
    volume = {17},
    number = {10},
    pages = {891--921}
}
```

#### Knjiga (`@book`)

```bibtex
@book{knuth1997,
    author = {Knuth, Donald E.},
    title = {The Art of Computer Programming, Volume 1: Fundamental Algorithms},
    publisher = {Addison-Wesley},
    year = {1997},
    edition = {3rd},
    isbn = {0-201-89683-4}
}
```

#### Članek v zborniku (`@inproceedings`)

```bibtex
@inproceedings{lecun1998,
    author = {LeCun, Yann and Bottou, L{\'e}on and Bengio, Yoshua and Haffner, Patrick},
    title = {Gradient-based learning applied to document recognition},
    booktitle = {Proceedings of the IEEE},
    year = {1998},
    volume = {86},
    number = {11},
    pages = {2278--2324}
}
```

#### Več avtorjev

```bibtex
@article{multiple2023,
    author = {Smith, John and Doe, Jane and Johnson, Bob},
    title = {A collaborative study},
    journal = {Journal of Examples},
    year = {2023}
}
```

Pri več kot 3 avtorjih lahko uporabite `and others`:
```bibtex
author = {Smith, John and Doe, Jane and Johnson, Bob and others}
```

#### Doktorska disertacija (`@phdthesis`)

```bibtex
@phdthesis{turing1938,
    author = {Turing, Alan Mathison},
    title = {Systems of Logic Based on Ordinals},
    school = {Princeton University},
    year = {1938}
}
```

#### Spletna stran (`@misc`)

```bibtex
@misc{wiki2024,
    author = {{Wikipedia contributors}},
    title = {Machine Learning --- {W}ikipedia{,} The Free Encyclopedia},
    year = {2024},
    url = {https://en.wikipedia.org/wiki/Machine_learning},
    note = {[Online; dostopno 28-januar-2025]}
}
```

#### Tehnično poročilo (`@techreport`)

```bibtex
@techreport{goodfellow2014,
    author = {Goodfellow, Ian and Pouget-Abadie, Jean and Mirza, Mehdi},
    title = {Generative Adversarial Networks},
    institution = {Universit{\'e} de Montr{\'e}al},
    year = {2014},
    number = {arXiv:1406.2661}
}
```

### Uporaba BibTeX v LaTeX dokumentu

#### 1. Priprava preambule

```latex
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage[slovene]{babel}
% Za URL povezave v literaturi:
\usepackage{url}
\usepackage{hyperref}

\begin{document}
```

#### 2. Citiranje v besedilu

```latex
Kot je pokazal Einstein~\cite{einstein1905}, ...

Več avtorjev je raziskovalo to temo~\cite{lecun1998, knuth1997}.

Glede na~\cite{turing1938}, lahko trdimo ...
```

#### 3. Dodajanje seznama literature na konec dokumenta

```latex
\bibliographystyle{plain}  % ali alpha, abbrv, unsrt, itd.
\bibliography{moja-literatura}  % brez .bib končnice!

\end{document}
```

### Stili bibliografije

| Stil | Opis |
|------|------|
| `plain` | Številčno, urejeno po avtorjih |
| `alpha` | Skrajšave (npr. [Knu97]) |
| `abbrv` | Skrajšana imena revij in imen |
| `unsrt` | Številčno, v vrstnem redu pojavljanja |
| `ieeetr` | IEEE stil |

### Posebni primeri

#### Citiranje brez pojavljanja v besedilu

```latex
\nocite{einstein1905}  % Doda vir v seznam, ne citira ga
\nocite{*}             % Doda VSE vire iz .bib datoteke
```

#### Več citatov naenkrat

```latex
\cite{vir1, vir2, vir3}
```

#### Citati v poljubnem besedilu

```latex
Glej~\cite[stran 42]{knuth1997} za podrobnosti.
Kot navaja~\cite[poglavje 3]{einstein1905}, ...
```

### Kompilacija dokumenta z BibTeX

Za pravilno delovanje BibTeX morate dokument večkrat kompilirati:

```bash
pdflatex dokument.tex     # 1. korak
bibtex dokument           # 2. korak (brez .tex!)
pdflatex dokument.tex     # 3. korak
pdflatex dokument.tex     # 4. korak
```

Ali v enem ukazu:
```bash
pdflatex dokument && bibtex dokument && pdflatex dokument && pdflatex dokument
```

---

## 4. Primer celotne implementacije

### Datoteka `dokument.tex`

```latex
\documentclass[a4paper,12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[slovene]{babel}
\usepackage{amsmath, amssymb, amsthm}
\usepackage{url}

% Definicija novih ukazov
\newcommand{\R}{\mathbb{R}}
\newcommand{\p}{\mathbb{P}}
\newcommand{\norm}[1]{\|#1\|}

% Definicija novih operatorjev
\DeclareMathOperator{\diag}{diag}
\DeclareMathOperator*{\argmax}{arg\,max}

\title{Primer uporabe ukazov in virov}
\author{Janez Novak}
\date{\today}

\begin{document}

\maketitle

\section{Uvod}

V tej nalogi bomo raziskovali funkcije na $\R$ in izračunali 
$\argmax_{x \in \R} f(x)$, kot je opisano v~\cite{knuth1997}.

Verjetnost $\p(A)$ je definirana na~\cite{turing1938}.
Norma vektorja je $\norm{x} = 5$.

\section{Rezultati}

Matrika $A$ ima $\diag(A) = (1, 2, 3)$ na glavni diagonali.

\bibliographystyle{plain}
\bibliography{literatura}

\end{document}
```

### Datoteka `literatura.bib`

```bibtex
@book{knuth1997,
    author = {Knuth, Donald E.},
    title = {The Art of Computer Programming},
    publisher = {Addison-Wesley},
    year = {1997}
}

@phdthesis{turing1938,
    author = {Turing, Alan Mathison},
    title = {Systems of Logic Based on Ordinals},
    school = {Princeton University},
    year = {1938}
}
```

---

## Povzetek

1. **`\newcommand`**: Za definiranje poljubnih ukazov (simboli, bližnjice, makroji)
2. **`\DeclareMathOperator`**: Za matematične operatorje s pravilnimi razmiki
3. **BibTeX**: Za upravljanje literature s strukturiranimi vnosi v `.bib` datoteki
4. **Citiranje**: `\cite{ključ}`, `\nocite{ključ}`, `\bibliographystyle{stil}`, `\bibliography{datoteka}`
