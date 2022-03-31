---
title: IP-pools maken
description: '"Leer hoe u ip-pools beheert"'
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# IP-pools maken {#create-ip-pools}

## Informatie over IP-pools {#about-ip-pools}

Met Journey Optimizer kunt u IP-pools maken om de IP-adressen van uw subdomeinen te groeperen.

Het maken van IP-pools wordt ten zeerste aanbevolen voor e-maillevering. Door dit te doen, kunt u de reputatie van subdomain verhinderen uw andere subdomeinen te beïnvloeden.

Bijvoorbeeld, moet één beste praktijk één IP pool voor uw marketing berichten, en een andere voor uw transactionele berichten hebben. Op deze manier, als een van uw marketingberichten slecht presteert en door een klant als spam wordt gedeclareerd, heeft dit geen invloed op de transactieberichten die naar dezelfde klant worden verzonden, die nog steeds transactionele berichten (aanschafbevestigingen, wachtwoordherstelberichten, enz.) zal ontvangen.

## Een IP-pool maken {#create-ip-pool}

Ga als volgt te werk om een IP-pool te maken:

1. Toegang krijgen tot **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** en klik vervolgens op **[!UICONTROL Create IP Pool]**.

   ![](assets/ip-pool-create.png)

1. Geef een naam en een beschrijving (optioneel) voor de IP-pool op.

   >[!NOTE]
   >
   >De naam van het subdomein moet beginnen met een letter (A-Z) en mag alleen alfanumerieke tekens of speciale tekens ( _, ., - ) bevatten.

1. Selecteer de IP adressen om in de pool van de drop-down lijst te omvatten, dan klik **[!UICONTROL Submit]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Alle IP adressen provisioned met uw instantie zijn beschikbaar in de lijst.

De IP pool wordt nu gecreeerd en toont in de lijst. U kunt deze selecteren voor toegang tot de eigenschappen en voor weergave van de bijbehorende berichtvoorinstelling. Voor meer op hoe te om een berichtvooraf ingesteld met een IP pool te associëren, verwijs naar [deze sectie](message-presets.md)).

![](assets/ip-pool-created.png)

## Een IP-pool bewerken {#edit-ip-pool}

Om een IP pool uit te geven:

1. Klik in de lijst op de naam van de IP-pool om deze te openen.

   ![](assets/ip-pool-list.png)

1. Bewerk de eigenschappen naar wens. U kunt de beschrijving wijzigen en IP-adressen toevoegen of verwijderen.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Ga met extra zorg te werk wanneer het overwegen van het schrappen van IP, aangezien dit extra lading op andere IPs zal zetten en ernstige gevolgen voor uw leverbaarheid kan hebben. Neem in geval van twijfel contact op met een leverancier.

1. Sla uw wijzigingen op.

>[!NOTE]
>
>De naam van de IP-pool kan niet worden bewerkt. Als u het wilt wijzigen, moet u de IP pool schrappen en een andere met de naam van uw keus creëren.

De update is onmiddellijk of asynchroon van kracht, afhankelijk van de IP pool die aan een wordt geassocieerd [berichtvoorinstelling](message-presets.md) of niet:

* Als de IP pool is **niet** geselecteerd in een berichtvoorinstelling, wordt de update onmiddellijk uitgevoerd (**[!UICONTROL Success]** status).
* Als de IP pool **is** geselecteerd in een berichtvoorinstelling, kan de update 7 tot 10 werkdagen duren (**[!UICONTROL Processing]** status).

Als u de updatestatus van de IP-pool wilt controleren, klikt u op de knop **[!UICONTROL More actions]** en selecteert u **[!UICONTROL Recent updates]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Zodra een IP Groep met succes wordt bijgewerkt, kunt u moeten wachten:
>* een paar minuten voordat het wordt verbruikt door de eenheidspublicaties,
>* tot de volgende partij voor de IP pool om in partijberichten efficiënt te zijn.


U kunt ook de opdracht **[!UICONTROL Delete]** knoop om een IP pool te schrappen. U kunt geen IP-pool verwijderen die is gekoppeld aan een berichtvoorinstelling.
