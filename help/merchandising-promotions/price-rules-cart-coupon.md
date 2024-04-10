---
title: Codes de coupon
description: Découvrez comment utiliser des codes de coupons avec des règles de prix de panier pour appliquer une remise lorsqu’un ensemble de conditions est rempli.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 7407df02ca62e36b4dd60dba418eae3e6aa34491
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 0%

---

# Codes de coupon

Les codes coupons sont utilisés avec [règles de prix de panier](price-rules-cart.md) pour appliquer une remise lorsqu&#39;un ensemble de conditions est rempli. Par exemple, un code de coupon peut être créé pour un groupe de clients spécifique ou pour toute personne qui effectue un achat dépassant un certain montant. Pour appliquer le coupon à un achat, le client peut saisir le code de coupon dans le panier, ou éventuellement dans la caisse de votre _brique et mortier_ magasin. Voici quelques façons d’utiliser les coupons dans votre boutique :

- Envoyer les coupons par e-mail aux clients
- Produire des coupons imprimés
- Création de coupons en magasin pour les utilisateurs d’appareils mobiles

Les codes de coupon peuvent être envoyés par e-mail ou inclus dans des newsletters, des catalogues et des publicités. La liste des codes coupon peut être exportée et envoyée à un imprimeur. Vous pouvez également créer des coupons en magasin avec un code de réponse rapide que les acheteurs peuvent numériser avec leur téléphone intelligent. Le code QR peut renvoyer vers une page de votre site contenant plus d’informations sur la promotion.

Depuis Commerce 2.4.7, les acheteurs peuvent appliquer plusieurs coupons à un panier. Les commerçants peuvent également appliquer plusieurs coupons à l&#39;aide de l&#39;aide à l&#39;achat.

## Configuration des codes coupon

La longueur et le format des codes coupon générés automatiquement sont contrôlés par la configuration. Les caractères peuvent être définis sur tous les nombres, toutes les lettres ou une combinaison de ces éléments. Vous pouvez insérer un tiret à intervalles réguliers pour faciliter la lecture et ajouter un préfixe et un suffixe pour associer le code à une campagne ou une initiative spécifique.

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Promotions]**.

   ![Configuration des clients : codes de coupon spécifiques générés automatiquement](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Développer le **[!UICONTROL Auto Generated Specific Coupon Codes]** section.

   ![Configuration des clients : codes de coupon spécifiques générés automatiquement](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Saisir le **[!UICONTROL Code Length]**, y compris le préfixe, le suffixe et les séparateurs.

1. Définir le **[!UICONTROL Code Format]** à l’un des éléments suivants :

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. Pour **[!UICONTROL Code Prefix]**, saisissez la valeur qui doit apparaître au début de tous les codes coupon.

1. Pour **[!UICONTROL Code Suffix]**, saisissez la valeur qui doit apparaître à la fin de tous les codes coupon.

1. Pour **[!UICONTROL Dash Every X Characters]**, saisissez le nombre de caractères compris entre chaque tiret.

   Les codes coupon avec des motifs de tirets différents sont considérés comme des codes différents, même si les nombres sont les mêmes.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Créer des coupons

>[!NOTE]
>
>Avant de créer des coupons, utilisez le `bin/magento cron:run` pour vérifier que cron est en cours d’exécution. Voir [Exécutez cron depuis la ligne de commande](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) dans le _Guide de configuration_ pour plus d’informations.

### Méthode 1 : créer un coupon spécifique

1. Suivez les instructions pour créer un [règle de prix de panier](price-rules-cart.md).

1. Dans le **[!UICONTROL Rule Information]** section, définir **[!UICONTROL Coupon]** vers `Specific Coupon`.

1. Saisir un **[!UICONTROL Coupon Code]** à utiliser avec la promotion.

   Le format du code (numérique, alphanumérique ou alphabétique) est déterminé par l’ [configuration](#configure-coupon-codes).

1. Pour limiter le nombre de fois où le coupon peut être utilisé, procédez comme suit :

   - Saisir le nombre de **[!UICONTROL Uses per Coupon]**.
   - Saisir le nombre de **[!UICONTROL Uses per Customer]**.

   Pour une utilisation illimitée, laissez ces champs vides.

   ![Règle de prix du panier - Informations sur le coupon](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si plusieurs clients et clientes utilisent simultanément le même coupon en même temps, il est possible que la limite d’utilisation définie soit dépassée en raison du retard du traitement du coupon.

1. Pour rendre le coupon valide pour une période donnée, procédez comme suit :

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Effectuez le **De** et **Vers** dates. Pour sélectionner la date, cliquez sur **Calendrier** (![Icône de calendrier](../assets/icon-calendar.png)) en regard de chaque champ. Si vous laissez la période vide, la règle n’expire pas.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Effectuez l’une des opérations suivantes :

     **Option 1 :** Planifier une nouvelle mise à jour

      - Clic **[!UICONTROL Schedule New Update]** dans le coin supérieur droit de la page.

        ![Planifier la mise à jour](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Saisir le **[!UICONTROL Update Name]** et **[!UICONTROL Description]**.

      - Choisir le **Date de début** et **[!UICONTROL End Date]** à partir du Calendrier ( ![Icône de calendrier](../assets/icon-calendar.png) ). Si vous laissez la période vide, la règle n’expire pas.

      - Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

        ![Règle de prix du panier - modification planifiée](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Option 2 :** Affecter à une mise à jour existante :

      - Sélectionner **[!UICONTROL Assign to Another Update]**.

      - Recherchez la mise à jour dans la liste, puis cliquez sur **[!UICONTROL Select]**.

1. Terminer le [règle de prix de panier](price-rules-cart.md) en fonction des besoins.

### Méthode 2 : générer un lot de coupons

La génération des coupons de remise est une opération asynchrone, qui s’exécute en arrière-plan afin que vous puissiez continuer à travailler dans l’administrateur sans attendre la fin de l’opération. Le système affiche un message lorsque la tâche est terminée.

1. Suivez les instructions pour créer un [règle de prix de panier](price-rules-cart.md).

1. Sous **[!UICONTROL Coupon Code]**, sélectionnez le **[!UICONTROL Use Auto Generation]** case à cocher.

1. Pour limiter le nombre de fois où chaque client peut utiliser le coupon, saisissez le nombre de **[!UICONTROL Uses per Customer]**.

   ![Règle de prix du panier : génération de coupons numérotés automatiquement](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si plusieurs clients et clientes utilisent simultanément le même coupon en même temps, il est possible que la limite d’utilisation définie soit dépassée en raison du retard du traitement du coupon.

1. Défilement vers le bas et développement ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Manage Coupon Codes]** et procédez comme suit :

   ![Règle de prix du panier - Gestion des codes coupon](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Pour **[!UICONTROL Coupons Qty]**, saisissez le nombre de coupons que vous souhaitez générer.

   - Saisir le **[!UICONTROL Code Length]**, sans inclure le préfixe, le suffixe ou les séparateurs.

   - Définir le **[!UICONTROL Code Format]** à l’un des éléments suivants :

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Facultatif) Saisissez un **[!UICONTROL Code Prefix]** à ajouter au début du code.

   - (Facultatif) Saisissez un **[!UICONTROL Code Suffix]** à ajouter à la fin du code.

   - (Facultatif) Pour **[!UICONTROL Dash Every X Characters]**, saisissez le nombre de caractères compris entre chaque tiret. Par exemple, si le code comporte 12 caractères et qu’il y a un tiret tous les quatre caractères, il ressemble à ceci : `xxxx-xxxx-xxxx`. Les tirets rendent les codes plus faciles à lire et à saisir.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Generate]**.

   Le système affiche `Message is added to queue, wait to get your coupons soon`.

   Une fois la tâche cron terminée, la liste des codes générés s’affiche.

   | Champ | Description |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Code de coupon unique créé et pouvant être utilisé pour la réception de conditions spéciales. |
   | [!UICONTROL Created] | Date de création du code coupon. |
   | [!UICONTROL Used] | Indique si le coupon a été utilisé. |
   | [!UICONTROL Times Used] | Indique le nombre de fois où le code coupon a été utilisé. |

   {style="table-layout:auto"}

Vous pouvez exporter des codes de coupon vers un fichier CSV ou XML Excel en sélectionnant le format de fichier et en cliquant sur **[!UICONTROL Export]**.

Pour supprimer des codes coupon, sélectionnez un ou plusieurs codes dans la liste. Sélectionner `Delete` à partir du **[!UICONTROL Actions]**  sélecteur, puis cliquez sur **[!UICONTROL Submit]**.

>[!NOTE]
>
>Bien que Commerce permette de configurer plusieurs codes de coupon, un client ne peut utiliser qu’un seul code de coupon dans le panier. Pour permettre l’utilisation simultanée de plusieurs codes de bon dans le panier, vous pouvez utiliser une extension correspondante à partir de . [Commerce Marketplace](https://marketplace.magento.com/).

## Rapport Coupons

Le _Coupons_ Le rapport agrège les données de chaque coupon utilisé au cours d’une période spécifique. Comme les coupons sont appliqués à partir du panier, le rapport inclut les données de tous les coupons échangés, quels que soient [état de la commande](../stores-purchase/order-status.md). Par conséquent, le rapport peut inclure à la fois les totaux prévus et les totaux réels. Le rapport peut être filtré pour une vue de magasin, une période, un statut de commande et une règle de prix de panier spécifiques.

Dans l’exemple suivant, le code de coupon « H20 » a été utilisé par deux clientes et clients. L&#39;une des commandes est facturée, mais l&#39;autre l&#39;est toujours _en attente_. Les colonnes Sous-total ventes prévisionnel, Remise vente et Total ventes affichent les montants agrégés des deux commandes, mais seule la commande facturée réelle apparaît dans les colonnes Sous-total, Remise et Total. Chaque ligne du rapport représente une promotion de coupon unique.

![Rapport Coupons](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Exécuter le rapport

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Si vous disposez de plusieurs vues de magasin, définissez **[!DNL Store View]** dans le coin supérieur gauche pour établir la portée du rapport.

1. Pour actualiser les ventes [statistiques](../getting-started/sales-reports.md#refresh-statistics) pour la journée, cliquez sur _Dernière mise à jour_ message en haut de l’espace de travail.

   Cliquez ensuite pour sélectionner le **[!UICONTROL Coupons]** case à cocher et clic **[!UICONTROL Refresh]**.

   ![Rapport Coupons - Statistiques d’actualisation](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Pour filtrer les données, procédez comme suit :

   ![Rapport Coupon - Filtres](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Date Used]** à l’un des éléments suivants :

      - `Order Created`
      - `Order Updated`

     Le _Commande mise à jour_ Le rapport est créé en temps réel et ne nécessite pas d’actualisation.

   - Pour définir la période couverte par le rapport, définissez **[!UICONTROL Period]** à l’un des éléments suivants :

      - `Day`
      - `Month`
      - `Year`

   - Pour définir la période de l&#39;état, saisissez **De** et **Vers** dates au format M/J/AA.

   - Pour imprimer un rapport pour un rapport spécifique [état de la commande](../stores-purchase/order-status.md), set **[!UICONTROL Order Status]** vers `Specified` et choisissez le statut de la commande dans la liste.

   - Pour omettre les lignes sans données du rapport, définissez **[!UICONTROL Empty Rows]** vers `No`.

   - Pour définir l’activité de coupon incluse dans le rapport, effectuez l’une des opérations suivantes :

      - Pour inclure toutes les activités de coupon de toutes les règles de prix, définissez **[!UICONTROL Cart Price Rule]** vers `Any`.
      - Pour inclure uniquement l’activité liée à une règle de prix spécifique, définissez **[!UICONTROL Cart Price Rule]** vers `Specified` et sélectionnez la règle prix du panier dans la liste.

1. Une fois prêt à exécuter le rapport, cliquez sur **[!UICONTROL Show Report]**.

   Le rapport s’affiche au bas de la page.

### Options de filtre

| Champ | Description |
|--- |--- |
| [!UICONTROL Date Used] | Identifie le champ de date utilisé comme base du rapport. Options :<br/>**[!UICONTROL Order Created]**: génère l&#39;état en fonction de la date à laquelle la commande a été passée par le client. Pour vous assurer que les données les plus récentes sont incluses, cliquez sur le lien dans le message pour actualiser les statistiques.<br/>**[!UICONTROL Order Updated]**: génère l’état en fonction de la date de la dernière mise à jour des commandes. Ce rapport utilise des données en temps réel et ne nécessite pas d’actualisation des statistiques. |
| [!UICONTROL Period] | Détermine le type de période utilisé pour le rapport. Options : `Day` / `Month` / `Year` |
| [!UICONTROL From] | Indique la première date de la plage de données de commande incluse dans l&#39;état. |
| [!UICONTROL To] | Indique la dernière date de la plage de données de commande incluse dans l&#39;état. |
| [!UICONTROL Order Status] | Filtre le rapport par statut de commande. L&#39;état peut être généré pour toutes les commandes ou peut être limité à un statut de commande spécifique. Options : <br/>**[!UICONTROL Any]**: inclut toutes les commandes, quel que soit leur statut.<br/>**[!UICONTROL Specified]**: inclut uniquement les commandes avec le statut spécifié. Les commandes annulées ne sont pas incluses dans l&#39;état. |
| [!UICONTROL Empty Rows] | Détermine si le rapport inclut des lignes de données vides susceptibles d’être récupérées. Options : `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Détermine les promotions de coupon incluses dans le rapport. Options :<br/>**[!UICONTROL Any]**: inclut les informations de commande pour toute promotion de coupon utilisée au cours de la période spécifiée.<br/>**[!UICONTROL Specified]**: inclut uniquement les informations de commande pour la promotion de coupon sélectionnée au cours de la période spécifiée. |

{style="table-layout:auto"}

### Colonnes du rapport

| Colonne | Description |
|--- |--- |
| [!UICONTROL Interval] | Indique la période d’utilisation des coupons à inclure dans le rapport. L’intervalle peut être un jour, un mois, une année spécifique ou une plage de dates. La date de l’intervalle est formatée comme dans les exemples suivants, en fonction de la valeur définie dans **[!UICONTROL Period]** paramètre :<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | Code remise saisi par les clients dans le panier pour recevoir la remise. |
| [!UICONTROL Price Rule] | Nom de la règle de prix associée au coupon. |
| [!UICONTROL Uses] | Nombre de fois où le coupon a été utilisé pendant la période spécifiée pour le rapport. |
| [!UICONTROL Sales Subtotal] | Sous-total prévisionnel de toutes les commandes passées avec le coupon. <br/>Le sous-total des ventes représente le sous-total agrégé de toutes les commandes admissibles et comprend `Pending` commandes client non encore facturées. |
| [!UICONTROL Sales Discount] | Montant de remise prévu pour toutes les commandes passées avec le coupon. <br/>La remise représente le montant de remise agrégé de toutes les commandes admissibles et comprend `Pending` commandes client non encore facturées. |
| [!UICONTROL Sales Total] | Total général prévisionnel de toutes les commandes passées avec le coupon. Le total des ventes inclut tous les frais d&#39;expédition et de manutention, moins le montant de la remise. <br/>Le total des ventes représente le montant total général agrégé de toutes les commandes admissibles et comprend `Pending` commandes client non encore facturées. La valeur inclut le sous-total plus les frais d&#39;expédition et de manutention, moins la remise, plus les taxes. <br/> Calculé par : `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Sous-total agrégé de toutes les commandes facturées qui ont utilisé le coupon. |
| [!UICONTROL Discount] | Remise agrégée de toutes les commandes facturées qui ont utilisé le coupon. |
| [!UICONTROL Total] | Total de commande agrégé de toutes les commandes facturées qui ont utilisé le coupon. |

{style="table-layout:auto"}
