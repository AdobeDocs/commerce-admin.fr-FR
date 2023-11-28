---
title: Clé de chiffrement
description: Découvrez comment générer ou ajouter automatiquement votre propre clé de chiffrement, qui doit être modifiée régulièrement pour améliorer la sécurité.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Clé de chiffrement

Adobe Commerce et Magento Open Source utilisent une clé de chiffrement pour protéger les mots de passe et d’autres données sensibles. Un standard du secteur [!DNL ChaCha20-Poly1305] algorithme est utilisé avec une clé 256 bits pour chiffrer toutes les données nécessitant un chiffrement. Cela inclut les données de carte de crédit et les mots de passe d’intégration (module de paiement et d’expédition). En outre, un algorithme de hachage sécurisé (SHA-256) puissant est utilisé pour hacher toutes les données qui ne nécessitent pas de décryptage.

Lors de l’installation initiale, vous êtes invité à laisser Commerce générer une clé de chiffrement ou à saisir l’une des vôtres. L’outil de clé de chiffrement vous permet de modifier la clé selon vos besoins. La clé de chiffrement doit être modifiée régulièrement pour améliorer la sécurité. La clé d’origine peut être compromise à tout moment. Chaque fois que la clé est modifiée, toutes les données héritées sont réencodées à l’aide de la nouvelle clé.

Pour obtenir des informations techniques, voir [Installation sur site avancée](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) dans le _Guide d’installation_.

## Étape 1 : rendre le fichier modifiable

Pour modifier la clé de chiffrement, assurez-vous que le fichier suivant est modifiable : `[your store]/app/etc/env.php`

## Étape 2 : modification de la clé de chiffrement

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Clé de chiffrement système](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Effectuez l’une des opérations suivantes :

   - Pour générer une nouvelle clé, définissez **[!UICONTROL Auto-generate Key]** to `Yes`.
   - Pour utiliser une autre clé, définissez **[!UICONTROL Auto-generate Key]** to `No`. Ensuite, dans le **[!UICONTROL New Key]** , saisissez ou collez la clé à utiliser.

1. Cliquez sur **[!UICONTROL Change Encryption Key]**.

1. Conservez un enregistrement de la nouvelle clé à un emplacement sécurisé.

   Il est nécessaire de décrypter les données, en cas de problèmes éventuels avec vos fichiers.
