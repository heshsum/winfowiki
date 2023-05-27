# Simplex Algorithmus

## Allgemeines
Ein Lineares Problem lässt sich in Matrixform schreiben:

$$
Ax=b
$$

- $A$ ist dabei eine $m x (n+m)$ Matrix  
- $x$ ist ein $(n + m)$-dimensionaler Vektor  
- b ist ein $m$-dimensionaler Vektor

Dies ergibt ein Gleichungssystem ohne eindeutige Lösung.  
Jedoch: wenn $n$ Einträge von $x$ gleich Null und $m$ Einträge ungleich Null sind, dann ergibt sich daraus:

$$
A^{(0)}x^{(0)}=b
$$

- $A$ ist eine $m x m$ Matrix
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

2.  Die aktuelle Isozielwertgerade (d.h. der aktuelle $Z$-Wert der Zielfunktion) wird die die Basisvariablen bestimmt.
3.  Man tauscht eine Basisvariable mit einer Nichtbasisvariable, um eine benachbarte Ecke zu bestimmen, die den höchstmöglichen Anstieg der Zielfunktion verspricht.  
    Ist kein Anstieg mehr möglich, wird der Simplex-Algorithmus abgebrochen, denn die aktuelle Ecke liefert bereits die optimale Lösung.
4. Zur Näherung an die Optimallösung verschiebt man die Isozielwertgerade parallel, sodass diese die neue Ecke schneidet.  
    Dabei findet ein *Eckentausch* bzw. ein *Basiswechsel* statt.