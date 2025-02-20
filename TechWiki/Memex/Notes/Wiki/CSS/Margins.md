---
tags: margins
category: wiki
---

Margin ist der Abstand eines Elements zu seinen siblings.
(Dies steht im Gegensatz zu Padding welches der Abstand zwischen parent und children ist.)

Margins werden kombiniert [[Margin Collapse]]
- zwischen siblings in block Richtung
- von child zu parent solange der parent keinen [[Block Formatting Context]] erschafft.

Beim kombinieren gewinnt immer der größte Margin.

Margins können auch negativ sein.
Beim kombinieren von positiven und negativen Margins werden der größte positive und der größte negative Wert gesucht und diese verrechnet.

Im [[Flex Formatting Context]] und im [[Grid Formatting Context]] passiert kein Margin collapse.