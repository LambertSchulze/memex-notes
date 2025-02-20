---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-18
---
> The observer pattern defines a one-to-many dependency between objects so that when one object changes state, _all_ of its dependents are notified and updated automatically.

> The observer pattern allows a bunch of objects to be notified by a _central_ object when something happens.

Das Observer Pattern gehört auch zu den [[Design Patterns#Behavioral Patterns]]

Ein _Observer_ kann sich bei einem _Subjekt_ anmelden um über ein Event benachrichtigt zu werden.
Dafür muss eir eine Hook implementieren die das Subjekt für ihn aufrufen kann.
In dieser steht die Logik die passieren soll wenn das Event eingetreten ist.

Als zweites muss sich der Observer beim Subjekt subscriben.
Dies ruft dann in seiner Subscriber Liste alle Observer auf die sich dort eingetragen haben und führt bei denen die Hook aus.

Das Subjekt kann auch eine Funktion zum unsubscriben zur Verfügung stellen.

---
Es ist eine gute Idee wenn ein Observer ein Interface implementiert, in dem die Hook vorgeschrieben ist die es implementieren muss.
Dadurch kann das Subjekt in seiner Subscriber Liste alle Observer über das einheitliche Interface ansteuern.