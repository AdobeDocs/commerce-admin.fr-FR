---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL General] &gt; [!UICONTROL Web] de l’administrateur Commerce.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Options générales](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Champ | Champ d’application | Description |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Global | Si les réécritures de serveur web sont activées, insère le code de magasin de la vue actuelle dans l’URL. Options : `Yes` / `No`. <br />Lorsque ce champ est défini sur `Yes`, vous devez inclure les codes de magasin dans les URL de votre navigateur pour vous assurer que les réécritures d’URL sont correctement mappées et que toutes les pages sont ouvertes avec succès. Cela évite les erreurs _404 Page introuvable_. |
| [!UICONTROL Auto-redirect to Base URL] | Affichage en magasin | (Pour les configurations à une seule boutique) En cas de lien rompu sur votre site, redirige le trafic vers l’URL de base, plutôt que vers une page avec un message &quot;404 Page introuvable&quot;. Options : ` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Important :_**N’utilisez pas la redirection automatique vers l’URL de base pour les configurations multi-magasin. |
| [!UICONTROL Catalog media URL format] | Global | Définit le [format d’URL](../../catalog/catalog-urls.md) affecté aux produits et aux catégories. Options : hachage unique par variante d’image (mode hérité) définit le nom de fichier converti en tant que valeur de hachage unique. L’optimisation des images basée sur les paramètres de requête définit le processus [d’optimisation d’image](../../content-design/media-gallery-image-optimization.md) en fonction des paramètres de requête. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web > Optimisation du moteur de recherche](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Affichage en magasin | Les systèmes basés sur PHP incluent généralement un fichier appelé `index.php` dans le dossier racine. Par défaut, le nom de fichier apparaît dans l’URL juste après le nom du dossier racine. Lorsque cette option est activée, le système omet `index.php` de l’URL. Cette bonne pratique en matière d’utilisation rend chaque URL plus concise et n’a aucun impact sur les performances ou le classement du site. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > URL de base](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Base URL] | Affichage en magasin | Adresse complète du dossier racine Commerce qui ne s’exécute pas sur un canal chiffré (SSL). L’URL doit se terminer par une barre oblique. |
| [!UICONTROL Base Link URL] | Affichage en magasin | Balise de balisage utilisée comme espace réservé pour l’URL de base. |
| [!UICONTROL Base URL for Static View Files] | Affichage en magasin | Chemin d’accès pointant vers l’emplacement des fichiers statiques utilisés par le thème, tels que CSS, polices, images et JavaScript. Un espace réservé est utilisé pour représenter l’URL de base. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier différent pour chaque site. Définissez la portée de configuration sur le site approprié avant de saisir l’URL de base pour les fichiers d’affichage statique. Vous pouvez également spécifier un dossier en dehors de votre installation Commerce. |
| [!UICONTROL Base URL for User Media Files] | Affichage en magasin | Chemin d’accès qui pointe vers l’emplacement des images du catalogue et d’autres fichiers multimédia. Un espace réservé est utilisé pour représenter l’URL de base. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier multimédia différent pour chacun d’eux. Vous avez ainsi la possibilité de sauvegarder et de restaurer séparément chaque dossier multimédia. Vous pouvez également spécifier un dossier multimédia en dehors de votre installation Commerce. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > URL de base (sécurisé)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Affichage en magasin | Adresse complète du dossier racine Commerce fourni avec le protocole sécurisé (SSL/TLS) chiffré. L’URL doit se terminer par une barre oblique. |
| [!UICONTROL Secure Base Link URL] | Affichage en magasin | Balise de balisage utilisée comme espace réservé pour l’URL de base qui s’exécute sur un canal sécurisé. |
| [!UICONTROL Secure Base URL for Static View Files] | Affichage en magasin | Balise de balisage qui pointe vers l’emplacement des fichiers statiques tels que CSS, les polices, les images et JavaScript utilisés par le thème. Les fichiers peuvent se trouver sur un canal non sécurisé ou sécurisé. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier différent pour chaque site. Définissez la portée de configuration sur le site approprié avant de saisir l’URL de base pour les fichiers d’affichage statique. Vous pouvez également spécifier un dossier en dehors de votre installation Commerce. |
| [!UICONTROL Secure Base URL for User Media Files] | Affichage en magasin | Chemin d’accès qui pointe vers l’emplacement des images du catalogue et d’autres fichiers multimédia. Les fichiers peuvent se trouver sur un canal non sécurisé ou sécurisé. Un espace réservé est utilisé pour représenter l’URL de base. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier multimédia différent pour chacun d’eux. Vous avez ainsi la possibilité de sauvegarder et de restaurer séparément chaque dossier multimédia. Vous pouvez également spécifier un dossier multimédia en dehors de votre installation Commerce. |
| [!UICONTROL Use Secure URLs on Storefront] | Affichage en magasin | Si votre domaine comporte un certificat de sécurité, vous pouvez choisir d’exécuter storefront, avec ou sans chiffrement SSL. Options : <br />**`Yes`**- Les URL de magasin commencent par `https` pour indiquer que la page est fournie avec un protocole chiffré et sécurisé.<br />**`No`** - Les URL du magasin commencent par `http` pour indiquer que la page est diffusée sans protocole sécurisé. |
| [!UICONTROL Use Secure URLs in Admin] | Global | Si votre domaine comporte un certificat de sécurité, vous pouvez choisir d’exécuter l’administrateur de la boutique, avec ou sans chiffrement SSL. Options : <br />**`Yes`**- Les URL d’administration commencent par `https` pour indiquer que la page est fournie avec un protocole chiffré et sécurisé.<br />**`No`** - Les URL d’administration commencent par `http` pour indiquer que la page est diffusée sans protocole sécurisé.<br /> Lorsque les URL sécurisées sont activées pour le magasin et l’administrateur, deux champs supplémentaires s’affichent pour activer et configurer `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Affichage en magasin | Lorsqu&#39;elle est activée, [`HSTS`][1] fournit une mesure de sécurité contre les attaques &quot;man in the middle&quot; et empêche les utilisateurs de remplacer le message &quot;certificat non valide&quot;. Options : `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Affichage en magasin | Lorsqu’elle est activée, convertit les requêtes non sécurisées (`HTTP`) reçues du navigateur en protocole sécurisé (`HTTPS`). Options : `Yes` / `No` |
| [!UICONTROL Offloader Header] | Global | Spécifie la valeur `offloader_header` dans la configuration du serveur pour identifier le protocole entre le client et l’équilibreur de charge. La plupart des installations Commerce utilisent la valeur par défaut `X-Forwarded-Proto` (XFP) pour identifier le protocole comme `HTTP` ou `HTTPS`. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web > Pages par défaut](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Affichage en magasin | Indique la landing page associée à l’URL de base. Cette valeur est définie par défaut sur &quot;cms&quot; pour indiquer une page du système de gestion de contenu Commerce (CMS). Vous pouvez également utiliser un autre type de landing page, tel qu’un blog. Par exemple, si un blog est installé sur le serveur à l’emplacement `magento/blog`, vous pouvez saisir le nom du dossier &quot;blog&quot; comme chemin relatif à la sélection des pages. |
| [!UICONTROL CMS Home Page] | Affichage en magasin | Pour choisir la page d’accueil du magasin, sélectionnez simplement la page CMS dans la liste. Par défaut, la page d’accueil de CMS répertorie l’ensemble des pages CMS disponibles pour votre boutique. |
| [!UICONTROL Default No-route URL] | Affichage en magasin | Contient l’URL de la page par défaut que vous souhaitez afficher lorsqu’une erreur `404 Page not Found` se produit. La valeur par défaut est `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Affichage en magasin | Identifie une page CMS spécifique que vous souhaitez afficher lorsqu’une erreur 404 Page introuvable se produit. La page par défaut est 404 Not Found. |
| [!UICONTROL CMS No Cookies Page] | Affichage en magasin | Identifie une page CMS spécifique qui s’affiche lorsque les cookies ne sont pas activés pour le navigateur. La page explique pourquoi les cookies sont utilisés et comment les activer pour chaque navigateur. La page par défaut est Activer les cookies. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Affichage en magasin | Détermine si un chemin de navigation s’affiche sur toutes les pages CMS du catalogue. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![Disposition par défaut](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/design/layout/page-layout) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Global | Détermine la [mise en page](../../content-design/page-layout.md) utilisée par défaut pour les pages de produits. Options : <br/>**`No layout updates`**- Par défaut, les mises à jour de mise en page ne sont pas disponibles pour les pages de produits.<br/>**`Empty`** - Par défaut, utilise une mise en page vierge pour les pages de produits. <br/>**`1 column`**- Par défaut, utilise une mise en page à une seule colonne pour les pages de produits.<br/>**`2 columns with left bar`** - Par défaut, utilise une mise en page à deux colonnes avec la barre latérale gauche pour les pages de produit. <br/>**`2 columns with right bar`**- Par défaut, utilise une mise en page à deux colonnes avec la barre latérale à droite pour les pages de produit.<br/>**`3 columns`** - Par défaut, utilise une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages de produits.<br/>**`Page -- Full Width`**- (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Page - Largeur complète pour les pages de produit.<br/>**`Category - Full Width`** - (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Catégorie - Largeur complète pour les pages de produit. <br/>**`Product - Full Width`**- (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Produit - Largeur complète pour les pages de produit. |
| [!UICONTROL Default Category Layout] | Global | Détermine la [mise en page](../../content-design/page-layout.md) utilisée par défaut pour les pages de catégorie. Options : <br/>**`No layout updates`**- Par défaut, les mises à jour de mise en page ne sont pas disponibles pour les pages de catégorie.<br/>**`Empty`** - Par défaut, utilise une mise en page vierge pour les pages de catégorie. <br/>**`1 column`**- Par défaut, utilise une mise en page à une seule colonne pour les pages de catégorie.<br/>**`2 columns with left bar`** - Par défaut, utilise une mise en page à deux colonnes avec la barre latérale gauche pour les pages de catégorie. <br/>**`2 columns with right bar`**- Par défaut, utilise une mise en page à deux colonnes avec la barre latérale droite pour les pages de catégorie.<br/>**`3 columns`** - Par défaut, utilise une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages de catégorie.<br/>**`Page - Full Width`**- (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Page - Largeur complète pour les pages de catégorie.<br/>**`Category - Full Width`** - (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Catégorie - Largeur complète pour les pages de catégorie. <br/>**`Product - Full Width`**- (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Produit - Largeur complète pour les pages de catégorie. |
| Disposition de page par défaut | Global | Détermine la [mise en page](../../content-design/page-layout.md) utilisée par défaut pour les pages CMS. Options : <br/>**`No layout updates`**- Par défaut, les mises à jour de mise en page ne sont pas disponibles pour les pages CMS.<br/>**`Empty`** - Par défaut, utilise une mise en page vierge pour les pages CMS. <br/>**`1 column`**- Par défaut, utilise une mise en page à une seule colonne pour les pages CMS.<br/>**`2 columns with left bar`** - Par défaut, utilise une mise en page à deux colonnes avec la barre latérale gauche pour les pages CMS.<br/>**`2 columns with right bar`**- Par défaut, utilise une mise en page à deux colonnes avec la barre latérale droite pour les pages CMS.<br/>**`3 columns`** - Par défaut, utilise une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages CMS.<br/>**`Page - Full Width`**- (Nécessite [!UICONTROL Page Builder]) Par défaut, utilise la disposition Page - Largeur complète pour les pages CMS.<br/>**`Category - Full Width`** - (Nécessite [!UICONTROL Page Builder]) Par défaut, utilise la disposition Catégorie - Largeur complète pour les pages CMS. <br/>**`Product - Full Width`**- (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Produit - Largeur complète pour les pages CMS. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web > Paramètres du cookie par défaut](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Affichage en magasin | Détermine la durée d’existence d’un cookie avant sa suppression automatique. La valeur par défaut est de 3 600 secondes (1 heure) |
| [!UICONTROL Cookie Path] | Affichage en magasin | Spécifie les dossiers sur le serveur où les cookies Commerce peuvent être utilisés. Pour rendre les cookies Commerce disponibles partout dans l’installation, définissez le Chemin du cookie sur une seule barre oblique : `/`. Cette valeur ne peut contenir que le chemin du cookie et **_ne peut pas_** contenir d’autres paramètres de cookie. |
| [!UICONTROL Cookie Domain] | Affichage en magasin | Détermine si les cookies Commerce sont disponibles pour les sous-domaines. Par exemple, pour prendre en charge `mysubdomain`.domain.com, saisissez le nom de votre domaine avec un point au début, comme `.domain.com`. Cette valeur ne peut contenir que le domaine du cookie et **_ne peut pas_** contenir d’autres paramètres de cookie. |
| [!UICONTROL Use HTTP Only] | Affichage en magasin | Détermine si les cookies Commerce peuvent être utilisés uniquement sur un canal non sécurisé (http) ou également sur un canal chiffré (https). Options : `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Site Web | Détermine si le mode de restriction des cookies est activé. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > Validation de session](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Global | Vérifie que l’adresse IP d’une requête correspond aux données `$_SESSION`. La session se termine si une autre adresse IP est détectée. Options : `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Global | Vérifie les données proxy entrantes et vérifie que l’adresse proxy d’une requête correspond aux données `$_SESSION`. La session se termine si une autre adresse proxy est détectée. Options : `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Global | Vérifie les données de proxy sortantes et vérifie que l’adresse de transfert d’une requête correspond aux données `$_SESSION`. La session se termine si une autre adresse de transfert est détectée. Options : `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Global | `USER_AGENT` fait référence au navigateur ou à l’appareil utilisé pour accéder au site web. Il vérifie que le nom et la version du navigateur et du système d’exploitation correspondent aux données `$_SESSION`. La session se termine si un autre agent utilisateur est détecté d’une requête à une autre au cours de la même session. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![ Web > Détection des fonctionnalités de navigateur](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Affichage en magasin | Si les cookies sont désactivés par le navigateur, il est automatiquement redirigé vers la page CMS No Cookies (Aucun cookie). Options : `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Affichage en magasin | Si JavaScript est désactivé par le navigateur, un avis l’invite à activer les options JavaScript : `Yes` / `No` (désactive) s’affiche. |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Affichage en magasin | Affiche un message si le cache local est désactivé. Options : `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
