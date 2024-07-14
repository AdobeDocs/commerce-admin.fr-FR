---
title: Balises marketing
description: Découvrez les balises qui contiennent des fragments de code pour référencer un objet dans votre magasin.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Balises marketing

Une balise de balisage est une directive qui contient un fragment de code avec une référence relative à un objet de votre magasin, tel qu’une variable, une URL, une image ou un bloc. Les balises de balisage peuvent être utilisées partout où l’éditeur est disponible et incorporé dans l’HTML des modèles [email](email-templates.md) et [newsletter](../merchandising-promotions/newsletter-template.md), ainsi que d’autres types de [contenu](../content-design/introduction.md#content).

Les balises de balisage sont entourées de deux accolades et peuvent être générées par l’outil Widget ou directement saisies dans le contenu de l’HTML. Par exemple, plutôt que de coder en dur le chemin d’accès complet à une page, vous pouvez utiliser une balise pour représenter l’URL du magasin. Les balises de balisage présentées dans les exemples suivants sont les suivantes :

{{$include /help/_includes/directives-caution.md}}

## Variable personnalisée

La balise de balisage variable peut être utilisée pour insérer une [variable personnalisée](variables-custom.md) dans un modèle de courrier électronique, des blocs, des newsletters et des pages de contenu.

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## URL du magasin

La balise de balisage d’URL de magasin représente l’URL de base de votre site web et est utilisée comme substitut à la première partie d’une URL complète, y compris le nom de domaine. Il existe deux versions de cette balise de balisage : l’une qui va directement à votre magasin, l’autre avec une barre oblique (`/`) à la fin qui est utilisée lorsqu’un chemin est ajouté.

\{\{url du magasin=&#39;apparel/chaussures/femmes&#39;}}

## URL du média

La balise d’URL de média dynamique représente l’emplacement et le nom de fichier d’une image stockée sur un réseau de diffusion de contenu (CDN). La balise peut être utilisée pour placer une image sur une page, un bloc, une bannière ou un modèle de courrier électronique.

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## Identifiant du bloc

La balise de balisage d’identifiant de bloc est l’une des plus faciles à utiliser. Elle peut être utilisée pour placer un bloc directement sur une page CMS, voire l’imbriquer dans un autre bloc. Vous pouvez utiliser cette technique pour modifier un bloc pour différentes promotions ou langues. La balise de balisage d’identifiant de bloc fait référence à un bloc à l’aide de son identifiant.

\{\{block id=&#39;block-id&#39;}

## Balise de modèle

Une balise de modèle fait référence à un fichier de modèle PHTML et peut être utilisée pour afficher le bloc sur une page CMS ou un bloc statique. Le code de l&#39;exemple suivant peut être ajouté à une page ou à un bloc pour afficher le formulaire de contact.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}

Le code de l’exemple suivant peut être ajouté à une page ou à un bloc pour afficher une liste de produits d’une catégorie spécifique, par identifiant de catégorie.

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}

## Code widget

L’outil Widget peut être utilisé pour afficher des listes de produits ou pour insérer des liens complexes, tels que celui qui accède à une page de produit spécifique, en fonction de l’ID du produit. Le code généré inclut la référence de bloc, l’emplacement du module de code et le modèle PHTML correspondant. Une fois le code généré, vous pouvez le copier et le coller d’un emplacement à un autre.

Le code de l’exemple suivant peut être ajouté à une page ou à un bloc pour afficher la liste des nouveaux produits.

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}

Le code de l’exemple suivant peut être ajouté à une page ou à un bloc pour afficher un lien vers un produit spécifique, par ID de produit.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;My Product Link&quot; title=&quot;My Product Link&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## Utilisation de balises dans les liens

Vous pouvez utiliser des balises avec des balises d’ancrage d’HTML et créer un lien direct vers n’importe quelle page de votre magasin. Le lien peut être intégré à des pages de contenu, des blocs ou des modèles d’email et de newsletter. Vous pouvez également utiliser cette technique pour lier une image à une page spécifique.

### Étape 1. Identification de l’URL de destination

Si possible, accédez à la page à laquelle vous souhaitez créer un lien et copiez l’URL complète dans la barre d’adresse de votre navigateur. La partie de l’URL dont vous avez besoin se trouve après le `.com/`. Sinon, copiez la clé URL de la page CMS que vous souhaitez utiliser comme destination du lien.

#### URL complète vers la page de catégorie

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### URL complète vers la page de produit

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### URL complète vers la page CMS

`https://mystore.com/about-us`

### Étape 2. Ajouter les balises à l’URL

La balise URL du magasin représente l’URL de base de votre site web et est utilisée comme substitut à la partie adresse HTTP de l’URL du magasin, y compris le nom de domaine et `.com`. Il existe deux versions de la balise, que vous pouvez utiliser, en fonction des résultats que vous souhaitez obtenir.

`store direct_url` - Liens directement vers une page.

`store url` - Place une barre oblique à la fin, de sorte que des références supplémentaires peuvent être ajoutées en tant que chemin.

Dans les exemples suivants, la clé URL est entourée de guillemets simples et l’ensemble de la balise de balisage est entouré d’accolades doubles. Lorsqu’elle est utilisée avec une balise d’ancrage, celle-ci est placée entre les guillemets doubles de l’ancre. Pour éviter toute confusion, vous pouvez alterner à l’aide de guillemets simples et doubles pour chaque ensemble imbriqué de guillemets.

Si vous commencez avec une URL complète, supprimez la partie de l’URL (`http://` ou `https://`) de l’adresse HTTP, via et incluant l’ `.com/`. À la place, saisissez la balise de balisage URL de magasin, en passant par le guillemet simple d’ouverture.

#### Balise de balisage de l’URL de magasin

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

Sinon, saisissez la première partie de la balise Store URL et collez la clé ou le chemin d’accès de l’URL que vous avez copié précédemment.

### Balise de balisage URL de magasin avec clé URL

`{{store url=`

Pour terminer la balise de balisage, saisissez les guillemets doubles fermants et les accolades doubles.

`{{store url='apparel/shoes/womens'}}`

### Étape 3. Fin de la balise d’ancrage

Placez la balise de balisage complétée à l’intérieur d’une balise d’ancrage, à l’aide de la balise de balisage au lieu de l’URL cible. Ajoutez ensuite le texte du lien et la balise d’ancrage de fermeture.

#### Balisage dans la balise d’ancrage

\&lt;a href=&quot;\{\{la balise de balisage va ici}&quot;>Texte de lien\&lt;/a>

Collez la balise d’ancrage complétée dans le code d’une page, d’un bloc, d’une bannière ou d’un modèle de courrier électronique CMS dans lequel vous souhaitez que le lien s’affiche.

### Lien complet avec balisage

\&lt;a href=&quot;\{\{store url=&#39;apparel/chaussures&#39;}}&quot;>Vente de chaussures\&lt;/a>
