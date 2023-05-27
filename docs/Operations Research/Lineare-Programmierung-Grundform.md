# Lineare Programmierung - Grundform
## Zielfunktion:
$max Z(x_1, x_2, ... ,x_n) = c_1x_1 + c_2 + x_2 + ... +  c_nx_n$

## Restriktionen:

### Technische Koeffizienten:
$a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n ≤ b_1$
$a_{21}x_1 + a_{22}x_2 + ... + a_{2n}x_n ≤ b_2$
$a_{m1}x_1 + a_{m2}x_2 + ... + a_{mn}x_n ≤ b_m$


$x_1, x_2, ..., x_n ≤ 0$


## Strukturvariablen/Entscheidungsvariablen
- $x_1, x_2$, etc sind Strukturvariablen

## Bedingungen
- Die Strukturvariablen müssen linear sein --> "lineare Programmierung"
- Die Grundform gilt nur für Maximierungen, nicht für Minimierungen
- Restriktionen sind immer ≤. Wenn ≥ -> multiplizieren mit -1
	- $5x_1 + 5x_2 ≥ 2$
	- $-5x_1 - 5x_2 ≤ -2$
- Falls eine Restriktion ein = hat -> durch zwei Ungleichungen ersetzen
	- aus $2x_1 - 3x_2 = 4$ wird:
	- $2x_1 - 3x_2 ≤ 4$
	- $2x_1 - 3x_2 ≥ 4$ -> $-2x_1 + 3x_2 ≤ -4$
