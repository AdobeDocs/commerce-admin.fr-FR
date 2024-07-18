---
title: URL de magasin
description: Découvrez les URL de magasin et comment configurer l’URL de base et les codes de magasin.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
source-git-commit: c7839f0a86be4459ba7f555fd2d2e748d81c4ebb
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 0%

---

# URL de magasin

Chaque site web d’une installation Adobe Commerce ou Magento Open Source comporte une URL de base affectée au storefront et une autre URL affectée à l’administrateur. Adobe utilise des variables pour définir des liens internes par rapport à l’URL de base, ce qui permet de déplacer un magasin entier d’un emplacement à un autre sans mettre à jour les liens. Les URL de base standard commencent par `http` et les URL de base sécurisées commencent par `https`.

- **URL de base** — `http://www.yourdomain.com/magento/`
- **URL de base sécurisée** — `https://www.yourdomain.com/magento/`
- **URL avec adresse IP** — `http://###.###.###.###/magento/` ou `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>Ne modifiez pas l’URL d’administration de la configuration de l’URL de base par défaut. Pour modifier l’URL ou le chemin d’accès de l’administrateur, voir [Utilisation d’une URL d’administration personnalisée](#use-a-custom-admin-url).

## Utiliser un protocole sécurisé

Les URL de base de votre magasin ont été initialement configurées lors de votre installation d’Adobe Commerce. Si un certificat de sécurité était disponible à l’époque, vous pouvez spécifier les URL `HTTPS` à utiliser pour le magasin, l’administrateur ou les deux. Si votre installation Adobe Commerce comprend plusieurs magasins ou si vous prévoyez d’ajouter d’autres magasins par la suite, vous pouvez inclure le code de magasin dans l’URL. Toutes les ressources et opérations d’Adobe peuvent être utilisées avec un protocole sécurisé.

Si aucun certificat de sécurité n’était disponible pour le domaine au moment de l’installation, veillez à mettre à jour la configuration avant de lancer votre boutique. Une fois qu’un certificat de sécurité a été établi pour votre domaine, vous pouvez configurer ou les deux URL de base pour qu’elles fonctionnent avec le protocole SSL (Secure Sockets Layer) chiffré et TLS (Transport Layer Security][1]).[

>[!IMPORTANT]
>
>Adobe recommande vivement de transmettre toutes les pages d’un site de production, y compris les pages de contenu et de produit, à l’aide d’un protocole sécurisé.

Adobe Commerce et Magento Open Source peuvent être configurés par défaut pour diffuser toutes les pages de plus de `HTTPS`. Si votre magasin a fonctionné avec le protocole standard, vous pouvez améliorer la sécurité en activant [HTTP Strict Transport Security][2] (HSTS) et en mettant à niveau toutes les demandes de page non sécurisées. HSTS est un protocole d’accord préalable qui empêche les navigateurs de rendre les pages `HTTP` standard transmises avec un protocole non sécurisé pour le domaine spécifié. Comme les moteurs de recherche ont peut-être déjà indexé chaque page de votre magasin avec des URL `HTTP` standard, vous pouvez configurer Commerce pour mettre à niveau automatiquement toutes les demandes de page non sécurisées vers `HTTPS` afin de ne pas perdre de trafic. Lorsque Commerce est configuré pour utiliser des URL sécurisées pour le storefront et l’administrateur, deux champs supplémentaires s’affichent pour vous permettre d’activer `HSTS`.

## Configuration de l’URL de base

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous _Général_ dans le panneau de gauche, sélectionnez **[!UICONTROL Web]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Base URL]** .

   - **[!UICONTROL Base URL]** — Saisissez l’URL de base complète pour votre magasin. Veillez à terminer l’URL par une barre oblique afin qu’elle puisse être étendue à l’aide de clés URL supplémentaires provenant de votre magasin. Par exemple : `http://yourdomain.com/`

     >[!NOTE]
     >
     >Ne modifiez pas l’espace réservé dans le champ _[!UICONTROL Base Link URL]_. Il s’agit d’un espace réservé utilisé pour créer des liens relatifs vers l’URL de base.

   - **[!UICONTROL Base URL for Static View Files]** — (Facultatif) Spécifiez un autre emplacement pour l’URL de base pour les fichiers d’affichage statique en saisissant le chemin d’accès commençant par l’espace réservé suivant :

     \{\{unsecure_base_url}

   - **[!UICONTROL Base URL for User Media Files]** — (Facultatif) Spécifiez un autre emplacement pour l’URL de base pour les fichiers multimédias utilisateur en saisissant le chemin commençant par l’espace réservé suivant :

     \{\{unsecure_base_url}

     Dans le cas d’une installation standard, il n’est pas nécessaire de mettre à jour les chemins d’accès des fichiers d’affichage statique ou des fichiers multimédias, car ils sont relatifs à l’URL de base.

   ![Configuration générale - URL de base web](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Les espaces réservés aux accolades doubles sont des balises de marquage pour les variables.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Configuration de l’URL de base sécurisée

Si votre domaine dispose d’un certificat de sécurité valide, vous pouvez configurer les URL du storefront et de l’administrateur pour transmettre des données sur un canal sécurisé (https). Sans certificat de sécurité valide, votre boutique ne peut pas fonctionner avec le protocole sécurisé (SSL/TLS).

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur _[!UICONTROL Base URLs (Secure])_ et procédez comme suit :

   ![Configuration générale - URL de base sécurisées](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** — Saisissez l’URL de base sécurisée complète, suivie d’une barre oblique. Par exemple : `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** — Ne modifiez pas l’espace réservé dans le champ URL du lien de base sécurisé. Il est utilisé pour créer des liens relatifs vers l’URL de base sécurisée.

   - **[!UICONTROL Secure Base URL for Static View Files]** — (Facultatif) Spécifiez un autre emplacement pour l’URL de base sécurisée pour les fichiers d’affichage statique en saisissant le chemin d’accès commençant par l’espace réservé suivant :

     \{\{secure_base_url}

   - **[!UICONTROL Secure Base URL for User Media Files]** — (Facultatif) Spécifiez un autre emplacement pour l’URL de base sécurisée pour les fichiers multimédias utilisateur en saisissant le chemin commençant par l’espace réservé suivant :

     \{\{secure_base_url}

1. Pour améliorer la sécurité, définissez les deux options suivantes sur `Yes`.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. Pour _[!UICONTROL Enhanced Security Settings]_, procédez comme suit :

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** — Si vous souhaitez que votre boutique affiche uniquement des demandes de page HTTPS sécurisées, définissez sur `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]** — Pour mettre à niveau toutes les demandes de pages HTTP non sécurisées standard pour sécuriser HTTPS, définissez cette variable sur `Yes`.

1. Définissez le **[!UICONTROL Offloader Header]** pour votre serveur.

   La plupart des installations Commerce utilisent la valeur par défaut `X-Forward-Proto` pour identifier le protocole comme `HTTP` ou `HTTPS`. Si la configuration de votre serveur utilise un en-tête de déchargement différent, saisissez-le ici.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Inclure le code de magasin dans les URL

>[!NOTE]
>
>Lorsque l’option _Ajouter le code de magasin aux URL_ est définie sur `Yes`, vous devez inclure les codes de magasin dans les URL de votre navigateur. Ce paramètre garantit que les réécritures d’URL sont correctement mappées et que toutes les pages sont ouvertes correctement, sans erreur _&quot;404 Page introuvable&quot;_.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous _[!UICONTROL General]_dans le panneau de gauche, sélectionnez **[!UICONTROL Web]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL URL Options]** .

1. Définissez **[!UICONTROL Add Store Code]** selon vos préférences :

   - **[!UICONTROL URL with Store Code]** : `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]** : `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![Configuration générale - options d’URL web](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Cliquez sur le lien **[!UICONTROL Cache Management]** dans le message en haut de l’espace de travail. Suivez ensuite les instructions pour actualiser le cache.

   ![Message de gestion du cache](./assets/msg-cache-management.png)

## Dépannage des URL

Si, après avoir suivi les instructions de configuration, certaines pages continuent à être diffusées avec l’URL non sécurisée (`http://`), procédez comme suit :

- Remplacez l’URL de base (non sécurisée) par l’URL HTTPS sécurisée.
- Sur le serveur, modifiez le fichier `.htaccess` (ou équilibreur de charge) afin que l’URL non sécurisée soit redirigée vers l’URL sécurisée.

## Utilisation d’une URL d’administration personnalisée

En tant que [bonne pratique de sécurité](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), Adobe vous recommande d’utiliser une URL d’administration unique au lieu de l’ _admin_ par défaut ou un terme courant tel que _backend_. Bien qu’il ne protège pas directement votre site d’un mauvais acteur déterminé, il peut réduire l’exposition aux scripts qui tentent d’obtenir un accès non autorisé.

>[!NOTE]
>
>Vérifiez auprès de votre fournisseur d’hébergement avant d’implémenter une URL d’administration personnalisée. Certains fournisseurs d’hébergement ont besoin d’une URL standard pour respecter les règles de protection du pare-feu.

Dans une installation standard, l’URL d’administration et le chemin d’accès suivent immédiatement l’URL de base. Le chemin d’accès de l’administrateur est un répertoire situé sous la racine.

- **URL de base par défaut** : `http://yourdomain.com/magento/`
- **Chemin d’accès d’administrateur par défaut** : `admin`
- **URL et chemin d’accès d’administrateur par défaut** : `http://yourdomain.com/magento/admin`

Bien qu’il soit possible de modifier l’URL d’administration et le chemin d’accès vers un autre emplacement, toute erreur supprime l’accès à l’administrateur et doit être corrigée à partir du serveur.

>[!NOTE]
>
>Par mesure de précaution, n’essayez pas vous-même de modifier l’URL d’administration, sauf si vous savez comment modifier les fichiers de configuration sur le serveur. Pour les projets Adobe Commerce déployés sur l’infrastructure cloud, modifiez l’URL d’administration en suivant les [instructions](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=en#admin-url) du *Guide de l’infrastructure d’Adobe Commerce on Cloud*.

### Méthode 1 : modification depuis l’administrateur

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Admin Base URL]** .

1. Définissez les options de configuration de l’URL personnalisée :

   ![Configuration avancée - URL de base d’administration](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour modifier le paramètre.

   - Définissez **[!UICONTROL Use Custom Admin URL]** sur `Yes`.

   - Saisissez le **[!UICONTROL Custom Admin URL]** : `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >L’URL d’administration doit se trouver dans la même installation Commerce et avoir la même racine de document que le storefront.

   - Définissez **[!UICONTROL Custom Admin Path]** sur `Yes`.

   - Pour **[!UICONTROL Custom Admin Path]**, saisissez le chemin à utiliser comme nom de dossier d’administrateur personnalisé.

     Exemple : `sample_custom_admin`

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Une fois les modifications enregistrées, déconnectez-vous de l’administrateur et reconnectez-vous à l’aide de la nouvelle URL et du nouveau chemin d’accès d’administration.

### Méthode 2 : modifiez le chemin d’accès administrateur à partir de la ligne de commande du serveur

1. Ouvrez le fichier `app/etc/env.php` dans un éditeur de texte, puis modifiez la valeur du paramètre `frontName` de la section `backend`. Enregistrez ensuite le fichier.

   Veillez à n’utiliser que des caractères minuscules.

   >[!NOTE]
   >
   >   Cette méthode vous permet de modifier le chemin d’accès à l’administrateur, mais pas l’URL d’administration.

   >[!TIP]
   >
   >Pour Adobe Commerce sur l’infrastructure cloud, vous pouvez configurer un chemin d’accès d’administrateur personnalisé à l’aide de la variable `ADMIN_URL` dans l’interface utilisateur de Cloud. Voir la [ rubrique sur les variables d’administration ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) dans le _Guide de l’infrastructure de Commerce on Cloud_.

   - **Chemin d’accès par défaut**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **Nouveau chemin d’accès à l’administrateur**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. Utilisez l’une des méthodes suivantes pour effacer le cache :

   - Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Cliquez ensuite sur **[!UICONTROL Flush Magento Cache]**.
   - Sur le serveur, exécutez les opérations suivantes :

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >Les modifications effectuées à l’aide de la méthode 1 ont la priorité sur les modifications apportées dans le fichier `app/etc/env.php`.

### Méthode 3 : modifiez le chemin d’accès administrateur à l’aide de l’interface de ligne de commande de Commerce

Vous pouvez utiliser la commande CLI `setup:config:set` pour modifier le chemin d’accès à l’administrateur. L’exemple suivant utilise l’option `--backend-frontname` pour modifier le chemin d’accès de la racine Commerce en un nouveau chemin d’accès administrateur :

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

Cette commande met à jour l’option de configuration `backend` > `frontName` dans le fichier `app/etc/env.php`.

## Restaurer l’URL d’administration et le chemin d’accès d’administrateur par défaut

Si vous avez défini une URL d’administration non valide ou un chemin d’accès d’administrateur et que vous n’avez plus accès au serveur principal, il existe un moyen de la corriger à partir de la ligne de commande.

1. Pour rétablir l’URL d’administration par défaut, exécutez la commande suivante :

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. Pour revenir au chemin d’accès d’administration par défaut (défini dans le `app/etc/env.php` comme décrit dans la Méthode 2), exécutez cette commande :

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. Utilisez l’une des méthodes suivantes pour effacer le cache :

   - Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Cliquez ensuite sur **[!UICONTROL Flush Magento Cache]**.
   - Sur le serveur, exécutez les opérations suivantes :

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
