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
source-git-commit: fc12ee65fc773c70b88504a951e5f5c5b2b3b0e6
workflow-type: tm+mt
source-wordcount: '581'
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

In dat geval gebruikt [!DNL Journey Optimizer] **[!UICONTROL Execution fields]** om te bepalen welk e-mailadres of telefoonnummer bij voorrang van de profielservice moet worden gebruikt.

Als u de velden wilt controleren die standaard worden gebruikt, opent u het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Executions fields]** .

![](assets/primary-address-execution-fields.png)

>[!NOTE]
>
>De gebieden van de uitvoering zijn beschikbaar voor de kanalen van e-mail en van SMS.

De huidige waarden worden gebruikt voor alle leveringen op sandboxniveau. U kunt deze velden zo nodig bijwerken.

In de meeste gevallen wijzigt u een uitvoeringsveld globaal en definieert u een waarde die moet worden gebruikt voor alle e-mail- of SMS-berichten. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## De beheerinstellingen bijwerken {#admin-settings}

Voer de onderstaande stappen uit om de uitvoeringsvelden globaal op sandboxniveau te wijzigen.

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Executions fields]** .

1. Klik op **[!UICONTROL Edit]** om de standaardwaarden te wijzigen.

   ![](assets/primary-address.png)

1. Klik op het huidige veld van uw keuze of op het pictogram Bewerken om een nieuw veld te selecteren.

   ![](assets/primary-address-edit.png)

1. De lijst met beschikbare XDM-velden van het e-mailtype wordt weergegeven. Selecteer het te gebruiken veld.

   ![](assets/primary-address-select-field.png)

1. Klik op **[!UICONTROL Save]** om uw keuze te bevestigen.

Het uitvoeringsveld wordt bijgewerkt en wordt nu gebruikt als primair adres.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## Het standaarduitvoeringsveld in de reisparameters overschrijven {#override-execution-address-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="Een aangepaste waarde definiëren"
>abstract="In sommige specifieke gevallen kunt u het standaardadres voor uitvoering overschrijven. Gebruik **toelaten parameteropheffing** pictogram rechts van het gebied om een douane primair adres te bepalen."
>additional-url="https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/configuration/primary-email-addresses#journey-parameters" text="Het uitvoeringsadres"

Voor specifieke gebruiksgevallen kunt u het uitvoeringsveld dat globaal is ingesteld negeren en een andere waarde definiëren op het niveau van de reis.

Het overschrijven van deze waarde kan bijvoorbeeld nuttig zijn om:

* Test een e-mailbericht. U kunt uw eigen e-mailadres toevoegen: nadat u de reis hebt gepubliceerd, wordt het e-mailbericht naar u verzonden.
* Stuur een e-mail naar de abonnees van een lijst. Leer meer in [&#x200B; dit gebruiksgeval &#x200B;](../building-journeys/message-to-subscribers-uc.md).

Wanneer het toevoegen van een **[!UICONTROL Email]** of **[!UICONTROL SMS]** actie aan a [&#x200B; reis &#x200B;](../email/create-email.md#create-email-journey-campaign), wordt het primaire e-mailadres getoond onder de reis geavanceerde parameters.

Overschrijf deze waarde met het pictogram **[!UICONTROL Enable parameter override]** rechts van het veld.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>Overschrijven van e-mailadressen mag alleen worden gebruikt voor specifieke gebruiksgevallen. Meestal hoeft u het e-mailadres niet te wijzigen, omdat de waarde die wordt gedefinieerd als het primaire adres in de **[!UICONTROL Execution fields]** het adres is dat moet worden gebruikt.

## Het standaard uitvoeringsveld in de kanaalconfiguratie overschrijven {#override-execution-address-channel-config}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="Het standaard te gebruiken uitvoeringsadres overschrijven"
>abstract="Als er meerdere e-mailadressen of telefoonnummers beschikbaar zijn in de database (persoonlijk, professioneel, enz.), kunt u aangeven welke prioriteit u wilt geven aan het verzenden. Het primaire adres wordt bepaald op het zandbakniveau, maar hier kunt u het gebrek met voeten treden dat voor deze specifieke kanaalconfiguratie plaatst."

U kunt het standaarduitvoeringsadres voor een specifieke e-mail of een sms [&#x200B; kanaalconfiguratie &#x200B;](channel-surfaces.md) veranderen.

Ga hiertoe naar de sectie **[!UICONTROL Execution dimension]** en bewerk het veld onder **[!UICONTROL Execution Address]** .

![](assets/sms-config-execution-address.png){width=85%}

Selecteer vervolgens een item in de lijst met beschikbare XDM-velden van het e-mailtype.

![](assets/sms-config-execution-field.png)

Het uitvoeringsgebied wordt bijgewerkt en dan gebruikt als primair adres voor de campagnes of de reizen gebruikend deze kanaalconfiguratie. Het treedt het [&#x200B; algemene plaatsen &#x200B;](#admin-settings) met voeten die op het zandbakniveau wordt bepaald.

<!--[Learn more on the execution address in the email configuration ](../email/email-settings.md#execution-address)-->
