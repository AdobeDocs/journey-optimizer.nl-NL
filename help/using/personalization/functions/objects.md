---
title: Functiebibliotheek
description: Functiebibliotheek
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 3%

---

# Objectfuncties {#objects}

![](../../assets/do-not-localize/badge.png)

## Is null{#isNull}

De functie `isNull` bepaalt of een objectverwijzing niet bestaat.

**Indeling**

```sql
{%= isNull(object) %}
```

**Voorbeeld**

De volgende verrichting controleert als het huisadres van de persoon niet bestaat.

```sql
{%= isNull(person.homeAddress) %}
```

## Is niet null{#isNotNull}

De functie `isNotNull` bepaalt of een objecten verwijzing bestaat.

**Indeling**

```sql
{%= isNotNull(object) %}
```

**Voorbeeld**

De volgende verrichting controleert als het huisadres van de persoon bestaat.

```sql
{%= isNotNull(person.homeAddress) %}
```
