# O-Notation - Worst-Case-Laufzeit
Die O-Notation ist eine Abschätzung der Laufzeit eines Algorithmus bei unendlich großen Eingabegrößen.  
Mit der O-Notation wird die (theoretische) qualitative obere Schranke für die Laufzeit eines Algorithmus angegeben.

*Qualitativ* bezeichnet dabei, dass $O(g(n))$ eine echte Zahl als obere Schranke angibt, sondern bloß eine Konstante.  
Die *quantitative* obere Schranke wird von Faktoren wie Prozessor, Parallelität, Eingaben, I/O usw. beeinflusst.  
Die Bezugsgröße der *qualitativen* oberen Schranke abstrahiert somit die Performanz eines Algorithmus von der Hardware. Stattdessen werden Einteilungen in Klassen vorgenommen werden (konstant, logarithmisch, lineas, polynomial, exponentiell, u.a.).

> Für eine Funktion $g(n)$ bezeichnet man mit $O(g(n))$ eine Menge von Funktionen mit folgender Eigenschaft:  
> $O(g(n)) = \{f(n)$  : es ex. positive Konstanten $c$ und $n_0$,  
> so dass $0 ≤ f (n) ≤ c ⋅ g(n)$ für alle $n ≥ n_0\}$

> $O(g(n))$ ist die **Menge** aller Funktionen ${f(n)}$ bei denen die positiven Konstanten $c$ und $n_0$ existieren,  
> sodass gilt: $f(n) ≥ 0$ und $f(n) ≤ c ⋅ g(n)$  
> für: $n ≥ n_0$.

> $f(n) ∈ O(g(n))$, wenn $f(n) ≤ c ⋅g(n)$ für $n ≥ n_0$  
> Das bedeutet:  
> $f(n) ∈ O (g(n))$, wenn $f$ <u>nicht schneller</u> wächst als $g$.

## Bestimmung einer möglichst einfachen scharfen oberen Schranke
Man ist nicht nur an irgendeiner oberen Schranke interessiert, sondern diese sollte möglichst scharf (d.h. möglichst klein) sein.

Dazu eignet sich folgendes Vorgehen:
1. Streiche alle Konstanten weg
2. Nehme den Term mit dem größten Wachstum (da dieser langfristig das Wachstum von Laufzeit/Ressourcen dominiert, siehe [Laufzeitanalyse Grundlagen](Laufzeitanalyse-Grundlagen.md)).

### Beispiel Bestimmung der scharfen Schranke
1. Ausgangsgleichung:  
$f(n) = 3n^2 +  7n ⋅ log_n + 100$  
2. Streiche alle Konstanten weg:  
$f(n) = \cancel 3n^2 +  \cancel7n ⋅ log_n + \cancel{100}$  
3. Es bleibt:  
$f(n) = n^2 + n ⋅ log_n$  
4. Nehme den Term mit dem größten Wachstum:  
Wir wissen, dass $n^2$ stärker wächst als $n ⋅ log_n$.  
Daher lässt sich dies weiter vereinfachen:  
$f(n) = n^2 + \cancel{n ⋅ log_n}$  
5. Ergebnis:  
$f(n) ∈ O(n^2)$  

### Beispiel 2
1. Ausgangsgleichung:  
$f(n) = 4n^2 + 100n^3$  
2. Streichung der Konstanten:  
$f(n) = \cancel4 n^2 + \cancel{100}n^3$  
3. Nehme den Term mit dem größten Wachstum:  
$f(n) = n^3$  
4. Ergebnis:  
$f(n) ∈ O(n^3)$

## Weiterführende Links
[Khan Academy](https://de.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/big-o-notation)