---
title: Configuration des libellés d’expédition
description: Découvrez comment configurer le magasin pour générer des libellés d’expédition.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Configuration des libellés d’expédition

Les paramètres suivants doivent être définis au niveau du produit et dans la configuration de chaque opérateur utilisé pour imprimer les étiquettes. Pour imprimer des étiquettes, tous les opérateurs exigent que vous ouvriez un compte. Ensuite, effectuez la configuration dans votre magasin pour chaque opérateur que vous prévoyez d’utiliser.

## Exigences de l’opérateur

| [!UICONTROL Carrier] | Conditions |
|-------|--------|
| [USPS](usps.md) | Nécessite un compte USPS. Depuis le 23 février 2018, USPS exige que toutes les étiquettes d’expédition incluent le postage. |
| [UPS](ups.md) | Nécessite un compte UPS. Les étiquettes d’expédition ne sont disponibles que pour les envois qui proviennent d’identifiants spécifiques aux États-Unis. Elles sont requises pour les magasins situés en dehors des États-Unis. |
| [FedEx](fedex.md) | Nécessite un compte FedEx. Pour les magasins situés en dehors des États-Unis, les étiquettes d’expédition sont prises en charge pour les envois internationaux uniquement. FedEx n&#39;autorise pas les envois intérieurs qui proviennent de l&#39;extérieur des États-Unis |
| [DHL](dhl.md) | Nécessite un compte DHL. Les étiquettes d’expédition ne sont prises en charge que pour les envois provenant des États-Unis. |

{style="table-layout:auto"}

## Etape 1 : vérification du pays de fabrication

Le pays de fabrication est requis pour tous les produits qui sont expédiés à l&#39;international par USPS et FedEx. Si vous disposez de nombreux produits qui doivent être mis à jour, vous pouvez effectuer l’une des opérations suivantes : [import](../systems/data-import.md) les mises à jour ou utilisez la grille Inventaire pour mettre à jour plusieurs enregistrements.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Mettez à jour l’enregistrement des libellés d’expédition à l’aide de l’une des méthodes suivantes.

### Méthode 1 : mise à jour d’un seul enregistrement

1. Dans la grille, recherchez le produit à mettre à jour et ouvrez-le en mode d’édition.

1. Mettez à jour le **Pays de fabrication** selon les besoins.

   ![Pays de fabrication](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

### Méthode 2 : mise à jour de plusieurs enregistrements

1. Dans la grille, cochez la case de chaque produit à mettre à jour.

   Par exemple, tous les produits fabriqués en Chine.

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Update Attributes` et cliquez sur **[!UICONTROL Submit]**.

1. Dans le _Mise à jour des attributs_ formulaire, recherchez les **Pays de fabrication** et sélectionnez le champ **Modifier** .

1. Choisissez le pays.

1. Cliquez sur **[!UICONTROL Save]**.

## Étape 2 - Vérification des informations sur le magasin

{{beta2-updates}}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Origin]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Street Address]** - Adresse postale du lieu d’envoi des envois. Par exemple, l’emplacement de votre société ou de votre entrepôt. Ce champ est obligatoire pour les libellés d’expédition.
   - **[!UICONTROL Street Address Line 2]** - Toute information d’adresse supplémentaire, comme le plancher ou l’entrée. Il est recommandé d&#39;utiliser ce champ.

   ![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Dans le _Ventes_ dans le panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL USPS]** et vérifiez que les champs suivants sont remplis :

   - **[!UICONTROL Secure Gateway URL]** - Le système entre automatiquement l’URL de la passerelle.
   - **[!UICONTROL Password]** - Le mot de passe est fourni par USPS et vous donne accès à leur système via les services web.
   - **Longueur, Largeur, Hauteur, Fille** - Dimensions par défaut du module. Pour faire apparaître ces champs, définissez **[!UICONTROL Size]** to `Large`.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **FedEx** et vérifiez que les champs suivants sont renseignés :

   - Nombre de mètres
   - Clé
   - Mot de passe

   Ces informations sont fournies par l’opérateur et sont nécessaires pour accéder à son système par le biais des services Web.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL General]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Store Information]** et vérifiez que les champs suivants sont renseignés :

   - **[!UICONTROL Store Name]** - Nom de la vue de magasin ou de magasin.
   - **[!UICONTROL Store Contact Telephone]** : numéro de téléphone du contact principal pour la vue magasin ou magasin.
   - **[!UICONTROL Country]** - Le pays où votre magasin est basé.
   - **[!UICONTROL VAT Number]** - Le cas échéant, le numéro de taxe sur la valeur ajoutée de votre magasin. (Non requis pour les magasins basés aux États-Unis)
   - **[!UICONTROL Store Contact Address]** - Adresse postale du contact principal pour la vue du magasin ou du magasin.

1. Si vous disposez de plusieurs magasins et que les informations de contact diffèrent de la valeur par défaut, définissez **[!UICONTROL Store View]** pour chaque et vérifiez que les informations sont complètes.

   Si les informations sont manquantes, une erreur s’affiche lorsque vous essayez d’imprimer les libellés.

   ![Informations sur le magasin](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.
