# Simplex Algorithmus

## Allgemeines
Ein Lineares Problem lässt sich in Matrixform schreiben:

$$
Ax=b
$$

- $A$ ist dabei eine $m ⋅ (n+m)$ Matrix  
- $x$ ist ein $(n + m)$-dimensionaler Vektor  
- b ist ein $m$-dimensionaler Vektor

Dies ergibt ein Gleichungssystem ohne eindeutige Lösung.  
Jedoch: wenn $n$ Einträge von $x$ gleich Null und $m$ Einträge ungleich Null sind, dann ergibt sich daraus:

$$
A^{(0)}x^{(0)}=b
$$

- $A$ ist eine $m ⋅ m$ Matrix
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

