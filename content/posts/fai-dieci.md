---
title: "Fai 10, soluzioni e le alternative"
date: 2026-03-18T00:00:00+02:00
draft: false
summary: "Descrizione del gioco _Make 10_, uno script per trovale le soluzioni e la ricerca di soluzioni diverse da 10."
tags: ["python", "matematica"]
---

Ho trovato per Android il gioco [4=10](https://play.google.com/store/apps/details?id=app.fourequalsten.fourequalsten_app),
completamente offline e ottimo per passare qualche minuto in attesa senza fare doom-scrolling
e da lì è partita la curiosità.

## Fai 10

Il gioco è semplice: dati un quattro numeri,
lo scopo è ottenere il numero `10` usando tutti e quattro i numeri esattamente una volta,
combinandoli con operazioni matematiche.

Nella mia versione sono ammesse:

- addizione
- sottrazione
- moltiplicazione
- divisione
- parentesi per cambiare l’ordine delle operazioni

Poi ci sono altre varianti in cui
la posizione di una o più cifre è fissa,
oppure viene negata la possiblità di utilizzare partentesi,
o si possono sare solo alcune operazioni,
o alcune operazioni hanno una posizione fissa,
o simili costrizioni.


### Esempio

Mi vengono fornite queste quattro cifre: `4`, `8`, `4`, `7`.

Alcune delle soluzioni sono:

- `8 / 4 × 7 − 4 = 10` 
- `7 + (4 + 8) / 4 = 10`

Più le tante variazioni matematiche, come:

- `(8 + 4) / 4 + 7`
- `8 / (4 / 7) - 4` (che equivale a `8 / 4 * 7 - 4`)

## La storia

Sembra che il gioco sia nato come "The Sydney Train Game",
perchè a Sydney le carrozze dei treni sono indentificate da quattro cifre
e i pendolari hanno iniziato ad utilizzarle mentalmente per arrivare a 10.  
Nel tempo è diventato una piccola tradizione tra gli utenti e il nomer è rimasto.

L'ho trovato descritto su [Reddit nel 2011](https://www.reddit.com/r/sydney/comments/gzx2d/cityrail_number_game/).

## Soluzioni

Ho scritto [questo piccolo script](https://gist.github.com/timendum/328086fc7ee29b7a901725308108716a#file-find_solution-py)
in Python che trova tutte le soluzioni, gestisce restrizioni sulle operazioni disponibili,
cioè è possibile elencare le operazioni che possono apparire nella soluzione, se non sono tutte.

Se non ho sbagliato l'implementazione, ci sono 549 possibili soluzioni
del problema base con obliettivo 10 se ammettiamo le parentesi,
che diventano 439 senza parentesi.

## Alternative

Come passo successivo mi sono chiesto se ci fossero dei numeri alternativi a 10,
per lo stesso problema, cioè quale sia il migliore obbiettivo del problema.

Quindi ho scritto [quest altro piccolo script](https://gist.github.com/timendum/328086fc7ee29b7a901725308108716a#file-sol_count-py)
che fa il giro e prova tutto, di default si ferma alla prima soluzione,
ma potrebbe trovarle tutte.

| target | con parentesi | senza parentesi |
|:-------|:--------------|:----------------|
| 1      | 656           | 583             |
| 2      | 654           | 573             |
| 3      | 612           | 529             |
| 4      | 606           | 509             |
| 5      | 604           | 485             |
| 6      | 612           | 498             |
| 7      | 597           | 471             |
| 8      | 595           | 471             |
| 9      | 587           | 465             |
| 10     | 549           | 439             |
| 11     | 495           | 424             |
| 12     | 541           | 400             |
| 13     | 447           | 372             |
| 14     | 483           | 377             |
| 15     | 478           | 357             |
| 16     | 487           | 340             |
| 17     | 390           | 303             |
| 18     | 471           | 294             |
| 19     | 361           | 269             |
| 20     | 422           | 249             |

Quindi 12 sarebbe un buon candidato alternativo nel caso di parentesi.
