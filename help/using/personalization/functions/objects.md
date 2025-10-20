---
title: Objectfunctiebibliotheek
description: Objectfunctiebibliotheek
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 3%

---

# Objectfuncties {#objects}

## Is null{#isNull}

De functie `isNull` bepaalt of een objectverwijzing niet bestaat.

**Syntaxis**

```sql
{%= isNull(object) %}
```

**Voorbeeld**

De volgende verrichting controleert als het huisadres van de persoon niet bestaat.

```sql
{%= isNull(person.homeAddress) %}
```

## Is niet null{#isNotNull}

De functie `isNotNull` bepaalt of een objectverwijzing bestaat.

**Syntaxis**

```sql
{%= isNotNull(object) %}
```

**Voorbeeld**

De volgende verrichting controleert als het huisadres van de persoon bestaat.

```sql
{%= isNotNull(person.homeAddress) %}
```
