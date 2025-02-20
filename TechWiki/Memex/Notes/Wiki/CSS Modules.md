---
tags: css, nextjs
category: wiki
---

### Best practices

:: kein nesting von Selectoren
- Man muss es nicht machen und sollte es nicht machen.
  Es gibt im nachhinein Probleme wenn man deligiertes CSS mitbekommt welches das native eigentlich überschreiben sollte
:: Composing
- man kann classes auf andere classes anwenden
  ```.myClass {
	  composes: otherClass from '.style.css';
}```
  Das muss am Anfang der class stehen.
  Wenn man mehrere Klassen aus unterschiedlichen files anwendet ist die Reihenfolge _undefined_!
:: Global
- man kann eine Klasse global definieren
  ```:global(.textRed) {
	  color: red;
}```
- das selbe gilt für `:local` scope
- beim selectieren kann man in global und local scope springen
```.localA :global .global-b :local(.a.b) .global-c {
	...
}```
:: Variablen
- 