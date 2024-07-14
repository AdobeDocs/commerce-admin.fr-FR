---
title: Ajout de vidéos de produit
description: Découvrez comment configurer des vidéos de produit pour votre boutique, ce qui nécessite une clé d’API de données YouTube à partir d’un compte Google, et ajouter un lien vidéo pour un produit.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: e439c1082834cbc81f6ccc7ca99e240d649c8b81
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Ajout de vidéos de produit

Pour ajouter une vidéo de produit, vous devez d’abord obtenir une clé API de votre compte Google et la saisir dans la configuration de votre boutique. Vous pouvez ensuite créer un lien vers la vidéo à partir du produit.

## Étape 1 : Obtention de la clé de l’API YouTube

1. Connectez-vous à votre compte Google et rendez-vous sur la [console de développement Google][1].

1. Dans le champ de recherche en haut, saisissez `YouTube Data API v3` et cliquez sur l’icône de recherche.

1. Lorsque la page API s’affiche, assurez-vous qu’elle est activée.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Credentials]**.

1. Selon que vous disposez ou non d’informations d’identification, effectuez l’une des opérations suivantes :

   - Si vous disposez déjà des informations d’identification nécessaires, copiez la clé dans la table _API keys_ .

   - Si vous ne disposez pas encore des informations d’identification pour cette API, cliquez sur **[!UICONTROL Create Credentials]** dans la partie supérieure et suivez les invites pour créer les informations d’identification nécessaires. Sous _Obtenir vos informations d’identification_, copiez la clé API et cliquez sur **[!UICONTROL Done]**.

1. Copiez la clé API dans le Presse-papiers.

1. Cliquez sur l’icône Modifier à droite et définissez les restrictions pour vous assurer que la clé d’API est limitée aux référents corrects.

1. Patientez quelques instants pendant que la clé est générée, puis copiez-la dans le Presse-papiers.

   À l’étape suivante, vous allez coller la clé dans la configuration de votre magasin.

## Étape 2 : configuration de la clé dans Commerce

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et collez votre **[!UICONTROL YouTube API key]**._[!UICONTROL Product Video]_

   ![Configuration de vidéo de produit](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, actualisez le cache.

## Étape 3 : Lien vers la vidéo

1. Ouvrez un produit en mode d’édition.

1. Accédez à la section _[!UICONTROL Images and Videos]_et développez-la.

   ![Images et vidéos](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. cliquez sur **[!UICONTROL Add Video]**.

   Si vous n&#39;avez pas encore configuré votre clé d&#39;API YouTube, cliquez sur **[!UICONTROL OK]** pour continuer. Vous ne pouvez pas créer de lien vers une vidéo YouTube, mais vous pouvez passer par le processus.

1. Pour **[!UICONTROL Url]**, saisissez l’URL de la vidéo YouTube ou Vimeo.

   ![Nouvelle vidéo pour le produit](./assets/product-video-add.png){width="600" zoomable="yes"}

1. Cliquez en dehors du champ et attendez les commentaires sur la clé API ou la vidéo.

   Si tout est extrait, YouTube fournit des informations de base sur la vidéo.

1. Saisissez les **[!UICONTROL Title]** et **[!UICONTROL Description]** de la vidéo.

1. Pour télécharger un **[!UICONTROL Preview Image]**, accédez à l’image et sélectionnez le fichier.

   >[!NOTE]
   >
   >Après le téléchargement, l’image d’aperçu qui s’affiche est automatiquement générée par un fournisseur de services vidéo externe. Vous ne pouvez pas modifier l’image à partir de l’administrateur Adobe Commerce.

1. Si vous préférez utiliser les métadonnées vidéo, cliquez sur **[!UICONTROL Get Video Information]**.

1. Pour déterminer l’utilisation de la vidéo dans le magasin, cochez la case correspondant à chaque **[!UICONTROL Role]** qui s’applique :

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Si l’option de configuration _[!UICONTROL Autostart base video]_est définie sur `Yes` mais que la lecture de la vidéo ne commence pas automatiquement, cela peut être dû aux stratégies de lecture automatique qui sont appliquées par le navigateur et ne peuvent pas être contrôlées par Adobe Commerce. Chaque navigateur pris en charge possède ses propres stratégies de lecture automatique qui peuvent changer au fil du temps et la lecture de votre vidéo risque de ne plus être automatique à l’avenir. La bonne pratique recommandée consiste à ne pas vous fier à la lecture automatique pour les fonctionnalités critiques de l’entreprise et à tester le comportement de lecture automatique de la vidéo dans votre boutique avec chaque navigateur pris en charge.

## Maintenir l’accès aux API

Selon le développeur de Google [Termes et conditions], YouTube peut désactiver l’accès à l’API pour les comptes inactifs depuis plus de 90 jours. Cette occurrence peut empêcher l’affichage de vos vidéos. Pour maintenir l’accès à votre API à jour, utilisez une tâche cron pour effectuer un test ping sur l’API à intervalles réguliers :

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## Référence de champ

| Champ | Description |
|--- |--- |
| [!UICONTROL URL] | URL de la vidéo associée. |
| [!UICONTROL Title] | Titre de la vidéo. |
| [!UICONTROL Description] | Description de la vidéo. |
| [!UICONTROL Preview Image] | Image chargée utilisée comme prévisualisation de la vidéo dans votre magasin. |
| [!UICONTROL Get Video Information] | Récupère les métadonnées vidéo stockées sur le serveur hôte. Vous pouvez utiliser les données d’origine ou les mettre à jour si nécessaire. |
| [!UICONTROL Role] | Détermine la manière dont l’image d’aperçu est utilisée dans votre magasin. Vous pouvez choisir n&#39;importe quelle combinaison d&#39;options : `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` |

{style="table-layout:auto"}

[1]: https://console.developers.google.com/
[Termes et conditions]: https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services
