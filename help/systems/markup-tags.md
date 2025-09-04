---
title: Balises de marquage
description: Découvrez les balises de balisage qui contiennent des fragments de code pour référencer un objet dans votre magasin.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Balises de marquage

Une balise de balisage est une directive qui contient un fragment de code avec une référence relative à un objet de votre magasin, tel qu’une variable, une URL, une image ou un bloc. Les balises de balisage peuvent être utilisées partout où l’éditeur est disponible et intégrées à l’HTML de modèles [e-mail](email-templates.md) et [newsletter](../merchandising-promotions/newsletter-template.md), ainsi que d’autres types de [contenu](../content-design/introduction.md#content).

Les balises de balisage sont entourées d’accolades doubles et peuvent être générées par l’outil Widget ou saisies directement dans le contenu HTML. Par exemple, plutôt que de coder en dur le chemin d’accès complet d’une page, vous pouvez utiliser une balise de balisage pour représenter l’URL du magasin. Les balises de balisage présentées dans les exemples suivants sont les suivantes :

{{$include /help/_includes/directives-caution.md}}

## Variable personnalisée

La balise de balisage de variable peut être utilisée pour insérer une [variable personnalisée](variables-custom.md) dans un modèle d’e-mail, des blocs, des newsletters et des pages de contenu.

\{\{CustomVar code= « my_custom_variable »}}

## URL de la boutique

La balise de balisage de l’URL du magasin représente l’URL de base de votre site web et est utilisée comme substitut de la première partie d’une URL complète, y compris le nom de domaine. Il existe deux versions de cette balise de balisage : l’une va directement dans votre magasin, et l’autre comporte une barre oblique (`/`) à la fin, utilisée lorsqu’un chemin est ajouté.

\{\{store url=&#39;vêtements/chaussures/femmes&#39;}}

## URL du média

La balise de balisage d’URL Dynamic Media représente l’emplacement et le nom de fichier d’une image stockée sur un réseau de diffusion de contenu (CDN). La balise peut être utilisée pour placer une image sur une page, un bloc, une bannière ou un modèle d’e-mail.

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## ID de bloc

La balise Balisage de l’ID de bloc est l’une des plus faciles à utiliser. Elle peut être utilisée pour placer un bloc directement sur une page CMS, ou même imbriquée dans un autre bloc. Vous pouvez utiliser cette technique pour modifier un bloc pour différentes promotions ou langues. La balise de balisage ID de bloc référence un bloc par son identifiant.

\{\{block id=&#39;block-id&#39;}}

## Balise du modèle

Une balise de modèle fait référence à un fichier de modèle HTML et peut être utilisée pour afficher le bloc sur une page CMS ou un bloc statique. Le code de l’exemple suivant peut être ajouté à une page ou à un bloc pour afficher le formulaire Nous contacter.

\{\{block class= »Magento\Contact\Block\ContactForm » name=« contactForm » template= »Magento_Contact::form.phtml »}}

Le code de l’exemple suivant peut être ajouté à une page ou à un bloc pour afficher une liste de produits d’une catégorie spécifique, par ID de catégorie.

\{\{block type=« catalog/product_list » category_id=« 22 » template= »catalog/product/list.phtml« }}

## Code du widget

L’outil Widget peut être utilisé pour afficher des listes de produits ou pour insérer des liens complexes, tels qu’un lien vers une page de produit spécifique, en fonction de l’ID de produit. Le code généré inclut la référence du bloc, l’emplacement du module de code et le modèle HTML correspondant. Une fois le code généré, vous pouvez le copier-coller d’un emplacement à un autre.

Le code de l’exemple suivant peut être ajouté à une page ou à un bloc pour afficher la liste des nouveaux produits.

\{\{widget type=« catalog/product_widget_new » display_type=« new_products » products_count=« 10 » template= »catalog/product/widget/new/content/new_grid.phtml« }}

Le code de l’exemple suivant peut être ajouté à une page ou à un bloc pour afficher un lien vers un produit spécifique, par ID de produit.

\{\{widget type=« catalog/product_widget_link » anchor_text=« My Product Link » title=« My Product Link » template= »catalog/product/widgetlink/link_block.phtml » id_path=« product/31 »}}

## Utiliser des balises de balisage dans les liens

Vous pouvez utiliser les balises de balisage avec les balises d’ancrage HTML et le lien direct vers n’importe quelle page de votre boutique. Le lien peut être incorporé dans des pages de contenu, des blocs ou des modèles d’e-mail et de newsletter. Vous pouvez également utiliser cette technique pour lier une image à une page spécifique.

### Étape 1. Identifier l’URL de destination

Si possible, accédez à la page à laquelle vous souhaitez créer le lien, puis copiez l’URL complète à partir de la barre d’adresse de votre navigateur. La partie de l’URL dont vous avez besoin se trouve après le `.com/` . Sinon, copiez la clé URL de la page CMS que vous souhaitez utiliser comme destination du lien.

#### URL complète vers la page de catégorie

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### URL complète vers la page du produit

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### URL complète vers la page CMS

`https://mystore.com/about-us`

### Étape 2. Ajoutez le balisage à l’URL

La balise URL de magasin représente l’URL de base de votre site web et est utilisée comme substitut de la partie adresse HTTP de l’URL de magasin, y compris le nom de domaine et le `.com`. Vous pouvez utiliser deux versions de la balise , en fonction des résultats que vous souhaitez obtenir.

`store direct_url` : fournit des liens directs vers une page.

`store url` - Place une barre oblique à l’extrémité pour que d’autres références puissent être ajoutées sous forme de chemin.

Dans les exemples suivants, la clé d’URL est placée entre guillemets simples et l’ensemble de la balise de balisage est placé entre des accolades doubles. Lorsqu’elle est utilisée avec une balise d’ancrage, la balise de balisage est placée entre les guillemets doubles de l’ancrage. Pour éviter toute confusion, vous pouvez alterner l’utilisation de guillemets simples et doubles pour chaque ensemble imbriqué de guillemets.

Si vous commencez avec une URL complète, supprimez la partie adresse HTTP (`http://` ou `https://`) de l’URL, jusqu’au `.com/` inclus. À sa place, saisissez la balise de balisage de l’URL de la boutique, en commençant par le guillemet simple d’ouverture.

#### Balise de balisage de l’URL du magasin

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

Sinon, saisissez la première partie de la balise de balisage de l’URL du magasin et collez la clé d’URL ou le chemin d’accès que vous avez copié précédemment.

### Balise de balisage d’URL de magasin avec clé d’URL

`{{store url=`

Pour terminer la balise de balisage, saisissez les guillemets doubles et les accolades doubles fermants.

`{{store url='apparel/shoes/womens'}}`

### Étape 3. Terminer la balise d’ancrage

Placez la balise de balisage terminée dans une balise d’ancrage, à l’aide de la balise de balisage au lieu de l’URL cible. Ajoutez ensuite le texte du lien et la balise d’ancrage de fermeture.

#### Balisage dans la balise d’ancrage

\&lt;a href=« \{\{la balise de balisage va ici}}« >Texte du lien\&lt;/a>

Collez la balise d’ancrage terminée dans le code d’une page, d’un bloc, d’une bannière ou d’un modèle d’e-mail CMS où vous souhaitez que le lien apparaisse.

### Lien complet avec balisage

\&lt;a href=« \{\{store url=&#39;habillement/chaussures&#39;}}« >Vente de chaussures\&lt;/a>

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
