---
title: "Orientamento delle città italiane"
date: 2018-07-16T00:00:00+02:00
tags: ["reddit", "geografia"]
summary: "Ho creato dei grafici che rappresentano \"come sono orientate\" le città italiane."
---

Ispirato da [questo articolo](http://geoffboeing.com/2018/07/city-street-orientations-world/) 
ho creato, grazie a
[tanto bel codice](https://github.com/gboeing/osmnx-examples/blob/master/notebooks/17-street-network-orientations.ipynb)
quasi già pronto,
dei grafici che rappresentano "come sono orientate" le città italiane.

In pratica il programma,
che trovate condiviso [su anaconda](https://notebooks.anaconda.org/timendum/street-network-orientations),
scarica da [OpenStreetMap](http://openstreetmap.org/)
le strate di una città,
poi semplifica la cartina,
fa l'elenco delle strade che rimangono
e ne calcola l'orientamento,
cioè trova qual'è la loro direzione seguendo la bussola,
quindi il tutto viene rappresentato in grafico.

Due note sui grafici:

1. non sono normalizzati tra loro,
cioè gli assi solo lunghi diversi tra grafici.
1. Sui grafici vengono rappresentate
quante strade sono orientate in un certo modo.

Ho analizzato le città con più abitanti d'Italia più alcune città interessanti.

![Roma](/images/orientamento/PllPntU.png)

![Milano](/images/orientamento/HmsZR4J.png)

![Napoli](/images/orientamento/Lzsm9CV.png)

![Torino](/images/orientamento/jzuPoug.png)

![Palermo](/images/orientamento/u6dQozd.png)

![Genova](/images/orientamento/JpX9Ehy.png)

![Bologna](/images/orientamento/yBsGGlW.png)

![Firenze](/images/orientamento/MP1RZaW.png)

![Catania](/images/orientamento/cZPT77g.png)

![Reggio Calabria](/images/orientamento/YDaLddB.png)

![Bari](/images/orientamento/YjLijPy.png)

![Giulianova](/images/orientamento/cQGwCwE.png)

![Parmanova](/images/orientamento/iChp2xi.png)

![Cortemaggiore](/images/orientamento/pd4CVCh.png)

![Bergamo](/images/orientamento/h6MOs07.png)

![Bitonto](/images/orientamento/jCx4dNu.png)

![Grammichele](/images/orientamento/YSRFVZD.png)

![Verona](/images/orientamento/FYJOW85.png)

![Messina](/images/orientamento/ImyAL6l.png)

![Padova](/images/orientamento/9yXfgio.png)

![Latina](/images/orientamento/r5xZXB1.png)


Per i più curiosi
[su questo album](https://imgur.com/a/EBYIOIG)
trovate la cartina semplificata di ogni città analizzata.

Extra sui grafici:
ho provato ad aggiungere "peso" in base alla lunghezza della strada,
il risultato non cambia sensibilmente.

Edit: Aggiungo, a parte, [Venezia](https://imgur.com/a/s5s4fZR), però tecnicamente il comune di Venezia include anche Mestre e le zone limitrofe.  
Se passo all'isola invece, chiaramente le strade per le automobili sono pochissime, quindi devo cambiare l'estrazione dei dati per includere anche le strade pedonali etc.
