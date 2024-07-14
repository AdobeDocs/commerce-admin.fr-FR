---
title: Pages
description: Découvrez les pages de contenu principal incluses dans le magasin de démonstration  [!DNL Commerce] et modifiez la configuration Pages par défaut.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Pages

Le contenu peut être visualisé en termes de durée de vie, comme n’importe quel produit d’un magasin. Saviez-vous que la durée de vie du contenu des médias sociaux est inférieure à 24 heures ? La durée de vie potentielle du contenu que vous créez peut vous aider à décider où investir vos ressources.

Le contenu avec une longue durée de conservation est parfois appelé _contenu vert constant_. Parmi les exemples de contenus sans cesse renouvelés, citons les succès client, les instructions _how to_ et la FAQ (questions fréquentes). En revanche, les contenus périssables par nature incluent des événements, des nouvelles de l&#39;industrie et des communiqués de presse.

![Page À propos de nous incluse dans l’exemple de magasin Luma ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Pages de contenu principal

La boutique de démonstration [!DNL Commerce] contient des exemples de pages de contenu principal pour vous aider à démarrer. Toutes ces pages peuvent être modifiées selon vos besoins. Consultez les pages suivantes de votre boutique et assurez-vous que le contenu véhicule votre message, votre voix et votre marque.

### Accueil

La page de démonstration [Accueil](../getting-started/storefront.md#home-page) comprend une bannière, un carrousel d’image, plusieurs blocs statiques avec des liens et une liste de nouveaux produits.

### Politique de confidentialité

La page [Politique de confidentialité](../getting-started/privacy-policy.md) du magasin doit être mise à jour avec vos propres informations. En règle générale, votre politique de confidentialité doit expliquer à vos clients le type d’informations que votre entreprise collecte et leur utilisation.

### 404 Introuvable

La page 404 Page introuvable est nommée pour le code de réponse renvoyé lorsqu’une page est introuvable. Les redirections d’URL réduisent le nombre d’affichages de cette page. Cependant, lorsque cela est nécessaire, vous pouvez tout aussi bien profiter de l’occasion pour proposer des liens vers des produits que le client pourrait trouver intéressants.

### Accès refusé

{{b2b-feature}}

La page [Accès refusé](../b2b/account-company-roles-permissions.md) s’affiche lorsque les autorisations attribuées à un utilisateur de l’entreprise empêchent l’accès à la page.

### Activation des cookies

La page [Activer les cookies](../getting-started/compliance-cookie-law.md) s’affiche lorsque les cookies des visiteurs de votre site ne sont pas activés dans leur navigateur. La page fournit des instructions détaillées et illustrées pour activer les cookies pour les navigateurs les plus populaires.

### Service indisponible

La page [503 Service Unavailable](../configuration-reference/general/general.md) est nommée pour le code de réponse renvoyé lorsque le serveur est indisponible.

### À propos de nous

La page À propos de nous est liée à partir du pied de page de votre boutique. Vous pouvez inclure des images, des vidéos, des liens vers des communiqués de presse et des annonces. L’exemple de page comporte une image à droite et une image décorative pour indiquer la fin de la page.

### Service client

La page Service client est un autre noeud de la hiérarchie de la page. Les deux en-têtes de la page contiennent du contenu qui ne devient visible que lorsque le client clique sur l’en-tête.

![Page du service client sur le storefront](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Configuration des pages par défaut

La configuration _Pages par défaut_ détermine la page d’entrée associée à l’ [URL de base](../stores-purchase/store-urls.md) et la page d’accueil correspondante. Il détermine également la page qui s’affiche lorsqu’une erreur _Page introuvable_ se produit et si un [chemin de navigation](../catalog/navigation-breadcrumb-trail.md) apparaît en haut de chaque page.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Default Pages]** .

   ![Pages par défaut](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Affichage en magasin | Indique la landing page associée à l’URL de base. Par défaut, ce champ est défini sur `cms` pour indiquer une page du système de gestion de contenu [!DNL Commerce]. Vous pouvez également utiliser un autre type de landing page, tel qu’un blog. Par exemple, si un blog est installé sur le serveur à l’emplacement `magento/blog`, vous pouvez saisir le nom du dossier `blog` comme chemin d’accès relatif à la sélection des pages. |
   | [!UICONTROL CMS Home Page] | Affichage en magasin | Pour choisir la page d’accueil du magasin, sélectionnez simplement la page CMS dans la liste. Par défaut, la page d’accueil du CMS répertorie l’ensemble des pages CMS disponibles pour votre magasin. |
   | [!UICONTROL Default No-route URL] | Affichage en magasin | Contient l’URL de la page par défaut que vous souhaitez afficher lorsqu’une erreur `404 Page not Found` se produit. La valeur par défaut est `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Affichage en magasin | Identifie une page CMS spécifique que vous souhaitez afficher lorsqu’une erreur 404 Page introuvable se produit. La page par défaut est `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Affichage en magasin | Identifie une page CMS spécifique qui s’affiche lorsque les cookies ne sont pas activés pour le navigateur. La page explique pourquoi les cookies sont utilisés et comment les activer pour chaque navigateur. La page par défaut est `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Affichage en magasin | Détermine si un chemin de navigation apparaît sur toutes les pages CMS du catalogue. Options : `Yes` / `No` |

   {style="table-layout:auto"}

1. Pour **[!UICONTROL Default Web URL]**, saisissez le chemin d’accès relatif au dossier dans l’installation [!DNL Commerce] contenant la landing page.

   Le paramètre par défaut, `cms`, indique une page provenant du système de gestion de contenu [!DNL Commerce].

   >[!NOTE]
   >
   >Pour une vue de magasin spécifique, décochez la case **[!UICONTROL Use Default]** en regard de _[!UICONTROL Default Web URL]_et tous les autres paramètres par défaut à modifier.

1. Définissez **[!UICONTROL CMS Home Page]** sur la page CMS à utiliser comme page d’accueil. D’autres pages créées peuvent être utilisées comme page d’accueil, par exemple :

   - Bienvenue dans la boutique en ligne exclusive
   - Points récompensés
   - À propos de nous
   - Service client
   - Activation des cookies
   - Politique de confidentialité
   - Société : accès refusé

1. Pour **[!UICONTROL Default No-route URL]**, saisissez le chemin d’accès relatif au dossier dans l’installation [!DNL Commerce] où la page est redirigée lorsqu’une erreur _404 Page introuvable_ se produit.

   La valeur par défaut est `cms/index/noRoute`.

1. Définissez **[!UICONTROL CMS No Route Page]** sur la page CMS qui s’affiche lorsqu’une erreur _404 Page introuvable_ se produit.

1. Définissez **[!UICONTROL CMS No Cookies Page]** sur la page CMS qui s’affiche lorsque les cookies sont désactivés dans le navigateur. La page explique pourquoi les cookies sont utilisés et comment les activer pour chaque navigateur. La page par défaut est `Enable Cookies`.

1. Si vous souhaitez qu’un chemin de navigation s’affiche en haut de toutes les pages CMS, définissez **[!UICONTROL Show Breadcrumbs for CMS Pages]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
