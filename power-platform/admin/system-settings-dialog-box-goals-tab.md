---
title: "System Settings Goals tab   | MicrosoftDocs"
description: System Settings Goals tab 
author: jimholtz
manager: kvivek
ms.service: power-platform
ms.component: pa-admin
ms.topic: conceptual
ms.date: 10/09/2018
ms.author: jimholtz
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---
# System Settings Goals tab

Set the duration and frequency of the automatic rollup of goals. These settings only affect the automatic handling of all goals set in model-driven apps in Dynamics 365, such as Dynamics 365 Sales and Customer Service. You can always perform a manual rollup for any goal at any time.  

[!INCLUDE [cc-settings-moving](../includes/cc-settings-moving.md)] 
  
1. [!INCLUDE[proc_permissions_system_admin_and_customizer](../includes/proc-permissions-system-admin-and-customizer.md)]  
  
    Check your security role  
  
   - [!INCLUDE[proc_follow_steps_in_link](../includes/proc-follow-steps-in-link.md)]  
  
   - [!INCLUDE[proc_dont_have_correct_permissions](../includes/proc-dont-have-correct-permissions.md)]  
  
2. If you are using a Sales web application, go to **Settings** > **Administration** > **System Settings**, and then select the **Goals** tab.

   OR

   If you are using the Sales Hub App, select the Site map icon ![Site map icon](/dynamics365/customer-engagement/sales-enterprise/media/site-map-icon.png "Site map icon"), then select ellipsis ![Ellipsis to open more options](/dynamics365/customer-engagement/sales-enterprise/media/ellipsis-more-options.png "Ellipsis to open more options") , then select **App Settings**, and then select **Goals Settings**.
  
  
|                            Settings                            |                                                                                  Description                                                                                   |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Set the roll-up expiration time and the roll-up frequency.** |                                                                                                                                                                                |
|     Days after the goal end date when the rollup will stop     | Default: 30 days. Set the number of days after the ending date of a goal for model-driven apps in Dynamics 365 to stop including a goal in a rollup. |
|                  Roll-up recurrence frequency                  |                                                      Default: 24 hours. Set the number of hours between each goal rollup.                                                      |
  
### See also  
 [Administrator and Sales Manager Guide](/dynamics365/customer-engagement/sales-enterprise/admin-guide.md)  
 [Progress Against Goals report](/dynamics365/customer-engagement/basics/sales-insights-reports.md#BKMK_ProgressGoals)
