---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-19
---
Ist der Cousin des [[Chain of Responsibility Pattern]].
Gehört daher auch zu den [[Design Patterns#Behavioral Patterns]].

Der Unterschied zum CoR Pattern ist dass die Middleware es _immer_ durch die Kette schafft.

---
Middleware ist so flexibel dass man es dynamisch hinzufügen, entfernen oder die Reihenfolge der Ausführungskette ändern kann.

Allerdings ist Middleware schwer zu debuggen.
Es könnte sein dass ein Request von keinem in der Kette bearbeitet wird.
Wird die Kette zu lang geht es auf die Performance.

---
Das Middleware Pattern bedient das [[Open Closed Principle]] und das [[Single Responsibility Principle]].
