Margins von children in einem BFC werden nicht mit dem Margin eines Elements kombiniert welches einen BFC erschafft.

Das `html` Element definiert den äußersten und initial BFC.
Das heisst das jedes Element im `html` Element laut den Regeln von [[Flow Layout]].

Man kann ein Element ein eigenes BFC machen lassen
- mit `display: flow-root`
- mit `contain: layout`
- wenn sie [[Float]] benutzen
- wenn sie [[Absolute Position]]ed sind
- wenn sie flex items, grid items oder table cells sind
- wenn sie [[Multicolumn Container]]s sind