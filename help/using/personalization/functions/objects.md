---
title: Objectfunctiebibliotheek
description: Objectfunctiebibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 3%

---

# Objectfuncties {#objects}

## Is null{#isNull}

De `isNull` Deze functie bepaalt of een objectverwijzing niet bestaat.

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

De `isNotNull` Deze functie bepaalt of er een objectverwijzing bestaat.

**Indeling**

```sql
{%= isNotNull(object) %}
```

**Voorbeeld**

De volgende verrichting controleert als het huisadres van de persoon bestaat.

```sql
{%= isNotNull(person.homeAddress) %}
```