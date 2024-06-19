---
solution: Journey Optimizer
product: journey optimizer
title: Infobip-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten en MMS met Journey Optimizer met Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# Infobip-provider configureren {#sms-configuration-infobip}

Ga als volgt te werk om Infobip met Journey Optimizer te configureren:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]** en selecteert u de **[!UICONTROL API Credentials]** -menu. Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw API-referenties, zoals hieronder wordt beschreven.

   * **[!UICONTROL SMS vendor]**: Infobip.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL API base URL]** en **[!UICONTROL API key]**: ga naar de startpagina van uw webinterface of de API-sleutelbeheerpagina om uw referenties te zoeken. Meer informatie in [Infobip-documentatie](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Opt-In Keywords]**: voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **[!UICONTROL Opt-In Message]**. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-In Message]**: voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-In Message]**.

   * **[!UICONTROL Opt-Out Keywords]**: voer de standaardwaarde of trefwoorden in die automatisch uw **[!UICONTROL Opt-Out Message]**. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-Out Message]**: voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-Out Message]**.

   * **[!UICONTROL Help Keywords]**: voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **Help-bericht**. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Help Message]**: voer de aangepaste reactie in die automatisch als uw **Help-bericht**.

   * **[!UICONTROL Double Opt-In Keywords]**: voer de trefwoorden in die het dubbele aanmeldingsproces activeren. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Double Opt-In Message]**: voer de aangepaste reactie in die automatisch wordt verzonden als antwoord op de dubbele aanmeldingsbevestiging.

   * **[!UICONTROL Principal Entity ID]**: voer de toegewezen DLT-hoofd-id in.

   * **[!UICONTROL Content Template ID]**: voer uw geregistreerde sjabloon-id voor DLT-inhoud in.

   * **[!UICONTROL Validity Period]**: voer de geldigheidsperiode van het bericht in uren in. Als berichten niet binnen deze termijn kunnen worden geleverd, zal het systeem extra pogingen doen om hen opnieuw te verzenden. De standaardgeldigheidsperiode is ingesteld op 48 uur.

   * **[!UICONTROL Callback Data]**: voer de aanvullende clientgegevens in die worden verzonden via de URL Waarschuwen.

   * **[!UICONTROL Inbound Number]**: voeg uw unieke binnenkomende nummer toe. Hierdoor kunt u dezelfde API-referenties gebruiken in verschillende sandboxen, elk met een eigen binnenkomend nummer.

1. Klikken **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak voor SMS- en MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
