# Simplex Algorithmus

## Allgemeines
Ein Lineares Problem lässt sich in Matrixform schreiben:

$$
Ax=b
$$

- $A$ ist dabei eine $m ⨯ (n+m)$ Matrix  
- $x$ ist ein $(n + m)$-dimensionaler Vektor  
- b ist ein $m$-dimensionaler Vektor

Dies ergibt ein Gleichungssystem ohne eindeutige Lösung.  
Jedoch: wenn $n$ Einträge von $x$ gleich Null und $m$ Einträge ungleich Null sind, dann ergibt sich daraus:

$$
A^{(0)}x^{(0)}=b
$$

- $A$ ist eine $m ⨯ m$ Matrix
- $x$ ist ein $m$-dimensionaler Vektor

**Soweit $A^{(0)}$ eine *singuläre* Matrix ist, hat die neue Gleichung eine eindeutige Lösung.**

## Beispiel

### Lineare Programmierung in Grundform:

$maxZ(x_1, x_2) = 4x_1 + 3x_2$  
$x_2 ≤ 6$  
$x_1 + x_2 ≤ 7$  
$3x_1 + 2x_2 ≤ 18$  
$x_1, x_2 ≥ 0$  

### Lineare Programmierung in Normalform:

$maxZ(x_1, x_2) = 4x_1 + 3x_2$  
$x_2 + y_1 = 6$  
$x_1 + x_2 + y_2 = 7$  
$3x_1 + 2x_2 + y3 = 18$  
$x_1, x_2, y_1, y_2, y_3 ≥ 0$

Diese Restriktionen lassen sich nun in Form einer Matrix der Form $Ax = b$ schreiben:

$A = \begin{bmatrix}
0 & 1 & 1 & 0 & 0 \\ 
1 & 1 & 0 & 1 & 0 \\ 
3 & 2 & 0 & 0 & 1 \\ 
\end{bmatrix}$
$x = \begin{pmatrix}
x_1 \\
x_2 \\
y_1 \\
y_2 \\
y_3 \\
\end{pmatrix}$
$b = \begin{pmatrix}
6 \\
7 \\
18 \\
\end{pmatrix}$

Hieraus lässt sich relativ simpel eine gültige Lösung ableiten, bei der $x_1$ und $x_2$ jeweils Null sind und die Schlupfvariablen maximiert werden:

$x = \begin{pmatrix}
x_1 \\
x_2 \\
y_1 \\
y_2 \\
y_3 \\
\end{pmatrix}$
$= \begin{pmatrix}
0 \\
0 \\
6 \\
7 \\
18 \\
\end{pmatrix}$

Die reduzierte $3 x 3$-Matrix hat nun das Format $A^{(0)}x^{(0)} = b$ mit den Inhalten:

$A^{(0)} = \begin{bmatrix}
1 & 0 & 0 \\ 
0 & 1 & 0 \\ 
0 & 0 & 1 \\ 
\end{bmatrix}$
$x^{(0)} = \begin{pmatrix}
y_1 \\
y_2 \\
y_3 \\
\end{pmatrix}$
$b^{(0)} = \begin{pmatrix}
6 \\
7 \\
18 \\
\end{pmatrix}$

Dieses neue LGS hat eine eindeutige Lösung.

## Die Simplex-Iteration
Der Simplex-Algorithmus besteht aus einer oder mehreren Durchläufen, bis die optimale Lösung gefunden wurden  

1.  Die aktuelle Lösung besteht aus

    1.  $m$ Basisvariablen (die nicht Null sind)
    2.  $n$ Nichtbasisvariablen, die die aktuelle Ecke der Fläche bestimmen

2.  Die aktuelle Isozielwertgerade (d.h. der aktuelle $Z$-Wert der Zielfunktion) wird durch die Basisvariablen bestimmt.
3.  Man tauscht eine Basisvariable mit einer Nichtbasisvariable, um eine benachbarte Ecke zu bestimmen, die den höchstmöglichen Anstieg der Zielfunktion verspricht.  
    Ist kein Anstieg mehr möglich, wird der Simplex-Algorithmus abgebrochen, denn die aktuelle Ecke liefert bereits die optimale Lösung.
4. Zur Näherung an die Optimallösung verschiebt man die Isozielwertgerade parallel, sodass diese die neue Ecke schneidet.

### Beispiel für den Simplex-Algorithmus
#### Lineares Problem in Grundform
Ausgangspunkt ist eine Lineares Problem in Grundform: 

$maxZ(x_1, x_2) = 4x_1 + 3x_2$  
$x_2 ≤ 6$  
$x_1 + x_2 ≤ 7$  
$3x_1 + 2x_2 ≤ 18$  
$x_1, x_2 ≥ 0$

#### In Normalform überführen
Das LP muss als erstes in die Normalform konvertiert werden (siehe [hier](Lineare-Programmierung-Normalform.md)).  
Das so erhaltene LP sieht wie folgt aus:

$Z = 0 + 4x_1 + 3x_2$  
(I) $y_1 = 6 - x_2$  
(II) $y_2 = 7 - x_1 - x_2$  
(III) $y_3 = 18 - 3x_1 - 2x_2$  
$x_1, x_2, y_1, y_2, y_3 ≥ 0$

#### 1. Durchlauf

##### Eintrittvariable wählen
> Als Eintrittsvariable wird diejenige Nichtbasisvariable der Zielfunktion genutzt, die das größte Wachstum aufweist.  

Die Eintrittsvariable in diesem Beispiel ist daher $x_1$.

##### Austrittsvariable wählen
Um die Austrittsvariable zu bestimmen löst die Gleichungen nach der gewählten Eintrittsvariable auf.  
Da (I) nicht die Eintrittsvariable $x_1$ enthält, ist dies nur bei (II) und (III) möglich:

(II) $y_2 = 7 - x_1 - x_2$  
$= x_1 = 7 - x_2 - y_2$

(III) $y3 = 18 - 3x_1 - 2x_2$  
$= 3x_1 = 18 - y_3 - 2x_2$  
$= x_1 = 6 - \frac{1}{3}y_3 - \frac{2}{3}x_2$

> Die Austrittsvariable ist die Austrittsvariable, die den kleinsten Wert ≥ 0 für die Eintrittsvariable aufweist.

In diesem Fall ist dies bei Gleichung (III), daher ist die Austrittsvariable $y_3$.

##### Umrechnung des Gleichungssystems
Die Umrechnung des Gleichungssystems erfolgt in zwei Schritten:

1. $x_1$ und $y_3$ tauschen die Plätze, d.h. (III) wird nach $x_1$ umgestellt.  
2. $x_1$ wird in jeder Gleichung durch den errechneten Term ersetzt.  

$Z = 0 + 4(6 - \frac{1}{3}y_3 - \frac{2}{3}x_2)+3x_2$  
(I) $y_1 = 6 - x_2$  
(II) $y_2 = 7 - (6 - \frac{1}{3}y_3 - \frac{2}{3}x_2) - x_2$  
(III) $x_1 = 6 - \frac{1}{3}y_3 - \frac{2}{3}x_2$

Vereinfacht:

$Z = 24 - \frac{4}{3}y_3 + \frac{1}{3}x_2$  
(I) $y_1 = 6 - x_2$  
(II) $y_2 = 1 + \frac{1}{3}y_3 - \frac{1}{3}x_2$  
(III) $x_1 = 6 - \frac{1}{3}y_3 - \frac{2}{3}x_2$

#### 2. Durchlauf
Ausgangspunkt des 2. Durchlauf ist das letzte LP des ersten Durchlaufs.


##### Eintrittsvariable wählen
Als Eintrittsvariablen kommen $y_3$ und $x_2$ infrage.  
Da $y_3$ einen negativen Faktor hat, würde die Zielfunktion kleiner werden, je größer $y_3$ wird.  
Daher ist $x_2$ die Variable mit dem größten Wachstum und somit auch die Eintrittsvariable.

##### Austrittsvariable wählen
Es wird nach $x_2$ aufgelöst:

(I) $y_1 = 6 - x_2$  
$= x_2 = 6 - y_1$

(II) $y_2 = 1 + \frac{1}{3}y_3 - \frac{1}{3}x_2$  
$= x_2 = 3 + y_3 + y_2$

(III) $x_1 = 6 - \frac{1}{3}y_3 - \frac{2}{3}x_2$  
$= x_2 = 9 - \frac{1}{2}y_3 - x_1$

Die Austrittsvariable ist $y_2$

##### Umrechnung des Gleichungssystems
1. (II) wird nach $x_2$ umgestellt.
2. In (I) und (III) wird der erhaltene Term für $x_2$ eingesetzt

$Z = 24 - \frac{4}{3}y_3 + \frac{1}{3}(3 + y_3 - 3y_2)$  
(I) $y_1 = 6 - (3 + y_3 - 3y_2)$  
(II) $x_2 = 3 + y_3 - 3y_2$  
(III) $x_1 = 6 - \frac{1}{3}y_3 - \frac{2}{3}(3 + y_3 - 3y_2)$

Vereinfacht:

$Z = 24 - \frac{4}{3}y_3 + \frac{1}{3}(3 + y_3 - 3y_2)$  
$= 25 - y_3 - y_2$

(I) $y_1 = 6 - (3 + y_3 - 3y_2)$  
$= y_1 = 3 - y_3 - 3y_2$

(II) $x_2 = 3 + y_3 - 3y_2$

(III) $x_1 = 6 - \frac{1}{3}y_3 - \frac{2}{3}(3 + y_3 - 3y_2)$  
$= x_1 = 4 - y_3 + 2y_2$

#### Ende des Verfahrens
Würde man an dieser fortfahren, würden $y_2$ oder $y_3$ größer als Null und Z daher kleiner als 25 werden.  
Somit ist der bisherige Stand die optimale Lösung.

Ergebnis:  
$Z^{*} = 25$ mit $x_1^{*} = 4$ und $x_2^{*} = 3$.