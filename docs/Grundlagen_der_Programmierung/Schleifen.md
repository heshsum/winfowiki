# Schleifen und Anweisungen

## if-Anweisung
Mit einer if-Anweisung können Operationen unter bestimmten Bedingungen ausgeführt werden.

```java
if(1 > 0) {
    System.out.println("Zahl ist größer als 0.");
} else if (i < 0) {
    System.out.println("Zahl ist kleiner als 0.");
} else {
    System.out.println("Zahl ist 0.");
}
```

## for-Loop
```java
for (int i=0; i<j; i++) {
    System.out.println("i = ", i);
}
```

## for-each Loop
```java
int[] zahlen = {1, 5, 12, -2};
    
for (int zahl : zahlen) {
    System.out.println("Die aktuelle Zahl lautet: " + zahl);
}
```


## while-Loop
```java
int i = 0;
int j = 5;

while(i < j) {
    System.out.println("Die aktuelle Zahl lautet: " + i);
    i++;
}
```