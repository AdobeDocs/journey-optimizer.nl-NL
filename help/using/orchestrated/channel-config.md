---
solution: Journey Optimizer
product: journey optimizer
title: De kanaalconfiguratie configureren
description: Leer hoe te om uw configuratie van het Kanaal te vormen
version: Campaign Orchestration
source-git-commit: 2bdabace34546bd27c2e3c19a3aee3c8a3eae5f2
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# De kanaalconfiguratie configureren {#channel-configuration}

Na vestiging uw [&#x200B; Doel Dimension &#x200B;](target-dimension.md), moet u uw **[!UICONTROL Channel Configuration]** vormen en aangewezen **[!UICONTROL Execution Details]** bepalen. Zo kunt u definiëren:

* **het niveau van berichtlevering**: bijvoorbeeld, verzendend één bericht per ontvanger, zoals één enkele e-mail per individu.

* **het uitvoeringsadres**: het specifieke contactgebied dat voor het verzenden, zoals een e-mailadres of een telefoonaantal moet worden gebruikt.

U kunt als volgt de kanaalconfiguratie configureren:

1. Begin door uw **[!UICONTROL Channel configuration]** te maken en te configureren.

   U kunt ook een bestaande **[!UICONTROL Channel configuration]** bijwerken.

   ➡️ [&#x200B; volg de stappen die in deze pagina &#x200B;](../email/surface-personalization.md) worden gedetailleerd

1. Open vanuit de sectie **[!UICONTROL Execution details]** van uw **[!UICONTROL Channel configuration]** de tab **[!UICONTROL Orchestrated campaigns]** .

   ![](assets/target-dimension-3.png)

1. Klik op **[!UICONTROL Enabled]** om deze compatibel te maken met geordende campagnes.

1. Kies uw leveringsmethode:

   * **[!UICONTROL Target Dimension]**: verzenden naar de primaire entiteit, bijvoorbeeld de ontvanger.

   * **[!UICONTROL Target + Secondary Dimension]**: verzenden met zowel primaire als secundaire entiteiten, bijvoorbeeld ontvanger + contract.

1. Selecteer van drop-down uw [&#x200B; eerder gecreeerd Doel Dimension &#x200B;](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. Als u **[!UICONTROL Target + Secondary Dimension]** hebt geselecteerd als de leveringsmethode, kiest u een **[!UICONTROL Secondary Dimension]** om de context voor het verzenden van berichten te definiëren.

1. Kies onder de sectie **[!UICONTROL Execution Address]** welke **[!UICONTROL Source]** moet worden gebruikt om het bezorgadres op te halen, zoals het e-mailadres of telefoonnummer:

   * **[!UICONTROL Profile]**: selecteer deze optie als het bezorgingsadres, bijvoorbeeld e-mail, rechtstreeks in het hoofdprofiel van de klant wordt opgeslagen.

     Nuttig wanneer het verzenden van berichten naar de belangrijkste klant, niet een specifieke bijbehorende entiteit.

   * **[!UICONTROL Target Dimension]**: Kies deze optie als het bezorgadres is opgeslagen in de primaire entiteit, bijvoorbeeld een ontvanger.

     Nuttig wanneer elke ontvanger zijn eigen bezorgadres heeft, zoals een ander e-mailadres of telefoonnummer.

   * **[!UICONTROL Secondary Dimension]**: Wanneer u **[!UICONTROL Target + Secondary Dimension]** als leveringsmethode gebruikt, selecteert u de relevante **[!UICONTROL Secondary Dimension]** die u eerder hebt geconfigureerd.

     Als de secundaire dimensie bijvoorbeeld een boeking of abonnement vertegenwoordigt, kan het uitvoeringsadres, zoals een e-mail, van dat niveau worden genomen. Dit is handig wanneer profielen bij het boeken of abonneren op een service andere contactgegevens gebruiken.

1. Van het **[!UICONTROL Delivery address]** gebied, klik ![&#x200B; geef pictogram &#x200B;](assets/do-not-localize/edit.svg) uit om het specifieke gebied te kiezen voor uw berichtlevering te gebruiken.

   ![](assets/target-dimension-4.png)

1. Klik op **[!UICONTROL Submit]** wanneer dit is geconfigureerd.

Uw kanaal is nu klaar om met **Geordende Campagnes** te gebruiken, en de berichten zullen volgens de geselecteerde doeldimensie worden geleverd.

## Parameters voor URL-tracking {#url-tracking}

Wanneer u uw kanaalconfiguratie configureert, kunt u URL-volgparameters definiëren om de prestaties van uw e-mailcampagnes te controleren door metagegevens toe te voegen aan uw bijgehouden koppelingen - voor analytische en rapportagedoeleinden.

Hiervoor zijn contextafhankelijke kenmerken beschikbaar die specifiek zijn voor georkestreerde campagnes met de syntaxis `{{context.system.source.*}}` :

* **`context.system.source.id`**: geordende campagne-id
* **`context.system.source.name`**: geordende naam van de campagne
* **`context.system.source.versionId`**: ID geordende campagneversie
* **`context.system.source.actionId`**: ID van knooppunt voor kanaalhandeling
* **`context.system.source.actionName`**: naam van knooppunt voor kanaalhandeling
* **`context.system.source.channel`**: kanaaltype (E-mail, SMS, Push)
* **`context.system.IdentityNamespace`**: Naamruimte gebruikt

Bijvoorbeeld:

```
www.YourLandingURL.com?utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content={{context.system.source.actionName}}
```

Leer meer over URL het volgen parameters in [&#x200B; deze sectie &#x200B;](../email/url-tracking.md).
