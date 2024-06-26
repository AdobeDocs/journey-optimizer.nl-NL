---
solution: Journey Optimizer
product: journey optimizer
title: Bedrijfsvoorschriften
description: Leer hoe u frequentieregels definieert
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: bericht, frequentie, regels, druk
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: f47f4e783dd66d9031c7f7c447c1b20418a583c0
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 0%

---

# Bedrijfsvoorschriften {#frequency-rules}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_message_frequency_rules"
>title="Zakelijke regels"
>abstract="De de frequentieregels van het bericht zijn een type van bedrijfsregel die het aantal tijden beperken de gebruikers berichten ontvangen of reizen over één of veelvoudige kanalen ingaan. Deze regels voor meerdere kanalen sluiten te vaak gevraagde profielen automatisch uit van berichten en handelingen."

[!DNL Journey Optimizer] staat u toe om te controleren hoe vaak de gebruikers een bericht zullen ontvangen of in een reis over één of veelvoudige kanaal zullen ingaan. Regels voor berichtfrequentie waarmee automatisch overgevraagde profielen worden uitgesloten van berichten en handelingen.

Voor een merk kan het bijvoorbeeld de regel zijn dat niet meer dan 4 marketingberichten per maand naar hun klanten worden gestuurd. Hiervoor kunt u een bedrijfsregel gebruiken die het aantal verzonden berichten beperkt op basis van een of meer kanalen gedurende een maandelijkse kalenderperiode.

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>De bedrijfsregels zijn verschillend van opt-out beheer, dat gebruikers toestaat om van het ontvangen van mededelingen van een merk af te zien. [Meer informatie](../privacy/opt-out.md#opt-out-management)

➡️ [Deze functie in video detecteren](#video)

## Toegang tot bedrijfsregels {#access-rules}

De bedrijfsregels zijn beschikbaar bij de **[!UICONTROL Administration]** > **[!UICONTROL Business rules]** -menu. Alle regels worden weergegeven, gesorteerd op wijzigingsdatum. Gebruik het filterpictogram om te filteren op de categorie, status en/of kanaal. U kunt ook op het berichtlabel zoeken.

![](assets/message-rules-filter.png)

### Machtigingen{#permissions-frequency-rules}

Om tot bedrijfsregels toegang te hebben, te creëren, uit te geven of te schrappen, moet u hebben **[!UICONTROL Manage frequency rules]** toestemming.

Gebruikers met de **[!UICONTROL View frequency rules]** de toestemming kan regels bekijken, maar niet om hen te wijzigen of te schrappen.

![](assets/message-rules-access.png)

Meer informatie over machtigingen in [deze sectie](../administration/high-low-permissions.md).

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

1. Toegang krijgen tot de **[!UICONTROL Business rules]** lijst en klik vervolgens op **[!UICONTROL Create rule]**.

   ![](assets/message-rules-create.png)

1. Bepaal de regelnaam en selecteer de categorie van de berichtregel.

   >[!NOTE]
   >
   >Alleen de **[!UICONTROL Marketing]** -categorie is beschikbaar.

   ![](assets/message-rules-details.png)

1. Van de **[!UICONTROL Duration]** selecteert u een tijdkader voor de bijschriften die u wilt toepassen. [Meer informatie](#frequency-cap)

1. Plaats het maximum voor uw regel, betekenend het maximumaantal berichten dat naar een individueel gebruikersprofiel elke maand, of week kan worden verzonden <!--or day--> - volgens de bovenstaande selectie.

   <!--![](assets/message-rules-capping.png)-->

1. Selecteer het kanaal dat u voor deze regel wilt gebruiken: **[!UICONTROL Email]**, **[!UICONTROL Push notification]**, **[!UICONTROL SMS]** of **[!UICONTROL Direct mail]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >U moet ten minste één kanaal selecteren om de regel te kunnen maken.

1. Selecteer meerdere kanalen als u de afdekking op alle geselecteerde kanalen als een totaal aantal wilt toepassen.

   Stel de aftopping bijvoorbeeld in op 15 en selecteer het e-mailadres en het pushkanaal. Als een profiel al 10 marketingberichten en 5 marketingpushmeldingen voor de geselecteerde periode heeft ontvangen, wordt dit profiel uitgesloten van de eerstvolgende levering van elke marketingmail of pushmelding.

1. Klikken **[!UICONTROL Save as draft]** om de regel te bevestigen. Uw bericht wordt toegevoegd aan de regellijst, met de **[!UICONTROL Draft]** status.

   ![](assets/message-rules-created.png)

### Frequentiegrens {#frequency-cap}

Van de **[!UICONTROL Duration]** Selecteer deze optie in de vervolgkeuzelijst als u de afbeelding maandelijks of wekelijks wilt laten toewijzen.

>[!NOTE]
>
>Dagelijkse frequentiegrens is ook beschikbaar op verzoek. [Meer informatie](#daily-frequency-cap)

De frequentiegrens is gebaseerd op de geselecteerde kalenderperiode. Deze wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader.

![](assets/message-rules-capping-duration.png)

De teller loopt voor elke periode als volgt af:

* **[!UICONTROL Monthly]** De frequentie-instelling is geldig tot de laatste dag van de maand op 23:59:59 UTC De maandelijkse vervaldatum voor januari is bijvoorbeeld 01-31 23:59:59 UTC

* **[!UICONTROL Weekly]**: De frequentiekapitaal is geldig tot zaterdag 23:59:59 UTC van die week als de kalenderweek op zondag begint. De vervaldatum staat los van de instelling van de regel. Bijvoorbeeld, als de regel op Donderdag wordt gecreeerd, is deze regel geldig tot Zaterdag bij 23:59:59.

### Dagelijkse frequentie dop {#daily-frequency-cap}

Naast de maanden- en wekelijkse frequentie is ook de dagelijkse frequentie-limiet op aanvraag beschikbaar. Neem voor meer informatie contact op met uw Adobe.

De dagelijkse frequentiedop is geldig tot 23 dagen:59:59 UTC en wordt opnieuw ingesteld op 0 aan het begin van de volgende dag.

>[!NOTE]
>
>Om ervoor te zorgen dat de dagelijkse regels voor frequentiecontrole correct zijn, moet het gebruik van [streamingsegmentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} wordt aanbevolen. Meer informatie over methoden voor publieksevaluatie vindt u in [deze sectie](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

## Een bedrijfsregel activeren {#activate-rule}

Wanneer gecreeerd, heeft een bedrijfsregel **[!UICONTROL Draft]** status en heeft nog geen invloed op een bericht. Als u deze wilt inschakelen, klikt u op de ellips naast de regel en selecteert u **[!UICONTROL Activate]**.

![](assets/message-rules-activate.png)

Het activeren van een regel heeft invloed op berichten waarop deze van toepassing is bij de volgende uitvoering. Leer hoe u [pas een bedrijfsregel op een bericht toe](#apply-frequency-rule).

>[!NOTE]
>
>Het kan tot 10 minuten duren voordat een regel volledig geactiveerd is. U hoeft geen berichten te wijzigen of ritten opnieuw te publiceren voordat een regel van kracht wordt.

Als u een bedrijfsregel wilt deactiveren, klikt u op de ellips naast de regel en selecteert u **[!UICONTROL Deactivate]**.

![](assets/message-rules-deactivate.png)

De status van de regel verandert in **[!UICONTROL Inactive]** en de regel zal niet op toekomstige berichtuitvoeringen van toepassing zijn. Berichten die momenteel worden uitgevoerd, worden niet beïnvloed.

>[!NOTE]
>
>Het deactiveren van een regel heeft geen invloed op tellingen van afzonderlijke profielen en stelt deze niet opnieuw in.

## Pas een bedrijfsregel op een bericht toe {#apply-frequency-rule}

Volg onderstaande stappen om een bedrijfsregel toe te passen op een bericht.

1. Wanneer u een [reis](../building-journeys/journey-gs.md), voeg een bericht toe door één van de kanalen te selecteren u voor uw regel bepaalde.

1. Selecteer de categorie die u voor de [regel gemaakt](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Momenteel alleen de **[!UICONTROL Marketing]** rubriek is beschikbaar voor bedrijfsregels.

1. U kunt op de knop **[!UICONTROL Frequency rule]** koppeling om het scherm met frequentieregels weer te geven in een nieuw tabblad. [Meer informatie](#access-rules)

   Alle regels die overeenkomen met de geselecteerde categorie en kanalen worden automatisch toegepast op dit bericht.

   >[!NOTE]
   >
   >Berichten waarbij de geselecteerde categorie is **[!UICONTROL Transactional]** niet worden getoetst aan de frequentievoorschriften.

1. U kunt het aantal profielen dat is uitgesloten van levering bekijken in het dialoogvenster [Algemeen rapport](../reports/global-report.md)en in de [Live-rapport](../reports/live-report.md), waar de bedrijfsregels worden vermeld als mogelijke reden voor gebruikers die van levering worden uitgesloten.

>[!NOTE]
>
>Verschillende regels kunnen op hetzelfde kanaal van toepassing zijn, maar wanneer het onderste hoofdlettergebruik is bereikt, wordt het profiel uitgesloten van de volgende leveringen.

## Voorbeeld: meerdere regels combineren {#frequency-rule-example}

U kunt verschillende bedrijfsregels combineren, zoals in het onderstaande voorbeeld wordt beschreven.

1. [Een bedrijfsregel maken](#create-new-rule) gebeld *Algemene marketinglimiet*:

   * Selecteer alle kanalen.
   * Afbeelding instellen op 12 per maand.

   ![](assets/message-rules-ex-overall-cap.png)

1. Om het aantal op marketing-gebaseerde pushberichten verder te beperken dat een gebruiker wordt verzonden, creeer een tweede regel genoemd *Push Marketing Cap*:

   * Selecteer Push-kanaal.
   * Afbeelding instellen op 4 per maand.

   ![](assets/message-rules-ex-push-cap.png)

1. Opslaan en [activate](#activate-rule) de regel.

1. [Een bericht maken](../building-journeys/journeys-message.md) voor elk kanaal wilt u door communiceren en selecteren **[!UICONTROL Marketing]** categorie voor elk bericht. [Leer hoe u een bedrijfsregel toepast](#apply-frequency-rule)

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
>Bij het testen van bedrijfsregels wordt aanbevolen een nieuw gemaakt product te gebruiken [testprofiel](../audience/creating-test-profiles.md)Omdat er geen manier is om de teller opnieuw in te stellen tot de volgende maand wanneer de frequentie-instelling van een profiel is bereikt. Als u een regel deactiveert, kunnen beperkte profielen berichten ontvangen, maar worden er geen tellerverhogingen verwijderd of verwijderd.

## Hoe kan ik-video {#video}

Leer hoe u bedrijfsregels maakt, activeert, test en rapporteert.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
