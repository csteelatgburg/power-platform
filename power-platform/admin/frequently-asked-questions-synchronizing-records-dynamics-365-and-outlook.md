---
title: "Frequently asked questions about synchronizing records between model-driven apps in Dynamics 365 and Outlook  | MicrosoftDocs"
description: Frequently asked questions about synchronizing records between model-driven apps in Dynamics 365 and Outlook 
author: jimholtz
manager: kvivek
ms.service: power-platform
ms.component: pa-admin
ms.topic: conceptual
ms.date: 05/15/2018
ms.author: jimholtz
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---
# Frequently asked questions about synchronizing records between model-driven apps in Dynamics 365 and Microsoft Outlook

## What's the best way to use Outlook and model-driven apps in Dynamics 365 together?  
 There are three ways to use model-driven apps in model-driven apps in Dynamics 365, such as Dynamics 365 Sales and Customer Service, such as Dynamics 365 Sales and Customer Service, and [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] together:  
  
- [!INCLUDE[pn_ms_dyn_crm_app_for_outlook](../includes/pn-ms-dyn-crm-app-for-outlook.md)]  
  
- [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)] 
  
- [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)] folder tracking  
  
  Use [!INCLUDE[pn_ms_dyn_crm_app_for_outlook](../includes/pn-ms-dyn-crm-app-for-outlook.md)] paired with [!INCLUDE[cc_server_side_synch](../includes/cc-server-side-synch.md)] to view model-driven apps in Dynamics 365 data in [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] and track [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] records in model-driven apps in Dynamics 365. You can use [!INCLUDE[pn_ms_dyn_crm_app_for_outlook](../includes/pn-ms-dyn-crm-app-for-outlook.md)] together with [!INCLUDE[pn_microsoft_outlook_web_app](../includes/pn-microsoft-outlook-web-app.md)],  the [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] desktop application, or with [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] mobile. With [!INCLUDE[pn_crm_app_for_outlook_short](../includes/pn-crm-app-for-outlook-short.md)], model-driven apps in Dynamics 365 information appears next to a user’s [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] email messages or appointments. For example, people can preview information about contacts and leads stored in model-driven apps in Dynamics 365 and add contacts directly from an email message. They can also link email, appointment, and contact records  to new or existing records, such as  opportunity, account, or case records. To use [!INCLUDE[pn_crm_app_for_outlook_short](../includes/pn-crm-app-for-outlook-short.md)], you must synchronize email with [!INCLUDE[cc_server_side_synch](../includes/cc-server-side-synch.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Integrate your email system](../admin/integrate-synchronize-your-email-system.md)  
  
> [!IMPORTANT]
> As of 1/29/2018, based on overwhelming customer feedback and our desire to continue supporting our customers, we have **decided not to deprecate [!INCLUDE[pn-crm-2016-outlook-shortest](../includes/pn-crm-2016-outlook-shortest.md)]** ([!INCLUDE[pn-outlook](../includes/pn-outlook.md)] add-in). Please read [this blog post](https://blogs.msdn.microsoft.com/crm/2018/01/29/continued-support-for-outlook-add-in-dynamics-365-for-outlook/) for more details.

## How often are records synchronized through server-side sync?  
 If you synchronize records with [!INCLUDE[cc_server_side_synch](../includes/cc-server-side-synch.md)], the process is dynamic and unique for each user’s mailbox. The synchronization algorithm ensures that mailboxes are synced according to dynamic parameters such as the number of email messages and the activity within the mailbox. Normally, email synchronization occurs every 5 minutes. When a mailbox has many email messages, the interval can be reduced dynamically to 2 minutes. If the mailbox is less active, the interval can be increased up to 12 minutes. Generally speaking, you can assume that a mailbox will be synced at least once every 12 minutes. 

However, when you use Dynamics 365 App for Outlook to track or set the regarding record for an email or appointment, synchronization happens immediately in most scenarios for received emails and sent appointments. If the immediate synchronization in Dynamics 365 App for Outlook fails, we leverage server-side synchronization to create or update the activity record.
  
## Where can I find information on troubleshooting server-side synchronization issues?  
 You can find information on troubleshooting and known issues here: [Troubleshooting and things to know about server-side synchronization](../admin/troubleshooting-monitoring-server-side-synchronization.md).  
  
## Do security permissions affect synchronization?  
 Yes. If a system administrator has implemented security for particular fields or records, it can affect the data that’s synchronized.  
  
## Privacy notices  
[!INCLUDE[cc_privacy_crm_server_side_sync](../includes/cc-privacy-crm-server-side-sync.md)]
  
 [!INCLUDE[cc_privacy_crm_sync_to_outlook](../includes/cc-privacy-crm-sync-to-outlook.md)]
  
 [!INCLUDE[cc_privacy_crm_outlook1](../includes/cc-privacy-crm-outlook1.md)]
  
### See also 
 [Integrate your email system](../admin/integrate-synchronize-your-email-system.md)   
 [Dynamics 365 App for Outlook User's Guide](/dynamics365/customer-engagement/outlook-app/dynamics-365-app-outlook-user-s-guide.md)   
 [Track Outlook email by moving it to a tracked Exchange folder](track-outlook-email-by-moving-it-tracked-exchange-folder.md)   
 [Set personal options that affect tracking and synchronization between model-driven apps in Dynamics 365 and Outlook or Exchange](set-personal-options-affect-tracking-synchronization-between-dynamics-365-outlook-exchange.md)
