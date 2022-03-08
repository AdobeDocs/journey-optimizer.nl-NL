---
title: Journey Optimizer Aan de slag voor systeembeheer
description: Als systeembeheerder, leer meer hoe te om met Journey Optimizer te werken
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# Aan de slag voor systeembeheerders {#get-started-sys-admins}

![beheerder](assets/do-not-localize/user-2.png)

Voordat u begint met [!DNL Adobe Journey Optimizer]hebt u verschillende stappen nodig om uw omgeving voor te bereiden.  U moet deze stappen uitvoeren zodat [Gegevensengineer](data-engineer.md) en [Reiswerker](marketer.md) kan beginnen met werken met [!DNL Adobe Journey Optimizer].


Als **Systeembeheerder**, moet u **productprofielen begrijpen en machtigingen toewijzen** voor sandboxbeheer en kanaalconfiguratie. U moet ook een of meer sandboxen instellen en deze beheren voor de beschikbare productprofielen. Vervolgens kunt u teamleden toewijzen aan productprofielen.

Deze mogelijkheden kunnen worden beheerd door **[!UICONTROL Product administrators]** die toegang hebben tot de beheerconsole. [Meer informatie over Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Meer informatie over toegangsbeheer vindt u op de volgende pagina&#39;s:

1. **Sandboxen maken** om uw instanties in afzonderlijke, geïsoleerde virtuele omgevingen te verdelen. **Sandboxen** worden gemaakt in [!DNL Journey Optimizer]. Meer informatie in het dialoogvenster [Sandboxen](../../administration/sandboxes.md) sectie.

   >[!NOTE]
   >Als **Systeembeheerder** als u de **[!UICONTROL Sandboxes]** menu in [!DNL Journey Optimizer]kunt u uw machtigingen in de [Admin Console](https://adminconsole.adobe.com/){_blank}. Leer hoe u uw productprofiel kunt bijwerken in [deze pagina](../../administration/permissions.md#edit-product-profile).

1. **Productprofielen begrijpen**. Productprofielen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Meer informatie in het dialoogvenster [Productprofielen buiten de verpakking](../../administration/ootb-product-profiles.md) sectie.

1. **Machtigingen instellen** voor productprofielen, waaronder **Sandboxen** en geef toegang tot uw teamleden door deze toe te wijzen aan verschillende productprofielen. Deze stap wordt uitgevoerd in het dialoogvenster [Admin Console](https://adminconsole.adobe.com/){_blank}. Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die zijn toegewezen aan **[!UICONTROL Product profile]**. Elke toestemming wordt verzameld onder mogelijkheden, bijvoorbeeld Reis, Berichten of Aanbiedingen, die de verschillende functionaliteiten of voorwerpen in vertegenwoordigen [!DNL Journey Optimizer]. Meer informatie in het dialoogvenster [Machtigingsniveaus](../../administration/high-low-permissions.md) sectie.

Bovendien moet u gebruikers die toegang tot Assets Essentials nodig hebben, toevoegen aan de **Assets Essentials Consumer Users** of/en **Assets Essentials-gebruikers** Productprofielen. [Meer informatie in Assets Essentials-documentatie](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>Voor Journey Optimizer-producten die zijn verkregen vóór 6 januari 2022, moet u [!DNL Adobe Experience Manager Assets Essentials] voor uw organisatie. Meer informatie in het dialoogvenster [Assets Essentials implementeren](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;} -sectie.

Bij toegang [!DNL Journey Optimizer] voor het eerst, bent u provisioned een productiesandbox en toegewezen een bepaald aantal IPs afhankelijk van uw contract.

Als u uw reizen wilt maken en berichten wilt verzenden, opent u de **ADMINISTRATIE** -menu. Bladeren in het dialoogvenster **[!UICONTROL Channels]** om uw e-mailberichten en voorinstellingen te configureren.

>[!NOTE]
>Als **Systeembeheerder** als u de **[!UICONTROL Channels]** menu in [!DNL Journey Optimizer]kunt u uw machtigingen in de [Admin Console](https://adminconsole.adobe.com/){_blank}. Leer hoe u uw productprofiel kunt bijwerken in [deze pagina](../../administration/permissions.md#edit-product-profile).

Voer de onderstaande stappen uit:

1. **Berichten en kanalen configureren**: voorinstellingen definiëren, instellingen voor e-mail- en pushberichten aanpassen en aanpassen

   * Definiëren **Instellingen voor pushmeldingen** in beide [!DNL Adobe Experience Platform] en [!DNL Adobe Experience Platform Launch]. [Meer informatie](../../messages/push-gs.md)

   * Maken **berichtvoorinstellingen** om alle technische parameters te configureren die vereist zijn voor e-mail- en pushberichten. [Meer informatie](../../configuration/message-presets.md)

   * Het aantal dagen beheren waarin **opnieuw** worden uitgevoerd voordat e-mailadressen naar de suppressielijst worden verzonden. [Meer informatie](../../configuration/manage-suppression-list.md)

1. **Subdomeinen delegeren**: voor om het even welk nieuw subdomain dat in Journey Optimizer moet worden gebruikt, zal de eerste stap het delegeren zijn. [Meer informatie](../../configuration/about-subdomain-delegation.md)

   ![](../../assets/subdomain.png)

1. **IP-pools maken**: Verbeter uw e-mailleverbaarheid en reputatie door IP adressen te groeperen die aan uw instantie worden geleverd. [Meer informatie](../../configuration/ip-pools.md)

   ![](../../assets/ip-pool.png)

1. **De onderdrukking en lijst van gewenste personen beheren**: verbeter uw leverbaarheid met onderdrukking en lijsten van gewenste personen

   * A [onderdrukkingslijst](../../messages/suppression-list.md) bestaat uit e-mailadressen die u van uw leveringen wilt uitsluiten, omdat het verzenden naar deze contacten uw verzendende reputatie en leveringspercentages zou kunnen beschadigen. U kunt alle e-mailadressen controleren die automatisch van het verzenden van een reis, zoals ongeldige adressen, adressen worden uitgesloten die constant elektronische stuiteren, en uw e-mailreputatie, en ontvangers die een spamklacht van één of andere soort tegen één van uw e-mailberichten negatief zouden kunnen beïnvloeden. Leer hoe u de [onderdrukkingslijst](../../configuration/manage-suppression-list.md) en [opnieuw](../../configuration/retries.md).
   ![](../../assets/suppression-list-filtering-example.png)

   * De [lijst van gewenste personen](../../messages/allow-list.md) kunt u afzonderlijke e-mailadressen of domeinen opgeven die de enige ontvangers of domeinen zijn die geautoriseerd zijn om de e-mails te ontvangen die u verzendt vanuit een specifieke sandbox. Dit kan voorkomen dat u per ongeluk e-mailberichten naar de adressen van de echte klant stuurt wanneer u zich in een testomgeving bevindt. Leer hoe u [de lijst van gewenste personen inschakelen](../../messages/allow-list.md).
   Meer informatie over het beheer van de aflevering vindt u in [!DNL Adobe Journey Optimizer] [op deze pagina](../../messages/deliverability.md).
