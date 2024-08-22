---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Aan de slag voor systeembeheer
description: Als systeembeheerder, leer meer hoe te om met Journey Optimizer te werken
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 1%

---

# Aan de slag voor systeembeheerders {#get-started-sys-admins}

Voordat u [!DNL Adobe Journey Optimizer] gaat gebruiken, moet u de omgeving in verschillende stappen voorbereiden.  U moet deze stappen uitvoeren zodat de [ Ingenieur van Gegevens ](data-engineer.md) en [ Praktijk van de Reis ](marketer.md) met [!DNL Adobe Journey Optimizer] kan beginnen te werken.


Als Beheerder van het a **Systeem**, moet u **productprofielen begrijpen en toestemmingen** voor zandbakbeleid en kanaalconfiguratie toewijzen. U moet ook een of meer sandboxen instellen en deze beheren voor de beschikbare productprofielen. Vervolgens kunt u teamleden toewijzen aan productprofielen.

Deze mogelijkheden kunnen worden beheerd door **[!UICONTROL Product administrators]** die toegang hebben tot de beheerconsole. [ leer meer over Adobe Admin Console ](https://helpx.adobe.com/nl/enterprise/admin-guide.html) {target="_blank"}.

Meer informatie over toegangsbeheer vindt u op de volgende pagina&#39;s:

1. **creeer zandbakken** om uw instanties in afzonderlijke, geïsoleerde virtuele milieu&#39;s te verdelen. **Sandboxes** wordt gecreeerd in [!DNL Journey Optimizer]. Leer meer in de [ zandbakken ](../../administration/sandboxes.md) sectie.

   >[!NOTE]
   >Als Beheerder van het a **Systeem**, als u niet het **[!UICONTROL Sandboxes]** menu in [!DNL Journey Optimizer] ziet, werk uw toestemmingen in de [ Admin Console ](https://adminconsole.adobe.com/) {target="_blank"} bij. Leer hoe te om uw productprofiel in [ bij te werken deze pagina ](../../administration/permissions.md#edit-product-profile).
   >

1. **Begrijp productprofielen**. Productprofielen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Leer meer in de [ uit-van-de-doos productprofielen ](../../administration/ootb-product-profiles.md) sectie.

1. **plaats toestemmingen** voor productprofielen, met inbegrip van **Sandboxes**, en geef toegang tot uw teamleden door hen aan verschillende productprofielen toe te wijzen. Deze stap wordt uitgevoerd in de [ Admin Console ](https://adminconsole.adobe.com/) {target="_blank"}. Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die aan **[!UICONTROL Product profile]** zijn toegewezen. Elke toestemming wordt verzameld onder mogelijkheden, bijvoorbeeld Reis of Aanbiedingen, die de verschillende functionaliteiten of voorwerpen in [!DNL Journey Optimizer] vertegenwoordigen. Leer meer in de [ niveaus van de Toestemming ](../../administration/high-low-permissions.md) sectie.

Bovendien moet u gebruikers toevoegen die toegang tot Assets Essentials aan de **Gebruikers van de Assets Essentials Consumenten** of **gebruikers van Assets Essentials** de profielen van het Product nodig hebben. [ las meer in de documentatie van Assets Essentials ](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html) {target="_blank"}.

>[!NOTE]
>Voor Journey Optimizer-producten die zijn verkregen vóór 6 januari 2022, moet u [!DNL Adobe Experience Manager Assets Essentials] implementeren voor uw organisatie. Leer meer in [ opstellen Assets Essentials ](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html) {target="_blank"} sectie.

Wanneer u [!DNL Journey Optimizer] voor het eerst opent, beschikt u over een productiesandbox en kunt u een bepaald aantal IP&#39;s toewijzen, afhankelijk van uw contract.

Om uw reizen te kunnen tot stand brengen en berichten te verzenden, heb toegang tot het **menu van het BEHEER**. Blader in het menu **[!UICONTROL Channels]** om uw berichten en kanaalconfiguraties (d.w.z. voorinstellingen voor berichten) te configureren.

>[!NOTE]
>Als Beheerder van het a **Systeem**, als u niet het **[!UICONTROL Channels]** menu in [!DNL Journey Optimizer] ziet, werk uw toestemmingen in de [ Admin Console ](https://adminconsole.adobe.com/) {target="_blank"} bij. Leer hoe te om uw productprofiel in [ bij te werken deze pagina ](../../administration/permissions.md#edit-product-profile).
>

Voer de onderstaande stappen uit:

1. **vorm berichten en kanalen**: bepaal configuraties, pas en pas e-mail, sms en duw berichtmontages aan

   * Bepaal **duw berichten montages** in zowel [!DNL Adobe Experience Platform] als [!DNL Adobe Experience Platform Launch]. [Meer informatie](../../push/push-gs.md)

   * Creeer **kanaalconfiguraties** (d.w.z. voorinstellingen van het bericht) om alle technische parameters te vormen die voor e-mail, sms en duw bericht worden vereist. [Meer informatie](../../configuration/channel-surfaces.md)

   * Vorm het **kanaal van SMS** om alle technische parameters te vormen die voor SMS worden vereist. [Meer informatie](../../sms/sms-configuration.md)

   * Beheer het aantal dagen waarin **opnieuw probeert** alvorens e-mailadressen naar de onderdrukkingslijst te verzenden wordt uitgevoerd. [Meer informatie](../../configuration/manage-suppression-list.md)

1. **Afgevaardigde subdomeinen**: voor om het even welk nieuw subdomain dat in Journey Optimizer moet worden gebruikt, zal de eerste stap het moeten afvaardigen. [Meer informatie](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **creeer IP pools**: verbeter uw e-mailleverbaarheid en reputatie door IP adressen te groeperen die met uw instantie worden voorzien. [Meer informatie](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **beheert de onderdrukking en de lijsten van gewenste personen**: verbeter uw leveringsbaarheid met onderdrukking en lijsten van gewenste personen

   * A [ suppressielijst ](../../reports/suppression-list.md) bestaat uit e-mailadressen die u van uw leveringen wilt uitsluiten, omdat het verzenden naar deze contacten uw verzendende reputatie en leveringspercentages zou kunnen kwetsen. U kunt alle e-mailadressen controleren die automatisch van het verzenden in een reis, zoals ongeldige adressen worden uitgesloten, adressen die constant elektronische stuiteren, en uw e-mailreputatie, en ontvangers die een spamklacht van één of andere soort tegen één van uw e-mailberichten negatief zouden kunnen beïnvloeden. Leer hoe te om de [ suppressielijst ](../../configuration/manage-suppression-list.md) te beheren en [ opnieuw probeert ](../../configuration/retries.md).

   ![](../assets/suppression-list-filtering-example.png)

   * De [ lijst van gewenste personen ](../../configuration/allow-list.md) laat u toe om individuele e-mailadressen of domeinen te specificeren die de enige ontvangers of domeinen zullen zijn die worden gemachtigd om de e-mails te ontvangen u van een specifieke zandbak verzendt. Dit kan voorkomen dat u per ongeluk e-mailberichten naar de adressen van de echte klant stuurt wanneer u zich in een testomgeving bevindt. Leer hoe te [ om de lijst van gewenste personen ](../../configuration/allow-list.md) toe te laten.

   Leer meer over leveringsbaarheidsbeheer in [!DNL Adobe Journey Optimizer] [ in deze pagina ](../../reports/deliverability.md).
