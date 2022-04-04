---
title: Lijst van gewenste personen
description: Leer hoe u de lijst van gewenste personen gebruikt.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: e1a9ac4a13f82312233fe4a34d06046b67c026dc
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 1%

---

# Lijst van gewenste personen {#allow-list}

Het is mogelijk om een specifieke verzendende-veilige lijst bij te bepalen [sandbox](../administration/sandboxes.md) niveau, om een veilige omgeving voor testdoeleinden te hebben.

Bijvoorbeeld, op een non-production instantie, waar de fouten kunnen voorkomen, verzekert de lijst van gewenste personen u geen risico om ongewenste berichten naar uw klanten te verzenden.

>[!NOTE]
>
>Deze functie is nu beschikbaar voor productie- en niet-productie-sandboxen.

Met de lijst van gewenste personen kunt u afzonderlijke e-mailadressen of domeinen opgeven die de enige ontvangers of domeinen zijn die geautoriseerd zijn om de e-mails te ontvangen die u vanuit een specifieke sandbox verzendt. Dit kan voorkomen dat u per ongeluk e-mailberichten naar de adressen van de echte klant stuurt wanneer u zich in een testomgeving bevindt.

>[!CAUTION]
>
>Deze functie is alleen van toepassing op het e-mailkanaal.

## De lijst van gewenste personen inschakelen {#enable-allow-list}

<!--To enable the allowed list on a non-production sandbox, you need to update the general settings using the corresponding API end point in the Message Presets Service. Using this API, you can also disable the feature at any time.

You can update the allowed list before or after enabling the feature.-->

Volg onderstaande stappen om de lijst van gewenste personen in te schakelen.

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]**.

   ![](assets/allow-list-access.png)

1. Klik op **[!UICONTROL Edit]**.

   ![](assets/allow-list-edit.png)

1. Selecteer **[!UICONTROL Enable allow list]**.

   ![](assets/allow-list-enable.png)

1. Klik op **[!UICONTROL Save]**. De lijst van gewenste personen is ingeschakeld.

   ![](assets/allow-list-enabled.png)

De logica lijst van gewenste personen wordt toegepast wanneer de functie is ingeschakeld **en** als de lijst van gewenste personen **niet** leeg. Meer informatie in [deze sectie](#logic).

>[!NOTE]
>
>Als deze optie is ingeschakeld, wordt de functie lijst van gewenste personen gerespecteerd bij het uitvoeren van reizen, maar ook bij het testen van berichten met [proefdrukken](../design/preview.md#send-proofs) en het testen van reizen met behulp van de [testmodus](../building-journeys/testing-the-journey.md).

## Entiteiten toevoegen aan de lijst van gewenste personen {#add-entities}

Als u nieuwe e-mailadressen of domeinen wilt toevoegen aan de lijst van gewenste personen voor een specifieke sandbox, moet u de API voor onderdrukking aanroepen met de `ALLOWED` waarde voor de `listType` kenmerk. Bijvoorbeeld:

![](assets/allow-list-api.png)

U kunt de opdracht **Toevoegen**, **Verwijderen** en **Get** bewerkingen.

>[!NOTE]
>
>De lijst van gewenste personen kan maximaal 1.000 items bevatten.

Meer informatie over het maken van API-aanroepen in het dialoogvenster [Adobe Experience Platform API&#39;s](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target=&quot;_blank&quot;} naslagdocumentatie.

## Lijst van gewenste personen-logica {#logic}

Wanneer de lijst van gewenste personen **leeg**, wordt de logica van de lijst van gewenste personen niet toegepast. Dit betekent dat u e-mailberichten naar alle profielen kunt verzenden, mits deze zich niet op de [onderdrukkingslijst](suppression-list.md).

Wanneer de lijst van gewenste personen **niet leeg**, wordt de logica van de lijst van gewenste personen toegepast:

* Indien een entiteit **niet op de lijst van gewenste personen**, en niet op de onderdrukkingslijst, zal de overeenkomstige ontvanger niet de e-mail ontvangen, omdat **[!UICONTROL Not allowed]**.

* Indien een entiteit **op de lijst van gewenste personen** en niet in de suppressielijst, kan de e-mail naar de desbetreffende ontvanger worden verzonden. Indien de entiteit zich echter ook op de [onderdrukkingslijst](suppression-list.md), de overeenkomstige ontvanger de e-mail niet zal ontvangen omdat **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>De profielen met **[!UICONTROL Not allowed]** status worden uitgesloten tijdens het verzenden van berichten. Daarom moet **Reisrapporten** geeft aan dat deze profielen door de reis zijn gegaan ([Segment lezen](../building-journeys/read-segment.md) en [Bericht](../building-journeys/journeys-message.md) de **E-mailrapporten** worden niet opgenomen in de **[!UICONTROL Sent]** Metrische gegevens worden uitgefilterd voordat e-mail wordt verzonden.
>
>Meer informatie over de [Live rapport](../reports/live-report.md) en [Algemeen rapport](../reports/global-report.md).

## Uitsluitingsrapportage {#reporting}

Wanneer deze functie is ingeschakeld in een niet-productiesandbox, kunt u e-mailadressen of domeinen ophalen die zijn uitgesloten van een verzendende server omdat deze zich niet op de lijst van gewenste personen bevonden. Om dit te doen, kunt u gebruiken [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} om de API-aanroepen hieronder uit te voeren.

Om de **aantal e-mails** die niet werden verzonden omdat de ontvangers niet op de lijst van gewenste personen waren, gebruik de volgende vraag:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Om de **lijst met e-mailadressen** die niet werden verzonden omdat de ontvangers niet op de lijst van gewenste personen waren, gebruik de volgende vraag:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
