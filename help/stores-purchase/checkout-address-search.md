---
title: Recherche d’adresses au passage en caisse
description: Découvrez comment inclure la recherche d’adresses lors du passage en caisse sur votre boutique.
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
TQID: https://experienceleague.adobe.com/fMrmhB3-kGvDKNBnI1PCUhndVN0RhQprpZGB6rjfo8o
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 434
ht-degree: 0%

---

# Recherche d’adresses au passage en caisse

{{ee-feature}}

Vos clients peuvent avoir de nombreuses adresses et informations enregistrées dans leur carnet d&#39;adresses, en particulier les clients réguliers, les clients récurrents ou les sociétés qui saisissent plusieurs commandes et lieux d&#39;expédition. L’affichage de nombreuses adresses peut considérablement ralentir le chargement et les processus de passage en caisse et entraîner une expérience d’achat négative. Pour augmenter la réactivité du passage en caisse, il est recommandé d’activer et de configurer la recherche d’adresses pour votre site.

>[!NOTE]
>
>La recherche d’adresses n’est pas activée par défaut. Vous pouvez configurer cette fonctionnalité pour qu’elle inclue la fonctionnalité sur votre site.

Lorsque cette fonctionnalité est activée et que le nombre d’adresses enregistrées du client atteint ou dépasse la limite configurée, les étapes _Expédition_ et _Révision et paiements_ n’affichent qu’une seule adresse (la valeur par défaut). Le client peut modifier l’adresse sélectionnée en cliquant sur **Modifier l’adresse**, puis en recherchant l’adresse correcte par ville, État, rue ou code postal. Cette fonctionnalité prend également en charge la sélection d’adresses pour le passage en caisse du registre des cadeaux.

![Passage en caisse avec les adresses d’expédition enregistrées affichées](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Si le client ne dispose pas d&#39;une adresse de livraison par défaut, la page _Livraison_ s&#39;affiche _Aucune adresse sélectionnée_. Dans ce cas, le client doit cliquer sur **Modifier l’adresse** pour sélectionner une adresse enregistrée ou sur **Nouvelle adresse** pour ajouter et sélectionner une adresse avant de procéder au passage en caisse. Si le client ne dispose pas d’une adresse de facturation par défaut, la page _Vérifier et payer_ affiche l’adresse sélectionnée pour l’expédition avec l’option _Modifier l’adresse_.

![Message Extraction sans adresse sélectionnée](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Recherche d&#39;adresses verrouillées pour les devis

![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement)

L&#39;activation de la recherche d&#39;adresses affecte également le passage en caisse pour les commandes créées à partir de devis où le nombre d&#39;adresses enregistrées du client atteint ou dépasse la limite configurée. Lorsque le devis est terminé et que le client passe en caisse, seule l&#39;adresse d&#39;expédition sélectionnée s&#39;affiche. La page affiche également un message indiquant que l&#39;adresse d&#39;expédition est verrouillée et ne peut être modifiée que dans le devis.

![Adresse d&#39;expédition verrouillée pour un devis](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Activer la recherche d’adresses

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Checkout Options]** .

   ![Configuration - Options de paiement](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Pour obtenir une description détaillée de chacun de ces paramètres de configuration, consultez [Options de paiement](../configuration-reference/sales/checkout.md#checkout-options) dans le _Guide de référence de configuration_.

1. Définissez **[!UICONTROL Enable Address Search]** sur `Yes`.

1. Pour spécifier le seuil d’inclusion de la fonction de recherche d’adresses, définissez l’option **[!UICONTROL Number of Customer Addresses Limit]** .

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour effectuer cette modification.

   Lorsque le nombre d’adresses enregistrées du client atteint ou dépasse cette limite, la page affiche l’adresse par défaut (si le client en a une) ou _Aucune adresse sélectionnée_ avec l’option _Modifier l’adresse_. La limite par défaut est `10`.

1. Cliquez sur **[!UICONTROL Save Config]**.
