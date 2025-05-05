---
title: Clients maintenant en ligne
description: L’option _Maintenant en ligne_ du menu [!UICONTROL Customers &#x200B;] répertorie tous les clients et visiteurs qui sont actuellement en ligne dans votre boutique.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Clients maintenant en ligne

L’option **[!UICONTROL Now Online]** du menu [!DNL Customers] répertorie tous les clients et visiteurs qui sont actuellement en ligne dans votre boutique. L’intervalle de temps pendant lequel les clients sont affichés en ligne est défini dans la configuration et détermine la durée pendant laquelle l’activité [!DNL Customer's] est visible depuis l’administrateur. Par défaut, l’intervalle est de 15 minutes. La session se termine si le clavier n’est pas utilisé pendant cette période et que les clients doivent à nouveau se connecter à leurs comptes pour continuer à effectuer des achats. Il est important de noter que le contenu des paniers est enregistré pour un accès ultérieur.

![Clients en ligne](assets/customers-now-online.png){width="700" zoomable="yes"}

L’état en ligne des clients n’est mis à jour que lors de la connexion, de l’enregistrement ou de tout autre événement de changement d’état du client. Il comprend des événements liés au panier, tels que l’ajout, la suppression et la modification de produits.

>[!NOTE]
>
>Les visites de page seules ne mettent pas à jour l’état en ligne du client. Pour collecter ces informations, il est recommandé de [ configurer des Google Analytics](../merchandising-promotions/google-analytics.md) (seuls ou avec [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) ou d’utiliser d’autres logiciels d’analyse avec Adobe Commerce.

## Afficher tous les clients actuellement en ligne

Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Pour plus d’informations sur l’aide à un client en ligne pour effectuer un achat, voir [Assistance achat](../stores-purchase/introduction.md#shopping-assistance).

## Configuration de l’intervalle

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Online Customers Options]** et procédez comme suit :

   ![Options du client en ligne](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Pour **[!UICONTROL Online Minutes Interval]**, saisissez le nombre de minutes pendant lesquelles la session du client doit être visible depuis l’administrateur. Laissez le champ vide pour accepter l’intervalle par défaut de 15 minutes.

   - Pour **[!UICONTROL Customer Data Lifetime]**, saisissez le nombre de minutes avant l’expiration des données non enregistrées saisies par le client.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Descriptions des colonnes

| Colonne | Description |
| --- | --- |
| **[!UICONTROL ID]** | ID de client d’un client enregistré. |
| **[!UICONTROL First Name]** | Prénom d’un client enregistré. |
| **[!UICONTROL Last Name]** | Nom d’un client enregistré. |
| **[!UICONTROL Email]** | Adresse électronique d’un client enregistré. |
| **[!UICONTROL Last Activity]** | Date et heure de la dernière activité du client dans votre magasin. |
| **[!UICONTROL Type]** | Options : `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | Dernière URL visitée par le client. |
| **[!UICONTROL Company]** | Nom de la société à laquelle appartient l’utilisateur. |

{style="table-layout:auto"}
