---
title: Libellés d’expédition
description: Découvrez le workflow des étiquettes d’expédition pour les envois réguliers et les produits avec autorisation de retour de marchandises.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Libellés d’expédition

Commerce comprend un haut niveau d’intégration avec les principaux opérateurs de transport, ce qui vous permet d’accéder aux systèmes d’expédition des opérateurs pour effectuer le suivi des commandes, créer des libellés d’expédition, etc. Des étiquettes d’expédition peuvent être créées pour les envois réguliers et les produits avec autorisation de retour de marchandises. Outre les informations fournies par le transporteur, le libellé inclut également le numéro de commande Commerce, le numéro du package et la quantité totale de packages pour l’expédition.

![Libellé d’expédition prioritaire USPS](./assets/shipping-usps-priority-label.png){width="300"}

- [Configuration des libellés d’expédition](shipping-label-configure.md)
- [Création de libellés et de packages d’expédition](shipping-label-create.md)

## Workflow des libellés d&#39;expédition

Les libellés d’expédition peuvent être produits au moment de la création d’une expédition, ou ultérieurement. Les libellés d’expédition sont stockés au format PDF et téléchargés sur votre ordinateur.

### Étape 1 : le marchand envoie la demande de libellé d&#39;expédition

Le responsable du commerce/magasin complète les informations nécessaires à la génération des étiquettes et envoie la demande.

### Étape 2 : Demande envoyée à l&#39;opérateur

Le commerce contacte l’opérateur de transport et crée une commande dans le système de l’opérateur. Une commande distincte est créée pour chaque module expédié.

### Etape 3 : l&#39;opérateur envoie le libellé et le numéro de tracking

Le transporteur envoie le libellé et le numéro de tracking de l&#39;expédition.

- Une seule expédition avec plusieurs packages reçoit plusieurs libellés d’expédition.

- Si vous générez plusieurs fois les mêmes libellés d’expédition, les numéros de suivi d’origine sont conservés.

- Pour les produits renvoyés avec des numéros RMA, les anciens numéros de suivi sont remplacés par de nouveaux.

### Étape 4 : le marchand télécharge et imprime le libellé

Une fois le libellé d&#39;expédition généré, la nouvelle expédition est enregistrée et le libellé peut être imprimé. Si le libellé d&#39;expédition ne peut pas être créé en raison de problèmes de connexion ou pour toute autre raison, l&#39;envoi n&#39;est pas créé. Selon les paramètres du navigateur, le fichier du PDF peut être ouvert et imprimé. Chaque libellé apparaît sur une page distincte dans le PDF.
