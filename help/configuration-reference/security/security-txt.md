---
title: '[!UICONTROL Security] > [!UICONTROL Security.txt]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Security.txt] de [!UICONTROL Security] &gt ; de l’administrateur Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
TQID: https://experienceleague.adobe.com/fXStEab1k6GKC5Tj7CStSGou3uNB-wJk5rZ-7EiFkcg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Pour plus d’informations sur la modification de ces paramètres de configuration, voir [Signalement des problèmes de sécurité](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Général](./assets/txt-general.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Site internet | Une fois activé, un fichier `security.txt` contenant les informations nécessaires aux chercheurs en sécurité est enregistré afin de vous signaler les vulnérabilités potentielles. Options : <br />**`Yes`**- Crée le fichier `security.txt` en fonction des informations saisies dans les sections _Coordonnées_ et _Autres informations_.<br />**`No`** - (par défaut) Ne crée pas le fichier `security.txt`. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Coordonnées](./assets/txt-contact-info.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email] | Site internet | Adresse e-mail à laquelle les rapports de sécurité peuvent être envoyés. |
| [!UICONTROL Phone] | Site internet | Numéro de téléphone qui peut être utilisé pour signaler des problèmes de sécurité. |
| [!UICONTROL Contact Page] | Site internet | URL d’une page de votre site qui répertorie les contacts de sécurité, ou de votre page _Nous contacter_. Exemples : <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Autres informations](./assets/txt-other-info.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Encryption] | Site internet | Une URL qui pointe vers l&#39;emplacement d&#39;une clé de chiffrement que les chercheurs en sécurité peuvent utiliser pour envoyer des communications chiffrées. _&#x200B;**Ne saisissez pas la clé de chiffrement dans ce champ.**&#x200B;_ <br/><br/>Il incombe au chercheur de vérifier que la clé provient d&#39;une source digne de confiance. Les chercheurs ne doivent pas supposer que la clé est la même que celle utilisée pour générer la signature numérique. Exemple :<br />Clé OpenPGP du serveur web - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Site internet | Une URL qui pointe vers une page de votre magasin où les chercheurs en sécurité sont reconnus, telle que `https://mystore.com/hall-of-fame.html`. Pour éviter de futures attaques, incluez uniquement une description générale sans révéler d’informations spécifiques sur les problèmes de vulnérabilité. Exemple : <br />Nous remercions les chercheurs suivants :<br />(aaaa/mm/jj) Justin Thyme - injection SQL |
| [!UICONTROL Preferred Languages] | Site internet | Spécifie au moins un langage de rapport de sécurité préféré. Séparez les différents [codes de langue](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) de deux caractères par une virgule. Toutes les langues spécifiées ont la même priorité. Par exemple, pour spécifier l’anglais, l’espagnol et le français, saisissez `en, es, fr`. |
| [!UICONTROL Hiring] | Site internet | URL d’une page du site répertoriant les postes liés à la sécurité. Exemple : `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Site internet | URL de la page qui décrit votre politique de sécurité et vos pratiques de création de rapports de vulnérabilité. Exemple : `https://mystore.com/security-reporting.html` Valeur par défaut : `https://mystore.com/security` |
| [!UICONTROL Signature] | Site internet | Un lien vers votre fichier de signature numérique. La signature numérique doit être générée à partir de la ligne de commande et est enregistrée dans le dossier `.well-known` sur le serveur. Pour plus d’informations, voir [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) sur GitHub. Exemple : `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
