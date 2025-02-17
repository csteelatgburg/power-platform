---
title: Control environment creation and management | Microsoft Docs
description: Control who can create and manage environments in the Power Platform Admin center
author: jimholtz
manager: kvivek
ms.service: power-platform
ms.component: pa-admin
ms.topic: quickstart
ms.date: 10/09/2019
ms.author: jimholtz
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---

# Control who can create and manage environments in the Power Platform Admin center 

With the new provisioning model, those with the correct licenses can create an environment as long as 1GB of capacity is available. To restrict environment creation and management to admins, do the following:

1. Sign in to the Power Platform Admin center at [https://admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com).
2. Select the **Gear** icon (![Gear icon](media/selection-rule-gear-button.png)) in the upper-right corner of the Power Platform site.
3. Select **Only specific admins**.

   > [!div class="mx-imgBorder"] 
   > ![](./media/governance-setting.png "Specify Global admins")

The following admins will be able to create new environments in the Power Platform Admin center:

- Office 365 Global admins
- Service admins
- Delegated admins

> [!NOTE]
> Environments created prior to restriction can still be managed after restriction by those who created the environment. Restriction will prevent any new environments being created and managed. 

## Control environment creation through PowerShell

Download and install the admin PowerShell cmdlets as described [here](https://www.powershellgallery.com/packages/Microsoft.PowerApps.Administration.PowerShell/2.0.1). For more information about our cmdlets, see [PowerShell support for PowerApps (preview)](powerapps-powershell.md).

Use the following commands to restrict environment creation to Global admin, service admin, and Delegated admin. 

```
$settings = @{ DisableEnvironmentCreationByNonAdminUsers = $true }
Set-TenantSettings $settings
```

## FAQ

### Can I disable Trial environment creation for users in the tenant?
Yes. Use the following PowerShell commands to restrict Trial environment creation.

```
$settings = @{ DisableTrialEnvironmentCreationByNonAdminUsers = $true }
Set-TenantSettings $settings
```

Download and install the admin PowerShell cmdlets as described [here](https://www.powershellgallery.com/packages/Microsoft.PowerApps.Administration.PowerShell/2.0.1). For more information about our cmdlets, see [PowerShell support for PowerApps (preview)](powerapps-powershell.md).


