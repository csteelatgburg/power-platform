---
title: "Enable the hybrid experience  | MicrosoftDocs"
description: Some features are not yet present in the Unified Interface but can be enabled for display as legacy dialogs in the Unified Interface through the hybrid experience.
author: jimholtz
manager: kvivek
ms.service: power-platform
ms.component: pa-admin
ms.topic: conceptual
ms.date: 10/05/2019
ms.author: jimholtz
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---
# Enable the hybrid experience

[!INCLUDE [cc-settings-moving](../includes/cc-settings-moving.md)] 

Most of the core functionalities of sales and customer service have moved to the [Unified Interface](about-unified-interface.md) experience. Some of the features that are not yet on Unified Interface can now be accessed in the Unified Interface client. 

The following features are not yet present in the Unified Interface but can be enabled for display as legacy dialogs in the Unified Interface through the hybrid experience.

- [Advanced Find](/dynamics365/customer-engagement/basics/save-advanced-find-search.md) 
- Bulk edit
- [Merge records](/dynamics365/customer-engagement/basics/merge-duplicate-records-accounts-contacts-leads.md)
- [Record sharing](/dynamics365/customer-engagement/basics/assign-record-user-team.md)
- [Audit History](/dynamics365/customer-engagement/developer/auditing-overview.md)
- All options under **Set Personal Options** (![Settings gear](media/settings-gear-icon.png "Settings gear"))

 > [!NOTE]
   > The hybrid experience is not available for on-premises versions or on mobile.  

These features are enabled through a setting in System Settings.

1. Go to **Settings** > **Administration** > **System Settings**.  
2. Select the **General** tab.  
3. Set **Enable embedding of certain legacy dialogs in Unified Interface browser client** to **Yes**.

![Enable hybrid experience](media/hybrid-system-settings.png "Enable hybrid experience")

When you enable the hybrid experience, commands appear on the command bar. For example, when you select an account, **Edit**, **Merge**, and **Share** commands are available.

![Commands on command bar](media/hybrid-edit-merge-share.png "Commands on command bar")

You can select **Share** to share this account with another user or team.

![Share account](media/hybrid-share-account.png "Share account")

If you disable the hybrid experience, these commands are not available in the command bar.

![Commands not on command bar](media/hybrid-no-edit-merge-share.png "Commands not on command bar")

### See also  
 [Unified Interface](about-unified-interface.md)
