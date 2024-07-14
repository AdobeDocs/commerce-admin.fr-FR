---
title: Portée du compte client
description: La portée des comptes clients peut être limitée au site web sur lequel le compte a été créé ou partagé avec tous les sites web et magasins de la hiérarchie de magasin.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Portée du compte client

L’en-tête de chaque page de votre boutique étend une invitation pour les acheteurs à _Se connecter ou s’inscrire_ pour un compte avec votre boutique. Les clients qui ouvrent un compte bénéficient de nombreux avantages, notamment :

* **Créer un compte client** - Les visiteurs peuvent créer un compte client afin d’utiliser le storefront comme client enregistré.
* **Créer un compte d’entreprise** Selon la configuration, un visiteur de votre boutique peut choisir de créer un compte d’entreprise. Pour plus d’informations, voir [Adobe Commerce B2B](../b2b/introduction.md).
* **Passage en caisse plus rapide** : les clients enregistrés passent plus rapidement en caisse car la plupart des informations se trouvent déjà dans leurs comptes.
* **Self-service** - Les clients enregistrés peuvent mettre à jour leurs informations, vérifier l’état des commandes et même réorganiser leurs commandes à partir de leurs comptes.

Les clients peuvent accéder à leur compte en cliquant sur le lien **[!UICONTROL My Account]** dans l’en-tête du magasin. À partir de leur compte, les clients peuvent afficher et modifier des informations, notamment les adresses passées et actuelles, les préférences de facturation et d’expédition, les abonnements à des newsletters, des listes de souhaits, etc.

![Mon compte](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Définition de la portée des comptes clients

La portée des comptes clients peut être limitée au site web sur lequel le compte a été créé ou partagé avec tous les sites web et magasins de la hiérarchie de magasin.

>[!NOTE]
>
>Si le site web est exclu du groupe de clients, le client n’est pas autorisé à se connecter au site web lorsque la portée des comptes de clients est limitée au site web ou partagée avec tous les sites web. Voir [Création d’un groupe de clients](customer-groups.md#create-a-customer-group) pour plus d’informations sur l’exclusion de sites web des groupes.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Account Sharing Options]** .

   ![Options de partage de compte](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Share Customer Accounts]** sur l’une des options suivantes :

   | Option | Description |
   | --- | --- |
   | `Global` | Partage les informations du compte client avec chaque site web et magasin de l’installation. |
   | `Per Website` | Limite les informations du compte client au site web sur lequel le compte a été créé. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Si nécessaire, décochez la case **[!UICONTROL User system value]** pour apporter la modification.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Lorsque `Global` est sélectionné, les informations sur les clients de **Mon compte** (adresses et informations de compte telles que les coordonnées) sont partagées.
