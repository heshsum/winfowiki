# SQL Grundlagen

## Ergebnis
Das Ergebnis von Abfragen ist immer eine Tabelle.

## Tabellen erstellen
```sql
CREATE TABLE Tabellenname(
    nameColumn1 typeColumn1,
    nameColumn2 typeColumn2
);
```

## Schlüssel
Ans Ende des CREATE Statements lässt sich die Schlüsseldefinition hängen

### Primärschlüssel
```sql
CREATE TABLE Tabellenname(
    nameColumn1 typeColumn1,
    nameColumn2 typeColumn2,
    PRIMARY KEY(nameColumn1)
);
```

### Zusammengesetzter Schlüssel
```sql
CREATE TABLE Tabellenname(
    nameColumn1 typeColumn1,
    nameColumn2 typeColumn2,
    PRIMARY KEY(nameColumn1, nameColumn2)
);
```

### Fremdschlüssel
```sql
CREATE TABLE tableName1(
    nameColumn1 typeColumn1,
    nameColumn2 typeColumn2,
    FOREIGN KEY(nameColumn1) REFERENCES tableName2(nameColumn2)
);
```


## Tabellen Abfragen
### Einfache Abfrage
```sql
SELECT nameColumn1 FROM table;
```

### Abfrage mit WHERE-Bedingungen
```sql
SELECT *
FROM tableName
WHERE attributeName = attributeValue
;
```

### Abfrage mit HAVING-Bedingungen
Die Bedingung ```HAVING``` wird verwendet, wenn innerhalb einer ```WHERE``` Bedingung eine Aggregation erfolgen soll:

```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5
;
```

## Sortierung
```sql
SELECT attributeName
FROM tableNAME
ORDER BY attributeName ASC/DESC
;
```
## Gruppierung
```sql
SELECT attributeName1, attributeName2
FROM tableName
GROUP BY attributeName1
;
```

## Daten hinzufügen
```sql
INSERT INTO Tabellenname(column1, column2) VALUES
(wertColumn1, wertColumn2)
;
```

### Mehrere Zeilen gleichzeitig hinzufügen
```sql
INSERT INTO tableName(column1, column2) VALUES
(valueColumn1, valueColumn2),
(valueColumn1, valueColumn2)
;
```

## Daten aktualisieren
```sql
UPDATE tableName
SET attributeName = valueName
WHERE attributeName = value
;
```
