---
title: Modifications incompatibles avec l’arrière-plan d’Adobe Commerce B2B
description: Découvrez les modifications apportées aux versions d’Adobe Commerce B2B qui peuvent nécessiter la mise à jour de votre code personnalisé.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Modifications incompatibles avec l’arrière-plan d’Adobe Commerce B2B

Consultez les informations de référence de haut niveau pour toutes les modifications incompatibles en amont dans B2B pour les versions Adobe Commerce. Pour connaître les modifications incompatibles ayant un impact majeur et nécessitant des explications détaillées et des instructions spéciales, reportez-vous à la section Principales .

## Tons clairs

### 1.4.2 à 1.5.0

Avec l’ajout d’une affectation multi-entreprise, les comptes utilisateurs de l’entreprise peuvent désormais avoir plusieurs valeurs `company_id`. Le `Magento\Company\Api\Data\CompanyCustomerInterface` a été mis à jour afin de définir la valeur par défaut `company_id` pour un utilisateur. La valeur par défaut est définie sur la première société affectée au compte utilisateur de l’entreprise.

Si vous effectuez une mise à niveau à partir d’une version précédente, Adobe recommande de mettre en oeuvre les méthodes suivantes dans les classes qui utilisent `Magento\Company\Api\Data\CompanyCustomerInterface`.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Référence

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
