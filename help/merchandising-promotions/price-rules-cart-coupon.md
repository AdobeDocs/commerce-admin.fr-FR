---
title: Codes de coupon
description: Découvrez comment utiliser des codes de coupons avec des règles de prix de panier pour appliquer une remise lorsqu’un ensemble de conditions est rempli.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 9ba2b4f7847559e2c59c7bec3b87781c12270712
workflow-type: tm+mt
source-wordcount: '1922'
ht-degree: 0%

---

# Codes de coupon

Les codes promotionnels sont utilisés avec les [règles de prix de panier](price-rules-cart.md) pour appliquer une remise lorsqu’un ensemble de conditions est rempli. Par exemple, un code coupon peut être créé pour un groupe de clients spécifique ou pour toute personne qui effectue un achat dépassant un certain montant. Pour appliquer le coupon à un achat, le client peut saisir le code du coupon dans le panier ou éventuellement à la caisse de votre magasin _physique_. Voici quelques façons d’utiliser les coupons dans votre boutique :

- Envoyer les coupons par e-mail aux clients
- Produire des coupons imprimés
- Créer des coupons en magasin pour les utilisateurs mobiles

Les codes promotionnels peuvent être envoyés par e-mail ou inclus dans des newsletters, des catalogues et des publicités. La liste des codes de coupon peut être exportée et envoyée à un imprimeur. Vous pouvez également créer des coupons en magasin avec un code de réponse rapide que les acheteurs peuvent numériser avec leur téléphone intelligent. Le code QR peut renvoyer vers une page de votre site contenant plus d’informations sur la promotion.

Depuis Commerce 2.4.7, les acheteurs peuvent appliquer plusieurs coupons à un panier. Les commerçants peuvent également appliquer plusieurs coupons à l&#39;aide de l&#39;aide à l&#39;achat.

>[!NOTE]
>
>Les règles de prix de panier ayant la même priorité n’entraînent pas de remise combinée. Chaque règle (coupon) est appliquée séparément aux produits correspondants, un par un, en fonction de l’identifiant de règle de prix de panier dans la base de données. Pour contrôler l’ordre dans lequel les remises sont appliquées, Adobe recommande de définir une priorité différente pour chaque règle de prix de panier ajoutée.

## Configuration des codes coupon

>[!BEGINSHADEBOX]

Par défaut, Commerce prend en charge deux méthodes de création de codes de coupon :

1. Création d’un code de coupon spécifique unique
1. Génération de plusieurs codes de coupon _aléatoires_

Si vous avez déjà une liste de codes coupon que vous souhaitez importer et associer à une règle de prix de panier, vous devez envisager d’utiliser une extension du [Commerce Marketplace](https://marketplace.magento.com/).

>[!ENDSHADEBOX]

La longueur et le format des codes coupon générés automatiquement sont contrôlés par la configuration. Les caractères peuvent être définis sur tous les nombres, toutes les lettres ou une combinaison de ces éléments. Vous pouvez insérer un tiret à intervalles réguliers pour faciliter la lecture et ajouter un préfixe et un suffixe pour associer le code à une campagne ou une initiative spécifique.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Promotions]**.

   ![Configuration des clients - codes de coupon spécifiques générés automatiquement](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Développez la section **[!UICONTROL Auto Generated Specific Coupon Codes]** .

   ![Configuration des clients - codes de coupon spécifiques générés automatiquement](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Saisissez le **[!UICONTROL Code Length]**, y compris le préfixe, le suffixe et les séparateurs.

1. Définissez la **[!UICONTROL Code Format]** sur l’une des options suivantes :

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. Par **[!UICONTROL Code Prefix]**, saisissez la valeur qui doit apparaître au début de tous les codes coupon.

1. Par **[!UICONTROL Code Suffix]**, saisissez la valeur qui doit apparaître à la fin de tous les codes coupon.

1. Par **[!UICONTROL Dash Every X Characters]**, saisissez le nombre de caractères compris entre chaque tiret.

   Les codes coupon avec des tirets différents sont considérés comme des codes différents, même si les nombres sont identiques.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Créer des coupons

>[!NOTE]
>
>[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} Avant de créer des coupons, utilisez la commande `bin/magento cron:run` pour vérifier que cron est en cours d’exécution. Voir [Exécuter cron à partir de la ligne de commande](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) dans le _Guide de configuration_ pour plus d’informations.

### Méthode 1 : créer un coupon spécifique

1. Suivez les instructions pour créer une [ règle de prix de panier ](price-rules-cart.md).

1. Dans la section **[!UICONTROL Rule Information]**, définissez **[!UICONTROL Coupon]** sur `Specific Coupon`.

1. Saisissez un **[!UICONTROL Coupon Code]** à utiliser avec la promotion.

   Le format du code (numérique, alphanumérique ou alphabétique) est déterminé par la [ configuration ](#configure-coupon-codes).

1. Pour limiter le nombre de fois où le coupon peut être utilisé, procédez comme suit :

   - Saisissez le nombre de **[!UICONTROL Uses per Coupon]**.
   - Saisissez le nombre de **[!UICONTROL Uses per Customer]**.

   Pour une utilisation illimitée, laissez ces champs vides.

   ![Règle de prix du panier - Informations sur le coupon](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si plusieurs clients utilisent simultanément le même coupon en même temps, il est possible que la limite d’utilisation définie soit dépassée en raison du retard du traitement des coupons.

1. Pour rendre le coupon valide pour une période donnée, procédez comme suit :

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Complétez les dates **De** et **À**. Pour sélectionner la date, cliquez sur l’icône **Calendrier** (![icône Calendrier](../assets/icon-calendar.png)) en regard de chaque champ. Si vous laissez la période vide, la règle n’expire pas.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Effectuez l’une des opérations suivantes :

     **Option 1 :** Planifier une nouvelle mise à jour

      - Cliquez sur **[!UICONTROL Schedule New Update]** dans le coin supérieur droit de la page.

        ![Planifier la mise à jour](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Saisissez les **[!UICONTROL Update Name]** et les **[!UICONTROL Description]**.

      - Sélectionnez la **Date de début** et **[!UICONTROL End Date]** dans le Calendrier ( ![icône Calendrier](../assets/icon-calendar.png) ). Si vous laissez la période vide, la règle n’expire pas.

      - Cliquez ensuite sur **[!UICONTROL Save]**.

        ![Règle de prix du panier - modification planifiée](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Option 2 :** Affecter à une mise à jour existante :

      - Sélectionnez **[!UICONTROL Assign to Another Update]**.

      - Recherchez la mise à jour dans la liste, puis cliquez sur **[!UICONTROL Select]**.

1. Renseignez la [règle de prix de panier](price-rules-cart.md) si nécessaire.

### Méthode 2 : générer un lot de coupons

La génération des coupons de remise est une opération asynchrone, qui s’exécute en arrière-plan afin que vous puissiez continuer à travailler dans l’administration sans attendre que l’opération se termine. Le système affiche un message lorsque la tâche est terminée.

1. Suivez les instructions pour créer une [ règle de prix de panier ](price-rules-cart.md).

1. Sous **[!UICONTROL Coupon Code]**, cochez la case **[!UICONTROL Use Auto Generation]** .

1. Pour limiter le nombre de fois où chaque client peut utiliser le coupon, saisissez le nombre de **[!UICONTROL Uses per Customer]**.

   ![Règle de prix du panier - générer des coupons numérotés automatiquement](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si plusieurs clients utilisent simultanément le même coupon en même temps, il est possible que la limite d’utilisation définie soit dépassée en raison du retard du traitement des coupons.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Manage Coupon Codes]**, puis procédez comme suit :

   ![Règle de prix du panier - Gérer les codes coupon](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Par **[!UICONTROL Coupons Qty]**, saisissez le nombre de coupons que vous souhaitez générer.

   - Saisissez le **[!UICONTROL Code Length]**, sans inclure le préfixe, le suffixe ou les séparateurs.

   - Définissez la **[!UICONTROL Code Format]** sur l’une des options suivantes :

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Facultatif) Saisissez un **[!UICONTROL Code Prefix]** à ajouter au début du code.

   - (Facultatif) Saisissez un **[!UICONTROL Code Suffix]** à ajouter à la fin du code.

   - (Facultatif) Par **[!UICONTROL Dash Every X Characters]**, saisissez le nombre de caractères entre chaque tiret. Par exemple, si le code comporte 12 caractères et qu’il y a un tiret tous les quatre caractères, il ressemble à `xxxx-xxxx-xxxx`. Les tirets facilitent la lecture et la saisie des codes.

1. Cliquez ensuite sur **[!UICONTROL Generate]**.

   Le système affiche des `Message is added to queue, wait to get your coupons soon`.

   Une fois la tâche cron terminée, la liste des codes générés s’affiche.

   | Champ | Description |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Code de coupon unique créé et pouvant être utilisé pour la réception de conditions spéciales. |
   | [!UICONTROL Created] | Date de création du code coupon. |
   | [!UICONTROL Used] | Indique si le coupon a été utilisé. |
   | [!UICONTROL Times Used] | Indique le nombre de fois où le code coupon a été utilisé. |

   {style="table-layout:auto"}

Vous pouvez exporter des codes de coupon dans un fichier CSV ou XML Excel en sélectionnant le format de fichier et en cliquant sur **[!UICONTROL Export]**.

Pour supprimer des codes coupon, sélectionnez un ou plusieurs codes dans la liste. Sélectionnez `Delete` dans le sélecteur de **[!UICONTROL Actions]**, puis cliquez sur **[!UICONTROL Submit]**.

## Rapport Coupons

Le rapport _Coupons_ agrège les données de chaque coupon utilisé au cours d’une période spécifique. Comme les coupons sont appliqués à partir du panier, le rapport inclut les données de tous les coupons échangés, quel que soit le [statut de la commande](../stores-purchase/order-status.md). Par conséquent, le rapport peut inclure à la fois les totaux prévus et les totaux réels. Le rapport peut être filtré pour une vue de magasin, une période, un statut de commande et une règle de prix de panier spécifiques.

Dans l’exemple suivant, le code de coupon « H20 » a été utilisé par deux clients. Une des commandes est facturée, mais l&#39;autre est toujours _en attente_. Les colonnes Sous-total ventes prévisionnel, Remise vente et Total vente affichent les montants agrégés des deux commandes, mais seule la commande facturée réelle apparaît dans les colonnes Sous-total, Remise et Total. Chaque ligne du rapport représente une promotion de coupon unique.

![Rapport Coupons](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Exécuter le rapport

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Si vous disposez de plusieurs vues de magasin, définissez **[!DNL Store View]** dans le coin supérieur gauche pour établir la portée du rapport.

1. Pour actualiser les ventes [statistiques](../getting-started/sales-reports.md#refresh-statistics) pour la journée, cliquez sur le message _Dernière mise à jour_ en haut de l’espace de travail.

   Cliquez ensuite pour sélectionner la case à cocher **[!UICONTROL Coupons]** et cliquez sur **[!UICONTROL Refresh]**.

   ![Rapport Coupons - Statistiques de renouvellement](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Pour filtrer les données, procédez comme suit :

   ![Rapport Coupon - Filtres](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Date Used]** sur l’une des options suivantes :

      - `Order Created`
      - `Order Updated`

     Le rapport _Commande mise à jour_ est créé en temps réel et ne nécessite pas d&#39;actualisation.

   - Pour définir la période couverte par le rapport, définissez **[!UICONTROL Period]** sur l’une des valeurs suivantes :

      - `Day`
      - `Month`
      - `Year`

   - Pour définir la période de l&#39;état, entrez les dates **De** et **À** au format M/J/AA.

   - Pour imprimer un état pour un [statut de commande](../stores-purchase/order-status.md) spécifique, définissez **[!UICONTROL Order Status]** sur `Specified` et choisissez le statut de la commande dans la liste.

   - Pour omettre des lignes sans données dans le rapport, définissez **[!UICONTROL Empty Rows]** sur `No`.

   - Pour définir l’activité de coupon incluse dans le rapport, effectuez l’une des opérations suivantes :

      - Pour inclure toutes les activités de coupon de toutes les règles de prix, définissez **[!UICONTROL Cart Price Rule]** sur `Any`.
      - Pour inclure uniquement l’activité liée à une règle de prix spécifique, définissez **[!UICONTROL Cart Price Rule]** sur `Specified` et sélectionnez la règle de prix de panier dans la liste.

1. Une fois prêt à exécuter le rapport, cliquez sur **[!UICONTROL Show Report]**.

   Le rapport s’affiche au bas de la page.

### Options de filtre

| Champ | Description |
|--- |--- |
| [!UICONTROL Date Used] | Identifie le champ de date utilisé comme base du rapport. Options : <br/>**[!UICONTROL Order Created]**&#x200B;génère l&#39;état en fonction de la date à laquelle la commande a été passée par le client. Pour vous assurer que les données les plus récentes sont incluses, cliquez sur le lien dans le message pour actualiser les statistiques.<br/>**[!UICONTROL Order Updated]** : génère l&#39;état en fonction de la date de la dernière mise à jour des commandes. Ce rapport utilise des données en temps réel et ne nécessite pas d’actualisation des statistiques. |
| [!UICONTROL Period] | Détermine le type de période utilisé pour le rapport. Options : `Day` / `Month` / `Year` |
| [!UICONTROL From] | Indique la première date de la plage de données de commande incluse dans l&#39;état. |
| [!UICONTROL To] | Indique la dernière date de la plage de données de commande incluse dans l&#39;état. |
| [!UICONTROL Order Status] | Filtre le rapport par statut de commande. L&#39;état peut être généré pour toutes les commandes ou peut être limité à un statut de commande spécifique. Options : <br/>**[!UICONTROL Any]**: inclut toutes les commandes, quel que soit leur statut.<br/>**[!UICONTROL Specified]** : inclut uniquement les commandes avec le statut spécifié. Les commandes annulées ne sont pas incluses dans l&#39;état. |
| [!UICONTROL Empty Rows] | Détermine si le rapport inclut des lignes de données vides qui pourraient être récupérées. Options : `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Détermine les promotions de coupon incluses dans le rapport. Options : <br/>**[!UICONTROL Any]**: inclut des informations sur la commande pour toute promotion de coupon utilisée pendant la période spécifiée.<br/>**[!UICONTROL Specified]** : inclut uniquement les informations de commande pour la promotion de coupon sélectionnée au cours de la période spécifiée. |

{style="table-layout:auto"}

### Colonnes du rapport

| Colonne | Description |
|--- |--- |
| [!UICONTROL Interval] | Indique la période d’utilisation des coupons à inclure dans le rapport. L’intervalle peut être un jour, un mois, une année spécifique ou une plage de dates spécifique. La date de l’intervalle est formatée comme dans les exemples suivants, en fonction de la valeur définie dans **[!UICONTROL Period]** paramètre :<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | Code remise saisi par les clients dans le panier pour recevoir la remise. |
| [!UICONTROL Price Rule] | Nom de la règle de prix associée au coupon. |
| [!UICONTROL Uses] | Nombre de fois où le coupon a été utilisé pendant la période spécifiée pour le rapport. |
| [!UICONTROL Sales Subtotal] | Sous-total prévisionnel de toutes les commandes passées avec le coupon. <br/>Le sous-total ventes représente le sous-total agrégé de toutes les commandes admissibles et inclut `Pending` commandes client qui ne sont pas encore facturées. |
| [!UICONTROL Sales Discount] | Montant de remise prévu pour toutes les commandes passées avec le coupon. <br/>La remise représente le montant de remise agrégé de toutes les commandes admissibles et inclut `Pending` commandes client qui ne sont pas encore facturées. |
| [!UICONTROL Sales Total] | Total général prévisionnel de toutes les commandes passées avec le coupon. Le total des ventes inclut tous les frais d’expédition et de manutention, moins le montant de la remise. <br/>Le total des ventes représente le montant total global agrégé de toutes les commandes admissibles et inclut `Pending` commandes client qui ne sont pas encore facturées. La valeur inclut le sous-total plus les frais d&#39;expédition et de manutention, moins la remise, plus les taxes. <br/> Calculé par : `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Sous-total agrégé de toutes les commandes facturées qui ont utilisé le coupon. |
| [!UICONTROL Discount] | Remise agrégée de toutes les commandes facturées qui ont utilisé le coupon. |
| [!UICONTROL Total] | Total de commande agrégé de toutes les commandes facturées qui ont utilisé le coupon. |

{style="table-layout:auto"}
