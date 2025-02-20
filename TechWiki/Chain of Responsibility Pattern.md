---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-19
---
> The Chain of Responsibility is a way to set up a sequence of methods to be executed, where each method can decide to execute the _next_ one in the chain or _stop_ the sequence entirely.

Gehört zu den [[Design Patterns#Behavioral Patterns]].

Man teilt eine Logik in mehrere _handler_ auf.
Jeder von denen kann entscheiden ob er die Anfrage erfüllt, oder an den nächsten weitergibt.
Diese handler kettet man hintereinander.

Zu dem _HandlerInterface_ des Patterns gehören zwei Methoden:
1. `setNext()`
2. `handle()`

---
Die CoR ist ähnlich zum [[Middleware Pattern]].
Allerdings kann die CoR die Kette zu irgendeinem Punkt abbrechen.