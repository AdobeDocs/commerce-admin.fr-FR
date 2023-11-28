---
title: Taux de change des primes
description: Découvrez comment configurer les taux de change de récompense qui déterminent le nombre de points de récompense gagnés.
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Taux de change des primes

{{ee-feature}}

Les taux de change déterminent le nombre de points gagnés en fonction du montant de la commande et de la valeur des points gagnés. Différents taux de change peuvent être appliqués à différents sites web et différents groupes de clients. Si plusieurs taux de change de différents sites web et groupes de clients s’appliquent au même client, les règles de priorité suivantes s’appliquent :

## Priorité des taux de change

**1**: s’applique à un site web spécifique et à un groupe de clients spécifique.

**2**: s’applique à tous les sites web et à un groupe de clients spécifique.

**3**: s’applique à un site web spécifique et à tous les groupes de clients.

**4**: s’applique à tous les sites web et à tous les groupes de clients.

Lors de la conversion d’une devise en points, le nombre de points ne peut pas être divisé. Tout reste de devise est arrondi. Par exemple, si 2,00 $ convertit en dix points, les points sont gagnés par groupes de 2,00 $. Par conséquent, une commande de 7,00 $ rapporterait 30 points, et les 1,00 $ restants seraient réduits. Le montant monétaire de la commande est défini comme le montant que le marchand reçoit, ou le total général moins les frais d’expédition, de taxe, de remises, le crédit de magasin et les cartes-cadeaux. Les points sont gagnés au moment où il n’y a pas d’articles non facturés dans la commande (tous les articles sont payés ou annulés). Si un utilisateur administrateur ne souhaite pas autoriser les clients à gagner des points de récompense pour les commandes annulées, ces points peuvent être déduits manuellement de la page Gérer les clients .

## Configurer les taux de change

![Taux de change des primes](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Rate]**.

1. Dans le **[!UICONTROL Reward Exchange Rate Information]** , procédez comme suit :

   ![Taux de change des primes - information](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Website]** aux sites où s&#39;applique le taux de change de la récompense.

   - Définir **[!UICONTROL Customer Group]** aux groupes auxquels s&#39;applique le taux de change des récompenses.

   - Définir **[!UICONTROL Direction]** à l’une des options suivantes :

      - `Points to Currency`
      - `Currency to Points`

   Pour les paramètres Direction , le montant est représenté dans la devise de base du site web.

1. Saisissez le **[!UICONTROL Rate]** en fonction des _[!UICONTROL Direction]_.

   | Direction | Paramètres de taux |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | Dans la première _[!UICONTROL Rate]_, saisissez le nombre de points. Dans la seconde_[!UICONTROL Rate]_ , saisissez la valeur monétaire des points. |
   | [!UICONTROL Currency to Points] | Dans la première  _[!UICONTROL Rate]_, saisissez la valeur monétaire. Dans la seconde_[!UICONTROL Rate]_ , saisissez le nombre de points représentés par la valeur monétaire. |

   Lors de la conversion de points en devise, le nombre de points ne peut pas être divisé. Par exemple, si dix points sont convertis à 2,00 $, les points doivent être échangés en groupes de dix. Par conséquent, 25 points seraient remboursés pour 4,00 $, et 5 points resteraient dans le solde du client.

   Il est recommandé de configurer une conversion pour les deux `Points to Currency` et `Currency to Points`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Supprimer un taux de change de récompense

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Recherchez le taux de change de récompense à supprimer et ouvrez-le en mode édition.

1. Dans la barre de menus, cliquez sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Website] | Les sites web sur lesquels s&#39;appliquent les taux de récompense. |
| [!UICONTROL Customer Group] | Les groupes de clients auxquels s&#39;appliquent les taux de récompense. |
| [!UICONTROL Direction] | Détermine le type de transaction que le taux de change définit. Options : <br/>**[!UICONTROL Points to Currency]**- Définit le nombre de points pouvant être appliqués comme crédit au montant d’une commande. Dans la première _[!UICONTROL Rate]_, saisissez le nombre de points. Dans la seconde_[!UICONTROL Rate]_ , saisissez la valeur monétaire des points.<br/>**[!UICONTROL Currency to Points]** - Définit le montant d’une commande qui peut gagner des points du client. Dans la première  _[!UICONTROL Rate]_, saisissez la valeur monétaire. Dans la seconde_[!UICONTROL Rate]_ , saisissez le nombre de points représentés par la valeur monétaire. |
