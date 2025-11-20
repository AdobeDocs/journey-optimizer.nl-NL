---
solution: Journey Optimizer
product: journey optimizer
title: Een campagne bekijken en activeren
description: Meer informatie over het reviseren en activeren van campagnes in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campagne, revisie, validatie, activering, activering, optimaliseren
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 8cb37cf0fb9dc8048d7da8ddda0c67280477d57f
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# Een door API geactiveerde campagne uitvoeren {#execute}

Nadat de campagne is geactiveerd, moet u het gegenereerde voorbeeld-cURL-verzoek ophalen en deze in de API gebruiken om de payload te bouwen en de campagne te starten.

## Lees hier meer {#must-read}

* **begin/einddata van de Campagne** - als u een specifieke begin en/of einddatum toen het creëren van de campagne hebt gevormd, zal het niet buiten deze data worden uitgevoerd, en API vraag zal ontbreken.

* **onderbreking van de Vraag** - de vraag aan de Interactieve REST API van de Uitvoering van het Bericht heeft een onderbreking van 60 sec. In het geval van onverwachte onderbrekingen zijn er echter interne herpogingen beschikbaar om de levering te garanderen.

## De campagne activeren {#trigger}

1. Open de campagne en kopieer en plak vervolgens het laadverzoek vanuit de sectie **[!UICONTROL cURL request]** . Deze nuttige lading omvat alle verpersoonlijkings (profiel en context) variabelen die in het bericht worden gebruikt. Het is beschikbaar zodra de campagne live is.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >De eindpunten in de cURL- sectie verschillen tussen standaard en [&#x200B; Hoge productie campigns &#x200B;](../campaigns/api-triggered-high-throughput.md).

1. Gebruik dit cURL-verzoek in de API&#39;s om de payload te bouwen en de campagne te starten. Voor meer informatie, verwijs naar de [&#x200B; Interactieve documentatie van API van de Uitvoering van het Bericht &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution), waar alle eindpunten voor standaard en Hoge productie campagnes worden vermeld.

   API vraagvoorbeelden zijn ook beschikbaar op [&#x200B; deze pagina &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

## Problemen oplossen {#troubleshooting}

### Azure Cosmos DB-verificatiefouten (500 Interne serverfout) {#cosmosdb-auth-errors}

Als u **500 Interne Fouten van de Server** ontmoet wanneer het teweegbrengen van API-teweeggebrachte campagnes, en de systeemlogboeken a **403 Verboden** fout van Azure Cosmos- OB met een bericht zoals:

_&quot;De toegang tot uw rekening wordt momenteel ingetrokken omdat de Azure Cosmos DB-service het AAD-verificatietoken voor de standaardidentiteit van de account niet kan verkrijgen&quot;_

Deze fout komt typisch voor wanneer de Azure dienstHoofd die voor de authentificatie van Cosmos DB wordt vereist is onbruikbaar gemaakt, geschrapt, of misconfigured.

+++Hoe kan ik dit probleem oplossen?

1. **verifieer uw Azure de diensthoofd** - zorg ervoor dat uw Azure de diensthoofd of beheerde identiteit wordt toegelaten en niet gehandicapt of in uw Azure Actieve Folder geschrapt is.

1. **de toestemmingen van de Controle** - Bevestig dat het de diensthoofd de noodzakelijke toestemmingen heeft om tot de middelen van Azure Key Vault en van DB Cosmos toegang te hebben. De dienst principal moet aangewezen roltaken hebben om met Azure Cosmos DB voor authentiek te verklaren.

1. **de configuratie van Coosmos DB CMK van 0&rbrace; van het Overzicht Azure Cosmos- Configuratie CMK - als u Klant-Beheerde Sleutels (CMK) gebruikt, raadpleeg de** Azure het oplossen van problemengids van Cosmos DB CMK [&#x200B; voor gedetailleerde stappen om AAD symbolische aankoop te herstellen.](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"}

1. **re-laat en test** toe - na het verbeteren van de configuratie, re-laat het de diensthoofd toe als het onbruikbaar werd gemaakt, en test uw transactie API vraag opnieuw om te bevestigen dat de authentificatie slaagt en de berichten worden geleverd.

>[!NOTE]
>
>Deze kwestie wordt typisch veroorzaakt door een misconfiguration of toevallig het onbruikbaar maken van de Azure dienstHoofd die voor de authentificatie van DB Cosmos wordt vereist. Het houden van het de diensthoofd toegelaten en behoorlijk gevormd zal deze fout in de toekomst verhinderen.

+++
