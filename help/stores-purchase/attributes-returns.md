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

Les attributs de retour sont utilisés pour stocker les informations nécessaires pendant le processus de retour de produit. Les attributs par défaut incluent la condition du produit renvoyé, la raison du retour et un champ qui indique comment le retour a été résolu. Le processus de création d’un attribut de retour est similaire à la création d’un [attribut du client](../customers/attribute-properties.md).

![Admin - Renvoie les attributs](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Création d’un attribut de retour

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Attribute]**.

   ![Nouveau retour - propriétés d’attribut](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Définition des propriétés

1. Pour identifier l’attribut lors de la saisie des données, définissez **[!UICONTROL Default Label]**.

1. Pour **[!UICONTROL Attribute Code]**, saisissez un code qui identifie l’attribut dans le système.

1. Pour déterminer le type de contrôle d’entrée utilisé pour la saisie de données, définissez **[!UICONTROL Input Type]** sur l’un des paramètres suivants :

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Pour faire du champ un élément obligatoire, définissez **[!UICONTROL Values Required]** sur `Yes`.

1. Pour attribuer une valeur initiale au champ, saisissez une valeur **[!UICONTROL Default Value]**.

1. Pour valider les données entrées dans le champ pour une précision certaine avant l’enregistrement, définissez **[!UICONTROL Input Validation]** sur l’une des options suivantes :

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Pour les types d’entrée `Text Field` et `Text Area`, saisissez les valeurs **[!UICONTROL Minimum Text Length]** et **[!UICONTROL Maximum Text Length]**.

1. Pour appliquer un filtre de prétraitement, définissez **[!UICONTROL Input/Output Filter]** sur l&#39;une des options suivantes :

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Pour rendre l’attribut visible aux clients, définissez **[!UICONTROL Show on Storefront]** sur `Yes` dans la section _[!UICONTROL Storefront Properties]_.

1. (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer où cet attribut s’affiche par rapport aux autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

### Gestion des libellés/options

1. Dans le panneau de gauche, choisissez **[!UICONTROL Manage Labels/Options]**.

1. Dans la section **[!UICONTROL Manage Titles (Size, Color, etc.)]** , saisissez le libellé de chaque vue de magasin.

   ![Gérer les étiquettes](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Si **[!UICONTROL Input Type]** pour l’attribut est `Dropdown`, gérez les options de la section **[!UICONTROL Manage Options (Values of Your Attribute)]**.

   - Pour ajouter une option, cliquez sur **[!UICONTROL Add Option]** et saisissez le libellé Admin et chaque vue de magasin.
   - Pour faire d’une option la valeur par défaut sélectionnée, choisissez **[!UICONTROL Is Default]**.
   - Pour supprimer une option, cliquez sur **[!UICONTROL Delete]**.

1. Pour enregistrer les modifications, cliquez sur **[!UICONTROL Save Attribute]**.
