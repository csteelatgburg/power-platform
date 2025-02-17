---
title: "System Settings Customization tab  | MicrosoftDocs"
description: System Settings Customization tab 
author: jimholtz
manager: kvivek
ms.service: power-platform
ms.component: pa-admin
ms.topic: conceptual
ms.date: 10/30/2017
ms.author: jimholtz
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---
# System Settings Customization tab 

Use the tab to set preferences for plug-in and workflow tracing and also the use of application mode.

[!INCLUDE [cc-settings-moving](../includes/cc-settings-moving.md)] 
  
## Open the System Settings dialog box (if it isn’t already open)  
  
1. [!INCLUDE[proc_permissions_system_admin_and_customizer](../includes/proc-permissions-system-admin-and-customizer.md)]  
  
    Check your security role  
  
   - [!INCLUDE[proc_follow_steps_in_link](../includes/proc-follow-steps-in-link.md)]  
  
   - [!INCLUDE[proc_dont_have_correct_permissions](../includes/proc-dont-have-correct-permissions.md)]  
  
2. [!INCLUDE[proc_settings_administration](../includes/proc-settings-administration.md)]  
  
3. Choose **System Settings** and then choose the **Customization** tab.  
  
|                                                                       Settings                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                        Description                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                                 **Application mode**                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Set whether model-driven apps in Dynamics 365, such as Dynamics 365 Sales and Customer Service, can be opened in a browser window without menu, navigation, and command bars. |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|                                 Open model-driven apps in Dynamics 365 in Application mode                                  |                                                                                                                                                                                                 Select this check box to enable application mode. When this mode is enabled, model-driven apps in Dynamics 365 can be opened in a browser without menus, navigation, or toolbars. Hiding these parts of the browser cause model-driven apps in Dynamics 365 to appear like a separate applications rather than a website. By default, application mode isn’t enabled.                                                                                                                                                                                                 |
|                                                   **Plug-in and custom workflow activity tracing**                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|                                                          Enable logging to plug-in trace log                                                          | You can now store detailed information about an exception or trace event raised by a custom code to help developers debug plug-ins or custom workflow activity that they develop using the customization methods supported by model-driven apps in Dynamics 365.<br /><br /> -   To capture trace logs only for exceptions, select **Exception**.<br />-   To capture logs for all errors and general trace events, select **All**.<br />-   To disable capturing trace logs, select **Off**.<br /><br /> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Debug a plug-in](/dynamics365/customer-engagement/developer/debug-plugin.md)  **Warning:**  We recommend that you don’t keep this option enabled for an extended period because it may have performance implications in your organization. |
|                                                               **Enable Microsoft Power Automate**                                                               |                                                                                                                                                                                                                                                                                                                                                       More information: [Enable embedded Power Automate to automate processes](enable-embedded-flow-in-your-organization.md)                                                                                                                                                                                                                                                                                                                                                        |
|                                                   Show Power Automate on forms and in the site map                                                    |                                                                                                                                                                                                                                                                                                                                                                   Default: Yes. Choose **Yes** to enable embedded Power Automate flows in your organization.                                                                                                                                                                                                                                                                                                                                                                   |
  
### See also  
 [Debug a plug-in](/dynamics365/customer-engagement/developer/debug-plugin.md)
