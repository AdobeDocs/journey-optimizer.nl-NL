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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 7d7c1b72530d99b8cceb1067f2576ad66c0052a6
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# IP-pools maken

## Informatie over IP-pools {#about-ip-pools}

Met Journey Optimizer kunt u IP-pools maken om de IP-adressen van uw subdomeinen te groeperen.

Het maken van IP-pools wordt ten zeerste aanbevolen voor e-maillevering. Door dit te doen, kunt u de reputatie van subdomain verhinderen uw andere subdomeinen te beïnvloeden.

Bijvoorbeeld, moet één beste praktijk één IP pool voor uw marketing berichten, en een andere voor uw transactionele berichten hebben. Op deze manier, als een van uw marketingberichten slecht presteert en door een klant als spam wordt gedeclareerd, heeft dit geen invloed op de transactieberichten die naar dezelfde klant worden verzonden, die nog steeds transactionele berichten (aanschafbevestigingen, wachtwoordherstelberichten, enz.) zal ontvangen.

## Een IP-pool maken {#create-ip-pool}

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

## Een IP-pool bewerken {#edit-ip-pool}

Om een IP pool uit te geven:

1. Klik in de lijst op de naam van de IP-pool om deze te openen.

   ![](../assets/ip-pool-list.png)

1. Bewerk de eigenschappen naar wens. U kunt de beschrijving wijzigen en IP-adressen toevoegen of verwijderen.

   ![](../assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Ga met extra zorg te werk wanneer het overwegen van het schrappen van IP, aangezien dit extra lading op andere IPs zal zetten en ernstige gevolgen voor uw leverbaarheid kan hebben. Neem in geval van twijfel contact op met een leverancier.

1. Sla uw wijzigingen op.

>[!NOTE]
>
>De naam van de IP-pool kan niet worden bewerkt. Als u het wilt wijzigen, moet u de IP pool schrappen en een andere met de naam van uw keus creëren.

De update is onmiddellijk of asynchroon van kracht, afhankelijk van de IP pool die aan een [bericht vooraf ingesteld](message-presets.md) of niet wordt geassocieerd:

* Als de IP-pool **niet** is geselecteerd in een berichtvoorinstelling, is de update onmiddellijk (**[!UICONTROL Success]** status).
* Als de IP-pool **is** geselecteerd in een berichtvoorinstelling, kan de update 7-10 werkdagen duren (**[!UICONTROL Processing]** status).

<!--If a message preset has been associated with the IP pool, you first need to remove it before editing the IP pool. Once the your modifications have been done, you can associate the message preset again.-->

Om de IP status van de poolupdate te controleren, klik **[!UICONTROL More actions]** knoop en selecteer **[!UICONTROL Recent updates]**.

![](../assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Zodra een IP Groep met succes wordt bijgewerkt, kunt u moeten wachten:
>* een paar minuten voordat het wordt verbruikt door de eenheidspublicaties,
>* tot de volgende partij voor de IP pool om in partijberichten efficiënt te zijn.


U kunt de **[!UICONTROL Delete]** knoop ook gebruiken om een IP pool te schrappen. U kunt geen IP-pool verwijderen die is gekoppeld aan een berichtvoorinstelling.

