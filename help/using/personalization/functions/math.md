---
title: Bibliotheek met wiskundige functies
description: Bibliotheek met wiskundige functies
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: dc313d7cbee9e412b9294b644fddbc7840f90339
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# Wiskundige functies {#math}

Leer hoe te om functies Math in de redacteur van de Uitdrukking te gebruiken.

## Absoluut {#absolute}

De `absolute` functie wordt gebruikt om een getal om te zetten is absolute waarde.

**Syntaxis**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

De `formatNumber` wordt gebruikt om een aantal in zijn taal-gevoelige vertegenwoordiging te formatteren.

Het accepteert een getal en een tekenreeks die de landinstelling vertegenwoordigen en retourneert een opgemaakte tekenreeks van het getal in de gewenste landinstelling.

**Syntaxis**

```sql
{%= formatNumber(number/double,string) %}: string
```

U kunt opmaak en geldige landinstellingen gebruiken, zoals in [Documentatie oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) en [Ondersteunde landinstellingen](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Voorbeeld**

Deze query retourneert een opgemaakte tekenreeks in het Arabisch die overeenkomt met 123456,789 als invoernummer.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

De `random` Deze functie wordt gebruikt om een willekeurige waarde tussen 0 en 1 te retourneren.

**Syntaxis**

```sql
{%= random() %}: double
```

## Omlaag afronden {#round-down}

De `roundDown` Deze functie wordt gebruikt om een getal omlaag te afronden.

**Syntaxis**

```sql
{%= roundDown(double) %}: double
```

## Omhoog afronden {#round-up}

De `Count only null` Deze functie wordt een getal naar boven afgerond.

**Syntaxis**

```sql
{%= roundUp(double) %}: double
```

## Naar hexadecimale tekenreeks {#to-hex-string}

De `toHexString` functie converteert een getal naar de hexadecimale tekenreeks.

**Syntaxis**

```sql
{%= toHexString(number) %}: string
```

**Voorbeeld**

Deze query retourneert de hexadecimale waarde 158 i.e 9e.

```sql
{%= toHexString(158) %}
```

## Naar percentage {#to-percentage}

De `toPercentage` wordt gebruikt om een getal om te zetten in een percentage.

**Syntaxis**

```sql
{%= toPercentage(double) %}: string
```

## Naar precisie {#to-precision}

De `toPrecision` wordt gebruikt om een getal om te zetten in de vereiste precisie.

**Syntaxis**

```sql
{%= toPrecision(double,int) %}: string
```

## Naar tekenreeks {#to-string}

De **toString** functie converteert een willekeurig getal naar de tekenreeksrepresentatie.

**Syntaxis**

```sql
{%= toString(string) %}: string
```

**Voorbeeld**

Deze query retourneert &quot;12&quot;.

```sql
{%= toString(12) %} 
```
