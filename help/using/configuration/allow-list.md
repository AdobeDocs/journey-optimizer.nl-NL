---
solution: Journey Optimizer
product: journey optimizer
title: Een lijst van gewenste personen instellen
description: Leer hoe u een lijst van gewenste personen in Journey Optimizer instelt en beheert om het verzenden van e-mail te beperken tot vertrouwde adressen en domeinen op sandboxniveau.
feature: Deliverability
role: Admin
level: Intermediate
keywords: lijst van gewenste personen, veilige lijst, e-mail, leverbaarbaarheid, sandbox, domeinen, onderdrukking, configuratie
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 56d0d176385dfbb74222fd33115c01553f50d107
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 2%

---

# Een lijst van gewenste personen instellen {#allow-list}

De lijst van gewenste personen is een het verzenden-veilige lijst u op het [ zandbak ](../administration/sandboxes.md) niveau kunt bepalen. Het beperkt het verzenden van e-mail naar specifieke adressen of domeinen, die ervoor zorgen dat slechts uitdrukkelijk vermelde ontvangers berichten van een bepaalde zandbak kunnen ontvangen.

>[!CAUTION]
>
>Deze functie geldt alleen voor het e-mailkanaal. Het is beschikbaar voor productie- en niet-productie-sandboxen.

Op niet-productiesandboxen, waar het onbedoelde verzenden kan voorkomen, verhindert de lijst van gewenste personen ongewenste berichten echte klantenadressen te bereiken, die een veilig milieu voor testende doeleinden verstrekken.

Wanneer de lijst van gewenste personen actief maar leeg is, worden geen e-mails verzonden. Dit maakt het een nuttige noodrem: als een kritiek probleem zich voordoet, kunt u een lege lijst van gewenste personen activeren om alle uitgaande communicatie vanuit [!DNL Journey Optimizer] te stoppen totdat het probleem is opgelost. Leer meer over de [ logica van de lijst van gewenste personen ](#logic).

U kunt Journey Optimizer ook gebruiken **REST API van de Onderdrukking** om uitgaande berichten programmatically door onderdrukking en lijsten van gewenste personen te beheren. [ Leer hoe te met de HULPMIDDEL te werken REST API ](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## Toegang tot de lijst van gewenste personen {#access-allowed-list}

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** en selecteer **[!UICONTROL Allowed list]** om de gedetailleerde lijst met toegestane e-mailadressen en domeinen te openen.

![ pagina die van de Lijst van gewenste personen de lijst van toegestane e-mailadressen en domeinen ](assets/allow-list-access.png) toont

>[!CAUTION]
>
>De toestemmingen om de lijst van gewenste personen te bekijken, uit te voeren en te leiden zijn beperkt tot [ Beheerders van de Reis ](../administration/ootb-product-profiles.md#journey-administrator). Leer meer over het beheren van [!DNL Journey Optimizer] de toegangsrechten van gebruikers in [ deze sectie ](../administration/permissions-overview.md).

Selecteer de knop **[!UICONTROL Download CSV]** als u de lijst van gewenste personen als een CSV-bestand wilt exporteren.

Gebruik de knop **[!UICONTROL Delete]** om een item permanent te verwijderen.

U kunt zoeken op de e-mailadressen of -domeinen en filteren op de **[!UICONTROL Address type]** . Als deze optie is geselecteerd, kunt u het filter wissen dat boven op de lijst wordt weergegeven.

![ Lijst van gewenste personen die door adrestype ](assets/allowed-list-filtering-example.png) wordt gefiltreerd

## De lijst van gewenste personen activeren {#enable-allow-list}

Volg onderstaande stappen om de lijst van gewenste personen te activeren.

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]**.

1. Selecteer de schakelknop.

   ![ knoop van de knevel om de lijst van gewenste personen te activeren ](assets/allow-list-edit.png)

1. Selecteer **[!UICONTROL Activate allowed list]**. De lijst van gewenste personen is nu actief.

   ![ Bevestiging dat de lijst van gewenste personen nu actief is ](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Nadat u de lijst van gewenste personen hebt geactiveerd, duurt het 10 minuten voordat deze tijdens uw reizen en campagnes van kracht wordt. Ook het bijwerken van de lijst met lijsten van gewenste personen en onderdrukking kan 10 minuten duren.

De logica lijst van gewenste personen is van toepassing wanneer de functie actief is. Lees meer in [deze sectie](#logic).

>[!NOTE]
>
>Wanneer geactiveerd, wordt de eigenschap van de lijst van gewenste personen geëerd wanneer het uitvoeren van reizen, maar ook wanneer het testen van berichten met [ proeven ](../content-management/proofs.md) en het testen reizen gebruikend de [ testwijze ](../building-journeys/testing-the-journey.md).

## De lijst van gewenste personen deactiveren {#deactivate-allow-list}

Volg onderstaande stappen om de lijst van gewenste personen te deactiveren.

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]**.

1. Selecteer de schakelknop.

   ![ knoop van de knevel om de lijst van gewenste personen ](assets/allow-list-edit-active.png) te deactiveren

1. Selecteer **[!UICONTROL Deactivate allowed list]**. De lijst van gewenste personen is niet meer actief.

   ![ Bevestiging dat de lijst van gewenste personen nu inactief is ](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Nadat u de lijst van gewenste personen hebt gedeactiveerd, is er een vertraging van 10 minuten voordat deze van kracht wordt tijdens uw reizen en campagnes. Ook het bijwerken van de lijst met lijsten van gewenste personen en onderdrukking kan 10 minuten duren.

De logica lijst van gewenste personen is niet van toepassing wanneer de functie wordt gedeactiveerd. Lees meer in [deze sectie](#logic).

## Entiteiten toevoegen aan de lijst van gewenste personen {#add-entities}

Om nieuwe e-mailadressen of domeinen aan de lijst van gewenste personen voor een specifieke zandbak toe te voegen, kunt u of [ manueel de lijst ](#manually-populate-list) bevolken, of een [ API vraag ](#api-call-allowed-list) gebruiken.

>[!NOTE]
>
>De lijst van gewenste personen kan maximaal 1.000 items bevatten.

### De lijst van gewenste personen handmatig vullen {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="Voeg adressen of domeinen aan de lijst van gewenste personen toe"
>abstract="U kunt handmatig nieuwe e-mailadressen of domeinen aan de lijst van gewenste personen toevoegen door deze een voor een te selecteren."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="Voeg adressen of domeinen aan de lijst van gewenste personen toe"
>abstract="U kunt handmatig nieuwe e-mailadressen of domeinen aan de lijst van gewenste personen toevoegen door deze een voor een te selecteren."

U kunt de lijst van gewenste personen [!DNL Journey Optimizer] handmatig vullen door een e-mailadres of een domein toe te voegen via de gebruikersinterface.

>[!NOTE]
>
>U kunt slechts één e-mailadres of domein tegelijk toevoegen.

Volg de onderstaande stappen om dit te doen.

1. Selecteer de knop **[!UICONTROL Add email or domain]**.

   ![ voeg e-mail of domeinknoop op de pagina van de lijst van gewenste personen toe ](assets/allowed-list-add-email.png)

1. Kies het adrestype: **[!UICONTROL Email address]** of **[!UICONTROL Domain address]**.

1. Voer het e-mailadres of domein in waarnaar u e-mails wilt verzenden.

   >[!NOTE]
   >
   >Controleer of u een geldig e-mailadres (zoals abc@company.com) of domein (zoals abc.company.com) invoert.

1. Geef indien nodig een reden op.

   ![ Vorm om een e-mailadres of domein aan de lijst van gewenste personen, met een facultatief redengebied ](assets/allowed-list-add-email-address.png) toe te voegen

   >[!NOTE]
   >
   >Alle ASCII-tekens in het bereik 32 tot en met 126 zijn toegestaan in het veld **[!UICONTROL Reason]** . De volledige lijst kan op [ worden gevonden deze pagina ](https://en.wikipedia.org/wiki/ASCII#Printable_characters){target="_blank"} bijvoorbeeld.

1. Klik op **[!UICONTROL Submit]**.

### Entiteiten toevoegen met een API-aanroep {#api-call-allowed-list}

Als u de lijst van gewenste personen wilt vullen, kunt u de API voor onderdrukking ook aanroepen met de `ALLOWED` -waarde voor het `listType` -kenmerk. Bijvoorbeeld:

![ Voorbeeld API vraag om een ingang aan de lijst van gewenste personen toe te voegen gebruikend de onderdrukking API ](assets/allow-list-api.png)

U kunt **uitvoeren voeg** toe, **schrapt** en **krijgt** verrichtingen.

Leer meer over het maken van API vraag in [ Adobe Experience Platform APIs ](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} verwijzingsdocumentatie.

## De lijst van gewenste personen downloaden {#download-allowed-list}

Voer de volgende stappen uit om de lijst van gewenste personen als een CSV-bestand te exporteren:

1. Selecteer de knop **[!UICONTROL Download CSV]**.

   ![ download CSV knoop op de pagina van de lijst van gewenste personen ](assets/allowed-list-download-csv.png)

1. Wacht tot het bestand is gegenereerd.

   ![ Bericht die op het CSV- dossier wijzen wordt geproduceerd ](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >De downloadtijd is afhankelijk van de bestandsgrootte. Dit betekent het aantal adressen in de lijst van gewenste personen.
   >
   >Voor een bepaalde sandbox kan één downloadverzoek tegelijkertijd worden verwerkt.

1. Nadat het bestand is gegenereerd, ontvangt u een melding. Klik op het belpictogram rechtsboven op het scherm om het scherm weer te geven.

1. Klik op de melding zelf om het bestand te downloaden.

   ![ Bericht met een downloadverbinding voor het geproduceerde Csv- dossier ](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >De koppeling is 24 uur geldig.

## Lijst van gewenste personen-logica {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="De lijst van gewenste personen beheren"
>abstract="Wanneer de lijst van gewenste personen wordt geactiveerd, ontvangen alleen de ontvangers die zijn opgenomen in de lijst van gewenste personen e-mailberichten van deze sandbox. Wanneer deze functie is gedeactiveerd, ontvangen alle ontvangers e-mailberichten."

Wanneer de lijst van gewenste personen [ actief ](#enable-allow-list) is, is de volgende logica van toepassing:

* Als de lijst van gewenste personen **** leeg is, zal geen e-mail worden verzonden.

* Als een entiteit **op de lijst van gewenste personen** is, en niet op de suppressielijst, wordt e-mail verzonden naar de overeenkomstige ontvanger(s). Nochtans, als de entiteit ook op de [ suppressielijst ](../reports/suppression-list.md) is, zullen de overeenkomstige ontvanger(s) niet e-mail ontvangen, de reden die **[!UICONTROL Suppressed]** is.

* Als een entiteit **niet op de lijst van gewenste personen** (en niet op de onderdrukkingslijst) is, zullen de overeenkomstige ontvanger(s) niet e-mail ontvangen, de reden die **[!UICONTROL Not allowed]** is.

>[!NOTE]
>
>De profielen met de status **[!UICONTROL Not allowed]** worden tijdens het verzenden van berichten uitgesloten. Daarom terwijl de **rapporten van de Reis** deze profielen zullen tonen zoals die door de reis ([ gelezen Publiek ](../building-journeys/read-audience.md) en [ berichtactiviteiten ](../building-journeys/journey-action.md)) zijn bewogen, zullen de **E-mail rapporten** niet hen in de **[!UICONTROL Sent]** metriek omvatten aangezien zij voorafgaand aan e-mail het verzenden worden uitgefilterd.
>
>Leer meer over het [ Levende Rapport ](../reports/live-report.md) en [ rapport van Customer Journey Analytics ](../reports/report-gs-cja.md).

Wanneer de lijst van gewenste personen [ ](#deactivate-allow-list) wordt gedeactiveerd, worden alle e-mails die u van de huidige zandbak verzendt verzonden naar alle ontvangers (mits zij niet op de suppressielijst), met inbegrip van echte klantenadressen zijn.

## Uitsluitingsrapportage {#reporting}

Wanneer de lijst van gewenste personen actief is, kunt u e-mailadressen of domeinen terugwinnen die van het verzenden werden uitgesloten omdat zij niet op de lijst van gewenste personen waren. Om dit te doen, kunt u de [ Dienst van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} gebruiken om de API hieronder vraag te maken.

Om het **aantal e-mails** te krijgen die niet werden verzonden omdat de ontvangers niet op de lijst van gewenste personen waren, gebruik de volgende vraag:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Om de **lijst van e-mailadressen** te krijgen die niet werden verzonden omdat de ontvangers niet op de lijst van gewenste personen waren, gebruik de volgende vraag:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
