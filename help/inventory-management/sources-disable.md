---
title: Désactivation des sources d’inventaire
description: Découvrez comment désactiver les sources et modifier les informations, notamment l’emplacement et le point de contact.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Désactivation des sources

Pour vous assurer que toutes les données de commande sont conservées dans [!DNL Commerce], les sources ne peuvent pas être supprimées. Les sources, commandes et envois sont directement liés les uns aux autres. Vous pouvez désactiver les sources et modifier les informations, notamment l’emplacement et le point de contact.

Selon l’état de vos emplacements, vous pouvez désactiver une source. Une source désactivée conserve toutes les affectations par stocks et produits, mais n’est pas accessible pour les stocks et les commandes.

Lorsqu’une source est désactivée :

- [!DNL Inventory Management] ignore et ne répertorie pas la source pour le traitement de l’envoi ou des commandes.
- Les stocks n’ont pas accès aux quantités d’inventaire de la source pour les totaux d’inventaire agrégés.
- Les envois de commande ne peuvent pas être attribués à des emplacements désactivés.

Vous ne pouvez pas désactiver la source par défaut. [!DNL Commerce] utilise cette source pour tous les nouveaux produits importés, pour les produits en bundle et pour la prise en charge du système tiers. Vous pouvez activer ou désactiver des sources personnalisées à tout moment.

Définir la source sur `disabled` s’avère utile dans les cas suivants :

- Ajout d’un magasin ou d’un entrepôt : lorsque vous ouvrez de nouveaux magasins ou que vous mettez en ligne de nouveaux entrepôts et des emplacements d’expédition, ajoutez une entrée source pour configurer l’inventaire des produits à l’aide de l’importation et connectez-vous aux stocks potentiels.
- Envois saisonniers : les jours fériés peuvent être très chargés. Vous pouvez restreindre l’expédition à des emplacements d’expédition spécifiques, tels que des entrepôts, pour conserver les emplacements en brique et mortier bien approvisionnés et axés sur les acheteurs locaux. Vous pouvez également ajouter de nouveaux emplacements d’expédition pendant une période limitée afin de gérer des taux de ventes plus élevés et des commandes entrantes.
- Fermeture d’un emplacement : lors de la fermeture d’un emplacement pour le déplacement vers de nouvelles installations ou de manière permanente, désactivez cette option pour arrêter de nouveaux envois depuis l’emplacement.

## Désactivation d’une ou de plusieurs sources personnalisées

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Cochez la case pour chaque source personnalisée activée à désactiver.

1. Cliquez sur le bouton _Actions_ dans le coin supérieur gauche et choisissez **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] sources - menu Actions](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL OK]**.

## Activation ou désactivation d’une source personnalisée unique

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Localisez une source personnalisée et cliquez sur **[!UICONTROL Edit]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur _Général_ section et modification **[!UICONTROL Is Enabled]**:

   | Option | Description |
   | ----- | ----- |
   | `Yes` | La source est activée. La quantité s’ajoute à la quantité vendable. Les listes source avec la quantité actuelle lors des commandes d’expédition. L’algorithme de sélection de la source vérifie la source pour l’expédition. |
   | `No` | La source est désactivée. Les quantités ne sont pas ajoutées aux quantités commercialisables. La source ne figure pas dans la liste lors des commandes d’expédition. Les options d’expédition ignorent cette source. |

1. Cliquez sur **[!UICONTROL Save and Close]**.
