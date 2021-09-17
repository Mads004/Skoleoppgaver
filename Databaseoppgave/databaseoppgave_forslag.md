# Dokumentasjon Databaseoppgave 

## Oppgave 2

A.
Denne koden Viser hvilke jenter som går i klassen.

```sql
Select 'Fornavn', 'Etternavn' From 'Elev' WHERE 'Kjonn' = 'J';
```

___

B. 
Denne koden viser guttene i klasse 2.

```sql
SELECT 'Fornavn', 'Etternavn' FROM 'Elev' WHERE 'Kjonn' = 'G' And Klasse = '2'
```

___

C. 
Denne koden viser hvor mange jenter det er i klasse 2

```sql
SELECT COUNT('Kjonn') FROM 'Elev' WHERE 'Kjonn' = 'J' AND 'Klasse' = '2'
```

___

D. Denne koden finner alle Elevene som begynner på J.

```sql
SELECT 'Fornavn', 'Etternavn' FROM 'Elev' WHERE 'Fornavn' LIKE 'J%'
```

___

E. 
Denne koden finner alle elevene som har Fornavn som begynner på M og går i Klasse 2.
```sql
SELECT 'Fornavn', 'Etternavn', 'Klasse' FROM 'Elev' WHERE 'Fornavn' LIKE 'M%' AND 'Klasse' = '2'
```

___

F. 
Denne koden finner alle Elevene som har hobby fotball. 

```sql
SELECT 'Fornavn', 'Etternavn', 'Hobby' FROM 'Elev' WHERE 'Hobby' = 'Fotball';
```

___
## Oppgave 4

Denne koden legger til datamaskin i elev databasen
```sql
UPDATE `Elev` SET `Datamaskin`= '1' WHERE `ElevID`='1' OR `ElevID`='4' OR `ElevID`='8';
```

___


## OPPGAVE 5

```SQL
ALTER TABLE 'Elev' ADD FOREIGN KEY 'Datamaskin' REFERENCES 'Datamaskin' ('DatamaskinID')
```

___

## Oppgave 6
Denne koden vil sortere elevene etter forbokstav

```sql
SELECT * FROM `Elev` ORDER BY `Elev`.`Fornavn` ASC
```

___

## Oppgave 7

```sql
SELECT Klasse, COUNT(Kjonn) FROM elev GROUP BY Klasse HAVING COUNT(Kjonn) >= 2 ORDER BY Klasse ASC

```

___

## Oppgave 8

Denne koden vil oppdatere hobbyen til 'Thomas' til Golf

```sql
UPDATE 'Elev'
SET 'Hobby' = 'Golf'
WHERE 'ElevID' = 1;
```

___

## Oppgave 9

Denne koden vil legge til en ny elev i klassen

```sql
INSERT INTO 'Elev' ('Fornavn', 'Etternavn', 'Klasse', 'Hobby', 'Kjonn', 'Datamaskin')
VALUES ('Jens', 'Skagen', '2', 'Fotball', 'G', '3');
```

___

## Oppgave 10

Denne koden vil slette Jesn fra databasen

```sql 
DELETE FROM 'Elev' WHERE 'Fornavn'='Jens';
```

## Bra jobbet, Theodor. Vakker dokumentasjon med Markdown. Alle svarene er riktige. 
