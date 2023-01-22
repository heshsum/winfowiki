# Listen und Mengen - abstrakter Datentyp
- Die allermeisten Algorithmen bearbeiten Daten zur Lösung eines Problems
- I.d.R. handelt es sich um verschiedene Einzelwerte --> Daten, die in einer bestimmten Struktur vorliegen --> Datenstruktur
- Mit einer Datenstruktur sind Operationen für Zugriff oder Veränderung verbunden
- Der Rechner benötigt aber eine konkrete Realisierung (Realisierung in Binärdaten, etc.)

> Ein **abtrakter Datentyp** ist ein Datentyp, der ausschließlich über seine Operationen definiert wird.
> Die innere Repräsentation der Daten und die Realsiierung der Operationen sind jedoch verkapselt, d.h. nach außen nicht sichtbar. 

# Abstrakter Datentyp Sammlung
- Bei den meisten praktischen Anwendungen handelt es sich um eine Sammlung von Daten

## Sammlung und ihre Operationen
### Bsp. Verwaltung von Studierendendatensätzen
- Einfügen
- Entfernen
- Suchen
- Ändern
- Iteration durch alle Elemente einer Sammlung

### Sortierte und unsortierte Sammlungen
Sammlungen können sortiert und unsortiert vorliegen.

# Listen
> Eine Liste ist eine **Folge von Elementen**, die in einer Reihenfolge vorliegen.

Daraus, dass es sich um Elemente in einer bestimmten Reihenfolge handelt, ergeben sich weitere Operationen:
- Ermittlung des Wertes an einer bestimmten Position (Index)
- Einfügen an einer bestimmten Position/Index
- Entfernen an einer bestimmten Position/Index


# Mengen
> Eine Menge ist eine ungeordnete Sammlung von Werten mit der Eigenschaft, dass kein Wert mehrfach vorkommt

Zusätzliche Operationen sind die Vereinigung oder der Durchschnitt von Mengen