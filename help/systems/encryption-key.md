---
title: Clé de chiffrement
description: Découvrez comment générer ou ajouter automatiquement votre propre clé de chiffrement, qui doit être modifiée régulièrement pour améliorer la sécurité.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Clé de chiffrement

>[!NOTE]
>
>Si vous avez tenté d’effectuer ces étapes et que vous rencontrez des problèmes, reportez-vous à l’article [Résolution des problèmes de rotation de la clé de chiffrement : CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102) de la base de connaissances.

Adobe Commerce et Magento Open Source utilisent une clé de chiffrement pour protéger les mots de passe et d’autres données sensibles. Un algorithme [!DNL ChaCha20-Poly1305] standard est utilisé avec une clé de 256 bits pour chiffrer toutes les données nécessitant un chiffrement. Cela inclut les données de carte de crédit et les mots de passe d’intégration (module de paiement et d’expédition). En outre, un algorithme de hachage sécurisé (SHA-256) puissant est utilisé pour hacher toutes les données qui ne nécessitent pas de décryptage.

Lors de l’installation initiale, vous êtes invité à laisser Commerce générer une clé de chiffrement ou à en saisir une. L’outil de clé de chiffrement vous permet de modifier la clé selon vos besoins. La clé de chiffrement doit être modifiée régulièrement pour améliorer la sécurité. La clé d’origine peut être compromise à tout moment.

Pour obtenir des informations techniques, reportez-vous à la section [Installation sur site avancée](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) du _Guide d’installation_.

>[!IMPORTANT]
>
>Avant de suivre ces instructions pour modifier la clé de chiffrement, assurez-vous que le fichier suivant est modifiable : `[your store]/app/etc/env.php`

**Pour modifier une clé de chiffrement :**

Les instructions suivantes nécessitent l’accès à un terminal.

1. Activez le [mode de maintenance](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

   ```bash
   bin/magento maintenance:enable
   ```

1. Désactivez les tâches cron.

   _Projets d’infrastructure cloud :_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Projets sur site_

   ```bash
   crontab -e
   ```

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Clé de chiffrement système](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Effectuez l’une des opérations suivantes :

   - Pour générer une nouvelle clé, définissez **[!UICONTROL Auto-generate Key]** sur `Yes`.
   - Pour utiliser une autre clé, définissez **[!UICONTROL Auto-generate Key]** sur `No`. Ensuite, dans le champ **[!UICONTROL New Key]** , saisissez ou collez la clé que vous souhaitez utiliser.

1. Cliquez sur **[!UICONTROL Change Encryption Key]**.

   >[!NOTE]
   >
   >Conservez un enregistrement de la nouvelle clé à un emplacement sécurisé. Il est nécessaire de décrypter les données, en cas de problèmes éventuels avec vos fichiers.

1. Videz le cache.

   _Projets d’infrastructure cloud :_

   ```bash
   magento-cloud cc
   ```

   _Projets sur site :_

   ```bash
   bin/magento cache:flush
   ```

1. Activez les tâches cron.

   _Projets d’infrastructure cloud :_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Projets sur site :_

   ```bash
   crontab -e
   ```

1. Désactivez le mode de maintenance.

   ```bash
   bin/magento maintenance:disable
   ```
