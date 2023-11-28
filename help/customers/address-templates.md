---
title: Modèles d’adresse client
description: Découvrez comment personnaliser les modèles d’adresse du client.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Modèles d’adresse client

{{ee-feature}}

Vous pouvez modifier le modèle qui contrôle le format des adresses de facturation et d’expédition du client qui apparaissent sur les factures imprimées, les envois et les remboursements, ainsi que dans le carnet d’adresses du compte du client. Si vous souhaitez inclure des informations supplémentaires, vous pouvez créer des [attributs personnalisés](attribute-properties.md) qui sont associés au compte client et [address](address-attributes.md)et les incorporer dans le modèle.

## Exemple 1 : format court

Pour [!UICONTROL Text One Line] modèle d’adresse :

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Exemple 2 : format long

Pour [!UICONTROL Text], [!UICONTROL HTML], et [!UICONTROL PDF] modèles d’adresse :

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Modèles d’adresse client](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Modifier l’ordre des champs d’adresse

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et sélectionnez **[!UICONTROL Customer Configuration]**.

1. Cliquez pour développer la **[!UICONTROL Address Templates]** .

   La section comprend un ensemble distinct d’instructions de mise en forme pour chacun des éléments suivants :

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Modifiez chaque modèle selon vos besoins, à l’aide des exemples à titre de référence.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
