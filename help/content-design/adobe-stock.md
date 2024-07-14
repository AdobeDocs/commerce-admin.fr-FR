---
title: Intégration Adobe Stock
description: Intégrez Adobe Stock à votre instance  [!DNL Commerce] pour accéder à d’innombrables ressources multimédias à utiliser dans votre boutique.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Intégration Adobe Stock

Pour accéder à d’innombrables ressources multimédias à utiliser dans votre boutique, intégrez [Adobe Stock][adobe-stock] à [!UICONTROL Commerce].

![Résultats de la recherche Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Le service Adobe Stock permet aux entreprises d’accéder à des millions de photos, de vecteurs, d’illustrations, de vidéos, de modèles et de ressources 3D organisés, de haute qualité et libres de droits pour tous leurs projets de création. [!DNL Commerce] utilisateurs peuvent rapidement rechercher, prévisualiser et acquérir sous licence des ressources Adobe Stock. Les utilisateurs peuvent également les enregistrer dans le [stockage multimédia][media-storage], le tout sans quitter l’espace de travail Admin.

## Conditions préalables

Cette intégration requiert :

- Un compte [Adobe Developer][dev-console]
- Adobe Commerce ou Magento Open Source, 2.3.4 ou version ultérieure

L’obtention de licences pour les images Adobe Stock requiert :

- Un [compte d&#39;Adobe][adobe-signin]
- Un abonnement [Adobe Stock][adobe-stock] payant associé au compte

## Intégrer [!DNL Commerce] et Adobe Stock

La configuration de l’intégration Adobe Stock pour Adobe Commerce est un processus en deux étapes :

1. [Création d’une intégration adobe.developer](#create-an-adobe-developer-integration) pour générer une clé API
1. [Configuration de l’intégration Adobe Stock dans Commerce Admin](#configure-the-adobe-stock-integration)

### Création d’une intégration Adobe Developer

1. Accédez au [Adobe Developer Console][dev-console].

1. Sous _[!UICONTROL Quick Start]_, cliquez sur **[!UICONTROL Create new project]**.

1. Dans le bloc _[!UICONTROL Project overview]_, cliquez sur **[!UICONTROL Add API]**.

1. Sélectionnez **[!UICONTROL Adobe Stock]** dans la liste des intégrations et cliquez sur **[!UICONTROL Next]**.

1. Sélectionnez OAuth 2.0 **[!UICONTROL Web App]**.

1. Spécifiez le **[!UICONTROL redirect URI]**.

   L’URI de redirection par défaut se présente sous la forme `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, par exemple `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, où :

   - `${HOST}` est votre nom de domaine [!DNL Commerce] entièrement qualifié (par exemple, `https://store.myshop.com`).
   - `${ADMIN_URI}` est votre URI d’administrateur [!DNL Commerce] (tel que `admin_hgkq1l`), qui peut être récupéré en exécutant `magento info:adminuri`.

1. Spécifiez le **[!UICONTROL Redirect URI pattern]**, qui est identique à votre URI de redirection avec deux différences :

   - Toutes les périodes (`.`) doivent être précédées de deux barres obliques inverses (`\\`).
   - Ajoutez `.*` à la fin du modèle.

   En utilisant l’exemple de l’URI de redirection par défaut précédent, il serait `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Cliquez sur **[!UICONTROL Next]**.

1. Vérifiez les portées disponibles et cliquez sur **[!UICONTROL Save configured API]**.

1. Sur la page qui suit, copiez votre **[!UICONTROL Client ID]** (clé API) et **[!UICONTROL Client secret]**.

   Ces informations sont utilisées dans les étapes de la section suivante.

### Configuration de l’intégration Adobe Stock

Pour définir la configuration système dans votre administrateur [!DNL Commerce], utilisez la _clé API_ et le _secret client_ générés dans la [section précédente][create-integration].

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** et procédez comme suit :

   - Définissez **[!UICONTROL Enabled Adobe Stock]** sur `Yes`.

   - Saisissez votre **[!UICONTROL API Key (Client ID)]**.

   - Saisissez votre **[!UICONTROL Client Secret]**.

   - Cliquez sur **[!UICONTROL Test Connection]** pour valider vos clés.

   ![ Configuration avancée - Intégration Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Donnez quelques secondes à la validation. Si vos informations d’identification sont valides, une _connexion réussie&quot; verte s’affiche.Message_.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
