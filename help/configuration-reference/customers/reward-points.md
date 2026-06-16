---
title: '[!UICONTROL Customers] > [!UICONTROL Reward Points]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Reward Points] de [!UICONTROL Customers] &gt ; de l’administrateur Commerce.
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
TQID: https://experienceleague.adobe.com/jK-FLPd4mglaptKFOhoRsYtAdwRqStPRWM4zMc48qd4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 779
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>La configuration [Taux de change de récompense](../../merchandising-promotions/reward-exchange-rates.md) est requise pour l’échange de points de récompense par les clients et les administrateurs lors du passage en caisse.

## [!UICONTROL Reward Points]

![&#x200B; Points de récompense &#x200B;](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | Global | Active ou désactive les points de récompense. Options : `Yes` / `No`. |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | Site internet | Lorsqu’ils sont activés, les clients peuvent gagner des points par le biais de leurs activités et les échanger lors du passage en caisse. Si cette option est désactivée, seuls les utilisateurs administrateurs peuvent attribuer et échanger des points au nom des clients. Options : `Yes` / `No`. |
| [!UICONTROL Customers May See Reward Points History] | Site internet | Lorsqu’ils sont activés, les clients peuvent consulter un historique détaillé de chaque acquisition, échange et expiration de points de récompense dans le tableau de bord de leur compte. Options : `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | Site internet | Exige que les clients atteignent un solde minimum de points avant de pouvoir les échanger contre des commandes. Laisser en blanc sans minimum. |
| [!UICONTROL Cap Reward Points Balance At] | Site internet | Empêche les clients d&#39;accumuler plus de ce solde maximal de points. Laisser en blanc pour ne pas avoir de valeur maximale. |
| [!UICONTROL Reward Points Expire in (days)] | Site internet | Indique la durée de vie des points de récompense en jours. Chaque lot de points gagnés au cours d’activités distinctes a une durée de vie distincte. Chaque lot dans l&#39;historique des points de récompense indique le nombre de jours restants avant l&#39;expiration des points. L’historique peut être consulté à partir du tableau de bord du compte du client, si activé, et à partir de l’administrateur. Laissez vide pour éviter toute expiration. |
| [!UICONTROL Reward Points Expiry Calculation] | Site internet | Détermine la méthode utilisée pour déterminer à quel moment les points de récompense expirent. Options : <br/>**`Static`**- Détermine la durée de vie restante des points de récompense en fonction du nombre de jours définis dans la configuration. Si la limite d’expiration dans la configuration change, la date d’expiration des points existants ne change pas.<br/>**`Dynamic`** - Calcule le nombre de jours restants chaque fois que le solde du point de récompense augmente. Si la limite d’expiration dans la configuration change, les calculs d’expiration de tous les points existants sont mis à jour en conséquence. |
| [!UICONTROL Refund Reward Points Automatically] | Global | Détermine si les points de récompense disponibles sont remboursés automatiquement. Options : `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | Global | Lorsque cette fonctionnalité est activée, cela détermine si les points de récompense gagnés lors d’achats sont annulés en tout ou en partie lors du remboursement de la commande. Seuls les points de récompense de la commande qui les a gagnés sont affectés lorsque cette commande est remboursée. Options : `Yes` / `No`. |
| [!UICONTROL Landing Page] | Affichage de la boutique | Spécifie la page CMS qui explique votre programme de points de récompense. Un lien vers la page Récompenses par défaut s’affiche aux emplacements de votre magasin où vous pouvez gagner des points. |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![Actions d’acquisition de points de récompense par les clients](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | Site internet | Détermine si des points de récompense sont gagnés pour les achats en fonction des [taux de change de récompense](../../merchandising-promotions/reward-exchange-rates.md) configurés. Options : `Yes` / `No` |
| [!UICONTROL Registration] | Site internet | Spécifie le nombre de points gagnés pour l&#39;ouverture d&#39;un compte client. |
| [!UICONTROL Newsletter Signup] | Site internet | Indique le nombre de points gagnés par les clients enregistrés qui s’abonnent à une newsletter. (Les points ne sont pas disponibles pour les abonnements des invités.) Si un client se désabonne, puis s’abonne à nouveau, les points ne sont pas gagnés pour le deuxième abonnement. |
| [!UICONTROL Converting Invitation to Customer] | Site internet | Spécifie le nombre de points gagnés par un client qui envoie une invitation, lorsque le destinataire ouvre ensuite un compte client. |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | Site internet | Limite le nombre de conversions d’invitation qui peuvent être utilisées pour gagner des points pour le client qui envoie l’invitation. Laisser vide sans limite. |
| [!UICONTROL Converting Invitation to Order] | Site internet | Spécifie le nombre de points gagnés par un client qui envoie une invitation lorsque le destinataire passe une commande initiale. |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | Site internet | Limite le nombre de conversions de commande pouvant rapporter des points à la personne qui envoie l’invitation. Si rien n’est indiqué, il n’existe aucune limite maximale. |
| [!UICONTROL Invitation Conversion to Order Reward] | Site internet | Indique la fréquence à laquelle un client peut gagner des points de récompense lorsque des invités effectuent des achats. Options : <br/>**`Each`**- Le client reçoit des points de récompense pour chaque commande facturée passée par l&#39;invité. Les points de récompense sont attribués en fonction des taux de change définis pour la combinaison requise entre un site web et un groupe de clients.<br/>**`First`** - Le client ne reçoit des points de récompense que pour la première commande facturée passée par les invités. Si plusieurs invités s&#39;enregistrent et passent une commande, seul le montant de la première commande est converti en points de récompense et accordé au client. |
| [!UICONTROL Review Submission] | Site internet | Détermine le nombre de points gagnés par un client qui soumet une révision dont la publication a été approuvée. |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | Site internet | Limite le nombre d’avis pouvant être utilisés pour gagner des points par client. Laisser vide sans limite. |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![Paramètres de notification par e-mail](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email Sender] | Affichage de la boutique | Détermine le contact du magasin qui apparaît comme l&#39;expéditeur des e-mails de mise à jour de solde et de notification d&#39;expiration. |
| [!UICONTROL Subscribe Customers by Default] | Global | Détermine le statut d&#39;abonnement par défaut des clients pour les e-mails de mise à jour de solde et de notification d&#39;expiration. |
| [!UICONTROL Balance Update Email] | Affichage de la boutique | Détermine le modèle utilisé pour la notification envoyée aux clients chaque fois que leur solde de points est mis à jour. Modèle par défaut : `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | Affichage de la boutique | Détermine le modèle d’e-mail que les clients et clientes reçoivent lorsque la limite d’avertissement d’expiration a été atteinte pour un lot de points. Modèle par défaut : `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | Global | Indique le nombre de jours avant expiration du point pour envoyer la notification. Laissez vide pour n’envoyer aucune notification d’expiration. La notification n’est pas envoyée si le nombre de jours renseignés est supérieur à la durée de vie restante des points. |

{style="table-layout:auto"}
