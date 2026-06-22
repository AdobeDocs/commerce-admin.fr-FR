---
title: Espace de travail du produit
description: Découvrez les paramètres et les commandes disponibles dans l’espace de travail du produit.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
TQID: https://experienceleague.adobe.com/O9e0Z-bHxbokLZd4RbT1puWWAGWnF7SDqvGcc4Bteco
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 467
ht-degree: 0%

---

# Espace de travail du produit

L’espace de travail du produit est globalement identique pour tous les types de produits, bien que la sélection des champs change en fonction du jeu d’attributs utilisé. Les attributs de produit se trouvent dans la partie supérieure du formulaire, suivis de sections extensibles d’informations sur les produits. Lorsqu’un nouveau produit est enregistré pour la première fois, le sélecteur de _[!UICONTROL Store View]_&#x200B;s’affiche dans le coin supérieur gauche du formulaire.

![Espace de travail du produit](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## paramètre [!UICONTROL Enable Product]

L’état en ligne du produit est indiqué par le commutateur en haut du formulaire. Pour modifier le statut en ligne, définissez le commutateur de **[!UICONTROL Enable Product]** sur `Yes` ou `No`.

| Contrôle | Description |
|-------- | ----------- |
| ![Activer/désactiver oui](../assets/toggle-yes.png) | Indique que le produit est en ligne. |
| ![Basculer no](../assets/toggle-no.png) | Indique que le produit est hors ligne. |

{style="table-layout:auto"}

## Jeu d’attributs

Le nom du [jeu d’attributs](attribute-sets.md) s’affiche dans le coin supérieur gauche et détermine les champs qui apparaissent dans l’enregistrement du produit. Pour choisir un autre jeu d’attributs, cliquez sur la flèche vers le bas en regard du nom du jeu d’attributs par défaut.

![Jeu d’attributs](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Développer/réduire

Pour développer ou réduire une section, cliquez sur l’icône de développement ![Sélecteur de développement](../assets/icon-display-expand.png) ou de réduction ![Sélecteur de réduction](../assets/icon-display-collapse.png).

## [!UICONTROL Save] menu

Le menu _[!UICONTROL Save]_&#x200B;comprend plusieurs options permettant d’enregistrer et de continuer, d’enregistrer et de créer un produit, d’enregistrer et de dupliquer le produit ou d’enregistrer et de fermer le produit.

![Enregistrer le menu](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Commande | Description |
|--- |--- |
| [!UICONTROL Save] | Enregistrer le produit actuel et continuer à travailler. |
| [!UICONTROL Save & New] | Enregistrez et fermez le produit actuel, puis démarrez un nouveau produit basé sur le même type de produit et le même modèle. |
| [!UICONTROL Save & Duplicate] | Enregistrez et fermez le produit actuel, puis ouvrez un nouveau duplicata. |
| [!UICONTROL Save & Close] | Enregistrer le produit actif et revenir à l’espace de travail _[!UICONTROL Products]_. |

{style="table-layout:auto"}

## Valeurs de champ par défaut

Pour gagner du temps lors de la création de produits, la valeur par défaut de plusieurs champs de produit fait référence à des valeurs d’un autre champ. Vous pouvez accepter la valeur par défaut ou en saisir une autre. Les champs suivants ont généré automatiquement des valeurs par défaut :

| Champ | Par défaut |
|----- |------- |
| [!UICONTROL SKU] | En fonction du nom du produit. |
| [!UICONTROL Meta Title] | En fonction du nom du produit. |
| [!UICONTROL Meta Keywords] | En fonction du nom du produit. |
| [!UICONTROL Meta Description] | En fonction du nom et de la description du produit. |

{style="table-layout:auto"}

Les espaces réservés qui représentent la valeur d’un autre champ sont entourés de doubles accolades. Tout code d’attribut inclus dans le produit [jeu d’attributs](attribute-sets.md) peut être utilisé comme espace réservé.

![Génération automatique des champs de produit](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Pour obtenir la liste détaillée de ces paramètres, voir [Génération automatique des champs de produit](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) dans le _Guide de référence de configuration_.

### Modifier la valeur de l’espace réservé

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL Product Fields Auto-Generation]** et apportez les modifications nécessaires aux valeurs de l’espace réservé.

   Par exemple, si vous souhaitez inclure un mot-clé spécifique pour chaque produit ou expression à inclure dans chaque méta-description, saisissez directement la valeur dans le champ approprié.

   >[!NOTE]
   >
   >Si vous souhaitez conserver les valeurs d’espace réservé existantes, conservez les accolades doubles qui encadrent chaque balise.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### Espaces réservés courants

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`

