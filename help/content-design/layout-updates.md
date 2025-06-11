---
title: Mises à jour de la disposition
description: Découvrez comment utiliser les mises à jour de disposition pour personnaliser la disposition d’une page.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 0%

---

# Mises à jour de la disposition

Avant de commencer à travailler avec des mises à jour de disposition personnalisées, il est important de comprendre comment les pages de votre boutique sont construites et la différence entre les termes *mise en page* et *mise à jour de disposition*. La mise en page fait référence à la composition visuelle et structurelle de la page. La mise à jour de la disposition fait référence à un ensemble spécifique d’instructions XML qui peuvent remplacer ou personnaliser la construction de la page.

La disposition XML de votre magasin de [!DNL Commerce] est une structure hiérarchique de conteneurs et de blocs. Certains éléments apparaissent sur chaque page, tandis que d’autres apparaissent uniquement sur des pages spécifiques. Pour en savoir plus sur la disposition, les conteneurs et les blocs, consultez la [présentation des dispositions](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) dans le _guide de développement de Frontend_.

L’outil [Widget](widgets.md) est un moyen facile d’ajouter un [bloc de contenu](blocks.md) existant à la disposition par défaut d’une page. Pour les mises à jour plus avancées, vous devez enregistrer le code de mise à jour de la mise en page XML sur le serveur, puis référencer le fichier en tant que mise à jour de mise en page personnalisée par l’administrateur. Pour une présentation du processus, voir [Utiliser les mises à jour de disposition](layout-updates.md#place-a-block-using-layout-updates).

Dans le diagramme suivant, les noms qui font référence aux conteneurs sont noirs et les types de blocs, ou chemins de classe de bloc, sont bleus.

![Diagramme de disposition en blocs standard](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Type de bloc | Description |
|--- |--- |
| `page/html` | Le nom de ce bloc est `root` et il s’agit de l’un des rares blocs racine de la disposition. Vous pouvez également créer votre propre bloc et le nommer `root`, qui est le nom standard des blocs de ce type. Il ne peut y avoir qu’un seul bloc de ce type par page. |
| `page/html_head` | Le nom du bloc est `head` et il est l’enfant du bloc racine. Chaque page ne peut contenir qu’un seul bloc de ce type, qui ne doit pas être supprimé. |
| `page/html_notices` | Le nom du bloc est `global_notices` et il est l’enfant du bloc racine. Si ce bloc est supprimé de la disposition, les avis globaux n’apparaissent pas sur la page. Il ne peut y avoir qu’un seul bloc de ce type par page. |
| `page/html_header` | Le nom du bloc est `header` et il est l’enfant du bloc racine. Ce bloc correspond à l’en-tête visuel en haut de la page et contient plusieurs blocs standard. Chaque page ne peut contenir qu’un seul bloc de ce type, qui ne doit pas être supprimé. |
| `page/html_wrapper` | Bien qu’il soit inclus dans la disposition par défaut, ce bloc est obsolète et n’est inclus que pour garantir une rétrocompatibilité. N’utilisez pas de blocs de ce type. |
| `page/html_breadcrumbs` | Le nom de ce bloc est `breadcrumbs` et il est un enfant du bloc d’en-tête . Ce bloc affiche le chemin de navigation de la page active. Il ne peut y avoir qu’un seul bloc de ce type par page. |
| `page/html_footer` | Le nom du bloc est `footer` et il est l’enfant du bloc racine. Le bloc de pied de page correspond au pied de page visuel en bas de la page et contient plusieurs blocs standard. Chaque page ne peut contenir qu’un seul bloc de ce type, qui ne doit pas être supprimé. |
| `page/template_links` | La mise en page standard comporte deux blocs de ce type. Le bloc `top.links` est un enfant du bloc d’en-tête et correspond au menu de navigation supérieur. Le bloc `footer_links` est un enfant du bloc de pied de page et correspond au menu de navigation du bas. <br/><br/>**_Remarque :_**&#x200B;il est possible de manipuler les liens du modèle, comme le montrent les exemples. |
| `page/switch` | Dans une disposition standard, il existe deux blocs de ce type. Le bloc `store_language` est un enfant du bloc d’en-tête et correspond au sélecteur de langue supérieur. Le bloc `store_switcher` est un enfant du bloc de pied de page et correspond au sélecteur de magasin inférieur. |
| core/messages | Dans une disposition standard, il existe deux blocs de ce type. Le bloc `global_messages` affiche des messages globaux. Le bloc `messages` est utilisé pour afficher tous les autres messages. Si vous supprimez ces blocs, le client ne verra aucun message. |
| `core/text_list` | Ce type de bloc est largement utilisé dans [!DNL Commerce] comme espace réservé pour le rendu des blocs enfants. |
| `core/profiler` | Il n’existe qu’une seule instance de ce type de bloc par page. Il est utilisé pour le profileur de [!DNL Commerce] interne et ne doit pas être utilisé à d’autres fins. |

{style="table-layout:auto"}

## Placer un bloc à l’aide des mises à jour de la disposition

[Les mises à jour de la disposition](layout-updates.md) permettent de personnaliser la disposition d’une page. Les mises à jour de la disposition offrent plus de flexibilité qu’un [widget](widgets.md), mais nécessitent un accès au serveur et des connaissances de base en XML.

Les étapes suivantes indiquent comment utiliser une mise à jour de mise en page pour placer un bloc sur une page. Pour obtenir des exemples spécifiques et de l’aide sur la syntaxe, voir [Tâches courantes de personnalisation de la disposition](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) dans le _Guide de développement de Frontend_.

### Étape 1 : créer le bloc

1. Créez le [bloc](block-add.md) que vous souhaitez placer.

1. Prenez note de la `block_id`, car elle est utilisée dans les instructions de mise à jour de la mise en page.

### Étape 2 : Composer la mise à jour de la mise en page en XML

1. Composez les instructions de mise en page en XML pour [référencer un bloc CMS](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Enregistrez les [instructions de mise en page](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) sur le serveur, dans le dossier de mise en page où les fichiers XML sont enregistrés pour le thème.

   Par exemple :

   `<theme_dir>/<Namespace>_<Module>/layout`

   L’identificateur de mise en page est le nom de fichier qui commence par `cms_page_view_selectable_`, suivi de la clé URL de la page CMS, de l’option de mise à jour de la mise en page et du suffixe du fichier `xml`. Dans l’exemple suivant, `customer-service` est la clé URL de la page et `ChatTool` est l’option que vous sélectionnez pour appliquer la mise à jour de la disposition à la page.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Élément | Description |
   |--- |--- |
   | Identifiant de page CMS | Clé URL de la page avec une barre oblique (`/`) remplacée par un trait de soulignement (`_`). |
   | Nom de mise à jour de la disposition | L’option qui s’affiche pour _Mise à jour de la disposition personnalisée_. |

   {style="table-layout:auto"}

### Étape 3 : référencer la mise à jour de la disposition à partir de la page

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez la page sur laquelle vous souhaitez placer le bloc et ouvrez-la en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Design]** .

1. Pour afficher toutes les mises à jour de disposition disponibles associées à la page, cliquez sur le menu **[!UICONTROL Custom Layout Update]**.

   ![Liste de mise à jour de la disposition personnalisée](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Sélectionnez la mise à jour de disposition à appliquer à la page.

### Étape 4 : enregistrer et actualiser le cache

1. Cliquez ensuite sur **[!UICONTROL Save & Close]**.

1. Dans le message situé en haut de l’espace de travail, cliquez sur **[!UICONTROL Cache Management]** et actualisez tous les éléments de cache non valides.
