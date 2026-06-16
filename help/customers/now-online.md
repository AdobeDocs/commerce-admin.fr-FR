---
title: Clients désormais en ligne
description: L’option _Maintenant en ligne_ du menu [!UICONTROL Customers &#x200B;] répertorie tous les clients et visiteurs qui sont actuellement en ligne dans votre boutique.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
TQID: https://experienceleague.adobe.com/jtyDgy3jFmn0XymAYcpc2AOLLWSTDw-3OGkvG9a1SDc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 342
ht-degree: 1%

---

# Clients désormais en ligne

L’option **[!UICONTROL Now Online]** du menu [!DNL Customers] répertorie tous les clients et visiteurs qui sont actuellement en ligne dans votre boutique. L’intervalle de temps pendant lequel les clients et clientes sont actuellement en ligne est défini dans la configuration et détermine la durée pendant laquelle l’activité de [!DNL Customer's] est visible depuis l’administration. Par défaut, l’intervalle est de 15 minutes. La session se termine si le clavier n’est pas utilisé pendant cette période et les clients doivent se reconnecter à leur compte pour continuer leurs achats. Il est important de noter que le contenu des paniers est enregistré pour un accès ultérieur.

![Clients en ligne](assets/customers-now-online.png){width="700" zoomable="yes"}

Le statut en ligne des clients est mis à jour uniquement lors de la connexion, de l’enregistrement du client ou de tout autre événement modifiant le statut. Il inclut des événements liés au panier, tels que l’ajout, la suppression et la modification de produits.

>[!NOTE]
>
>Les visites de page seules ne mettent pas à jour le statut en ligne du client. Pour collecter ces informations, il est recommandé de [configurer Google Analytics](../merchandising-promotions/google-analytics.md) (seul ou avec [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) ou d’utiliser d’autres logiciels d’analyse avec Adobe Commerce.

## Consulter tous les clients actuellement en ligne

Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Pour plus d’informations sur l’aide apportée à un client en ligne pour finaliser un achat, voir [Aide au shopping](../stores-purchase/introduction.md#shopping-assistance).

## Configuration de l’intervalle de temps

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Online Customers Options]** et procédez comme suit :

   ![Options du client en ligne](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Par **[!UICONTROL Online Minutes Interval]**, saisissez le nombre de minutes pendant lesquelles la session client doit être visible par l’administrateur. Laissez le champ vide pour accepter l’intervalle par défaut de 15 minutes.

   - Par **[!UICONTROL Customer Data Lifetime]**, saisissez le nombre de minutes avant l’expiration de toutes les données non enregistrées saisies par le client.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Descriptions des colonnes

| Colonne | Description |
| --- | --- |
| **[!UICONTROL ID]** | ID de client d’un client enregistré. |
| **[!UICONTROL First Name]** | Prénom d’un client enregistré. |
| **[!UICONTROL Last Name]** | Nom d’un client enregistré. |
| **[!UICONTROL Email]** | Adresse e-mail d’un client enregistré. |
| **[!UICONTROL Last Activity]** | Date et heure de la dernière activité du client dans votre boutique. |
| **[!UICONTROL Type]** | Options : `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | Dernière URL visitée par le client ou la cliente. |
| **[!UICONTROL Company]** | Nom de la société à laquelle l’utilisateur appartient. |

{style="table-layout:auto"}
