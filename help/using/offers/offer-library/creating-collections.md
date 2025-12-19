---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Verzamelingen maken
description: Leer hoe u aanbiedingen kunt organiseren met gebruik van verzamelingen
badge: label="Verouderd" type="Informative"
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 2%

---

# Verzamelingen maken {#create-collections}

>[!TIP]
>
>Het besluit, de nieuwe beslissingsmogelijkheden van [!DNL Adobe Journey Optimizer], is nu beschikbaar via de op code gebaseerde ervaring en e-mailkanalen! [Meer informatie](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="Over aanbiedingsverzamelingen"
>abstract="Met aanbiedingen kunt u uw aanbiedingen ordenen door deze te hergroeperen in categorieën van uw keuze."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic"
>title="Dynamische verzameling"
>abstract="Gebruik verzamelingskwalificatoren om aanbiedingen voor een verzameling dynamisch te kwalificeren."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static"
>title="Statische verzameling"
>abstract="U kunt aanbiedingen handmatig selecteren en groeperen aan de hand van criteria zoals status, kwalificatie voor verzameling, datum en kanaal."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static_select"
>title="Voorvertoning statische verzameling"
>abstract="De statische inzamelingen worden gebouwd door individuele aanbiedingen manueel te selecteren om in de inzameling te omvatten. De verzameling kan alleen worden bijgewerkt door er handmatig meer aanbiedingen aan toe te voegen."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic_select"
>title="Dynamische voorvertoning van verzameling"
>abstract="Met dynamische verzamelingen worden aanbiedingen verzameld op basis van verzamelingsaanduidingen. Deze verzamelingen worden automatisch bijgewerkt. Als bijvoorbeeld een nieuwe aanbieding wordt gemaakt met de kwalificatie &#39;sport&#39; voor de verzameling, wordt deze automatisch toegevoegd aan de corresponderende verzameling."

Met verzamelingen kunt u uw aanbiedingen ordenen door deze te hergroeperen in categorieën van uw keuze. U kunt bijvoorbeeld een &quot;sport&quot;-collectie maken die alleen sportgerelateerde aanbiedingen bevat.

➡️ [Ontdek deze functie in video](#video)

De lijst met aanbiedingsverzamelingen is toegankelijk in het menu **[!UICONTROL Offers]** .

![](../assets/collections_list.png)

U kunt twee typen verzamelingen maken:

* **de Dynamische inzamelingen** zijn inzamelingen van aanbiedingen die op inzamelingsbepalende elementen (eerder als &quot;markeringen worden bekend&quot;) worden gebaseerd. Deze verzamelingen worden automatisch bijgewerkt. Bijvoorbeeld, als een nieuwe aanbieding met het geselecteerde inzamelingsbepaler wordt gecreeerd, zal het automatisch aan de inzameling worden toegevoegd.

* **de Statische inzamelingen** zijn inzamelingen die door individuele aanbiedingen manueel te selecteren om in de Inzameling te omvatten worden gebouwd. De verzameling kan alleen worden bijgewerkt door er handmatig meer aanbiedingen aan toe te voegen.

Ga als volgt te werk om een verzameling te maken:

1. Ga naar de tab **[!UICONTROL Collections]** en klik vervolgens op **[!UICONTROL Create collection]** .

1. Geef de naam en het type verzameling op dat u wilt maken.

   ![](../assets/collection_create.png)

1. Als u een dynamische verzameling wilt maken, selecteert u in het linkerdeelvenster de verzamelingskwalificatie van de aanbiedingen die u aan de verzameling wilt toevoegen en klikt u op **[!UICONTROL Save]** . Alle aanbiedingen met de geselecteerde inzamelingskwalificatie zullen in de inzameling worden bewaard.

   Voor meer op de verwezenlijking van inzamelingsbepalers, zie [&#x200B; inzamelingsbepalende eigenschappen &#x200B;](../offer-library/creating-tags.md) creëren.

   ![](../assets/dynamic_collection.png)

1. Als u een statische verzameling wilt maken, gebruikt u het linkerdeelvenster om de lijst met aanbiedingen (status, kwalificatie van verzameling, datum, kanaal, inhoudstype) te filteren en selecteert u vervolgens de aanbiedingen die u aan de verzameling wilt toevoegen.

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >Statische verzamelingen worden niet automatisch bijgewerkt. Om aanbiedingen aan een statische inzameling toe te voegen, moet u het uitgeven en hen manueel toevoegen.

1. Selecteer **[!UICONTROL Manage access]** als u aangepaste of basislabels voor gegevensgebruik wilt toewijzen aan een statische verzameling. [&#x200B; leer meer over de Controle van de Toegang van het Niveau van Objecten (OLAC) &#x200B;](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >Het gebruik van OLAC is niet beschikbaar voor dynamische inzamelingen. Het moet op het niveau van de aanbiedingen worden beheerd. Daarom is het mogelijk dat u geen aanbiedingen in een dynamische verzameling ziet als u geen toegang hebt tot een van deze aanbiedingen.

1. Zodra de inzameling wordt gecreeerd, toont het in de lijst. U kunt het selecteren om het uit te geven of te schrappen.

   ![](../assets/collection_created.png)

## Hoe kan ik-video {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329376?quality=12)


