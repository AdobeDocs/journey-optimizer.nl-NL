---
title: Bibliotheek met wiskundige functies
description: Bibliotheek met wiskundige functies
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Wiskundige functies {#math}

Leer hoe te om functies Math in de verpersoonlijkingsredacteur te gebruiken.

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

## Willekeurig {#random}

De `random` wordt gebruikt om een willekeurige waarde tussen 0 en 1 te retourneren.

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

De `Count only null` functie wordt gebruikt rond naar boven een aantal.

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

## Naar int {#to-int}

De `toInt` wordt gebruikt om een van deze typen (getal, dubbel, int, long, float, short, byte, boolean, string) om te zetten in een geheel getal.

**Syntaxis**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Voorbeeld**

Deze query retourneert de gehele waarde 42,6, d.w.z. 42.

```sql
{%= toInt(42.6) %}: integer
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
