---
title: Périmètre du compte client
description: L’étendue des comptes clients peut être limitée au site web sur lequel le compte a été créé ou partagée avec tous les sites web et magasins de la hiérarchie du magasin.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/ah5XmCeeX4Kc9czcllRq9zZX4W3rkkqkzcoUXtJjo5I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 0%

---

# Périmètre du compte client

L’en-tête de chaque page de votre boutique envoie une invitation aux acheteurs afin qu’ils _se connecter ou s’enregistrer_ ouvrent un compte dans votre boutique. Les clients qui ouvrent un compte bénéficient d’une série d’avantages, notamment :

* **Créer un compte client** - Les visiteurs peuvent créer un compte client afin de pouvoir utiliser le storefront en tant que client enregistré.
* **Créer un compte d’entreprise** Selon la configuration, un visiteur de votre boutique peut choisir de créer un compte d’entreprise. Pour plus d’informations, voir [Adobe Commerce B2B](../b2b/introduction.md).
* **Passage en caisse plus rapide** — Les clients enregistrés passent en caisse plus rapidement, car une grande partie des informations se trouve déjà dans leur compte.
* **Libre-service** — Les clients enregistrés peuvent mettre à jour leurs informations, vérifier l&#39;état des commandes et même effectuer une nouvelle commande à partir de leurs comptes.

Les clients peuvent accéder à leur compte en cliquant sur le lien **[!UICONTROL My Account]** dans l’en-tête du magasin. À partir de leur compte , les clients peuvent afficher et modifier des informations, notamment les adresses passées et actuelles, les préférences de facturation et d’expédition, les abonnements à des newsletters, des listes de souhaits, etc.

![&#x200B; Mon compte &#x200B;](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Définition de l’étendue des comptes clients

L’étendue des comptes clients peut être limitée au site web sur lequel le compte a été créé ou partagée avec tous les sites web et magasins de la hiérarchie du magasin.

>[!NOTE]
>
>Si le site web est exclu du groupe de clients, le client n’est pas autorisé à se connecter au site web lorsque la portée des comptes clients est limitée au site web ou partagée avec tous les sites web. Voir [Créer un groupe de clients](customer-groups.md#create-a-customer-group) pour plus d’informations sur l’exclusion de sites web des groupes.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Account Sharing Options]** .

   ![Options de partage de compte](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Share Customer Accounts]** sur l’une des options suivantes :

   | Option | Description |
   | --- | --- |
   | `Global` | Partage les informations de compte client avec chaque site web et magasin de l’installation. |
   | `Per Website` | Limite les informations du compte client au site web sur lequel le compte a été créé. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Si nécessaire, décochez la case **[!UICONTROL User system value]** pour apporter la modification.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Lorsque `Global` est sélectionné, les informations du client dans **Mon compte** (adresses et informations de compte telles que les coordonnées) sont partagées.
