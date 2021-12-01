---
title: "Analisi sui comuni che guadagnano di più con la polizia municipale"
date: 2016-10-10T00:00:00+02:00
draft: false
toc: true
summary: "Ho fatto qualche grafico sui comuni che incassano di più con la pulizia municipale."
tags: ["reddit", "politica"]
---

Grazie ai dati messi a disposizione da openpolis/openbilanci ho fatto qualche grafico sui comuni che incassano di più con la pulizia municipale; questo comprende tutte le entrate realizzate nell’esercizio delle funzioni di polizia, tra cui le contravvenzioni per infrazioni al codice della strada.

**Premessa**

Tutte le analisi partono dai dati su incasso **_pro capite_** cioè quanto un comune incassa per ogni abitante del comune stesso.

I dati sono del 2014.

Non tutti i comuni hanno presentato questa voce, l'esempio più grosso è Napoli.


### Iniziamo con un grafico per regione

![Grafico](/images/guadagno-vigili/regioni.png)

[Grafico interattivo](https://datawrapper.dwcdn.net/gOnHg/2/)

### Maggiori comuni

Con più di 200.000 abitanti

![Grafico](/images/guadagno-vigili/maggiori.png)

[Grafico interattivo](https://datawrapper.dwcdn.net/gadmR/2/)

### Top 50 comuni

![Grafico](/images/guadagno-vigili/comuni.png)

[Grafico interattivo](/subpages/guadagno-vigili/comuni/)

## Fonti

[Blog OpenPolis](http://blog.openpolis.it/2016/10/05/quanto-guadagnano-i-comuni-con-multe-e-contravvenzioni/10182)

[Dati grezzi](http://www.sharecsv.com/s/19b8ee877302321b2c9ada38609b06dc/regioni.csv)

[Dati di Open Bilanci](http://www.openbilanci.it/classifiche/entrate/consuntivo-entrate-cassa-entrate-extratributarie-servizi-pubblici-polizia-locale/2014)


### Cosa ho utilizzato
Ho preso i dati dal post di openpolis. Li ho elaborati con Excel: una tabella pivot e un ordinamento top 50.

Per i grafici ho usato [Google geochart](https://developers.google.com/chart/interactive/docs/gallery/geochart).

Per la creazione delle pagine ho usato [Thimble di Mozilla](https://thimble.mozilla.org/).

#### Aggiornamento 2021-10-05

Le mappe originali erano su Google Charts, ma a causa del cambio di licenza, non è più possibie includere i grafici gratuitamente.  
Ho quindi salvato degli screenshot e migrato i dati su DataWrapper.