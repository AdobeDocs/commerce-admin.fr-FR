---
title: Jeux d’attributs
description: Découvrez comment organiser les attributs en groupes, qui déterminent où ils apparaissent dans l’enregistrement de produit.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 43550b9370f4ed4b631ae7773324ed0913718a79
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Jeux d’attributs

Lors de la création d’un produit, l’une des premières étapes consiste à choisir le jeu d’attributs utilisé comme modèle pour l’enregistrement de produit. Le jeu d’attributs détermine les champs disponibles lors de la saisie des données, ainsi que les valeurs qui s’affichent pour le client.

Les attributs sont organisés en groupes qui déterminent où ils apparaissent dans l’enregistrement de produit. Votre magasin est fourni avec un jeu d’attributs initial (appelé _default_) qui comprend un ensemble d’attributs couramment utilisés. Si vous souhaitez n’ajouter que quelques attributs, vous pouvez les ajouter à ce jeu d’attributs par défaut. Si vous vendez des produits qui nécessitent des types d’informations spécifiques, il peut être préférable de créer un ensemble d’attributs dédié qui inclut les attributs spécifiques nécessaires au produit.

![Visionneuses d’attributs](./assets/attribute-sets.png){width="700" zoomable="yes"}

## Création d’un jeu d’attributs

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Cliquez sur **[!UICONTROL Add New Set]**.

   ![Ensemble d’attributs - nom de modification](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. Saisissez un **[!UICONTROL Name]** pour le jeu d’attributs.

1. Définissez **[!UICONTROL Based On]** sur un jeu d’attributs existant à utiliser comme modèle.

1. Cliquez sur **[!UICONTROL Save]**.

   La page suivante affiche les informations suivantes :

   - La colonne de gauche affiche le nom du jeu d’attributs. Le nom est à titre de référence interne et peut être modifié si nécessaire.
   - Le centre de la page répertorie la sélection actuelle des groupes d’attributs.
   - La colonne de droite répertorie la sélection des attributs qui ne sont actuellement pas affectés au jeu d’attributs.

1. Pour ajouter un attribut à l’ensemble, faites glisser l’attribut de la liste **[!UICONTROL Unassigned Attributes]** vers le dossier approprié dans la colonne **[!UICONTROL Groups]**. Pour supprimer un attribut de l’ensemble, faites-le glisser vers la liste **[!UICONTROL Unassigned Attributes]**.

   >[!NOTE]
   >
   >Les attributs système sont marqués par un point et ne peuvent pas être supprimés de la liste _[!UICONTROL Groups]_. Ils peuvent toutefois être déplacés vers un autre groupe du jeu d’attributs.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

![Ensemble d’attributs - edit](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## Création d’un groupe d’attributs

1. Dans la colonne _[!UICONTROL Groups]_&#x200B;du jeu d’attributs, cliquez sur **[!UICONTROL Add New]**.

1. Saisissez un **[!UICONTROL Name]** pour le nouveau groupe, puis cliquez sur **[!UICONTROL OK]**.

1. Effectuez l’une des opérations suivantes :

   - Faites glisser **[!UICONTROL Unassigned Attributes]** vers le nouveau groupe.
   - Faites glisser les attributs de n’importe quel autre groupe vers le nouveau groupe.
   - Faites glisser des attributs inutiles vers **[!UICONTROL Unassigned Attributes]**.

   Le nouveau groupe devient une section d’attributs dans n’importe quel produit basé sur le jeu d’attributs.

## Suppression d’un jeu d’attributs

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Sélectionnez l’ensemble d’attributs dans la liste et ouvrez-le en mode d’édition.

1. Cliquez sur **[!UICONTROL Delete]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.
