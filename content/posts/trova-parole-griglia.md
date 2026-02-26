---
title: "Trova le parole in griglia"
date: 2026-02-26T00:00:00+02:00
draft: false
summary: "Una pagina per trovare le parole più lunghe in una griglia di lettere."
tags: ["parole"]
---

Dopo aver assistito a due puntate di Deejay vs Deejay, ho sviluppato questa piccola
pagina in React + Vite + TailwindCSS che trova le parole più lunghe
in una griglia di lettere.

## [Trova le parole in griglia](https://timendum.github.io/trova-parole-griglia/)

È appena l'utente inserisce una lettera per casella di un quadrato almeno 3x3,
la pagina trova le parole più lunghe composte da lettere adiacenti,
cioè sopra, sotto, a sinistra, a destra o in diagonale.

Per la lista delle parole mi sono affidato a
[napolux/paroleitaliane](https://github.com/napolux/paroleitaliane),
in particolare ho preso il file 660000_parole_italiane e trasformato in JSON.

Il codice è disponibile su GitHub:
[timendum/trova-parole-griglia](https://github.com/timendum/trova-parole-griglia).

Confesso che l'algoritmo è in buona parte vibe-coded,
perché l'interesse che volevo dedicarci non era più alto.
