# Master-Theorem

## Allgemeines
Das Master-Theorem ist eine Theorem zur Analyse rekursiver Algorithmen.  
Die Laufzeit rekursiver Algorithmen lässt sich durch folgende rekursive Gleichung ausdrücken:

$$
T(n) = D(n) + a ⋅ T(n/b) + C(n)
$$
Gültig ist dies für $n >= n_0$.

Erklärung:
Ein Ausgangsproblem der Größe $n$ wird dabei in $a$ Teilprobleme zerlegt.
Jedes Teilproblem hat die Größe $n/b$.

$T(n)$ = Laufzeit zur Lösung eines Problems der Größe $n$.  
$D(n)$ = Zeit zum Zerlegen des Ausgangsproblems  
$a ⋅ T(n/b)$ = Zeit zum Lösen von $a$ Teilproblemen der Größe $n/b$  
$C(n)$ = Zeit zum Zusammenfügen der Teilprobleme

Mit dem Master-Theorem können solche rekursiven Gleichungen aufgelöst werden.

## Beispiel Mergesort

- Mergesort zerlegt in 2 Teilprobleme der Größe $n/2$
- Aufwand für das Zusammenfügen: $O(n)$
- Aufwand für das Zerlegen: $O(1)$

Für Größe Probleme der Größe $n$:

$$
T(n) =
    \begin{cases}
	O(1) && \text{für n = 1}\\
	2 ⋅T(n/2) + O(n) && \text{für n > 1}
    \end{cases}
$$

## Anwendung des Master-Theorems
Die rekursive Funktion muss sich wie folgt ausdrücken lassen:  
Wenn $n = b^i$ für ganzzahlige $i$ und
$$
T(n) =
    \begin{cases}
	O(1) && \text{für } n = 1\\
	a ⋅T(n/b) + f(n) && \text{für }n = b^i
    \end{cases}       
$$

$n = b^i$ steht dafür, dass ein Problem $n$ rekursiv in $b$ gleiche Teile zerlegt werden kann.
$f(n)$ bezeichnet den Aufwand für das Zerlegen und Zusammenfügen
dann gilt:
$$
T(n) =
    \begin{cases}
	Θ(n^{log_b a}) && \text{, wenn } f(n) ∈ O(n^{log_b a - ∈}) \\
	Θ(n^{log_b a} log_2 n) && \text{, wenn } f(n) ∈ Θ(n^{log_b a}) \\
	Θ(f(n)) && \text{, wenn } f(n) ∈ Ω(n^{log_b a + ∈}) \text{ und } && \\  &&  a\ f(n/b) <= c\ f(n)  \text{ und genügend großes } n\\
    \end{cases}       
$$

### Fälle und Bedingungen
Die drei Fälle sind abhängig von $f(n)$, also vom Aufwand für das Zerlegen und Zusammenfügen.  
Zur Analyse werden die Werte von $a$ und $b$ in die jeweilige Formel für $f(n)$ eingesetzt. Dabei der Analyse wird immer beim Fall 2 gestartet.

### Ablauf

#### 1. Prüfung der Bedingung 2. Fall
Es wird immer bei der Prüfung der Bedigung für den zweiten Fall gestartet. Je nach Ergebnis kann dann ggf. ein weiterer Fall oder direkt die Laufzeit bestimmt werden.

D.h.: $a$ und $b$ einsetzen in $f(n) ∈ Θ(n^{log_b a})$.  
Wenn $f(n)$ größer oder kleiner ausfällt als $Θ(n^{log_ba})$, dann noch einmal für den 1. oder 3. Fall testen.

#### 2. Berechnung der Laufzeit
Je nach Ergebnis der Prüfung der Bedingung muss dann $T(n)$ anhand einer der drei Formeln bestimmt werden.


## Weiterführende Links
1. https://hpi.de/friedrich/teaching/units/rekurrenzen-und-master-theorem.html
2. https://page.mi.fu-berlin.de/mulzer/notes/ha/master.pdf