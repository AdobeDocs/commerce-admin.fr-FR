---
title: Clé de chiffrement
description: Découvrez comment modifier votre propre clé de chiffrement, ce qui doit être fait régulièrement pour améliorer la sécurité.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/jC0eV49rzff4ZZ0idMG4ChWZh80Yz43ZTmZ9CjYFhnk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 0%

---

# Clé de chiffrement

>[!NOTE]
>
>Si vous avez tenté d’effectuer ces étapes et rencontrez des problèmes, reportez-vous à l’article [Dépannage de la rotation de la clé de chiffrement : CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102) de la base de connaissances.

Adobe Commerce et Magento Open Source utilisent une clé de chiffrement pour protéger les mots de passe et d’autres données sensibles. Un algorithme de [!DNL ChaCha20-Poly1305] standard est utilisé avec une clé de 256 bits pour chiffrer toutes les données qui nécessitent un chiffrement. Cela inclut les données de carte de crédit et les mots de passe d’intégration (module de paiement et d’expédition). En outre, un algorithme de hachage sécurisé puissant (SHA-256) est utilisé pour hacher toutes les données qui ne nécessitent pas de déchiffrement.

Lors de l’installation initiale, vous êtes invité à laisser Commerce générer une clé de chiffrement ou à saisir l’une des vôtres. L’outil Clé de chiffrement vous permet de modifier la clé selon vos besoins. La clé de chiffrement doit être changée régulièrement pour améliorer la sécurité, et à tout moment la clé d&#39;origine peut être compromise.

Pour obtenir des informations techniques, consultez [Installation sur site avancée](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) dans le _Guide d’installation_ et [Reclassement des données](https://developer.adobe.com/commerce/php/development/security/data-encryption/) dans le _Guide de développement PHP_.

>[!IMPORTANT]
>
>- Avant de suivre ces instructions pour modifier la clé de chiffrement, assurez-vous que le fichier suivant est accessible en écriture : `[your store]/app/etc/env.php`
>- La fonction de modification de la clé de chiffrement dans les paramètres d’administration est obsolète et a été supprimée dans la version 2.4.8. Vous devez utiliser la commande CLI décrite sur cette page pour modifier votre clé de chiffrement après la mise à niveau vers la version 2.4.8.
>- La rotation de la clé de chiffrement invalidera immédiatement toutes les sessions client et administrateur (à l’exclusion des utilisateurs de l’intégration) et nécessitera qu’ils se reconnectent.

**Pour modifier une clé de chiffrement :**

Les instructions suivantes nécessitent l’accès à un terminal.

1. Activez le [mode de maintenance](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

   ```bash
   bin/magento maintenance:enable
   ```

1. Désactivez les tâches cron.

   _Projets d&#39;infrastructure cloud :_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Projets sur site_

   ```bash
   crontab -e
   ```

1. Modifiez la clé de chiffrement à l’aide de l’une des méthodes suivantes.

   +++Commande CLI

   Vérifiez que la nouvelle commande existe :

   ```bash
   bin/magento list | grep encryption:key:change
   ```

   La sortie suivante devrait s’afficher :

   ```bash
   encryption:key:change Change the encryption key inside the env.php file.
   ```

   Si cette sortie s’affiche, exécutez la commande d’interface de ligne de commande suivante et assurez-vous qu’elle se termine sans erreur. Si vous devez rechiffrer certaines valeurs de configuration système ou certains champs de paiement, consultez le [guide détaillé sur le rechiffrement](https://developer.adobe.com/commerce/php/development/security/data-encryption/) dans le _Guide de développement PHP_.

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++Paramètres d’administration

   >[!IMPORTANT]
   >
   >Cette fonctionnalité a été abandonnée et supprimée dans la version 2.4.8. Adobe recommande de modifier les clés de chiffrement avec l’interface de ligne de commande.

   1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![Clé de chiffrement système](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Effectuez l’une des opérations suivantes :

      - Pour générer une nouvelle clé, définissez **[!UICONTROL Auto-generate Key]** sur `Yes`.
      - Pour utiliser une autre clé, définissez **[!UICONTROL Auto-generate Key]** sur `No`. Ensuite, dans le champ **[!UICONTROL New Key]** , saisissez ou collez la clé à utiliser.

   1. Cliquez sur **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Conservez l’enregistrement de la nouvelle clé dans un emplacement sécurisé. Il est nécessaire de déchiffrer les données si des problèmes se produisent avec vos fichiers.

   +++

1. Videz le cache.

   _Projets d&#39;infrastructure cloud :_

   ```bash
   magento-cloud cc
   ```

   _Projets locaux :_

   ```bash
   bin/magento cache:flush
   ```

1. Activez les tâches cron.

   _Projets d&#39;infrastructure cloud :_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Projets locaux :_

   ```bash
   crontab -e
   ```

1. Désactivez le mode de maintenance.

   ```bash
   bin/magento maintenance:disable
   ```
