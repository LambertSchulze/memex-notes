---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-19
---
Das Command Pattern ist ein [[Design Patterns#Behavioral Patterns]].

> They _encapsulate_ a request as a stand-alone object, allowing parameterization of clients with different requests, queueing or logging requests, and support undoable operations.

> The _command pattern_ encapsulates a task into an object, decoupling what it does, how it does it, and when it gets done. It also makes _undoing_ actions easy because it can keep a history of changes.

Das Command Pattern besteht aus 3 Haupt-Bestandteilen:

1. Das (Command) Interface:
   Hat eine public Methode, typischerweise `execute()`
2. Die eigentlichen Funktionen die das Interface implementieren und die Logik besitzen
3. Ein _invoker_ Objekt:
   Es hält die Referenz zur Command Klasse und führt irgendwann den Befehl aus.

Kapselt man Aktionen in Objekte kann man für diese auch eine _queue_ oder eine _history_ erstellen.

Das Command Pattern bedient das [[Single Responsibility Principle]] und das [[Open Closed Principle]].
Es erhöht allerdings auch die Komplexität der Codebase durch viele neue Klassen.

---
Für eine _undo_ Möglichkeit muss eine `undo()` Funktion erstellt werden.
Diese macht das Gegenteil von `execute()` und wird bei undo aufgerufen.

