---
title: Référence des attributs de données client
description: Utilisez cette référence d’attributs de données client lorsque vous utilisez des exportations et des importations de données client.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Référence des attributs de données client

Les tableaux suivants répertorient les attributs d’une exportation type du fichier principal des clients et des adresses de clients. L’installation qui a été utilisée pour exporter ces données comporte deux sites web et plusieurs vues de magasin, avec les exemples de données installés.

Chaque attribut, ou champ, est représenté dans le fichier CSV sous la forme d’une colonne et les enregistrements de client sont représentés par des lignes. Les colonnes qui commencent par un trait de soulignement sont des entités de service qui contiennent des propriétés ou des données complexes.

## Fichier principal des clients

| Attribut | Description |
|--- |--- |
| `email` | Adresse électronique du client. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Indicateur de confirmation. |
| `created_at` | Date de création du compte client. |
| `created_in` | Vue du magasin dans lequel le compte a été créé. |
| `disable_auto_group_change` | Détermine si des groupes de clients peuvent être affectés de manière dynamique lors de la validation de l’ID de TVA. |
| `dob` | Date de naissance du client. <br><br>**_Important :_**&#x200B;Conformément aux bonnes pratiques actuelles en matière de sécurité et de confidentialité, passez en revue le stockage et le traitement de la date de naissance complète des clients (mois, jour, année). Lorsqu&#39;elle est collectée avec d&#39;autres identifiants personnels (tels que_nom complet _), elle présente un risque potentiel d&#39;ordre juridique et de sécurité. Nous vous recommandons de limiter le stockage des dates de naissance complètes des clients et de plutôt proposer d’utiliser l’année de naissance du client comme alternative. |
| `firstname` | Prénom du client. |
| `gender` | Genre du client. |
| `group_id` | Identifiant du groupe de clients auquel le client est affecté. |
| `lastname` | Nom du client. |
| `middlename` | Nom intermédiaire ou initial intermédiaire du client. |
| `password_hash` | Hachage de mot de passe |
| `prefix` | Tout préfixe utilisé avec le nom du client (par exemple `Mr.`, `Ms.`, `Mrs.` et `Dr.`). |
| `rp_token` | Réinitialisez le jeton de mot de passe. |
| `rp_token_created_at` | Date à laquelle le mot de passe a été réinitialisé. |
| `store_id` | Identifiant de magasin |
| `suffix` | Tout suffixe utilisé avec le nom du client (par exemple `Jr.`, `Sr.` et `Esquire`). |
| `taxvat` |  |
| `website_id` | Identifiant du site web sur lequel le compte du client a été créé. |
| `password` | Mot de passe du client. |

{style="table-layout:auto"}

## Adresses clients

| Attribut | Description |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | Ville où se trouve l’adresse du client. |
| `company` | Nom de la société, le cas échéant pour cette adresse. |
| `country_id` | Identifiant du pays où se trouve l’adresse du client. |
| `fax` | Le numéro de fax du client, le cas échéant. |
| `firstname` | Prénom du client. |
| `lastname` | Nom du client. |
| `middlename` | Nom intermédiaire ou initial intermédiaire du client. |
| `postcode` | Code postal où se trouve l’adresse du client. |
| `prefix` | Tout préfixe utilisé avec le nom du client (par exemple `Mr.`, `Ms.`, `Mrs.` et `Dr.`). |
| `region` | La région où se trouve l’adresse du client. |
| `region_id` | Identifiant de région |
| `street` | Adresse postale du client. Une deuxième ligne de l’adresse postale est disponible si la configuration l’indique. |
| `suffix` | Si utilisé, le suffixe associé au nom du client (par exemple `Jr.`, `Sr.` ou `III`). |
| `telephone` | Numéro de téléphone du client associé à l’adresse. |
| `vat_id` | L’identifiant TVA est un identifiant interne du numéro de TVA du client lorsqu’il est utilisé dans la validation de la TVA. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Identifie l’adresse de facturation par défaut. La valeur `1` indique que l’adresse est l’adresse de facturation par défaut du client. Valeurs : 1 / 0 |
| `_address_default_shipping_` | Identifie l’adresse de livraison par défaut. La valeur `1` indique que l’adresse est l’adresse de livraison par défaut du client. Valeurs : `1` / `0` |

{style="table-layout:auto"}
