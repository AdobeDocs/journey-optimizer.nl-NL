---
solution: Journey Optimizer
product: journey optimizer
title: De uitvoeringsadressen wijzigen
description: Leer hoe u kunt bepalen welk e-mailadres u moet gebruiken via de profielservice.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: primair, uitvoeren, e-mail, doel, profiel, optimaliseer
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# De uitvoeringsadressen wijzigen {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Bepaal welk adres moet worden gebruikt"
>abstract="Als er meerdere e-mailadressen of telefoonnummers beschikbaar zijn in de database (persoonlijk, professioneel, enz.), kunt u aangeven welke prioriteit u wilt geven aan het verzenden."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Bepaal welk adres moet worden gebruikt"
>abstract="Bewerk de velden die worden gebruikt om het e-mailadres of telefoonnummer van het profiel te bepalen waaraan prioriteit moet worden gegeven bij het verzenden."

Wanneer u een profiel als doel instelt, zijn mogelijk verschillende e-mailadressen of telefoonnummers beschikbaar in de database (professioneel e-mailadres, persoonlijk telefoonnummer, enz.).

In dat geval [!DNL Journey Optimizer] gebruik **[!UICONTROL Execution fields]** om te bepalen welk e-mailadres of telefoonnummer bij voorrang van de profielservice moet worden gebruikt.

Als u de velden wilt controleren die standaard worden gebruikt, gaat u naar de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]** -menu.

![](assets/primary-address-execution-fields.png)

De huidige waarden worden gebruikt voor alle leveringen op sandboxniveau. U kunt deze velden zo nodig bijwerken.

In de meeste gevallen wijzigt u een uitvoeringsveld globaal en definieert u een waarde die moet worden gebruikt voor alle e-mail- of SMS-berichten. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## De beheerinstellingen bijwerken {#admin-settings}

Voer de onderstaande stappen uit om de uitvoeringsvelden globaal op sandboxniveau te wijzigen.

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]**.

1. Klikken **[!UICONTROL Edit]** de standaardwaarden wijzigen.

   ![](assets/primary-address.png)

1. Klik op het huidige veld van uw keuze of op het pictogram Bewerken om een nieuw veld te selecteren.

   ![](assets/primary-address-edit.png)

1. De lijst met beschikbare XDM-velden van het e-mailtype wordt weergegeven. Selecteer het te gebruiken veld.

   ![](assets/primary-address-select-field.png)

1. Klikken **[!UICONTROL Save]** om uw keuze te bevestigen.

Het uitvoeringsveld wordt bijgewerkt en wordt nu gebruikt als primair adres.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## Een waarde in de parameters van de rit overschrijven {#journey-parameters}

Alleen voor specifieke gebruiksgevallen kunt u het uitvoeringsveld dat globaal is ingesteld negeren en een andere waarde definiëren op het niveau van de reis, met name voor het e-mailkanaal.

Wanneer u een **[!UICONTROL Email]** een handeling [reis](../email/create-email.md#create-email-journey-campaign), wordt het primaire e-mailadres weergegeven onder de geavanceerde parameters voor de reis.

In bepaalde specifieke contexten kunt u deze waarde overschrijven met de opdracht **[!UICONTROL Enable parameter override]** pictogram rechts van **[!UICONTROL address]** veld.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>Overschrijven van e-mailadressen mag alleen worden gebruikt voor specifieke gebruiksgevallen. Meestal hoeft u het e-mailadres niet te wijzigen omdat de waarde die in het dialoogvenster **[!UICONTROL Execution fields]** Dat is de methode die moet worden gebruikt.

Het overschrijven van deze waarde kan bijvoorbeeld nuttig zijn om:

* Test een e-mailbericht. U kunt uw eigen e-mailadres toevoegen: nadat u de reis hebt gepubliceerd, wordt het e-mailbericht naar u verzonden.
* Stuur een e-mail naar de abonnees van een lijst. Meer informatie in [dit geval gebruiken](../building-journeys/message-to-subscribers-uc.md).
