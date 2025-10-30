---
title: Configurer les étiquettes d'expédition
description: Découvrez comment configurer le magasin pour générer des étiquettes d’expédition.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# Configurer les étiquettes d&#39;expédition

Les paramètres suivants doivent être définis au niveau du produit et dans la configuration de chaque support utilisé pour imprimer des étiquettes. Pour imprimer des étiquettes, tous les opérateurs exigent d&#39;ouvrir un compte. Effectuez ensuite la configuration dans votre boutique pour chaque opérateur que vous prévoyez d’utiliser.

## Exigences de l’opérateur

| [!UICONTROL Carrier] | Conditions requises |
|-------|--------|
| [ USPS ](usps.md) | Nécessite un compte USPS pour l&#39;affranchissement des étiquettes d&#39;expédition. |
| [UPS](ups.md) | Nécessite un compte UPS. Les étiquettes d&#39;expédition ne sont disponibles que pour les expéditions provenant des États-Unis. Des informations d&#39;identification spécifiques aux États-Unis sont requises pour les magasins situés en dehors des États-Unis. |
| [FedEx ](fedex.md) | Nécessite un compte FedEx. Pour les magasins situés à l’extérieur des États-Unis, les étiquettes d’expédition sont prises en charge uniquement pour les envois internationaux. FedEx n&#39;autorise pas les expéditions intérieures provenant de l&#39;extérieur des États-Unis |
| [ DHL ](dhl.md) | Nécessite un compte DHL. Les étiquettes d&#39;expédition ne sont prises en charge que pour les expéditions provenant des États-Unis. |

{style="table-layout:auto"}

## Étape 1 : Vérification du pays de fabrication

Le pays de fabrication est requis pour tous les produits expédiés à l&#39;international par USPS et FedEx. Si plusieurs produits doivent être mis à jour, vous pouvez [importer](../systems/data-import.md) les mises à jour ou utiliser la grille d&#39;inventaire pour mettre à jour plusieurs enregistrements.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Mettez à jour l&#39;enregistrement d&#39;étiquette d&#39;expédition en utilisant l&#39;une des méthodes suivantes.

### Méthode 1 : mise à jour d’un seul enregistrement

1. Dans la grille, recherchez le produit à mettre à jour, puis ouvrez-le en mode d’édition.

1. Mettez à jour le **pays de fabrication** selon les besoins.

   ![Pays de fabrication](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

### Méthode 2 : mise à jour de plusieurs enregistrements

1. Dans la grille, cochez la case de chaque produit à mettre à jour.

   Par exemple, tous les produits fabriqués en Chine.

1. Définissez la commande **[!UICONTROL Actions]** sur `Update Attributes`, puis cliquez sur **[!UICONTROL Submit]**.

1. Dans le formulaire _Mettre à jour les attributs_, recherchez le champ **Pays de fabrication** et cochez la case **Modifier**.

1. Choisissez le pays.

1. Cliquez sur **[!UICONTROL Save]**.

## Etape 2 Vérification des informations de la boutique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Origin]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Street Address]** - Adresse postale du lieu d&#39;expédition. Par exemple, l’emplacement de votre entreprise ou de votre entrepôt. Ce champ est obligatoire pour les étiquettes d&#39;expédition.
   - **[!UICONTROL Street Address Line 2]** - Toute information supplémentaire sur l&#39;adresse, comme l&#39;étage ou l&#39;entrée. L’utilisation de ce champ est recommandée.

   ![Origine](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Dans la section _Ventes_ du panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL USPS]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Secure Gateway URL]** - Le système saisit automatiquement l’URL de la passerelle.
   - **[!UICONTROL Password]** - Le mot de passe est fourni par USPS et vous donne accès à leur système via les services Web.
   - **Longueur, Largeur, Hauteur, Largeur** - Dimensions par défaut du package. Pour que ces champs s’affichent, définissez **[!UICONTROL Size]** sur `Large`.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **FedEx** et vérifiez que les champs suivants sont remplis :

   - Numéro du compteur
   - Clé
   - Mot de passe

   Ces informations sont fournies par l’opérateur et sont nécessaires pour accéder à son système par le biais des services Web.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL General]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Store Information]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Store Name]** - Nom du magasin ou de la vue de magasin.
   - **[!UICONTROL Store Contact Telephone]** - Numéro de téléphone du contact principal pour la vue du magasin ou du magasin.
   - **[!UICONTROL Country]** - Pays dans lequel votre boutique est basée.
   - **[!UICONTROL VAT Number]** - Le cas échéant, le numéro de taxe sur la valeur ajoutée de votre magasin. (Non requis pour les magasins basés aux États-Unis)
   - **[!UICONTROL Store Contact Address]** - Adresse postale du contact principal pour l’affichage du magasin ou du magasin.

1. Si vous disposez de plusieurs magasins et que les informations de contact diffèrent de celles par défaut, définissez **[!UICONTROL Store View]** pour chacun d’eux et vérifiez que les informations sont complètes.

   Si les informations sont manquantes, une erreur s’affiche lorsque vous essayez d’imprimer les étiquettes.

   ![Informations sur le magasin](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.
