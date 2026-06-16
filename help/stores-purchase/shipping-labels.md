---
title: Étiquettes d’expédition
description: Découvrez le workflow d’étiquette d’expédition pour les expéditions standard et les produits avec autorisation de retour de marchandise.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
TQID: https://experienceleague.adobe.com/Cjf9-372TRGIfWXpWR20OUII5XorPdfO1qgG-b2yPYI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# Étiquettes d’expédition

Commerce comprend un haut niveau d’intégration avec les principaux transporteurs, ce qui vous donne accès aux systèmes d’expédition des transporteurs pour effectuer le suivi des commandes, créer des étiquettes d’expédition, etc. Des étiquettes d&#39;expédition peuvent être créées pour les expéditions régulières et les produits avec une autorisation de retour de marchandise. En plus des informations fournies par le transporteur, l&#39;étiquette comprend également le numéro de commande Commerce, le numéro du colis et la quantité totale de colis pour l&#39;expédition.

![étiquette d&#39;expédition prioritaire USPS](./assets/shipping-usps-priority-label.png){width="300"}

- [Configurer les étiquettes d&#39;expédition](shipping-label-configure.md)
- [Créer des étiquettes et des colis d&#39;expédition](shipping-label-create.md)

## Workflow d’étiquette d’expédition

Les étiquettes d&#39;expédition peuvent être produites au moment de la création d&#39;une expédition ou plus tard. Les étiquettes d&#39;expédition sont stockées au format PDF et sont téléchargées sur votre ordinateur.

### Étape 1 : le marchand soumet la demande d&#39;étiquette d&#39;expédition

Le commerçant/responsable de magasin remplit les informations nécessaires pour générer les étiquettes et soumet la demande.

### Étape 2 : requête envoyée à l’opérateur

Commerce contacte le transporteur et crée une commande dans le système du transporteur. Une commande distincte est créée pour chaque colis expédié.

### Étape 3 : l&#39;opérateur envoie le libellé et le numéro de suivi

Le transporteur envoie l&#39;étiquette d&#39;expédition et le numéro de suivi pour l&#39;expédition.

- Une seule expédition avec plusieurs colis reçoit plusieurs étiquettes d&#39;expédition.

- Si vous générez les mêmes étiquettes d&#39;expédition plusieurs fois, les numéros de suivi d&#39;origine sont conservés.

- Pour les produits retournés avec des numéros de retour client, les anciens numéros de suivi sont remplacés par de nouveaux.

### Étape 4 : Le commerçant télécharge et imprime l&#39;étiquette

Une fois l’étiquette d’expédition générée, la nouvelle expédition est enregistrée et l’étiquette peut être imprimée. Si l&#39;étiquette d&#39;expédition ne peut pas être créée en raison de problèmes de connexion ou pour toute autre raison, l&#39;expédition n&#39;est pas créée. Selon les paramètres de votre navigateur, le fichier PDF peut être ouvert et imprimé. Chaque libellé apparaît sur une page distincte dans le PDF.
