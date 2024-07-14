---
title: Types d’entrée d’attribut
description: Découvrez les types d’entrée disponibles pour les attributs de produit, qui déterminent le type de données pouvant être entrées et le format du champ ou du contrôle d’entrée.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Types d’entrée d’attribut

Lorsqu’ils sont affichés à partir de l’administrateur, les attributs sont les champs que vous remplissez lors de la création d’un produit. Le type d’entrée affecté à un attribut détermine le type de données qui peut être entré et le format du champ ou du contrôle d’entrée. Du point de vue du client, les attributs fournissent des informations sur le produit et sont les options et les champs de saisie de données qui doivent être renseignés pour acheter un produit.

## Types d’entrée

| Propriété | Description |
|--- |--- |
| [!UICONTROL Text Field] | Champ de saisie d’une seule ligne pour le texte. |
| [!UICONTROL Text Area] | Champ de saisie multi-lignes permettant de saisir des paragraphes de texte, comme une description de produit. Vous pouvez utiliser l’éditeur WYSIWYG pour mettre en forme le texte avec des balises d’HTML ou saisir les balises directement dans le texte. |
| [!UICONTROL Text Editor] | Éditeur de texte entièrement fonctionnel à l’emplacement de l’attribut. |
| [!UICONTROL Date] | Affiche une valeur de date au [format recommandé](#date-and-time-options) et [fuseau horaire](../getting-started/store-details.md#locale-options). Les valeurs de date peuvent être sélectionnées à partir d’une liste ou d’un calendrier ( ![Icône Calendrier](../assets/icon-calendar.png) ). <br/><br/>**_Remarque :_**Selon la configuration de votre système, les utilisateurs de_Admin _peuvent saisir des dates directement dans un champ ou sélectionner une date dans le calendrier ou la liste. Pour plus d&#39;informations sur la spécification des valeurs de date et d&#39;heure, voir [Options de date et d&#39;heure](#date-and-time-options). |
| [!UICONTROL Date and Time] | Affiche une valeur de date et d’heure au [format recommandé](#date-and-time-options) et [fuseau horaire](../getting-started/store-details.md#locale-options). La date et l’heure peuvent être saisies manuellement ou sélectionnées à partir d’un calendrier. Exemple de format : MM/JJ/AAAA HH:MM |
| [!UICONTROL Yes/No] | Affiche une liste déroulante avec des options prédéfinies `Yes` et `No`. |
| Liste déroulante | Affiche une liste déroulante de valeurs qui n’acceptent qu’une seule sélection. Le type d’entrée Liste déroulante est un composant clé de [produits configurables](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Affiche une liste déroulante de valeurs qui acceptent plusieurs sélections. |
| [!UICONTROL Price] | Ce type d’entrée est utilisé pour créer des champs de prix en plus des attributs prédéfinis : `Price`, `Special Price`, `Tier Price` et `Cost`. La devise utilisée est déterminée par votre configuration système. |
| [!UICONTROL Media Image] | Associe une image supplémentaire à un produit, tel qu’un logo de produit, des instructions de soin ou des ingrédients d’une étiquette alimentaire. Lorsque vous ajoutez un attribut d’image multimédia au jeu d’attributs d’un produit, il devient un type d’image supplémentaire, avec Base, Petit et Miniature. L’attribut image du média peut être exclu du [navigateur multimédia storefront](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | Permet de définir des [taux FPT](../stores-purchase/fixed-product-tax.md) en fonction des exigences de vos paramètres régionaux. |
| [!UICONTROL Visual Swatch] | Affiche un échantillon représentant la couleur, la texture ou le motif d’un produit configurable. Un [échantillon visuel](swatches.md) peut être rempli avec une valeur de couleur hexadécimale ou afficher une image téléchargée qui représente la couleur, le matériau, la texture ou le motif de l’option. |
| [!UICONTROL Text Swatch] | Représentation textuelle d’une option de produit configurable fréquemment utilisée pour sa taille. [Les échantillons de texte](swatches.md) peuvent également inclure des valeurs de couleur hexadécimales. |
| [!UICONTROL Page Builder] | Un espace de travail [[!DNL Page Builder]](../page-builder/workspace.md) à l’emplacement de l’attribut qui facilite l’ajout de contenu engageant à la page du produit. |

{style="table-layout:auto"}

## Options de date et d’heure

Vous pouvez personnaliser le format des champs Date et Heure, puis sélectionner le contrôle d’entrée utilisé pour la saisie de données. Les valeurs de date peuvent être sélectionnées dans une liste déroulante ou un calendrier contextuel.

![Exemple - storefront popup calendar](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_Pour formater les champs Date/Heure :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et cliquez sur le sous-élément **[!UICONTROL Catalog]** .

1. Développez la section **[!UICONTROL Date & Time Custom Options]** .

   ![Configuration du catalogue - options de date et d’heure](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [_Options personnalisées de date et d’heure_](../configuration-reference/catalog/catalog.md) dans la _référence de configuration_.

1. Pour utiliser un calendrier contextuel comme contrôle d’entrée pour les champs de date, définissez **[!UICONTROL Use JavaScript Calendar]** sur `Yes`.

1. Pour établir le **[!UICONTROL Date Fields Order]**, définissez l’ordre de chaque partie du champ de date selon les besoins :

   - Mois
   - Jour
   - Année

1. Pour définir le format d’heure de votre choix, définissez **Format d’heure** sur l’un des formats suivants :

   - `12h AM/PM`
   - `24h`

1. Pour établir les **[!UICONTROL Year Range]** pour les valeurs déroulantes, saisissez l’année (AAAA) à laquelle définir les dates **[!UICONTROL from]** et **[!UICONTROL to]**.

   S’il est vide, le champ correspond par défaut à l’année en cours.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
