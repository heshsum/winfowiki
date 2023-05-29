# Lineare Programmierung - Normalform

## Allgemeines
Für die Normalform wird eine LP in Grundform genommen und die ≤ durch = ersetzt.
Außerdem müssen die Schlupfvariablen beachtet werden.


## Zielfunktion:
$max Z(x_1, x_2, ... ,x_n) = c_1x_1 + c_2 + x_2 + ... +  c_nx_n$

## Restriktionen:

### Technische Koeffizienten:
$a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n + y_1 = b_1$
$a_{21}x_1 + a_{22}x_2 + ... + a_{2n}x_n + y_2 = b_2$
$a_{m1}x_1 + a_{m2}x_2 + ... + a_{mn}x_n + y_m = b_m$

### Nichtnegativitätsbedingungen
$x_1, x_2, ..., x_n ≥ 0$


### Strukturvariablen/ Entscheidungsvariablen
$x_1, x_2$, etc sind Strukturvariablen

### Schlupfvariablen
Im Gegensatz zur Grundform muss bei der Normalform der Schlupf berücksichtigt werden.  
Existiert Schlupf, wird die LP in der Normalform andernfalls ungültig.

## Umformung von der Grundform in die Normalform
1. Zielfunktion gleich Null setzen
2. Kleiner-gleich durch Gleichheitszeichen ersetzen und Schlupfvariablen einfügen
3. Nichtnegativitätsbedingungen aktualisieren

### Beispiel
Gegeben sei ein LP in Grundform:

$maxZ(x_1, x_2) = 4x_1 + 3x_2$  
$x_2 ≤ 6$  
$x_1 + x_2 ≤ 7$  
$3x_1 + 2x_2 ≤ 18$  
$x_1, x_2 ≥ 0$

#### Zielfunktion anpassen
Die Zielfunktion wird zu einer einfachen Gleichung.  
Hier wurde noch 0 stellvertretend für die Nichtbasisvariablen eingefügt:
$maxZ(x_1, x_2) = 4x_1 + 3x_2 | -4x_1 -3x_2$  
$\rightarrow Z = 0 + 4x_1 + 3x_2$

#### Kleiner-gleich durch Gleich ersetzen und Schlupfvariablen einfügen
$x_2 ≤ 6$  
$\rightarrow x_2 + y_1 = 6$  
$= y_1 = 6-x_2$

$x_1 + x_2 ≤ 7$  
$\rightarrow x_1 + x_2 + y_2 = 7$  
$= y_2 = 7 - x_1 - x_2$

$3x_1 + 2x_2 ≤ 18$  
$\rightarrow 3x_1 + 2x_2 + y_3 = 18$  
$= y_3 = 18 - 3x_1 - 2x_2$

#### Nichtnegativitätsbedingungen aktualisieren
$x_1, x_2 ≥ 0$  
$\rightarrow x_1, x_2, y_1, y_2, y_3 ≥ 0$


