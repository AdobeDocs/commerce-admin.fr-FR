---
title: Référence des attributs de données client
description: Utilisez cette référence d’attributs de données client lorsque vous utilisez des imports et des exports de données client.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Référence des attributs de données client

Les tableaux suivants répertorient les attributs d’une exportation standard du fichier principal et des adresses des clients. L’installation utilisée pour exporter ces données comporte deux sites web et plusieurs vues de magasin, avec les exemples de données installés.

Chaque attribut, ou champ, est représenté dans le fichier CSV sous la forme d’une colonne et les enregistrements des clients sont représentés par des lignes. Les colonnes qui commencent par un trait de soulignement sont des entités de service qui contiennent des propriétés ou des données complexes.

## Fichier principal des clients

| Attribut | Description |
|--- |--- |
| `email` | Adresse e-mail du client. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Indicateur de confirmation. |
| `created_at` | Date de création du compte client. |
| `created_in` | Vue du magasin dans lequel le compte a été créé. |
| `disable_auto_group_change` | Détermine si les groupes de clients peuvent être affectés dynamiquement pendant la validation du numéro de TVA. |
| `dob` | Date de naissance du client. <br><br>**_Important:_** conformément aux bonnes pratiques actuelles en matière de sécurité et de confidentialité, révisez le stockage et le traitement de la date de naissance complète des clients (mois, jour, année). Lorsqu’elles sont collectées avec d’autres identifiants personnels (tels que _nom complet_), il s’agit d’un risque potentiel pour la sécurité et la légalité. Nous recommandons de limiter le stockage des dates de naissance complètes des clients et suggérons plutôt d’utiliser l’année de naissance du client comme alternative. |
| `firstname` | Prénom du client. |
| `gender` | Sexe du client. |
| `group_id` | ID du groupe de clients auquel le client est affecté. |
| `lastname` | Nom du client. |
| `middlename` | Deuxième prénom ou deuxième initiale du client. |
| `password_hash` | Hachage du mot de passe |
| `prefix` | Tout préfixe utilisé avec le nom du client (par exemple `Mr.`, `Ms.`, `Mrs.` et `Dr.`). |
| `rp_token` | Réinitialiser le jeton de mot de passe. |
| `rp_token_created_at` | Date de réinitialisation du mot de passe. |
| `store_id` | ID de magasin |
| `suffix` | Tout suffixe utilisé avec le nom du client (par exemple `Jr.`, `Sr.` et `Esquire`). |
| `taxvat` |  |
| `website_id` | Identifiant du site web sur lequel le compte client a été créé. |
| `password` | Mot de passe du client. |

{style="table-layout:auto"}

## Adresses des clients

| Attribut | Description |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | Ville où se trouve l’adresse du client. |
| `company` | Nom de la société, le cas échéant, pour cette adresse. |
| `country_id` | Identifiant du pays où se trouve l’adresse du client. |
| `fax` | Numéro de fax du client, le cas échéant. |
| `firstname` | Prénom du client. |
| `lastname` | Nom du client. |
| `middlename` | Deuxième prénom ou deuxième initiale du client. |
| `postcode` | Code postal de l’adresse du client. |
| `prefix` | Tout préfixe utilisé avec le nom du client (par exemple `Mr.`, `Ms.`, `Mrs.` et `Dr.`). |
| `region` | Région dans laquelle se trouve l’adresse du client. |
| `region_id` | ID de région |
| `street` | Adresse postale du client. Une deuxième ligne de l’adresse postale est disponible si elle est spécifiée dans la configuration. |
| `suffix` | S’il est utilisé, le suffixe associé au nom du client (par exemple `Jr.`, `Sr.` ou `III`). |
| `telephone` | Numéro de téléphone du client associé à l’adresse. |
| `vat_id` | Le numéro de TVA est un identifiant interne du numéro de TVA du client lorsqu&#39;il est utilisé dans la validation de la TVA. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Identifie l’adresse de facturation par défaut. Une valeur `1` indique que l’adresse est l’adresse de facturation par défaut du client. Valeurs : 1 / 0 |
| `_address_default_shipping_` | Indique l’adresse de livraison par défaut. Une valeur `1` indique que l’adresse est l’adresse de livraison par défaut du client. Valeurs : `1` / `0` |

{style="table-layout:auto"}
