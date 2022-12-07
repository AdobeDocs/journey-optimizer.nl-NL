---
title: Directe-mailconfiguratie
description: Leer hoe u direct-mailkanaal kunt configureren in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: 978751263ba2ed21e35e41e767f1e31ddbe59d53
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# Directe-mailconfiguratie {#direct-mail-configuration}

[!DNL Journey Optimizer] staat u toe om de dossiers te personaliseren en te produceren die door directe postleveranciers worden vereist om post naar uw klanten te verzenden.

Wanneer [een direct-mailbericht maken](../direct-mail/create-direct-mail.md), definieert u de doelpublieksgegevens, inclusief de gekozen contactgegevens (bijvoorbeeld het postadres). Er wordt dan automatisch een bestand met deze gegevens gegenereerd en geëxporteerd naar een server, waar uw directe-mailprovider het bestand kan ophalen en de daadwerkelijke verzending kan verzorgen.

Voordat u dit bestand kunt genereren, moet u het volgende maken:

1. A [bestand dat configuratie verplettert](#file-routing-configuration) om de server op te geven waar het bestand wordt geëxporteerd.

1. A [direct-mailoppervlak](#direct-mail-surface) dat het dossier zal van verwijzingen voorzien dat configuratie verplettert.

>[!CAUTION]
>
>Als u geen dossier gevormd hebt dat optie verplettert, zult u geen direct-mailoppervlak kunnen tot stand brengen.

## Bestands-routering configureren {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definieer het bestand dat de configuratie verplettert"
>abstract="Nadat u een direct-mailbericht hebt gemaakt, wordt het bestand met de doelpublieksgegevens gegenereerd en geëxporteerd naar een server. U moet de serverdetails specificeren zodat uw direct-mailleverancier tot dat dossier voor levering direct-mail kan toegang hebben en gebruiken."
<!-->
>additional-url=&quot;https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/create-direct-mail.html&quot; text=&quot;Create a direct mail message&quot;—>

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definieer het bestand dat de configuratie verplettert"
>abstract="U moet definiëren waar het bestand wordt geëxporteerd voordat uw direct-mailprovider het kan gebruiken."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuratie van bestandsroutering"
>abstract="Selecteer het dossier dat configuratie van uw keus verplettert, die bepaalt waar het dossier voor uw direct-mailleverancier aan gebruik zal worden uitgevoerd."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Selecteer het servertype voor uw bestand"
>abstract="Kies welk type server u wilt gebruiken voor het exporteren van uw bestanden voor directe e-mail. Momenteel worden alleen Amazon S3 en SFTP ondersteund door Journey Optimizer."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Kies het AWS-gebied"
>abstract="Selecteer het geografische gebied van de AWS-server waarop u uw bestanden voor directe e-mail wilt exporteren. In het algemeen verdient het de voorkeur het gebied te kiezen dat het dichtst bij de locatie van uw directe-mailprovider ligt."

Om een direct-mailbericht te leveren, [!DNL Journey Optimizer] Hiermee genereert en exporteert u het bestand met de doelgegevens naar een server.

U moet die serverdetails specificeren zodat uw direct-mailleverancier tot dat dossier voor het leveren van post kan toegang hebben en gebruiken.

Om het dossier te vormen die, volg de stappen hieronder verpletteren.

1. Toegang krijgen tot **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL File routing configuration]** > **[!UICONTROL File Routing]** en klik vervolgens op **[!UICONTROL Create routing configuration]**.

   ![](assets/file-routing-config-button.png)

1. Plaats een naam voor uw configuratie.

1. Selecteer **[!UICONTROL Server type]** die u wilt gebruiken voor het exporteren van de direct-mailbestanden.

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Momenteel worden alleen Amazon S3 en SFTP ondersteund in [!DNL Journey Optimizer].

1. Vul de gegevens en referenties voor uw server in, zoals het serveradres, de toegangstoets, enzovoort.

   ![](assets/file-routing-config-sftp-details.png)

1. Als u **[!UICONTROL Amazon S3]**, kiest u de **[!UICONTROL AWS region]** waar de serverinfrastructuur zal worden gevestigd.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >AWS-regio&#39;s zijn geografische gebieden die AWS gebruikt om haar cloudinfrastructuur te hosten. In het algemeen verdient het de voorkeur het gebied te kiezen dat het dichtst bij de locatie van uw directe-mailprovider ligt.

1. Selecteer **[!UICONTROL Submit]**. Het dossier dat configuratie verplettert wordt gecreeerd met **[!UICONTROL Active]** status. Het is nu klaar om te worden gebruikt in een [direct-mailoppervlak](#direct-mail-surface).

   >[!NOTE]
   >
   >U kunt ook **[!UICONTROL Save as draft]** om het dossier tot stand te brengen dat configuratie verplettert, maar u zult niet het in een oppervlakte kunnen selecteren tot het is **[!UICONTROL Active]**.

## Een direct-mailoppervlak maken {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Instellingen voor direct mail definiëren"
>abstract="Een direct-mailoppervlak bevat de instellingen voor de opmaak van het bestand dat de doelpublieksgegevens bevat en wordt gebruikt door de mailprovider. U moet ook bepalen waar het dossier door het dossier te selecteren verplettert configuratie zal worden uitgevoerd."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/direct-mail-configuration.html#file-routing-configuration" text="Bestands-routering configureren"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="De drempelwaarde voor het splitsen van bestanden definiëren"
>abstract="U moet het maximumaantal records instellen voor elk bestand dat publieksgegevens bevat. U kunt een willekeurig getal tussen 1 en 200.000 records selecteren. Nadat de opgegeven drempelwaarde is bereikt, wordt een ander bestand gemaakt voor de resterende records."

Direct mailen met [!DNL Journey Optimizer], moet u een kanaaloppervlak maken om de instellingen te definiëren voor de opmaak van het bestand dat wordt gebruikt door de mailprovider.

Een direct-mailoppervlak moet ook het bestand bevatten dat de configuratie verplettert die de server definieert waar het direct-mailbestand wordt geëxporteerd.

1. Maak een kanaaloppervlak. [Meer informatie](../configuration/channel-surfaces.md)

1. Selecteer **[!UICONTROL Direct mail]** kanaal.

   ![](assets/surface-direct-mail-channel.png)

1. Bepaal de direct-mailmontages in de specifieke sectie van de configuratie van de kanaaloppervlakte.

   ![](assets/surface-direct-mail-settings.png)

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Selecteer de bestandsindeling: **[!UICONTROL CSV]** of **[!UICONTROL Text delimited]**.

1. Selecteer **[!UICONTROL File routing configuration]** onder de mensen die je creëerde. Hiermee bepaalt u waar het bestand wordt geëxporteerd zodat uw direct-mailprovider het kan gebruiken.

   >[!CAUTION]
   >
   >Als u geen dossier gevormd hebt dat optie verplettert, zult u geen direct-mailoppervlak kunnen tot stand brengen. [Meer informatie](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Verzend het direct-mailoppervlak.

U kunt nu [een direct-mailbericht maken](../direct-mail/create-direct-mail.md) in een campagne. Nadat de campagne is gestart, wordt het bestand met de doelgegevens van het publiek automatisch geëxporteerd naar de server die u hebt gedefinieerd. De direct-mailprovider kan dat bestand vervolgens ophalen en doorgaan met de directe-maillevering.

>[!NOTE]
>
>Dubbele rijen worden automatisch verwijderd.
>
>Als het maximumaantal records (dat wil zeggen rijen) voor elk bestand met profielgegevens te hoog is, wordt automatisch een ander bestand gemaakt voor de resterende records.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->