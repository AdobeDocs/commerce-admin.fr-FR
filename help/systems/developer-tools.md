---
title: Outils de développement
description: Découvrez les outils de développement avancés disponibles pour aider les développeurs à travailler sur des projets de personnalisation.
exl-id: 34529aa9-201f-4817-b53b-a15b6a78a923
role: Admin, Developer
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# Outils de développement

Utilisez les outils de développement avancés pour déterminer le mode de compilation lors du développement front-end, créer une liste autorisée d’adresses IP et afficher des indications de chemin d’accès au modèle. Il existe également des outils permettant d’apporter facilement des modifications ponctuelles au texte dans l’interface du storefront et de l’administrateur.

- [Journaux d’action](action-log.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)
- [Workflow de développement front-end](#frontend-development-workflow)
- [Utiliser des signatures de fichiers statiques](#static-file-signatures)
- [Optimisation des fichiers de ressources](#optimizing-resource-files)
- [Restrictions du client du développeur](#client-restrictions)
- [Conseils sur le chemin du modèle](#template-path-hints)
- [Traduire en ligne](#translate-inline)

## Modes de fonctionnement

Votre instance Adobe Commerce ou Magento Open Source peut être déployée pour s’exécuter en _mode de production_ ou _mode développeur_. Les outils et paramètres de configuration conçus spécifiquement pour les développeurs ne sont accessibles que lorsque le magasin est en cours d’exécution en _mode développeur_.

Le mode de fonctionnement ne peut être modifié qu’à partir de la ligne de commande du serveur par un utilisateur disposant des autorisations appropriées. Voir [Définir le mode de fonctionnement](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/set-mode.html?lang=fr) dans le _Guide de configuration_ pour plus d’informations.

La plupart des rubriques de la documentation pour les commerçants s’appliquent à une instance Commerce exécutée en mode de production. Toutefois, les paramètres de configuration et outils suivants ne peuvent être utilisés que lorsque l’installation est en cours d’exécution en mode Développeur.

## Workflow de développement front-end

Le type de workflow de développement front-end détermine si la compilation Less a lieu côté client ou serveur au cours du développement. Less est une extension de CSS qui comporte des fonctionnalités et des conventions supplémentaires et qui produit du code rationalisé. Une compilation Less côté client est recommandée pour le développement de thèmes. La compilation côté serveur est le mode par défaut. Les options du workflow de développement ne sont pas disponibles pour les magasins en mode de production.
Voir [Compilation LESS côté client ou côté serveur](https://developer.adobe.com/commerce/frontend-core/guide/css/quickstart/compilation-mode/){:target="_blank"} dans la documentation destinée aux développeurs et développeuses de Commerce.

>[!NOTE]
>
>La configuration du workflow de développement front-end est disponible uniquement en [mode Développeur](../systems/developer-tools.md#operation-modes).

![Configuration avancée - Workflow de développement front-end](../configuration-reference/advanced/assets/developer-frontend-development-workflow.png){width="600" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Front-end Development Workflow]** .

1. Définissez **[!UICONTROL Workflow Type]** sur l’une des options suivantes :

   - `Client side less compilation` - La compilation a lieu dans le navigateur à l’aide de la bibliothèque `less.js` native.
   - `Server side less compilation` - La compilation a lieu sur le serveur en utilisant la bibliothèque Less PHP. Il s’agit du mode par défaut pour la production.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Signatures de fichiers statiques

L’ajout d’une signature numérique à l’URL des fichiers statiques permet aux navigateurs de détecter lorsqu’une version plus récente du fichier est disponible. Les fichiers statiques qui peuvent être suivis à l’aide de signatures numériques comprennent les fichiers JavaScript, CSS, images et polices. La signature est ajoutée au chemin d’accès directement après l’URL de base. Si la signature d’un fichier diffère de celle stockée dans le cache du navigateur, la version la plus récente du fichier est utilisée.

Voir [Signature de contenu statique](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/static-content-signing.html?lang=fr){:target="_blank"} dans la documentation destinée aux développeurs de Commerce.

>[!NOTE]
>
>La configuration Paramètres de fichier statique est disponible uniquement lorsque vous travaillez en [mode développeur](../systems/developer-tools.md#operation-modes).

![Configuration avancée - Paramètres des fichiers statiques](../configuration-reference/advanced/assets/developer-static-files-settings.png){width="600" zoomable="yes"}

Pour obtenir la liste détaillée des paramètres de configuration, voir [_Paramètres de fichier statique_](../configuration-reference/advanced/developer.md) dans le _Référence de configuration_.

**_Pour activer les fichiers statiques signés :_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Static Files Settings]** .

1. Définissez **[!UICONTROL Sign Static Files]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Optimisation des fichiers de ressources

Le temps de chargement des fichiers de ressources peut être réduit en fusionnant et en regroupant les fichiers, ainsi qu’en réduisant le code.

- La fusion combine des fichiers distincts du même type en un seul fichier.
- Le regroupement est une technique qui permet de regrouper des fichiers distincts afin de réduire le nombre de requêtes HTTP requises pour charger une page.
- La minimisation supprime les espaces, les sauts de ligne et les commentaires, mais n’affecte pas les fonctionnalités du code. Comme les fichiers réduits ne peuvent pas être modifiés, le processus ne doit être appliqué que lorsque vous êtes prêt à passer en production.

Par défaut, Adobe Commerce et Magento Open Source ne fusionnent pas, ne regroupent pas ou ne réduisent pas au minimum les fichiers. Le développeur du projet doit déterminer les méthodes d’optimisation des fichiers à utiliser.

Pour plus d’informations, consultez [Bonnes pratiques relatives aux performances](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/overview.html?lang=fr).

>[!NOTE]
>
>Les fichiers CSS et JavaScript ne peuvent être optimisés qu’en [mode Développeur](../systems/developer-tools.md#operation-modes).

| Type de fichier | Opérations prises en charge |
| --------------- | -------------------- |
| Fichiers CSS | `MergeMinify` |
| Fichiers JavaScript | `MergeBundleMinify` |
| Fichiers de modèle | `Minify` |

{style="table-layout:auto"}

**_Pour optimiser les fichiers de ressources, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Pour optimiser les fichiers CSS, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL CSS Settings]** et procédez comme suit :

   - Définissez **[!UICONTROL Merge CSS Files]** sur `Yes`.
   - Définissez **[!UICONTROL Minify CSS Files]** sur `Yes`.

   ![ Configuration avancée - Paramètres CSS ](../configuration-reference/advanced/assets/developer-css-settings.png){width="600" zoomable="yes"}

[_Paramètres CSS_](../configuration-reference/advanced/developer.md)

1. Pour optimiser les fichiers JavaScript, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL JavaScript Settings]** et procédez comme suit :

   - Définissez **[!UICONTROL Merge JavaScript Files]** sur `Yes`.
   - Définissez **[!UICONTROL Minify JavaScript Files]** sur `Yes`.

   ![Configuration avancée - Paramètres JavaScript](../configuration-reference/advanced/assets/developer-javascript-settings.png){width="600" zoomable="yes"}

1. Pour réduire les fichiers de modèle PHTML, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Template Settings]** et définissez **[!UICONTROL Minify Html]** sur `Yes`.

   ![Configuration avancée - Paramètres du modèle](../configuration-reference/advanced/assets/developer-template-settings.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Restrictions du client

Placer sur la liste autorisée Avant d’utiliser un outil tel que [conseils de chemin d’accès pour les modèles](#template-path-hints), veillez à ajouter votre adresse IP aux restrictions pour les développeurs et les clientes et développeuses, afin de ne pas perturber l’expérience d’achat des clients et clientes de la boutique. Si vous ne connaissez pas votre adresse IP, vous pouvez la rechercher en ligne.

>[!NOTE]
>
>Les restrictions client pour les développeurs peuvent être définies en [mode Développeur](../systems/developer-tools.md#operation-modes) uniquement.

Pour obtenir des informations techniques, consultez [Custom VCL for allow requests](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-allowlist.html?lang=fr) dans le guide _Commerce on Cloud Infrastructure_.

**_Pour ajouter votre adresse IP à la liste autorisée :_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Developer Client Restrictions]** .

   ![Configuration avancée - Restrictions du client développeur](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Allow IPs]**, saisissez votre adresse IP.

   Si l’accès est nécessaire pour plusieurs adresses IP, séparez-les par une virgule.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, actualisez tous les caches non valides.

## Indications de chemin du modèle

Les indications de chemin du modèle sont un outil de diagnostic qui ajoute une notation avec le chemin d’accès à chaque modèle utilisé sur la page. Les indications de chemin d’accès du modèle peuvent être activées pour le storefront ou l’administrateur.

>[!NOTE]
>
>Les Template Path Hints peuvent être modifiés en [mode développeur](../systems/developer-tools.md#operation-modes) uniquement.

Voir [Rechercher des modèles, des mises en page et des styles](https://developer.adobe.com/commerce/frontend-core/guide/themes/debug/){:target="_blank"} dans la documentation destinée aux développeurs de Commerce.

![Exemple de storefront - conseils sur le chemin d’accès du modèle](./assets/storefront-template-path-hints.png){width="700" zoomable="yes"}

### Étape 1 : ajouter votre adresse IP à la place sur la liste autorisée

Avant d’utiliser les indications de chemin d’accès du modèle, ajoutez votre adresse IP à la [liste autorisée ](#client-restrictions) afin d’éviter toute interférence avec les clients qui font leurs achats dans le magasin. Lorsque vous avez terminé, veillez à effacer le cache de Commerce pour supprimer toutes les indications du magasin.

![Configuration avancée - Restrictions du client développeur](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

### Étape 2 : activer les indications de chemin d’accès du modèle

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Debug]** et procédez comme suit :

   ![Configuration avancée - Débogage](../configuration-reference/advanced/assets/developer-debug.png){width="600" zoomable="yes"}

   - Pour activer les indications de chemin d’accès du modèle pour le magasin, définissez **[!UICONTROL Enabled Template Path Hints for Storefront]** sur `Yes`.

   - Pour activer les indications de chemin d’accès du modèle pour le magasin uniquement lorsque l’URL inclut le paramètre `templatehints`, définissez **Activer les indications pour Storefront avec le paramètre d’URL** sur `Yes`. Définissez ensuite la valeur du paramètre si nécessaire. La valeur par défaut est `magento`, mais vous pouvez utiliser une valeur personnalisée. Par exemple, si vous définissez la valeur sur `lorem`, vous utiliserez `mymagento.com?templatehints=lorem` pour afficher des conseils sur les modèles.

   - Pour activer les indications de chemin du modèle pour l’administrateur, définissez **[!UICONTROL Enabled Template Path Hints for Admin]** sur `Yes`.

   - Pour inclure les noms des blocs, définissez **[!UICONTROL Add Block Class Type to Hints]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### Étape 3 : vider le cache

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Flush Magento Cache]**.

## Traduire en ligne

Vous pouvez utiliser l’outil Traduire en ligne en [mode développeur](../systems/developer-tools.md#operation-modes) pour retoucher le texte de l’interface afin de refléter votre voix et votre marque. Lorsque le mode Traduire en ligne est activé, tout texte de la page qui peut être modifié est signalé en rouge. Il est facile de modifier les libellés des champs, les messages et tout autre texte qui apparaît dans le storefront et l’admin. Par exemple, de nombreux thèmes utilisent une terminologie telle que _Mon compte_, _Ma liste de souhaits_ et _Mon tableau de bord_ pour aider les clients à trouver leur chemin. Cependant, vous pouvez préférer simplement utiliser les mots _Compte_, _Liste de souhaits_ et _Tableau de bord_.

>[!NOTE]
>
>L’outil Traduire en ligne est disponible uniquement lorsque vous travaillez en [mode Développeur](../systems/developer-tools.md#operation-modes).

Voir [Présentation des traductions](https://developer.adobe.com/commerce/frontend-core/guide/translations/) dans la documentation destinée aux développeurs de Commerce.

![Exemple de storefront - texte traduisible](./assets/storefront-translate-inline.png){width="700" zoomable="yes"}

Si votre boutique est disponible dans plusieurs langues, vous pouvez apporter des ajustements précis au texte traduit pour le paramètre régional. Sur le serveur , le texte de l’interface est conservé dans un fichier CSV distinct pour chaque bloc de sortie et est organisé par paramètre régional. Plutôt que d’utiliser l’outil _Traduire en ligne_, vous pouvez également modifier les fichiers CSV directement sur le serveur. Les fichiers de traduction sont stockés dans `app/code/Magento/<module_name>/i18n/<language_locale>.csv`.

>[!NOTE]
>
>Pour utiliser l’outil Traduire en ligne , votre navigateur doit autoriser les pop-ups.

### Étape 1 : désactiver les caches de sortie

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Cochez les cases suivantes :

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Définissez la commande **[!UICONTROL Actions]** sur `Disable`, puis cliquez sur **[!UICONTROL Submit]**.

### Étape 2 : activer l’outil Traduire en ligne

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Pour utiliser une vue de magasin spécifique, définissez la **[!UICONTROL Store View]** à mettre à jour.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Translate Inline]** .

   Décochez la case **[!UICONTROL Use Website]** selon les besoins pour modifier ces paramètres.

   L’option _[!UICONTROL Enabled for Admin]_&#x200B;n’est pas disponible lors de la modification d’une vue de magasin spécifique.

   ![Configuration avancée - Traduire en ligne](../configuration-reference/advanced/assets/developer-translate-inline.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled for Storefront]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, actualisez les caches non valides, mais laissez les caches désactivés tels quels pour l’instant.

### Étape 3 : mettre à jour le texte

1. Ouvrez votre storefront dans un navigateur et accédez à la page à modifier.

   Si nécessaire, utilisez le sélecteur de langues pour modifier la vue du magasin. Chaque chaîne de texte traduisible est entourée en rouge. Lorsque vous pointez sur une zone de texte, une icône de livre ( ![icône de livre](../assets/icon-book.png) ) s’affiche.

1. Cliquez sur l’icône représentant un livre pour ouvrir la fenêtre _Traduire_ et procédez comme suit :

   - Si la modification concerne l’affichage spécifique du magasin, cochez la case **[!UICONTROL Store View Specific]** .

   - Saisissez le nouveau texte de **[!UICONTROL Custom]**.

1. Cliquez ensuite sur **[!UICONTROL Submit]**.

   ![Saisir du texte personnalisé](./assets/storefront-translate-inline-detail.png){width="700" zoomable="yes"}

1. Pour afficher vos modifications dans le magasin, actualisez le navigateur.

1. Répétez ce processus pour tous les éléments du magasin à modifier.

### Étape 4 : Restaurer les paramètres d&#39;origine

1. Revenez à l’administration de votre boutique.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Définissez **[!UICONTROL Store View]** sur la vue spécifique qui a été modifiée.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Translate Inline]** .

1. Définissez **[!UICONTROL Enabled for Frontend]** sur `No`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Cochez la case des caches de sortie suivants qui ont été précédemment désactivés :

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Définissez la commande **[!UICONTROL Actions]** sur `Enable`, puis cliquez sur **[!UICONTROL Submit]**.

1. Lorsque vous y êtes invité, actualisez tous les caches non valides.

### Étape 5 : vérifier les modifications dans votre boutique

Accédez à votre storefront et examinez chaque page mise à jour pour vous assurer que les modifications sont correctes. Dans cet exemple, `Customer Login` a été remplacé par `Customer Sign In`. Si des modifications ont été apportées à une vue spécifique, utilisez le sélecteur de langues pour passer à la vue appropriée.

![Exemple de storefront - connexion client traduite](./assets/storefront-translate-inline-customer-sign-in.png){width="700" zoomable="yes"}
