---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-20
---
> _State_ is a way to organize your code so that an object can change its _behavior_ when its _internal state_ changes. It helps you represent different states as separate classes and allows the _object_ to switch between these states _seamlessly_.

Es gehört zu den [[Design Patterns#Behavioral Patterns]].

Es ist aus drei Elementen aufgebaut:
1. Context Klasse
   Sie hält eine Referenz auf das State Objekt.
   Verändert ihr Verhalten basierend auf den State.
2. Einheitliches Interface für alle verschiedenen State Klassen
   Dort stehen alle Methoden zu Aktionen drinnen die in jedem Zustand gemacht werden müssen.
3. Konkrete State Klassen
   Implementieren die Aktionen ihrem Zustand entsprechend.

Jedes State Objekt braucht eine Referenz auf die Context Klasse um in ihr den State ändern zu können.

---
Das State Pattern ist vom Aufbau wie das [[Strategie Pattern]].
Der einzige strukturelle Unterschied ist dass ein State Referenzen auf andere State Objekte haben kann.

Das State Pattern verändert das Verhalten seines Kontextes basierend auf den internen State ändert.
Das Strategie Pattern bietet dem Kontext _unabhängig vom State_ unterschiedliche Algorithmen an.

> A car can be in different states. The engine can be on, and the engine can be off. The battery can be dead. The tank can be empty, and so on. In all of these states, the car will behave differently. However, a driver can access the car’s interface: steering wheel, pedals, gears, etc. These are the states, and the entire behavior can be considered a combination of the conditions. All the states would provide a distinct behavior

