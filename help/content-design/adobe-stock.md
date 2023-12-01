---
title: Intégration Adobe Stock
description: Intégrez Adobe Stock à votre [!DNL Commerce] pour accéder à d’innombrables ressources multimédias à utiliser dans votre magasin.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Intégration Adobe Stock

Pour accéder à d’innombrables ressources multimédia à utiliser dans votre magasin, intégrez [Adobe Stock][adobe-stock] avec [!UICONTROL Commerce].

![Résultats de la recherche Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Le service Adobe Stock permet aux entreprises d’accéder à des millions de photos, de vecteurs, d’illustrations, de vidéos, de modèles et de ressources 3D organisés, de haute qualité et libres de droits pour tous leurs projets de création. [!DNL Commerce] Les utilisateurs peuvent rapidement rechercher, prévisualiser et acquérir sous licence des ressources Adobe Stock. Les utilisateurs peuvent également les enregistrer dans la variable [stockage multimédia][media-storage], le tout sans quitter l’espace de travail Admin.

## Conditions préalables

Cette intégration requiert :

- Un [Adobe Developer][dev-console] account
- Adobe Commerce ou Magento Open Source, 2.3.4 ou version ultérieure

L’obtention de licences pour les images Adobe Stock requiert :

- Un [Compte Adobe][adobe-signin]
- A payé [Adobe Stock][adobe-stock] plan associé au compte

## Intégrer [!DNL Commerce] et Adobe Stock

La configuration de l’intégration Adobe Stock pour Adobe Commerce est un processus en deux étapes :

1. [Création d’une intégration adobe.developer](#create-an-adobe-developer-integration) pour générer une clé API
1. [Configuration de l’intégration Adobe Stock dans l’administrateur Commerce](#configure-the-adobe-stock-integration)

### Création d’une intégration Adobe Developer

1. Accédez au [Console Adobe Developer][dev-console].

1. Sous _[!UICONTROL Quick Start]_, cliquez sur **[!UICONTROL Create new project]**.

1. Dans le _[!UICONTROL Project overview]_block, cliquez sur **[!UICONTROL Add API]**.

1. Sélectionner **[!UICONTROL Adobe Stock]** dans la liste intégrations, puis cliquez sur **[!UICONTROL Next]**.

1. Sélectionnez OAuth 2.0. **[!UICONTROL Web App]**.

1. Spécifiez la variable **[!UICONTROL redirect URI]**.

   L’URI de redirection par défaut se trouve dans le formulaire. `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, par exemple `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, où :

   - `${HOST}` est votre [!DNL Commerce] nom de domaine complet (par exemple, `https://store.myshop.com`).
   - `${ADMIN_URI}` est votre [!DNL Commerce] URI d’administration (comme `admin_hgkq1l`), qui peut être récupéré en exécutant `magento info:adminuri`.

1. Spécifiez la variable **[!UICONTROL Redirect URI pattern]**, qui est identique à votre URI de redirection avec deux différences :

   - N’importe quel point (`.`) doit être précédée de deux barres obliques inversées (`\\`).
   - Ajouter `.*` à la fin du modèle.

   En utilisant l’exemple de l’URI de redirection par défaut précédent, ce serait `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Cliquez sur **[!UICONTROL Next]**.

1. Vérifiez les portées disponibles et cliquez sur **[!UICONTROL Save configured API]**.

1. Sur la page qui suit, copiez votre **[!UICONTROL Client ID]** (clé API) et **[!UICONTROL Client secret]**.

   Ces informations sont utilisées dans les étapes de la section suivante.

### Configuration de l’intégration Adobe Stock

Pour définir la configuration du système dans votre [!DNL Commerce] Admin, utilisez la méthode _Clé API_ et _Client secret_ généré dans la variable [section précédente][create-integration].

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** et procédez comme suit :

   - Définir **[!UICONTROL Enabled Adobe Stock]** to `Yes`.

   - Saisissez votre **[!UICONTROL API Key (Client ID)]**.

   - Saisissez votre **[!UICONTROL Client Secret]**.

   - Cliquez sur **[!UICONTROL Test Connection]** pour valider vos clés.

   ![Configuration avancée - Intégration d’Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Donnez quelques secondes à la validation. Si vos informations d’identification sont valides, un vert s’affiche. _Connexion réussie !_ message.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
