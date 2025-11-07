---
solution: Journey Optimizer
product: journey optimizer
title: Audit van Journey Optimizer-bronnen
description: Leer hoe u acties kunt bijhouden die zijn uitgevoerd met Journey Optimizer-bronnen.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# Audit van Journey Optimizer-bronnen {#track-changes}

## Over auditlogboeken {#audit-logs}

>[!IMPORTANT]
>
>Als u het auditlogboek wilt weergeven en exporteren, moet u de machtiging **[!DNL View User Activity Log]** hebben verleend. [Meer informatie](../administration/ootb-product-profiles.md)

Met Journey Optimizer kunt u acties identificeren die door gebruikers in het systeem worden uitgevoerd op verschillende services en mogelijkheden, zoals reizen, berichten, landingspagina&#39;s enzovoort.

Dit staat u toe om de zichtbaarheid van activiteiten te verhogen die in het systeem worden uitgevoerd, kwesties problemen op te lossen, en uw zaken te helpen aan verordeningen en collectief beleid van het gegevensbeheer voldoen.

Elke actie wordt opgenomen met metagegevens in &quot;auditlogs&quot; die toegankelijk zijn in Adobe Experience Platform. Voor meer op controlelogboeken, met inbegrip van hoe te om hen in UI of API te bekijken en te beheren, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html).

![](assets/audit-logs.png)

## Gebeurtenistypen die zijn vastgelegd in auditlogboeken {#events}

In de volgende tabel wordt aangegeven op welke acties Journey Optimizer-bronnen worden opgenomen in auditlogboeken. De volledige lijst van acties die in de logboeken van de Controle worden gevangen is beschikbaar in [ documentatie van het Platform van de Ervaring van Adobe ](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html#category).

>[!NOTE]
>
>De logboeken van de controle met betrekking tot **besluitvormingsbeheer** zijn slechts zichtbaar van het Csv- dossier dat kan worden gedownload gebruikend de **[!UICONTROL Download log]** knoop.

| Bron | Actie |
|-----------|------------------|
| AJO-campagne | Maken/verwijderen/bijwerken/activeren/stoppen |
| Algemene instelling AJO-kanaal | Maken/verwijderen/bijwerken |
| AJO IP-pool | Maken/verwijderen/bijwerken |
| AJO-landingspagina | Maken/Verwijderen/Bijwerken/Publiceren/Publiceren ongedaan maken |
| AJO-landingspagina HTML-sjabloon | Maken/verwijderen/bijwerken |
| Voorinstelling AJO-bestemmingspagina | Maken/verwijderen/bijwerken |
| Subdomein AJO-landingspagina | Maken/verwijderen/bijwerken |
| AJO-berichtvoorinstelling | Maken/verwijderen/bijwerken |
| AJO PTR-record | Maken/verwijderen/bijwerken |
| Door AJO opgeslagen expressiesjabloon | Maken/verwijderen/bijwerken |
| AJO SMS API-gebruikersgegevens | Maken/verwijderen/bijwerken |
| AJO-subdomein | Maken/verwijderen/bijwerken |
| AJO-suppressielijst | CSV maken/verwijderen/downloaden |
| Veldgroepen | Maken/verwijderen/bijwerken |
| Reis | Maken/verwijderen/bijwerken/stoppen/publiceren |
| Aangepaste actie voor reizen | Maken/verwijderen/bijwerken |
| Gegevensbron voor reis | Maken/verwijderen/bijwerken |
| Journaal | Maken/verwijderen/bijwerken |
| Regel voor berichtfrequentie | Maken/verwijderen/bijwerken |
| Beoordelingsstrategie | Maken/verwijderen/bijwerken |
