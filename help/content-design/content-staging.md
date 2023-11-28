---
title: Évaluation du contenu
description: L’évaluation de contenu permet à votre équipe d’entreprise de créer, de prévisualiser et de planifier facilement toute une gamme de mises à jour de contenu pour votre boutique, directement depuis l’administrateur.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Évaluation du contenu

{{ee-feature}}

L’évaluation du contenu permet à votre équipe d’entreprise de créer, de prévisualiser et de planifier facilement un large éventail de mises à jour de contenu pour votre boutique, directement depuis le _Administration_. Par exemple, plutôt que de penser en termes de page statique, considérez une page comme un ensemble d’éléments différents qui peuvent être transformés. _on_ ou _off_ selon un calendrier. Vous pouvez utiliser l’évaluation du contenu pour créer une page qui change automatiquement tout au long de l’année selon un calendrier.

Le terme _campaign_ fait référence à l’enregistrement d’une modification planifiée ou d’une collection de modifications gérées à partir du tableau de bord d’évaluation. Les modifications peuvent être visualisées dans un calendrier ou une chronologie. Les termes _modification planifiée_ et _mise à jour planifiée_ sont interchangeables et font référence à une seule modification.

Lorsque vous planifiez une modification du contenu pour une période spécifique, le contenu revient à la version précédente à l’expiration de la modification planifiée. Vous pouvez créer plusieurs versions du même contenu de base à utiliser pour des mises à jour ultérieures. Vous pouvez également revenir en arrière dans la chronologie pour afficher les versions précédentes du contenu. Pour enregistrer une version préliminaire, il vous suffit d’attribuer une date dans la frise chronologique si lointaine qu’elle ne sera jamais mise en production.

## Objets et campagnes d’évaluation de contenu

Lorsqu’une nouvelle mise à jour planifiée est créée pour l’un des objets suivants, une campagne correspondante est créée en tant qu’espace réservé, et la variable _[!UICONTROL Scheduled Changes]_s’affiche en haut de la page. La campagne d’espace réservé a une date de début, mais pas une date de fin. Vous pouvez planifier des mises à jour du contenu dans le cadre d’une campagne, puis prévisualiser et partager les modifications par date, heure ou vue de magasin. Une fois qu’une nouvelle campagne est créée pour un objet, vous pouvez l’affecter comme mise à jour planifiée pour d’autres objets.

- [Produits](../catalog/product-scheduled-changes.md)
- [Catégories](../catalog/category-scheduled-changes.md)
- [Règles de prix du catalogue](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Règles de prix du panier](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [Pages CMS](pages-workspace.md#scheduled-changes)
- [Blocs CMS](blocks.md)

## Workflow d’évaluation de contenu

1. **Création du contenu de base**

   La ligne de base est le contenu d’une ressource sans campagne et comprend tout ce qui se trouve en dessous de la ligne de base _[!UICONTROL Scheduled Changes]_en haut de la page. Le contenu de base est toujours utilisé, sauf s’il existe une campagne active avec des modifications planifiées pour cet emplacement dans la chronologie.

1. **Créer la première campagne**

   Créez votre première campagne avec les dates de début et de fin selon vos besoins. Pour que la campagne soit ouverte, laissez la date de fin vide. À la fin de la première campagne, le contenu de base d’origine est restauré.

   >[!NOTE]
   >
   >La date de début et la date de fin de la campagne doivent être définies à l’aide de la variable **_default_** Fuseau horaire de l’administrateur, converti à partir du fuseau horaire local de chaque site web. Prenons l’exemple de plusieurs sites web dans différents fuseaux horaires, mais que vous souhaitez lancer une campagne basée sur un fuseau horaire américain. Dans ce cas, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local, puis définir **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** dans converti de chaque fuseau horaire de site web local vers le fuseau horaire d’administration par défaut.

1. **Ajouter une seconde campagne**

   Créez la seconde campagne, avec les dates de début et de fin nécessaires. La seconde campagne peut être affectée à une période entièrement différente. Lors de la création de plusieurs campagnes pour la même ressource, les campagnes ne peuvent pas se chevaucher. Vous pouvez créer autant de campagnes que nécessaire.

   >[!NOTE]
   >
   >Toutes les mises à jour planifiées sont appliquées consécutivement, ce qui signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à la fois. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir une mise à jour planifiée différente pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

1. **Restaurer le contenu de base**

   Si toutes les campagnes comportent des dates de fin, le contenu de base est restauré chaque fois que toutes les campagnes actives se terminent.

>[!NOTE]
>
>Lorsqu’une mise à jour intermédiaire est active pour une entité, la modification de l’entité modifie la mise à jour d’évaluation active actuelle. Elle n’affecte pas le contenu de base, qui est restauré à la fin de la mise à jour intermédiaire.

## [!UICONTROL Content Staging] tableau de bord

La variable [!UICONTROL Content Staging] [tableau de bord](content-staging-dashboard.md) offre une visibilité sur toutes les modifications et mises à jour prévues du site. Il est possible de prévisualiser n’importe quel jour, plage de dates ou période d’une campagne et de la partager avec d’autres personnes.

![Tableau de bord intermédiaire](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Démonstration de l’évaluation du contenu

Pour en savoir plus sur l’évaluation du contenu, regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## Ressources de dépannage

Pour obtenir de l’aide sur la résolution des problèmes liés à l’évaluation du contenu, voir : [!DNL Commerce] Prise en charge des articles de la base de connaissances :

- [Erreur 404 sur toutes les pages en raison d’un problème d’évaluation du contenu](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [Mises à jour de l’évaluation du contenu planifiées non affichées avec le cache fastidieux obsolète](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [Puis-je planifier des mises à jour d’évaluation de contenu pour les prix dans un catalogue partagé ?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
