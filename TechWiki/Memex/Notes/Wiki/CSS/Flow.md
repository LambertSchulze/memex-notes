---
tags: css
category: wiki
---

Dies ist der standard [[Layout Modus|Modus]] wie CSS Elemente positioniert.
Er ist für Textdokumente ausgelegt,
ähnlich wie in WYSIWYG Text Editoren.

Alle HTML Elemente die nicht `table` sind, benutzen den Flow Modus.
`inline` Elemente werden wie Textbausteine aneinander gehängt.
Größere Elemente wie headings oder paragraphs sind `block` Elemente,
die untereinander gesetzt werden.

Inline Elemente werden Seite an Seite aneinander gereiht.
Fehlt der Platz, springen sie auf die nächste Zeile.
Die Richtung hängt dabei von der benutzten Sprache ab.

Das `z-index` Attribut ist in Flow nicht implementiert, da in diesem Modus keine Elemente übereinander liegen können.

