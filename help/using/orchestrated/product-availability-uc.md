---
solution: Journey Optimizer
product: journey optimizer
title: Gebruikers op de hoogte stellen van de beschikbaarheid van producten
description: Gebruikers op de hoogte stellen van de beschikbaarheid van producten
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Gebruikers op de hoogte stellen van de beschikbaarheid van producten {#product-availability-uc}

>[!BEGINSHADEBOX]

In dit geval wordt verzending op meerdere niveaus geïllustreerd: voor elk wenslijstitem wordt een aparte e-mail gegenereerd met het e-mailadres dat bij het afzonderlijke item is opgeslagen in plaats van de record voor de ontvanger. Hierdoor kunnen klanten afzonderlijke meldingen ontvangen voor elk product op hun verlanglijst, zelfs als ze verschillende e-mailadressen gebruiken voor verschillende items.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Ontwerp een back-in-stock melding om klanten te informeren wanneer items van hun Wishlist weer beschikbaar komen. Dit bericht helpt belangstellende klanten opnieuw aan de slag te gaan en moedigt hen aan om hun aankoop te voltooien terwijl de voorraad wordt aangevuld.

1. Begin met het opzetten van een nieuwe campagne die specifiek gericht is op Wishlist-hernieuwde betrokkenheid. Dit verzekert uw overseinen zich op klanten concentreren die reeds aankoopintentie door producten aan hun verlanglijst hebben getoond te bewaren.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Vul **[!UICONTROL Campaign Settings]** in, zoals de naam van de campagne, een beschrijving, de begin- en einddatum en relevante tags.

1. Voeg een **[!UICONTROL Build audience]** activiteit met Wishlist als **[!UICONTROL Targeting dimension]** toe.

   ![](assets/notify-1.png){zoomable="yes"}

1. Voeg uw voorwaarde toe om slechts vorstenlijsten te omvatten die in de afgelopen 36 maanden worden gecreeerd.

   ![](assets/notify-2.png){zoomable="yes"}

1. Voeg een **[!UICONTROL Change dimension]** activiteit toe om van vorstenlijsten terug naar de respectieve klant terug te gaan die voor het richten wordt geplaatst.

   ![](assets/notify-3.png){zoomable="yes"}

1. Nadat u de conceptmodus hebt gestart, geeft u een voorvertoning van de doelgroep weer met details van de lijst met aarzelaars. Klik voor meer informatie op een uitvoerresultaat en selecteer **[!UICONTROL Preview results]** .

   Hier, toont de gegevens zowel ontvangers als hun punten van het Schiderlijst. Sommige klanten hebben meerdere Wishlist-items en ontvangen door verzending op meerdere niveaus een aparte e-mail voor elk item. In sommige gevallen gebruiken klanten verschillende e-mailadressen voor afzonderlijke back-in-stock aanvragen.

   ![](assets/notify-4.png){zoomable="yes"}

1. Om een afzonderlijke e-mail voor elk punt te kunnen verzenden, zorg ervoor dat [&#x200B; uw e-mailconfiguratie &#x200B;](../orchestrated/target-dimension.md) met `Recipients - email` als **[!UICONTROL Profile Target Dimension]** en `Wishlistitems` als **[!UICONTROL Secondary dimension]** wordt geplaatst.

   Selecteer vervolgens in het menu **[!UICONTROL Execution Address]** de optie `wishlist.email` as **[!UICONTROL Secondary dimension]** . Elk item in de lijst met websites activeert een aparte e-mail, waarbij het e-mailadres wordt gebruikt dat in de gegevens in de lijst met websites is opgeslagen als secundaire dimensie.

   ![](assets/notify-5.png){zoomable="yes"}

1. Voeg een **[!UICONTROL Email]** activiteit toe om een bericht van de productbeschikbaarheid tot stand te brengen. Klik op **[!UICONTROL Edit content]** om uw inhoud te ontwerpen.

   ➡️ [&#x200B; Leer meer op e-mailverpersoonlijking &#x200B;](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Nadat uw campagne is getest en klaar is, klikt u op **[!UICONTROL Publish]** om deze actief te maken.

Met deze georkestreerde campagne, ontvangt de klant een afzonderlijke e-mail voor elk van hun wenst lijstpunten. Elk bericht wordt verzonden naar het specifieke e-mailadres verbonden aan die wenslijst, met gepersonaliseerde inhoud die uit de details van dat bepaalde wenslijstpunt wordt getrokken.

