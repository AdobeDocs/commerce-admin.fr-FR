---
title: Intégration d’Adobe Stock
description: Intégrez Adobe Stock à votre instance pour accéder  [!DNL Commerce]  nombreuses ressources multimédias à utiliser dans votre magasin.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 9aec049cfaa12f342d66f45a75af0ce50a23c2c8
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Intégration d’Adobe Stock

Pour accéder à d’innombrables ressources multimédias à utiliser dans votre magasin, intégrez [Adobe Stock](https://stock.adobe.com) à [!UICONTROL Commerce].

![Résultats de la recherche Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Le service Adobe Stock permet aux entreprises d’accéder à des millions de photos, de vecteurs, d’illustrations, de vidéos, de modèles et de ressources 3D organisés, de haute qualité et libres de droits pour tous leurs projets de création. [!DNL Commerce] utilisateurs peuvent rechercher, prévisualiser et acquérir rapidement des licences pour les ressources Adobe Stock. Les utilisateurs peuvent également les enregistrer dans le [espace de stockage multimédia](./media-storage.md), le tout sans quitter l’espace de travail d’administration.

## Conditions préalables

Cette intégration nécessite :

- Un compte [Adobe Developer](https://developer.adobe.com/console/home)
- Adobe Commerce ou Magento Open Source, version 2.3.4 ou ultérieure

L’obtention d’une licence pour les images Adobe Stock requiert :

- Un compte [Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html)
- Un plan [Adobe Stock](https://stock.adobe.com) payant associé au compte

## Intégrer [!DNL Commerce] et Adobe Stock

La configuration de l&#39;intégration d&#39;Adobe Stock pour Adobe Commerce est un processus en deux étapes :

1. [Créer une intégration adobe.developer](#create-an-adobe-developer-integration) pour générer une clé API
1. [Configuration de l’intégration d’Adobe Stock dans Commerce Admin](#configure-the-adobe-stock-integration)

### Création d’une intégration Adobe Developer

1. Accédez à [Adobe Developer Console](https://developer.adobe.com/console/home).

1. Sous _[!UICONTROL Quick Start]_, cliquez sur **[!UICONTROL Create new project]**.

1. Dans le bloc _[!UICONTROL Project overview]_, cliquez sur **[!UICONTROL Add API]**.

1. Sélectionnez **[!UICONTROL Adobe Stock]** dans la liste des intégrations et cliquez sur **[!UICONTROL Next]**.

1. Sélectionnez la **[!UICONTROL Web App]** OAuth 2.0 .

1. Spécifiez la **[!UICONTROL redirect URI]**.

   L’URI de redirection par défaut se présente sous la forme `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, par exemple `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, où :

   - `${HOST}` est votre [!DNL Commerce] nom de domaine complet (par exemple, `https://store.myshop.com`).
   - `${ADMIN_URI}` est votre URI d’administrateur [!DNL Commerce] (tel que `admin_hgkq1l`), qui peut être récupéré en exécutant `magento info:adminuri`.

1. Spécifiez la **[!UICONTROL Redirect URI pattern]**, qui est identique à l’URI de redirection, avec deux différences :

   - Les points (`.`) doivent être précédés de deux barres obliques inverses (`\\`).
   - Ajoutez `.*` à la fin du motif.

   En reprenant l’exemple de l’URI de redirection par défaut précédent, le modèle serait `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`

1. Cliquez sur **[!UICONTROL Next]**.

1. Vérifiez les portées disponibles et cliquez sur **[!UICONTROL Save configured API]**.

1. Sur la page qui suit, copiez vos **[!UICONTROL Client ID]** (clé API) et **[!UICONTROL Client secret]**.

   Ces informations sont utilisées dans les étapes de la section suivante.

### Configuration de l’intégration Adobe Stock

Pour définir la configuration système dans votre administrateur [!DNL Commerce], utilisez les clés _API_ et _Secret client_ générées dans la [section précédente](#create-an-adobeio-integration).

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** et procédez comme suit :

   - Définissez **[!UICONTROL Enabled Adobe Stock]** sur `Yes`.

   - Saisissez votre **[!UICONTROL API Key (Client ID)]**.

   - Saisissez votre **[!UICONTROL Client Secret]**.

   - Cliquez sur **[!UICONTROL Test Connection]** pour valider vos clés.

   ![Configuration avancée - Intégration Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Accordez quelques secondes à la validation. Si vos informations d’identification sont valides, un _vert Connexion réussie !_ le message.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
