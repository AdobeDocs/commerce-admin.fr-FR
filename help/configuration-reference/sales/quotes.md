---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Quotes] de [!UICONTROL Sales] &gt ; de l’administrateur Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Avec l’installation et l’activation d’Adobe Commerce B2B, l’expérience d’achat peut être personnalisée avec des fonctionnalités spécifiques à l’entreprise. Adobe Commerce B2B est une solution intégrée qui prend en charge les modèles B2B et B2C. Pour plus d’informations sur les fonctionnalités B2B, consultez le [Guide de l’utilisateur Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![Général](./assets/quotes-general.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Site internet | Montant minimal du sous-total du panier, après toutes les remises, qui est requis avant qu’un client puisse soumettre une demande de devis. Valeur par défaut : `0` |
| [!UICONTROL Minimum Amount Message] | Affichage de la boutique | Message qui apparaît dans le panier lorsqu’un client tente de soumettre une demande de devis, mais que le montant minimum requis n’est pas atteint. |
| [!UICONTROL Default Expiration Period] | Site internet | Détermine la durée de vie par défaut d&#39;un [devis](../../b2b/quote-price-negotiation.md) comme période à partir de la date d&#39;envoi de la demande de devis. Options : `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Fichiers joints](./assets/quotes-attached-files.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Détermine les formats de fichier pouvant être joints à une citation. Valeurs par défaut prises en charge : `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` et `jpeg` |
| [!UICONTROL Maximum file size] | Global | Détermine la taille maximale d&#39;un fichier joint à une citation. Ce paramètre peut être remplacé par la configuration du serveur. |

{style="table-layout:auto"}
