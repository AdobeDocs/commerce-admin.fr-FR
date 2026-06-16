---
title: Registres des cadeaux
description: Découvrez comment les registres de cadeaux peuvent promouvoir les ventes lorsque les clients peuvent inviter leurs amis et leur famille à acheter les produits qu’ils ont sélectionnés en cadeau.
exl-id: 2e5e3d52-e93e-444c-88a1-1eaa7f178b99
feature: Marketing Tools, Gift, Storefront
TQID: https://experienceleague.adobe.com/fWjH1PgahxEIm-4uH9di-G-GPxc-Nxku2oMcCqcV958
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 379
ht-degree: 0%

---

# Registres des cadeaux

{{ee-feature}}

Adobe Commerce permet à vos clients de créer des registres de cadeaux pour des occasions spéciales et d’inviter leurs proches à acheter leurs cadeaux dans le registre des cadeaux. Adobe Commerce effectue le suivi des articles achetés et des quantités restantes.

![Exemple storefront - registre cadeau pour bébé](./assets/storefront-gift-registry-create-baby-info.png){width="700" zoomable="yes"}

Le propriétaire du registre des cadeaux peut ajouter des produits au registre à partir de son [tableau de bord client](gift-registry-storefront.md#gift-registry-information). En outre, les produits peuvent être transférés de la liste de souhaits ou du panier. En tant qu&#39;administrateur de magasin, vous pouvez afficher et partager les registres de cadeaux des clients. Vous pouvez également effectuer des opérations de maintenance, comme ajouter des articles depuis le panier du client, mettre à jour des quantités ou supprimer un registre des cadeaux.

Pour accéder à un registre des cadeaux, les destinataires peuvent cliquer sur le lien contenu dans l&#39;e-mail qu&#39;ils reçoivent ou effectuer une recherche par nom, adresse e-mail ou ID de registre des cadeaux. Dans la plupart des magasins, le pied de page de chaque page comporte un lien vers le registre des cadeaux, bien que l&#39;emplacement puisse varier selon le thème. En outre, l&#39;outil [Widget](../content-design/widgets.md) peut être utilisé pour placer [Gift Registry Search](gift-registry-search.md) n&#39;importe où dans votre boutique.

Les visiteurs du Registre qui souhaitent effectuer un achat peuvent ajouter l&#39;article à leur panier directement à partir du registre des cadeaux. Lorsque la commande est passée, le registre des cadeaux est mis à jour pour refléter l&#39;achat.

## Workflow du registre des cadeaux

1. **Configurer le registre des cadeaux pour la boutique**. L&#39;administrateur du magasin [active le registre des cadeaux](gift-registry-configure.md) et [configure le type et les attributs du registre](gift-registry-create.md).

1. **Le client crée son propre registre**. Un [client crée un registre des cadeaux](gift-registry-storefront.md#create-a-new-gift-registry) à partir de son compte de boutique pour une occasion à venir, et remplit les champs requis dans chaque section du registre des cadeaux. Après avoir ajouté des éléments au registre, il peut être partagé avec les amis et la famille.

1. **Le client partage son registre**. Chaque [invitation](gift-registry-storefront.md#share-a-gift-registry) contient un lien vers le registre des cadeaux. Si la fonction [Recherche du registre des cadeaux](gift-registry-search.md) est disponible dans la boutique, les clients peuvent rechercher des registres des cadeaux spécifiques par nom, adresse e-mail ou ID de registre des cadeaux.

1. **Les destinataires de l&#39;invitation passent des commandes**. Ceux qui reçoivent une invitation ou des informations sur le registre peuvent passer une commande pour n&#39;importe quel article directement à partir du registre des cadeaux. Au fur et à mesure que des articles sont vendus, Adobe Commerce met à jour le nombre d’articles du registre des cadeaux et en informe le propriétaire.
