---
title: "Recover database space by deleting audit logs  | MicrosoftDocs"
description: Recover database space by deleting audit logs
author: jimholtz
manager: kvivek
ms.service: power-platform
ms.component: pa-admin
ms.topic: conceptual
ms.date: 03/19/2019
ms.author: jimholtz
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---
# Recover database space by deleting audit logs

[!INCLUDE [cc-settings-moving](../includes/cc-settings-moving.md)] 

When you enable auditing, model-driven apps in Dynamics 365, such as Dynamics 365 Sales and Customer Service, store the change history for transactions in the form of audit logs in the database. You can delete the old or unwanted logs to clean up the database space.  
  
> [!CAUTION]
>  When you delete an audit log, you can no longer view the audit history for the period covered by that audit log.  
  
1. [!INCLUDE[proc_permissions_system_admin_and_customizer](../includes/proc-permissions-system-admin-and-customizer.md)]  
  
    Check your security role  
  
   - [!INCLUDE[proc_follow_steps_in_link](../includes/proc-follow-steps-in-link.md)]  
  
   - [!INCLUDE[proc_dont_have_correct_permissions](../includes/proc-dont-have-correct-permissions.md)]  
  
2. [!INCLUDE[proc_settings_auditing](../includes/proc-settings-auditing.md)]  
  
3. Choose **Audit Log Management**  
  
4. Select the oldest audit log. Then, on the command bar, choose **Delete Logs**.  
  
5. In the confirmation message, choose **OK**.  
  
   > [!NOTE]
   >  You can only delete the oldest audit log in the system. To delete more than one audit log, continue to delete the oldest audit log until you have deleted enough logs.  
  
### See also  
[Audit data and user activity](audit-data-user-activity.md)<br />
[Retrieve and delete the history of audited data changes](/dynamics365/customer-engagement/developer/retrieve-and-delete-the-history-of-audited-data-changes.md)
