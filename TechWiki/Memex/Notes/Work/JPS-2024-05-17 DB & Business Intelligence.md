Data Modeling and Sql [https://www.andreas-paech.de/entity-relationship-modeling-0cec516c5e964253a09398a0419d0865]
Normalisation [https://www.andreas-paech.de/normalisation-ac2b98be09a64d358c9de787fe49c455]


### ER-Model
Entity-Relationship Modell. Zeigt den Aufbau einer Datenbank und ihrer Tabellen.

### CHEN Notation
Diagramm zum aufmalen eines Modells.

### Normalformen
#### Erste Normalform
Eine Tabelle ist in der 1. NF wenn es nur atomisierte, unteilbare Werte hat und einen primary Key (unique identifier) hat.

In der ersten Normalform hat jedes Feld einen einzigen Wert.

#### Zweite Normalform
Eine Tabelle ist in der 2. NF wenn sie in der 1. NF ist und alle Attribute funktional Abhängig sind vom primary Key, nicht nur ein Teil von denen sind.

Hast du zwei Felder die zusammengenommen einen Tabelleneintrag eindeutig identifizieren, so müssen alle anderen Felder auch von beiden abhängen.
Hängt ein Feld nur von einem der beiden ab, muss man diese in eine eigene Tabelle aussondern.

#### Dritte Normalform
Eine Tabelle ist in der 3. NF wenn sie in der 2. NF ist und alle Attribute ausschliesslich vom primary key abhängen.

Hast du Felder die untereinander abhängen, lager die in eine eigene Tabelle aus.
Bsp:

| Buch-Titel | Author | Nationalität des Authors |

Nationalität d. Authors hängt vom Author ab der wiederum vom Buch abhängt.
Author und seine Nationalität sollten in eine eigene Tabelle ausgelagert werden.

---

- ein primary key sollte keine Information enthalten
- eine Änderung dieser Information würde eine Neuberechnung des kompletten binary tree nötig machen.
- Dies ist nicht nur für den Tree ein hoher Rechenaufwand, sondern kann auch in der Praxis ein hoher Aufwand sein

### Boyce-Codd normal form
Wird auch die 3.5 Normalform genannt. Sie ist ein bisschen strikter als die 3. NF [https://en.wikipedia.org/wiki/Boyce%E2%80%93Codd_normal_form]


Beispiel: Notion als relationales, dokumentenbasiertes DB-System
- Link 1: https://www.andreas-paech.de/er-modeling-in-notion-ecommerce-usecase-39b57f7489f2466ab911a5af97b93c9c
- Link 2: https://www.andreas-paech.de/er-modeling-in-notion-lecture-list-aa1e2e495aeb46188f528bda6ee2aca6

Zu lesen:
- SQL statements (SELECT ... FROM ... (JOIN) ... WHERE ... GROUP BY ... HAVING ... ORDER BY ... (LIMIT))
- SQL Use-case 1: OEM-Automative https://www.andreas-paech.de/sql-usecase-1-oem-automative-70bd988164b84c5f86f17f14d70bae8a
- SQL - Structured Query Language https://www.andreas-paech.de/structured-query-language-sql-fc98c087c10a42f8919b3429dcccc739
- SQLite Setup https://www.andreas-paech.de/local-setup-with-sqlite-27fdd80a991742d497775c78e2e0768a
- 