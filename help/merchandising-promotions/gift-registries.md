---
title: Enregistrements de cadeaux
description: Découvrez comment les registres de cadeaux peuvent promouvoir les ventes lorsque les clients peuvent inviter leurs amis et leur famille à acheter leurs produits sélectionnés comme cadeaux.
exl-id: 2e5e3d52-e93e-444c-88a1-1eaa7f178b99
feature: Marketing Tools, Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Enregistrements de cadeaux

{{ee-feature}}

Adobe Commerce permet à vos clients de créer des registres de cadeaux pour les occasions spéciales et d’inviter leurs amis et leur famille à acheter leurs cadeaux dans le registre des cadeaux. Adobe Commerce effectue le suivi des articles achetés et des quantités restantes.

![Exemple de vitrine - registre des cadeaux pour bébés](./assets/storefront-gift-registry-create-baby-info.png){width="700" zoomable="yes"}

Le propriétaire du registre des cadeaux peut ajouter des produits au registre à partir de son [tableau de bord du client](gift-registry-storefront.md#gift-registry-information). De plus, les produits peuvent être transférés depuis la liste de souhaits ou le panier. En tant qu’administrateur de magasin, vous pouvez afficher et partager les registres de cadeaux des clients. Vous pouvez également effectuer des opérations de maintenance, telles que l’ajout d’articles dans le panier du client, la mise à jour de quantités ou la suppression d’un registre des cadeaux.

Pour accéder à un registre des cadeaux, les destinataires peuvent cliquer sur le lien contenu dans l’e-mail qu’ils reçoivent, ou effectuer une recherche par nom, adresse électronique ou identifiant de registre des cadeaux du destinataire. Dans la plupart des magasins, le pied de page de chaque page comporte un lien vers le registre des cadeaux, bien que l’emplacement puisse varier en fonction du thème. En outre, la variable [Widget](../content-design/widgets.md) peut être utilisé pour placer [Recherche dans le registre des cadeaux](gift-registry-search.md) n&#39;importe où dans votre magasin.

Les visiteurs du registre qui souhaitent effectuer un achat peuvent ajouter l’article dans leur panier directement à partir du registre des cadeaux. Lorsque la commande est passée, le registre des cadeaux est mis à jour pour refléter l’achat.

## Workflow du registre des cadeaux

1. **Configuration du registre des cadeaux pour le magasin**. L’administrateur du magasin [active le registre des cadeaux](gift-registry-configure.md), et [configuration du type de registre et des attributs ;](gift-registry-create.md).

1. **Le client crée son propre registre**. A [le client crée une liste de cadeaux](gift-registry-storefront.md#create-a-new-gift-registry) à partir de leur compte de boutique pour un événement à venir et remplissez les champs requis dans chaque section du registre des cadeaux. Après avoir ajouté des éléments au registre, ils peuvent être partagés avec des amis et de la famille.

1. **Le client partage son registre**. Un lien vers le registre des cadeaux est inclus dans chaque [invitation](gift-registry-storefront.md#share-a-gift-registry). If [Recherche dans le registre des cadeaux](gift-registry-search.md) est disponible dans le magasin, les clients peuvent rechercher des registres de cadeaux spécifiques par nom, adresse électronique ou ID de registre de cadeaux.

1. **Les destinataires de l&#39;invitation passent des commandes**. Ceux qui reçoivent une invitation ou des informations sur le registre peuvent commander n’importe quel article directement à partir du registre des cadeaux. Lorsque des articles sont vendus, Adobe Commerce met à jour le nombre d’articles du registre des cadeaux et en informe le propriétaire.
