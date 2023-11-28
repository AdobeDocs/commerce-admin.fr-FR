---
title: Notes de mise à jour d’ [!DNL Page Builder]
description: Consultez les notes de mise à jour pour plus d’informations sur toutes les [!DNL Page Builder] versions.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# Notes de mise à jour pour [!DNL Page Builder]

Ces notes de mise à jour décrivent les versions de [!DNL Page Builder] et incluent :

![Nouveau](../assets/new.svg) Nouvelles fonctionnalités

![Correction d’un problème](../assets/fix.svg) Correctifs et améliorations

![Problème connu](../assets/bug.svg) Problèmes connus

>[!IMPORTANT]
>
>À compter de la version 2.4.3, [!DNL Page Builder] est désormais disponible en tant qu’extension groupée en Magento Open Source. Il s’agit désormais de l’outil d’édition de contenu par défaut pour Adobe Commerce et Magento Open Source. Il peut remplacer l’éditeur WYSIWG par n’importe quel module tiers.

## 1.7.2 pour Commerce 2.4.5

![Nouveau](../assets/new.svg) **Nouvelle entité wrapper - [!DNL Columns] conteneur introduit pour les dispositions de colonnes** - Auparavant, les utilisateurs ne pouvaient ajouter des colonnes que dans un autre type de contenu conteneur/wrapper, tel qu’une [!DNL Tab] ou [!DNL Row]. Maintenant, le [!DNL Column] possède son propre wrapper et peut être ajouté directement sur scène. En outre, la variable [!DNL Columns] Le conteneur comporte un élément settings où les utilisateurs peuvent spécifier la configuration de cette entité wrapper.<!--- PB-500-->

![Nouveau](../assets/new.svg) **Nouvelles options de menu pour dupliquer, masquer et supprimer des groupes de colonnes** - Grâce à ces nouvelles options, les utilisateurs peuvent dupliquer, masquer et supprimer [!DNL Columns] groupes — comme ils le peuvent avec les types de contenu.<!--- PB-507-->

![Nouveau](../assets/new.svg) <!-- Issue 594 -->**Ajout de la prise en charge des colonnes multilignes au groupe Colonnes** - Avec cet ajout, les utilisateurs peuvent manipuler plusieurs lignes de colonnes dans une seule. [!DNL Columns] pour rendre les mises en page de colonnes beaucoup plus flexibles.<!--- PB-108-->

Voir [Disposition - Colonne](./column.md) pour plus d’informations sur l’utilisation de la nouvelle [!DNL Columns] groupe.

## 1.7.1 pour Commerce 2.4.4

![Correction d’un problème](../assets/fix.svg) Page Builder est désormais compatible avec PHP 8.1.<!--- AC-1300-->

![Correction d’un problème](../assets/fix.svg) Les vendeurs peuvent désormais ajouter un texte alternatif (`alt_text`) aux images (image, bannière, diapositive) afin d’améliorer l’accessibilité du contenu.<!--- PB-1193-->

![Correction d’un problème](../assets/fix.svg) Les utilisateurs administrateurs dont les autorisations sont limitées à la modification du contenu ne voient plus d’erreur lors de l’utilisation du créateur de pages pour ajouter un widget de produit à une page CMS. Page Builder affiche également un nombre de produits précis sur la page des paramètres du widget. Auparavant, le créateur de pages nécessitait des autorisations pour le module de catalogue lors de la récupération du nombre de produits et affichait cette erreur : `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Correction d’un problème](../assets/fix.svg) Les problèmes d’affichage liés au menu Format du générateur de pages sont désormais résolus avec la mise à niveau de la bibliothèque TinyMCE 5. <!--- AC-446-->

![Correction d’un problème](../assets/fix.svg) Vous pouvez désormais utiliser la souris pour modifier une **Texte à afficher** dans la fenêtre contextuelle Insérer un lien . <!--- AC-982-->

![Correction d’un problème](../assets/fix.svg) Le Créateur de pages affiche désormais toutes les options comme prévu dans le menu d’options Taille de police . Auparavant, toutes les options n’étaient pas affichées. <!--- AC-1056-->

![Correction d’un problème](../assets/fix.svg) Mise à niveau de la fonction `phpgt/dom` Dépendance du compositeur pour `magento/magento2-page-builder` vers les dernières versions. <!--- magento/magento2-page-builder/pull/779-->

![Correction d’un problème](../assets/fix.svg) Le générateur de pages ne redimensionne plus les boîtes de dialogue Insérer un lien et Insérer une image lors de l’affichage du curseur dans une petite colonne. <!--- AC-973-->

![Correction d’un problème](../assets/fix.svg) Le menu Propriétés du tableau du générateur de pages s’affiche désormais comme prévu. <!--- AC-407-->

![Correction d’un problème](../assets/fix.svg) Les points du curseur ne sont plus affichés sur le modal Insérer un lien ou une image lorsque la souris ne survole pas le curseur. <!--- AC-406-->

![Correction d’un problème](../assets/fix.svg) La taille de police utilisée pour afficher les options du menu Tableau a été optimisée. <!--- AC-396-->

![Correction d’un problème](../assets/fix.svg) Correction des anomalies avec le positionnement des boîtes de dialogue Insérer/Modifier l’image et Insérer/Modifier le lien . <!--- AC-397-->

![Correction d’un problème](../assets/fix.svg) Page Builder ne génère plus d’erreur lorsque vous cliquez sur **Éditeur de texte** pour une bannière. <!--- AC-398-->

![Correction d’un problème](../assets/fix.svg) Le Créateur de pages ne convertit plus tous les blocs dynamiques en une seule langue lors de la mise à niveau. <!--- MC-42265-->

## 1.6.0 pour Adobe Commerce 2.4.2

![Nouveau](../assets/new.svg) <!-- Issue 558 -->**Nouveau [!DNL Page Builder] style** - [!DNL Page Builder] des améliorations massives ont été apportées à la manière dont le contenu est stylisé. Les modifications facilitent désormais la création de sélecteurs CSS simples pour remplacer les styles de type de contenu existants. Ces modifications permettent de créer des [!DNL Page Builder] thèmes avec une réactivité riche pour tous les types de contenu.

![Nouveau](../assets/new.svg) <!-- Issue 429 -->**Conteneur de lignes désormais facultatif** - Vous pouvez désormais créer du contenu dans [!DNL Page Builder] sans avoir besoin d’un conteneur de lignes. Outre la ligne, vous pouvez désormais faire glisser et déposer directement sur la scène les types de contenu suivants : HTML, Bloc, Bloc dynamique, Colonnes et Onglets.

![Nouveau](../assets/new.svg) <!-- Issue 636 -->**Nouveau sélecteur de fenêtre réactive** - Vous pouvez maintenant prévisualiser votre [!DNL Page Builder] contenu à différentes largeurs d’appareil (points d’arrêt) à l’aide des nouveaux boutons de sélecteur de fenêtre d’affichage Admin au-dessus de la scène. Le sélecteur de fenêtre d’affichage simule le style de votre contenu lorsqu’il est affiché sur le storefront à l’aide de différents appareils.

![Nouveau](../assets/new.svg) <!-- Issue 637 -->**Nouveaux champs de formulaire spécifiques à un point d’arrêt** - Les valeurs de champ de type Contenu peuvent désormais être définies sur des points d’arrêt de fenêtre d’affichage spécifiques. Les indicateurs d’icône en regard des champs indiquent la fenêtre d’affichage à laquelle s’applique la valeur du champ de type de contenu.

![Nouveau](../assets/new.svg) <!-- Issue 559 -->**Suppression des entrées de champ de formulaire prédéfinies** - Les paramètres de formulaire avancés pour les marges, les plages et les propriétés liées aux bordures (bordure, largeur de bordure et rayon de bordure) sont désormais définis comme `default`, de sorte que les valeurs puissent être définies par le CSS d’un module.

![Nouveau](../assets/new.svg) <!-- Issue 635, 557,  -->**Ajout de l’interlettrage** - Les lignes et les colonnes contiennent désormais des espaces supplémentaires autour des types de contenu sur la scène, mais pas sur le storefront. L’espacement des scènes supplémentaire facilite l’accès aux menus des options de survol avec la souris pour les types de contenu conteneur et contenu.

![Correction d’un problème](../assets/fix.svg) <!-- MC-37348 -->**Correction du défilement automatique vers les révisions** - Le défilement automatique vers les révisions de produits sur le storefront est maintenant corrigé.

![Correction d’un problème](../assets/fix.svg) <!-- MC-36227 -->**Contenu recadré fixe** - Les descriptions de catégorie et de produit longues ne sont plus recadrées.

![Correction d’un problème](../assets/fix.svg) <!-- MC-35402 -->**Correction du contenu de la catégorie de fond perdu plein largeur** - Le contenu des catégories peut désormais être affiché en pleine largeur ou en plein fond perdu.

![Correction d’un problème](../assets/fix.svg) <!-- MC-37989 -->**Amélioration de la sécurité**

## 1.5.1 pour Adobe Commerce 2.4.1-p1

![Correction d’un problème](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Affichage des erreurs** - Correction d’un problème en raison duquel [!DNL Page Builder] affiché une erreur lors de l’ajout de sous-catégories Catalog dans l’Admin.

## 1.5.0 pour Adobe Commerce 2.4.1

![Nouveau](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Modification immersive, plein écran** - Edition [!DNL Page Builder] Le contenu est désormais en plein écran uniquement pour toutes les zones contrôlées par [!DNL Page Builder]. Cette modification inclut les pages CMS, les pages de produits et de catégories, les blocs et les blocs dynamiques. La modification en plein écran met l’accent sur votre contenu et fournit une vue qui correspond mieux à l’expérience de l’utilisateur sur le storefront.

![Nouveau](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] aperçus de contenu **- Par défaut : [!DNL Page Builder] fournit désormais des aperçus de contenu non seulement pour les pages CMS, les blocs et les blocs dynamiques, mais également pour les pages de produits et de catégories. Vous pouvez configurer cette fonction pour qu’elle soit activée ou désactivée pour les pages Produit et Catégorie à l’aide de la nouvelle [!DNL Page Builder] Paramètre Aperçu de contenu, accessible dans la configuration du magasin sous Gestion de contenu > Outils de contenu avancé.

![Nouveau](../assets/new.svg) <!-- Issue 543 -->**Amélioration de l’accès aux descriptions courtes des produits** - Par défaut, une brève description du produit s’affiche maintenant avant la description plus longue. Cette modification entraîne une correspondance avec l’ordre dans lequel ils apparaissent sur le storefront et évite la nécessité de faire défiler le contenu de description plus longue pour accéder à la brève description.

![Nouveau](../assets/new.svg) <!-- Issue 419 -->**Liens imbriqués empêchés dans les bannières et les diapositives** - L’ajout de liens vers le contenu et les éléments externes des bannières et des diapositives a créé des liens imbriqués qui ne s’affichaient pas ou ne se comportaient pas correctement sur le storefront. Pour résoudre ce problème, il n’est plus possible d’ajouter des liens à *both* la zone Texte du message et l’attribut Lien pour les bannières et les diapositives.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 421 --> Correction d’un problème en raison duquel la définition du rayon de bordure vide sur un élément d’onglet provoquait des erreurs et endommageait le contenu de l’élément d’onglet.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 422 --> Correction d’un problème en raison duquel l’ajout de certaines combinaisons de conditions au filtre Condition des produits provoquait des erreurs qui empêchaient l’enregistrement du formulaire Produits.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 425 -->Correction d’un problème en raison duquel le type de contenu Curseur ne se comportait pas correctement lorsque le paramètre Boucle infinie était désactivé.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 426 -->Correction du prix minimum publié afin qu’il fonctionne désormais dans [!DNL Page Builder].

![Correction d’un problème](../assets/fix.svg) <!-- Issue 436 -->Correction d’un problème dans Safari et IE 11 qui empêchait de faire glisser une image vers la zone de chargement dans les bannières et les diapositives.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 525 -->Correction d’un problème en raison duquel le type de contenu Curseur ne réagissait pas dans Firefox.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 567 -->Correction d’un problème en raison duquel la configuration du widget créait des sélecteurs incorrects dans le DOM pour les différentes apparences.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 609 -->Correction d’un problème en raison duquel la barre d’outils En-tête masquait le menu d’options du type de contenu, ce qui empêchait l’accès au formulaire et à d’autres options.

![Correction d’un problème](../assets/fix.svg) <!-- Issue 612, 613 -->Correction de problèmes en raison desquels les curseurs et plusieurs lignes utilisant des arrière-plans de parallaxe ne s’affichaient pas correctement après le basculement du mode plein écran plusieurs fois.

![Correction d’un problème](../assets/fix.svg) <!--MC-35220-->Correction du problème qui empêchait de copier le contenu d’un type de contenu En-tête vers un type de contenu Texte . [!DNL Page Builder] de l’enregistrement.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34620 -->Correction du type de contenu Texte pour qu’il gère et enregistre correctement les caractères non latins-1.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34679 -->Fixe [!DNL Page Builder] Styles CSS qui entraînaient le rendu incorrect du menu de site du thème Luma pour les petits ports d’affichage et les écrans mobiles.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34848 -->Correction du type de contenu HTML pour afficher correctement les widgets incorporés tels que &quot;Commande par SKU&quot; sur le storefront.

## 1.4.1 pour Adobe Commerce 2.4.0-p1

![Nouveau](../assets/new.svg) <!-- PB-590 --> Mise à niveau vers TinyMCE 4. Suppression de TinyMCE 3 pour améliorer la sécurité.

## 1.4.0 pour Adobe Commerce 2.4.0

![Nouveau](../assets/new.svg) <!-- PB-494 -->Prise en charge de PHP 7.4.

![Correction d’un problème](../assets/fix.svg) <!-- MC-31247 -->Correction d’un problème en raison duquel le type de contenu Produits n’affichait pas les produits configurables lorsque la condition était définie sur le prix.

![Correction d’un problème](../assets/fix.svg) <!-- PB-179 -->Correction de la configuration Alignement des produits pour positionner uniquement le conteneur de produits lui-même, et non le contenu du conteneur de produits, tel que le nom, le prix, les boutons, les images et d’autres éléments du produit.

![Correction d’un problème](../assets/fix.svg) <!-- MC-33556 -->Amélioration des performances.

![Correction d’un problème](../assets/fix.svg) Amélioration de la sécurité.

## 1.3.3-p1 pour Adobe Commerce 2.3.6-p1

![Correction d’un problème](../assets/fix.svg) Amélioration de la sécurité.

## 1.3.3 pour Adobe Commerce 2.3.6

![Correction d’un problème](../assets/fix.svg) <!-- MC-32766 -->Correction du type Contenu texte pour enregistrer correctement les directives de variable ajoutées aux attributs html.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34590 -->Correction du type de contenu Texte pour qu’il gère et enregistre correctement les caractères non latins-1.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34677 -->Fixe [!DNL Page Builder] Styles CSS qui entraînaient le rendu incorrect du menu de site du thème Luma pour les petits ports d’affichage et les écrans mobiles.

![Correction d’un problème](../assets/fix.svg) <!-- MC-34846 -->Correction du type de contenu HTML pour afficher correctement les widgets incorporés comme _Commande par SKU_ sur la vitrine.

![Correction d’un problème](../assets/fix.svg) Correction d&#39;une erreur qui empêchait parfois les utilisateurs d&#39;enregistrer des formulaires de type contenu. Erreur (&quot;[!DNL Page Builder] était rendu pendant 5 secondes sans déverrouiller&quot;), l’icône de chargeur fonctionnait indéfiniment après avoir tenté d’enregistrer un formulaire.

## 1.3.2 pour Adobe Commerce 2.3.5-p2

![Nouveau](../assets/new.svg) Amélioration de la sécurité.

## 1.3.1 pour Adobe Commerce 2.3.5-p1

Cette version de [!DNL Page Builder] n’est qu’une mise à jour de numéro de version pour Adobe Commerce 2.3.5-p1. Toutes les fonctionnalités décrites pour la version 1.3.0 s’appliquent également à cette version.

## 1.3.0 pour Adobe Commerce 2.3.5

![Nouveau](../assets/new.svg) **Modèles** - [!DNL Page Builder] comporte désormais des modèles qui peuvent être créés à partir de contenu existant et appliqués à de nouvelles zones de contenu. [!DNL Page Builder] les modèles enregistrent le contenu et les mises en page des pages, blocs, blocs dynamiques, attributs de produit et descriptions de catégorie existants. Par exemple, vous pouvez enregistrer une [!DNL Page Builder] Page CMS en tant que modèle, puis appliquez ce modèle (avec tout son contenu et toutes ses mises en page) pour créer rapidement des pages CMS pour votre site. Cette nouvelle fonctionnalité est décrite ici : [Modèles](templates.md).

![Nouveau](../assets/new.svg) **Arrière-plans vidéo pour les lignes, bannières et curseurs** - [!DNL Page Builder] Les lignes, bannières et curseurs peuvent désormais utiliser des vidéos pour leurs arrière-plans. Ces nouvelles fonctionnalités sont décrites ici : [Lignes](row.md), [Bannières](banner.md), [Curseurs](slider.md).

![Nouveau](../assets/new.svg) **Ajouts et améliorations de la prise en charge vidéo** - [!DNL Page Builder] prend désormais en charge un plus large éventail de formats vidéo. Outre les vidéos YouTube et Vimeo, le type de contenu vidéo et les arrière-plans vidéo prennent désormais en charge les liens URL vidéo vers des formats vidéo tels que `.mp4` et d’autres formats pris en charge par le navigateur. Le type de contenu Vidéo ajoute également une fonction de lecture automatique. Ces nouvelles fonctionnalités sont décrites ici : [Type de contenu vidéo](video.md).

![Nouveau](../assets/new.svg) **Lignes de hauteur complète, bannières et curseurs** - [!DNL Page Builder] Les lignes, bannières et curseurs peuvent désormais définir leur hauteur sur la pleine hauteur de la page à l’aide d’un nombre avec n’importe quelle unité CSS (px, %, vh, em) ou d’un calcul entre unités (100vh - 237px). Ces nouvelles fonctionnalités sont décrites ici : [Lignes](row.md), [Bannières](banner.md), [Curseurs](slider.md).

![Nouveau](../assets/new.svg) **Bibliothèque de mise à niveau de type de contenu** - Les développeurs peuvent désormais créer des versions de [!DNL Page Builder] types de contenu sans introduire de problèmes rétrocompatibles avec les versions précédentes. Avant cette version, des modifications importantes apportées aux configurations de type de contenu créaient des problèmes d’affichage et de perte de données avec des enregistrements précédemment enregistrés. [!DNL Page Builder] types de contenu. La nouvelle bibliothèque de mise à niveau élimine ces problèmes. La bibliothèque est conçue pour mettre à niveau les versions précédentes des types de contenu enregistrés dans la base de données afin qu’elles correspondent aux modifications de configuration apportées aux nouvelles versions. [!DNL Page Builder] exécute la bibliothèque de mise à niveau sur les types de contenu natifs si nécessaire pour une nouvelle version. Cette modification garantit que la variable [!DNL Page Builder] les types de contenu sont toujours mis à niveau pour correspondre à toute modification apportée aux types de contenu pour une version plus récente.

>[!IMPORTANT]
>
>Si vous avez créé des entités de base de données supplémentaires pour le stockage [!DNL Page Builder] contenu, vous _must_ ajoutez ces entités à vos `etc/di.xml`. Dans le cas contraire, la variable [!DNL Page Builder] le contenu stocké dans votre entité n’est pas mis à jour, ce qui peut entraîner des pertes de données et des problèmes d’affichage. Par exemple, si vous avez créé une entité de blog qui stocke [!DNL Page Builder] contenu, vous devez ajouter votre entité de blog à votre `etc/di.xml` en tant que `UpgradableEntitiesPool` pour que la bibliothèque de mise à niveau puisse mettre à jour la variable [!DNL Page Builder] types de contenu utilisés dans votre blog. Pour plus d’informations et d’instructions sur l’utilisation de la bibliothèque de mise à niveau, voir [Mise à niveau des types de contenu](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) dans le _Guide du développeur de Page Builder_.

![Nouveau](../assets/new.svg) **Documentation sur l’ajout de nouvelles apparences** - Informations sur les développeurs maintenant publiées à propos de [ajout d’aspects](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) pour les types de contenu existants ou personnalisés.

![Correction d’un problème](../assets/fix.svg) **Correctifs**

- <!-- PB-50 -->Correction d’un problème en raison duquel le menu TinyMCE pour le contenu d’une diapositive s’affichait sous d’autres types de contenu si le conteneur parent de la diapositive était dupliqué.
- <!-- PB-166 -->Mis à jour [!DNL Page Builder] mettre en oeuvre une méthode de destruction pour empêcher les fuites de mémoire dans certains scénarios.
- <!-- PB-170 -->Amélioration des performances de TinyMCE lorsque plusieurs instances sont utilisées sur l’étape d’administration.
- <!-- PB-252 -->Correction d’un problème en raison duquel le type de contenu Bloc dynamique n’était pas rendu sur l’étape Admin si la ligne supérieure était marquée comme masquée.
- <!-- PB-273 -->Événements de survol de la souris perfectionnés sur l’étape d’administration en supprimant un délai de 200 ms des différentes commandes de l’interface utilisateur. Cette modification facilite l’utilisation d’éléments de contenu imbriqués sur la scène.
- <!-- PB-294 -->Correction d’un problème en raison duquel le symbole de devise était échappé de manière incorrecte dans le widget Liste de produits dans le bloc/bloc dynamique de l’étape Admin.
- <!-- PB-296 -->Correction d’un problème en raison duquel le total du produit sur la variable [!DNL Page Builder] le panneau d’édition ne fonctionnait pas pour les produits de stock MSI personnalisés.
- <!-- PB-317 -->Correction d’un problème en raison duquel l’enregistrement [!DNL Page Builder] le contenu avec des images d’arrière-plan sur Microsoft Edge n’affiche pas ces images sur le storefront.
- <!-- PB-390 -->Correction d’un problème en raison duquel imbriqué [!DNL Page Builder] l’enregistrement du contenu échoue si les utilisateurs cliquent sur le bouton Enregistrer avant que la page ne soit entièrement rendue.
- <!-- PB-418 -->Correction d’une erreur d’exception générée dans les tâches cron en raison de [!DNL Page Builder] analytics.

## 1.2.2 pour Adobe Commerce 2.3.4-p2

![Nouveau](../assets/new.svg) Amélioration de la sécurité.

## 1.2.1 pour Adobe Commerce 2.3.4-p1

![Nouveau](../assets/new.svg) Amélioration de la sécurité.

## 1.2.0 pour Adobe Commerce 2.3.4

![Nouveau](../assets/new.svg)  **[!DNL Page Builder]intégration avec PWA Studio** - Ajout [!DNL Page Builder] rendu du contenu vers l’application Venia en PWA Studio. [!DNL Page Builder] le contenu peut désormais être visualisé dans l’application Venia PWA Studio. Voir [!DNL Page Builder] documentation dans [PWA Studio] pour toutes les informations sur cette nouvelle fonctionnalité.

![Nouveau](../assets/new.svg) **Ajout d’un carrousel de produit** - <!-- PB-77, PB-173, PB-175 -->Le type de contenu Produits fournit désormais une option permettant d’afficher vos produits dans un format de carrousel/curseur, y compris plusieurs options permettant de personnaliser le carrousel selon vos besoins.

![Nouveau](../assets/new.svg) **Ajout du tri des SKU du produit** - <!-- PB-69 -->Le type de contenu Produits permet désormais de trier vos produits par SKU dans l’ordre dans lequel vous les ajoutez à une liste au sein de l’administrateur.

![Nouveau](../assets/new.svg) **Ajout du tri des catégories de produits** - <!-- PB-181 -->. Le type de contenu Produits offre désormais une option pour trier vos produits par catégorie. _position_, les affichant dans l’ordre dans lequel ils apparaissent dans votre catalogue de commerce.

![Nouveau](../assets/new.svg) **Ajout des totaux de sélection de produit** - <!-- PB-107 -->. L’éditeur d’administration de type de contenu Produits affiche désormais le nombre total de produits qui correspondent aux options de sélection de produits.

![Correction d’un problème](../assets/fix.svg) **Correctifs**

- <!-- PB-237 -->Amélioration de la sécurité.
- <!-- PB-41 -->Correction des recherches dans les composants de sélection de l’interface utilisateur afin d’effectuer une seule requête AJAX par terme de recherche.
- <!-- PB-76, PB-84-->Mise à jour des aperçus de produit dans l’administrateur pour qu’ils correspondent au storefront, y compris les options d’évaluation des étoiles, de couleur et de taille du produit, le cas échéant.
- <!-- PB-169 -->Correction d’un problème en raison duquel [!DNL Page Builder] n’a pas pu être enregistré lorsque la minification et le regroupement JavaScript sont activés dans Commerce.
- <!-- PB-241 -->Correction des aperçus administrateur des produits, blocs et blocs dynamiques afin qu’ils s’affichent correctement sur les installations Commerce qui définissent différentes URL pour l’administrateur et le serveur frontal.
- <!-- PB-238 -->Correction des aperçus administrateur des produits, blocs et blocs dynamiques pour un rendu correct sur les installations Commerce avec B2B installé avec l’événement _Connexion uniquement_ activée. Avant ce correctif, la variable [!DNL Page Builder] l’aperçu entraîne la redirection de la page vers la connexion au compte client.
- <!-- PB-239 -->Correction d’une erreur de session qui pouvait se produire lors de la prévisualisation d’une grande page dans le [!DNL Page Builder] Administrateur.
- <!-- PB-248 -->Mis à jour [!DNL Page Builder] Styles LESS pour empêcher la duplication des styles storefront.

## 1.1.1 pour Adobe Commerce 2.3.3-p1

![Nouveau](../assets/new.svg) Amélioration de la sécurité.

## 1.1.0 pour Adobe Commerce 2.3.3

![Nouveau](../assets/new.svg) <!-- MC-15250 -->Ajout d’un tri explicite des produits au type de contenu Produits .

![Nouveau](../assets/new.svg) <!-- MC-17823 -->Ajout de boutons permettant d’insérer des images, des widgets et des variables dans le type de contenu HTML.

![Correction d’un problème](../assets/fix.svg) Amélioré [!DNL Page Builder] sécurité.

![Correction d’un problème](../assets/fix.svg) <!-- MC-1805 -->Mis à jour [!DNL Page Builder] pour prendre en charge la version 7.3 de PHP.

![Correction d’un problème](../assets/fix.svg) <!-- MC-4137 -->Mise à jour de TinyMCE vers la version 4.9.5. Cette mise à jour, ainsi que les améliorations supplémentaires, ont corrigé plusieurs problèmes de l’éditeur intégré TinyMCE :

- Des variables, des images et des liens d’image sont ajoutés à l’endroit où se trouve le curseur.
- Les tableaux et les cellules de tableau peuvent être centrés.
- Copier/coller colle maintenant le contenu à la position du curseur.
- Les liens peuvent être appliqués au texte sélectionné.
- Les puces sont correctement alignées.
- Les modifications de l’éditeur intégré peuvent être enregistrées sans cliquer au préalable en dehors de l’éditeur.

![Correction d’un problème](../assets/fix.svg) <!-- MC-3880 -->Correction d’un problème en raison duquel la hauteur minimale et l’alignement vertical étaient incohérents entre les sections du panneau de modification pour chaque type de contenu.

![Correction d’un problème](../assets/fix.svg) <!-- MC-14994 -->Correction d’un problème en raison duquel la barre d’outils du type de contenu En-tête était mal positionnée lors du premier dépôt sur la scène.

![Correction d’un problème](../assets/fix.svg) <!-- MC-15742 -->Correction des marges codées en dur dans les types de contenu Curseur et Vidéo.

![Correction d’un problème](../assets/fix.svg) <!-- MC-16241 -->Correction d’un problème en raison duquel le symbole d’astérisque requis s’affichait deux fois sur les champs du formulaire.

## 1.0.3 pour Adobe Commerce 2.3.2-p2

![Nouveau](../assets/new.svg) Amélioration de la sécurité.

## 1.0.2 pour Adobe Commerce 2.3.2-p1

![Nouveau](../assets/new.svg) Amélioration de la sécurité.

## 1.0.1 pour Adobe Commerce 2.3.2

![Nouveau](../assets/new.svg) Garantit la compatibilité avec Adobe Commerce 2.3.2.

## 1.0.0 pour Adobe Commerce 2.3.1

![Nouveau](../assets/new.svg) Disponibilité générale


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
