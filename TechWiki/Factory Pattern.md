---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-18
---
Das Factory Pattern ist ein [[Design Patterns#Creational Patterns]].
Es verbirgt die Details wie ein Objekt instanziiert vor dem Code der es benutzt.

Anstatt ein Objekt direkt mit `new` zu erschaffen lässt man es sich von der Factory geben.
Diese entscheidet welches Objekt erzeugt wird unter Berücksichtigung des Inputs.

---
Das Pattern hat fünf Bestandteile:
1. Es gibt ein Interface für die _Produkte_ welche die Factory erschaffen soll
2. Konkrete Klassen implementieren dieses Interface
3. Ein Interface der Factory.
   Dies ist optional aber nützlich wenn man Familien an Produkten erschaffen möchte.
4. Die konkrete Factory
5. Der _Client_ welcher die Factory benutzt und Produkte von ihr erzeugen lässt.