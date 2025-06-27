---
title: Analyse de sécurité
description: Découvrez comment exécuter une analyse de sécurité renforcée et surveiller chacun de vos sites Adobe Commerce et Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 8e634311cd84a9e797a36218c29abb4699d72835
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Analyse de sécurité

L&#39;analyse de sécurité améliorée vous permet de surveiller chacun de vos sites Adobe Commerce et Magento Open Source, y compris PWA, pour détecter les risques de sécurité connus et les programmes malveillants, et de recevoir des mises à jour de correctifs et des notifications de sécurité.

- Obtenez insight pour obtenir le statut de sécurité en temps réel de votre boutique.
- Recevez des suggestions basées sur les bonnes pratiques pour vous aider à résoudre les problèmes.
- Planifiez une analyse de sécurité hebdomadaire, quotidienne ou à la demande.
- Exécutez plus de 21 000 tests de sécurité pour identifier les logiciels malveillants potentiels.
- Accédez aux rapports de sécurité historiques qui suivent et surveillent la progression de vos sites.
- Accédez au rapport d’analyse qui indique les vérifications réussies et ayant échoué, avec les actions recommandées.

L&#39;outil Analyse de sécurité est disponible gratuitement depuis le tableau de bord de votre compte [Commerce/Magento](../getting-started/commerce-account-create.md). Pour obtenir des informations techniques, consultez [Configuration de l’outil d’analyse de sécurité](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html?lang=fr#set-up-the-security-scan-tool) dans le _Guide de Commerce sur les infrastructures cloud_.

![Outil d’analyse de sécurité](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Exécuter une analyse de sécurité

1. Connectez-vous à votre compte [Commerce/Magento](../getting-started/commerce-account-create.md).

1. Dans le volet de gauche, cliquez sur l’onglet [!UICONTROL Security Scan] . (Si nécessaire, passez en revue et acceptez les conditions mises à jour pour l&#39;utilisation de l&#39;outil Analyse de sécurité.)

   - Dans le panneau de gauche, choisissez **[!UICONTROL Security Scan]**.
   - Cliquez sur **[!UICONTROL Go to Security Scan]**.
   - Lisez le **[!UICONTROL Terms and Conditions]**.
   - Cliquez sur **[!UICONTROL Agree]** pour continuer.

1. Sur la page _[!UICONTROL Monitored Websites]_, cliquez sur **[!UICONTROL +Add Site]**.

   Si vous disposez de plusieurs sites avec des domaines différents, configurez une analyse distincte pour chaque domaine.

   ![Sites surveillés](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Pour vérifier que vous êtes propriétaire du domaine du site en ajoutant un code de confirmation, effectuez l’une des opérations suivantes :

   **Commerce storefront**:

   - Saisissez les **[!UICONTROL Site URL]** et les **[!UICONTROL Site Name]**.
   - Cliquez sur **[!UICONTROL Generate Confirmation Code]**.
   - Cliquez sur **Copier** pour copier votre code de confirmation dans le presse-papiers.

     ![Générer le code de confirmation](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Connectez-vous à l’administrateur de votre boutique en tant qu’utilisateur disposant de droits d’administrateur complets et procédez comme suit :

      - Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Recherchez votre site dans la liste, puis cliquez sur **[!UICONTROL Edit]**.
      - Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL HTML Head]** .
      - Faites défiler jusqu’à **[!UICONTROL Scripts and Style Sheets]** et cliquez dans la zone de texte à la fin de tout code existant, puis collez le code de confirmation dans la zone de texte.

        ![ Scripts et feuilles de style ](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Cliquez ensuite sur **[!UICONTROL Save Configuration]**.

   **PWA storefront**:

   - Saisissez les **[!UICONTROL Site URL]** et les **[!UICONTROL Site Name]**.

   - Par **[!UICONTROL Confirmation Code]**, choisissez l’option `META Tag` , puis cliquez sur **[!UICONTROL Generate Code]**.

   - Cliquez sur **[!UICONTROL Copy]** pour copier la balise META du code de confirmation générée dans le presse-papiers.

     ![Générer le code de confirmation](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Accédez au répertoire du projet de storefront PWA Studio et procédez comme suit :

      - Dans le répertoire du projet PWA Studio, accédez à `packages > venia-concept > template.html`.
      - Ajoutez le code de confirmation copié (la balise META générée) à l’en-tête HTML et enregistrez les modifications.

        ![Copier le code de confirmation](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Revenez à l’interface de ligne de commande PWA Studio et utilisez yarn pour installer les dépendances de projet et exécuter la commande de création de projet.

        ```sh
        yarn install &&
        yarn build
        ```

      - *Dans votre projet cloud* créez un dossier `pwa` et copiez le contenu dans le dossier `dist` de votre projet de storefront.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Utilisez l’outil d’interface de ligne de commande Git pour évaluer, valider et pousser ces modifications vers votre projet cloud.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Une fois le processus de création terminé, les modifications seront déployées sur votre vitrine PWA.

1. Revenez à la page _[!UICONTROL Security Scan]_&#x200B;de votre compte Commerce, puis cliquez sur **[!UICONTROL Verify Confirmation Code]**&#x200B;pour établir la propriété du domaine.

1. Après une confirmation réussie, configurez les options de **[!UICONTROL Set Automatic Security Scan]** pour l’un des types suivants :

   **Scan Weekly (recommandé)** :

   - Choisissez les **[!UICONTROL Week Day]**, **[!UICONTROL Time]** et **[!UICONTROL Time Zone]** que l&#39;analyse doit avoir lieu chaque semaine.
   - Par défaut, l’analyse est planifiée pour commencer chaque semaine à minuit, le samedi UTC, et se poursuivre jusqu’au début du dimanche.

     ![Scan Weekly](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Scan Daily** :

   - Choisissez le **[!UICONTROL Time]** et **[!UICONTROL Time Zone]** que l&#39;analyse doit avoir lieu tous les jours.
   - Par défaut, l’analyse est planifiée pour commencer chaque jour à minuit (UTC).

     ![Scan Daily](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Saisissez l&#39;**[!UICONTROL Email Address]** où vous souhaitez recevoir des notifications d&#39;analyses terminées et de mises à jour de sécurité.

   ![Adresse électronique](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Submit]**.

   Une fois la propriété du domaine vérifiée, le site apparaît dans la liste Sites web surveillés de votre compte Commerce.

1. Si vous disposez de plusieurs sites web avec des domaines différents, répétez cette procédure pour configurer une analyse de sécurité pour chacun.

## Supprimer une analyse de sécurité

>[!NOTE]
>
>Seule la personne qui a configuré l&#39;analyse à l&#39;origine peut la supprimer du compte. S’ils ne se sont pas connectés à leur [compte](https://account.magento.com) depuis août 2022, ils doivent d’abord s’assurer qu’ils se sont [inscrits à un Adobe ID](https://account.magento.com).

**Supprimer une analyse**

1. Connectez-vous au compte [Commerce/Magento](../getting-started/commerce-account-create.md).

1. Dans le panneau de gauche, cliquez sur l’onglet [!UICONTROL Security Scan] . (Si nécessaire, passez en revue et acceptez les conditions mises à jour pour l&#39;utilisation de l&#39;outil Analyse de sécurité.)

   - Cliquez sur **[!UICONTROL Go to Security Scan]**.
   - Lisez le **[!UICONTROL Terms and Conditions]**.
   - Cliquez sur **[!UICONTROL Agree]** pour continuer.

1. Sur la page _[!UICONTROL Monitored Websites]_, recherchez la liste déroulante sous la colonne [!UICONTROL Actions], puis sélectionnez **[!UICONTROL Delete]**&#x200B;pour le ou les sites web appropriés.
