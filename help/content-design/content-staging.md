---
title: Évaluation du contenu
description: L’évaluation de contenu permet à votre équipe commerciale de créer, de prévisualiser et de planifier facilement un large éventail de mises à jour de contenu pour votre boutique directement depuis l’administration.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Évaluation du contenu

{{ee-feature}}

L’évaluation du contenu permet à votre équipe commerciale de créer, de prévisualiser et de planifier facilement un large éventail de mises à jour de contenu pour votre boutique directement depuis l’_Admin_. Par exemple, plutôt que de réfléchir en termes de page statique, considérez une page comme un ensemble de différents éléments qui peuvent être activés _activés_ ou _désactivés_ selon un planning. Vous pouvez utiliser l’évaluation du contenu pour créer une page qui change automatiquement tout au long de l’année selon un planning.

Le terme _campagne_ fait référence à l’enregistrement d’une modification planifiée ou à un ensemble de modifications gérées à partir du tableau de bord d’évaluation. Les modifications peuvent être affichées dans un calendrier ou un journal. Les termes _modification planifiée_ et _mise à jour planifiée_ sont interchangeables et font référence à une modification unique.

Lorsque vous planifiez une modification de contenu pour une période spécifique, le contenu revient à la version précédente à l’expiration de la modification planifiée. Vous pouvez créer plusieurs versions du même contenu de base à utiliser pour les mises à jour ultérieures. Vous pouvez également revenir en arrière sur la chronologie pour afficher les versions précédentes du contenu. Pour enregistrer un brouillon, il vous suffit d’affecter une date sur le journal qui est tellement éloignée dans le futur qu’elle ne passe jamais en production.

## Objets et campagnes d’évaluation de contenu

Les champs liés à la date de début et à la date de fin ont été supprimés d’Adobe Commerce et ne peuvent pas être modifiés directement sur la page règle de prix de panier, règle de prix de catalogue, produit, catégorie et CMS . Vous devez créer une mise à jour planifiée pour ces activations.

Toutes les mises à jour planifiées sont appliquées de manière consécutive, ce qui signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à la fois. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir une mise à jour planifiée différente pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut, et non de la mise à jour planifiée précédente.

Lorsqu’une nouvelle mise à jour planifiée est créée pour l’un des objets suivants, une campagne correspondante est créée comme espace réservé et la zone de _[!UICONTROL Scheduled Changes]_&#x200B;s’affiche en haut de la page. La campagne d’espace réservé comporte une date de début, mais pas de fin. Vous pouvez planifier des mises à jour du contenu dans le cadre d’une campagne, puis prévisualiser et partager les modifications par date, heure ou vue de magasin. Une fois qu’une nouvelle campagne est créée pour un objet, vous pouvez l’affecter en tant que mise à jour planifiée à d’autres objets.

- [Produits](../catalog/product-scheduled-changes.md)
- [Catégories](../catalog/category-scheduled-changes.md)
- [Règles de prix de catalogue](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Règles de prix du panier](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [Pages CMS](pages-workspace.md#scheduled-changes)
- [Blocs CMS](blocks.md)

## Workflow d’évaluation du contenu

1. **Créer le contenu de base**

   La ligne de base correspond au contenu d’une ressource sans campagne et inclut tous les éléments situés sous la section _[!UICONTROL Scheduled Changes]_&#x200B;en haut de la page. Le contenu de base est toujours utilisé, sauf s’il existe une campagne active avec des modifications planifiées à cet emplacement sur le journal.

1. **Créer la première campagne**

   Créez votre première campagne avec les dates de début et de fin selon vos besoins. Pour que la campagne soit ouverte, ne renseignez pas la date de fin. Lorsque la première campagne se termine, le contenu de base d’origine est restauré.

   La date de début et la date de fin de la campagne doivent être définies à l’aide du fuseau horaire **_par défaut_** Administrateur, converti à partir du fuseau horaire local de chaque site web. Prenons l’exemple où plusieurs sites web se trouvent dans des fuseaux horaires différents et où vous souhaitez lancer une campagne basée sur un fuseau horaire américain. Dans ce cas, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local, et définir **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** dans convertis de chaque fuseau horaire local du site web vers le fuseau horaire par défaut de l’administrateur.

1. **Ajouter une deuxième campagne**

   Créez la deuxième campagne, avec les dates de début et de fin selon les besoins. La deuxième campagne peut être affectée à une période entièrement différente. Lors de la création de plusieurs campagnes pour la même ressource, les campagnes ne peuvent pas se chevaucher. Vous pouvez créer autant de campagnes que nécessaire.

   Plusieurs ressources peuvent être affectées à une campagne existante qui n’a pas encore démarré. Par exemple, deux prix de produit différents peuvent être mis à jour dans la portée de la même campagne avec une date de début ultérieure.

   >[!NOTE]
   >
   >Si une campagne est liée à plusieurs entités, elle ne peut être modifiée qu’à partir du [Tableau de bord d’évaluation de contenu](content-staging-dashboard.md).

1. **Restaurer le contenu de base**

   Si toutes les campagnes comportent des dates de fin, le contenu de base est restauré chaque fois que toutes les campagnes actives se terminent.

   >[!NOTE]
   >
   >Si une campagne active est initialement créée sans date de fin, la campagne ne peut pas être modifiée ultérieurement pour inclure une date de fin. Dans ce cas, il est nécessaire de créer une campagne en double et de saisir la date de fin nécessaire.

>[!NOTE]
>
>Lorsqu&#39;une mise à jour d&#39;évaluation est active pour une entité, la modification de l&#39;entité modifie la mise à jour d&#39;évaluation active actuelle. Cela n’affecte pas le contenu de la ligne de base, qui est restauré à la fin de la mise à jour de l’évaluation.

## [!UICONTROL Content Staging] dashboard

Le [!UICONTROL Content Staging] [tableau de bord](content-staging-dashboard.md) offre une visibilité sur toutes les modifications et mises à jour prévues du site. Il est possible de prévisualiser n’importe quel jour, plage de dates ou période d’une campagne et de les partager avec d’autres personnes.

![Tableau de bord d’évaluation](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Démonstration de l&#39;évaluation du contenu

Pour en savoir plus sur l’évaluation du contenu, regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12&learn=on)

## Résolution des problèmes liés aux ressources

Pour obtenir de l’aide sur la résolution des problèmes d’évaluation du contenu, consultez les articles suivants de la base de connaissances de l’assistance [!DNL Commerce] :

- [Erreur 404 sur toutes les pages en raison d’un problème d’évaluation du contenu](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html?lang=fr)
- [Les mises à jour d’évaluation de contenu planifiées ne s’affichent pas avec le cache Fastly obsolète](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html?lang=fr)
- [Puis-je planifier des mises à jour d’évaluation de contenu pour les prix dans un catalogue partagé ?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html?lang=fr)
