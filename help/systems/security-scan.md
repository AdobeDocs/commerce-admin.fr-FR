---
title: Analyse de sécurité
description: Découvrez comment exécuter une analyse de sécurité améliorée et surveiller chacun de vos sites Adobe Commerce et Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Analyse de sécurité

L’analyse de sécurité améliorée vous permet de surveiller chacun de vos sites Adobe Commerce et Magento Open Sources, y compris PWA, pour détecter les risques de sécurité connus et les logiciels malveillants, ainsi que de recevoir des mises à jour de correctifs et des notifications de sécurité.

- Découvrez l’état de sécurité en temps réel de votre boutique.
- Recevez des suggestions en fonction des bonnes pratiques pour résoudre les problèmes.
- Planifiez l’analyse de sécurité pour qu’elle s’exécute toutes les semaines, tous les jours ou à la demande.
- Exécutez plus de 21 000 tests de sécurité pour identifier les logiciels malveillants potentiels.
- Accédez aux rapports de sécurité historiques qui effectuent le suivi et le suivi de la progression de vos sites.
- Accédez au rapport d’analyse qui affiche les vérifications réussies et en échec, avec toutes les actions recommandées.

L’outil d’analyse de sécurité est disponible gratuitement depuis le tableau de bord de votre [compte Commerce/Magento](../getting-started/commerce-account-create.md). Pour obtenir des informations techniques, reportez-vous à la section [Configuration de l’outil d’analyse de sécurité](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) du _Guide d’infrastructure de Commerce on Cloud_.

![Outil d’analyse de sécurité](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Exécution d’une analyse de sécurité

1. Sur la page d’accueil de Commerce, connectez-vous à votre [compte Commerce/Magento](../getting-started/commerce-account-create.md).

1. Examinez et acceptez les conditions d’utilisation de l’outil d’analyse de sécurité.

   - Dans le panneau de gauche, choisissez **[!UICONTROL Security Scan]**.
   - Cliquez sur **[!UICONTROL Go to Security Scan]**.
   - Lisez le **[!UICONTROL Terms and Conditions]**.
   - Cliquez sur **[!UICONTROL Agree]** pour continuer.

1. Sur la page _[!UICONTROL Monitored Websites]_, cliquez sur **[!UICONTROL +Add Site]**.

   Si vous disposez de plusieurs sites avec des domaines différents, configurez une analyse distincte pour chaque domaine.

   ![Sites surveillés](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Pour vérifier que vous êtes propriétaire du domaine du site en ajoutant un code de confirmation, effectuez l’une des opérations suivantes :

   **Commerce storefront** :

   - Saisissez les **[!UICONTROL Site URL]** et **[!UICONTROL Site Name]**.
   - Cliquez sur **[!UICONTROL Generate Confirmation Code]**.
   - Cliquez sur **Copier** pour copier votre code de confirmation dans le Presse-papiers.

     ![Générer un code de confirmation](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Connectez-vous à l’administrateur de votre boutique en tant qu’utilisateur disposant de droits d’administrateur complets et procédez comme suit :

      - Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Recherchez votre site dans la liste, puis cliquez sur **[!UICONTROL Edit]**.
      - Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL HTML Head]** .
      - Faites défiler l’écran jusqu’à **[!UICONTROL Scripts and Style Sheets]** et cliquez dans la zone de texte à la fin d’un code existant, puis collez le code de confirmation dans la zone de texte.

        ![Scripts et feuilles de style](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Configuration]**.

   **PWA storefront** :

   - Saisissez les **[!UICONTROL Site URL]** et **[!UICONTROL Site Name]**.

   - Pour **[!UICONTROL Confirmation Code]**, choisissez l’option `META Tag`, puis cliquez sur **[!UICONTROL Generate Code]**.

   - Cliquez sur **[!UICONTROL Copy]** pour copier le code de confirmation généré META Tag dans le presse-papiers.

     ![Générer un code de confirmation](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Accédez au répertoire du projet storefront PWA Studio et procédez comme suit :

      - Dans le répertoire du projet du PWA Studio, accédez à `packages > venia-concept > template.html`.
      - Ajoutez le code de confirmation copié (la balise META générée) à l’en-tête de l’HTML et enregistrez les modifications.

        ![Copier le code de confirmation](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Revenez à l’interface de ligne de commande du PWA Studio et utilisez yarn pour installer les dépendances du projet et exécuter la commande de génération du projet.

        ```sh
        yarn install &&
        yarn build
        ```

      - *Dans votre projet cloud*, créez un dossier `pwa` et copiez le contenu dans le dossier `dist` de votre projet storefront.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Utilisez l’outil d’interface de ligne de commande Git pour organiser, valider et transmettre ces modifications à votre projet Cloud.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Une fois le processus de création terminé, les modifications sont déployées vers l’interface de votre boutique de PWA.

1. Revenez à la page _[!UICONTROL Security Scan]_&#x200B;de votre compte Commerce et cliquez sur **[!UICONTROL Verify Confirmation Code]**&#x200B;pour établir la propriété du domaine.

1. Après une confirmation réussie, configurez les options **[!UICONTROL Set Automatic Security Scan]** pour l’un des types suivants :

   **Analyser hebdomadaire (recommandé)** :

   - Sélectionnez les **[!UICONTROL Week Day]**, **[!UICONTROL Time]** et **[!UICONTROL Time Zone]** que l&#39;analyse doit avoir lieu chaque semaine.
   - Par défaut, l’analyse doit commencer chaque semaine à minuit le samedi, en UTC, et se poursuivre jusqu’au début du dimanche.

     ![Analyser hebdomadaire](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Analyser quotidiennement** :

   - Sélectionnez les **[!UICONTROL Time]** et **[!UICONTROL Time Zone]** que l&#39;analyse doit avoir lieu chaque jour.
   - Par défaut, l’analyse est planifiée tous les jours à minuit (UTC).

     ![Analyser quotidiennement](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Saisissez le **[!UICONTROL Email Address]** où vous souhaitez recevoir les notifications des analyses terminées et des mises à jour de sécurité.

   ![Adresse de courriel](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Submit]**.

   Une fois la propriété du domaine vérifiée, le site apparaît dans la liste Sites web surveillés de votre compte Commerce.

1. Si vous disposez de plusieurs sites web avec des domaines différents, répétez cette procédure pour configurer une analyse de sécurité pour chacun d’eux.
