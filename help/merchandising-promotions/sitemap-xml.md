---
title: Cartes du site
description: Découvrez comment configurer un plan de site pour indexer toutes les pages et images de vos sites Commerce.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# Cartes du site

Une carte du site améliore la manière dont votre boutique est indexée par les moteurs de recherche et est conçue pour trouver des pages qui peuvent être ignorées par les moteurs de recherche web. Un plan du site peut être configuré pour indexer toutes les pages et toutes les images.

Lorsque cette option est activée, Commerce crée un fichier appelé `sitemap.xml` qui est enregistré dans votre installation à l’emplacement spécifié. La configuration permet de définir la fréquence des mises à jour et la priorité de chaque type de contenu. La carte de votre site doit être mise à jour aussi souvent que le contenu de votre site change, ce qui peut être quotidien, hebdomadaire ou mensuel.

Lorsque votre site est en cours de développement, vous pouvez inclure des instructions dans la variable `robots.txt` pour les moteurs de recherche web afin d’éviter l’indexation du site. Avant le lancement, vous pouvez modifier les instructions pour permettre l’indexation du site.

Pour obtenir des informations techniques, voir [Ajout de sitemap et robots.txt][1] dans le _Guide d’infrastructure de Commerce on Cloud_.

![Grille du plan de site](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Étape 1. Configuration de la carte du site

Procédez comme suit : [Configuration du plan de site XML](#site-map-configuration) pour déterminer ce qui est inclus et la fréquence de mise à jour de la carte du site.

## Étape 2. Générer la carte du site

1. Sur le _Administration_ , accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Cliquez sur **[!UICONTROL Add Site Map]**.

   ![Grille de plan de site](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Entrer la carte du site **[!UICONTROL Filename]**. Par exemple: `sitemap.xml`

1. Saisissez le **[!UICONTROL Path]** pour déterminer où se trouve le fichier de carte du site sur le serveur. Assurez-vous que le chemin est modifiable.

   - `/sitemap/` - Place le fichier de carte du site dans un répertoire appelé _sitemap_.

   - `/` - Place le fichier de mappage de site à la racine ou au chemin d’accès de base de votre installation Commerce.

   ![Nouveau plan du site](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save & Generate]**.

   Il peut s’écouler quelques minutes avant que la carte du site n’apparaisse dans la grille.

## Étape 3. Configuration et activation de robots.txt (facultatif)

Procédez comme suit : [robots de moteur de recherche](seo-overview.md#search-engine-robots) configuration avec des instructions qui dirigent les moteurs de recherche pour analyser les parties de votre site que vous souhaitez indexer.

## Étape 4. Envoyer la carte de votre site aux moteurs de recherche

Vous pouvez envoyer la carte de votre site à différents moteurs de recherche en leur fournissant le lien vers la variable `sitemap.xml` dans votre installation Commerce. Pour copier le lien, procédez comme suit :

1. Dans le _Carte du site_ , cliquez avec le bouton droit sur l’URL dans la **[!UICONTROL Link for Google]** colonne .

1. Dans le menu, choisissez **[!UICONTROL Copy Link Address]**.

Pour plus d’informations, voir les instructions relatives au moteur de recherche spécifique. Voici des liens vers des instructions pour deux principaux moteurs de recherche :

- [Google][2]
- [Microsoft® Bing][3]

## Étape 5 : Restaurer les instructions de robot précédentes (facultatif)

Vous pouvez désormais restaurer les restrictions d’origine (par défaut).

## Gestion des plans de site et des robots.txt pour plusieurs sites web

Si vous disposez de plusieurs sites web, vous pouvez simplifier le processus de création et d’envoi de plans de site. Simplement [create](#site-map-configuration) un ou plusieurs plans de site qui incluent des URL pour tous vos magasins vérifiés et enregistrent les plans de site à un seul emplacement. Tous les sites doivent être vérifiés dans [Console de recherche Google](https://support.google.com/webmasters/answer/7451001).

Pour créer des plans de site pour une instance multi-magasin, procédez comme suit :

1. Créez un dossier appelé `sitemaps` à la racine de votre site web, puis créez des sous-dossiers pour chaque domaine :

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Créez ou modifiez les listes de plans de site pour chaque magasin et définissez la variable **[!UICONTROL Path]** à celle que vous avez créée pour le magasin :

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Si nécessaire, mettez à jour votre fichier robots.txt .

   Pour vous assurer que les araignées du moteur de recherche sont correctement dirigées vers les nouveaux plans de site, vous pouvez mettre à jour ou créer le fichier robots.txt . Ajoutez les lignes suivantes en haut.

       Plan du site web
       Plan du site : https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       Plan du site : https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Si votre site utilise la variable [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) moteur de serveur web, vous devez mettre à jour la variable [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) dans la racine de votre site web afin de rediriger toutes les autres requêtes de plan de site vers l’emplacement approprié.

## Descriptions des colonnes

| Colonne | Description |
|------|-----------|
| [!UICONTROL ID] | Numéro d’enregistrement séquentiel de la carte du site actuel. |
| [!UICONTROL Filename] | Nom de fichier de la carte du site. |
| [!UICONTROL Path] | Emplacement où se trouve la carte du site sur le serveur. Par exemple : <br/>`/sitemap/` - Place le fichier de carte du site dans un répertoire appelé _sitemap_, à un niveau situé sous la racine de l’installation de Commerce. <br/>`/` - Place le fichier de mappage de site à la racine ou au chemin d’accès de base de l’installation de Commerce. |
| [!UICONTROL Link for Google] | URL de la carte du site à soumettre à Google et aux autres moteurs de recherche. |
| [!UICONTROL Last Generated] | Indique la date et l’heure de la dernière génération du plan du site. |
| [!UICONTROL Store View] | Vue du magasin où s’applique la carte du site. |
| [!UICONTROL Generate] | Régénère la carte du site. |

{style="table-layout:auto"}

## Configuration de la carte du site

La carte de votre site doit être mise à jour aussi souvent que le contenu de votre site change, ce qui peut être quotidien, hebdomadaire ou mensuel. Le paramétrage permet de définir la fréquence et la priorité de chaque type de contenu.

### Étape 1. Définition de la fréquence et de la priorité des mises à jour du contenu

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL XML Sitemap]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Categories Options]** et procédez comme suit :

   >[!NOTE]
   >
   >Si nécessaire, effacez la variable **[!UICONTROL Use system value]** pour modifier ces paramètres.

   - Définir **[!UICONTROL Frequency]** à l’une des options suivantes :

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - Pour **[!UICONTROL Priority]**, saisissez une valeur entre `0.0` et `1.0`. Zéro a la priorité la plus faible.

   ![Plan du site XML - Options des catégories](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Options des catégories](../configuration-reference/catalog/xml-sitemap.md#categories-options) dans le _Référence de configuration_.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Products Options]** et complétez la section **[!UICONTROL Frequency]** et **[!UICONTROL Priority]** selon les besoins.

   Pour obtenir la liste détaillée de ces options, voir [Options de produits](../configuration-reference/catalog/xml-sitemap.md#products-options) dans le _Référence de configuration_.

1. Pour déterminer la mesure dans laquelle les images sont incluses dans le plan du site, définissez **[!UICONTROL Add Images into Sitemap]** à l’une des options suivantes :

   - `None`
   - `Base Only`
   - `All`

   ![Configuration de catalogue - produits de plan de site XML](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL CMS Pages Options]** et complétez la section **[!UICONTROL Frequency]** et **[!UICONTROL Priority]** selon les besoins.

   ![Configuration du catalogue - pages CMS de plan de site XML](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Options des pages CMS](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) dans le _Référence de configuration_.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Store Url Options]** et complétez la section **[!UICONTROL Frequency]** et **[!UICONTROL Priority]** selon les besoins.

   ![Configuration du catalogue - URL de magasin du plan de site XML](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Options D’Url De Magasin](../configuration-reference/catalog/xml-sitemap.md#store-url-options) dans le _Référence de configuration_.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### Étape 2. Définition des paramètres de génération

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Generation Settings]** .

   Si nécessaire, effacez la variable **Utiliser la valeur système** pour modifier ces paramètres.

   ![Configuration du catalogue - Paramètres de génération du plan de site XML](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Paramètres de génération](../configuration-reference/catalog/xml-sitemap.md#generation-settings) dans le _Référence de configuration_.

1. Pour générer un plan de site, définissez **[!UICONTROL Enabled]** to `Yes` et procédez comme suit :

   - Définir **[!UICONTROL Start Time]** à l’heure, à la minute et à la seconde où vous souhaitez que le plan du site soit mis à jour.

   - Définir **[!UICONTROL Frequency]** à l’une des options suivantes :

      - `Daily`
      - `Weekly`
      - `Monthly`

   - Pour **[!UICONTROL Error Email Recipient]**, saisissez l’adresse électronique de la personne qui doit recevoir la notification en cas d’erreur lors d’une mise à jour du plan du site.

   - Définir **[!UICONTROL Error Email Sender]** au contact du magasin qui apparaît comme expéditeur de la notification d&#39;erreur.

   - Définir **[!UICONTROL Error Email Template]** au modèle utilisé pour la notification d&#39;erreur.

### Étape 3. Définition des limites de fichier de carte du site

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Sitemap File Limits]** .

   ![Configuration du catalogue - limites de fichier du plan de site XML](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Limites des fichiers du plan de site](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) dans le _Référence de configuration_.

1. Pour **[!UICONTROL Maximum No of URLs per File]**, saisissez le nombre maximal d’URL pouvant être incluses dans le plan du site.

   Par défaut, la limite est de 50 000.

1. Pour **[!UICONTROL Maximum File Size]**, saisissez la plus grande taille en octets allouée au plan du site.

   La taille par défaut est de 10 485 760 octets.

### Étape 4. Définition des paramètres d’envoi du moteur de recherche

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Submission Settings]** .

   ![Configuration du catalogue - Paramètres d’envoi du moteur de recherche de plan de site XML](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Si vous utilisez un `robots.txt` afin de fournir des instructions aux moteurs de recherche qui analysent votre site, définissez **[!UICONTROL Enable Submission to Robots.txt]** to `Yes`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
