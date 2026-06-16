---
title: '[!DNL AR Viewer] pour la configuration d’Adobe Commerce'
description: Découvrez comment gérer les ressources de modèle 3D à l’aide de l [!DNL AR Viewer] extension pour vos listes de produits.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
TQID: https://experienceleague.adobe.com/6OlcZ4Psm3INgVm7f-Y9JvqfUdmR6Rg48tcigLAHiaE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 313
ht-degree: 0%

---

# Gestion des modèles 3D de produit avec [!DNL AR Viewer] pour Adobe Commerce

Pour chaque produit, vous pouvez charger un fichier `.USDZ` qui permet d’utiliser des modèles AR et 3D dans votre liste de produits.

Le [!DNL AR Viewer] ne prend en charge que les fichiers `.USDZ`.

## Installation de l’extension

[!DNL AR Viewer] est installé en tant qu’extension de [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Pour plus d’informations sur le processus d’installation de l’extension _](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) consultez le[_ Guide d’installation .

Une fois l’extension [!DNL AR Viewer] installée et configurée, les utilisateurs administrateurs peuvent configurer, personnaliser et gérer les listes de produits afin d’inclure des modèles 3D.

## Ajout d’un modèle 3D

1. Ouvrez le produit en mode d’édition.

1. Pour utiliser une vue de magasin spécifique, définissez le sélecteur de **[!UICONTROL Store View]** sur la vue applicable.

   >[!NOTE]
   >
   >Les nouveaux modèles 3D de produit sont _toujours_ chargés et visibles dans les vues de magasin _toutes_, même si la portée du `All Store Views` n’est pas utilisée pour le chargement. <br/><br/>Pour masquer des modèles 3D de produit d’une vue de magasin spécifique, vous devez basculer vers cette vue de magasin, cocher la case **[!UICONTROL Hide from Product Page]** du modèle 3D, puis cliquer sur **[!UICONTROL Save]**.

1. Faites défiler vers le bas et développez la section _[!UICONTROL Product 3D Model]_.

   ![Menu contextuel](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Ajoutez le modèle 3D (fichier `.USDZ`) du produit.

1. Cliquez sur **[!UICONTROL Save]**.

### Suppression d’un modèle 3D

Pour supprimer un modèle 3D des détails du produit :

1. Cliquez sur **[!UICONTROL Delete]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Afficher les modèles 3D du produit

Lorsque les détails du produit sont mis à jour avec le modèle 3D :

1. Le [!DNL AR Viewer] génère un code QR dans la description du produit qui code le fichier AR.

1. Un client peut voir ce code QR sur la page du produit.

1. Lorsque les clients scannent le code QR avec leurs appareils mobiles, une expérience AR est générée sur l’appareil mobile.

>[!NOTE]
>
> Pour visionner une série de vidéos de démonstration d’un utilisateur ajoutant un modèle 3D à un produit, reportez-vous à la page [Visionneuse AR pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) dans _Vidéos et tutoriels Commerce_.
