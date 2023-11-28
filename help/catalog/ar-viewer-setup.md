---
title: '[!DNL AR Viewer] pour la configuration Adobe Commerce'
description: En savoir plus sur la gestion des ressources de modèle 3D à l’aide de [!DNL AR Viewer] pour vos listes de produits.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Gestion des modèles 3D de produit avec la méthode [!DNL AR Viewer] pour Adobe Commerce

Pour chaque produit, vous pouvez charger un `.USDZ` qui permet d’utiliser des modèles AR et 3D dans votre liste de produits.

La variable [!DNL AR Viewer] uniquement prend en charge `.USDZ` fichiers .

## Installation de l’extension

[!DNL AR Viewer] est installé en tant qu’extension à partir de la fonction [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Voir [_Guide d’installation_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) pour plus d’informations sur le processus d’installation de l’extension.

Après la [!DNL AR Viewer] est installée et configurée, les utilisateurs administrateurs peuvent configurer, personnaliser et gérer les listes de produits pour inclure des modèles 3D.

## Ajout d’un modèle 3D

1. Ouvrez le produit en mode d’édition.

1. Pour utiliser une vue de magasin spécifique, définissez la variable **[!UICONTROL Store View]** sélectionnez la vue appropriée.

   >[!NOTE]
   >
   >Les nouveaux modèles 3D de produit sont _always_ chargé et visible dans _all_ vues de magasin, même si la variable `All Store Views` n’est pas utilisée pour le chargement. <br/><br/>Pour masquer un modèle 3D de produit dans une vue de magasin spécifique, vous devez passer à cette vue, puis sélectionner l’option **[!UICONTROL Hide from Product Page]** correspondant au modèle 3D, puis cliquez sur **[!UICONTROL Save]**.

1. Faites défiler l’écran vers le bas et développez _[!UICONTROL Product 3D Model]_.

   ![Menu contextuel](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Ajoutez le modèle 3D (`.USDZ` ) du produit.

1. Cliquez sur **[!UICONTROL Save]**.

### Suppression d’un modèle 3D

Pour supprimer un modèle 3D des détails du produit :

1. Cliquez sur **[!UICONTROL Delete]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Affichage des modèles 3D de produit

Lorsque les détails du produit sont mis à jour avec le modèle 3D :

1. La variable [!DNL AR Viewer] génère un code QR dans la description du produit qui code le fichier AR.

1. Un client peut voir ce code QR dans la page du produit.

1. Lorsque les clients analysent le code QR avec leurs appareils mobiles, une expérience AR est générée sur l’appareil mobile.

>[!NOTE]
>
> Pour une série de vidéos de démonstration d’un utilisateur ajoutant un modèle 3d à un produit, reportez-vous à la section [Visionneuse AR pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) page _Vidéos et Tutorials commerciaux_.
