---
title: "Avanti - Matteo Renzi Simulator"
date: 2017-07-18T00:00:00+02:00
draft: false
summary: "Sono venuto finalmente in possesso di _Avanti_ il libro di Matteo Renzi, dopo il successo di Alessandro Di Battista Simulator, ho quindi pensato di generare alcune frasi partendo dai più di 400kb di testo presenti, con il modello di markov, lo stesso che alimenta /r/italy_SS e /r/subredditSimulator."
tags: ["reddit", "politica"]
---

Grazie a Medialibrary, sono venuto finalmente in possesso di _Avanti_ il libro di Matteo Renzi.

Dopo il successo di [Alessandro Di Battista Simulator](https://www.reddit.com/r/italy/comments/5udtly/a_testa_in_su_alessandro_di_battista_simulator/), ho quindi pensato di generare alcune frasi partendo dai più di 400kb di testo presenti, con il modello di markov, lo stesso che alimenta /r/italy_SS e /r/subredditSimulator.

Ecco il risultato, buon divertimento:
> Lo specchio è il mondo del virale, la finestra è il lavoro degli incentivi e del Jobs Act.  
> E sicuramente vale la pena di fare qualche ragionamento in più e dimezzare le ore della cassa integrazione.  
> Che, lungi dall’essere solo un fattore etico, siamo in presenza di una ferita inaccettabile al diritto all’uguaglianza sostanziale.  
> Per ogni telecamera nuova che viene installata, ci deve essere un euro in più investito in sicurezza, ci deve essere un videomaker o un regista teatrale che sperimenta.  
> Ma lo penso anche ricordando a me stesso che non ci sono più le banche d’affari di una volta.  
> Ragazzi come Linarello e i suoi imitatori distruggevano i telai meccanici per non far morire quella straordinaria comunità.  
> L’idea che, con la nostra fatica e il nostro tentativo di creare una squadra economica, l’“unità di missione”, a Palazzo Chigi sono dipinti come i nuovi unni.  
> In una trasmissione televisiva disponibile a fare un campionato con l’Affrico.  
> E l’8 gennaio 2008, dopo la vittoria emoziona anche i robot.  
>   
> Perché quello che è accaduto con il governo dei mille giorni già definiscono in modo chiaro e puntuale.  
> I numeri del resto sono chiari e per una volta almeno ti rendi utile in casa.  
> Nella settimana della sconfitta vedo tre volte il presidente della Repubblica ha chiesto a tutte le forze politiche pensano il lavoro nello stesso modo.  
> No, non è l’impegno a dimettermi in caso di sconfitta non riconoscerà la vittoria della Clinton.  
> La mia impressione è che, al netto di tutto quello che fai, non hai il diritto di decidere da solo di andartene.  
> Ci hanno detto che la politica è un’altra.  
> In questo senso il Movimento 5 Stelle ma anche il senso del dovere.  
> La visione per la quale un avviso di garanzia non deve dimettersi automaticamente.  
> Se su alcuni punti non la penso allo stesso modo poi si alleeranno contro altri primi ministri.  
> In realtà qui l’unica cosa da cambiare è il significato autentico del costante attacco di De Bortoli.  
> Forse la ruggine per le dimissioni da presidente del Consiglio a visitare un carcere.  
> Eppure siamo circondati da una contronarrazione puramente distruttiva, che fa male all’Europa, che, da speranza politica, diventa guardiana antipatica.  
> Forse perché rimpiange la stagione dei malus, quella in cui la mia è la prima visita privata con la famiglia.  
> Puoi candidarti alla leadership e presentare i risultati di ciò che accadeva nel mondo del credito finché era legittimo farlo.  
> È soprattutto il modo di porsi nel rapporto con i paesi amici.  


Note tecniche:

* se qualcuno ha altri libri che meritano, me li segnali pure, se riesco potrei replicare il risultato più che volentieri.
* no, non condividerò il file originale, sarebbe una chiara violazione dei copyright del libro.
* per chi volesse replicare, io ho usato [markovify](https://github.com/jsvine/markovify), con i seguenti parametri: sequenze di 3/4 parole, massimo 6/10 della frase uguale all'originale.
* ho dovuto eliminare una dozzina di frasi, che sono state generate uguali ad altre.
* il file epub originale era molto buono, l'ho solo convertito con Calibre in txt e tolte le parti di troppo (numero del capitolo, frontespizio, colophon e simili).