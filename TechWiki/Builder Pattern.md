---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-18
---
> A creational design pattern that lets you build and configure complex objects step-by-step.

> The pattern allows you to produce different types and representations of an object using the same construction code.

Ein Objekt das einem hilft ein anderes Objekt zu bauen.
Es gehört zu den [[Design Patterns#Creational Patterns]].

Es kann sehr nützlich sein um API Aufrufe zu übernehmen oder dem Objekt Zugriff auf andere Adapter zu verschaffen.

---
In der Regel ruft man beim Konstruieren Funktionen auf die bestimmte Attribute setzen:

```JS
const thing = new ThingBuilder()
	.setAttribute('this')
	.setSomeOtherAttribute('that')
	.makeItDoSomethingSpecial()
	.create()
```

---
Man kann einen Builder vor dem returnen des Objektes wieder nullen.
Dadurch kann man mit ein und demselben Builder mehrere Objekte erzeugen.

Ansonsten kann man auch mit einer Builder Instanz nur ein einziges Objekt erzeugen lasse

---
Das Builder Pattern kann Logik für das instanziieren eines Objektes einkapseln.
Damit erfüllt es das [[Single Responsibility Principle]].