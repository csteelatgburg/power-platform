---
title: "Copy an environment to a Sandbox environment  | MicrosoftDocs"
description: Learn how to copy a Sandbox environment. 
author: jimholtz
manager: kvivek
ms.service: power-platform
ms.component: pa-admin
ms.topic: conceptual
ms.date: 08/30/2019
ms.author: jimholtz
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
---
# Copy an environment

You can use Copy environment in the Power Platform Admin center to copy the model-driven apps in Dynamics 365, such as Dynamics 365 Sales and Customer Service, and all data from any environment to a Sandbox environment. You can select two levels of copy: **Everything** or **Customizations and schemas only**.  

> [!div class="mx-imgBorder"] 
> ![](media/copy-menu.png "Copy menu")

> [!NOTE]
> - You can only copy an environment to a Sandbox environment.
> - The source and destination environments must be in the same region.
> - Currently, any components that have not been added to a solution (including canvas apps, flows, custom connectors, and connections) will not be copied to the target environment.


  
## Copy over everything
 An Everything copy includes all application data, users, and customizations, and schemas from the source environment and is suitable for:  
  
- User acceptance testing  
- Upgrade testing  
- Preview in production (TAP/EA)  
- Training  
  
**An example scenario**  
  
Isaac, a business application developer, has received a request from the sales department to configure and deploy a social media integration solution from another company vendor.  Isaac has never installed a solution from this vendor and is unsure what impact this would have on the production application.  He’d like to import the solution into an environment that is nearly identical to, but isolated from, production to learn about the solution and make the appropriate configuration changes. Isaac submits a request to Thomas, the IT Manager for Contoso, to create an Everything copy Sandbox environment for him.  
  
After the Everything copy is complete, Isaac receives a mail from Thomas telling him the Sandbox environment is ready.  Isaac logs into the Sandbox environment and makes the necessary changes to make sure that production external services will not be impacted by the Sandbox environment.  Once changes are complete, Isaac turns off administration mode and enables background services.  Isaac is able to use the Everything copy Sandbox environment to do his testing and later manually import the solution into production.  
  
## Copy over customizations and schemas only 
 A Customizations and schemas only copy only includes users, customizations, and schema from the source environment and is suitable for:  
  
- Iterative team development  
- Partner/ISV solutions  
- Proof of concept  
  
**An example scenario**  
  
Isaac has a large development project starting next week for the sales department.  He has a team of developers ready to start on the project, some of whom are internal to Contoso and some are external vendors. The Contoso sales application contains Personally Identifiable Information (PII) that the sales manager has explicitly stated must not be made available to any external parties for privacy and legal liability reasons.  Isaac requests a customizations and schemas only copy Sandbox environment that does not contain any production data or users. In addition, Isaac creates a Office 365 security group to give the development team access to the Sandbox environment.  
  
After modifying and enabling some of the plug-ins, the developer Sandbox environment functions the same and is completely isolated from the production application.  The development team works on their modifications in this environment for several weeks.  They package their changes into a solution and export/import to deploy to the Everything copy Sandbox environment.  After a successful round of testing and signoffs, the changes are manually deployed to production.  
  
### Entities copied in a Customizations and schemas only copy  
 The following entities are copied when you do a Customizations and schemas only copy:  

| Entities |  
|-----------|  
|BusinessUnit|  
|ConnectionRole|  
|Currency|  
|DuplicateRule|  
|DuplicateRuleCondition|  
|EmailServerProfile|  
|FieldPermission|  
|FieldSecurityProfile|  
|ImportMap|  
|InternalAddress|  
|Mailbox|  
|Organization|  
|Position|  
|Report|  
|Resource|  
|ResourceGroup|  
|Role|  
|RollupField|  
|SavedQuery|  
|SLAKPIenvironment|  
|Solution|  
|Subject|  
|Team|  
|TeamTemplate|  
|Template|  
|SystemUser|  

## Copy an environment to a Sandbox environment
  
1. Go to the [Power Platform Admin center](https://admin.powerplatform.microsoft.com) and sign in using Environment Admin or System Administrator role credentials.
  
   > [!NOTE]
   > Environment Admins or System Administrators can copy all available environments. System administrators can copy environments for which they have the Environment Admin or System Administrator role.  
  
2. From the left-side menu, select **Environments**, and then select an environment to copy.

3. Select **Copy** from the top menu bar.
  
4. Select the desired copy over level.
  
   > [!div class="mx-imgBorder"] 
   > ![](media/copy-environment1.png "Copy environment")

5. Select a Sandbox environment.
  
    A target environment can be a Sandbox or Preview environment; not a Production environment.  
  
   > [!WARNING]
   >  The target environment will be deleted and replaced with a copy of the data and customizations from the source environment. You won’t be able to recover any deleted data.  

6. To restrict environment access to people in a security group select **Edit** (![Edit](media/edit-button.png)).

7. Edit the details for the copied environment, and then select **Copy**.

   > [!div class="mx-imgBorder"] 
   > ![](media/copy-environment2.png "Copy environment")

8. Select **Confirm** to overwrite the target environment.

The overwrite process starts.

> [!div class="mx-imgBorder"] 
> ![](media/copy-environment-status.png "Copy environment status")
  
Once the copy process is complete, the target environment is placed in [Administration mode](sandbox-environments.md#administration-mode) and background operations are disabled. The next section describes recommended Administrator actions for the newly created copy (target) environment.  
 
### Next steps after copying an environment  
 To ensure the newly created copy (target) environment does not impact your Production environment, once the copy operation is complete, two things happen:  
  
1. The newly created copy environment is placed in administration mode. Only those with System Administrator or System Customizer security roles can sign in and manage the copy environment. Regular users cannot sign in and use the copy environment.  
  
2. Background operations are disabled in the copy environment. Disabled operations include workflows and synchronization with Microsoft Exchange.  
  
**Review components**  
  
 You should review the status of application components in the copy environment with external connections such as Yammer, email, plug-ins, custom workflow activities, etc. Review these and consider what action to take:  
  
1. Disable the component.  
  
2. Redirect the component to another service environment such as one running Exchange or SharePoint.  
  
3. Do nothing – leave the component as is in the copy environment. For example, you might decide to allow Yammer posting to both the copy and Production environments.  
  
   Here are some possible application components in the copy environment that could have external connections and therefore could impact services with the same connections in your Production environment.  
  
- **Email**. A mailbox cannot be synced with two different environments. For an Everything copy environment, the user mailboxes in the copy environment must be disabled so the mailboxes do not attempt to send or receive email, or track appointments, contacts, or tasks. Set synchronization for the following to None.  
  
    - Incoming Email  
    - Outgoing Email  
    - Appointments, Contacts, Tasks  
  
  More information: [Set the delivery method for incoming and outgoing email](https://docs.microsoft.com/dynamics365/customer-engagement/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
- **SharePoint**. Deactivate or redirect SharePoint to a sandbox SharePoint environment to prevent impacting documents managed by SharePoint. Go to **Settings** > **Documentation Management** > **SharePoint Sites**. Select your site, and then click **Deactivate**.  
  
- **Yammer**. Disable Yammer or redirect to a separate Yammer service to prevent posts made in the copy environment conflicting with posts made in the Production environment. Go to **Settings** > **Administration** > **Yammer Configuration**.  
  
     After creating a new Sandbox environment, workflows and system jobs might be pending execution. Apart from these jobs, if you have connected Yammer to model-driven apps in Dynamics 365 there will be Yammer activity streams posted from model-driven apps in Dynamics 365 to Yammer asynchronously. These activity streams are not visible through the system jobs. If there were any pending Yammer activity streams before the Disable Background Process is turned on, these activity steams will be posted to the current Yammer configuration once the Disable Background Process is turned back off. In the Sandbox environment, if you have your current Yammer configuration connected to the same Yammer network as your production environment, you might see duplicate activity streams. To avoid duplicate Yammer activity streams, redirect your Sandbox environment to another Yammer network (possibly a test network) before turning background processes back on.  
  
- **Platform extensibility**. Consider disabling the following that could be running in the copy environment and impacting external service components.  
  
    - **Server-side plug-ins**.  
    - **Workflow custom activity**.  
- **Client extensibility**. Review the following.  
    - **Client-side JavaScript**. Take a look at your JavaScript and HTML web resources for read/write operations that could impact external services.  
    - **IFRAMES**. Determine if the target of an IFRAME is a Production environment.  
