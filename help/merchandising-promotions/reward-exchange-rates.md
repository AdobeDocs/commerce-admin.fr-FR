---
title: Taux de change de récompense
description: Découvrez comment configurer les taux de change de récompense qui déterminent le nombre de points de récompense gagnés.
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
TQID: https://experienceleague.adobe.com/Iwr92ju0R1z6DFP-5n4O4bqIBYnYWtdn18ImbHJhoHU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 571
ht-degree: 0%

---

# Taux de change de récompense

{{ee-feature}}

Les taux de change de récompense déterminent le nombre de points gagnés en fonction du montant de la commande et de la valeur des points gagnés. Différents taux de change peuvent être appliqués à différents sites web et groupes de clients. Si plusieurs taux de change de différents sites web et groupes de clients s’appliquent au même client, les règles de priorité suivantes s’appliquent :

## Priorité taux de change

**1** : s’applique à un site web et à un groupe de clients spécifiques.

**2** : s’applique à tous les sites web et à un groupe de clients spécifique.

**3** : s’applique à un site web spécifique et à tous les groupes de clients.

**4** : s’applique à tous les sites web et groupes de clients.

Lors de la conversion d&#39;une devise en points, le nombre de points ne peut pas être divisé. Le reste de la devise est arrondi à l’unité inférieure. Par exemple, si 2,00 $ sont convertis en dix points, les points sont gagnés par groupes de 2,00 $. Par conséquent, une commande de 7 $ rapporterait 30 points et les 1 $ restants seraient arrondis à la baisse. Le montant monétaire de la commande est défini comme le montant que le marchand reçoit, ou le total général moins les frais d’expédition, les taxes, les remises, le crédit du magasin et les cartes-cadeaux. Les points sont gagnés au moment où il n&#39;y a aucun article non facturé dans la commande (tous les articles sont payés ou annulés). Si un utilisateur administrateur ne souhaite pas permettre aux clients d’accumuler des points de récompense pour les commandes annulées, ces points peuvent être déduits manuellement à partir de la page Gérer les clients .

## Configurer des taux de change

![Taux de change de récompense](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Rate]**.

1. Dans la section **[!UICONTROL Reward Exchange Rate Information]**, procédez comme suit :

   ![Taux de change de récompense - informations](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Website]** sur les sites où le taux de change de récompense s&#39;applique.

   - **[!UICONTROL Customer Group]** aux groupes auxquels s&#39;applique le taux de change de la récompense.

   - Définissez **[!UICONTROL Direction]** sur l’une des options suivantes :

      - `Points to Currency`
      - `Currency to Points`

   Pour l’un ou l’autre de ces paramètres, le montant est représenté dans la devise de base du site web.

1. Saisissez les valeurs **[!UICONTROL Rate]** en fonction du paramètre _[!UICONTROL Direction]_.

   | Direction | Paramètres des taux |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | Dans le premier champ de _[!UICONTROL Rate]_, saisissez le nombre de points. Dans le deuxième champ&#x200B;_[!UICONTROL Rate]_, entrez la valeur monétaire des points. |
   | [!UICONTROL Currency to Points] | Dans le premier champ _[!UICONTROL Rate]_, saisissez la valeur monétaire. Dans le deuxième champ de&#x200B;_[!UICONTROL Rate]_, saisissez le nombre de points représenté par la valeur monétaire. |

   Lors de la conversion de points en devise, le nombre de points ne peut pas être divisé. Par exemple, si dix points sont convertis en $2,00, les points doivent être échangés par groupes de dix. Par conséquent, 25 points seraient remboursés pour 4,00 $, avec 5 points restants dans le solde du client.

   Il est recommandé de configurer une conversion pour `Points to Currency` et `Currency to Points`.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

## Supprimer un taux de change de récompense

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Recherchez le taux de change de récompense à supprimer et ouvrez-le en mode d’édition.

1. Dans la barre de menus, cliquez sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Website] | Sites web sur lesquels les taux de récompense s’appliquent. |
| [!UICONTROL Customer Group] | Groupes de clients auxquels s’appliquent les taux de récompense. |
| [!UICONTROL Direction] | Détermine le type de transaction défini par le taux de change. Options : <br/>**[!UICONTROL Points to Currency]**- Définit le nombre de points pouvant être crédités sur le montant d’une commande. Dans le premier champ de _[!UICONTROL Rate]_, saisissez le nombre de points. Dans le deuxième champ&#x200B;_[!UICONTROL Rate]_, entrez la valeur monétaire des points.<br/>**[!UICONTROL Currency to Points]** - Définit le montant d’une commande qui peut rapporter des points client. Dans le premier champ _[!UICONTROL Rate]_, saisissez la valeur monétaire. Dans le deuxième champ de&#x200B;_[!UICONTROL Rate]_, saisissez le nombre de points représenté par la valeur monétaire. |
