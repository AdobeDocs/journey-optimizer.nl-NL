---
title: 'Het primaire e-mailadres wijzigen '
description: Leer hoe u kunt bepalen welk e-mailadres u moet gebruiken via de profielservice.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 59cba4086cd198a8be597a9971105569d5db2eee
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 6%

---

# De primaire adressen wijzigen {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Bepaal welk adres moet worden gebruikt"
>abstract="Wanneer verscheidene adressen in het gegevensbestand (persoonlijk, beroeps, enz.) beschikbaar zijn, kunt u kiezen welk adres om voor het verzenden voorrang te geven."

Wanneer u een profiel als doel instelt, zijn mogelijk verschillende e-mailadressen beschikbaar in de database (persoonlijk, professioneel e-mailadres, enz.).

Met [!DNL Journey Optimizer]kunt u bepalen welk e-mailadres u wilt gebruiken via de profielservice en u kunt opgeven wanneer meerdere adressen beschikbaar zijn. Volg de onderstaande stappen om dit te doen.

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]**.

   ![](assets/primary-address-execution-fields.png)

1. Het veld dat standaard wordt gebruikt om de e-mailadressen van de profielen te bepalen, wordt op dit scherm weergegeven. Klikken **[!UICONTROL Edit]** om deze te wijzigen.

   ![](assets/primary-address.png)

1. Klik op het huidige veld of op het bewerkingspictogram om een nieuw veld te selecteren.

   ![](assets/primary-address-edit.png)

1. De lijst met beschikbare XDM-velden van het e-mailtype wordt weergegeven. Selecteer het veld dat u wilt gebruiken.

   ![](assets/primary-address-field.png)

1. Klikken **[!UICONTROL Save]** om uw keuze te bevestigen.

   ![](assets/primary-address-save.png)

   Het uitvoeringsveld wordt bijgewerkt en wordt nu gebruikt als primair adres.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
