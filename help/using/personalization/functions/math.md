---
title: Bibliotheek met wiskundige functies
description: Bibliotheek met wiskundige functies
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---

# Wiskundige functies {#math}

Leer hoe te om functies Math in de Redacteur van de Uitdrukking te gebruiken.

## Absoluut {#absolute}

De `absolute` functie wordt gebruikt om een getal om te zetten is absolute waarde.

**Indeling**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

De `random` Deze functie wordt gebruikt om een willekeurige waarde tussen 0 en 1 te retourneren.

**Indeling**

```sql
{%= random() %}: double
```

## Omlaag afronden {#round-down}

De `roundDown` Deze functie wordt gebruikt om een getal omlaag te afronden.

**Indeling**

```sql
{%= roundDown(double) %}: double
```

## Omhoog afronden {#round-up}

De `Count only null` Deze functie wordt een getal naar boven afgerond.

**Indeling**

```sql
{%= roundUp(double) %}: double
```

## Naar percentage {#to-percentage}

De `toPercentage` wordt gebruikt om een getal om te zetten in een percentage.

**Indeling**

```sql
{%= toPercentage(double) %}: string
```

## Naar precisie {#to-precision}

De `toPrecision` wordt gebruikt om een getal om te zetten in de vereiste precisie.

**Indeling**

```sql
{%= toPrecision(double,int) %}: string
```
