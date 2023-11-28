---
title: Renvoie l’attribut
description: Découvrez les attributs de retour et comment créer les attributs nécessaires au traitement des retours sur votre magasin.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Renvoie l’attribut

{{ee-feature}}

Les attributs de retour sont utilisés pour stocker les informations nécessaires pendant le processus de retour de produit. Les attributs par défaut incluent la condition du produit renvoyé, la raison du retour et un champ qui indique comment le retour a été résolu. Le processus de création d’un attribut de retour est similaire à la création d’un [Attribut du client](../customers/attribute-properties.md).

![Admin - Renvoie les attributs](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Création d’un attribut de retour

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Attribute]**.

   ![Nouveau retour - propriétés d’attribut](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Définition des propriétés

1. Pour identifier l’attribut lors de la saisie des données, définissez la variable **[!UICONTROL Default Label]**.

1. Pour **[!UICONTROL Attribute Code]**, saisissez un code qui identifie l’attribut dans le système.

1. Pour déterminer le type de contrôle d’entrée utilisé pour la saisie de données, définissez **[!UICONTROL Input Type]** à l’une des options suivantes :

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Pour que le champ devienne un élément obligatoire, définissez **[!UICONTROL Values Required]** to `Yes`.

1. Pour attribuer une valeur initiale au champ, saisissez une **[!UICONTROL Default Value]**.

1. Pour valider l’exactitude des données saisies dans le champ avant l’enregistrement, définissez **[!UICONTROL Input Validation]** à l’une des options suivantes :

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Pour le `Text Field` et `Text Area` types d’entrée, saisissez **[!UICONTROL Minimum Text Length]** et **[!UICONTROL Maximum Text Length]**.

1. Pour appliquer un filtre de prétraitement, définissez **[!UICONTROL Input/Output Filter]** à l’une des options suivantes :

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Pour rendre l’attribut visible aux clients, définissez **[!UICONTROL Show on Storefront]** to `Yes` dans le _[!UICONTROL Storefront Properties]_.

1. (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer où cet attribut apparaît par rapport aux autres dans la même partie de la page. (`0` = first, `1` = second, `2` = troisième, etc.)

### Gestion des libellés/options

1. Dans le panneau de gauche, choisissez **[!UICONTROL Manage Labels/Options]**.

1. Dans le **[!UICONTROL Manage Titles (Size, Color, etc.)]** , saisissez le libellé de chaque vue de magasin.

   ![Gestion des étiquettes](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Si la variable **[!UICONTROL Input Type]** car l’attribut est `Dropdown`, gérez les options de la variable **[!UICONTROL Manage Options (Values of Your Attribute)]** .

   - Pour ajouter une option, cliquez sur **[!UICONTROL Add Option]** et saisissez le libellé pour Admin et chaque vue de magasin.
   - Pour faire d’une option la valeur par défaut sélectionnée, choisissez **[!UICONTROL Is Default]**.
   - Pour supprimer une option, cliquez sur **[!UICONTROL Delete]**.

1. Pour enregistrer les modifications, cliquez sur **[!UICONTROL Save Attribute]**.
