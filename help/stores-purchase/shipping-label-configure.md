---
title: Configurer les étiquettes d'expédition
description: Découvrez comment configurer le magasin pour générer des étiquettes d’expédition.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Configurer les étiquettes d&#39;expédition

Les paramètres suivants doivent être définis au niveau du produit et dans la configuration de chaque support utilisé pour imprimer des étiquettes. Pour imprimer des étiquettes, tous les opérateurs exigent d&#39;ouvrir un compte. Ensuite, effectuez la configuration dans votre magasin pour chaque opérateur que vous prévoyez d’utiliser.

## Exigences de l’opérateur

| [!UICONTROL Carrier] | Conditions requises |
|-------|--------|
| [USPS](usps.md) | Nécessite un compte USPS. Depuis le 23 février 2018, USPS exige que toutes les étiquettes d&#39;expédition incluent l&#39;affranchissement. |
| [UPS](ups.md) | Nécessite un compte UPS. Les étiquettes d&#39;expédition ne sont disponibles que pour les expéditions provenant des États-Unis. Des informations d&#39;identification spécifiques aux États-Unis sont requises pour les magasins situés en dehors des États-Unis. |
| [FedEx](fedex.md) | Nécessite un compte FedEx. Pour les magasins situés à l&#39;extérieur des États-Unis, les étiquettes d&#39;expédition sont prises en charge uniquement pour les expéditions internationales. FedEx n&#39;autorise pas les expéditions intérieures provenant de l&#39;extérieur des États-Unis |
| [DHL](dhl.md) | Nécessite un compte DHL. Les étiquettes d&#39;expédition ne sont prises en charge que pour les expéditions provenant des États-Unis. |

{style="table-layout:auto"}

## Étape 1 : Vérification du pays de fabrication

Le pays de fabrication est requis pour tous les produits expédiés à l&#39;international par USPS et FedEx. Si vous disposez de nombreux produits à mettre à jour, vous pouvez effectuer l’une des opérations suivantes : [importer](../systems/data-import.md) l&#39;onglet met à jour ou utilise la grille Inventaire pour mettre à jour plusieurs enregistrements.

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Mettez à jour l&#39;enregistrement de l&#39;étiquette d&#39;expédition en utilisant l&#39;une des méthodes suivantes.

### Méthode 1 : mise à jour d’un seul enregistrement

1. Dans la grille, recherchez le produit à mettre à jour, puis ouvrez-le en mode d’édition.

1. Mettre à jour **Pays de fabrication** en fonction des besoins.

   ![Pays de fabrication](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.

### Méthode 2 : mise à jour de plusieurs enregistrements

1. Dans la grille, cochez la case de chaque produit à mettre à jour.

   Par exemple, tous les produits fabriqués en Chine.

1. Définir le **[!UICONTROL Actions]** contrôle sur `Update Attributes` et cliquez sur **[!UICONTROL Submit]**.

1. Dans le _Mettre à jour les attributs_ formulaire, rechercher le **Pays de fabrication** et sélectionnez le champ **Modification** case à cocher.

1. Choisissez le pays.

1. Clic **[!UICONTROL Save]**.

## Étape 2 Vérification des informations sur le magasin

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Origin]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Street Address]** - Adresse postale du lieu à partir duquel les expéditions sont envoyées. Par exemple, l’emplacement de votre entreprise ou de votre entrepôt. Ce champ est obligatoire pour les étiquettes d&#39;expédition.
   - **[!UICONTROL Street Address Line 2]** - Toute information supplémentaire sur l&#39;adresse, comme l&#39;étage ou l&#39;entrée. L’utilisation de ce champ est recommandée.

   ![Origine](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Dans le _Ventes_ dans le panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL USPS]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Secure Gateway URL]** - Le système saisit automatiquement l’URL de la passerelle.
   - **[!UICONTROL Password]** - Le mot de passe est fourni par USPS et vous donne accès à leur système via les services Web.
   - **Longueur, Largeur, Hauteur, Taille** - Dimensions par défaut du package Pour que ces champs s’affichent, définissez **[!UICONTROL Size]** vers `Large`.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **FedEx** et vérifiez que les champs suivants sont remplis :

   - Numéro du compteur
   - Clé
   - Mot de passe

   Ces informations sont fournies par l’opérateur et sont nécessaires pour accéder à son système par le biais des services Web.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL General]** en dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Store Information]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Store Name]** - Nom du magasin ou de la vue de magasin.
   - **[!UICONTROL Store Contact Telephone]** - Numéro de téléphone du contact principal pour l’affichage du magasin ou du magasin.
   - **[!UICONTROL Country]** - Pays où se trouve votre boutique.
   - **[!UICONTROL VAT Number]** - Le cas échéant, le numéro de TVA de votre magasin. (Non requis pour les magasins situés aux États-Unis)
   - **[!UICONTROL Store Contact Address]** - Adresse postale du contact principal pour l’affichage du magasin.

1. Si vous disposez de plusieurs magasins et que les informations de contact diffèrent de la valeur par défaut, définissez **[!UICONTROL Store View]** pour chaque et vérifiez que les informations sont complètes.

   Si les informations sont manquantes, une erreur s’affiche lorsque vous essayez d’imprimer les étiquettes.

   ![Informations sur la boutique](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.
