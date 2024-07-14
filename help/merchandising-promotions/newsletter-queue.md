---
title: Files d’attente de newsletter
description: Découvrez comment gérer les files d’attente de newsletter pour envoyer plusieurs lots de newsletter.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Files d’attente de newsletter

Pour gérer la charge sur le serveur, les newsletters avec de nombreux abonnés sont envoyées dans une file d’attente de plusieurs lots. Vous pouvez vérifier régulièrement la file d’attente de la newsletter pour vérifier l’état et voir combien d’entre elles ont été traitées. Tous les problèmes qui se produisent pendant la transmission apparaissent sur le rapport _Problème de newsletter_.

## Envoyer une newsletter

1. Dans le menu _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. Dans la grille, recherchez le [modèle de newsletter](newsletter-template.md) à envoyer et définissez la colonne **[!UICONTROL Action]** sur `Queue Newsletter`.

1. Pour **[!UICONTROL Queue Date Start]**, sélectionnez la date de début de la transmission à partir du calendrier (![Icône Calendrier](../assets/icon-calendar.png)).

1. Pour **[!UICONTROL Subscribers From]**, sélectionnez chaque vue de magasin à inclure dans l’explosion de l’email.

1. Renseignez les informations d’en-tête de l’email :

   - Saisissez une brève description de la newsletter pour la ligne **[!UICONTROL Subject]** de l’en-tête de l’email.

   - Saisissez le **[!UICONTROL Sender Name]**.

   - Pour **[!UICONTROL Sender Email]**, saisissez l’adresse email de l’expéditeur.

     Le nom et l&#39;adresse email par défaut de l&#39;expéditeur sont indiqués dans la configuration.

     ![Informations sur la file d’attente de la newsletter](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Le cas échéant, saisissez une note dans la zone **[!UICONTROL Message]** au-dessus des instructions de désabonnement.

   >[!NOTE]
   >
   >Ne supprimez pas les instructions, qui sont requises par la loi dans de nombreuses juridictions.

1. Pour appliquer des styles personnalisés à une newsletter, ajoutez-les dans le champ **[!UICONTROL Newsletter Styles]** .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save and Resume]**.

   La newsletter apparaît dans la file d’attente en attente de traitement.

## Vérifier les problèmes

Dans le menu _Admin_, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Barre de boutons

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Renvoie à la page Modèles de newsletter sans enregistrer les modifications. |
| **[!UICONTROL Reset]** | Réinitialise les modifications non enregistrées du formulaire d’informations sur la file d’attente sur leurs valeurs précédentes. |
| **[!UICONTROL Preview Template]** | Ouvre une page d’aperçu dans un onglet distinct. |
| **[!UICONTROL Save and Resume]** | Enregistre toutes les modifications apportées. Place la newsletter dans la file d’attente. |
| **[!UICONTROL Save Newsletter]** | Enregistre toutes les modifications apportées. Place la newsletter dans la file d’attente. |

{style="table-layout:auto"}

## Colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique attribué à chaque modèle de newsletter. |
| [!UICONTROL Queue Start] | Date à laquelle la newsletter a été envoyée. |
| [!UICONTROL Queue End] | Date à laquelle l’envoi de la newsletter s’est terminé. |
| [!UICONTROL Subject] | Objet du modèle de newsletter. |
| [!UICONTROL Status] | Indique le statut du publipostage à la newsletter. Valeurs possibles : `Sent`, `Canceled`, `Not Sent`, `Sending` ou `Paused`. |
| [!UICONTROL Processed] | Indique le nombre de newsletters envoyées. |
| [!UICONTROL Recipients] | Indique le nombre de newsletters reçues par les abonnés. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]** : ouvre une fenêtre distincte pour prévisualiser le modèle. |

{style="table-layout:auto"}
