---
title: IP-pools maken
description: '"Leer hoe u ip-pools beheert"'
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Applicatie-instellingen
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# IP-pools maken

## Informatie over IP-pools

Met Journey Optimizer kunt u IP-pools maken om de IP-adressen van uw subdomeinen te groeperen.

Het maken van IP-pools wordt ten zeerste aanbevolen voor e-maillevering. Door dit te doen, kunt u de reputatie van subdomain verhinderen uw andere subdomeinen te beïnvloeden.

Bijvoorbeeld, moet één beste praktijk één IP pool voor uw marketing berichten, en een andere voor uw transactionele berichten hebben. Deze manier, als één van uw marketing berichten slecht presteert en als spam door een klant wordt verklaard, zal dit niet de transactionele berichten beïnvloeden die naar deze zelfde klant worden verzonden, die nog transactionele berichten (koopbevestigingen, wachtwoordterugwinningsberichten etc.) zullen ontvangen.

## Een IP-pool maken

Ga als volgt te werk om een IP-pool te maken:

1. Open het menu **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** en klik vervolgens op **[!UICONTROL Create IP Pool]**.

   ![](../assets/ip-pool-create.png)

1. Geef een naam en een beschrijving (optioneel) voor de IP-pool op.

   >[!NOTE]
   >
   >De naam van het subdomein moet beginnen met een letter (A-Z) en mag alleen alfanumerieke tekens of speciale tekens ( _, ., - ) bevatten.

1. Selecteer de IP adressen om in de pool van de drop-down lijst te omvatten, dan klik **[!UICONTROL Submit]**.

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Alle IP adressen provisioned met uw instantie zijn beschikbaar in de lijst.

De IP pool wordt nu gecreeerd en toont in de lijst. U kunt deze selecteren voor toegang tot de eigenschappen en voor weergave van de bijbehorende berichtvoorinstelling. Voor meer op hoe te om een bericht vooraf ingesteld met een IP pool te associëren, verwijs naar [deze sectie](message-presets.md)).

![](../assets/ip-pool-created.png)

Om een IP pool uit te geven, open het, dan geef zijn eigenschappen uit zoals gewenst.

>[!NOTE]
>
>Als een berichtvoorinstelling aan de IP-pool is gekoppeld, moet u deze eerst verwijderen voordat u de IP-pool kunt bewerken. Nadat u de wijzigingen hebt aangebracht, kunt u de berichtvoorinstelling opnieuw koppelen.
