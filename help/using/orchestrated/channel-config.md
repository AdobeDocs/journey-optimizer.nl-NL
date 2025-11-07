---
solution: Journey Optimizer
product: journey optimizer
title: De kanaalconfiguratie configureren
description: Leer hoe te om uw configuratie van het Kanaal te vormen
version: Campaign Orchestration
source-git-commit: 0b92d0e806c47b0d87ba53b7c7f1d56ee4453abb
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# De kanaalconfiguratie configureren {#channel-configuration}

Na vestiging uw [ Doel Dimension ](target-dimension.md), moet u uw **[!UICONTROL Channel Configuration]** vormen en aangewezen **[!UICONTROL Execution Details]** bepalen. Zo kunt u definiëren:

* **het niveau van berichtlevering**: bijvoorbeeld, verzendend één bericht per ontvanger, zoals één enkele e-mail per individu.

* **het uitvoeringsadres**: het specifieke contactgebied dat voor het verzenden, zoals een e-mailadres of een telefoonaantal moet worden gebruikt.

U kunt als volgt de kanaalconfiguratie configureren:

1. Begin door uw **[!UICONTROL Channel configuration]** te maken en te configureren.

   U kunt ook een bestaande **[!UICONTROL Channel configuration]** bijwerken.

   ➡️ [ volg de stappen die in deze pagina ](../email/surface-personalization.md) worden gedetailleerd

1. Open vanuit de sectie **[!UICONTROL Execution details]** van uw **[!UICONTROL Channel configuration]** de tab **[!UICONTROL Orchestrated campaigns]** .

   ![](assets/target-dimension-3.png)

1. Klik op **[!UICONTROL Enabled]** om deze compatibel te maken met geordende campagnes.

1. Kies uw leveringsmethode:

   * **[!UICONTROL Target Dimension]**: verzenden naar de primaire entiteit, bijvoorbeeld de ontvanger.

   * **[!UICONTROL Target + Secondary Dimension]**: verzenden met zowel primaire als secundaire entiteiten, bijvoorbeeld ontvanger + contract.

1. Selecteer van drop-down uw [ eerder gecreeerd Doel Dimension ](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. Als u **[!UICONTROL Target + Secondary Dimension]** hebt geselecteerd als de leveringsmethode, kiest u een **[!UICONTROL Secondary Dimension]** om de context voor het verzenden van berichten te definiëren.

1. Kies onder de sectie **[!UICONTROL Execution Address]** welke **[!UICONTROL Source]** moet worden gebruikt om het bezorgadres op te halen, zoals het e-mailadres of telefoonnummer:

   * **[!UICONTROL Profile]**: selecteer deze optie als het bezorgingsadres, bijvoorbeeld e-mail, rechtstreeks in het hoofdprofiel van de klant wordt opgeslagen.

     Nuttig wanneer het verzenden van berichten naar de belangrijkste klant, niet een specifieke bijbehorende entiteit.

   * **[!UICONTROL Target Dimension]**: Kies deze optie als het bezorgadres is opgeslagen in de primaire entiteit, bijvoorbeeld een ontvanger.

     Nuttig wanneer elke ontvanger zijn eigen bezorgadres heeft, zoals een ander e-mailadres of telefoonnummer.

   * **[!UICONTROL Secondary Dimension]**: Wanneer u **[!UICONTROL Target + Secondary Dimension]** als leveringsmethode gebruikt, selecteert u de relevante **[!UICONTROL Secondary Dimension]** die u eerder hebt geconfigureerd.

     Als de secundaire dimensie bijvoorbeeld een boeking of abonnement vertegenwoordigt, kan het uitvoeringsadres, zoals een e-mail, van dat niveau worden genomen. Dit is handig wanneer profielen bij het boeken of abonneren op een service andere contactgegevens gebruiken.

1. Van het **[!UICONTROL Delivery address]** gebied, klik ![ geef pictogram ](assets/do-not-localize/edit.svg) uit om het specifieke gebied te kiezen voor uw berichtlevering te gebruiken.

   ![](assets/target-dimension-4.png)

1. Klik op **[!UICONTROL Submit]** wanneer dit is geconfigureerd.

Uw kanaal is nu klaar om met **Geordende Campagnes** te gebruiken, en de berichten zullen volgens de geselecteerde doeldimensie worden geleverd.
