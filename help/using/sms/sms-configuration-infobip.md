---
solution: Journey Optimizer
product: journey optimizer
title: Infobip-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten en MMS met Journey Optimizer met Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# Infobip-provider configureren {#sms-configuration-infobip}

Ga als volgt te werk om Infobip met Journey Optimizer te configureren:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw API-referenties, zoals hieronder wordt beschreven.

   * **[!UICONTROL SMS vendor]**: Infobip.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL API base URL]** en **[!UICONTROL API key]** : open de webinterfacehomepage of de API-sleutelbeheerpagina om uw referenties te zoeken. Leer meer in [ Documentatie Infobip ](https://www.infobip.com/docs/api) {target="_blank"}.

   * **[!UICONTROL Opt-In Keywords]** : voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **[!UICONTROL Opt-In Message]** activeren. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-In Message]** : voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-In Message]** wordt verzonden.

   * **[!UICONTROL Opt-Out Keywords]** : voer de standaardwaarde of trefwoorden in die de **[!UICONTROL Opt-Out Message]** automatisch activeren. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-Out Message]** : voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-Out Message]** wordt verzonden.

   * **[!UICONTROL Help Keywords]**: ga het gebrek of douanesleutelwoorden in die uw **Bericht van de Hulp** automatisch zullen teweegbrengen. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Help Message]**: ga de douanereactie in die automatisch als uw **Bericht van de Hulp** wordt verzonden.

   * **[!UICONTROL Double Opt-In Keywords]** : voer de trefwoorden in die het dubbele aanmeldingsproces activeren. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Double Opt-In Message]**: voer de aangepaste reactie in die automatisch wordt verzonden als reactie op de dubbele aanmeldingsbevestiging.

   * **[!UICONTROL Principal Entity ID]**: voer uw toegewezen belangrijkste entiteit-id van DLT in.

   * **[!UICONTROL Content Template ID]**: voer uw geregistreerde sjabloon-id voor DLT-inhoud in.

   * **[!UICONTROL Validity Period]** : voer de geldigheidsperiode van het bericht in uren in. Als berichten niet binnen deze termijn kunnen worden geleverd, zal het systeem extra pogingen doen om hen opnieuw te verzenden. De standaardgeldigheidsperiode is ingesteld op 48 uur.

   * **[!UICONTROL Callback Data]**: voer de aanvullende clientgegevens in die worden verzonden via de URL Waarschuwen.

   * **[!UICONTROL Inbound Number]**: voeg uw unieke binnenkomende aantal toe. Hierdoor kunt u dezelfde API-referenties gebruiken in verschillende sandboxen, elk met een eigen binnenkomend nummer.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor SMS- en MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
