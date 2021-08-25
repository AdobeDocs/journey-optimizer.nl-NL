---
title: Lijst van gewenste personen
description: Leer hoe u de lijst van gewenste personen gebruikt.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# Lijst van gewenste personen {#allow-list}

Het is nu mogelijk om een specifieke het verzenden-veilige lijst op het [zandbak](administration/sandboxes.md) niveau te bepalen, om een veilige milieu voor testend doel te hebben. Op een niet-productiegeval, waar de fouten kunnen voorkomen, verzekert de lijst van gewenste personen u geen risico om ongewenste berichten naar uw klanten te verzenden.

Met de lijst van gewenste personen kunt u afzonderlijke e-mailadressen of domeinen opgeven die de enige ontvangers of domeinen zijn die geautoriseerd zijn om de e-mails te ontvangen die u vanuit een specifieke sandbox verzendt. Dit kan voorkomen dat u per ongeluk e-mailberichten naar de adressen van de echte klant stuurt wanneer u zich in een testomgeving bevindt.

>[!CAUTION]
>
>Deze functie is **niet** beschikbaar op productiestanddozen. Deze is alleen van toepassing op het e-mailkanaal.

## De lijst van gewenste personen inschakelen {#enable-allow-list}

Om de lijst van gewenste personen op een niet productiesandbox toe te laten, moet u de algemene montages bijwerken gebruikend het overeenkomstige API eindpunt in de Vooraf ingestelde Dienst van het Bericht.

* Met deze API kunt u de functie ook op elk gewenst moment uitschakelen.

* U kunt de lijst van gewenste personen bijwerken voor of na het inschakelen van de functie.

* De logica van de lijst van gewenste personen is van toepassing wanneer de functie **en** wordt ingeschakeld als de lijst van gewenste personen **not** leeg is. Meer informatie vindt u in [deze sectie](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>Als deze optie is ingeschakeld, wordt de functie lijst van gewenste personen gerespecteerd bij het uitvoeren van reizen, maar ook bij het testen van berichten met [proefdrukken](preview.md#send-proofs) en het testen van reizen met de [testmodus](building-journeys/testing-the-journey.md).

## Entiteiten toevoegen aan de lijst van gewenste personen {#add-entities}

Als u nieuwe e-mailadressen of domeinen wilt toevoegen aan de lijst van gewenste personen voor een specifieke sandbox, moet u de API voor onderdrukking aanroepen met de waarde `ALLOWED` voor het kenmerk `listType`. Bijvoorbeeld:

![](assets/allow-list-api.png)

U kunt de bewerkingen **Add**, **Delete** en **Get** uitvoeren.

>[!NOTE]
>
>De lijst van gewenste personen kan maximaal 1.000 items bevatten.

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Lijst van gewenste personen-logica {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Wanneer de lijst van gewenste personen **empty** is, wordt de logica van de lijst van gewenste personen niet toegepast. Dit betekent dat u e-mailberichten naar profielen kunt verzenden, op voorwaarde dat deze niet voorkomen in de [suppressielijst](suppression-list.md).

Wanneer de lijst van gewenste personen **niet leeg** is, wordt de logica van de lijst van gewenste personen toegepast:

* Als een entiteit **niet op de lijst van gewenste personen**, en niet op de onderdrukkingslijst is, zal de overeenkomstige ontvanger niet de e-mail ontvangen, de reden is **[!UICONTROL Not allowed]**.

* Als een entiteit **op de lijst van gewenste personen**, en niet op de onderdrukkingslijst is, kan e-mail naar de overeenkomstige ontvanger worden verzonden. Als de entiteit zich echter ook op de [suppressielijst](suppression-list.md) bevindt, zal de overeenkomstige ontvanger de e-mail niet ontvangen, omdat **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>De profielen met de status **[!UICONTROL Not allowed]** worden uitgesloten tijdens het verzenden van berichten. Daarom, terwijl **Reis rapporteert** deze profielen zal tonen als die door de reis ([Leessegment](building-journeys/read-segment.md) en [Bericht](building-journeys/journeys-message.md) activiteiten) zijn bewogen, **E-mailrapporten** zullen niet hen in **[!UICONTROL Sent]** metriek omvatten aangezien zij voorafgaand aan e-mail verzenden worden gefilterd.
>
>Leer meer op [Levend Rapport](reports/live-report.md) en [Globaal Rapport](reports/global-report.md).

## Uitsluitingsrapportage {#reporting}

Wanneer deze functie is ingeschakeld in een niet-productiesandbox, kunt u e-mailadressen of domeinen ophalen die zijn uitgesloten van een verzendende server omdat deze zich niet op de lijst van gewenste personen bevonden. Om dit te doen, kunt u [de Dienst van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html) {target= &quot;_blank&quot;} gebruiken om de API hieronder vraag te maken.

Als u het **aantal e-mails** wilt ophalen dat niet is verzonden omdat de ontvangers zich niet op de lijst van gewenste personen bevonden, gebruikt u de volgende query:

```
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Als u de **lijst met e-mailadressen** wilt ophalen die niet zijn verzonden omdat de ontvangers zich niet op de lijst van gewenste personen bevonden, gebruikt u de volgende query:

```
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

