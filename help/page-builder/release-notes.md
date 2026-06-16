---
title: Notes de mise à jour de  [!DNL Page Builder]
description: Consultez les notes de mise à jour pour plus d’informations sur toutes  [!DNL Page Builder]  versions.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
TQID: https://experienceleague.adobe.com/gw4-6vCpburzac-VmejAMajwHjHNCTPmVkBUi5qOsuk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 2839
ht-degree: 0%

---

# Notes de mise à jour de [!DNL Page Builder]

Ces notes de mise à jour décrivent les versions d’[!DNL Page Builder] et incluent les éléments suivants :

![Nouveau](../assets/new.svg) Nouvelles fonctionnalités

![Correction d’un problème](../assets/fix.svg) Correctifs et améliorations

![Problème connu](../assets/bug.svg) Problèmes connus

>[!IMPORTANT]
>
>À compter de la version 2.4.3, [!DNL Page Builder] est désormais disponible sous la forme d’une extension groupée dans Magento Open Source. Il s’agit désormais de l’outil d’édition de contenu par défaut pour Adobe Commerce et Magento Open Source et peut remplacer l’éditeur WYSIWG par tout module tiers.

## 1.7.2 pour Commerce 2.4.5

![Nouveau](../assets/new.svg) **Nouvelle entité wrapper - Conteneur [!DNL Columns] introduit pour les mises en page de colonne** - Auparavant, les utilisateurs ne pouvaient ajouter des colonnes qu’à l’intérieur d’un autre type de contenu conteneur/wrapper, tel qu’un [!DNL Tab] ou un [!DNL Row]. Désormais, le [!DNL Column] possède son propre wrapper et peut être ajouté directement sur scène. En outre, le conteneur [!DNL Columns] comporte un élément settings dans lequel les utilisateurs peuvent spécifier la configuration pour cette entité wrapper.<!--- PB-500-->

![Nouveau](../assets/new.svg) **Nouvelles options de menu pour dupliquer, masquer et supprimer des groupes de colonnes** - Grâce à ces nouvelles options, les utilisateurs peuvent dupliquer, masquer et supprimer des groupes de [!DNL Columns], tout comme ils le peuvent avec les types de contenu.<!--- PB-507-->

![Nouveau](../assets/new.svg) <!-- Issue 594 -->**Nouvelle prise en charge des colonnes multilignes ajoutée au groupe de colonnes** - Avec cet ajout, les utilisateurs peuvent manipuler plusieurs lignes de colonnes à l’intérieur d’un groupe de [!DNL Columns] pour rendre les dispositions des colonnes beaucoup plus flexibles.
<!--- PB-108-->

Voir [Disposition - Colonne](./column.md) pour plus d’informations sur l’utilisation du nouveau groupe de [!DNL Columns].

## 1.7.1 pour Commerce 2.4.4

![Problème résolu](../assets/fix.svg) Page Builder est désormais compatible avec PHP 8.1.<!--- AC-1300-->

![Correction d’un problème](../assets/fix.svg) les commerçants peuvent désormais ajouter un texte secondaire (`alt_text`) aux images (image, bannière, diapositive) pour améliorer l’accessibilité du contenu.<!--- PB-1193-->

![Correction d’un problème](../assets/fix.svg) Les utilisateurs administrateurs disposant d’autorisations limitées à la modification de contenu ne voient plus d’erreur lors de l’utilisation de Page Builder pour ajouter un widget de produit à une page CMS. Page Builder affiche également un nombre précis de produits sur la page des paramètres du widget. Auparavant, Page Builder nécessitait des autorisations sur le module Catalogue lors de la récupération du nombre de produits et affichait cette erreur : `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problème résolu](../assets/fix.svg) Les problèmes d’affichage liés au menu Format de Page Builder sont désormais résolus avec la mise à niveau de la bibliothèque TinyMCE 5. <!--- AC-446-->

![Correction d’un problème](../assets/fix.svg) Vous pouvez désormais utiliser la souris pour modifier une valeur **Texte à afficher** dans la fenêtre contextuelle Insérer un lien. <!--- AC-982-->

![Problème résolu](../assets/fix.svg) Page Builder affiche désormais toutes les options comme prévu dans le menu Options de taille de police. Auparavant, toutes les options n’étaient pas affichées. <!--- AC-1056-->

![Correction d’un problème](../assets/fix.svg) Mise à niveau de la dépendance du compositeur d’`phpgt/dom` pour l’extension `magento/magento2-page-builder` vers les dernières versions. <!--- magento/magento2-page-builder/pull/779-->

![Correction d’un problème](../assets/fix.svg) Page Builder ne redimensionne plus les boîtes de dialogue Insérer un lien et Insérer une image lors de l’affichage du curseur dans une petite colonne. <!--- AC-973-->

![Correction d’un problème](../assets/fix.svg) Le menu Propriétés du tableau de Page Builder s’affiche désormais comme prévu. <!--- AC-407-->

![Problème résolu](../assets/fix.svg) Les points de curseur ne s’affichent plus sur la fenêtre modale Insérer un lien ou une image lorsque la souris ne survole pas le curseur. <!--- AC-406-->

![Problème résolu](../assets/fix.svg) La taille de police utilisée pour afficher les options du menu Tableau a été optimisée. <!--- AC-396-->

![Correction d’un problème](../assets/fix.svg) Correction des anomalies de positionnement des boîtes de dialogue Insérer/Modifier l’image et Insérer/Modifier le lien. <!--- AC-397-->

![Problème résolu](../assets/fix.svg) Page Builder ne renvoie plus d’erreur lorsque vous cliquez sur **Éditeur de texte** pour une bannière. <!--- AC-398-->

![Problème résolu](../assets/fix.svg) Page Builder ne convertit plus tous les blocs dynamiques en une seule langue lors de la mise à niveau. <!--- MC-42265-->

## 1.6.0 pour Adobe Commerce 2.4.2

![Nouveau](../assets/new.svg) <!-- Issue 558 -->**Nouveau style de [!DNL Page Builder]** - [!DNL Page Builder] a apporté des améliorations considérables à la manière dont il définit le style du contenu. Les modifications facilitent désormais la création de sélecteurs CSS simples pour remplacer les styles de type de contenu existants. Ces modifications permettent de créer des thèmes [!DNL Page Builder] avec une réactivité élevée pour tous les types de contenu.

![Nouveau](../assets/new.svg) <!-- Issue 429 -->**Conteneur de lignes désormais facultatif** - Vous pouvez désormais créer du contenu dans [!DNL Page Builder] sans avoir besoin de conteneur de lignes. Outre la ligne, vous pouvez désormais faire glisser et déposer directement sur la scène les types de contenu suivants : HTML, Bloc, Bloc dynamique, Colonnes et Onglets.

![Nouveau](../assets/new.svg) <!-- Issue 636 -->**Nouveau sélecteur de fenêtres d’affichage réactives** - Vous pouvez désormais prévisualiser le contenu de votre [!DNL Page Builder] à différentes largeurs d’appareil (points d’arrêt) à l’aide des nouveaux boutons du sélecteur de fenêtres d’affichage d’administration au-dessus de la scène. Le sélecteur de fenêtre d’affichage simule le style de votre contenu lorsqu’il est affiché sur le storefront à l’aide de différents appareils.

![Nouveau](../assets/new.svg) <!-- Issue 637 -->**Nouveaux champs de formulaire spécifiques au point d’arrêt** - Les valeurs des champs de type Contenu peuvent désormais être définies sur des points d’arrêt de fenêtre spécifiques. Les indicateurs d’icône en regard des champs affichent la fenêtre d’affichage à laquelle la valeur du champ de type de contenu est appliquée.

![Nouveau](../assets/new.svg) <!-- Issue 559 -->**Entrées de champ de formulaire prédéfini supprimées** - Les paramètres avancés des formulaires pour les marges, les marges intérieures et les propriétés liées aux bordures (bordure, largeur de bordure et rayon de bordure) sont désormais définis comme `default`, de sorte que les valeurs peuvent être définies par le CSS d’un module.

![Nouveau](../assets/new.svg) <!-- Issue 635, 557,  -->**Ajout de l’espacement d’étape** - Les lignes et les colonnes fournissent désormais des espaces supplémentaires autour des types de contenu contenus sur l’étape, mais pas sur le storefront. L’espacement d’étape supplémentaire facilite l’accès aux menus d’option de pointage de la souris pour les types de contenu conteneur et contenu .

![Problème résolu](../assets/fix.svg) <!-- MC-37348 -->**Correction du défilement automatique vers les avis** - Le défilement automatique vers les avis de produits sur le storefront est désormais corrigé.

![Problème résolu](../assets/fix.svg) <!-- MC-36227 -->**Contenu recadré fixe** - La longueur des descriptions de catégories et de produits n’est plus recadrée.

![Problème résolu](../assets/fix.svg) <!-- MC-35402 -->**Correction du contenu de catégorie pleine largeur et fond perdu** - Le contenu de catégorie peut désormais être affiché dans une disposition pleine largeur ou fond perdu.

![Correction d’un problème](../assets/fix.svg) <!-- MC-37989 -->**Améliorations apportées à la sécurité**

## 1.5.1 pour Adobe Commerce 2.4.1-p1

![Correction d’un problème](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Affichage d’erreur** - Correction d’un problème en raison duquel [!DNL Page Builder] affichait une erreur lors de l’ajout de sous-catégories de catalogue dans l’administration.

## 1.5.0 pour Adobe Commerce 2.4.1

![Nouveau](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Immersif, modification en plein écran** - La modification du contenu [!DNL Page Builder] est désormais en plein écran uniquement pour toutes les zones contrôlées par [!DNL Page Builder]. Cette modification inclut les pages CMS, les pages Produit et Catégorie, les blocs et les blocs dynamiques. La modification en plein écran met l’accent sur votre contenu et fournit une vue qui correspond mieux à l’expérience utilisateur sur le storefront.

![Nouveau](../assets/new.svg) aperçu de contenu <!-- Issue 544 -->**[!DNL Page Builder]**- Par défaut, [!DNL Page Builder] fournit désormais des aperçus de contenu non seulement pour les pages CMS, les blocs et les blocs dynamiques, mais également pour les pages Produit et Catégorie. Vous pouvez activer ou désactiver cette fonctionnalité pour les pages Produit et Catégorie à l’aide du nouveau paramètre d’aperçu de contenu [!DNL Page Builder], accessible dans la configuration du magasin sous Gestion de contenu > Outils de contenu avancés.

![Nouveau](../assets/new.svg) <!-- Issue 543 -->**Amélioration de l’accès aux descriptions courtes de produits** - Par défaut, une description courte de produit s’affiche désormais avant la description longue. Cette modification entraîne une correspondance avec l’ordre dans lequel ils apparaissent sur le storefront, et évite d’avoir à faire défiler le contenu de la description longue pour accéder à la description courte.

![Nouveau](../assets/new.svg) <!-- Issue 419 -->**Empêché les liens imbriqués dans les bannières et les diapositives** - L’ajout de liens vers le contenu et les éléments externes des bannières et des diapositives a créé des liens imbriqués qui ne s’affichaient pas ou ne se comportaient pas correctement sur le storefront. Pour résoudre ce problème, il n’est plus possible d’ajouter des liens à *à la fois* dans la zone Texte du message et dans l’attribut Lien pour les bannières et les diapositives.

![Problème résolu](../assets/fix.svg) <!-- Issue 421 --> Problème résolu où la définition d’un rayon de bordure vide sur un élément d’onglet provoquait des erreurs et interrompait le contenu de l’élément d’onglet.

![Problème résolu](../assets/fix.svg) <!-- Issue 422 --> problème résolu où l’ajout de certaines combinaisons de conditions au filtre Condition des produits provoquait des erreurs qui empêchaient l’enregistrement du formulaire Produits.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 425 -->correction d’un problème en raison duquel le type de contenu Curseur ne se comportait pas correctement lorsque le paramètre Boucle infinie était désactivé.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 426 -->Correction du prix minimum annoncé afin qu’il fonctionne désormais en [!DNL Page Builder].

![Correction d’un problème](../assets/fix.svg) <!-- Issue 436 -->correction d’un problème dans Safari et IE 11 qui empêchait le glisser-déposer d’une image dans la zone de chargement des bannières et des diapositives.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 525 -->correction d’un problème en raison duquel le type de contenu Curseur n’était pas réactif dans Firefox.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 567 -->correction d’un problème en raison duquel la configuration du widget créait des sélecteurs incorrects dans le DOM pour les différentes apparences.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 609 -->correction du problème en raison duquel la barre d’outils En-tête masquait le menu d’options du type de contenu, ce qui empêchait l’accès au formulaire et à d’autres options.

![Problème résolu](../assets/fix.svg) <!-- Issue 612, 613 -->Correction de problèmes en raison desquels les curseurs et plusieurs lignes utilisant des arrière-plans parallaxe ne s’affichaient pas correctement après plusieurs basculements en mode plein écran.

![Correction d’un problème](../assets/fix.svg) <!--MC-35220-->correction d’un problème en raison duquel une tentative de copie du contenu d’un type de contenu En-tête vers un type de contenu Texte empêchait l’enregistrement du [!DNL Page Builder].

![Correction d’un problème](../assets/fix.svg) <!-- MC-34620 -->correction du type de contenu texte pour gérer et enregistrer correctement les caractères non latins-1.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34679 -->correction [!DNL Page Builder] styles CSS qui entraînait un rendu incorrect par Safari 13.1 du menu de site du thème Luma pour les petits ports d’affichage et les écrans mobiles.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34848 -->correction du type de contenu HTML pour afficher correctement les widgets incorporés tels que « Classer par SKU » sur le Storefront.

## 1.4.1 pour Adobe Commerce 2.4.0-p1

![Nouveau](../assets/new.svg) <!-- PB-590 --> mis à niveau vers TinyMCE 4. Suppression de TinyMCE 3 pour améliorer la sécurité.

## 1.4.0 pour Adobe Commerce 2.4.0

![Nouveau](../assets/new.svg) <!-- PB-494 -->Ajout de la prise en charge de PHP 7.4.

![Correction d’un problème](../assets/fix.svg) <!-- MC-31247 -->Correction d’un problème en raison duquel le type de contenu Produits n’affichait pas les produits configurables lorsque la condition était définie sur le prix.

![Correction d’un problème](../assets/fix.svg) <!-- PB-179 -->Correction de la configuration de l’alignement des produits pour positionner uniquement le conteneur de produits lui-même, et non le contenu du conteneur de produits, tel que le nom, le prix, les boutons, les images et d’autres éléments du produit.

![Correction d’un problème](../assets/fix.svg) <!-- MC-33556 -->Amélioration des performances.

![Correction d’un problème](../assets/fix.svg) Améliorations apportées à la sécurité.

## 1.3.3-p1 pour Adobe Commerce 2.3.6-p1

![Correction d’un problème](../assets/fix.svg) Améliorations apportées à la sécurité.

## 1.3.3 pour Adobe Commerce 2.3.6

![Correction d’un problème](../assets/fix.svg) <!-- MC-32766 -->Correction du type de contenu texte pour enregistrer correctement les directives de variable ajoutées aux attributs HTML.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34590 -->correction du type de contenu texte pour gérer et enregistrer correctement les caractères non latins-1.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34677 -->correction [!DNL Page Builder] styles CSS qui entraînait un rendu incorrect par Safari 13.1 du menu de site du thème Luma pour les petits ports d’affichage et les écrans mobiles.

![Problème résolu](../assets/fix.svg) <!-- MC-34846 -->Correction du type de contenu HTML pour afficher correctement les widgets incorporés tels que _Classer par SKU_ sur le storefront.

![Correction d’un problème](../assets/fix.svg) Correction d’une erreur qui empêchait parfois les utilisateurs d’enregistrer les formulaires de type contenu. L’erreur (« [!DNL Page Builder] a effectué le rendu pendant 5 secondes sans libérer les verrous ») a entraîné la rotation indéfinie de l’icône du chargeur après avoir tenté d’enregistrer un formulaire.

## 1.3.2 pour Adobe Commerce 2.3.5-p2

![Nouveau](../assets/new.svg) Améliorations de la sécurité.

## 1.3.1 pour Adobe Commerce 2.3.5-p1

Cette version de [!DNL Page Builder] est simplement une mise à jour de numéro de version pour Adobe Commerce 2.3.5-p1. Toutes les fonctionnalités décrites pour la version 1.3.0 s’appliquent également à cette version.

## 1.3.0 pour Adobe Commerce 2.3.5

![Nouveau](../assets/new.svg) **Modèles** - [!DNL Page Builder] dispose désormais de modèles qui peuvent être créés à partir de contenu existant et appliqués à de nouvelles zones de contenu. Les modèles [!DNL Page Builder] enregistrent le contenu et les mises en page des pages, blocs, blocs dynamiques, attributs de produit et descriptions de catégorie existants. Par exemple, vous pouvez enregistrer une page [!DNL Page Builder] CMS existante en tant que modèle, puis appliquer ce modèle (avec tout son contenu et ses mises en page) pour créer rapidement des pages CMS pour votre site. Cette nouvelle fonctionnalité est documentée ici : [Modèles](templates.md).

![Nouveau](../assets/new.svg) **Arrière-plans vidéo pour les lignes, les bannières et les curseurs** : les lignes, bannières et curseurs [!DNL Page Builder] peuvent désormais utiliser des vidéos pour leurs arrière-plans. Ces nouvelles fonctionnalités sont documentées ici : [Lignes](row.md), [Bannières](banner.md), [Sliders](slider.md).

![Nouveau](../assets/new.svg) **Prise en charge de la vidéo : ajouts et améliorations** - [!DNL Page Builder] prend désormais en charge une plus grande variété de formats vidéo. Outre les vidéos YouTube et Vimeo, le type de contenu Vidéo et les fonds vidéo prennent désormais en charge les liens URL vers des formats vidéo tels que `.mp4` et d’autres formats pris en charge par le navigateur. Le type de contenu Vidéo ajoute également une fonction de lecture automatique. Ces nouvelles fonctionnalités sont documentées ici : [type de contenu vidéo](video.md).

![Nouveau](../assets/new.svg) **Lignes, bannières et curseurs pleine hauteur** - [!DNL Page Builder] Les lignes, bannières et curseurs peuvent désormais définir leur hauteur sur la hauteur totale de la page à l’aide d’un nombre avec n’importe quelle unité CSS (px, %, vh, em) ou d’un calcul entre les unités (100 vh - 237 px). Ces nouvelles fonctionnalités sont documentées ici : [Lignes](row.md), [Bannières](banner.md), [Sliders](slider.md).

![Nouveau](../assets/new.svg) **Bibliothèque de mise à niveau des types de contenu** - L’équipe de développement peut désormais créer des versions de [!DNL Page Builder] types de contenu sans introduire de problèmes de rétrocompatibilité avec les versions précédentes. Avant cette version, les modifications importantes apportées aux configurations de type de contenu créaient des problèmes d’affichage et de perte de données avec les types de contenu [!DNL Page Builder] précédemment enregistrés. La nouvelle bibliothèque de mise à niveau élimine ces problèmes. La bibliothèque est conçue pour mettre à niveau les versions précédentes des types de contenu enregistrés dans la base de données afin qu’elles correspondent aux modifications de configuration dans les nouvelles versions. [!DNL Page Builder] exécute la bibliothèque de mise à niveau sur les types de contenu natifs selon les besoins de la nouvelle version. Cette modification garantit que les types de contenu [!DNL Page Builder] intégrés sont toujours mis à niveau pour correspondre aux modifications apportées aux types de contenu pour une version plus récente.

>[!IMPORTANT]
>
>Si vous avez créé des entités de base de données supplémentaires pour stocker [!DNL Page Builder] contenu, vous _devez_ ajouter ces entités à votre `etc/di.xml`. Dans le cas contraire, le contenu [!DNL Page Builder] stocké dans votre entité n’est pas mis à jour, ce qui peut entraîner des pertes de données et des problèmes d’affichage. Par exemple, si vous avez créé une entité de blog qui stocke [!DNL Page Builder] contenu, vous devez ajouter votre entité de blog à votre fichier `etc/di.xml` en tant que type de `UpgradableEntitiesPool` afin que la bibliothèque de mise à niveau puisse mettre à jour les types de contenu [!DNL Page Builder] utilisés dans votre blog. Pour plus d’informations et d’instructions sur l’utilisation de la bibliothèque de mise à niveau, consultez [Mettre à niveau les types de contenu](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) dans le _Guide de développement de Page Builder_.

![Nouveau](../assets/new.svg) **Documentation pour l’ajout de nouvelles apparences** - Les informations de développement sont désormais publiées sur [l’ajout d’apparences](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) pour les types de contenu existants ou personnalisés.

![Problème résolu](../assets/fix.svg) **Divers correctifs**

- &#x200B;<!-- PB-50 -->Correction d’un problème en raison duquel le menu Minuscule pour le contenu d’une diapositive s’affichait sous d’autres types de contenu si le conteneur parent de la diapositive était dupliqué.
- &#x200B;<!-- PB-166 -->Mise à jour de la [!DNL Page Builder] pour implémenter une méthode de destruction afin d’éviter les fuites de mémoire dans certains scénarios.
- &#x200B;<!-- PB-170 -->Amélioration des performances de TinyMCE lorsque plusieurs instances sont utilisées sur l’étape d’administration.
- &#x200B;<!-- PB-252 -->Correction d’un problème en raison duquel le type de contenu Bloc dynamique n’était pas rendu sur l’étape d’administration si la ligne supérieure était marquée comme masquée.
- &#x200B;<!-- PB-273 -->Amélioration des événements de pointage de la souris sur l’étape d’administration en supprimant un délai de 200 ms de divers contrôles de l’interface utilisateur. Cette modification facilite le travail avec les éléments de contenu imbriqués sur la scène.
- &#x200B;<!-- PB-294 -->Correction d’un problème en raison duquel le symbole de devise était placé dans une séquence d’échappement incorrecte dans le widget Liste de produits au sein du bloc ou du bloc dynamique sur l’étape d’administration.
- &#x200B;<!-- PB-296 -->Correction d’un problème en raison duquel le total de produits du panneau d’édition de [!DNL Page Builder] ne fonctionnait pas pour les produits MSI Stock personnalisés.
- &#x200B;<!-- PB-317 -->Correction d’un problème en raison duquel l’enregistrement de contenu [!DNL Page Builder] avec des images d’arrière-plan sur Microsoft Edge n’effectue pas le rendu de ces images sur le storefront.
- &#x200B;<!-- PB-390 -->Correction d’un problème en raison duquel l’enregistrement du contenu [!DNL Page Builder] imbriqué échouait si les utilisateurs cliquaient sur le bouton Enregistrer avant que la page ne soit complètement rendue.
- &#x200B;<!-- PB-418 -->Correction d’une erreur d’exception déclenchée dans les tâches cron en raison d’analyses [!DNL Page Builder].

## 1.2.2 pour Adobe Commerce 2.3.4-p2

![Nouveau](../assets/new.svg) Améliorations de la sécurité.

## 1.2.1 pour Adobe Commerce 2.3.4-p1

![Nouveau](../assets/new.svg) Améliorations de la sécurité.

## 1.2.0 pour Adobe Commerce 2.3.4

![Nouveau &#x200B;](../assets/new.svg) intégration **[!DNL Page Builder]à PWA Studio** - Ajout du rendu de contenu [!DNL Page Builder] à l’application Venia dans PWA Studio. [!DNL Page Builder] contenu peut désormais être affiché dans l’application PWA Studio Venia. Consultez la documentation [!DNL Page Builder] dans [PWA Studio] pour obtenir toutes les informations sur cette nouvelle fonctionnalité.

![Nouveau](../assets/new.svg) **Carrousel de produits ajouté** - <!-- PB-77, PB-173, PB-175 -->Le type de contenu Produits offre désormais une option permettant d’afficher vos produits dans un format de carrousel/curseur, y compris plusieurs options permettant de personnaliser le carrousel en fonction de vos besoins.

![Nouveau](../assets/new.svg) **Tri des SKU de produit ajoutés** - <!-- PB-69 -->Le type de contenu Produits offre désormais une option pour trier vos produits par SKU dans l’ordre dans lequel vous les ajoutez à une liste dans l’Administration.

![Nouveau](../assets/new.svg) **Tri de catégorie de produits ajouté** - <!-- PB-181 -->. Le type de contenu Produits offre désormais une option permettant de trier vos produits par catégorie _position_, en les affichant dans l’ordre dans lequel ils apparaissent dans votre catalogue Commerce.

![Nouveau](../assets/new.svg) **Totaux de sélection de produits ajoutés** - <!-- PB-107 -->. L’éditeur d’administration du type de contenu Produits affiche désormais le nombre total de produits qui correspondent à vos options de sélection de produits.

![Problème résolu](../assets/fix.svg) **Divers correctifs**

- &#x200B;<!-- PB-237 -->Améliorations de la sécurité.
- &#x200B;<!-- PB-41 -->Correction des recherches dans les composants de sélection de l’interface utilisateur pour ne générer qu’une seule requête AJAX par terme de recherche.
- &#x200B;<!-- PB-76, PB-84-->Mise à jour des aperçus du produit dans l’interface d’administration pour qu’ils correspondent au storefront, y compris l’évaluation par étoiles, la couleur et les options de taille du produit, le cas échéant.
- &#x200B;<!-- PB-169 -->Correction d’un problème en raison duquel la [!DNL Page Builder] ne pouvait pas être enregistrée lorsque la minimisation et le regroupement JavaScript étaient activés dans Commerce.
- &#x200B;<!-- PB-241 -->Correction des aperçus Admin des produits, des blocs et des blocs dynamiques pour qu’ils s’affichent correctement sur les installations Commerce qui définissent des URL différentes pour l’administrateur et le serveur frontal.
- &#x200B;<!-- PB-238 -->Correction des aperçus Admin des produits, des blocs et des blocs dynamiques pour effectuer correctement le rendu sur les installations Commerce avec B2B installé avec l’option _Connexion seule_ activée. Avant cette correction, l’aperçu [!DNL Page Builder] entraînait la redirection de la page vers la connexion au compte client.
- &#x200B;<!-- PB-239 -->Correction d’une erreur de session qui pouvait se produire lors de la prévisualisation d’une grande page dans l’administrateur [!DNL Page Builder].
- &#x200B;<!-- PB-248 -->Mise à jour des styles [!DNL Page Builder] LESS pour éviter la duplication des styles de storefront.

## 1.1.1 pour Adobe Commerce 2.3.3-p1

![Nouveau](../assets/new.svg) Améliorations de la sécurité.

## 1.1.0 pour Adobe Commerce 2.3.3

![Nouveau](../assets/new.svg) <!-- MC-15250 -->Ajout d’un tri explicite des produits au type de contenu Produits.

![Nouveau](../assets/new.svg) <!-- MC-17823 -->Ajout de boutons pour insérer des images, des widgets et des variables dans le type de contenu HTML.

![Correction d’un problème](../assets/fix.svg) Amélioration de la sécurité [!DNL Page Builder].

![Correction d’un problème](../assets/fix.svg) <!-- MC-1805 -->Mise à jour de la [!DNL Page Builder] pour la prise en charge de PHP version 7.3.

![Correction d’un problème](../assets/fix.svg) <!-- MC-4137 -->Mise à jour de TinyMCE vers la version 4.9.5. Cette mise à jour, ainsi que les améliorations supplémentaires, ont corrigé plusieurs problèmes liés à l’éditeur en ligne TinyMCE :

- Les variables, images et liens d’image sont ajoutés à l’endroit où se trouve le curseur.
- Les tableaux et les cellules des tableaux peuvent être alignés au centre.
- Copier/coller colle maintenant le contenu à l’emplacement du curseur.
- Les liens peuvent être appliqués au texte sélectionné.
- Les puces sont correctement alignées.
- Les modifications apportées à l’éditeur intégré peuvent être enregistrées sans cliquer d’abord en dehors de l’éditeur.

![Correction d’un problème](../assets/fix.svg) <!-- MC-3880 -->correction d’un problème en raison duquel la hauteur minimale et l’alignement vertical étaient incohérents entre les sections du panneau d’édition pour chaque type de contenu.

![Correction d’un problème](../assets/fix.svg) <!-- MC-14994 -->correction d’un problème en raison duquel la barre d’outils du type de contenu En-tête se trouvait incorrectement lorsqu’elle était déposée pour la première fois sur la scène.

![Correction d’un problème](../assets/fix.svg) <!-- MC-15742 -->correction de marges codées en dur dans les types de contenu Slider et Vidéo.

![Correction d’un problème](../assets/fix.svg) <!-- MC-16241 -->correction d’un problème en raison duquel le symbole astérisque requis s’affichait deux fois sur les champs du formulaire.

## 1.0.3 pour Adobe Commerce 2.3.2-p2

![Nouveau](../assets/new.svg) Améliorations de la sécurité.

## 1.0.2 pour Adobe Commerce 2.3.2-p1

![Nouveau](../assets/new.svg) Améliorations de la sécurité.

## 1.0.1 pour Adobe Commerce 2.3.2

![Nouveau](../assets/new.svg) Garantit la compatibilité avec Adobe Commerce 2.3.2.

## 1.0.0 pour Adobe Commerce 2.3.1

![Nouvelle](../assets/new.svg) Mise à jour de la disponibilité générale


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
