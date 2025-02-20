---
category: note
tags:
  - SoftwareArchitecture
created: 2024-09-17
---
In Funktionaler Programmierung ist alles eine Funktion.
So wie in React.
JSX ist nur eine schöne Schreibweise für eine Funktion die DOM Elemente macht.

Aber einen anderen Punkt muss man eher im Kopf behalten:
In Funktionaler Programmierung sind Variablen nicht variabel.
Sie verändern sich nicht.

---
Kann ein Programm 100% funktional sein?
Sehr unwahrscheinlich.
Aber man kann bei Funktionaler Programmierung darauf achten, das überschreiben von Variablen zu minimieren.

---
Eine Herausforderung der FP ist der State.
Wie updated man einen State wenn man Variablen nicht verändern kann?

Wenn Speicherplatz und Rechenleistung kein Problem sind, kann man jede einzelne Transaktion speichern.
Dann kann der State berechnet werden indem man die Historie an Transaktionen durchrechnet.

[[Git]] ist ein Beispiel für dieses Vorgehen.