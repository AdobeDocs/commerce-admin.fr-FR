---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL General] &gt; [!UICONTROL General] de l’administrateur Commerce.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Voir [Options de pays](../../getting-started/store-details.md#country-options) pour plus d’informations sur ces champs et options de configuration.

![Général > Options de pays](./assets/general-country-options.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Default Country] | Affichage en magasin | Le pays où se trouve votre magasin. |
| [!UICONTROL Allow Countries] | Site Web | Les pays dans lesquels vous acceptez les commandes. |
| [!UICONTROL Zip/Postal Code is Optional for] | Global | Les pays qui n’ont pas besoin d’un code postal dans l’adresse d’expédition. |
| [!UICONTROL European Union Countries] | Global | Les pays qui sont membres de l’Union européenne. |
| [!UICONTROL Top Destinations] | Affichage en magasin | Les pays principaux que vous ciblez pour les ventes. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL State Options]

Voir [Options d’état](../../getting-started/store-details.md#state-options) pour plus d’informations sur ces champs et options de configuration.

![Général > Options d’état](./assets/general-state-options.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL State is required for] | Global | Les pays (où vous effectuez des activités) qui exigent qu’une région ou un état soit inclus dans l’adresse postale. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Global | Pour les pays où elle n’est pas requise, détermine si la variable _Région/état_ est inclus dans l’adresse postale du client.<br /> <br />**`Yes`**- Inclut la variable _Région/état_ dans l’adresse du client, même s’il n’est pas requis par le pays.<br />**`No`** : omet le champ Région/état de l’adresse du client si le pays ne l’exige pas. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Locale Options]

Voir [Options de paramètres régionaux](../../getting-started/store-details.md#locale-options) pour plus d’informations sur ces champs et options de configuration.

![Général > Options de paramètres régionaux](./assets/general-locale-options.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Timezone] | Site Web | Fuseau horaire du marché principal diffusé par le site web. En règle générale, le fuseau horaire est le même que celui utilisé dans l’emplacement physique de votre entreprise. |
| [!UICONTROL Locale] | Affichage en magasin | Langue, devise et système de mesure utilisés dans le marché fourni par la vue de magasin. |
| [!UICONTROL Weight Unit] | Affichage en magasin | Unité de mesure généralement utilisée pour les envois à partir des paramètres régionaux. Options : `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Affichage en magasin | Jour considéré comme étant le premier de la semaine dans le marché servi par la vue du magasin. |
| [!UICONTROL Weekend Days] | Affichage en magasin | Jours qui se produisent le week-end sur le marché servi par la vue du magasin. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![Général > Restrictions du site Web](./assets/general-website-restrictions.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Restrictions d’accès](../../merchandising-promotions/event-configure.md#access-restrictions) dans le _Guide de marchandisage et de promotions_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Site Web | Détermine si le site web fonctionne en mode restreint.<br /> <br />**`Yes`**- L&#39;accès au site web est restreint de la manière définie dans les champs ci-dessous.<br />**`No`** - Les restrictions sont désactivées et les paramètres suivants n’ont aucun effet. |
| [!UICONTROL Restriction Mode] | Site Web | Détermine le type de restriction d’accès qui s’applique au site web.<br /> <br />**`Website Closed`**- Tout accès au storefront est restreint et les URL du storefront sont temporairement redirigées vers la landing page. Ce paramètre peut s’avérer utile pendant la maintenance du site ou avant le lancement.<br />**`Private Sales: Login Only`** - Seuls les clients enregistrés peuvent se connecter pour accéder au storefront. Toutes les URL de storefront sont temporairement redirigées vers la landing page ou le formulaire de connexion spécifié. Les utilisateurs ne peuvent pas créer de compte dans ce mode.<br />**`Private Sales: Login and Register`**- Les utilisateurs doivent se connecter pour accéder au storefront. Toutes les URL de storefront sont temporairement redirigées vers le formulaire de connexion jusqu’à ce que l’utilisateur se connecte. Les utilisateurs peuvent s’inscrire à un compte lorsque le site est dans ce mode. |
| [!UICONTROL Startup Page] | Affichage en magasin | Lorsque le site web est en mode Ventes privées, ce paramètre détermine la page qui s’affiche jusqu’à ce que le client se connecte.<br />  <br />**`To login form`**- Les utilisateurs sont redirigés vers le formulaire de connexion jusqu’à ce qu’ils se connectent.<br />**`To landing page`** - Les utilisateurs sont redirigés vers la page statique spécifiée ci-dessous jusqu’à ce qu’ils se connectent.<br /> <br />**_Important !_**Veillez à inclure un lien vers la page de connexion à partir de la page d’entrée spécifiée afin que les clients puissent se connecter pour accéder au site complet. |
| [!UICONTROL Landing Page] | Affichage en magasin | Détermine la première page qui s’affiche lorsque le site web est en mode Ventes privées. |
| [!UICONTROL HTTP Response] | Site Web | Détermine la réponse HTTP envoyée lorsque le site web est fermé et qu’une connexion est tentée par un robot, un robot d’indexation ou un robot d’indexation.<br /> <br />**`503 Service unavailable`**- La page n’est pas disponible, mais l’araignée ne doit pas mettre à jour l’index.<br />**`200 OK`** - La page d’entrée est correcte et doit être traitée par l’araignée comme la seule page du site. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Site Web | Détermine si les champs de la variable _Connexion_ et _Mot de passe oublié_ les formulaires sont remplis automatiquement à partir des entrées précédentes. Options : `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Information]

![Général > Informations sur le magasin](./assets/general-store-information.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Informations sur le magasin](../../getting-started/store-details.md) dans le _Guide de démarrage_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Store Name] | Affichage en magasin | Nom du magasin associé à la vue de magasin. |
| [!UICONTROL Store Phone Number] | Affichage en magasin | Le numéro de téléphone principal du magasin (associé à la vue du magasin) est ouvert pour l’entreprise. Par exemple : Lun - Fri, 9-5, Sat 9-Midi PST |
| Pays | Site Web | Pays de l’entreprise qui gère le site web. |
| [!UICONTROL Region/State] | Site Web | Région ou état de l’entreprise qui gère le site web. |
| [!UICONTROL ZIP/Postal Code] | Site Web | Code postal de l’entreprise qui gère le site web. |
| [!UICONTROL City] | Site Web | Ville de l’entreprise qui gère le site web. |
| [!UICONTROL Street Address] | Site Web | Adresse postale ou de la rue de l’entreprise qui gère le site Web. |
| [!UICONTROL Street Address Line 2|]Site Web | La deuxième ligne de l’adresse postale, si nécessaire. |
| [!UICONTROL VAT Number] | Site Web | Numéro de taxe sur la valeur ajoutée de l’entreprise propriétaire de l’installation Commerce, le cas échéant. |
| [!UICONTROL Validate VAT Number] |  | Vérifie le numéro d’identification Taxe sur la valeur ajoutée. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Single-Store Mode]

![Général > Mode Boutique unique](./assets/general-single-store-mode.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Mode Boutique unique](../../getting-started/websites-stores-views.md#single-store-mode) dans le _Guide de démarrage_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Global | Lorsqu’elle est activée pour les installations à un seul magasin, la configuration Masque la zone d’étendue et les libellés de champ associés Options : `Yes` / `No` <br/>**_Remarque :_**Le mode Boutique unique est ignoré pour les magasins avec plusieurs vues. |

{:style=&quot;table-layout:auto&quot;}
