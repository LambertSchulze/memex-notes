---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-18
---
> The strategy pattern defines a family of algorithms, encapsulates each one and makes them _interchangeable_. It lets the algorithm vary independently from clients that use it.

> The strategy pattern is a way to allow _part_ of a class to be rewritten from the _outside_.

Das Strategie Pattern gehört zu den [[Design Patterns#Behavioral Patterns]].

Häufig wird das Strategie Pattern benutzt wenn es Situationen gibt in denen verschiedene Algorithmen benutzt werden müssen

---
In der Regel sieht das so aus:
Man hat ein Interface das auf verschiedene Weise implementiert wird.

Wer das Interface benutzt hat dann die Möglichkeit die verschiedenen Implementierungen auswechseln.

---
Das Pattern erfüllt das [[Single Responsibility Principle]] und das [[Open Closed Principle]].

