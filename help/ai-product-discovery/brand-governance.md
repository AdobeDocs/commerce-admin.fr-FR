---
title: Créer des règles de marque d’enrichissement de catalogue
description: Découvrez comment créer et gérer des règles de gouvernance de marque pour l’enrichissement du catalogue, définir les exigences en matière de copie de produit et appliquer des règles aux tâches d’enrichissement du catalogue.
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# Créer des règles de marque d’enrichissement de catalogue

Les règles de gouvernance de marque ne sont disponibles que pour l’enrichissement du catalogue. Elles ne s&#39;appliquent pas à l&#39;enrichissement PDP. Ces règles définissent les exigences pour les noms et descriptions de produits générés par [!DNL Commerce Catalog Agent]. Modifiez ou configurez une règle par défaut pour vos standards de marque par défaut, puis créez des règles personnalisées pour des campagnes, des catégories de produits ou des sous-marques spécifiques. Sélectionnez une règle lorsque vous créez une tâche d’[enrichissement du catalogue](catalog-enrichment.md).

## Gouvernance de marque ouverte

1. Dans l’administration, accédez à **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**.
1. Ouvrez l’onglet **[!UICONTROL Brand Governance]**.

L’onglet **Gouvernance des marques** contient la règle par défaut et les règles personnalisées que vous avez créées. Vous pouvez rechercher des règles ou filtrer la table des règles.

Pour chaque ligne, vous voyez **Nom de la règle**, **Champs**, **Tonalité**, **Dernière modification** et **État**. La règle par défaut est marquée **[!UICONTROL Default]**.

La zone **[!UICONTROL Needs your attention]** met en évidence les règles qui nécessitent un travail, telles que les brouillons qui doivent être configurés ou les règles avec conflits. Passez en revue les détails de la règle et utilisez l’action disponible, telle que **[!UICONTROL Finish setup]** ou **[!UICONTROL Fix conflict]**.

## Présentation des types de règle

L’enrichissement de catalogue prend en charge une règle par défaut et des règles personnalisées.

### Règle par défaut

Chaque instance [!DNL Adobe Commerce] comporte exactement une règle par défaut. [!DNL Adobe Commerce] crée cette règle avec des champs vides. Son nom est fixe en tant que **[!UICONTROL Global]**. Vous pouvez modifier la règle, mais vous ne pouvez pas la supprimer.

[!DNL Adobe Commerce] applique la règle par défaut lorsque vous créez une tâche d’enrichissement du catalogue sans sélectionner de règle personnalisée. La règle par défaut fournit la gouvernance de base pour l’enrichissement du catalogue.

### Règles personnalisées

Vous pouvez créer un nombre illimité de règles personnalisées pour une campagne, une catégorie de produits ou une sous-marque. Une règle personnalisée n’est pas appliquée automatiquement. Sélectionnez-la lors de la création d’une tâche d’enrichissement du catalogue.

Une règle personnalisée n’hérite pas des valeurs de la règle par défaut. Lorsque vous créez une règle personnalisée, vous pouvez copier les valeurs actuelles de la règle par défaut comme point de départ unique. Les modifications ultérieures apportées à la règle par défaut ne mettent pas à jour la règle personnalisée.

Utilisez la règle par défaut pour les normes qui doivent s’appliquer lorsqu’un utilisateur ne sélectionne pas de règle personnalisée. Créez une règle personnalisée pour une campagne ou une catégorie avec des exigences différentes. Ajoutez les exigences globales dont la règle personnalisée a également besoin, car les règles personnalisées n’héritent pas des valeurs globales.

## Création d’une règle personnalisée

Dans cette section, vous apprendrez à créer une règle de gouvernance de marque.

![Créer Une Règle De Gouvernance De Marque](./assets/brand-gov-create-rule.png)

1. Dans l’onglet **Gouvernance des marques**, cliquez sur **[!UICONTROL Create Rule]**.
1. Choisissez le mode de démarrage de la règle :
   - **[!UICONTROL Blank]** : définissez toutes les valeurs vous-même.
   - **[!UICONTROL Copy Global enrichment]** : commencez avec les valeurs actuelles de la règle par défaut comme une copie unique.
   - **[!UICONTROL Draft with AI]** : (**Prochainement**) Décrivez votre voix de marque pour obtenir des valeurs de règle suggérées.
1. Saisissez un **nom de règle** qui identifie son objectif, tel qu’une campagne, une catégorie ou une sous-marque.
1. Sous **Champs à améliorer**, configurez les exigences relatives au nom et à la description du produit.

   Configurez les noms et descriptions des produits séparément. Chaque champ a ses propres exigences de basculement d’activation et de gouvernance.

1. Définir **la longueur du nom du produit**.

   Définissez la plage de longueur minimale et maximale d’un nom de produit enrichi. Par exemple, une règle peut nécessiter un minimum de 20 caractères et un maximum de 200 caractères.

1. Définissez l’option **Majuscules** :

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]** : conservez les majuscules du texte source.

1. Décrivez la **tonalité de la marque**. Voir [définir le ton de la marque](#set-brand-tone) pour obtenir des conseils.
1. Définir les expressions obligatoires et exclues

   Ajoutez une expression **[!UICONTROL Must include]**.
   Ajoutez une expression **[!UICONTROL Never use]**.

1. Cliquez sur **[!UICONTROL Save as draft]** pour terminer plus tard, ou sur **[!UICONTROL Publish rule]** pour rendre la règle disponible à la sélection lors de la création d’une règle d’enrichissement de catalogue. Cliquez sur **[!UICONTROL Cancel]** pour quitter sans enregistrer.

1. Vous pouvez désormais appliquer la règle à une tâche d’enrichissement du catalogue [](catalog-enrichment.md).

### Définir le ton de la marque

Saisissez des conseils dans le champ multiligne **[!UICONTROL Brand tone]** pour décrire la voix et le style du nom enrichi.

Voici quelques exemples du ton que vous pouvez utiliser pour la **Description** :

- **B2B industriel** : `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **Mode de luxe** : `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **Électronique grand public** : `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **Aliments de spécialité et épicerie** : `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **Mobilier de maison** : `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
