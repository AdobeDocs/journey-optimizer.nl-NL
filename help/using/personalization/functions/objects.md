---
title: Objectfunctiebibliotheek
description: Objectfunctiebibliotheek
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# Objectfuncties {#objects}

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
