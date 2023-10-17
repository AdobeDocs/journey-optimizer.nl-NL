---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Aan de slag voor systeembeheer
description: Als systeembeheerder, leer meer hoe te om met Journey Optimizer te werken
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: c14a9385191cfa4368e0b84ab16a63c4c87e2c69
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 3%

---

# Aan de slag voor systeembeheerders {#get-started-sys-admins}

Voordat u begint met [!DNL Adobe Journey Optimizer]hebt u verschillende stappen nodig om uw omgeving voor te bereiden.  U moet deze stappen uitvoeren zodat [Gegevensengineer](data-engineer.md) en [Reiswerker](marketer.md) kan beginnen met werken met [!DNL Adobe Journey Optimizer].


Als **Systeembeheerder**, moet u **productprofielen begrijpen en machtigingen toewijzen** voor sandboxbeheer en kanaalconfiguratie. U moet ook een of meer sandboxen instellen en deze beheren voor de beschikbare productprofielen. Vervolgens kunt u teamleden toewijzen aan productprofielen.

Deze mogelijkheden kunnen worden beheerd door **[!UICONTROL Product administrators]** die toegang hebben tot de beheerconsole. [Meer informatie over Adobe Admin Console](https://helpx.adobe.com/nl/enterprise/admin-guide.html){target="_blank"}.

Meer informatie over toegangsbeheer vindt u op de volgende pagina&#39;s:

1. **Sandboxen maken** om uw instanties in afzonderlijke, geïsoleerde virtuele omgevingen te verdelen. **Sandboxen** worden gemaakt in [!DNL Journey Optimizer]. Meer informatie in het dialoogvenster [Sandboxen](../../administration/sandboxes.md) sectie.

   >[!NOTE]
   >Als **Systeembeheerder** als u de **[!UICONTROL Sandboxes]** menu in [!DNL Journey Optimizer]kunt u uw machtigingen in de [Admin Console](https://adminconsole.adobe.com/){target="_blank"}. Leer hoe u uw productprofiel kunt bijwerken in [deze pagina](../../administration/permissions.md#edit-product-profile).
   >

1. **Productprofielen begrijpen**. Productprofielen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Meer informatie in het dialoogvenster [Niet-de-doos productprofielen](../../administration/ootb-product-profiles.md) sectie.

1. **Machtigingen instellen** voor productprofielen, waaronder **Sandboxen** en geef toegang tot uw teamleden door deze toe te wijzen aan verschillende productprofielen. Deze stap wordt uitgevoerd in het dialoogvenster [Admin Console](https://adminconsole.adobe.com/){target="_blank"}. Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die zijn toegewezen aan **[!UICONTROL Product profile]**. Elke toestemming wordt verzameld onder mogelijkheden, bijvoorbeeld Reis of Aanbiedingen, die de verschillende functionaliteiten of voorwerpen in vertegenwoordigen [!DNL Journey Optimizer]. Meer informatie in het dialoogvenster [Machtigingsniveaus](../../administration/high-low-permissions.md) sectie.

Daarnaast moet u gebruikers die toegang tot Assets Essentials nodig hebben, toevoegen aan de **Assets Essentials Consumentengebruikers** of/en **Gebruikers Assets Essentials** Productprofielen. [Meer informatie in de documentatie bij Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target="_blank"}.

>[!NOTE]
>Voor Journey Optimizer-producten die zijn verkregen vóór 6 januari 2022, moet u [!DNL Adobe Experience Manager Assets Essentials] voor uw organisatie. Meer informatie in het dialoogvenster [Assets Essentials implementeren](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target="_blank"} sectie.

Bij toegang [!DNL Journey Optimizer] voor het eerst, bent u provisioned een productiesandbox en toegewezen een bepaald aantal IPs afhankelijk van uw contract.

Als u uw reizen wilt maken en berichten wilt verzenden, opent u het dialoogvenster **ADMINISTRATIE** -menu. Bladeren in het dialoogvenster **[!UICONTROL Channels]** -menu om uw berichten en kanaaloppervlakken te configureren (d.w.z. voorinstellingen voor berichten).

>[!NOTE]
>Als **Systeembeheerder** als u de **[!UICONTROL Channels]** menu in [!DNL Journey Optimizer]kunt u uw machtigingen in de [Admin Console](https://adminconsole.adobe.com/){target="_blank"}. Leer hoe u uw productprofiel kunt bijwerken in [deze pagina](../../administration/permissions.md#edit-product-profile).
>

Voer de onderstaande stappen uit:

1. **Berichten en kanalen configureren**: hiermee definieert u oppervlakken en past u de instellingen voor e-mail, sms en pushberichten aan

   * Definiëren **Instellingen voor pushmeldingen** in beide [!DNL Adobe Experience Platform] en [!DNL Adobe Experience Platform Launch]. [Meer informatie](../../push/push-gs.md)

   * Maken **kanaaloppervlakken** (d.w.z. voorinstellingen voor berichten) om alle technische parameters te configureren die vereist zijn voor e-mail, sms en pushmeldingen. [Meer informatie](../../configuration/channel-surfaces.md)

   * Vorm **SMS-kanaal** om alle technische parameters te configureren die voor SMS vereist zijn. [Meer informatie](../../sms/sms-configuration.md)

   * Het aantal dagen beheren waarin **opnieuw proberen** worden uitgevoerd voordat e-mailadressen naar de suppressielijst worden verzonden. [Meer informatie](../../configuration/manage-suppression-list.md)

1. **Subdomeinen delegeren**: voor elk nieuw subdomein dat in Journey Optimizer wordt gebruikt, is de eerste stap het delegeren. [Meer informatie](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **IP-pools maken**: verbeter uw e-mailleverbaarheid en reputatie door IP adressen te groeperen provisioned met uw instantie. [Meer informatie](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **De onderdrukking en lijsten van gewenste personen beheren**: verbeter uw leverbaarheid met onderdrukking en lijsten van gewenste personen

   * A [onderdrukkingslijst](../../reports/suppression-list.md) bestaat uit e-mailadressen die u van uw leveringen wilt uitsluiten, omdat het verzenden naar deze contacten uw verzendende reputatie en leveringspercentages zou kunnen beschadigen. U kunt alle e-mailadressen controleren die automatisch van het verzenden in een reis, zoals ongeldige adressen worden uitgesloten, adressen die constant elektronische stuiteren, en uw e-mailreputatie, en ontvangers die een spamklacht van één of andere soort tegen één van uw e-mailberichten negatief zouden kunnen beïnvloeden. Leer hoe u de [onderdrukkingslijst](../../configuration/manage-suppression-list.md) en [opnieuw proberen](../../configuration/retries.md).

   ![](../assets/suppression-list-filtering-example.png)

   * De [lijst van gewenste personen](../../configuration/allow-list.md) kunt u afzonderlijke e-mailadressen of domeinen opgeven die de enige ontvangers of domeinen zijn die geautoriseerd zijn om de e-mails te ontvangen die u verzendt vanuit een specifieke sandbox. Dit kan voorkomen dat u per ongeluk e-mailberichten naar de adressen van de echte klant stuurt wanneer u zich in een testomgeving bevindt. Leer hoe u [de lijst van gewenste personen inschakelen](../../configuration/allow-list.md).

   Meer informatie over het beheer van de aflevering vindt u in [!DNL Adobe Journey Optimizer] [op deze pagina](../../reports/deliverability.md).
