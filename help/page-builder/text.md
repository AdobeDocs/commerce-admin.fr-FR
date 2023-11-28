---
title: Eléments - Texte
description: En savoir plus sur le type de contenu Texte , utilisé pour ajouter un conteneur de texte dans le [!DNL Page Builder] scène.
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Eléments - Texte

Utilisez la variable _Texte_ type de contenu pour ajouter un conteneur de texte avec un éditeur WYSIWYG (&quot;Ce que vous voyez est ce que vous obtenez&quot;) dans la variable [[!DNL Page Builder] étape](workspace.md#stage). Vous pouvez en outre ajouter des liens, des images, des [variables](../systems/variables-predefined.md)et des widgets au texte à partir de la barre d’outils de l’éditeur.

![Texte formaté sur une bannière](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Outils de l’éditeur de texte

Vous pouvez accéder à l’éditeur de texte directement à partir de l’étape ou d’une page de paramètres. Les modifications apportées directement à la scène sont enregistrées automatiquement. Pour plus d’informations, voir [Utilisation de l’éditeur](../content-design/editor.md).

![Outil d’éditeur de texte - TinyMCE](./assets/pb-elements-text-editor-tools.png){width="600"}

## Zone d’outils Conteneur de texte

![Zone d’outils Conteneur de texte](./assets/pb-elements-text-toolbox.png){width="600"}

| Outil | Icône | Description |
| --------- | --------------------- | -------------- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur de texte vers un autre emplacement valide sur la page. |
| (label) | TEXTE | Identifie le conteneur actif en tant qu’élément de texte. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre les propriétés du conteneur de texte en mode d’édition. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur de texte. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur de texte masqué. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur de texte. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de texte et son contenu de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter du texte

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Elements]** et faites glisser un **[!UICONTROL Text]** d’un espace réservé à une ligne, une colonne ou un ensemble d’onglets sur l’étape.

   ![Faire glisser un espace réservé de texte sur l’étape](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. Utilisez l’éditeur pour saisir et mettre en forme le texte, le cas échéant.

   Pour plus d’informations, voir [Utilisation de l’éditeur](../content-design/editor.md).

   ![Éditeur de texte avec contenu](./assets/pb-elements-text-editor.png){width="600"}

## Création d’un lien

Le bouton Insérer un lien de l’éditeur facilite l’ajout d’un lien hypertexte à une image dans la galerie. Cependant, il peut également être utilisé pour créer un lien intégré dans du texte, si vous disposez déjà de l’URL. Contrairement au bouton Widget, le bouton Insérer/Modifier le lien n’est pas intégré aux pages, produits ou catégories du magasin.

Pour créer un lien vers un numéro de téléphone ou un email, voir [Ajout de variables personnalisées](../systems/variables-custom.md).

1. Dans le storefront, accédez à la page qui doit être la destination cible du lien et copiez les informations sur le lien.

   Vous pouvez utiliser l’URL complète ou une URL relative qui omet la référence à votre domaine de magasin.

   URL complète - `https://mystore.com/women/tops-women/tees-women.html`

   URL relative - `../women/tops-women/tees-women.html`

1. Sélectionnez le texte dans l’espace de l’éditeur, puis cliquez sur _Lien d’insertion/de modification_ ( ![Bouton Insérer/Modifier un lien](./assets/pb-icon-add-link.png){width="20"} ) dans la barre d’outils de l’éditeur.

   ![Ajout d’un lien vers du texte formaté](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. Pour **[!UICONTROL URL]**, saisissez le lien relatif que vous avez préparé.

1. Définir **[!UICONTROL Target]** to `None`.

   Ce paramètre permet d’ouvrir la page dans la même fenêtre du navigateur, plutôt que d’ouvrir un nouvel onglet.

1. Pour **[!UICONTROL Title]**, saisissez `Shop Tees`.

   La variable `Title` L’attribut link est utilisé par certains navigateurs comme info-bulle.

1. Pour enregistrer le lien et revenir au [!DNL Page Builder] espace de travail, cliquez sur **[!UICONTROL OK]**.

   ![Détails du lien](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## Insérer une image

1. Placez le curseur dans le texte à l’endroit où vous souhaitez insérer l’image.

1. Cliquez sur _Insérer/modifier une image_ ( ![Bouton Insérer/modifier une image](./assets/icon-pb-add-image.png){width="20"} ) dans la barre d’outils de l’éditeur.

1. Pour **[!UICONTROL Source]**, cliquez sur l’icône de recherche pour utiliser l’espace de stockage multimédia pour localiser et sélectionner une image.

1. Pour **[!UICONTROL Image Description]**, saisissez un texte descriptif pour l’image.

   Ce texte renseigne la variable `alt` l’attribut link pour l’image et est utilisé par certains navigateurs pour l’accessibilité.

1. Saisissez la largeur et la hauteur. **[!UICONTROL Dimensions]**, en pixels, pour le rendu de l’image sur la page.

   Conserver la variable **[!UICONTROL Constrain proportions]** cochée pour conserver automatiquement les proportions de l’image.

1. Pour insérer l’image, puis revenir au [!DNL Page Builder] espace de travail, cliquez sur **[!UICONTROL OK]**.

## Modification des paramètres de texte

1. Passez la souris sur le conteneur de texte pour afficher la boîte à outils et sélectionnez l’option _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   >[!NOTE]
   >
   >Étant donné que le conteneur de texte est imbriqué de manière stricte dans un autre conteneur, assurez-vous que vous disposez de la boîte à outils appropriée.

1. Mettez à jour le contenu suivant vos besoins.

1. Mettez à jour le _[!UICONTROL Advanced]_selon les besoins.

   - Pour contrôler le positionnement du texte dans le conteneur parent, choisissez une **[!UICONTROL Alignment]**:

     | Option | Description |
     | ------ |------------ |
     | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
     | `Left` | Aligne la liste le long de la bordure gauche du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
     | `Center` | Aligne la liste au centre du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
     | `Right` | Aligne le bloc le long de la bordure droite du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |

     {style="table-layout:auto"}

   - Définissez la variable **[!UICONTROL Border]** style appliqué aux quatre côtés du conteneur de texte :

     | Option | Description |
     | ------ |------------ |
     | `Default` | Applique le style de bordure par défaut spécifié par la feuille de style associée. |
     | `None` | Ne fournit aucune indication visible des bordures du conteneur. |
     | `Dotted` | La bordure du conteneur s’affiche sous la forme d’une ligne pointillée. |
     | `Dashed` | La bordure du conteneur s’affiche sous la forme d’une ligne en pointillés. |
     | `Solid` | La bordure du conteneur s’affiche sous la forme d’une ligne pleine. |
     | `Double` | La bordure du conteneur s’affiche sous la forme d’une ligne double. |
     | `Groove` | La bordure du conteneur s’affiche sous forme de ligne droite. |
     | `Ridge` | La bordure du conteneur s’affiche sous la forme d’une ligne à droite. |
     | `Inset` | La bordure du conteneur s’affiche sous la forme d’une ligne d’insertion. |
     | `Outset` | La bordure du conteneur apparaît comme une ligne de départ. |

     {style="table-layout:auto"}

   - Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

     | Option | Description |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
     | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
     | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

     {style="table-layout:auto"}

   - (Facultatif) Indiquez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur.

     Séparez plusieurs noms de classe par un espace.

   - Saisissez des valeurs, en pixels, pour la variable **[!UICONTROL Margins and Padding]** pour déterminer les marges extérieures et la marge intérieure du conteneur de texte.

     Saisissez les valeurs correspondantes dans le diagramme.

     | Zone de conteneur | Description |
     | -------------- |------------ |
     | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir au [!DNL Page Builder] workspace.
