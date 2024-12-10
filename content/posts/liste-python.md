---
title: "Uso avanzato delle liste in Python"
date: 2024-12-10T00:00:00+02:00
draft: false
summary: "Schemi per usare l'oggetto list di Python in maniera più efficace."
tags: ["programmazione", "python"]
---

Mi dimentico sempre che le `list` in Python possono essere fare molto di più che un array classico.

Quindi qualche schema per ricordarmi come funziona.

## Metodi

### pop

Con `pop` si possono riumuovere anche elementi in mezzo alla lista.

    >>> a = [10, 11, 12, 13, 14]
    >>> a.pop(3)
    13
    >>> a
    [10, 11, 12, 14]

### remove

Invece `remove` riumuovere un preciso elemento, **senza indice**, ovviamente non lo restituisce, dovrei già averlo.

In pratica equivale a `a.remove(a.index(x))`, quindi lancia un `ValueError` se l'elemento non esiste, proprio come `index`.

    >>> a = [10, 11, 12, 13, 14]
    >>> a.remove(13)
    <None>
    >>> a
    [10, 11, 12, 14]

### insert

Infine `insert` aggiunge un elemento nel posto indicato, facendo slittare gli altri.

    >>> a = [10, 11, 12, 13, 14]
    >>> a.insert(1, 60)
    <None>
    >>> a
    [10, 60, 11, 12, 13, 14]

Se l'indice è più grande della lunghezza della `list`, verrà aggiunto alla fine.

    >>> a = [10, 11, 12, 13, 14]
    >>> a.insert(100, 60)
    <None>
    >>> a
    [10, 11, 12, 13, 60]

## Ricette

### Inserire due oggetti al posto di uno

Vogliamo ad esempio da `[10, 11, 12, -1, 15]` togliere  `-1` nel seguente array e metterci `13` e `14`.

Con il primo modo, togliamo e poi inseriamo, occhio se se li inseriamo nella stessa posizione, vanno inseriti in **ordine inverso**, prima `14` poi `13`.

    >>> a = [10, 11, 12, -1, 15]
    >>> a.remove(-1)
    >>> a.insert(3, 14)
    >>> a.insert(3, 13)
    >>> a
    [10, 11, 12, 13, 14, 15]

In alternativa, possono essere inseriti nell'ordine giusto, ma l'indice va incrementato.

    >>> a = [10, 11, 12, -1, 15]
    >>> a.remove(-1)
    >>> a.insert(3, 13)
    >>> a.insert(4, 14)
    >>> a
    [10, 11, 12, 13, 14, 15]

Oppure, possiamo sovrascrivere ed inserire, con la stessa accortezza, cioè sovrascrivere con `14` e poi inserire con `13`.

    >>> a = [10, 11, 12, -1, 15]
    >>> a[3] = 14
    >>> a.insert(3, 13)
    >>> a
    [10, 11, 12, 13, 14, 15]

Infine stessa alternativa di prima, inserirli nell'ordine giusto ma incrementare l'indice.

    >>> a = [10, 11, 12, -1, 15]
    >>> a[3] = 13
    >>> a.insert(4, 14)
    >>>
    >>> a
    [10, 11, 12, 13, 14, 15]

### Invertire due elementi

Qui sempre meglio il classico "swap".

    >>> a = [10, 11, 24, 13, 42, 15]
    >>> x = a[2]
    >>> a[2] = a[4]
    >>> a[4] = x
    >>> a
    [10, 11, 42, 13, 24, 15]

O in un colpo solo.

    >>> a = [10, 11, 24, 13, 42, 15]
    >>> a[4], a[2] = a[2], a[4]
    >>> a
    [10, 11, 42, 13, 24, 15]