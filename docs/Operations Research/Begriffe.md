# Begriffe
An dieser Stelle werden die wichtigsten Begriffe aus dem Bereich Operations Research gesammelt und erklärt.

## Zielfunktion
Die Zielfunktion ist Teil einer Linearen Programmierung.
Sie ist eine mathematische Funktion, mit der bspw. der Preis oder eine Outputmenge berechnet wird.
Allgemein ausgedrückt sieht eine Zielfunktion wie folgt aus:
$$
max Z(x_1, x_2,..., x_n) = c_1x_1 + c_2x_2 +...+c_nx_n
$$

### Restriktionen (Nebenbedingungen) und Nichtnegativitätsbedingungen
Restriktionen sind Teil einer Linearen Programmierung und geben die mathematischen Rahmenbedingungen der Linearen Programmierung an, etwa erlaubte Minimal- oder Maximalwerte.

Die Schreibweise einer Restriktion unterscheidet sich von der [Grundform](Lineare-Programmierung-Grundform.md) und der [Normalform](Lineare-Programmierung-Normalform.md).

## Strukturvariablen

## Schlupf und Schlupfvariablen
Schlupf ist die Differenz zwischen einer (optimalen) Lösung eines LP und einer Restriktion.  

Beispiel:

$(R1) x_1 ≤ 12$  
Ergibt nun die optimale Lösung einen Wert von $8$ für $x_1$, so ist der Schlupf für $x_1$ gleich $3$.

## Basisvariablen
Basisvariablen sind Variablen, die in der Zielfunktion nicht den Wert Null erhalten müssen.

## Nichtbasisvariablen
Nichtbasisvariablen sind Variablen, die nicht in der Zielfunktion enthalten sind und daher den Wert Null erhalten müssen.

## Grundform
Die Grundform ist eine eine Darstellungsweise einer Linearen Programmierung.
Näheres dazu in [Lineare Programmierung - Grundform](Lineare-Programmierung-Grundform.md)

### Unterschiede zur Normalform
1. Restriktionen werden mit kleiner-gleich geschrieben (nicht mit Nichtnegativitätsbedingungen verwechseln).
2. In der Grundform sind in den Restriktionen keine Schlupfvariablen enthalten.

### Nebenbedindungen in der Grundform
Neben der Zielfunktion gibt es noch Restriktionen, die den Raum möglicher Lösungen einschränken und Nichtnegativitätsbedingungen, die für die Variablen gelten.

#### Restriktionen in der Grundform

## Normalform
Die Normalform ist eine Darstellungsweise einer Linearen Programmierung.

$$
a_{m1}x_1 + a_{m2}x_2 +...+ a_{mn}x_n ≤ b_m
$$

### Unterschiede zur Grundform
1. Restriktionen werden mit Gleichheitszeichen geschrieben.
2. Schlupfvariablen werden mit in den Restriktionen bedacht.

### Nebenbedingungenin der Normalform
Neben der Zielfunktion gibt es noch Restriktionen, die den Raum möglicher Lösungen einschränken und Nichtnegativitätsbedingungen, die für die Variablen gelten.

#### Restriktionen in der Normalform
Teil der Nebenbedingungen ist, dass die Variablen $x_1$ bis $x_n$ nicht kleiner als Null werden dürfen.
$$
a_{m1}x_1 + a_{m2}x_2 +...+ a_{mn}x_n + y_n = b_m
$$
 
## Nichtnegativitätsbedingungen
Teil der Nebenbedingungen ist, dass die Variablen $x_1$ bis $x_n$ und die Schlupfvariablen $y_1$ bis $y_n$ nicht kleiner als Null werden dürfen.

$$
x_1, x_2,...,y_1,...,y_n ≥ 0
$$

Näheres dazu in [Lineare Programmierung - Normalform](Lineare-Programmierung-Normalform.md)