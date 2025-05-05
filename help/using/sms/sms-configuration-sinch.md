---
solution: Journey Optimizer
product: journey optimizer
title: Sinch-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer met Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 1%

---

# Sinch-provider configureren {#sms-configuration-sinch}

Wanneer u de Sinch-provider gebruikt met Journey Optimizer, kunt u twee verschillende opties vinden:

* **Configuratie van SMS**: Opstelling uw geloofsbrieven van Sinch API om de berichten van SMS foutloos te verzenden.

* **Configuratie MMS**: Voor het overseinen van verschillende media (MMS), vorm uw Inch MMS API geloofsbrieven. Merk op dat het volgen en het antwoorden aan binnenkomende berichten, door de configuratie van SMS worden behandeld. De opstelling MMS is slechts voor uitgaande levering van het MMS bericht.

## Inloggegevens van de API{#create-api}

Voer de volgende stappen uit om uw Sinch-provider te configureren voor het verzenden van SMS-berichten en MMS met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** `>` **[!UICONTROL SMS Settings]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

+++ Lijst met SMS-referenties voor configuratie

   | Configuratievelden | Beschrijving |
   |---|---|    
   | SMS-leverancier | Sinch |
   | Naam | Kies een naam voor uw API-referentie. |
   | Service-id en API-token | Open de pagina met API&#39;s en je kunt je gegevens vinden op het tabblad SMS. Leer meer in [ de Documentatie van de Sinch ](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"} . |
   | Trefwoorden bij Inschakelen | Voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw aanmeldingsbericht activeren. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden. |
   | Bericht bij aanmelden | Voer de aangepaste reactie in die automatisch wordt verzonden als uw aanmeldingsbericht. |
   | Trefwoorden uitschakelen | Voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch het bericht Uitschakelen activeren. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden. |
   | Bericht bij Afmelden | Voer de aangepaste reactie in die automatisch wordt verzonden als uw bericht om te weigeren. |
   | Trefwoorden Help | Ga het gebrek of douanetrefwoorden in die automatisch uw **Bericht van de Hulp** zullen teweegbrengen. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden. |
   | Help-bericht | Ga de douanereactie in die automatisch als uw **Bericht van de Hulp** wordt verzonden. |
   | Dubbele invoegtrefwoorden | Voer de trefwoorden in die het dubbele aanmeldingsproces activeren. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden. [ Leer meer over SMS Dubbelopt-binnen ](https://video.tv.adobe.com/v/3427129/?learn=on). |
   | Dubbel bericht voor aanmelden | Voer de aangepaste reactie in die automatisch wordt verzonden als reactie op de dubbele aanmeldingsbevestiging. |
   | Inkomend getal | Voeg uw unieke binnenkomende aantal of korte code toe. Hierdoor kunt u dezelfde API-referenties gebruiken in verschillende sandboxen, elk met een eigen binnenkomend nummer of korte code. |
   | Aangepaste binnenkomende trefwoorden | Definieer unieke trefwoorden voor specifieke acties, zoals KORTING, AANBIEDINGEN, ENROLL. Deze trefwoorden worden vastgelegd en opgeslagen als kenmerken in het profiel, zodat u een kwalificatie voor een streaming segment op de reis kunt activeren en een aangepaste reactie of actie kunt leveren. |
   | Standaardbericht voor binnenkomende reactie | Ga het standaardantwoord in dat wordt verzonden wanneer een eindgebruiker binnenkomende SMS verzendt die om het even welke bepaalde sleutelwoorden niet aanpast. |
   | URL overschrijven | Voer uw aangepaste URL in ter vervanging van de standaardeindpunten voor SMS-leveringsrapporten, feedbackgegevens, binnenkomende berichten of gebeurtenismeldingen. Sinch verzendt alle relevante updates naar deze URL in plaats van de vooraf gedefinieerde. |

+++

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor SMS-berichten maken. [Meer informatie](sms-configuration-surface.md)

## Referenties voor MMS API instellen {#sinch-mms}

>[!IMPORTANT]
>
> Samen met de opstelling MMS, moet u ook de geloofsbrieven van Sinch API tot stand brengen specifiek voor het volgen van binnenkomende berichten en het beheren van toestemmingsverzoeken.

Voer de volgende stappen uit om Sinch MMS te configureren voor het verzenden van MMS met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** `>` **[!UICONTROL SMS Settings]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw MMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL SMS vendor]**: Sinch MMS.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Project ID]** , **[!UICONTROL App ID]** en **[!UICONTROL API Token]** : volg de onderstaande stappen om uw MMS API-referenties te verzamelen.

      * Voor **[!UICONTROL Project ID]** en **[!UICONTROL App ID]**: Heb toegang tot de [ API van de Gesprek - overzicht ](https://dashboard.sinch.com/convapi/overview) pagina van uw project van Sinch op uw Staaldashboard.
      * Voor **[!UICONTROL API Token]**: Verkrijg de [ sleutels van de Toegang ](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) voor uw Project van de Sinch en produceer a **Base64 API Symbolisch** uit uw Duidelijke Sleutels van de Toegang van het Project **&#x200B;**.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
