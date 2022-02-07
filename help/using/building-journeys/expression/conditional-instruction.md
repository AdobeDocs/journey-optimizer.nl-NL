---
product: adobe campaign
title: Voorwaardelijke instructie (indien, then, else)
description: Meer informatie over voorwaardelijke instructies
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
source-git-commit: 7588a675319324e43bbc61a71b1fdfaab9cce93a
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Voorwaardelijke instructie (indien, then, else) {#conditional-instruction}

De voorwaardelijke instructie (als vervolgens anders) wordt ondersteund in de geavanceerde editor. Hiermee kunnen complexere expressies worden gedefinieerd. Het bestaat uit de volgende elementen:

* **[!UICONTROL if]**: de eerst te beoordelen voorwaarde.
* **[!UICONTROL then]**: de expressie die moet worden geëvalueerd als het resultaat van de evaluatie van de voorwaarde waar is.
* **[!UICONTROL else]**: de expressie die moet worden geëvalueerd als het resultaat van de evaluatie van de voorwaarde onwaar is.

>[!NOTE]
>
>Haakjes zijn vereist voor alle expressies.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` moet een **boolean**.

`<expression2>` en `<expression3>` moeten hetzelfde type of compatibele typen hebben. De ondersteunde handtekeningen en geretourneerde typen zijn:

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Gebruik**

Met de voorwaardelijke instructie kunt u de workflow van de reis optimaliseren door het aantal conditieactiviteiten te verminderen. Binnen dezelfde actieactiviteit kunt u bijvoorbeeld twee alternatieven voor een velddefinitie opgeven met slechts één voorwaarde-expressie.

Voorbeeld voor een actieactiviteit (voor een gebied dat een koord als resultaat van de voorwaardelijke instructie verwacht):

```json
if (startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
