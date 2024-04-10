---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Examinez les paramètres de configuration sur le [!UICONTROL General] &gt; [!UICONTROL General] de l’Administration de Commerce.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 17006d71d73329abcf7c7d34a0b699172d645fa1
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Voir [Options du pays](../../getting-started/store-details.md#country-options) pour plus d’informations sur ces champs et options de configuration.

![Général > Options du pays](./assets/general-country-options.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Default Country] | Affichage de la boutique | Pays dans lequel se trouve votre magasin. |
| [!UICONTROL Allow Countries] | Site internet | Pays dans lesquels vous acceptez les commandes. |
| [!UICONTROL Zip/Postal Code is Optional for] | Global | Pays pour lesquels l&#39;adresse d&#39;expédition ne doit pas comporter de code postal. |
| [!UICONTROL European Union Countries] | Global | Pays membres de l&#39;Union européenne. |
| [!UICONTROL Top Destinations] | Affichage de la boutique | Pays principaux ciblés pour les ventes. |

{style="table-layout:auto"}

## [!UICONTROL State Options]

Voir [Options d’état](../../getting-started/store-details.md#state-options) pour plus d’informations sur ces champs et options de configuration.

![Général > Options d’état](./assets/general-state-options.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL State is required for] | Global | Pays (où vous exercez votre activité) pour lesquels une région ou un État doit être inclus dans l’adresse postale. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Global | Pour les pays où cela n’est pas nécessaire, détermine si les _Région/État_ Le champ est inclus dans l’adresse postale du client.<br /> <br />**`Yes`**- Inclut le _Région/État_ champ de l’adresse du client, même si le pays ne l’exige pas.<br />**`No`** - Omet le champ Région/État de l’adresse du client si le pays ne l’exige pas. |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

Voir [Options de paramètres régionaux](../../getting-started/store-details.md#locale-options) pour plus d’informations sur ces champs et options de configuration.

![Général > Options de paramètres régionaux](./assets/general-locale-options.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Timezone] | Site internet | Fuseau horaire du marché principal qui est desservi par le site web. Généralement, le fuseau horaire est le même que celui utilisé dans l&#39;emplacement physique de votre entreprise. |
| [!UICONTROL Locale] | Affichage de la boutique | Langue, devise et système de mesure utilisés dans le marché desservi par la vue du magasin. |
| [!UICONTROL Weight Unit] | Affichage de la boutique | Unité de mesure généralement utilisée pour les expéditions à partir du paramètre régional. Options : `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Affichage de la boutique | Jour considéré comme le premier jour de la semaine dans le marché desservi par la vue du magasin. |
| [!UICONTROL Weekend Days] | Affichage de la boutique | Les jours qui tombent le week-end au marché servis par la vue du magasin. |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![Général > Restrictions du site web](./assets/general-website-restrictions.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Restrictions d’accès](../../merchandising-promotions/event-configure.md#access-restrictions) dans le _Guide de merchandising et de promotion_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Site internet | Détermine si le site web fonctionne en mode restreint.<br /> <br />**`Yes`**- L&#39;accès au site Web est restreint de la manière indiquée dans les champs ci-dessous.<br />**`No`** - Les restrictions sont désactivées et les paramètres suivants n’ont aucun effet. |
| [!UICONTROL Restriction Mode] | Site internet | Détermine le type de restriction d’accès qui s’applique au site Web.<br /> <br />**`Website Closed`**- L’accès au storefront est limité et les URL de storefront sont temporairement redirigées vers la page de destination. Ce paramètre peut s’avérer utile pendant la maintenance du site ou avant le lancement.<br />**`Private Sales: Login Only`** - Seuls les clients enregistrés peuvent se connecter pour accéder au storefront. Toutes les URL de storefront sont temporairement redirigées vers la page de destination ou le formulaire de connexion spécifié. Les utilisateurs ne peuvent pas créer de compte dans ce mode.<br />**`Private Sales: Login and Register`**- Les utilisateurs doivent se connecter pour accéder au storefront. Toutes les URL de storefront sont temporairement redirigées vers le formulaire de connexion jusqu’à ce que l’utilisateur se connecte. Les utilisateurs peuvent créer un compte lorsque le site est en mode . |
| [!UICONTROL Startup Page] | Affichage de la boutique | Lorsque le site web est en mode Ventes privées, ce paramètre détermine la page qui s’affiche jusqu’à ce que le client se connecte.<br />  <br />**`To login form`**- Les utilisateurs sont redirigés vers le formulaire de connexion jusqu’à leur connexion.<br />**`To landing page`** - Les utilisateurs sont redirigés vers la page statique spécifiée ci-dessous jusqu’à leur connexion.<br /> <br />**_Important !_**Veillez à inclure un lien vers la page de connexion à partir de la page de destination spécifiée afin que les clients puissent se connecter pour accéder au site complet. |
| [!UICONTROL Landing Page] | Affichage de la boutique | Détermine la première page qui s&#39;affiche lorsque le site Web est en mode Ventes privées. |
| [!UICONTROL HTTP Response] | Site internet | Détermine la réponse HTTP envoyée lorsque le site Web est fermé et qu’un robot, un robot ou une araignée tente de se connecter.<br /> <br />**`503 Service unavailable`**- La page n’est pas disponible, mais l’indexation ne doit pas être mise à jour.<br />**`200 OK`** - La page de destination est correcte et doit être traitée par l’araignée comme la seule page du site. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Site internet | Détermine si les champs sur le _Login_ et _Mot de passe oublié_ les formulaires sont remplis automatiquement à partir des entrées précédentes. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![Général > Informations sur la boutique](./assets/general-store-information.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Informations sur la boutique](../../getting-started/store-details.md) dans le _Guide de prise en main_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Store Name] | Affichage de la boutique | Nom du magasin associé à l’affichage du magasin. |
| [!UICONTROL Store Phone Number] | Affichage de la boutique | Le numéro de téléphone principal du magasin (associé à l’affichage du magasin) est ouvert pour les affaires. Par exemple : lundi au vendredi, 9-5, samedi 9-midi (heure du Pacifique) |
| Pays | Site internet | Pays de l’entreprise qui exploite le site web. |
| [!UICONTROL Region/State] | Site internet | Région ou état de l’entreprise qui exploite le site web. |
| [!UICONTROL ZIP/Postal Code] | Site internet | Code postal de l’entreprise qui exploite le site web. |
| [!UICONTROL City] | Site internet | Ville où se trouve l’entreprise qui exploite le site web. |
| [!UICONTROL Street Address] | Site internet | Rue ou adresse postale de l’entreprise qui exploite le site web. |
| [!UICONTROL Street Address Line 2|]Site internet | Deuxième ligne de l’adresse de la rue d’affaires, si nécessaire. |
| [!UICONTROL VAT Number] | Site internet | Numéro de taxe sur la valeur ajoutée de l’entreprise propriétaire de l’installation de Commerce, le cas échéant. |
| [!UICONTROL Validate VAT Number] |  | Vérifie le numéro d&#39;identification TVA. |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![Général > Mode Magasin unique](./assets/general-single-store-mode.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Mode magasin unique](../../getting-started/websites-stores-views.md#single-store-mode) dans le _Guide de prise en main_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Global | Lorsqu’elle est activée pour les installations à magasin unique, masque la zone Portée de la configuration et les libellés de champ associés. Options : `Yes` / `No` <br/>**_Remarque :_**Le mode de magasin unique est ignoré pour les magasins avec plusieurs vues.<br/> L’activation du mode de magasin unique copie toutes les données spécifiques au catalogue et à l’entrepôt de produits de la vue d’entrepôt par défaut vers la portée de la vue d’entrepôt. Il ne copie les données de catalogue et de produit que si le magasin ne dispose que d’un seul magasin. Si le magasin comporte une vitrine désactivée et une vitrine activée, il ne copiera pas les données du catalogue et des produits.<br/> L’activation du mode de magasin unique ignore les paramètres de configuration spécifiques au magasin pour les données spécifiques au contenu. Il utilise plutôt les paramètres de configuration définis au niveau global pour assurer la cohérence entre l’interface utilisateur d’administration et le storefront. |

{style="table-layout:auto"}
