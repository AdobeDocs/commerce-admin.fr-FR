---
title: Codes de coupon
description: Découvrez comment utiliser des codes de coupons avec des règles de prix de panier pour appliquer une remise lorsqu’un ensemble de conditions est satisfait.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---

# Codes de coupon

Les codes coupon sont utilisés avec [règles de prix du panier](price-rules-cart.md) pour appliquer une remise lorsqu’un ensemble de conditions est satisfait. Par exemple, un code de bon peut être créé pour un groupe de clients spécifique ou pour toute personne effectuant un achat sur un certain montant. Pour appliquer le coupon à un achat, le client peut saisir le code du coupon dans le panier, ou éventuellement dans la caisse enregistreuse de votre _brique et mortier_ magasin. Vous trouverez ci-dessous quelques façons d’utiliser des coupons dans votre boutique :

- Coupons par e-mail aux clients
- Générer des bons imprimés
- Créer des bons en magasin pour les utilisateurs mobiles

Les codes coupon peuvent être envoyés par e-mail ou inclus dans les newsletters, catalogues et publicités. La liste des codes de coupon peut être exportée et envoyée vers une imprimante commerciale. Vous pouvez également créer des coupons en magasin avec un code de réponse rapide que les acheteurs peuvent analyser à l’aide de leur smartphone. Le code QR peut renvoyer vers une page de votre site contenant plus d’informations sur la promotion.

## Configuration des codes de bon

La longueur et le format des codes de bons générés automatiquement sont contrôlés par la configuration. Les caractères peuvent être définis sur tous les nombres, toutes les lettres ou une combinaison. Vous pouvez insérer un tiret à des intervalles définis pour faciliter la lecture et ajouter un préfixe et un suffixe pour associer le code à une campagne ou une initiative spécifique.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Promotions]**.

   ![Configuration des clients : codes de coupon spécifiques générés automatiquement](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Développez l’objet **[!UICONTROL Auto Generated Specific Coupon Codes]** .

   ![Configuration des clients : codes de coupon spécifiques générés automatiquement](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Saisissez le **[!UICONTROL Code Length]**, y compris le préfixe, le suffixe et les séparateurs.

1. Définissez la variable **[!UICONTROL Code Format]** à l’une des options suivantes :

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. Pour **[!UICONTROL Code Prefix]**, saisissez la valeur qui doit apparaître au début de tous les codes de bon.

1. Pour **[!UICONTROL Code Suffix]**, saisissez la valeur qui doit apparaître à la fin de tous les codes de bon.

1. Pour **[!UICONTROL Dash Every X Characters]**, saisissez le nombre de caractères entre chaque tiret.

   Les codes coupon avec différents modèles de tiret sont considérés comme des codes différents, même si les nombres sont identiques.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Créer des bons

>[!NOTE]
>
>Avant de créer des coupons, utilisez le `bin/magento cron:run` pour vérifier que cron est en cours d’exécution. Voir [Exécutez cron depuis la ligne de commande](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) dans le _Guide de configuration_ pour plus d’informations.

### Méthode 1 : création d’un coupon spécifique

1. Suivez les instructions pour créer une [règle de prix du panier](price-rules-cart.md).

1. Dans le **[!UICONTROL Rule Information]** , définissez **[!UICONTROL Coupon]** to `Specific Coupon`.

1. Saisissez un **[!UICONTROL Coupon Code]** à utiliser avec la promotion.

   Le format du code (numérique, alphanumérique ou alphabétique) est déterminé par la variable [configuration](#configure-coupon-codes).

1. Pour limiter le nombre d&#39;utilisations du coupon, procédez comme suit :

   - Saisissez le nombre de **[!UICONTROL Uses per Coupon]**.
   - Saisissez le nombre de **[!UICONTROL Uses per Customer]**.

   Pour une utilisation illimitée, laissez ces champs vides.

   ![Règle de prix du panier - Informations sur les coupons](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si plusieurs clients utilisent simultanément le même coupon, il est possible que la limite d’utilisation définie puisse être dépassée en raison du retard du traitement des coupons.

1. Pour que le coupon soit valide pendant une période donnée, procédez comme suit :

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Pour **De** et **À** dates. Pour sélectionner la date, cliquez sur le bouton **Calendrier** (![Icône Calendrier](../assets/icon-calendar.png)) en regard de chaque champ. Si vous laissez la période vide, la règle n’expire pas.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Effectuez l’une des opérations suivantes :

     **Option 1 :** Planifier une nouvelle mise à jour

      - Cliquez sur **[!UICONTROL Schedule New Update]** dans le coin supérieur droit de la page.

        ![Mise à jour du planning](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Saisissez le **[!UICONTROL Update Name]** et **[!UICONTROL Description]**.

      - Choisissez la **Date de début** et **[!UICONTROL End Date]** dans le calendrier ( ![Icône Calendrier](../assets/icon-calendar.png) ). Si vous laissez la période vide, la règle n’expire pas.

      - Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

        ![Règle de prix du panier - Modification planifiée](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Option 2 :** Attribuer à une mise à jour existante :

      - Sélectionner **[!UICONTROL Assign to Another Update]**.

      - Recherchez la mise à jour dans la liste, puis cliquez sur **[!UICONTROL Select]**.

1. Procédez comme suit : [règle de prix du panier](price-rules-cart.md) selon les besoins.

### Méthode 2 : générer un lot de bons

La génération de coupons de réduction est une opération asynchrone qui s’exécute en arrière-plan afin que vous puissiez continuer à travailler dans l’administrateur sans attendre que l’opération soit terminée. Le système affiche un message lorsque la tâche est terminée.

1. Suivez les instructions pour créer une [règle de prix du panier](price-rules-cart.md).

1. Sous **[!UICONTROL Coupon Code]**, sélectionnez la variable **[!UICONTROL Use Auto Generation]** .

1. Pour limiter le nombre d’utilisations du coupon par chaque client, indiquez le nombre de **[!UICONTROL Uses per Customer]**.

   ![Règle de prix du panier - générer des bons à numérotation automatique](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si plusieurs clients utilisent simultanément le même coupon, il est possible que la limite d’utilisation définie puisse être dépassée en raison du retard du traitement des coupons.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Manage Coupon Codes]** et procédez comme suit :

   ![Règle de prix du panier - Gestion des codes de coupon](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Pour **[!UICONTROL Coupons Qty]**, indiquez le nombre de bons à générer.

   - Saisissez le **[!UICONTROL Code Length]**, sans inclure le préfixe, le suffixe ou les séparateurs.

   - Définissez la variable **[!UICONTROL Code Format]** à l’une des options suivantes :

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Facultatif) Saisissez un **[!UICONTROL Code Prefix]** à ajouter au début du code.

   - (Facultatif) Saisissez un **[!UICONTROL Code Suffix]** à ajouter à la fin du code.

   - (Facultatif) Pour **[!UICONTROL Dash Every X Characters]**, saisissez le nombre de caractères entre chaque tiret. Par exemple, si le code comporte 12 caractères et qu’un tiret est inséré tous les quatre caractères, il ressemble à ce qui suit : `xxxx-xxxx-xxxx`. Les tirets facilitent la lecture et la saisie des codes.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Generate]**.

   Le système affiche `Message is added to queue, wait to get your coupons soon`.

   Une fois la tâche cron terminée, la liste des codes générés s’affiche.

   | Champ | Description |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Code unique de coupon qui a été créé et peut être utilisé pour recevoir des conditions spéciales. |
   | [!UICONTROL Created] | Date de création du code de coupon. |
   | [!UICONTROL Used] | Indique si le coupon a été utilisé. |
   | [!UICONTROL Times Used] | Indique le nombre de fois où le code de coupon a été utilisé. |

   {style="table-layout:auto"}

Vous pouvez exporter des codes de coupon vers un fichier CSV ou Excel XML en sélectionnant le format de fichier et en cliquant sur **[!UICONTROL Export]**.

Pour supprimer des codes de bon, sélectionnez un ou plusieurs codes dans la liste. Sélectionner `Delete` de la **[!UICONTROL Actions]**  , puis cliquez sur **[!UICONTROL Submit]**.

>[!NOTE]
>
>Même si Commerce permet de configurer plusieurs codes de bon, un client ne peut utiliser qu’un seul code de bon dans le panier. Pour permettre l’utilisation simultanée de plusieurs codes de bon dans le panier, vous pouvez utiliser une extension correspondante depuis [Commerce Marketplace](https://marketplace.magento.com/).

## Rapport Coupons

La variable _Coupons_ Ce rapport agrège les données de chaque coupon utilisé au cours d’une période spécifique. Les coupons étant appliqués à partir du panier, le rapport inclut les données de tous les bons échangés, indépendamment de [état de la commande](../stores-purchase/order-status.md). Par conséquent, le rapport peut inclure les totaux prévus et réels. Le rapport peut être filtré pour une vue de magasin, une période, un état de commande et une règle de prix du panier spécifiques.

Dans l&#39;exemple suivant, le code de coupon &quot;H20&quot; a été utilisé par deux clients. L&#39;une des commandes est facturée, mais l&#39;autre est toujours facturée. _en attente_. Les colonnes Sous-total des ventes, Répartition des ventes et Total des ventes projetées indiquent les montants agrégés des deux commandes, mais seule la commande réellement facturée apparaît dans les colonnes Sous-total, Remise et Total. Chaque ligne du rapport représente une promotion de coupon unique.

![Rapport Coupons](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Exécution du rapport

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Si vous avez plusieurs vues de magasin, définissez **[!DNL Store View]** dans le coin supérieur gauche pour définir la portée du rapport.

1. Pour actualiser les ventes [statistics](../getting-started/sales-reports.md#refresh-statistics) pour le jour, cliquez sur le bouton _Dernière mise à jour_ message en haut de l’espace de travail.

   Cliquez ensuite pour sélectionner la variable **[!UICONTROL Coupons]** case à cocher et clic **[!UICONTROL Refresh]**.

   ![Rapport Coupons - Actualiser les statistiques](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Pour filtrer les données, procédez comme suit :

   ![Rapport Coupon - Filtres](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Date Used]** à l’une des options suivantes :

      - `Order Created`
      - `Order Updated`

     La variable _Commande mise à jour_ est créé en temps réel et ne nécessite pas d’actualisation.

   - Pour définir la période couverte par le rapport, définissez **[!UICONTROL Period]** à l’une des options suivantes :

      - `Day`
      - `Month`
      - `Year`

   - Pour définir la période du rapport, saisissez la **De** et **À** dates au format M/J/AA.

   - Pour imprimer un rapport pour une [état de la commande](../stores-purchase/order-status.md), définit **[!UICONTROL Order Status]** to `Specified` et choisissez l’état de l’ordre dans la liste.

   - Pour omettre les lignes sans données du rapport, définissez **[!UICONTROL Empty Rows]** to `No`.

   - Pour définir l&#39;activité des coupons inclus dans le rapport, effectuez l&#39;une des opérations suivantes :

      - Pour inclure toutes les activités de coupon de toutes les règles de prix, définissez **[!UICONTROL Cart Price Rule]** to `Any`.
      - Pour inclure uniquement les activités liées à une règle de prix spécifique, définissez **[!UICONTROL Cart Price Rule]** to `Specified` et sélectionnez la règle de prix du panier dans la liste.

1. Une fois prêt à exécuter le rapport, cliquez sur **[!UICONTROL Show Report]**.

   Le rapport s’affiche au bas de la page.

### Options de filtre

| Champ | Description |
|--- |--- |
| [!UICONTROL Date Used] | Identifie le champ date utilisé comme base du rapport. Options :<br/>**[!UICONTROL Order Created]**: génère le rapport en fonction de la date à laquelle la commande a été passée par le client. Pour vous assurer que les données les plus récentes sont incluses, cliquez sur le lien contenu dans le message pour actualiser les statistiques.<br/>**[!UICONTROL Order Updated]**: génère le rapport en fonction de la date de la dernière mise à jour des commandes. Ce rapport utilise des données en temps réel et ne nécessite pas d’actualisation des statistiques. |
| [!UICONTROL Period] | Détermine le type de période utilisé pour le rapport. Options : `Day` / `Month` / `Year` |
| [!UICONTROL From] | Indique la première date de la plage de données de commande incluse dans le rapport. |
| [!UICONTROL To] | Indique la dernière date de la plage de données de commande incluse dans le rapport. |
| [!UICONTROL Order Status] | Filtre le rapport par état de commande. Le rapport peut être généré pour toutes les commandes ou peut être limité à un état de commande spécifique. Options : <br/>**[!UICONTROL Any]**: inclut toutes les commandes, quel que soit leur état.<br/>**[!UICONTROL Specified]**: inclut uniquement les commandes avec le statut spécifié. Les commandes annulées ne sont pas incluses dans le rapport. |
| [!UICONTROL Empty Rows] | Détermine si le rapport contient des lignes de données vides qui peuvent être récupérées. Options : `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Détermine les promotions de coupons qui sont incluses dans le rapport. Options :<br/>**[!UICONTROL Any]**: inclut les informations de commande pour toute promotion de coupon utilisée au cours de la période spécifiée.<br/>**[!UICONTROL Specified]**: inclut uniquement les informations de commande pour la promotion de coupon sélectionnée au cours de la période spécifiée. |

{style="table-layout:auto"}

### Colonnes de rapport

| Colonne | Description |
|--- |--- |
| [!UICONTROL Interval] | Indique la période d’utilisation des coupons à inclure dans le rapport. L’intervalle peut être un jour, un mois, une année ou une plage de dates spécifique. La date d’intervalle est formatée comme dans les exemples suivants, selon la valeur définie dans **[!UICONTROL Period]** paramètre :<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | Code de remise saisi par les clients dans le panier pour recevoir la remise. |
| [!UICONTROL Price Rule] | Nom de la règle de prix associée au coupon. |
| [!UICONTROL Uses] | Nombre de fois où le coupon a été utilisé au cours de la période spécifiée pour le rapport. |
| [!UICONTROL Sales Subtotal] | Sous-total projeté de toutes les commandes qui ont été passées avec le coupon. <br/>Le sous-total des ventes représente le sous-total agrégé de toutes les commandes admissibles et inclut `Pending` commandes ventes qui ne sont pas encore facturées. |
| [!UICONTROL Sales Discount] | Montant de remise prévu de toutes les commandes passées avec le coupon. <br/>La remise représente le montant de remise agrégé de toutes les commandes admissibles et inclut `Pending` commandes ventes qui ne sont pas encore facturées. |
| [!UICONTROL Sales Total] | Total général estimé de toutes les commandes passées avec le coupon. Le Total des ventes comprend les frais d’expédition et de gestion, moins le montant de remise. <br/>Le Total des ventes représente le total général agrégé de toutes les commandes admissibles et inclut `Pending` commandes ventes qui ne sont pas encore facturées. La valeur inclut le sous-total plus les frais d’expédition et de gestion, moins la remise, plus la taxe. <br/> Calculé par : `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Sous-total agrégé de toutes les commandes facturées qui ont utilisé le coupon. |
| [!UICONTROL Discount] | Remise agrégée de toutes les commandes facturées qui ont utilisé le coupon. |
| [!UICONTROL Total] | Total de la commande agrégé de toutes les commandes facturées qui ont utilisé le coupon. |

{style="table-layout:auto"}
