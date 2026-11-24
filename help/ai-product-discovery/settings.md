---
title: Paramètres d’enrichissement
description: Configurez la diffusion, les tâches mensuelles de trafic d’agents et les agents AI éligibles partagés par l’enrichissement du catalogue et l’enrichissement du PDP dans la découverte de produits IA.
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# Paramètres d’enrichissement

Utilisez l’onglet **[!UICONTROL Settings]** dans l’espace de travail IA de découverte de produits pour configurer votre instance Adobe Commerce. Une fois configurés, les enrichissements de catalogue et de PDP sont affichés dans l’espace de travail de découverte de produits d’IA.

Les champs de cet onglet identifient l’environnement [!DNL Adobe Commerce] et la vue de magasin auxquels se connecte la découverte de produit IA. Pour la connexion à IMS et les exigences de l’organisation, consultez les [conditions préalables à la découverte de produits de l’IA](prerequisites.md).

1. Dans l’administration, accédez à **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** ou **[!UICONTROL Product Details Page Enrichment]**.
1. Dans la liste **[!UICONTROL Scope]** en haut de la page, sélectionnez la vue de magasin que vous souhaitez configurer ou laissez **[!UICONTROL All Store Views]** pour gérer les paramètres entre les vues de magasin.
1. Ouvrez l’onglet **[!UICONTROL Settings]**.
1. Dans **[!UICONTROL Commerce Configuration]**, développez le panneau d’affichage du magasin étiqueté avec son URL.

   Fournissez les détails de votre environnement [!DNL Adobe Commerce] pour activer le service IA de découverte de produits et les workflows d’audit.

   ![Configuration de Commerce dans l’onglet Paramètres d’enrichissement du catalogue](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. Saisissez les informations de connexion requises pour la vue du magasin.

   - **[!UICONTROL Store View URL]** : URL correspondant à la vue du magasin (par exemple, `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]** : identifiant unique de l’environnement [!DNL Adobe Commerce] auquel la connexion accède.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** et **[!UICONTROL Store View Code]** : codes d’affichage du site web, du magasin et du magasin pour le site web Commerce. Ces valeurs doivent correspondre aux codes de votre administrateur Commerce.
   - **[!UICONTROL Host Name]** : nom d’hôte de votre instance [!DNL Adobe Commerce].
   - **(Facultatif - pour l’enrichissement du catalogue uniquement)** Sous **[!UICONTROL Catalog field limits]**, sélectionnez **[!UICONTROL Limit maximum characters for product name]** et spécifiez la limite de caractères pour les noms de produits générés. Sélectionnez **[!UICONTROL Limit maximum characters for product description]** et spécifiez la limite de caractères pour toutes les descriptions de produit générées.

1. Cliquez sur **[!UICONTROL Save]**.

Après l’enregistrement, attendez la fin de toute tâche de synchronisation ou de validation initiale avant de vous fier aux résultats du catalogue ou de l’audit pour cette vue de magasin. L&#39;affichage des suggestions de produits sur la page **[!UICONTROL Catalog Enrichment]** peut prendre jusqu&#39;à 24 heures.

Pour supprimer une configuration de vue de magasin, développez cette entrée et cliquez sur **[!UICONTROL Delete]**.

## Descriptions des champs {#commerce-connection-fields}

Les champs obligatoires sont identifiés par un astérisque (*) sur le formulaire **[!UICONTROL Commerce Configuration]**.

| Champ | Obligatoire | Description |
| --- | --- | --- |
| URL de la vue Boutique | Oui | URL correspondant à la vue du magasin (par exemple, `https://brand.example.com/fr/`). |
| Identifiant de l’environnement | Oui | Identifiant unique de l&#39;environnement [!DNL Adobe Commerce] auquel la connexion accède. |
| Code du site web | Oui | Code du site web du site web Commerce. |
| Code de magasin | Oui | Code de magasin du site web Commerce. |
| Code d’affichage du magasin | Oui | Affichage de la boutique du site web de Commerce. |
| Nom d’hôte | Oui | Nom d’hôte de votre instance [!DNL Adobe Commerce]. |
| Limites des champs du catalogue (enrichissement du catalogue uniquement) | Non | Définissez des limites de caractères pour les noms et descriptions de produits générés. |
