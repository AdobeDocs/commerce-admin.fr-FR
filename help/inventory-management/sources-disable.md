---
title: Désactiver les sources d’inventaire
description: Découvrez comment désactiver les sources et modifier les informations, y compris l’emplacement et le point de contact.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
TQID: https://experienceleague.adobe.com/l-S7b-E9rREgJ4AX5Zd6nneSDJe-OioeD-vk8YeSAak
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 406
ht-degree: 0%

---

# Désactiver les sources

Pour que toutes les données de commande soient conservées dans [!DNL Commerce], les sources ne peuvent pas être supprimées. Les sources, les commandes et les expéditions sont directement liées les unes aux autres. Vous pouvez désactiver les sources et modifier les informations, y compris l’emplacement et le point de contact.

Selon le statut de vos emplacements, vous pouvez désactiver une source. Une origine désactivée conserve toutes les affectations par stock et produit, mais n&#39;est pas accessible pour les stocks et les commandes.

Lorsqu’une source est désactivée :

- [!DNL Inventory Management] ignore et ne répertorie pas la source pour l&#39;expédition ou le traitement des commandes.
- Les stocks n&#39;accèdent pas aux quantités en stock de la source pour les totaux de stock agrégés.
- Les expéditions de commande ne peuvent pas être affectées à des emplacements désactivés.

Vous ne pouvez pas désactiver le Source par défaut. [!DNL Commerce] utilise cette source pour tous les nouveaux produits importés, pour les produits groupés et pour la prise en charge des systèmes tiers. Vous pouvez activer ou désactiver les sources personnalisées à tout moment.

La définition d’une source sur `disabled` est utile dans les cas suivants :

- Ajout d’un magasin ou d’un entrepôt - Lorsque vous ouvrez de nouveaux magasins ou mettez en ligne de nouveaux entrepôts et emplacements d’expédition, ajoutez une entrée source pour configurer le stock de produits à l’aide de l’importation et vous connecter aux stocks potentiels.
- Envois saisonniers - Les vacances peuvent être une période chargée de l&#39;année. Vous pouvez limiter l’expédition à partir d’emplacements d’expédition spécifiques, tels que des entrepôts, afin de conserver des emplacements physiques bien approvisionnés et de vous concentrer sur les acheteurs locaux. Vous pouvez également ajouter de nouveaux lieux d&#39;expédition pour une durée limitée afin de gérer des taux de ventes et de commandes entrantes plus élevés.
- Fermeture d&#39;un lieu - Lorsque vous fermez un lieu pour vous déplacer vers de nouvelles installations ou de façon permanente, désactivez cette option pour arrêter les nouvelles expéditions à partir de l&#39;endroit.

## Désactiver une ou plusieurs sources personnalisées

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Cochez la case de chaque source personnalisée activée que vous souhaitez désactiver.

1. Cliquez sur le menu _Actions_ dans le coin supérieur gauche et choisissez **[!UICONTROL Disable]**.

   Sources de ![[!DNL Inventory Management] - Menu Actions &#x200B;](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL OK]**.

## Activer ou désactiver une source personnalisée unique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Recherchez une source personnalisée et cliquez sur **[!UICONTROL Edit]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section _Général_ et modifiez les **[!UICONTROL Is Enabled]** :

   | Option | Description |
   | ----- | ----- |
   | `Yes` | Source est activé. La quantité s&#39;ajoute à la quantité commercialisable. L&#39;origine répertorie la quantité actuelle lors des commandes d&#39;expédition. L’algorithme de sélection Source vérifie la source pour l’expédition. |
   | `No` | Source est désactivé. Les quantités ne sont pas ajoutées aux quantités commercialisables. L&#39;origine ne s&#39;affiche pas lors de l&#39;expédition des commandes. Les options d’expédition ignorent cette source. |

1. Cliquez sur **[!UICONTROL Save and Close]**.
