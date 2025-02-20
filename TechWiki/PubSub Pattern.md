---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-18
---
PubSub ist ähnlich zum [[Observer Pattern]].
Es gehört zu den [[Design Patterns#Behavioral Patterns]].

Beim Observer Pattern ist der Observer das Subjekt welches seine Subscriber benachrichtigt.
Ein Observer kann auch eine grössere Klasse sein welches dies nebenbei macht.

Beim PubSub hat man eine dedizierte Klasse, den _Publisher_/_Event Dispatcher_ der sich um das benachrichtigen kümmert.

Ein _Listener_ subscribed sich beim _Dispatcher_ dass er benachrichtigt werden möchte.
Das _Subjekt_ gibt dann dem Dispatcher nur noch Bescheid wenn das Event eingetreten ist.

---
Den Listenern wird in der Regel ein _Event Objekt_ für deren Hook übergeben.
Dort stehen all die Daten zum Event drinnen.

---
PubSub hält sich besser an das [[Single Responsibility Principle]] als das [[Observer Pattern]].
