---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL General] d’[!UICONTROL Web] &gt; de l’administrateur Commerce.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Options générales](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Champ | Portée | Description |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Global | Si les réécritures du serveur Web sont activées, insère le code de magasin de l&#39;affichage actuel dans l&#39;URL. Options : `Yes` / `No`. <br />Lorsque ce champ est défini sur `Yes`, vous devez inclure les codes de magasin dans les URL de votre navigateur pour vous assurer que les réécritures d’URL sont correctement mappées et que toutes les pages sont ouvertes avec succès. Cela évite les erreurs _404 Page introuvable_. |
| [!UICONTROL Auto-redirect to Base URL] | Affichage de la boutique | (Pour les configurations à magasin unique) En cas de rupture de lien sur votre site, redirige le trafic vers l’URL de base, plutôt que vers une page contenant un message « Page 404 introuvable ». Options :` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Important:_** N’utilisez pas la redirection automatique vers l’URL de base pour les configurations multi-magasin. |
| [!UICONTROL Catalog media URL format] | Global | Définit le [format d’URL](../../catalog/catalog-urls.md) attribué aux produits et aux catégories. Options : le hachage unique par variante d’image (mode hérité) définit le nom de fichier converti comme une valeur de hachage unique. L’optimisation des images basée sur des paramètres de requête définit le processus [optimisation des images](../../content-design/media-gallery-image-optimization.md) en fonction des paramètres de requête. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web > Optimisation du moteur de recherche](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Affichage de la boutique | Les systèmes PHP incluent généralement un fichier appelé `index.php` dans le dossier racine. Par défaut, le nom du fichier s’affiche dans l’URL juste après le nom du dossier racine. Lorsque cette option est activée, le système omet les `index.php` de l’URL. Cette bonne pratique en matière de convivialité rend chaque URL plus concise et n’a aucun impact sur les performances ou le classement du site. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > URL de base](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Base URL] | Affichage de la boutique | Adresse complète du dossier racine Commerce qui ne s’exécute pas sur un canal chiffré (SSL). L’URL doit se terminer par une barre oblique. |
| [!UICONTROL Base Link URL] | Affichage de la boutique | Balise de mise en forme utilisée comme espace réservé pour l’URL de base. |
| [!UICONTROL Base URL for Static View Files] | Affichage de la boutique | Chemin d’accès qui pointe vers l’emplacement des fichiers statiques utilisés par le thème, tels que les fichiers CSS, les polices, les images et les JavaScript. Un espace réservé est utilisé pour représenter l’URL de base. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier différent pour chaque site. Définissez l’étendue de la configuration sur le site approprié avant de saisir l’URL de base pour les fichiers d’affichage statiques. Vous pouvez également définir un dossier en dehors de votre installation Commerce. |
| [!UICONTROL Base URL for User Media Files] | Affichage de la boutique | Chemin d’accès pointant vers l’emplacement des images de catalogue et d’autres fichiers multimédias. Un espace réservé est utilisé pour représenter l’URL de base. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier de médias différent pour chacun. Vous pouvez ainsi sauvegarder et restaurer chaque dossier de médias séparément. Vous pouvez également définir un dossier de médias en dehors de votre installation Commerce. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > URL de base (sécurisée)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Affichage de la boutique | Adresse complète du dossier racine Commerce fourni avec le protocole chiffré sécurisé (SSL/TLS). L’URL doit se terminer par une barre oblique. |
| [!UICONTROL Secure Base Link URL] | Affichage de la boutique | Balise de mise en forme utilisée comme espace réservé pour l’URL de base qui s’exécute sur un canal sécurisé. |
| [!UICONTROL Secure Base URL for Static View Files] | Affichage de la boutique | Balise de mise en forme qui pointe vers l’emplacement des fichiers statiques tels que les fichiers CSS, les polices, les images et les fichiers JavaScript utilisés par le thème. Les fichiers peuvent se trouver sur un canal non sécurisé ou sécurisé. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier différent pour chaque site. Définissez l’étendue de la configuration sur le site approprié avant de saisir l’URL de base pour les fichiers d’affichage statiques. Vous pouvez également définir un dossier en dehors de votre installation Commerce. |
| [!UICONTROL Secure Base URL for User Media Files] | Affichage de la boutique | Chemin d’accès pointant vers l’emplacement des images de catalogue et d’autres fichiers multimédias. Les fichiers peuvent se trouver sur un canal non sécurisé ou sécurisé. Un espace réservé est utilisé pour représenter l’URL de base. Si votre installation Commerce comporte plusieurs sites avec la même structure de dossiers, vous pouvez avoir un dossier de médias différent pour chacun. Vous pouvez ainsi sauvegarder et restaurer chaque dossier de médias séparément. Vous pouvez également définir un dossier de médias en dehors de votre installation Commerce. |
| [!UICONTROL Use Secure URLs on Storefront] | Affichage de la boutique | Si votre domaine dispose d’un certificat de sécurité, vous pouvez choisir d’exécuter le storefront, avec ou sans chiffrement SSL. Options : <br />**`Yes`**- les URL des magasins commencent par `https` pour indiquer que la page est diffusée avec un protocole chiffré et sécurisé.<br />**`No`** - Les URL des magasins commencent par `http` pour indiquer que la page est diffusée sans protocole sécurisé. |
| [!UICONTROL Use Secure URLs in Admin] | Global | Si votre domaine dispose d’un certificat de sécurité, vous pouvez choisir d’exécuter l’administrateur du magasin, avec ou sans chiffrement SSL. Options : <br />**`Yes`**- Les URL d’administration commencent par `https` pour indiquer que la page est diffusée avec un protocole chiffré et sécurisé.<br />**`No`** - Les URL d’administration commencent par `http` pour indiquer que la page est diffusée sans protocole sécurisé.<br /> Lorsque les URL sécurisées sont activées pour le magasin et l’administrateur, deux champs supplémentaires s’affichent pour activer et configurer `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Affichage de la boutique | Lorsqu’il est activé, [`HSTS`](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html) fournit une mesure de sécurité contre les attaques « d’hommes du milieu » et empêche les utilisateurs de remplacer le message « certificat non valide ». Options : `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Affichage de la boutique | Lorsque cette option est activée, convertit les requêtes non sécurisées (`HTTP`) reçues du navigateur au protocole sécurisé (`HTTPS`). Options : `Yes` / `No` |
| [!UICONTROL Offloader Header] | Global | Indique la valeur `offloader_header` dans la configuration de votre serveur pour identifier le protocole entre le client et la répartition de charge. La plupart des installations Commerce utilisent la valeur par défaut, `X-Forwarded-Proto` (XFP), pour identifier le protocole en tant que `HTTP` ou `HTTPS`. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web > Pages par défaut](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Affichage de la boutique | Indique la page de destination associée à l’URL de base. Cette valeur est définie par défaut sur « cms » pour indiquer une page du système de gestion de contenu Commerce (CMS). Vous pouvez également utiliser un autre type de page de destination, tel qu’un blog. Par exemple, si un blog est installé sur le serveur à l’adresse `magento/blog`, vous pouvez saisir le nom du dossier « blog » comme chemin d’accès relatif à la sélection de pages. |
| [!UICONTROL CMS Home Page] | Affichage de la boutique | Pour choisir la page d’accueil de la boutique, il vous suffit de sélectionner la page CMS dans la liste. Par défaut, la page d’accueil de CMS répertorie l’ensemble de la sélection de pages CMS disponibles pour votre boutique. |
| [!UICONTROL Default No-route URL] | Affichage de la boutique | Contient l’URL de la page par défaut qui doit apparaître lorsqu’une erreur `404 Page not Found` se produit. La valeur par défaut est `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Affichage de la boutique | Indique une page CMS spécifique à afficher lorsqu’une erreur 404 Page introuvable se produit. La page par défaut est 404 Introuvable. |
| [!UICONTROL CMS No Cookies Page] | Affichage de la boutique | Indique une page CMS spécifique qui s’affiche lorsque les cookies ne sont pas activés pour le navigateur. Cette page explique pourquoi les cookies sont utilisés et comment les activer pour chaque navigateur. La page par défaut est Activer les cookies. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Affichage de la boutique | Détermine si un chemin de navigation s’affiche sur toutes les pages CMS du catalogue. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![Dispositions par défaut](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/fr/docs/commerce-admin/content-design/design/layout/page-layout) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Global | Détermine la [mise en page](../../content-design/page-layout.md) utilisée par défaut pour les pages de produits. Options : <br/>**`No layout updates`**- Par défaut, les mises à jour de disposition ne sont pas disponibles pour les pages de produits.<br/>**`Empty`** - Par défaut, utilise une mise en page vierge pour les pages de produits. <br/>**`1 column`**- Par défaut, utilise une disposition sur une seule colonne pour les pages de produits.<br/>**`2 columns with left bar`** - Par défaut, utilise une disposition à deux colonnes avec la barre latérale gauche pour les pages de produits. <br/>**`2 columns with right bar`**- Par défaut, utilise une disposition à deux colonnes avec la barre latérale droite pour les pages de produits.<br/>**`3 columns`** - Par défaut, utilise une disposition à trois colonnes avec des barres latérales à gauche et à droite pour les pages de produits.<br/>**`Page -- Full Width`**- (Nécessite une [!DNL Page Builder]) Par défaut, utilise la disposition Page - Pleine largeur pour les pages de produits.<br/>**`Category - Full Width`** - (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Catégorie - Pleine largeur pour les pages de produits. <br/>**`Product - Full Width`**- (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Produit - Pleine largeur pour les pages de produits. |
| [!UICONTROL Default Category Layout] | Global | Détermine la [disposition](../../content-design/page-layout.md) utilisée par défaut pour les pages de catégories. Options : <br/>**`No layout updates`**- Par défaut, les mises à jour de disposition ne sont pas disponibles pour les pages de catégorie.<br/>**`Empty`** - Par défaut, utilise une mise en page vierge pour les pages de catégorie. <br/>**`1 column`**- Par défaut, utilise une disposition sur une seule colonne pour les pages de catégorie.<br/>**`2 columns with left bar`** - Par défaut, utilise une disposition à deux colonnes avec la barre latérale gauche pour les pages de catégories. <br/>**`2 columns with right bar`**- Par défaut, utilise une disposition à deux colonnes avec la barre latérale droite pour les pages de catégories.<br/>**`3 columns`** - Par défaut, utilise une disposition à trois colonnes avec des barres latérales à gauche et à droite pour les pages de catégories.<br/>**`Page - Full Width`**- (Nécessite une [!DNL Page Builder]) Par défaut, utilise la disposition Page - Pleine largeur pour les pages de catégorie.<br/>**`Category - Full Width`** - (Nécessite une [!DNL Page Builder]) Par défaut, utilise la disposition Catégorie - Pleine largeur pour les pages de catégories. <br/>**`Product - Full Width`**- (Nécessite [!DNL Page Builder]) Par défaut, utilise la disposition Produit - Pleine largeur pour les pages de catégorie. |
| Mise en page par défaut | Global | Détermine la [disposition](../../content-design/page-layout.md) utilisée par défaut pour les pages CMS. Options : <br/>**`No layout updates`**- Par défaut, les mises à jour de disposition ne sont pas disponibles pour les pages CMS.<br/>**`Empty`** - Par défaut, utilise une mise en page vierge pour les pages CMS. <br/>**`1 column`**- Par défaut, utilise une disposition sur une seule colonne pour les pages CMS.<br/>**`2 columns with left bar`** - Par défaut, utilise une disposition à deux colonnes avec la barre latérale gauche pour les pages CMS.<br/>**`2 columns with right bar`**- Par défaut, utilise une disposition à deux colonnes avec la barre latérale droite pour les pages CMS.<br/>**`3 columns`** - Par défaut, utilise une disposition à trois colonnes avec des barres latérales à gauche et à droite pour les pages CMS.<br/>**`Page - Full Width`**- (Nécessite une [!UICONTROL Page Builder]) Par défaut, utilise la disposition Page - Pleine largeur pour les pages CMS.<br/>**`Category - Full Width`** - (Nécessite une [!UICONTROL Page Builder]) Par défaut, utilise la disposition Catégorie - Pleine largeur pour les pages CMS. <br/>**`Product - Full Width`**- (Nécessite une [!DNL Page Builder]) Par défaut, utilise la disposition Produit - Pleine largeur pour les pages CMS. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web > Paramètres de cookie par défaut](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Affichage de la boutique | Détermine la durée d’existence d’un cookie avant sa suppression automatique. La valeur par défaut est de 3 600 secondes (1 heure) |
| [!UICONTROL Cookie Path] | Affichage de la boutique | Indique les dossiers du serveur dans lesquels les cookies Commerce peuvent être utilisés. Pour que les cookies Commerce soient disponibles partout dans l’installation, définissez le Chemin des cookies sur une seule barre oblique : `/`. Cette valeur ne peut contenir que le chemin d’accès au cookie et **_ne peut pas_** aucun autre paramètre de cookie. |
| [!UICONTROL Cookie Domain] | Affichage de la boutique | Détermine si les cookies Commerce sont disponibles pour les sous-domaines. Par exemple, pour prendre en charge `mysubdomain`.domain.com, saisissez le nom de votre domaine avec un point au début, comme `.domain.com`. Cette valeur ne peut contenir que le domaine du cookie et **_ne peut pas_** aucun autre paramètre de cookie. |
| [!UICONTROL Use HTTP Only] | Affichage de la boutique | Détermine si les cookies Commerce peuvent être utilisés uniquement sur un canal non sécurisé (http) ou peuvent également être utilisés sur un canal chiffré (https). Options : `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Site internet | Détermine si le mode de restriction des cookies est activé. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > Validation de session](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Global | Vérifie que l’adresse IP d’une requête correspond aux données `$_SESSION`. La session se termine si une autre adresse IP est détectée. Options : `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Global | Vérifie les données de proxy entrantes et vérifie que l’adresse de proxy d’une requête correspond aux données `$_SESSION`. La session se termine si une autre adresse proxy est détectée. Options : `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Global | Vérifie les données de proxy sortantes et vérifie que l’adresse transférée d’une requête correspond aux données `$_SESSION`. La session se termine si une autre adresse à transférer est détectée. Options : `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Global | `USER_AGENT` fait référence au navigateur ou à l’appareil utilisé pour accéder au site web. Il vérifie que le nom et la version du navigateur et du système d’exploitation correspondent aux données `$_SESSION`. La session s’arrête si un autre agent utilisateur est détecté d’une requête à une autre dans la même session. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web > Détection des fonctionnalités du navigateur](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Affichage de la boutique | Si les cookies sont désactivés par le navigateur, il redirige automatiquement vers la page CMS Aucun cookie . Options : `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Affichage de la boutique | Si JavaScript est désactivé par le navigateur, un avis s’affiche invitant l’utilisateur à activer les options de JavaScript : `Yes` / `No` (désactive) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Affichage de la boutique | Affiche un message si le cache local est désactivé. Options : `Yes` / `No` |

{style="table-layout:auto"}
