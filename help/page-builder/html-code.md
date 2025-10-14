---
title: Éléments - Code HTML
description: Découvrez le type de contenu Code HTML , utilisé pour ajouter des fragments de code HTML, CSS et JavaScript dans l’étape  [!DNL Page Builder] .
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Éléments - Code HTML

Utilisez le type de contenu _Code HTML_ pour ajouter des fragments de code HTML, CSS et JavaScript à l’étape [[!DNL Page Builder] &#x200B;](workspace.md#stage). Par exemple, si vous souhaitez ajouter un HTML personnalisé, déclarez une classe CSS pouvant être appliquée à un élément de la page. Vous pouvez également ajouter un fragment de code pour un logo, un bouton ou une bannière que vous avez reçu d’un fournisseur tiers.

## Boîte à outils Code HTML

![Boîte à outils Code HTML](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| Outil | Icon | Description |
| --------- | ---------- | ----------------- |
| Déplacer | ![&#x200B; Icône Déplacer &#x200B;](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur Code HTML vers un autre emplacement valide sur la page. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier le code HTML , qui permet de modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur Code HTML. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur Code HTML masqué. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur Code HTML. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur Code HTML et son contenu de l’étape. |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajout de code HTML

L&#39;exemple suivant montre comment incorporer du code [Google Font][1] et déclarer des classes d&#39;en-tête personnalisées qui remplacent la feuille de style actuelle.

### Étape 1 : choisir une police Google

1. Rendez-vous sur le site [Google Fonts][1] et sélectionnez la famille de polices que vous souhaitez utiliser.

1. Copiez le code généré à incorporer dans la section `<head>` de la page et collez-le temporairement dans un éditeur de texte.

   - Incorporer le code de police
   - Règle CSS

1. Ajoutez la règle de famille de polices à chaque classe d’en-tête, en plaçant les classes d’en-tête dans une balise `<style>`.

   Ce code est collé dans [!DNL Page Builder].

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### Étape 2 : ajouter le code à la page

1. Dans la barre latérale _Admin_ de votre boutique, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez la page où la police doit être disponible et ouvrez-la en mode d’édition.

1. Faites défiler vers le bas et développez la section **[!UICONTROL Content]** .

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Elements]** et faites glisser un espace réservé **[!UICONTROL HTML Code]** vers une ligne, une colonne ou un ensemble d’onglets sur la scène.

   Utilisez la ligne directrice rouge pour positionner le séparateur avant ou après un autre conteneur de contenu dans l’ensemble de lignes, colonnes ou onglets.

   ![Faire glisser un espace réservé de code HTML vers l’étape](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. Pointez sur le conteneur HTML pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Dans la zone de texte, collez le code des polices Google incorporées et les déclarations de style que vous avez préparés.

   Pour faciliter la lecture, vous pouvez saisir quelques espaces pour mettre le code en retrait.

   ![Code et styles HTML](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. Mettez à jour les paramètres restants si nécessaire (voir [Modifier les paramètres de code HTML](#html-settings) pour plus d’informations).

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

   La nouvelle police s’affiche lorsque la page est consultée via un navigateur.

### Étape 3 : prévisualiser la page

1. Dans la section _[!UICONTROL Currently Active]_, définissez **[!UICONTROL Enable Page]**&#x200B;sur `Yes`.

   ![Activation de la page](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

1. Recherchez la page dans la grille et sélectionnez **[!UICONTROL View]** dans la colonne _[!UICONTROL Actions]_.

   ![Prévisualiser les en-têtes de page avec la nouvelle famille de polices](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## Modifier les paramètres de code d’HTML {#html-settings}

1. Pointez sur le conteneur HTML pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Dans la zone de texte, modifiez le code selon vos besoins.

   Les codes HTML, CSS et JavaScript sont pris en charge. Vous pouvez saisir ici des extraits de code appartenant à la section `<head>` de la page.

   L’éditeur propose également des boutons pour insérer des éléments spéciaux dans le code :

   | Bouton | Description |
   | ------ | ----------- |
   | Insérer un widget... | Cliquez pour insérer un widget à l&#39;emplacement du curseur dans la zone de texte HTML. |
   | Insérer une image... | Cliquez pour insérer une image téléchargée ou une image de la Galerie à la position du curseur dans la zone de texte HTML. |
   | Insérer une variable... | Cliquez pour insérer une variable à la position du curseur dans la zone de texte HTML. |

1. Mettez à jour les paramètres _[!UICONTROL Advanced]_&#x200B;selon vos besoins.

   - Pour contrôler le positionnement du code dans le conteneur parent, choisissez une **[!UICONTROL Alignment]** :

     | Option | Description |
     | ------ | ----------- |
     | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
     | `Left` | Aligne la liste le long de la bordure gauche du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
     | `Center` | Aligne la liste au centre du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
     | `Right` | Aligne le bloc le long de la bordure droite du conteneur parent, en tenant compte de la marge intérieure spécifiée. |

     Dans l’exemple suivant, les options sont définies pour utiliser un alignement centré pour le bloc de code rendu.

     ![Diviseur avec alignement au centre](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur de code :

     | Option | Description |
     | ------ | ----------- |
     | `Default` | Applique le style de bordure par défaut spécifié par la feuille de style associée. |
     | `None` | Ne fournit aucune indication visible des bordures du conteneur. |
     | `Dotted` | La bordure du conteneur s’affiche sous la forme d’une ligne pointillée. |
     | `Dashed` | La bordure du conteneur s’affiche sous la forme d’une ligne en tirets. |
     | `Solid` | La bordure du conteneur s’affiche sous la forme d’une ligne continue. |
     | `Double` | La bordure du conteneur s’affiche sous la forme d’une ligne double. |
     | `Groove` | La bordure du conteneur s’affiche sous la forme d’une ligne rainurée. |
     | `Ridge` | La bordure du conteneur s’affiche sous la forme d’une ligne crantée. |
     | `Inset` | La bordure du conteneur s’affiche sous la forme d’une ligne insérée. |
     | `Outset` | La bordure du conteneur s’affiche sous la forme d’une ligne de départ. |

   - Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

     | Option | Description |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Spécifiez la couleur en choisissant une nuance, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
     | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
     | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

     {style="table-layout:auto"}

   - (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur.

     Séparez plusieurs noms de classe par un espace.

   - Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour déterminer les marges extérieures et la marge intérieure du conteneur de code.

     Saisissez les valeurs correspondantes dans le diagramme.

     | Zone conteneur | Description |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

[1]: https://fonts.google.com/

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
