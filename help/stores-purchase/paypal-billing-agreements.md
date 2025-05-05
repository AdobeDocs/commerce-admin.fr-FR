---
title: Contrats de facturation PayPal
description: Découvrez comment vous pouvez prendre en charge les contrats de facturation PayPal et un mode de paiement dans votre boutique.
exl-id: b0800b41-816a-4c48-a54d-41ddc1d586ce
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Contrats de facturation PayPal

Pour simplifier le processus de passage en caisse, les clients peuvent conclure un contrat de facturation avec PayPal en tant que fournisseur de services de paiement. Lors du passage en caisse, le client choisit le contrat de facturation comme mode de paiement. Le système de paiement vérifie le contrat de facturation par son numéro unique et charge le compte du client. Une fois un contrat de facturation en place, il n’est plus nécessaire pour le client de saisir les informations de paiement pour chaque achat. Les clients peuvent gérer leurs contrats de facturation à partir du tableau de bord de leur compte client, où l’état de chacun est affiché comme _Actif_ ou _Annulé_. Lorsqu&#39;un contrat de facturation est annulé, il ne peut pas être réactivé.

## Workflow de contrat de facturation

1. **Le client s&#39;inscrit à un contrat de facturation**. Une fois un contrat de facturation en place, d’autres contrats de facturation ne peuvent être ajoutés qu’à partir du compte client. Le nombre de contrats de facturation qu’un client peut créer n’est pas limité. Les clients peuvent utiliser l’une des méthodes suivantes pour souscrire à des contrats de facturation :

   - **S’abonner à un compte client** - Les clients peuvent s’abonner à un contrat de facturation à partir de leurs comptes clients.
   - **S’inscrire au paiement** - Les clients qui paient un achat avec le paiement express PayPal peuvent cocher une case pour créer un contrat de facturation. Bien que le contrat de facturation ne soit pas utilisé pour la commande actuelle, il devient disponible comme option de paiement la prochaine fois que le client passe une commande.
   - **S’inscrire par l’administrateur de magasin** - Sur demande du client, l’administrateur de magasin peut créer une commande client à l’aide du contrat de facturation client.

1. **PayPal vérifie et enregistre le contrat**. Lorsque le client passe la commande avec paiement par contrat de facturation, l’ID de référence du contrat de facturation et les détails du paiement de la commande client sont transférés à PayPal et enregistrés dans le compte client, avec les informations de référence. Si le paiement est autorisé, une commande est créée dans Commerce. L’ID de référence du contrat de facturation est envoyé au client et au magasin.

## Gestion des contrats de facturation

La page _[!UICONTROL Billing Agreements]_&#x200B;répertorie tous les contrats de facturation entre votre boutique et ses clients. Les commerçants peuvent filtrer les enregistrements par client ou par informations de contrat de facturation, y compris l’ID de référence du contrat de facturation, l’état et la date de création. Chaque enregistrement contient des informations générales sur le contrat de facturation, ainsi que toutes les commandes client qui l’ont utilisé comme mode de paiement. Vous pouvez afficher, annuler ou supprimer des contrats de facturation client. Un contrat de facturation annulé ne peut être supprimé que par l’administrateur du magasin.

### Afficher un contrat de facturation

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Recherchez le contrat de facturation dans la liste et cliquez pour l&#39;ouvrir.

Chaque page du contrat de facturation se compose de deux onglets : _[!UICONTROL General Information]_&#x200B;et&#x200B;_[!UICONTROL Related Orders]_.

#### Informations générales

Cet onglet contient les informations générales relatives au contrat de facturation :

- [!UICONTROL Reference ID] : identifiant numérique unique attribué au contrat de facturation actuel.
- [!UICONTROL Customer] : compte du client affecté au contrat de facturation actuel.
- [!UICONTROL Status] : statut du contrat de paiement.
- [!UICONTROL Created At] : Date de création.
- [!UICONTROL Updated At] : date de mise à jour.

![Vue du contrat de facturation](./assets/billing-agreement-view.png){width="600" zoomable="yes"}

#### Commandes connexes

Cet onglet affiche la liste des commandes passées avec le contrat de facturation actuel.

![Vue du contrat de facturation](./assets/billing-agreement-related-orders.png){width="600" zoomable="yes"}

### Annulation d’un contrat de facturation

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Recherchez le contrat de facturation dans la liste et cliquez pour l&#39;ouvrir.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Cancel]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Suppression d’un contrat de facturation

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Recherchez le contrat de facturation dans la liste et cliquez pour l&#39;ouvrir.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique attribué à chaque contrat de facturation |
| [!UICONTROL Email] | Adresse électronique de contact d’un client |
| [!UICONTROL First Name] | Prénom d’un client |
| [!UICONTROL Last Name] | Nom du client |
| [!UICONTROL Reference ID] | Identifiant de référence numérique unique attribué à chaque contrat de facturation |
| [!UICONTROL Status] | Statut du contrat de paiement. Options : `Active` ou `Canceled` |
| [!UICONTROL Created] | Date de création |
| [!UICONTROL Updated] | Mettre à jour la date |

{style="table-layout:auto"}

## Expérience Storefront

Les clients qui concluent un contrat de facturation avec un fournisseur de services de paiement peuvent effectuer des achats maintenant et les payer ultérieurement, conformément à l&#39;accord. La variable

![Liste des contrats de facturation dans le tableau de bord du client](./assets/billing-agreements-dashboard.png){width="700" zoomable="yes"}

| Colonne | Description |
|--- |--- |
| [!UICONTROL Reference ID] | Identifiant de référence numérique unique attribué à chaque contrat de facturation |
| [!UICONTROL Status] | Statut du contrat de paiement. Options : `Active` ou `Canceled` |
| [!UICONTROL Created At] | Date de création |
| [!UICONTROL Updated At] | Mettre à jour la date |
| [!UICONTROL Payment Method] | Fournisseur de paiement d’un contrat de facturation |
| [!UICONTROL View] | Bouton utilisé pour visualiser les contrats de facturation |

{style="table-layout:auto"}

### Créer un contrat de facturation

1. Dans le tableau de bord de leur compte, le client sélectionne **[!UICONTROL Billing Agreements]**.

1. Sous **[!UICONTROL New Billing Agreement]**, sélectionne un fournisseur de paiement.

1. Cliquez sur **[!UICONTROL Create]**.

Cette action redirige le client vers le site web du système de paiement.

![Nouvel accord de facturation dans le tableau de bord du compte client](./assets/create-billing-agreement-dashboard.png){width="700" zoomable="yes"}

### Afficher un contrat de facturation

1. Dans le tableau de bord de leur compte, le client sélectionne **[!UICONTROL Billing Agreements]**.

1. Sélectionne le contrat de facturation et clique sur **[!UICONTROL View]**.

![Afficher le contrat de facturation dans le tableau de bord du client](./assets/view-billing-agreement.png){width="700" zoomable="yes"}

### Annulation d’un contrat de facturation

1. Dans le tableau de bord de leur compte, le client sélectionne **[!UICONTROL Billing Agreements]**.

1. Sélectionne le contrat de facturation et clique sur **[!UICONTROL View]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Cancel]**, puis sur **[!UICONTROL OK]** pour confirmer.

>[!NOTE]
>
>Si un utilisateur administrateur (commerçant) annule le contrat de facturation, il ne peut pas être annulé sur le storefront. L’état _Annulé_ s’affiche pour cet accord.
