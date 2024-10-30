---
title: Cas d’utilisation et workflows des modèles de citations
description: Créez un modèle de devis à partir d’un devis existant afin de rationaliser la négociation des devis pour les commandes récurrentes.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# Cas d’utilisation et workflows des modèles de citations

La fonctionnalité Modèle de devis permet aux acheteurs et aux vendeurs de rationaliser le processus de devis en créant des modèles de devis réutilisables et personnalisables.

- **Guillemets personnalisables** : les acheteurs peuvent générer des guillemets liés à partir d’un modèle préapprouvé, ce qui permet de personnaliser les éléments dans des paramètres spécifiés, tels que les quantités et les sélections d’éléments de ligne.
- **Seuils de commande** : les vendeurs peuvent définir des engagements de commande minimum et maximum, en s’assurant que les acheteurs adhèrent aux volumes d’achat convenus.
- **Dates d’expiration** : les modèles peuvent avoir des périodes de validité, en s’assurant que les termes ne s’appliquent que pendant une période spécifiée.
- **Remises et tarifs** : les vendeurs peuvent utiliser les mêmes fonctionnalités de réduction sur les prix d’expédition, sur les articles et sur les lignes, ainsi que sur les prix d’expédition, disponibles avec des guillemets pour définir des remises pour les commandes récurrentes, ce qui simplifie le processus de négociation.
- **Suivi et création de rapports** : le système effectue le suivi du nombre de guillemets liés générés à partir du modèle et des commandes exécutées avec succès afin de fournir des informations sur l’exécution des quotas de commande convenus.

## Cas d’utilisation

Un acheteur d’entreprise peut utiliser un modèle de devis pour commander un ensemble spécifique de produits sur une période donnée. L&#39;acheteur configure les options suivantes de modèle de devis pour rendre le processus de devis plus efficace, cohérent et aligné sur les accords d&#39;achat stratégiques.

- Seuil de commandes permettant de spécifier le nombre minimal et maximal de commandes éligibles à une tarification négociée. Elle peut être utilisée pour appliquer et suivre les quotas de commande spécifiés dans les contrats.

- Seuils de quantité (quantités minimales/maximales) Le modèle spécifie un seuil de quantité pour définir la quantité minimale et maximale pouvant être achetée pour chaque commande, en veillant à ce que le vendeur puisse gérer efficacement les stocks tout en offrant à l’acheteur la possibilité d’ajuster les quantités selon les besoins.

## Workflow de modèle de devis

Les modèles de devis peuvent être lancés par l&#39;acheteur ou le vendeur.

**Étape 1 : création d’un modèle de devis (nouveau)**

- **L’acheteur crée le modèle de devis**

  Lors de la révision d&#39;un modèle de devis existant, l&#39;acheteur décide que l&#39;entreprise doit soumettre plusieurs commandes au cours de l&#39;année suivante et souhaite demander des remises supplémentaires en fonction de l&#39;activité récurrente. Ils créent un modèle de guillemet à l’aide de l’action *[!UICONTROL Create quote template]* sur le guillemet. Ensuite, ils lancent la négociation en envoyant le nouveau modèle au vendeur pour révision.

  Les acheteurs peuvent également créer un modèle de devis directement à partir de la page *[!UICONTROL My Quote Templates]** du storefront.

- **Représentant commercial** — Un représentant commercial peut créer un modèle de devis de l’administrateur au nom d’un acheteur d’entreprise spécifique. Le représentant commercial peut créer le modèle de devis dans l’administrateur à partir d’un devis existant ou de la grille [!UICONTROL Quote Templates] et l’enregistrer en tant que `draft` ou l’envoyer à l’acheteur pour lancer la négociation. En version préliminaire, la citation est visible uniquement pour le vendeur. Une fois le guillemet envoyé, l’état est `Submitted`. Il ne peut pas être modifié par le vendeur tant que l&#39;acheteur ne l&#39;a pas renvoyé.

  ![Le vendeur lance un devis d’acheteur à partir de la grille Devis dans l’Admin](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**Étape 2 : Révision et négociation de citations**

La révision ou la négociation d’un modèle de devis peut inclure la modification de quantités, la suppression d’articles, l’ajout de commentaires d’articles, l’application de remises sur les articles ou les devis (vendeur) et l’ajout d’une adresse de livraison (acheteur).

- **Le vendeur consulte la demande et envoie une réponse** : dans l’administrateur, le vendeur affiche le modèle de devis à partir de la grille *[!UICONTROL Quote Templates]** ou l’ouvre à partir du lien contenu dans la notification électronique. Sur le storefront, l’état du devis passe à `Pending`, et l’acheteur ne peut pas apporter de modifications. Suivant le même processus de [négociation de devis](quote-price-negotiation.md), le vendeur répond en offrant des rabais sur les prix et en ajustant les quantités et les articles selon les besoins, saisit un commentaire et renvoie le devis à l’acheteur. L&#39;acheteur et le représentant commercial sont informés par email que le vendeur a répondu.

- **L’acheteur consulte le modèle de devis du vendeur et envoie une réponse** : l’acheteur clique sur le lien dans la notification électronique pour ouvrir le modèle de devis, ou il ouvre le devis à partir de la page _Mes modèles de devis_ du tableau de bord du compte. L’acheteur peut laisser des notes au vendeur au niveau de l’article ou du devis, modifier les quantités et supprimer des articles.

L&#39;acheteur et le vendeur poursuivent le processus de négociation jusqu&#39;à ce qu&#39;un accord soit trouvé, ou le vendeur refuse le modèle de devis. Si l’acheteur modifie le devis (ajout ou suppression de produits ou modification des quantités de produits), le devis doit être renvoyé au vendeur pour révision.

- **L’acheteur ajoute une adresse de livraison** - L’acheteur doit ajouter une adresse de livraison au modèle de devis s’il n’en a pas. Une fois que l’acheteur a ajouté l’adresse, le vendeur peut fournir des options d’expédition et de livraison. Les méthodes d’expédition affichées dépendent de la configuration de Storefront.

Si l&#39;acheteur ajoute une adresse d&#39;expédition, l&#39;accord de négociation doit être révisé et le vendeur peut poursuivre le processus de négociation jusqu&#39;à ce qu&#39;un accord soit trouvé, ou le vendeur refuse le modèle de devis.

**Étape 3 : l’acheteur accepte le modèle de devis**

L&#39;acheteur accepte les conditions négociées dans le modèle. Une fois le modèle de devis accepté, l&#39;acheteur peut l&#39;utiliser pour générer des guillemets liés prévalidés qui peuvent être utilisés pour envoyer des commandes sans nécessiter d&#39;autres négociations.

Les options d’expédition sont verrouillées lors du passage en caisse.

### Afficher un modèle de devis

1. Dans la colonne **[!UICONTROL Actions]** d&#39;un enregistrement, cliquez sur **[!UICONTROL View]**.

1. Pour répondre à la demande du client, suivez les instructions et commencez le même processus de [négociation de prix](quote-price-negotiation.md) utilisé pour négocier des devis.

### Activité de modèle de devis

Affichez la chronologie de la négociation, la communication et toute autre activité de devis de [!UICONTROL Comments] et [!UICONTROL History Log] : les informations incluent les modifications d’état, les mises à jour des informations sur les clients et l’expédition, les mises à jour des articles et des prix, ainsi que d’autres informations importantes.

1. Ouvrez un modèle de guillemet.

1. Affichez les commentaires et l’historique de la négociation des guillemets en accédant à **[!UICONTROL Negotiation]** et en sélectionnant **[!UICONTROL Comments]** et **[!UICONTROL History Log]**.

   ![Afficher l’historique](./assets/quote-view-history.png){width="400"}

1. L’historique est également suivi au niveau des éléments de ligne.

   ![Afficher l’historique des éléments de ligne](./assets/quote-view-line-item-history.png){width="400"}


### Refuser un modèle de guillemet

Seuls les modèles de devis avec un état `In Review` peuvent être refusés.

1. Dans la grille *[!UICONTROL Quote Templates]*, ouvrez le modèle de guillemet que vous souhaitez refuser.

1. Sur le modèle de guillemet, cliquez sur **[!UICONTROL Decline]**.

1. Lorsque vous y êtes invité, saisissez la raison pour laquelle le guillemet a été refusé, puis cliquez sur **[!UICONTROL Confirm]**.
