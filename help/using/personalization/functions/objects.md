---
title: Objectfunctiebibliotheek
description: Objectfunctiebibliotheek
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

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
