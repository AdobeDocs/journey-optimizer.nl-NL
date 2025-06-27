---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-gegevens gebruiken (Beta)
description: Leer hoe te om de datasets van Adobe Experience Platform in  [!DNL Journey Optimizer]  Beslissing en verpersoonlijkingsmogelijkheden te gebruiken.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, editor
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: 416f82a932f0b484d8463ff24090a7061461822f
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Adobe Experience Platform-gegevens gebruiken {#aep-data}

>[!AVAILABILITY]
>
>Deze functie is momenteel beschikbaar voor alle klanten als een openbare bètaversie.
>
>Als u deze mogelijkheid wilt gebruiken, moet u eerst bètavoorwaarden accepteren voor uw organisatie.

Met Journey Optimizer kunt u gegevens van Adobe Experience Platform gebruiken in [!DNL Journey Optimizer] . Om dit te doen, moeten de datasets nodig voor raadplegingsverpersoonlijking eerst door een API vraag worden toegelaten zoals hieronder beschreven. Als u klaar bent, kunt u hun gegevens gebruiken met de mogelijkheden voor [!DNL Journey Optimizer] personalisatie en besluitvorming.

## Beperkingen en richtlijnen voor Beta {#guidelines}

Controleer voordat u begint de volgende beperkingen en richtlijnen:

* **grootte van de Dataset** is beperkt tot 5GB voor productiedatasets en 1GB voor dev zandbakdatasets
* **A maximum van 50 datasets kan** voor raadpleging per organisatie op elk ogenblik worden toegelaten.
* **Aantal verslagen** is beperkt tot 5M in productiedetecten en 1M in dev zandbakdatasets.
* **de Etikettering en de Handhaving van het Gebruik van Gegevens** wordt niet afgedwongen op dit ogenblik voor datasets die voor raadpleging worden toegelaten.
* **Datasets die voor raadpleging worden toegelaten en in verpersoonlijking worden gebruikt worden niet beschermd tegen schrapping**. Het is aan u om spoor te houden van welke datasets voor verpersoonlijking worden gebruikt om ervoor te zorgen zij niet worden geschrapt of worden verwijderd.

## Een dataset inschakelen voor gegevensopzoekhandeling {#enable}

Om gegevens van uw dataset voor verpersoonlijking te hefboomwerking, moet u een API vraag gebruiken om zijn status terug te winnen en de raadplegingsdienst toe te laten.

### Vereisten {#prerequisites-enable}

* Volg de richtingen die in [ worden gedetailleerd deze documentatie ](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) om uw milieu te vormen om API bevelen te verzenden.
* De API&#39;s van Adobe Journey Optimizer en Adobe Experience Platform moeten aan het project worden toegevoegd.

  ![](assets/aep-data-api.png)

* U moet de toestemming van datasets als deel van uw rol leiden.
* Het schema waarvoor de dataset gebaseerd is moet a **primaire identiteit** bevatten die als raadplegingssleutel kan dienst doen.

### API-oproepstructuur {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Waarbij:

* **URL** is `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **identiteitskaart van de Dataset** is de dataset waarvoor u wenst om toe te laten.
* **de Actie** laat OF onbruikbaar maakt toe.
* **het teken van de Toegang** kan van de ontwikkelaarsconsole worden teruggewonnen.
* **API sleutel** kan van de ontwikkelaarsconsole worden teruggewonnen.
* **IMS Org ID** is uw organisatie van Adobe.
* **Naam Sandbox** is de zandbaknaam de dataset in (d.w.z. prod, dev enz.) is.

>[!NOTE]
>
>Als u de hieronder weergegeven fout tegenkomt bij het proberen van een API-aanroep om gegevenssets in te schakelen, probeert u de Adobe Journey Optimizer API&#39;s uit uw project voor de ontwikkelaarsconsole te verwijderen en deze vervolgens opnieuw toe te voegen.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

Zodra een dataset voor raadpleging gebruikend een API vraag is toegelaten, kunt u zijn gegevens met [!DNL Journey Optimizer] verpersoonlijking en Beslissingsmogelijkheden gebruiken.

* [Adobe Experience Platform-gegevens gebruiken voor personalisatie](../personalization/aep-data-perso.md)
* [Adobe Experience Platform-gegevens gebruiken voor beslissingen](../experience-decisioning/aep-data-exd.md)
