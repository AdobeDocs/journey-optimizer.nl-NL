---
solution: Journey Optimizer
product: journey optimizer
title: Overzicht van gebruikersbeheer
description: Leer hoe u machtigingen definieert en beheert
feature: Access Management
topic: Administration
role: Admin, Architect
level: Intermediate
keywords: machtigingen, rechten, beperkingen, toegang, sandbox
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Aan de slag met toegangsbeheer {#permissions-overview}

Met [!DNL Journey Optimizer] kunt u de machtigingen definiëren en beheren die aan verschillende gebruikers zijn toegewezen. Machtigingen zijn een reeks rechten en beperkingen die toegang tot functies en mogelijkheden in producten toestaan of weigeren.

De controle van de toegang voor [!DNL Journey Optimizer] wordt verstrekt door **Toestemmingen** in Adobe Experience Cloud. Deze functionaliteit gebruikt rollen en beleid, die gebruikers met toestemmingen en zandbakken verbinden.

Als u toegangsbeheer voor Journey Optimizer wilt configureren, moet u over beheerdersrechten voor het systeem of het product beschikken voor uw organisatie. De minimumrol die toestemmingen kan verlenen of intrekken is een productbeheerder. Andere beheerderrollen die toestemmingen kunnen beheren zijn systeembeheerders (geen beperkingen). Zie het [ artikel van het Centrum van de Hulp van Adobe ](https://helpx.adobe.com/enterprise/using/admin-roles.html){target="_blank"} op administratieve rollen voor meer informatie.

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


Gebruikersbeheer in [!DNL Journey Optimizer] is gebaseerd op de volgende belangrijke concepten:

* **[!UICONTROL Roles]**: Rollen verwijzen naar een verzameling gebruikers die dezelfde machtigingen en sandboxen delen. Deze rollen staan u toe om toegang en toestemmingen voor verschillende groepen gebruikers binnen uw organisatie gemakkelijk te beheren. Een rol wordt geleverd met een reeks eenheidsrechten (toestemmingen) die gebruikers toegang tot bepaalde functionaliteit of voorwerpen in de interface verleent.
Met [!DNL Journey Optimizer] kunt u een keuze maken uit een reeks vooraf bestaande **[!UICONTROL Roles]** -indelingen, elk met verschillende machtigingsniveaus, om deze toe te wijzen aan uw gebruikers. Leer meer over de beschikbare **ingebouwde rollen** op [ deze pagina ](ootb-product-profiles.md).

* **[!UICONTROL Permissions]**: Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die aan **[!UICONTROL Roles]** zijn toegewezen. Elke machtiging wordt verzameld onder bronnen, bijvoorbeeld Reis of Aanbiedingen, die de verschillende functies of objecten in [!DNL Journey Optimizer] vertegenwoordigen. Leer meer in de [ niveaus van de Toestemming ](high-low-permissions.md) sectie.

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL Sandboxes]**: virtuele sandboxen verdelen instanties in afzonderlijke, geïsoleerde virtuele omgevingen. Sandboxen worden toegewezen via rollen in Machtigingen. Leer meer over [ gebruikend zandbakken ](sandboxes.md).

* **op voorwerp-gebaseerde toegangsbeheer**: Etiketten om de toegang tot een voorwerp te beperken. Deze aanpak beschermt gevoelige digitale middelen tegen onbevoegde gebruikers en zorgt voor een verdere bescherming van persoonsgegevens. Leer meer over [ op voorwerp-Gebaseerd toegangsbeheer ](object-based-access.md).

* **op attributen-gebaseerde toegangscontrole**: Vergunningen om gegevenstoegang voor specifieke teams of groepen gebruikers te beheren. Op attributen-gebaseerde toegangscontrole laat beheerders toe om toegang tot specifieke voorwerpen en/of mogelijkheden te controleren die op attributen worden gebaseerd. Kenmerken kunnen metagegevens zijn die aan een object worden toegevoegd, zoals een label dat aan een schemaveld of -segment wordt toegevoegd. Een beheerder bepaalt toegangsbeleid dat attributen omvat om de toestemmingen van de gebruikerstoegang te beheren. Leer meer over [ op attributen-gebaseerd toegangsbeheer ](attribute-based-access.md).


## Laten we dieper duiken

Nu u inzicht in de concepten van toegangsbeheer in **[!DNL Journey Optimizer]** hebt, is het tijd om dieper in deze documentatiesecties te duiken beginnen toestemmingen te vormen.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="Machtigingen" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong> de toegang van de Verlening </strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="Ingebouwde machtigingen" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong> Ingebouwde toestemmingen </strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="sandboxen beheren" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong> beheert zandbakken </strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="Toegangsbeheer op basis van kenmerken" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong> Op attributen-Gebaseerd toegangsbeheer </strong></a>
</div>
<p>
</td>
</tr></table>