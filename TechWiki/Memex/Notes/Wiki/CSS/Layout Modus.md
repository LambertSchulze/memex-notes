---
tags: css
category: css
---

CSS hat verschiedene Arten Elemente anzuordnen.

- [[Flow]]
- [[Positioned]]
	- Relative
	- [[Absolute Position]]
	- Fixed
	- Sticky
- [[Float]]
- [[Table]]
- [[Flex Formatting Context]]
- [[Grid Formatting Context]]

Jeder Modus setzt die child elements in einen *formatting context*.
Durch verschiedene Attribute gibt man an welcher benutzt werden soll.
Manche Attribute sind in verschiedenen Modi anders oder auch gar nicht implementiert.

Um zu wissen wie ein Element auf bestimmte Attribute reagiert,
muss man wissen welchen Layout modes das parent Element einsetzt.

Wirken verschiedene Modi auf ein und dasselbe Element entscheidet eine Rangfolge.
Der Positioned Modus schlägt dabei alle anderen.

