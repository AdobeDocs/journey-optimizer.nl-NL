---
solution: Journey Optimizer
product: journey optimizer
title: Infobip-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten en MMS met Journey Optimizer met Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '420'
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

   * **[!UICONTROL Custom Inbound Keywords]**: definieer unieke trefwoorden voor specifieke acties, zoals KORTING, AANBIEDINGEN, ENROLL. Deze trefwoorden worden vastgelegd en opgeslagen als kenmerken in het profiel, zodat u een kwalificatie voor een streaming segment op de reis kunt activeren en een aangepaste reactie of actie kunt leveren.

   * **[!UICONTROL Default Inbound Reply Message]**: voer het standaardantwoord in dat wordt verzonden wanneer een eindgebruiker een binnenkomend SMS-bericht verzendt dat niet overeenkomt met een van de gedefinieerde trefwoorden.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor SMS- en MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
