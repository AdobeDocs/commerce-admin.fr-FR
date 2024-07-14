---
title: '[!DNL AR Viewer] pour la configuration Adobe Commerce'
description: Découvrez comment gérer des ressources de modèle 3D à l’aide de l’extension  [!DNL AR Viewer] pour vos listes de produits.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Gestion des modèles 3D de produit avec [!DNL AR Viewer] pour Adobe Commerce

Pour chaque produit, vous pouvez charger un fichier `.USDZ` qui permet l’utilisation de modèles AR et 3D dans votre liste de produits.

[!DNL AR Viewer] ne prend en charge que les fichiers `.USDZ`.

## Installation de l’extension

[!DNL AR Viewer] est installé en tant qu&#39;extension à partir de [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Pour plus d’informations sur le processus d’installation de l’extension, consultez le [_Guide d’installation_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Une fois l’extension [!DNL AR Viewer] installée et configurée, les utilisateurs administrateurs peuvent configurer, personnaliser et gérer les listes de produits pour inclure des modèles 3D.

## Ajout d’un modèle 3D

1. Ouvrez le produit en mode d’édition.

1. Pour utiliser une vue de magasin spécifique, définissez le programme de sélection **[!UICONTROL Store View]** sur la vue applicable.

   >[!NOTE]
   >
   >Les nouveaux modèles 3D de produit sont _toujours_ chargés et visibles dans les _toutes_ vues de magasin, même si la portée `All Store Views` n’est pas utilisée pour le chargement. <br/><br/>Pour masquer un modèle 3D de produit d’une vue de magasin spécifique, vous devez passer à cette vue de magasin, cocher la case **[!UICONTROL Hide from Product Page]** du modèle 3D et cliquer sur **[!UICONTROL Save]**.

1. Faites défiler l’écran vers le bas et développez la section _[!UICONTROL Product 3D Model]_.

   ![Menu déroulant](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Ajoutez le modèle 3D (`.USDZ` fichier) du produit.

1. Cliquez sur **[!UICONTROL Save]**.

### Suppression d’un modèle 3D

Pour supprimer un modèle 3D des détails du produit :

1. Cliquez sur **[!UICONTROL Delete]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Affichage des modèles 3D de produit

Lorsque les détails du produit sont mis à jour avec le modèle 3D :

1. [!DNL AR Viewer] génère un code QR dans la description du produit qui code le fichier AR.

1. Un client peut voir ce code QR dans la page du produit.

1. Lorsque les clients analysent le code QR avec leurs appareils mobiles, une expérience AR est générée sur l’appareil mobile.

>[!NOTE]
>
> Pour une série de vidéos de démonstration d’un utilisateur ajoutant un modèle 3d à un produit, consultez la page [Visionneuse d’AR pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) dans _Vidéos et Tutorials Commerce_.
