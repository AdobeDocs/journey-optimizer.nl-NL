---
solution: Journey Optimizer
product: journey optimizer
title: Bedrijfsvoorschriften verbeteren
description: Meer informatie over het definiëren van regels voor zakelijke frequenties
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: bericht, frequentie, regels, druk
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 46c4d3081603115db71b01a05f12187cd7e0d34c
workflow-type: tm+mt
source-wordcount: '1230'
ht-degree: 0%

---

# Bedrijfsregels configureren {#frequency-rules}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_message_frequency_rules"
>title="Zakelijke regels"
>abstract="De de frequentieregels van het bericht zijn een type van bedrijfsregel die het aantal tijden beperken de gebruikers berichten ontvangen of reizen over één of veelvoudige kanalen ingaan. Deze regels voor meerdere kanalen sluiten te vaak gevraagde profielen automatisch uit van berichten en handelingen."

Met [!DNL Journey Optimizer] kunt u bepalen hoe vaak gebruikers een bericht ontvangen of een reis via een of meerdere kanalen invoeren. Regels voor berichtfrequentie waarmee automatisch overgevraagde profielen worden uitgesloten van berichten en handelingen.

Voor een merk kan het bijvoorbeeld de regel zijn dat niet meer dan 4 marketingberichten per maand naar hun klanten worden gestuurd. Hiervoor kunt u een bedrijfsregel gebruiken die het aantal verzonden berichten beperkt op basis van een of meer kanalen gedurende een maandelijkse kalenderperiode.

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>De bedrijfsregels zijn verschillend van opt-out beheer, dat gebruikers toestaat om van het ontvangen van mededelingen van een merk af te zien. [Meer informatie](../privacy/opt-out.md#opt-out-management)

➡️ [ ontdekt deze eigenschap in video ](#video)

## Toegang tot bedrijfsregels {#access-rules}

De bedrijfsregels zijn beschikbaar in het menu **[!UICONTROL Administration]** > **[!UICONTROL Business rules]** . Alle regels worden weergegeven, gesorteerd op wijzigingsdatum. Gebruik het filterpictogram om te filteren op de categorie, status en/of kanaal. U kunt ook op het berichtlabel zoeken.

![](assets/message-rules-filter.png)

### Machtigingen{#permissions-frequency-rules}

U moet beschikken over de machtiging **[!UICONTROL Manage frequency rules]** om bedrijfsregels te openen, te maken, te bewerken of te verwijderen.

Gebruikers met de machtiging **[!UICONTROL View frequency rules]** kunnen regels weergeven, maar deze niet wijzigen of verwijderen.

![](assets/message-rules-access.png)

Leer meer over toestemmingen in [ deze sectie ](../administration/high-low-permissions.md).

## Een bedrijfsregel maken {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Selecteer de categorie voor berichtregels"
>abstract="Als u een bericht activeert en erop toepast, worden alle bedrijfsregels die overeenkomen met de geselecteerde categorie, automatisch toegepast op dit bericht. Momenteel is alleen de marketingcategorie beschikbaar."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="De plafonnering voor uw bedrijfsregel instellen"
>abstract="Geef het maximumaantal berichten op dat binnen de gekozen tijdsperiode naar een klantprofiel wordt verzonden. De maximale frequentie wordt gebaseerd op de geselecteerde kalenderperiode en wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader."

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Bepaal de kanalen de bedrijfsregel op van toepassing is"
>abstract="Selecteer ten minste één kanaal. De bedekking wordt toegepast over kanalen als totale telling."

Volg onderstaande stappen om een nieuwe bedrijfsregel te maken.

1. Open de lijst **[!UICONTROL Business rules]** en klik vervolgens op **[!UICONTROL Create rule]** .

   ![](assets/message-rules-create.png)

1. Bepaal de regelnaam en selecteer de categorie van de berichtregel.

   >[!NOTE]
   >
   >Alleen de categorie **[!UICONTROL Marketing]** is beschikbaar.

   ![](assets/message-rules-details.png)

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Duration]** een tijdskader voor de uitlijning die u wilt toepassen. [Meer informatie](#frequency-cap)

1. Stel de plafonnering voor uw regel in. Dit is het maximum aantal berichten dat per maand of week naar een individueel gebruikersprofiel kan worden verzonden <!--or day--> - volgens de bovenstaande selectie.

   <!--![](assets/message-rules-capping.png)-->

1. Selecteer het kanaal dat u voor deze regel wilt gebruiken: **[!UICONTROL Email]**, **[!UICONTROL Push notification]**, **[!UICONTROL SMS]** of **[!UICONTROL Direct mail]** .

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >U moet ten minste één kanaal selecteren om de regel te kunnen maken.

1. Selecteer meerdere kanalen als u de afdekking op alle geselecteerde kanalen als een totaal aantal wilt toepassen.

   Stel de aftopping bijvoorbeeld in op 15 en selecteer het e-mailadres en het pushkanaal. Als een profiel al 10 marketingberichten en 5 marketingpushmeldingen voor de geselecteerde periode heeft ontvangen, wordt dit profiel uitgesloten van de eerstvolgende levering van elke marketingmail of pushmelding.

1. Klik op **[!UICONTROL Save as draft]** om het maken van de regel te bevestigen. Uw bericht wordt met de status **[!UICONTROL Draft]** toegevoegd aan de lijst met regels.

   ![](assets/message-rules-created.png)

### Frequentiegrens {#frequency-cap}

Selecteer in de vervolgkeuzelijst **[!UICONTROL Duration]** of u de uitlijning maandelijks of wekelijks wilt toepassen.

>[!NOTE]
>
>Dagelijkse frequentiegrens is ook beschikbaar op verzoek. [Meer informatie](#daily-frequency-cap)

De frequentiegrens is gebaseerd op de geselecteerde kalenderperiode. Deze wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader.

![](assets/message-rules-capping-duration.png)

De teller loopt voor elke periode als volgt af:

* **[!UICONTROL Monthly]**: Het frequentiekapitaal is geldig tot de laatste dag van de maand bij 23 :59: 59 UTC. Bijvoorbeeld, is de maandelijkse vervaldatum voor Januari 01-31 23 :59: 59 UTC.

* **[!UICONTROL Weekly]**: Het frequentiekapitaal is geldig tot Zaterdag 23 :59: 59 UTC van die week aangezien de kalenderweek op zondag begint. De vervaldatum staat los van de instelling van de regel. Bijvoorbeeld, als de regel op Donderdag wordt gecreeerd, is deze regel geldig tot Zaterdag bij 23 :59: 59.

### Dagelijkse frequentie dop {#daily-frequency-cap}

Naast de maanden- en wekelijkse frequentie is ook de dagelijkse frequentie-limiet op aanvraag beschikbaar. Neem hiervoor contact op met uw Adobe-vertegenwoordiger.

Het dagelijkse frequentiemaximum is geldig voor de dag tot 23 :59: 59 UTC en stelt aan 0 bij het begin van de volgende dag terug.

>[!NOTE]
>
>Om nauwkeurigheid voor dagelijkse frequentie die regels begrenst te verzekeren, wordt het gebruik van [ streaming segmentatie ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html) {target="_blank"} geadviseerd. Leer meer op de methodes van de publieksevaluatie in [ deze sectie ](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

## Een bedrijfsregel activeren {#activate-rule}

Wanneer een bedrijfsregel wordt gemaakt, heeft deze de status **[!UICONTROL Draft]** en heeft deze nog geen invloed op een bericht. Klik op de ellips naast de regel en selecteer **[!UICONTROL Activate]** om deze in te schakelen.

![](assets/message-rules-activate.png)

Het activeren van een regel heeft invloed op berichten waarop deze van toepassing is bij de volgende uitvoering. Leer hoe te [ een bedrijfsregel op een bericht ](#apply-frequency-rule) toepassen.

>[!NOTE]
>
>Het kan tot 10 minuten duren voordat een regel volledig geactiveerd is. U hoeft geen berichten te wijzigen of ritten opnieuw te publiceren voordat een regel van kracht wordt.

Als u een bedrijfsregel wilt deactiveren, klikt u op de ellips naast de regel en selecteert u **[!UICONTROL Deactivate]** .

![](assets/message-rules-deactivate.png)

De status van de regel verandert in **[!UICONTROL Inactive]** en de regel is niet van toepassing op toekomstige berichtuitvoeringen. Berichten die momenteel worden uitgevoerd, worden niet beïnvloed.

>[!NOTE]
>
>Het deactiveren van een regel heeft geen invloed op tellingen van afzonderlijke profielen en stelt deze niet opnieuw in.

## Pas een bedrijfsregel op een bericht toe {#apply-frequency-rule}

Volg onderstaande stappen om een bedrijfsregel toe te passen op een bericht.

1. Wanneer het creëren van a [ reis ](../building-journeys/journey-gs.md), voeg een bericht toe door één van de kanalen te selecteren u voor uw regel bepaalde.

1. Selecteer de categorie u voor de [ regel bepaalde u ](#create-new-rule) creeerde.

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Momenteel is alleen de categorie **[!UICONTROL Marketing]** beschikbaar voor bedrijfsregels.

1. U kunt op de koppeling **[!UICONTROL Frequency rule]** klikken om het scherm met frequentieregels op een nieuw tabblad weer te geven. [Meer informatie](#access-rules)

   Alle regels die overeenkomen met de geselecteerde categorie en kanalen worden automatisch toegepast op dit bericht.

   >[!NOTE]
   >
   >Berichten waarbij de geselecteerde categorie **[!UICONTROL Transactional]** is, worden niet aan de hand van de frequentieregels geëvalueerd.

1. U kunt het aantal profielen bekijken die van levering in het [ rapport van Customer Journey Analytics ](../reports/report-gs-cja.md) worden uitgesloten, en in het [ Levende rapport ](../reports/live-report.md), waar de bedrijfsregels als mogelijke reden voor gebruikers zullen worden vermeld die van levering worden uitgesloten.

>[!NOTE]
>
>Verschillende regels kunnen op hetzelfde kanaal van toepassing zijn, maar wanneer het onderste hoofdlettergebruik is bereikt, wordt het profiel uitgesloten van de volgende leveringen.

## Voorbeeld: meerdere regels combineren {#frequency-rule-example}

U kunt verschillende bedrijfsregels combineren, zoals in het onderstaande voorbeeld wordt beschreven.

1. [ creeer een bedrijfsregel ](#create-new-rule) geroepen *Globale Afbeelding van de Marketing*:

   * Selecteer alle kanalen.
   * Afbeelding instellen op 12 per maand.

   ![](assets/message-rules-ex-overall-cap.png)

1. Om het aantal op marketing-gebaseerde pushberichten verder te beperken dat een gebruiker wordt verzonden, creeer een tweede regel genoemd *Push Marketing Cap*:

   * Selecteer Push-kanaal.
   * Afbeelding instellen op 4 per maand.

   ![](assets/message-rules-ex-push-cap.png)

1. Sparen en [ activeer ](#activate-rule) de regel.

1. [ creeer een bericht ](../building-journeys/journeys-message.md) voor elk kanaal u door wilt communiceren en de **[!UICONTROL Marketing]** categorie voor elk bericht selecteren. [ Leer hoe te om een bedrijfsregel toe te passen ](#apply-frequency-rule)

   ![](assets/journey-message-category.png)


<!--
Learn how to create a message for the different channels in the following sections:
* [Create an email](../email/create-email.md)
* [Create a push notification](../push/create-push.md)
* [Create an SMS](../sms/create-sms.md)
* [Create a direct mail](../direct-mail/create-direct-mail.md)

Create an email and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../email/create-email.md)

Create a push notification and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../push/create-push.md)

Create an SMS and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../sms/create-sms.md)

Create a direct mail and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../direct-mail/create-direct-mail.md)
-->

In dit scenario wordt een individueel profiel:
* per maand maximaal 12 marketingberichten kunnen ontvangen;
* maar worden uitgesloten van het in de handel brengen van pushberichten nadat ze 4 pushmeldingen hebben ontvangen.

>[!NOTE]
>
>Wanneer het testen van bedrijfsregels, wordt het geadviseerd om een pas gecreeerd [ testprofiel ](../audience/creating-test-profiles.md) te gebruiken, omdat zodra de de frequentiedrempel van een profiel wordt bereikt, er geen manier is om de teller tot de volgende maand terug te stellen. Als u een regel deactiveert, kunnen beperkte profielen berichten ontvangen, maar worden er geen tellerverhogingen verwijderd of verwijderd.

## Hoe kan ik-video {#video}

Leer hoe u bedrijfsregels maakt, activeert, test en rapporteert.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
