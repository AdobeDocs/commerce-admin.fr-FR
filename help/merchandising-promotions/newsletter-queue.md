---
title: Files d’attente des newsletters
description: Découvrez comment gérer les files d’attente des newsletters pour envoyer plusieurs lots de newsletter.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Files d’attente des newsletters

Pour gérer la charge sur le serveur, les newsletters contenant de nombreux abonnés sont envoyées dans une file d’attente de plusieurs lots. Vous pouvez vérifier régulièrement la file d’attente de la newsletter pour connaître son statut et savoir combien de demandes ont été traitées. Tous les problèmes qui surviennent lors de la transmission apparaissent dans le rapport _Problème de newsletter_.

## Envoyer une newsletter

1. Dans le menu _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. Dans la grille, recherchez le [modèle de newsletter](newsletter-template.md) à envoyer et définissez la colonne **[!UICONTROL Action]** sur `Queue Newsletter`.

1. Par **[!UICONTROL Queue Date Start]**, sélectionnez la date à laquelle la transmission doit commencer dans le calendrier (![icône Calendrier](../assets/icon-calendar.png)).

1. Par **[!UICONTROL Subscribers From]**, sélectionnez chaque vue de magasin à inclure dans l’envoi massif d’e-mails.

1. Renseignez les informations d’en-tête de l’e-mail :

   - Saisissez une brève description de la newsletter pour la ligne **[!UICONTROL Subject]** de l’en-tête de l’e-mail.

   - Saisissez le **[!UICONTROL Sender Name]**.

   - Par **[!UICONTROL Sender Email]**, saisissez l’adresse e-mail de l’expéditeur.

     Le nom et l’adresse e-mail par défaut de l’expéditeur sont spécifiés dans la configuration.

     ![Informations sur la file d’attente de la newsletter](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Le cas échéant, saisissez une note dans la zone de **[!UICONTROL Message]** située au-dessus des instructions de désabonnement.

   >[!NOTE]
   >
   >Ne supprimez pas les instructions, qui sont requises par la loi dans de nombreuses juridictions.

1. Pour appliquer des styles personnalisés à une newsletter, ajoutez-les dans le champ **[!UICONTROL Newsletter Styles]** .

1. Cliquez ensuite sur **[!UICONTROL Save and Resume]**.

   La newsletter apparaît dans la file d’attente en attente de traitement.

## Rechercher les problèmes

Dans le menu _Admin_, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Barre de boutons

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Retourne à la page Modèles de newsletter sans enregistrer les modifications. |
| **[!UICONTROL Reset]** | Rétablit les valeurs précédentes des modifications non enregistrées dans le formulaire d’informations de file d’attente. |
| **[!UICONTROL Preview Template]** | Ouvre une page d’aperçu dans un onglet distinct. |
| **[!UICONTROL Save and Resume]** | Enregistre toutes les modifications effectuées. Met la newsletter en file d’attente. |
| **[!UICONTROL Save Newsletter]** | Enregistre toutes les modifications effectuées. Met la newsletter en file d’attente. |

{style="table-layout:auto"}

## Colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique attribué à chaque modèle de newsletter. |
| [!UICONTROL Queue Start] | Date d’envoi de la newsletter. |
| [!UICONTROL Queue End] | Date à laquelle la newsletter a fini d’être envoyée. |
| [!UICONTROL Subject] | Objet du modèle de newsletter. |
| [!UICONTROL Status] | Indique le statut du publipostage de la newsletter. Valeurs possibles : `Sent`, `Canceled`, `Not Sent`, `Sending` ou `Paused`. |
| [!UICONTROL Processed] | Indique le nombre de newsletters envoyées. |
| [!UICONTROL Recipients] | Indique le nombre de newsletters reçues par les abonnés. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]** : ouvre une fenêtre distincte pour prévisualiser le modèle. |

{style="table-layout:auto"}
