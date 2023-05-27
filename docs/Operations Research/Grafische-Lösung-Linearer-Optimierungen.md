Bei der grafischen Lösung der linearen Optimierung wird (wie der Name schon suggeriert) die Optimierung mit Hilfe von Zeichnungen im Koordinatensystem gelöst.

Die Grundidee liegt darin, Funktionen für die Zielfunktion und die verschiedenen Nebenbedingungen aufzustellen. Eingezeichnet in ein Koordinatensystem ergibt sich hieraus eine Fläche. Die optimale Lösung ist einer der Eckpunkte dieser Fläche.

# Ablauf
## Variablen festlegen
Als ersten Schritt müssen die Variablen festgelegt werden, nach denen optimiert werden soll. Oftmals sind dies in den Aufgabenstellungen Mengeneinheiten (etwa für Rezepte) oder Flächenangaben.
Kommen derartige Variablen vor, gilt sogleich die **Nichtnegativitätsbedingung** wie $x ≥ 0$ oder $y ≥ 0$.

## Nebenbedingungen aufstellen
Als zweiten Schritt müssen die **Nebenbedingungen** aufgestellt werden. 
Die **Nebenbedingungen** bestehen aus **Restriktionen** und **Nichtnegativitätsbedingungen**.

Dies ist bspw. die Höchstmenge Fett in einem Rezept. Achtung: diese Nebenbedingungen sind **Ungleichungen** wie bspw.:
1. $2x + 5y ≤ 25$ (für den Fall "höchstens") oder
2. $2x + 5y ≥ 25$ (für den Fall "mindestens")
3. $x ≥ 0$
4. $y ≥ 0$

## Zielfunktion festlegen
Die **Zielfunktion** ist die Funktion für die Errechnung des Endergebnisses, wie bspw. das Errechnen des Fettgehalts in einem Rezept.

Zielfunktionen werden zumeist angegeben in der Form von $z = 1,5x + 3y$

## Nebenbedingungen nach y umstellen und einzeichnen
Achtung: bei Ungleichungen handelt es sich nicht um Geraden (oder andere Graphen), sondern um Flächen!

$2x + 5y ≤ 25$
$= 5y ≤ -2x + 25$
$= y ≤ -\frac{2}{5}x + \frac{25}{5}$

$2x + 5y ≤ 25$
$= 5y ≤ -2x + 25$
$= y ≤ -\frac{2}{5}x + \frac{25}{5}$

## Zielfunktion nach y umstellen und einzeichnen
$z = 1,5x + 3y$
$=3y = -1,5x + z$
$= y = -\frac{1,5}{3}x + \frac{z}{3}$

## Zielfunktion parallel verschieben zum Eckpunkt
Die Koordinaten des Eckpunktes geben nun die Lösung für $x$ und $y$ an.