# Normalformen
Normalformen sind konzeptionelle Schemata bzw. Definitionen, denen der Aufbau von Tabellen folgen soll.  
Es gibt drei verschiedene Normalformen:

## Erste Normalform (1NF)
Die erste Normalform garantiert, dass man mit *ordentlichen* Tabellen arbeitet.  
Sie bedingt, dass alle Daten in atomarer Form gespeichert werden, d.h. jedes Attribut hat ein eigenes Feld und jedes Feld ist nur mit einem Datentyp gefüllt

## Zwei Normalform (2NF)
Die zweite Normalform besagt, dass

- die erste Normalform gegeben ist
- jedes Nicht-Schlüssel-Attribut vom Primärschlüssel **voll funktional abhängig ist**

## Dritte Normalform (3NF)
Die dritte Normalform besagt, dass

- die zweite Normalform vorliegt
- jedes Nichtschlüsselattribut nicht transitiv vom Primärschlüssel abhängig ist, d.h. **aus keinem Nichtschlüsselattribut folgt ein anderes Nichtschlüsselattribut**

## Siehe auch
[tinohempel.de](https://www.tinohempel.de/info/info/datenbank/normalisierung.htm)