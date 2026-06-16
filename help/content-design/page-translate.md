---
title: Traduction d’une page de contenu
description: Découvrez comment créer une version traduite de chaque page disponible dans une vue de magasin spécifique.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/9jox-v5fCEhPsaex70yQod--qH-Xnp9dkgmuxJGTZd0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 368
ht-degree: 0%

---

# Traduction d’une page de contenu

Si votre magasin comporte plusieurs vues dans différentes [langues](../stores-purchase/store-localize.md) et que vous avez défini le paramètre régional de chaque vue dans une langue différente, le site est partiellement traduit. L’étape suivante consiste à créer une version traduite de chaque page disponible dans une vue de magasin spécifique. La colonne [!UICONTROL Store View] de la liste des _[!UICONTROL Manage Pages]_&#x200B;affiche chaque vue dont la version de la page est traduite.

Pour traduire une page de contenu, vous devez créer une autre page qui possède la même clé URL que la page d’origine, mais qui est affectée à la vue spécifique du magasin. Ensuite, mettez à jour la page pour la vue spécifique avec le texte traduit. L’exemple suivant montre comment créer une version traduite de la page _À propos de nous_ pour la vue de magasin en espagnol.

## Étape 1 : copiez la clé URL de la page à traduire

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Dans la grille, recherchez la page à traduire et ouvrez en mode _édition_.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** et copiez le **[!UICONTROL URL Key]** dans le presse-papiers.

1. Pour revenir à la grille de _[!UICONTROL Pages]_, cliquez sur **[!UICONTROL Back]**&#x200B;dans la barre de boutons supérieure.

## Étape 2 : ajouter une page pour le contenu traduit

1. Cliquez sur **[!UICONTROL Add New Page]**.

1. Saisissez le **[!UICONTROL Page Title]** traduit.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** et terminez le texte traduit de la page.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** et procédez comme suit :

   - Collez le **[!UICONTROL URL Key]** que vous avez copié à partir de la page d’origine.

   - Saisissez le texte traduit pour les **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** et **[!UICONTROL Meta Description]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Page in Websites]** et définissez **[!UICONTROL Store View]** sur l’affichage du magasin dans lequel la page doit être disponible.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Design]** et définissez les **[!UICONTROL Layout]** de colonne de la page.

1. Cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, actualisez les [caches](../systems/cache-management.md) non valides.

## Étape 3 : vérifier la traduction

Pour vérifier la traduction, accédez au storefront et utilisez le sélecteur de langue pour modifier la vue du magasin.

Notez que certains éléments de la page doivent encore être traduits, notamment les liens du pied de page de l’entreprise [bloc](block-add.md), le [message de bienvenue](../getting-started/storefront-branding.md#change-the-welcome-message) et les [informations sur les produits](../stores-purchase/store-localize.md#localize-products).
