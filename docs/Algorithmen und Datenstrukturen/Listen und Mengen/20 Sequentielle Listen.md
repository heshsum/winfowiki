# Sequentielle Liste
## Sequentielle Liste am Beispiel Array
 > Die Realsierung einer Liste durch ein Array nennt man **sequentielle Liste**

### Annahmen:

 - Werte sind alle unmittelbar hintereinander abgelegt (keine Lücken)
 - beim Löschen von Werten rückend ie nachfolgenden Werte auf
 - Das Array ist i.d.R. größer als die Anzahl der abgelegten Werte
 - Zur Umsetzung benötigt man den Index des ersten freien Platzes --> ```firstFreeIndex```
 
 - Werte werden in aufeinanderfolgenden Speicherplätzen abgelegt
	 - Dadurch geringer Speicherplatzbedarf
 - Man kann über einen index auf verschiedene Werte zugreifen
 - Nachteil: Länge eines Arrays ist fest (anders als bei einer verketten Liste)
	 - Wenn der Platz ausgeschöpft ist, müssen ein neues Array angelegt und die Werte kopiert werden

## Operationen auf sequentiellen Listen
### Einfügen
- Einfügen ist nur möglich, wenn das Array nicht voll belegt ist.
- Ist ein Array voll, muss ein neues, größeres Array angelegt werden und alle Werte müssen kopiert werden (Zeitaufwand $O(n)$).
### Operationen
- Zugriff auf Index
- Wert einfügen
- ```FirstFreeIndex``` um $1$ erhöhen

Beides ist mit konstanter Laufzeit möglich. Daraus ergibt sich ein Worst-case/best-case Zeitaufwand von $O(1)$.

 
#### Zeitaufwand
Worst-case: $O(n)$
Der worst case tritt ein, wenn ein Element am Anfang eingefügt werden muss.
$n$ ist hierbei die Anzahl aller Elemente im Array.
 
Best-case: $O(1)$
Der best case tritt ein, wenn ein Element am Ende angefügt werden muss. --> konstanter Aufwand
 
### Entfernen
 - Alle Elements sollen immer unmittelbar hintereinander im Speicher liegen (keine Leerstellen)
- Bei Beibehaltung der Reihenfolge müssen alle nachfolgenden Elemente verschoben und der ```FristFreeIdnex``` um $1$ verringert werden. Daraus ergeben sich folgende Aufwände:
	- Worst case: $O(n)$ (wenn das erste Element gelöscht wird)
	- Best case: $O(1)$ (wenn das letzte Element gelöscht wird)
- Bei beliebiger Reihenfolge wird das zu löschende Element mit dem letzten Element aus dem Array überschrieben und der ```FirstFreeIndex``` um $1$ verringert. Daraus ergibt sich folgender Aufwand:
	- Worst case/ best-case: $O(1)$, da jede Teiloperation eine konstante Laufzeit hat.

### Entfernen aus sequentieller Liste (bei Beibehaltung der Reihenfolge)

- Element löschen, indem alle nachfolgenden Element um 1 nach vorn gerückt werden
- FirstFreeIndex aktualisieren

#### Zeitaufwand
Worst-case: $O(n)$
Dieser Fall tritt ein, wenn der erste Wert im Array gelöscht werden soll.
Dann müssen alle Werte des Arrays geändert werden

Best-case: $O(1)$
Dieser Fall tritt ein, wenn das letzte Element im Array gelöscht wird
 
### Entfernen aus sequentieller Liste bei beliebiger Reihenfolge
#### Ausgangslage
- Element mit dem letzten Element des Arrays überschreiben
- FirstFreeIndex um 1 verringern

Beide Aufgaben sind mit konstanter Laufzeit zu bewerkstelligen.
Daher ergibt sich:

#### Zeitaufwand
Worst-case/best-case: $O(1)$ 
 
 
### Suchen
 
### Suchen bei unbekannter Position
 Beim Suchen eines Elements mit Wert/Schlüssel $s$ muss im schlimmsten Fall die ganze Liste durchlaufen werden.
#### Zeitaufwand
$$ O(n) $$
 
### Suchen bei bekannter Position
Ist die Position bekannt, kann direkt über den Index darauf zugegriffen werden.
#### Zeitaufwand
$$ O(1) $$

### Iteration
> Die Iteration ist das Durchlaufen aller Listenelemente

#### Iteration bei Zugriff über Index
Der Zugriff über einen Index kostet konstante Zeit.
Bei einem Array der Größe $n$ ergibt sich für einen Zugriff auf die Indexpositionen $0$ bis $n-1$ daher ein Zeitaufwand von $O(n)$

#### Beispiel
```java
for (int i = 0; i < firstFreeIndex; i++) {
	System.out.println(A[i]);
}
```

## Java Klassen
### ArrayList
Die Java-Klasse ```ArrayList``` realisiert eine sequentielle List mit Inhalten beliebigen Types.
Die ```ArrayList``` basiert auf einem Array, welches nach bedarf beliebig vergrößert wird (d.h. es wird ein neues Array erstellt und alle Werte kopiert).

#### Beispiel
```Java
ArrayList<String> stringList = new ArrayList<>();
```
