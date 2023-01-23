# Methoden
Methoden in Java sind Code-Blöcke, die nach einem Aufruf ausgeführt werden.  
Die Kombination aus *Scope*, *Name*, *Rückgabewert* und *Parameter* nennt man **Signatur**.


Beispiel:
```java
public void printToString(String s) {
    System.out.println(s);
}
```

## Die main-Methode
Die main-Methode ist der Einstiegspunkt für ein Java-Programm. Wird ein Java-Programm ausgeführt, wird also zunächst die main-Methode aufgerufen.  
Der Code in der main-Methode wird daher auch direkt nach Start des Programms ausgeführt.  

Die main-Methode hat immer dieselbe Signatur. Beispiel:
```java
public static void main(String args[]) {
    do something;
}
```

## Scope
Der Scope einer Methode gibt an, von wo aus auf eine Methode zugegriffen werden kann.

| Modifier    | Class | Package | Subclass | Global |
| ----------- | ----- | ------- | -------- | ------ |
| public      | Y     | Y       | Y        | Y      |
| protected   | Y     | Y       | Y        | N      |
| no modifier | Y     | Y       | N        | N      |
| private     | Y     | N       | N        | N      |

[Offizielle Dokumentation](https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)

## Name
Der Methodenname ist nichts anderes als eine Bezeichnung für eine Methode.  
Man kann - mit ein paar Ausnahmen wie etwa main() - beliebige Namen für die eigenen Methoden nutzen.

Hier gleiche Beispielmethoden mit unterschiedlichen Namen:
```java
public void foo() {
    do something();
}

public void bar() {
    do something();
}
```

## Rückgabewert
Teil der Signatur einer Methode ist der Rückgabewert. So ist klar, ob oder was für einen Datentyp eine Methode zurückgibt.  
Rückgabewerte können beliebige primitive Datentypen oder auch Objekte sein - oder im Falle von ```void``` einfach nichts.

```java
public boolean greaterZero(int i) {
    if (i > 0) {
        return true;
    }
    return false;
}
```

## Parameter
Mit Hilfe von Parametern (im Beispiel ```String s```) können Objekte oder andere Informationen an eine Methode übergeben werden.

```java
public boolean printSomething(String s) {
    System.out.println(s);
}
```

## Methoden überladen
Man kann mehrere Varianten einer Methode erstellen, die denselben Namen tragen aber bspw. verschiedene Parameter nutzen.  
Dies kann hilfreich sein, etwa wenn man ein Auto-Objekt mal nur mit Hersteller und Modell (```String manufacturer, String model```) anlegen und mal das Jahr (```String manufacturer, String model, int year```) mitgeben will.

```java
public Car(String manufacturer, String model) {
    this.manufacturer = manufacturer;
    this.model = model;
}

public Car(String manufacturer, String model, int year) {
    this.manufacturer = manufacturer;
    this.model = model;
    this.year = year;
}
```
