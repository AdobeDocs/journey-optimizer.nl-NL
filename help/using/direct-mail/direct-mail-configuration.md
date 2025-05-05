---
title: Directe-mailconfiguratie
description: Leer hoe u direct-mailkanaal kunt configureren in Journey Optimizer
feature: Direct Mail, Surface
topic: Content Management
role: User
level: Experienced
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: 65b7b8323e37a0143a3941af1b9c2fb8b595a376
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 1%

---

# Directe-mailconfiguratie {#direct-mail-configuration}

Met [!DNL Journey Optimizer] kunt u de bestanden die worden vereist door directe-mailproviders aanpassen en genereren om e-mail naar uw klanten te sturen.

Wanneer [ creërend een direct-mailbericht ](../direct-mail/create-direct-mail.md), bepaalt u de gerichte publieksgegevens, met inbegrip van de gekozen contactinformatie (postadres bijvoorbeeld). Er wordt dan automatisch een bestand met deze gegevens gegenereerd en geëxporteerd naar een server, waar uw directe-mailprovider het bestand kan ophalen en de daadwerkelijke verzending kan verzorgen.

Voordat u dit bestand kunt genereren, moet u het volgende maken:

1. [ dossier dat van A configuratie ](#file-routing-configuration) verplettert om de server te specificeren waar het dossier zal worden uitgevoerd en het dossier coderen, indien nodig.

1. [ de direct-mailconfiguratie van A ](#direct-mail-configuration) die verwijzingen het dossier dat configuratie verplettert. Als u geen dossier gevormd hebt dat optie verplettert, zult u geen directe-mailconfiguratie kunnen tot stand brengen.


>[!CAUTION]
>
>* Om een dossier tot stand te brengen dat configuratie verplettert, moet u **[!DNL Manage file routing]** ingebouwde toestemming hebben. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager)
>
>* Directe-mailbestanden worden alleen gegenereerd op het moment van export. Het systeem slaat niet oneindig oudere exportbewerkingen op. Voor langere of permanente back-up configureert u een optie voor het routeren van bestanden (SFTP of cloudopslag).

## Bestands-routering configureren {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definieer het bestand dat de configuratie verplettert"
>abstract="Nadat u een direct-mailbericht hebt gemaakt, wordt het bestand met de doelpublieksgegevens gegenereerd en geëxporteerd naar een server. U moet de serverdetails specificeren zodat uw direct-mailleverancier tot dat dossier voor levering direct-mail kan toegang hebben en gebruiken."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/direct-mail/create-direct-mail" text="Een direct-mailbericht maken"

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
>abstract="Kies welk type server u wilt gebruiken voor het exporteren van uw direct-mailbestanden: Amazon S3, SFTP, Azure of Data Landing Zone."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Kies het AWS-gebied"
>abstract="Selecteer het geografische gebied van de AWS-server waarop u uw bestanden voor directe e-mail wilt exporteren. In het algemeen verdient het de voorkeur het gebied te kiezen dat het dichtst bij de locatie van uw directe-mailprovider ligt."

>[!NOTE]
>
>Amazon S3, SFTP, Azure en Data Landing Zone worden momenteel ondersteund in [!DNL Journey Optimizer] .

[!DNL Journey Optimizer] genereert en exporteert het bestand met de doelpublieksgegevens naar een server om een direct mailbericht te verzenden.

U moet die serverdetails specificeren zodat uw direct-mailleverancier tot dat dossier voor het leveren van post kan toegang hebben en gebruiken.

Om het dossier te vormen dat, volg de stappen hieronder verplettert.

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Direct mail settings]** > **[!UICONTROL File routing]** en klik op **[!UICONTROL Create file routing config]** .

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. Plaats een naam voor uw configuratie.

1. Selecteer het type server dat u wilt gebruiken voor het exporteren van uw direct-mailbestanden: Amazon S3, SFTP, Azure of Data Landing Zone.

   ![](assets/file-routing-config-type.png){width="800" align="center"}

1. Vul de velden in die specifiek zijn voor elk servertype, zoals hieronder wordt beschreven.

>[!BEGINTABS]

>[!TAB Amazon S3]

Als u **[!UICONTROL Amazon S3]** als **[!UICONTROL Server type]** hebt geselecteerd, vult u de gegevens en referenties voor uw server in:

* **de emmer van AWS**:Om te weten waar te om uw het emmernaam van AWS te vinden, verwijs naar [ deze pagina ](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html).

* **de toegangssleutel van AWS**: Om te weten waar te om uw de toegangs belangrijkste identiteitskaart van AWS te vinden, verwijs naar [ deze pagina ](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#access-keys-and-secret-access-keys).

* **geheime sleutel van AWS**: Om te weten waar te om uw geheime sleutel van AWS te vinden, verwijs naar [ deze pagina ](https://aws.amazon.com/fr/blogs/security/wheres-my-secret-access-key/).

* **gebied van AWS**: kies **[!UICONTROL AWS region]** waar de serverinfrastructuur zal worden gevestigd. AWS-regio&#39;s zijn geografische gebieden die AWS gebruikt om haar cloudinfrastructuur te hosten. In het algemeen verdient het de voorkeur het gebied te kiezen dat het dichtst bij de locatie van uw directe-mailprovider ligt.

![](assets/file-routing-config-aws-region.png){width="800" align="center"}

>[!TAB SFTP]

Als u **[!UICONTROL SFTP]** als **[!UICONTROL Server type]** hebt geselecteerd, vult u de gegevens en referenties voor uw server in:

* **Rekening**: De naam van de rekening die wordt gebruikt om met de server te verbinden SFTP.

* **adres van de Server**: &#x200B; URL van de server SFTP.

* **Haven**: Het aantal van de de verbindingshaven van FTP.

* **Wachtwoord**: &#x200B; Wachtwoord dat wordt gebruikt om met de server te verbinden SFTP.

![](assets/file-routing-config-sftp-detail.png)

>[!NOTE]
>
>Als u een pad op de server voor het opslaan van het bestand wilt opgeven, werkt u het veld **[!UICONTROL Filename]** van de campagne voor direct mail bij en voegt u het gewenste pad in. [Meer informatie](create-direct-mail.md#extraction-file)

>[!TAB  Azure ]

Als u **[!UICONTROL Azure]** als **[!UICONTROL Server type]** hebt geselecteerd, vult u de gegevens en referenties voor uw server in:

* **Azure Koord van de Verbinding**: Om uw **Azure Koord van de Verbinding** te vinden, verwijs naar [ deze pagina ](https://learn.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string#configure-a-connection-string-for-an-azure-storage-account).

  Het **Azure Koord van de Verbinding** zou het formaat hieronder moeten volgen:

  `DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey`

* **Naam van de Container**: Om uw **Naam van de Container** te vinden, verwijs naar [ deze pagina ](https://learn.microsoft.com/en-us/azure/storage/blobs/blob-containers-portal).

  De **Naam van de Container** zou slechts de naam van de container zonder enige schuine strepen moeten bevatten.

  >[!NOTE]
  >
  >Als u een pad in de container voor het opslaan van het bestand wilt opgeven, werkt u het veld **[!UICONTROL Filename]** van de campagne voor direct mail bij en voegt u het gewenste pad in. [Meer informatie](create-direct-mail.md#extraction-file)

  ![](assets/file-routing-config-azure-detail.png)

>[!TAB Gegevens die Zone  aanvoeren]

Als u **[!UICONTROL Data Landing Zone]** als **[!UICONTROL Server type]** hebt geselecteerd, zijn geen specifieke details vereist.

![](assets/file-routing-config-dlz-detail.png)

Alle klanten van [!DNL Adobe Experience Platform] zijn provisioned met één container van de Landing van de Zone van Gegevens per zandbak. Leer meer over Gegevens het Landing Zone in de [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}.

>[!ENDTABS]

Als u het bestand wilt versleutelen, kopieert en plakt u de coderingssleutel in het veld **[!UICONTROL PGP/GPG encryption key]** .

Selecteer **[!UICONTROL Submit]** als u de gegevens voor het servertype hebt ingevuld. Het dossier dat configuratie verplettert wordt gecreeerd met de **[!UICONTROL Active]** status. Het is nu klaar om in a [ direct-mailconfiguratie ](#direct-mail-surface) worden gebruikt.

U kunt **[!UICONTROL Save as draft]** ook selecteren om het dossier tot stand te brengen dat configuratie verplettert, maar u zult het niet in een configuratie kunnen selecteren tot het **[!UICONTROL Active]** is.

## Een configuratie voor direct mail maken {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Instellingen voor direct mail definiëren"
>abstract="Een direct-mailconfiguratie bevat de instellingen voor de opmaak van het bestand dat de doelpublieksgegevens bevat en wordt gebruikt door de mailprovider. U moet ook bepalen waar het dossier door het dossier te selecteren verplettert configuratie zal worden uitgevoerd."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/direct-mail/direct-mail-configuration#file-routing-configuration" text="Bestands-routering configureren"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="De drempelwaarde voor het splitsen van bestanden definiëren"
>abstract="U moet het maximumaantal records instellen voor elk bestand dat publieksgegevens bevat. U kunt een willekeurig getal tussen 1 en 200.000 records selecteren. Nadat de opgegeven drempelwaarde is bereikt, wordt een ander bestand gemaakt voor de resterende records."

Als u direct mail met [!DNL Journey Optimizer] wilt kunnen leveren, moet u een kanaalconfiguratie tot stand brengen om de montages voor het formatteren van het dossier te bepalen dat door de postleverancier zal worden gebruikt.

Een direct-mailconfiguratie moet ook het dossier omvatten dat configuratie verplettert die de server bepaalt waar uw direct-maildossier zal worden uitgevoerd.

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** . Klik op de knop **[!UICONTROL Create channel configuration]**. [Meer informatie](../configuration/channel-surfaces.md)

   ![](assets/direct-mail-config-1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in en selecteer vervolgens het kanaal dat u wilt configureren.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Als u aangepaste of basislabels voor gegevensgebruik aan de configuratie wilt toewijzen, kunt u **[!UICONTROL Manage access]** selecteren. [ leer meer over de Controle van de Toegang van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md).

1. Selecteer het kanaal **[!UICONTROL Direct mail]** .

   ![](assets/direct-mail-config-2.png)

1. Selecteer **[!UICONTROL Marketing action]**(s) om het toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)

1. Definieer de instellingen voor directe e-mail in de specifieke sectie van de kanaalconfiguratie.

   ![](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Selecteer de bestandsindeling: **[!UICONTROL CSV]** of **[!UICONTROL Text delimited]** .

1. Als u **[!UICONTROL Text delimited]** selecteert, definieert u het kolomscheidingsteken van uw keuze: tabulatie, puntkomma, pipe of en ampersand.

   ![](assets/surface-direct-mail-column-separator.png)

1. Selecteer de **[!UICONTROL File routing configuration]** onder de bestanden die u hebt gemaakt. Hiermee bepaalt u waar het bestand wordt geëxporteerd zodat uw direct-mailprovider het kan gebruiken.

   >[!CAUTION]
   >
   >Als u geen dossier gevormd hebt dat optie verplettert, zult u geen directe-mailconfiguratie kunnen tot stand brengen. [Meer informatie](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Verzend de configuratie voor direct mail.

U kunt [ een direct-mailbericht ](../direct-mail/create-direct-mail.md) binnen een campagne nu tot stand brengen. Nadat de campagne is gestart, wordt het bestand met de doelgegevens van het publiek automatisch geëxporteerd naar de server die u hebt gedefinieerd. De direct-mailprovider kan dat bestand vervolgens ophalen en doorgaan met de directe-maillevering.

>[!NOTE]
>
>Dubbele rijen waarbij alle waarden in de rij gelijk zijn, worden automatisch uit het bestand verwijderd.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->