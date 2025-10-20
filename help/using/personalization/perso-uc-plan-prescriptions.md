---
title: Voorbeelden van template Personalization
description: Journey Optimizer Personalization-voorbeelden
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# E-mail met voorschriften voor het gezondheidsplan {#plan-prescription}

Een profiel bevat gezondheidsplannen en elk plan bevat recepten. Voorschriften hebben verschillende statussen, zoals &quot;gereed&quot;, &quot;terugroepen&quot; of &quot;opgepikt&quot;.

In dit geval, willen wij één enkele e-mail naar elk profiel, met inbegrip van alle recepten verzenden die of klaar zijn om te nemen of worden teruggeroepen. Klik op de onderstaande tabbladen voor meer informatie over de syntaxis die u moet gebruiken om dit te implementeren.

>[!BEGINTABS]

>[!TAB  Gegenereerd Bericht ]

<p>Hallo Jan Doe,</p>
<p>Hier zijn de recepten die klaar zijn om te worden opgepakt of die zijn teruggeroepen:</p>

**Plan A van de Gezondheid**

<ul>

<li>
      <strong> Vereiste identiteitskaart:</strong> pres1 <br>
      <strong> Naam:</strong> Medicatie A <br>
      <strong> Staat:</strong> klaar
   </li>

<li>
      <strong> Vereiste identiteitskaart:</strong> pres2 <br>
      <strong> Naam:</strong> de Wijze B <br>
      <strong> Staat:</strong> herinnering
   </li>

</ul>

**Plan B van de Gezondheid B**

<ul>

<li>
      <strong> Vereiste identiteitskaart:</strong> pres4 <br>
      <strong> Naam:</strong> Verwerking D <br>
      <strong> Staat:</strong> klaar
   </li>

</ul>

>[!TAB  Malplaatje van HTML ]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB  Gegevens van het Profiel ]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]
