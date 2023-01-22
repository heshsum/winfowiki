# Laufzeitanalyse Grundlagen
Man ist an möglichst guten (effizienten) Algorithmen interessiert, daher analysiert man Algorithmen.

Bei der Analyse werden Vorhersagen über die Ressourcen getroffen, die ein Algorithmus benötigt, darunter:
- Zeit
- Speicher
- (Anzahl der) Prozessoren


## Hintergrunddisziplinen
Grundlagen der Analyse sind  
- Kombinatorik  
- elementare Wahrscheinlichkeitsrechnung  
- Algebra  
- Analysis  


## Eingabegröße/Problemgröße
Analysen werden immer in Abhängigkeit von der Eingabegröße bzw. Problemgröße vorgenommen.
Es ist klar, dass das Sortieren von 10.000 Werten länger dauert als das Sortieren von 100 Werten.
Was die Problemgröße/Eingabegröße bestimmt ist abhängig vom zu behandelnden Problem.


### Sortieren von Zahlenfolgen
Eingabegröße ist die Anzahl von Werten in der Folge.


### Multiplikation zweier beliebig großer Zahlen
Eingabegröße ist die Anzahl der Bits in Binärdarstellung beider Zahlen.

### Unterschiedliche Laufzeit bei gleicher Problemgröße
Die Laufzeit ist unter Umständen auch bei gleicher Problemgröße unterschiedlich.
Bei bestimmten Konstellationen kann die Laufzeit unterschiedlich sein, etwa kann das Sortieren von Arrays mit gleicher Länge je nach Inhalt unterschiedlich lange dauern.

## Worst-Case - Best-Case - Average-Case Laufzeit
Da es unterschiedliche Laufzeiten bei gleicher Eingabegröße $n$ gibt (je nach Konstellation der Daten), unterscheidet man zwischen verschiedenen Arten von Laufzeit:


### Best-Case Laufzeit
> Die Best-Case-Laufzeit bezeichnet die beste Laufzeit (kürzeste Laufzeit) unter allen Problemen der Größe $n$


### Worst-Case Laufzeit
> Die Worst-Case-Laufzeit bezeichnet die schlechteste Laufzeit (längste Laufzeit) unter allen Problemen der Größe $n$

Die Worst-Case Laufzeit ist häufig ähnlich der Average-Case Laufzeit.
Worst-Case Laufzeiten sind besonders wichtig, etwa für sicherheitskritische Anwendungsfälle (bspw. die Berechnung durch einen Autopiloten in einem Flugzeug).
Umgekehrt beschreibt die Worst-Case Laufzeit den Zeitrahmen, in dem ich garantiert eine Lösung zu meinem Problem erhalte.


### Average-Case Laufzeit
> Die Average-Case-Laufzeit bezeichnet die durchschnittliche Laufzeit aller Probleme der Größe $n$

Average-Case Laufzeiten sind schwer zu berechnen, da sie auf stochastischen Methoden basieren. Häufig sind sie aber nah an der Worst-Case Laufzeit.


## Messung von Laufzeiten
Die Messung von Laufzeiten basiert auf der Anzahl einfacher Operationen (bspw. Multiplikation, Sprungbefehl etc.). Unterschiedliche Operationen benötigen unterschiedlich viel Zeit. Wichtig ist für die Laufzeitanalyse, dass ein Typ von Operation immer eine (relativ) konstante Laufzeit hat.


## Additiver Term der größten Größenordnung
Angenommen ein Teil eines Algorithmus hat eine lineare Laufzeit und ein anderer Teil hat eine quadratische Laufzeit für die Problemgröße ```n```, so domiert die quadratische Laufzeit die Gesamtlaufzeit des Algorithmus.