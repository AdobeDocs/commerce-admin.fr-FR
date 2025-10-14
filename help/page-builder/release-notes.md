---
title: Notes de mise à jour de  [!DNL Page Builder]
description: Consultez les notes de mise à jour pour plus d’informations sur toutes les versions de  [!DNL Page Builder]  .
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Notes de mise à jour pour [!DNL Page Builder]

Ces notes de mise à jour décrivent les versions de [!DNL Page Builder] et incluent :

![New](../assets/new.svg) Nouvelles fonctionnalités

![Problème corrigé](../assets/fix.svg) Correctifs et améliorations

![Problème connu](../assets/bug.svg) Problèmes connus

>[!IMPORTANT]
>
>À compter de la version 2.4.3, [!DNL Page Builder] est désormais disponible en tant qu’extension groupée en Magento Open Source. Il s’agit désormais de l’outil d’édition de contenu par défaut pour Adobe Commerce et Magento Open Source. Il peut remplacer l’éditeur WYSIWG par n’importe quel module tiers.

## 1.7.2 pour Commerce 2.4.5

![Nouvelle &#x200B;](../assets/new.svg) **Nouvelle entité wrapper - [!DNL Columns] conteneur introduit pour les dispositions de colonnes** - Auparavant, les utilisateurs pouvaient ajouter des colonnes uniquement dans un autre type de contenu container/wrapper, tel qu’un [!DNL Tab] ou un [!DNL Row]. Désormais, le [!DNL Column] a son propre wrapper et peut être ajouté directement sur scène. De plus, le conteneur [!DNL Columns] comporte un élément settings où les utilisateurs peuvent spécifier la configuration de cette entité wrapper.<!--- PB-500-->

![&#x200B; Nouveau &#x200B;](../assets/new.svg) **Nouvelles options de menu pour dupliquer, masquer et supprimer des groupes de colonnes** - Grâce à ces nouvelles options, les utilisateurs peuvent dupliquer, masquer et supprimer des groupes [!DNL Columns] — comme ils le peuvent avec les types de contenu.<!--- PB-507-->

![Nouveau](../assets/new.svg) <!-- Issue 594 -->**Nouvelle prise en charge de colonnes multilignes ajoutée au groupe de colonnes** - Avec cet ajout, les utilisateurs peuvent manipuler plusieurs lignes de colonnes dans un groupe [!DNL Columns] pour rendre les dispositions de colonnes beaucoup plus flexibles.<!--- PB-108-->

Voir [Disposition - Colonne](./column.md) pour plus d’informations sur l’utilisation du nouveau groupe [!DNL Columns].

## 1.7.1 pour Commerce 2.4.4

![Problème corrigé](../assets/fix.svg) Le Créateur de pages est désormais compatible avec PHP 8.1.<!--- AC-1300-->

![Problème corrigé](../assets/fix.svg) Les vendeurs peuvent désormais ajouter un texte alternatif (`alt_text`) aux images (image, bannière, diapositive) pour améliorer l’accessibilité du contenu.<!--- PB-1193-->

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) Les utilisateurs administrateurs disposant d’autorisations limitées à la modification du contenu ne voyaient plus d’erreur lors de l’utilisation du Créateur de pages pour ajouter un widget de produit à une page CMS. Page Builder affiche également un nombre de produits précis sur la page des paramètres du widget. Auparavant, Page Builder nécessitait des autorisations pour le module Catalog lors de la récupération du nombre de produits et affichait cette erreur : `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problème corrigé](../assets/fix.svg) Les problèmes d’affichage avec le menu Format du générateur de pages sont désormais résolus avec la mise à niveau de la bibliothèque TinyMCE 5. <!--- AC-446-->

![Problème corrigé](../assets/fix.svg) Vous pouvez désormais utiliser la souris pour modifier une valeur **Texte à afficher** dans la fenêtre contextuelle Insérer un lien. <!--- AC-982-->

![Problème corrigé](../assets/fix.svg) Le Créateur de pages affiche désormais toutes les options comme prévu dans le menu Options Taille de police. Auparavant, toutes les options n’étaient pas affichées. <!--- AC-1056-->

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) Mise à niveau de la dépendance du compositeur `phpgt/dom` pour l’extension `magento/magento2-page-builder` vers les versions les plus récentes. <!--- magento/magento2-page-builder/pull/779-->

![Problème corrigé](../assets/fix.svg) Le générateur de pages ne redimensionne plus les boîtes de dialogue Insérer un lien et Insérer une image lors de l’affichage du curseur dans une petite colonne. <!--- AC-973-->

![Problème corrigé](../assets/fix.svg) Le menu Propriétés du tableau du générateur de pages s’affiche désormais comme prévu. <!--- AC-407-->

![Problème corrigé](../assets/fix.svg) Les points du curseur ne s’affichent plus sur le modal Insérer lien ou image lorsque la souris ne survole pas le curseur. <!--- AC-406-->

![Problème corrigé](../assets/fix.svg) La taille de police utilisée pour afficher les options du menu Tableau a été optimisée. <!--- AC-396-->

![Correction d’un problème](../assets/fix.svg) Correction des anomalies avec le positionnement des boîtes de dialogue Insérer/Modifier l’image et Insérer/Modifier le lien . <!--- AC-397-->

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) Le Créateur de pages ne renvoie plus d’erreur lorsque vous cliquez sur l’ **Éditeur de texte** pour une bannière. <!--- AC-398-->

![Problème corrigé](../assets/fix.svg) Le Créateur de pages ne convertit plus tous les blocs dynamiques en une seule langue lors de la mise à niveau. <!--- MC-42265-->

## 1.6.0 pour Adobe Commerce 2.4.2

![Nouveau](../assets/new.svg) <!-- Issue 558 -->**Nouveau [!DNL Page Builder] style** - [!DNL Page Builder] a apporté des améliorations massives à la manière dont il stylise le contenu. Les modifications facilitent désormais la création de sélecteurs CSS simples pour remplacer les styles de type de contenu existants. Ces modifications permettent de créer des thèmes [!DNL Page Builder] avec une réactivité riche pour tous les types de contenu.

![Nouveau](../assets/new.svg) <!-- Issue 429 -->**Conteneur de lignes désormais facultatif** - Vous pouvez désormais créer du contenu dans [!DNL Page Builder] sans avoir besoin d’un conteneur de lignes. Outre la ligne, vous pouvez désormais faire glisser et déposer directement sur la scène les types de contenu suivants : HTML, Bloc, Bloc dynamique, Colonnes et Onglets.

![Nouveau](../assets/new.svg) <!-- Issue 636 -->**Nouveau sélecteur de fenêtre réactive** - Vous pouvez désormais prévisualiser votre contenu [!DNL Page Builder] à différentes largeurs d’appareil (points d’arrêt) à l’aide des nouveaux boutons de sélecteur de fenêtre d’administration au-dessus de la scène. Le sélecteur de fenêtre d’affichage simule le style de votre contenu lorsqu’il est affiché sur le storefront à l’aide de différents appareils.

![New](../assets/new.svg) <!-- Issue 637 -->**Nouveaux champs de formulaire spécifiques à un point d’arrêt** - Les valeurs de champ de type de contenu peuvent désormais être définies sur des points d’arrêt de fenêtre d’affichage spécifiques. Les indicateurs d’icône en regard des champs indiquent la fenêtre d’affichage à laquelle s’applique la valeur du champ de type de contenu.

![Nouveau](../assets/new.svg) <!-- Issue 559 -->**Entrées de champ de formulaire prédéfinies supprimées** - Les paramètres de formulaire avancés pour les marges, les plages et les propriétés liées aux bordures (bordure, largeur de bordure et rayon de bordure) sont désormais définis comme `default`, de sorte que les valeurs puissent être définies par le CSS d’un module.

![Nouveau](../assets/new.svg) <!-- Issue 635, 557,  -->**Ajout de l’espacement dans les scènes** - Les lignes et les colonnes offrent désormais des espaces supplémentaires autour des types de contenu contenus contenus sur la scène, mais pas sur le storefront. L’espacement des scènes supplémentaire facilite l’accès aux menus des options de survol avec la souris pour les types de contenu conteneur et contenu.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-37348 -->**Correction du défilement automatique vers les révisions** - Le défilement automatique vers les révisions de produits sur le storefront est désormais résolu.

![&#x200B; Problème corrigé &#x200B;](../assets/fix.svg) <!-- MC-36227 -->**Contenu recadré** : la catégorie longue et les descriptions de produits ne sont plus recadrées.

![&#x200B; Problème corrigé &#x200B;](../assets/fix.svg) <!-- MC-35402 -->**Contenu de catégorie à fond plein vide fixe** : le contenu de la catégorie peut désormais s’afficher dans une disposition pleine largeur ou fond perdu.

![Correction d’un problème](../assets/fix.svg) <!-- MC-37989 -->**Améliorations de la sécurité**

## 1.5.1 pour Adobe Commerce 2.4.1-p1

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Affichage d’erreur** - Correction d’un problème en raison duquel [!DNL Page Builder] affichait une erreur lors de l’ajout de sous-catégories de catalogue dans l’administrateur.

## 1.5.0 pour Adobe Commerce 2.4.1

![Nouveau](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Modification immersive en plein écran** - La modification de contenu [!DNL Page Builder] est désormais en plein écran uniquement pour toutes les zones contrôlées par [!DNL Page Builder]. Cette modification inclut les pages CMS, les pages de produits et de catégories, les blocs et les blocs dynamiques. La modification en plein écran met l’accent sur votre contenu et fournit une vue qui correspond mieux à l’expérience de l’utilisateur sur le storefront.

![Nouvel &#x200B;](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] aperçus de contenu &#x200B;**- Par défaut, [!DNL Page Builder] fournit désormais des aperçus de contenu non seulement pour les pages CMS, les blocs et les blocs dynamiques, mais également pour les pages de produits et de catégories. Vous pouvez configurer cette fonction pour qu’elle soit activée ou désactivée pour les pages de produits et de catégories à l’aide du nouveau paramètre [!DNL Page Builder] Aperçu de contenu, accessible dans la configuration du magasin sous Gestion de contenu > Outils de contenu avancé.

![New](../assets/new.svg) <!-- Issue 543 -->**Accès amélioré aux descriptions courtes de produit** - Par défaut, une brève description de produit s’affiche maintenant avant la description plus longue. Cette modification entraîne une correspondance avec l’ordre dans lequel ils apparaissent sur le storefront et évite la nécessité de faire défiler le contenu de description plus longue pour accéder à la brève description.

![Nouveau](../assets/new.svg) <!-- Issue 419 -->**Liens imbriqués empêchés dans les bannières et les diapositives** - L’ajout de liens vers le contenu et les éléments externes des bannières et des diapositives a créé des liens imbriqués qui ne s’affichaient pas ou ne se comportaient pas correctement sur le storefront. Pour résoudre ce problème, les liens ne peuvent plus être ajoutés à *la zone Texte du message et l’attribut Lien pour les bannières et les diapositives*.

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 421 --> en raison duquel la définition du rayon de bordure vide sur un élément d’onglet provoquait des erreurs et endommageait le contenu de l’élément d’onglet.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 422 --> Correction d’un problème en raison duquel l’ajout de certaines combinaisons de conditions au filtre Condition des produits provoquait des erreurs qui empêchaient l’enregistrement du formulaire Produits.

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 425 --> en raison duquel le type de contenu du curseur ne se comportait pas correctement lorsque le paramètre Boucle infinie était désactivé.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 426 --> Correction du prix publicitaire minimum de sorte qu’il fonctionne désormais dans [!DNL Page Builder].

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 436 --> Correction d’un problème dans Safari et IE 11 qui empêchait de faire glisser une image vers la zone de chargement dans les bannières et les diapositives.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 525 --> Correction d’un problème en raison duquel le type de contenu du curseur ne réagissait pas dans Firefox.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 567 --> Correction d’un problème en raison duquel la configuration du widget créait des sélecteurs incorrects dans le DOM pour les différentes apparences.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 609 --> Correction d’un problème en raison duquel la barre d’outils En-tête masquait le menu d’options du type de contenu, ce qui empêchait l’accès au formulaire et à d’autres options.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- Issue 612, 613 --> Correction de problèmes en raison desquels les curseurs et plusieurs lignes utilisant des arrière-plans de parallaxe ne s’affichaient pas correctement après avoir basculé plusieurs fois en mode plein écran.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!--MC-35220--> Correction d’un problème en raison duquel la tentative de copie du contenu d’un type de contenu En-tête vers un type de contenu Texte empêchait l’enregistrement de [!DNL Page Builder].

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-34620 --> Correction du type de contenu Texte pour gérer et enregistrer correctement les caractères non latins-1.

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-34679 --> Correction des styles CSS [!DNL Page Builder] en raison desquels Safari 13.1 affichait incorrectement le menu du thème Luma pour les petits ports d’affichage et les écrans mobiles.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-34848 --> Correction du type de contenu HTML pour afficher correctement les widgets incorporés tels que &quot;Ordre par SKU&quot; sur le storefront.

## 1.4.1 pour Adobe Commerce 2.4.0-p1

![Nouveau](../assets/new.svg) <!-- PB-590 --> mis à niveau vers TinyMCE 4. Suppression de TinyMCE 3 pour améliorer la sécurité.

## 1.4.0 pour Adobe Commerce 2.4.0

![Nouveau](../assets/new.svg) <!-- PB-494 --> Ajout de la prise en charge de PHP 7.4.

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-31247 --> en raison duquel le type de contenu Produits n’affichait pas les produits configurables lorsque la condition était définie sur le prix.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- PB-179 --> Correction de la configuration d’alignement Produits pour positionner uniquement le conteneur de produits lui-même, et non le contenu du conteneur de produits, tel que le nom, le prix, les boutons, les images et d’autres éléments.

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-33556 -->Amélioration des performances.

![Correction d’un problème](../assets/fix.svg) améliorations de sécurité.

## 1.3.3-p1 pour Adobe Commerce 2.3.6-p1

![Correction d’un problème](../assets/fix.svg) améliorations de sécurité.

## 1.3.3 pour Adobe Commerce 2.3.6

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-32766 --> Correction du type de contenu Texte pour enregistrer correctement les directives de variable ajoutées aux attributs html.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-34590 --> Correction du type de contenu Texte pour gérer et enregistrer correctement les caractères non latins-1.

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-34677 --> Correction des styles CSS [!DNL Page Builder] en raison desquels Safari 13.1 affichait incorrectement le menu du thème Luma pour les petits ports d’affichage et les écrans mobiles.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-34846 --> Correction du type de contenu d’HTML pour afficher correctement les widgets incorporés tels que _Ordre par SKU_ sur le storefront.

![&#x200B; Correction d’un problème &#x200B;](../assets/fix.svg) qui empêchait parfois les utilisateurs d’enregistrer des formulaires de type contenu. L’erreur (&quot;[!DNL Page Builder] était rendu pendant 5 secondes sans libérer de verrous&quot;) provoquait une rotation indéfinie de l’icône de chargeur après avoir tenté d’enregistrer un formulaire.

## 1.3.2 pour Adobe Commerce 2.3.5-p2

![Nouvelles](../assets/new.svg) améliorations de sécurité.

## 1.3.1 pour Adobe Commerce 2.3.5-p1

Cette version de [!DNL Page Builder] n’est qu’une mise à jour de numéro de version pour Adobe Commerce 2.3.5-p1. Toutes les fonctionnalités décrites pour la version 1.3.0 s’appliquent également à cette version.

## 1.3.0 pour Adobe Commerce 2.3.5

![Nouveau](../assets/new.svg) **Modèles** - [!DNL Page Builder] comporte désormais des modèles qui peuvent être créés à partir de contenu existant et appliqués à de nouvelles zones de contenu. Les modèles [!DNL Page Builder] enregistrent le contenu et les mises en page des pages, blocs, blocs dynamiques, attributs de produit et descriptions de catégorie existants. Par exemple, vous pouvez enregistrer une page CMS [!DNL Page Builder] existante comme modèle, puis appliquer ce modèle (avec tout son contenu et toutes ses mises en page) pour créer rapidement des pages CMS pour votre site. Cette nouvelle fonctionnalité est décrite ici : [Modèles](templates.md).

![Nouveau](../assets/new.svg) **Arrière-plans vidéo pour les lignes, bannières et curseurs** - [!DNL Page Builder] Lignes, bannières et curseurs peuvent désormais utiliser des vidéos pour leurs arrière-plans. Ces nouvelles fonctionnalités sont documentées ici : [Lignes](row.md), [Bannières](banner.md), [Curseurs](slider.md).

![Nouveau](../assets/new.svg) **Ajouts et améliorations de la prise en charge de la vidéo** - [!DNL Page Builder] prend désormais en charge une plus grande variété de formats vidéo. Outre les vidéos YouTube et Vimeo, le type de contenu vidéo et les arrière-plans vidéo prennent désormais en charge les liens URL vidéo vers des formats vidéo tels que `.mp4` et d’autres formats pris en charge par le navigateur. Le type de contenu Vidéo ajoute également une fonction de lecture automatique. Ces nouvelles fonctionnalités sont documentées ici : [Type de contenu vidéo](video.md).

![Nouveau](../assets/new.svg) **Lignes, bannières et curseurs pleine hauteur** - [!DNL Page Builder] Lignes, bannières et curseurs peuvent désormais définir leur hauteur complète à l’aide d’un nombre avec une unité CSS quelconque (px, %, vh, em) ou d’un calcul entre unités (100vh - 237px). Ces nouvelles fonctionnalités sont documentées ici : [Lignes](row.md), [Bannières](banner.md), [Curseurs](slider.md).

![Nouveau](../assets/new.svg) **Bibliothèque de mise à niveau de type de contenu** - Les développeurs peuvent désormais créer des versions de types de contenu [!DNL Page Builder] sans présenter de problèmes rétrocompatibles avec les versions précédentes. Avant cette version, des modifications importantes apportées aux configurations de type de contenu créaient des problèmes d’affichage et de perte de données avec des types de contenu [!DNL Page Builder] précédemment enregistrés. La nouvelle bibliothèque de mise à niveau élimine ces problèmes. La bibliothèque est conçue pour mettre à niveau les versions précédentes des types de contenu enregistrés dans la base de données afin qu’elles correspondent aux modifications de configuration apportées aux nouvelles versions. [!DNL Page Builder] exécute la bibliothèque de mise à niveau sur les types de contenu natifs si nécessaire pour une nouvelle version. Cette modification garantit que les types de contenu [!DNL Page Builder] intégrés sont toujours mis à niveau pour correspondre à toute modification apportée aux types de contenu pour une version plus récente.

>[!IMPORTANT]
>
>Si vous avez créé des entités de base de données supplémentaires pour le stockage de contenu [!DNL Page Builder], vous _devez_ ajouter ces entités à votre `etc/di.xml`. Dans le cas contraire, le contenu [!DNL Page Builder] stocké dans votre entité n’est pas mis à jour, ce qui peut entraîner des pertes de données et des problèmes d’affichage. Par exemple, si vous avez créé une entité de blog qui stocke du contenu [!DNL Page Builder], vous devez ajouter votre entité de blog à votre fichier `etc/di.xml` en tant que type `UpgradableEntitiesPool` afin que la bibliothèque de mise à niveau puisse mettre à jour les types de contenu [!DNL Page Builder] utilisés dans votre blog. Pour plus d’informations et d’instructions sur l’utilisation de la bibliothèque de mise à niveau, voir [Mise à niveau des types de contenu](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) dans le _Guide du développeur de Page Builder_.

![Nouveau](../assets/new.svg) **Documentation pour l’ajout de nouvelles apparences** - Informations pour les développeurs maintenant publiées au sujet de l’ [ajout d’apparences](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) pour les types de contenu existants ou personnalisés.

![Problème corrigé](../assets/fix.svg) **Divers correctifs**

- &#x200B;<!-- PB-50 -->Correction d’un problème en raison duquel le menu TinyMCE pour le contenu d’une diapositive s’affichait sous d’autres types de contenu si le conteneur parent de la diapositive était dupliqué.
- &#x200B;<!-- PB-166 -->Mise à jour de [!DNL Page Builder] pour mettre en oeuvre une méthode de destruction afin d’empêcher les fuites de mémoire dans certains scénarios.
- &#x200B;<!-- PB-170 -->Amélioration des performances de TinyMCE lorsque plusieurs instances sont utilisées sur l’étape d’administration.
- &#x200B;<!-- PB-252 -->Correction d’un problème en raison duquel le type de contenu Bloc dynamique n’était pas rendu sur l’étape Admin si la ligne supérieure était marquée comme masquée.
- &#x200B;<!-- PB-273 -->Événements de survol de la souris perfectionnés sur l’étape d’administration en supprimant un délai de 200 ms des différentes commandes de l’interface utilisateur. Cette modification facilite l’utilisation d’éléments de contenu imbriqués sur la scène.
- &#x200B;<!-- PB-294 -->Correction d’un problème en raison duquel le symbole de devise était échappé de manière incorrecte dans le widget Liste de produits dans le bloc/bloc dynamique de l’étape Admin.
- &#x200B;<!-- PB-296 -->Correction d’un problème en raison duquel le total du produit sur le panneau d’édition [!DNL Page Builder] ne fonctionnait pas pour les produits de stock MSI personnalisés.
- &#x200B;<!-- PB-317 -->Correction d’un problème en raison duquel l’enregistrement du contenu [!DNL Page Builder] avec des images d’arrière-plan sur Microsoft Edge n’affichait pas ces images sur le storefront.
- &#x200B;<!-- PB-390 -->Correction d’un problème qui empêchait l’enregistrement du contenu imbriqué [!DNL Page Builder] si les utilisateurs cliquaient sur le bouton Enregistrer avant que la page ne soit entièrement rendue.
- &#x200B;<!-- PB-418 -->Correction d’une erreur d’exception générée dans les tâches cron en raison de [!DNL Page Builder] analytics.

## 1.2.2 pour Adobe Commerce 2.3.4-p2

![Nouvelles](../assets/new.svg) améliorations de sécurité.

## 1.2.1 pour Adobe Commerce 2.3.4-p1

![Nouvelles](../assets/new.svg) améliorations de sécurité.

## 1.2.0 pour Adobe Commerce 2.3.4

![Nouvelle &#x200B;](../assets/new.svg) **[!DNL Page Builder]intégration avec PWA Studio** - Ajout du rendu de contenu [!DNL Page Builder] à l’application Venia en PWA Studio. Le contenu [!DNL Page Builder] peut désormais être visualisé dans l’application Venia PWA Studio. Consultez la documentation [!DNL Page Builder] dans [PWA Studio] pour toutes les informations sur cette nouvelle fonctionnalité.

![Nouveau](../assets/new.svg) **Nouveau carrousel de produit** - <!-- PB-77, PB-173, PB-175 -->Le type de contenu Produits offre désormais une option pour afficher vos produits dans un format de carrousel/curseur, y compris plusieurs options pour personnaliser le carrousel en fonction de vos besoins.

![Nouveau](../assets/new.svg) **Tri SKU du produit ajouté** - <!-- PB-69 -->Le type de contenu Produits offre désormais une option pour trier vos produits par SKU dans l’ordre dans lequel vous les ajoutez à une liste dans l’administrateur.

![New](../assets/new.svg) **Ajout du tri des catégories de produits** - <!-- PB-181 -->. Le type de contenu Produits offre désormais une option pour trier vos produits par catégorie _position_, les affichant dans l’ordre dans lequel ils apparaissent dans votre catalogue Commerce.

![Nouveau](../assets/new.svg) **Nombre total de sélections de produits ajoutées** - <!-- PB-107 -->. L’éditeur d’administration de type de contenu Produits affiche désormais le nombre total de produits qui correspondent aux options de sélection de produits.

![Problème corrigé](../assets/fix.svg) **Divers correctifs**

- &#x200B;<!-- PB-237 -->Amélioration de la sécurité.
- &#x200B;<!-- PB-41 -->Correction des recherches dans les composants de sélection de l’interface utilisateur afin d’effectuer une seule requête AJAX par terme de recherche.
- &#x200B;<!-- PB-76, PB-84-->Mise à jour des aperçus de produit dans l’administrateur pour qu’ils correspondent au storefront, y compris les options d’évaluation des étoiles, de couleur et de taille du produit, le cas échéant.
- &#x200B;<!-- PB-169 -->Correction d’un problème en raison duquel [!DNL Page Builder] ne pouvait pas être enregistré lorsque la minification et le regroupement JavaScript étaient activés dans Commerce.
- &#x200B;<!-- PB-241 -->Correction des aperçus administrateur des produits, blocs et blocs dynamiques afin qu’ils s’affichent correctement sur les installations Commerce qui définissent différentes URL pour l’administrateur et le serveur frontal.
- &#x200B;<!-- PB-238 -->Correction des aperçus administrateur des produits, blocs et blocs dynamiques pour un rendu correct sur les installations Commerce avec B2B installé avec l’option _Connexion uniquement_ activée. Avant ce correctif, l’aperçu [!DNL Page Builder] provoquait la redirection de la page vers la connexion au compte client.
- &#x200B;<!-- PB-239 -->Correction d&#39;une erreur de session qui pouvait se produire lors de la prévisualisation d&#39;une grande page dans l&#39;administrateur [!DNL Page Builder].
- &#x200B;<!-- PB-248 -->Mise à jour des styles [!DNL Page Builder] LESS pour empêcher la duplication des styles storefront.

## 1.1.1 pour Adobe Commerce 2.3.3-p1

![Nouvelles](../assets/new.svg) améliorations de sécurité.

## 1.1.0 pour Adobe Commerce 2.3.3

![Nouveau](../assets/new.svg) <!-- MC-15250 -->Ajout d’un tri explicite de produits au type de contenu Produits.

![Nouveau](../assets/new.svg) <!-- MC-17823 --> Ajout de boutons pour insérer des images, des widgets et des variables dans le type de contenu HTML.

![Correction d’un problème](../assets/fix.svg) Amélioration de la sécurité [!DNL Page Builder].

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-1805 --> Mise à jour de [!DNL Page Builder] pour prendre en charge la version 7.3 de PHP.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-4137 --> Mise à jour de TinyMCE vers la version 4.9.5. Cette mise à jour, ainsi que les améliorations supplémentaires, ont corrigé plusieurs problèmes de l’éditeur intégré TinyMCE :

- Des variables, des images et des liens d’image sont ajoutés à l’endroit où se trouve le curseur.
- Les tableaux et les cellules de tableau peuvent être centrés.
- Copier/coller colle maintenant le contenu à la position du curseur.
- Les liens peuvent être appliqués au texte sélectionné.
- Les puces sont correctement alignées.
- Les modifications de l’éditeur intégré peuvent être enregistrées sans cliquer au préalable en dehors de l’éditeur.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-3880 --> Correction d’un problème en raison duquel la hauteur minimale et l’alignement vertical étaient incohérents entre les sections du panneau de modification pour chaque type de contenu.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-14994 --> Correction d’un problème en raison duquel la barre d’outils du type de contenu En-tête était mal positionnée lors du premier dépôt sur la scène.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-15742 --> Correction de marges codées en dur dans les types de contenu Curseur et Vidéo.

![Correction d’un problème &#x200B;](../assets/fix.svg) <!-- MC-16241 --> Correction d’un problème en raison duquel le symbole astérisque requis s’affichait deux fois sur les champs du formulaire.

## 1.0.3 pour Adobe Commerce 2.3.2-p2

![Nouvelles](../assets/new.svg) améliorations de sécurité.

## 1.0.2 pour Adobe Commerce 2.3.2-p1

![Nouvelles](../assets/new.svg) améliorations de sécurité.

## 1.0.1 pour Adobe Commerce 2.3.2

![New](../assets/new.svg) Assure la compatibilité avec Adobe Commerce 2.3.2.

## 1.0.0 pour Adobe Commerce 2.3.1

![Nouvelle &#x200B;](../assets/new.svg) Disponibilité générale


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
