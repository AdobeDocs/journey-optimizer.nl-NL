---
solution: Journey Optimizer
product: journey optimizer
title: Bedrijfsvoorschriften
description: Leer hoe u bedrijfsregels maakt en toepast
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: bericht, frequentie, regels, druk
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: c1eef06b0edc4e1bcd1b145f8f822295924b205c
workflow-type: tm+mt
source-wordcount: '1387'
ht-degree: 0%

---

# Bedrijfsvoorschriften {#business-rules}

>[!AVAILABILITY]
>
>De bedrijfsregels zijn momenteel beschikbaar als bèta om gebruikers slechts te selecteren.

[!DNL Journey Optimizer] Hiermee kunt u bepalen hoe vaak gebruikers een bericht ontvangen door kanaalregels in te stellen die automatisch overgevraagde profielen uitsluiten van berichten en handelingen.

Voor een merk kan een regel bijvoorbeeld zijn: om niet meer dan 4 marketingberichten per maand naar hun klanten te sturen. Hiervoor kunt u een regel voor de frequentie gebruiken die het aantal verzonden berichten beperkt op basis van een of meer kanalen gedurende een maandelijkse kalenderperiode.

Door het creëren van verschillende regelreeksen voor betere granulariteit, [!DNL Journey Optimizer] laat u toe om frequentiecapping op verschillende types van marketing mededelingen toe te passen. U kunt bijvoorbeeld een regelset maken om het aantal **promotionele communicatie** verzonden naar uw klanten, en creeer een andere die regel wordt geplaatst om het aantal te beperken **nieuwsbrieven** naar hen verzonden.

>[!NOTE]
>
>De bedrijfsregels zijn verschillend van opt-out beheer, dat gebruikers toestaat om van het ontvangen van mededelingen van een merk af te zien. [Meer informatie](../privacy/opt-out.md#opt-out-management)

## Toegangsregelsets {#access-rule-sets}

Regelsets zijn beschikbaar via de **[!UICONTROL Administration]** > **[!UICONTROL Business rules (Beta)]** -menu. Alle regels worden weergegeven, gesorteerd op aanmaakdatum.

![](assets/rule-sets-list.png)

Klik op de naam van een regelset om de inhoud ervan weer te geven en te bewerken. Alle regels inbegrepen in die regelreeks zijn vermeld.

Met het contextmenu rechtsboven kunt u:

* De naam en beschrijving van de regelset bewerken
* De regelset activeren - [Meer informatie](#activate-rule)
* De regelset verwijderen

![](assets/rule-set-example.png)

Voor elke regel in de regelset wordt de **[!UICONTROL More actions]** Met de knop kunt u:

* De regel bewerken
* De regel activeren [Meer informatie](#activate-rule)
* De regel verwijderen

![](assets/rule-set-example-rules.png)

<!--### Permissions{#permissions-frequency-rules}

To access, create, edit or delete message frequency rules, you must have the **[!UICONTROL Manage frequency rules]** permission. 

Users with the **[!UICONTROL View frequency rules]** permission are able to view rules, but not to modify or delete them.

![](assets/message-rules-access.png)

Learn more about permissions in [this section](../administration/high-low-permissions.md).-->

## Een regelset maken {#create-rule-set}

Volg onderstaande stappen om een regelset te maken.

1. Toegang krijgen tot de **[!UICONTROL Rules sets]** lijst en klik vervolgens op **[!UICONTROL Create rule set]**.

   ![](assets/rule-sets-create-button.png)

1. Bepaal de naam van de regelreeks, voeg indien gewenst een beschrijving toe en klik **[!UICONTROL Save]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >De naam van de regelset moet uniek zijn.

1. Nu kunt u [de regels](#create-new-rule) u aan deze regelreeks wilt toevoegen, en [activate](#activate-rule) het.

   >[!NOTE]
   >
   >Zorg ervoor alle regels u op uw berichten wilt toepassen ook in de regelreeks worden geactiveerd.

## Een regel maken {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="Selecteer de categorie voor berichtregels"
>abstract="Wanneer deze optie wordt geactiveerd en toegepast op een bericht, worden alle frequentieregels die overeenkomen met de geselecteerde categorie automatisch toegepast op dit bericht. Momenteel is alleen de marketingcategorie beschikbaar."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="De uitlijning van uw regel instellen"
>abstract="Geef het maximumaantal berichten op dat binnen de gekozen tijdsperiode naar een klantprofiel wordt verzonden. De maximale frequentie wordt gebaseerd op de geselecteerde kalenderperiode en wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Bepaal de kanalen waarop de regel van toepassing is"
>abstract="Selecteer ten minste één kanaal. De bedekking wordt toegepast over kanalen als totale telling."

Volg onderstaande stappen om een regel aan een regelset toe te voegen.

1. Van de regelreeks u enkel creeerde, klik **[!UICONTROL Add rule]**.

   ![](assets/rule-sets-create-rule-button.png)

1. Bepaal de regelnaam.

   >[!NOTE]
   >
   >De naam van de regelset moet uniek zijn.

1. Selecteer de categorie van de berichtregel.

   >[!NOTE]
   >
   >Momenteel alleen de **[!UICONTROL Marketing]** -categorie is beschikbaar.

1. Van de **[!UICONTROL Duration]** selecteert u een tijdkader voor de bijschriften die u wilt toepassen. [Meer informatie](#frequency-cap)

1. Stel de plafonnering voor uw regel in. Dit betekent het maximumaantal berichten dat naar een individueel gebruikersprofiel kan worden verzonden per maand, week of dag - volgens de bovenstaande selectie.

1. Selecteer het kanaal dat u voor deze regel wilt gebruiken: **[!UICONTROL Email]**, **[!UICONTROL SMS]**, **[!UICONTROL Push notification]** of **[!UICONTROL Direct mail]**.

   ![](assets/rule-set-channels.png)

   >[!NOTE]
   >
   >U moet ten minste één kanaal selecteren om de regel te kunnen maken.

1. Selecteer meerdere kanalen als u de afdekking op alle geselecteerde kanalen als een totaal aantal wilt toepassen.

   Stel de aftopping bijvoorbeeld in op 5 en selecteer zowel het e-mailadres als het sms-kanaal. Als een profiel al 3 marketingberichten en 2 marketingberichten voor de geselecteerde periode heeft ontvangen, wordt dit profiel uitgesloten van de eerstvolgende levering van een marketingbericht of -bericht.

1. Klikken **[!UICONTROL Save]** om de regel te bevestigen. Uw bericht wordt toegevoegd aan de regelreeks, met **[!UICONTROL Draft]** status.

   ![](assets/rule-set-rule-created.png)

1. Herhaal bovenstaande stappen om zoveel regels toe te voegen als nodig zijn voor de regelset.

Nu moet u elke regel activeren alvorens het op om het even welke berichten kan worden toegepast. [Meer informatie](#activate-rule)

>[!NOTE]
>
>Controleer of de regelset ook is geactiveerd om deze in uw berichten te kunnen selecteren.

### Frequentiegrens {#frequency-cap}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="Selecteer de categorie voor berichtregels"
>abstract="Wanneer deze optie wordt geactiveerd en toegepast op een bericht, worden alle frequentieregels die overeenkomen met de geselecteerde categorie automatisch toegepast op dit bericht. Momenteel is alleen de marketingcategorie beschikbaar."

Van de **[!UICONTROL Duration]** vervolgkeuzelijst, selecteert u of u de plafonnering maandelijks, wekelijks of dagelijks wilt toepassen.

De frequentiegrens is gebaseerd op de geselecteerde kalenderperiode. Deze wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader.

![](assets/rule-set-capping-duration.png)

De teller loopt voor elke periode als volgt af:

* **[!UICONTROL Monthly]** De frequentie-instelling is geldig tot de laatste dag van de maand op 23:59:59 UTC De maandelijkse vervaldatum voor januari is bijvoorbeeld 01-31 23:59:59 UTC

* **[!UICONTROL Weekly]**: De frequentiekapitaal is geldig tot zaterdag 23:59:59 UTC van die week als de kalenderweek op zondag begint. De vervaldatum staat los van de instelling van de regel. Bijvoorbeeld, als de regel op Donderdag wordt gecreeerd, is deze regel geldig tot Zaterdag bij 23:59:59.

* **[!UICONTROL Daily]** De dagelijkse frequentie dop is geldig tot 23:59:59 UTC en wordt opnieuw ingesteld op 0 aan het begin van de volgende dag.

### Dagelijkse frequentie dop {#daily-frequency-cap}

>[!CAUTION]
>
>Om ervoor te zorgen dat de dagelijkse regels voor frequentiecontrole correct zijn, moet het gebruik van [streamingsegmentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} is verplicht. Meer informatie over methoden voor publieksevaluatie vindt u in [deze sectie](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

Voor om het even welke segmentgrootte tot de grens van 60 miljoen berichten per uur<!--not clear-->, moet u ervoor zorgen dat uw campagnes ten minste twee uur van elkaar verwijderd zijn.


<!-- Journey example:

* If customer sets a Daily rule under the Global Ruleset for email <= 2/day:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for noon)
   * Journey 789 (scheduled for 1 pm)

   In this example, the Daily Frequency cap will not guarantee <= 2/day. The rule will only be guaranteed when Journeys are at least 2 hours apart:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for 2 pm)
   * Journey 789 (scheduled for 4 pm)-->

Als u bijvoorbeeld een dagelijkse regel instelt volgens een regel die is ingesteld voor het e-mailkanaal die minder dan of gelijk is aan twee dagen, en als u de volgende campagnes maakt:
* Campagne A (gepland voor 12.00 uur)
* Campagne A (gepland voor 15.00 uur)
* Campagne B (gepland voor 13.00 uur)

Deze instelling werkt niet om twee redenen:
* De dagelijkse maximale frequentie is niet gegarandeerd, omdat de campagnes niet twee uur van elkaar verwijderd zijn.
* Het is niet de beste praktijk om dezelfde campagne meerdere keren per dag te plannen om te profiteren van de dagelijkse limiet.

Het onderstaande voorbeeld dient te worden gevolgd door de dagelijkse frequentiedop:
* Campagne A (gepland voor 12.00 uur)
* Campagne B (gepland voor 2 uur &#39;s middags)

<!--* To use the Daily Cap with a Journey, customers can use either an Event Triggered Journey or an Audience Qualified Journey. If customers wish to use the Daily Cap with a Read Audience Journey, they should use a Campaign instead and associate a Local Ruleset with the campaign, following the example given above.-->

## Regels en regelsets activeren {#activate-rule}

Wanneer deze regel wordt gemaakt, heeft deze de **[!UICONTROL Draft]** status en heeft nog geen invloed op een bericht. Als u deze wilt inschakelen, klikt u op de knop **[!UICONTROL More actions]** naast de regel en selecteer **[!UICONTROL Activate]**.

![](assets/rule-set-activate-rule.png)

U moet ook de regel activeren die is ingesteld om deze in campagnes/reizen te kunnen openen en toe te passen op uw berichten.

![](assets/rule-set-activate-set.png)

Het activeren van een regelreeks zal om het even welke berichten beïnvloeden het op hun volgende uitvoering van toepassing is. Leer hoe u [een regel toepassen die op een bericht is ingesteld](#apply-rule-set).

>[!NOTE]
>
>Het kan 10 minuten duren voordat een regel of regel volledig is geactiveerd. U hoeft geen berichten te wijzigen of ritten opnieuw te publiceren voordat een regel van kracht wordt.

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

## Regels en regelsets deactiveren {#deactivate-rule}

Als u een regel of een regelset wilt deactiveren, klikt u op de knop **[!UICONTROL More actions]** naast het gewenste item en selecteer **[!UICONTROL Deactivate]**.

![](assets/rule-set-inactive-rule.png)

De status verandert in **[!UICONTROL Inactive]** en de regel zal niet op toekomstige berichtuitvoeringen van toepassing zijn. Berichten die momenteel worden uitgevoerd, worden niet beïnvloed.

>[!NOTE]
>
>Het deactiveren van een regel of regelset heeft geen invloed op tellingen van afzonderlijke profielen en stelt deze niet opnieuw in.

## Pas een frequentieregel toe op een bericht {#apply-frequency-rule}

Volg onderstaande stappen om een frequentieregel toe te passen op een bericht.

1. Wanneer u een [campagne](../campaigns/create-campaign.md)selecteert u een van de kanalen die u voor de regelset hebt gedefinieerd en bewerkt u de inhoud van het bericht.

1. Klik in het scherm voor de inhoudseditie op de knop **[!UICONTROL Add Business Rule]** knop.

1. Selecteer de [regelset gemaakt](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >Alleen [geactiveerd](#activate-rule) regelsets worden weergegeven in de lijst.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. U kunt het aantal profielen dat is uitgesloten van levering bekijken in het dialoogvenster [Algemeen rapport](../reports/global-report.md)en in de [Live-rapport](../reports/live-report.md), waarbij de frequentievoorschriften worden vermeld als mogelijke reden voor gebruikers die van levering zijn uitgesloten.

>[!NOTE]
>
>Verschillende regels kunnen op hetzelfde kanaal van toepassing zijn, maar wanneer het onderste hoofdlettergebruik is bereikt, wordt het profiel uitgesloten van de volgende leveringen.

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

Bij het testen van de frequentieregels wordt aanbevolen een nieuw [testprofiel](../audience/creating-test-profiles.md)Omdat er geen manier is om de teller opnieuw in te stellen tot de volgende periode, wanneer de frequentiegrens van een profiel eenmaal is bereikt. Als u een regel deactiveert, kunnen beperkte profielen berichten ontvangen, maar worden er geen tellerverhogingen verwijderd of verwijderd.

