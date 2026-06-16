---
title: Retourne l’attribut
description: Découvrez les attributs des retours et comment créer les attributs nécessaires au traitement des retours sur votre boutique.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
TQID: https://experienceleague.adobe.com/bKSZbmmyG9CWVIf0GzCgGImzHRIUV8HgD6asutC7lFo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 306
ht-degree: 0%

---

# Retourne l’attribut

{{ee-feature}}

Les attributs de retour sont utilisés pour stocker les informations nécessaires pendant le processus de retour du produit. Les attributs par défaut incluent la condition du produit renvoyé, le motif du renvoi et un champ indiquant comment le renvoi a été résolu. Le processus de création d’un attribut de retour est similaire à la création d’un [attribut du client](../customers/attribute-properties.md).

![Admin - Renvoie les attributs](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Création d’un attribut de retour

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Attribute]**.

   ![Nouveau retour - propriétés des attributs](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Définition des propriétés

1. Pour identifier l’attribut lors de la saisie des données, définissez le **[!UICONTROL Default Label]** .

1. Par **[!UICONTROL Attribute Code]**, saisissez un code qui identifie l’attribut dans le système.

1. Pour déterminer le type de contrôle d&#39;entrée utilisé pour la saisie de données, définissez **[!UICONTROL Input Type]** sur l&#39;une des options suivantes :

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Pour que le champ soit un élément obligatoire, définissez **[!UICONTROL Values Required]** sur `Yes`.

1. Pour attribuer une valeur initiale au champ, saisissez un **[!UICONTROL Default Value]**.

1. Pour valider la précision des données saisies dans le champ avant d’enregistrer l’enregistrement, définissez **[!UICONTROL Input Validation]** sur l’une des valeurs suivantes :

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Pour les types d’entrée `Text Field` et `Text Area`, saisissez les **[!UICONTROL Minimum Text Length]** et **[!UICONTROL Maximum Text Length]**.

1. Pour appliquer un filtre de prétraitement, définissez **[!UICONTROL Input/Output Filter]** sur l’une des options suivantes :

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Pour rendre l’attribut visible pour les clients, définissez **[!UICONTROL Show on Storefront]** sur `Yes` dans la section _[!UICONTROL Storefront Properties]_.

1. (Facultatif) Par **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer où cet attribut apparaît par rapport aux autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

### Gestion des libellés/options

1. Dans le panneau de gauche, choisissez **[!UICONTROL Manage Labels/Options]**.

1. Dans la section **[!UICONTROL Manage Titles (Size, Color, etc.)]** , saisissez le libellé de chaque vue de magasin.

   ![Gérer les libellés](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Si la **[!UICONTROL Input Type]** de l’attribut est `Dropdown`, gérez les options dans la section **[!UICONTROL Manage Options (Values of Your Attribute)]** .

   - Pour ajouter une option, cliquez sur **[!UICONTROL Add Option]** et saisissez le libellé pour Admin et chaque vue de magasin.
   - Pour définir une option sur la valeur par défaut sélectionnée, choisissez **[!UICONTROL Is Default]**.
   - Pour supprimer une option, cliquez sur **[!UICONTROL Delete]**.

1. Pour enregistrer les modifications, cliquez sur **[!UICONTROL Save Attribute]**.
