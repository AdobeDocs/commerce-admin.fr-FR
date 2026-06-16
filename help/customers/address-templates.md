---
title: Modèles d’adresses client
description: Découvrez comment personnaliser les modèles d’adresse du client.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/b8tCsMqk6IQJjs5YWCH4-CNmBPrz-3pdPG7ttH4eawk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# Modèles d’adresses client

{{ee-feature}}

Vous pouvez modifier le modèle qui contrôle le format des adresses de facturation et d’expédition du client qui apparaissent sur les factures imprimées, les livraisons et les remboursements, ainsi que dans le carnet d’adresses du compte client. Si vous souhaitez inclure des informations supplémentaires, vous pouvez créer des [attributs personnalisés](attribute-properties.md) associés au compte client et à l’[adresse](address-attributes.md) et les incorporer dans le modèle.

## Exemple 1 : format court

Pour [!UICONTROL Text One Line] modèle d’adresse :

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Exemple 2 : format long

Pour les modèles d’adresses [!UICONTROL Text], [!UICONTROL HTML] et [!UICONTROL PDF] :

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Modèles d’adresses client](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Modifier l’ordre des champs de l’adresse

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et sélectionnez **[!UICONTROL Customer Configuration]**.

1. Cliquez pour développer la section **[!UICONTROL Address Templates]**.

   Cette section comprend un ensemble distinct d’instructions de formatage pour chacun des éléments suivants :

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Modifiez chaque modèle selon vos besoins, en utilisant les exemples à titre de référence.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
