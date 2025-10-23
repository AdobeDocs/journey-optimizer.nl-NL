---
title: Bibliotheek met wiskundige functies
description: Bibliotheek met wiskundige functies
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 4%

---

# Wiskundige functies {#math}

Leer hoe te om functies Math in de verpersoonlijkingsredacteur te gebruiken.

## Absoluut {#absolute}

De functie `absolute` wordt gebruikt om een getal om te zetten in de absolute waarde ervan.

**Syntaxis**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

De functie `formatNumber` wordt gebruikt om een willekeurig getal op te maken in de taalgevoelige representatie.

Het accepteert een getal en een tekenreeks die de landinstelling vertegenwoordigen en retourneert een opgemaakte tekenreeks van het getal in de gewenste landinstelling.

**Syntaxis**

```sql
{%= formatNumber(number/double,string) %}: string
```

U kunt het formatteren en geldige scènes gebruiken zoals samengevat in [ documentatie van Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) en [ Gesteunde scènes ](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Voorbeeld**

Deze query retourneert een opgemaakte tekenreeks in het Arabisch die overeenkomt met 123456,789 als invoernummer.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Willekeurig {#random}

De functie `random` wordt gebruikt om een willekeurige waarde tussen 0 en 1 te retourneren.

**Syntaxis**

```sql
{%= random() %}: double
```

## Omlaag afronden {#round-down}

De functie `roundDown` wordt gebruikt om een getal omlaag te afronden.

**Syntaxis**

```sql
{%= roundDown(double) %}: double
```

## Omhoog afronden {#round-up}

De functie `roundUp` wordt gebruikt om een getal naar boven te afronden.

**Syntaxis**

```sql
{%= roundUp(double) %}: double
```

## Naar hexadecimale tekenreeks {#to-hex-string}

De functie `toHexString` zet om het even welk aantal in zijn hexadecimale koord om.

**Syntaxis**

```sql
{%= toHexString(number) %}: string
```

**Voorbeeld**

Deze query retourneert de hexadecimale waarde 158, d.w.z., 9e.

```sql
{%= toHexString(158) %}
```

## Naar int {#to-int}

De functie `toInt` wordt gebruikt om elk van deze typen (getal, double, int, long, float, short, byte, boolean, string) om te zetten in een geheel getal.

**Syntaxis**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Voorbeeld**

Deze query retourneert de gehele waarde 42.6, d.w.z. 42.

```sql
{%= toInt(42.6) %}: integer
```

## Naar percentage {#to-percentage}

De functie `toPercentage` wordt gebruikt om een getal om te zetten in een percentage.

**Syntaxis**

```sql
{%= toPercentage(double) %}: string
```

## Naar precisie {#to-precision}

De functie `toPrecision` wordt gebruikt om een getal om te zetten in de vereiste precisie.

**Syntaxis**

```sql
{%= toPrecision(double,int) %}: string
```

## Naar tekenreeks {#to-string}

De **toString** functie zet om het even welk aantal in zijn koordvertegenwoordiging.

**Syntaxis**

```sql
{%= toString(string) %}: string
```

**Voorbeeld**

Deze query retourneert &quot;12&quot;.

```sql
{%= toString(12) %} 
```
