---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Aan de slag voor systeembeheer
description: Als systeembeheerder, leer meer hoe te om met Journey Optimizer te werken
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 6c73a1ee024ca61b30d71e77268e51b93576ae62
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 1%

---

# Aan de slag voor systeembeheerders {#get-started-sys-admins}

Voordat u [!DNL Adobe Journey Optimizer] gaat gebruiken, moet u de omgeving in verschillende stappen voorbereiden.  U moet deze stappen uitvoeren zodat de [ Ingenieur van Gegevens ](data-engineer.md) en [ Praktijk van de Reis ](marketer.md) met [!DNL Adobe Journey Optimizer] kan beginnen te werken.

Als Beheerder van het a **Systeem**, moet u rollen **begrijpen en toestemmingen** voor zandbakbeleid en kanaalconfiguratie toewijzen. U moet ook een of meer sandboxen instellen en deze beheren voor de beschikbare rollen. U zult dan teamleden aan rollen kunnen toewijzen.

Deze functies kunnen worden beheerd door **[!UICONTROL Product administrators]** die toegang hebben tot het product Machtigingen. [ leer meer over Toestemmingen ](../../administration/permissions.md){target="_blank"}.

Meer informatie over toegangsbeheer vindt u op de volgende pagina&#39;s:

1. **creeer zandbakken** om uw instanties in afzonderlijke, geïsoleerde virtuele milieu&#39;s te verdelen. **Sandboxes** wordt gecreeerd in [!DNL Journey Optimizer]. Leer meer in de [ zandbakken ](../../administration/sandboxes.md) sectie.

   >[!NOTE]
   >Als a **Beheerder van het Systeem**, als u niet het **[!UICONTROL Sandboxes]** menu in [!DNL Journey Optimizer] kunt zien, moet u uw toestemmingen bijwerken. Leer hoe te om uw rol op [ bij te werken deze pagina ](../../administration/permissions.md#edit-product-profile).

1. **begrijp rollen**. Rollen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Leer meer in de [ uit-van-de-doos rollen ](../../administration/ootb-product-profiles.md) sectie.

1. **plaats toestemmingen** voor rollen, met inbegrip van **Sandboxes**, en geef toegang tot uw teamleden door hen aan verschillende rollen toe te wijzen. Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die aan **[!UICONTROL Role]** zijn toegewezen. Elke toestemming wordt verzameld onder mogelijkheden, bijvoorbeeld Reis of Aanbiedingen, die de verschillende functionaliteiten of voorwerpen in [!DNL Journey Optimizer] vertegenwoordigen. Leer meer in de [ niveaus van de Toestemming ](../../administration/high-low-permissions.md) sectie.

Bovendien moet u gebruikers toevoegen die toegang tot de Hoofdzaak van Activa aan de **Hoofdzaak van Activa Consumenten** of/en **de Gebruikers van de Hoofdzaak van Activa** rollen nodig hebben. [ las meer in de documentatie van de Hoofdzaak van Activa ](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target="_blank"}.

>[!NOTE]
>Voor Journey Optimizer-producten die zijn verkregen vóór 6 januari 2022, moet u [!DNL Adobe Experience Manager Assets Essentials] implementeren voor uw organisatie. Leer meer in [ opstellen de Hoofdzaak van Activa ](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target="_blank"} sectie.

Wanneer u [!DNL Journey Optimizer] voor het eerst opent, beschikt u over een productiesandbox en kunt u een bepaald aantal IP&#39;s toewijzen, afhankelijk van uw contract.

Om uw reizen te kunnen tot stand brengen en berichten te verzenden, heb toegang tot het **menu van het BEHEER**. Blader in het menu **[!UICONTROL Channels]** om uw berichten en kanaalconfiguraties (d.w.z. voorinstellingen voor berichten) te configureren.

>[!NOTE]
>Als Beheerder van het a **Systeem**, als u niet het **[!UICONTROL Channels]** menu in [!DNL Journey Optimizer] kunt zien, werk uw toestemmingen in het [ ](../../administration/permissions.md){target="_blank"} product van Toestemmingen bij.
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

   Leer meer over leveringsbaarheidsbeheer in [!DNL Adobe Journey Optimizer] [ op deze pagina ](../../reports/deliverability.md).
