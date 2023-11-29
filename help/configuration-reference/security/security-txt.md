---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Security] &gt; [!UICONTROL Security.txt] de l’administrateur Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Pour plus d’informations sur la modification de ces paramètres de configuration, voir [Rapports sur les problèmes de sécurité](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Général](./assets/txt-general.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Site Web | Lorsqu’elle est activée, une `security.txt` est enregistré et contient les informations dont les chercheurs en sécurité ont besoin pour vous signaler des vulnérabilités potentielles. Options :<br />**`Yes`**- Crée la variable `security.txt` en fonction des informations saisies dans le fichier _Coordonnées_ et _Autres informations_ sections.<br />**`No`** - (valeur par défaut) Ne crée pas la variable `security.txt` fichier . |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Coordonnées](./assets/txt-contact-info.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email] | Site Web | Adresse électronique à laquelle les rapports de sécurité peuvent être envoyés. |
| [!UICONTROL Phone] | Site Web | Numéro de téléphone qui peut être utilisé pour signaler les problèmes de sécurité. |
| [!UICONTROL Contact Page] | Site Web | L’URL d’une page de votre site qui répertorie les contacts de sécurité, ou _Nous contacter_ page. Exemples: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Autres informations](./assets/txt-other-info.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Encryption] | Site Web | URL pointant vers l’emplacement d’une clé de chiffrement que les chercheurs en sécurité peuvent utiliser pour envoyer des communications chiffrées. _**Ne saisissez pas la clé de chiffrement dans ce champ.**_ <br/><br/>Il est de la responsabilité du chercheur de vérifier que la clé provient d&#39;une source fiable. Les chercheurs ne doivent pas présumer que la clé est la même que celle utilisée pour générer la signature numérique. Exemple :<br />Clé OpenPGP du serveur web - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Site Web | Une URL qui pointe vers une page de votre magasin où les chercheurs en sécurité sont reconnus, par exemple`https://mystore.com/hall-of-fame.html`. Pour éviter de futures attaques, incluez uniquement une description générale sans révéler d’informations spécifiques sur les problèmes de vulnérabilité. Exemple :<br />Nous tenons à remercier les chercheurs suivants :<br />(aaaa/mm/jj) Justin Thyme - injection SQL |
| [!UICONTROL Preferred Languages] | Site Web | Spécifie au moins une langue de reporting de sécurité préférée. Séparez plusieurs caractères à deux caractères [codes langue](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) par une virgule. Toutes les langues spécifiées ont la même priorité. Par exemple, pour indiquer l’anglais, l’espagnol et le français, saisissez `en, es, fr`. |
| [!UICONTROL Hiring] | Site Web | URL d’une page du site qui répertorie les postes de travail liés à la sécurité. Exemple : `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Site Web | URL de la page qui décrit votre politique de sécurité et vos pratiques de reporting des vulnérabilités. Exemple : `https://mystore.com/security-reporting.html` Valeur par défaut : `https://mystore.com/security` |
| [!UICONTROL Signature] | Site Web | Un lien vers votre fichier de signature numérique. La signature numérique doit être générée à partir de la ligne de commande et est enregistrée dans le `.well-known` sur le serveur. Pour plus d’informations, voir [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) sur GitHub. Exemple : `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
