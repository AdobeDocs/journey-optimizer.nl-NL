---
title: Webkanaalconfiguratie
description: Webkanaalconfiguratie maken
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 2161baf0-38b7-4397-bffe-083929e8033a
source-git-commit: 37e60e5d7c0ad164cde67015b72341e1f4eda6a9
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 0%

---

# Webkanaalconfiguratie maken {#web-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="Overeenkomende regel voor pagina&#39;s"
>abstract="Als u een groep URL&#39;s met dezelfde criteria efficiënt wilt beheren en als doel wilt instellen, maakt u een overeenkomende regel Pagina&#39;s. Met deze regel kunt u meerdere URL&#39;s samenvoegen onder één regel, waardoor de toepassing van consistente instellingen en handelingen op deze pagina&#39;s eenvoudiger wordt."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="Standaard URL voor ontwerpen en voorvertonen"
>abstract="Met dit veld zorgt u ervoor dat de pagina&#39;s die door de regel worden gegenereerd of waaraan de regel is gekoppeld, een opgegeven URL hebben die essentieel is voor een effectieve weergave van inhoud en voor een voorvertoning."

Een webconfiguratie is een webeigenschap die wordt geïdentificeerd door een URL waar de inhoud wordt geleverd. De URL kan overeenkomen met één pagina of meerdere pagina&#39;s, zodat u wijzigingen kunt doorvoeren op een of meerdere webpagina&#39;s.

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** en klik op **[!UICONTROL Create channel configuration]** .

   ![](assets/web_config_1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Als u aangepaste of basislabels voor gegevensgebruik aan de configuratie wilt toewijzen, kunt u **[!UICONTROL Manage access]** selecteren. [ leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md).

1. Selecteer **kanaal 0} van het Web {.**

   ![](assets/web_config_2.png)

1. Selecteer **[!UICONTROL Marketing action]**(s) om het toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)

1. U kunt een **[!UICONTROL Page URL]** invoeren als u de wijzigingen alleen op één pagina wilt toepassen.

1. U kunt ook een **[!UICONTROL Pages matching rule]** maken om meerdere URL&#39;s met dezelfde regel als doel in te stellen, bijvoorbeeld als u de wijzigingen op een hoofdbanner op een hele website wilt toepassen of een bovenste afbeelding wilt toevoegen die op alle productpagina&#39;s van een website wordt weergegeven.

   Selecteer hiervoor **[!UICONTROL Pages matching rule]** .

1. Definieer de criteria voor de velden **[!UICONTROL Domain]** en **[!UICONTROL Page]** .

   Als u bijvoorbeeld elementen wilt bewerken die op alle pagina&#39;s met vrouwenproducten van uw Luma-website worden weergegeven, selecteert u **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `luma` en **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `women` .

   ![](assets/web_config_3.png)

1. Als u a **[!UICONTROL Page matching rule]** creeerde, moet u het **Standaard** auteursrecht ingaan en voorproef URL. Met deze stap zorgt u ervoor dat de pagina&#39;s die door de regel worden gegenereerd of waaraan de regel is gekoppeld, een aangewezen URL hebben voor zowel het maken van inhoud als het weergeven van voorvertoningen. Leer meer over pagina passende regel in de [ hieronder sectie ](#web-page-matching-rule).

1. Sla uw wijzigingen op.

U kunt nu uw configuratie selecteren wanneer het gebruiken van het Kanaal van het Web in campagnes of reizen.

## Regels voor paginaovereenkomst {#web-page-matching-rule}

Wanneer het creëren van een regel die veelvoudige pagina&#39;s aanpast zodat u de zelfde inhoudsveranderingen over veelvoudige pagina&#39;s tegelijk kunt toepassen, kunt u verschillende exploitanten op het **Domein** en op de **3} secties van de Weg {gebruiken om uw gewenste regel te bouwen.** Controleer hieronder de beschikbare operatoren.

Beschikbare operatoren voor het samenstellen van regels voor paginaovereenkomsten:

* **Domein**

  | Operator  | Beschrijving  | Voorbeelden  |
  |---|---|---|
  | Gelijk  | Exacte overeenkomst van het domein.  |
  | Begint met  | Komt overeen met alle domeinen (inclusief subdomeinen) die beginnen met de ingevoerde tekenreeks.  | Voorbeeld: &quot;Begint met: dev&quot; -> komt overeen met alle domeinen en subdomeinen die beginnen met &quot;dev&quot;, zoals: dev.example.com, dev.products.example.com, developer.example.com  |
  | Eindigt met  | Komt overeen met alle domeinen (inclusief subdomeinen) die eindigen met de ingevoerde tekenreeks.  | Voorbeeld: &quot;Eindigt met: example.com&quot; -> komt overeen met alle domeinen en subdomeinen die eindigen met &quot;example.com&quot;, zoals: stage.example.com, prod.example.com, myexample.com  |
  | Overeenkomende jokertekens  | Met de operator voor jokertekenovereenkomsten kan de gebruiker een jokertekenovereenkomst definiëren in het midden van de tekenreeks, zoals &quot;dev.*.example.com&quot;. De validatieregels bepalen dat de waarde één en slechts één jokerteken (sterretje) moet bevatten wanneer de operator &quot;jokertekenovereenkomst&quot; is.  | Voorbeeld: &quot;Jokertekentekoppeling: dev.*.example.com&quot; -> komt overeen met domeinen als: dev.products.example.com, dev.mytest.products.example.com, dev.blog.example.com  |
  | Alle  | Komt overeen met alle domeinen - nuttig bij het testen van een bepaald pad over domeinen  |


* **Weg**

<table>
    <thead>
    <tr>
        <th><strong>Operator</th>
        <th><strong>Beschrijving</th>
        <th><strong>Voorbeelden</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>Gelijk</td>
        <td>Exacte overeenkomst van het pad. </td>
        <td></td>
    </tr>
    <tr>
        <td>Begint met</td>
        <td>Komt overeen met alle paden (inclusief subpaden) die beginnen met de ingevoerde tekenreeks.</td>
        <td></td>
    </tr>
    <tr>
        <td>Eindigt met</td>
        <td>Komt overeen met alle paden (inclusief subpaden) die eindigen met de ingevoerde tekenreeks.</td>
        <td></td>
    </tr>
    <tr>
        <td>Alle</td>
        <td>Hiermee worden alle paden met elkaar vergeleken. Dit is handig wanneer u alle paden in een of meerdere domeinen aanwijst.</td>
        <td></td>
    </tr>
    <tr>
        <td>Overeenkomende jokertekens</td>
        <td>Met de operator voor jokertekens kan de gebruiker een interne jokerteken in het pad definiëren, zoals "/products/*/detail".  Het jokerteken * in de component Path ** komt overeen met een willekeurige reeks tekens totdat het eerste / teken wordt aangetroffen.  /*/ komt overeen met een willekeurige reeks tekens (inclusief subpaden)</td>
        <td>Voorbeeld: "Jokertekentekoppeling: /products/*/detail" komt overeen met alle paden zoals: <ul><li>example.com/products/yoga/detail</li><li>example.com/products/surf/detail</li><li>example.com/products/tennis/detail</li><li>example.com/products/yoga/pants/detail</li></ul>Voorbeeld: "Overeenkomsten: /prod*/detail, komt overeen met alle paden als: <ul><li>example.com/products/detail</li><li>example.com/production/detail</li></ul>komt niet overeen met paden als: <ul><li>example.com/products/yoga/detail</li></ul></td>
    </tr>
    <tr>
        <td>Bevat</td>
        <td>"contains" wordt omgezet in een jokerteken zoals "mystring" en komt overeen met alle paden die deze reeks tekens bevatten.</td>
        <td>Ex: "Bevat: product", komt overeen met alle paden die het tekenreeksproduct bevatten, zoals: <ul><li>example.com/products</li><li>example.com/yoga/perfproduct</li><li>example.com/surf/productdescription</li><li>example.com/home/product/page</li></ul></td>
    </tr>
    </tbody>
</table>

Als uw gebruikscase niet met één regel kan worden gemodelleerd, kunt u meerdere paginaregels toevoegen en kunt u de operatoren &#39;&#39;Of&#39;&#39; of &#39;&#39;Uitsluiten&#39;&#39; gebruiken. &#39;Uitsluiten&#39; is handig wanneer een pagina die overeenkomt met de gedefinieerde regel niet als doelpagina moet worden opgegeven: bijvoorbeeld alle pagina&#39;s &#39;example.com&#39; die &#39;product&#39; bevatten, met uitzondering van de volgende pagina: `https://example.com/blogs/productinfo` .
