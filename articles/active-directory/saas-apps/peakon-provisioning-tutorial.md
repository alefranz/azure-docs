---
title: 'Tutorial: Configure Peakon automatic user provisioning with Azure Active Directory'
description: Learn how to configure Azure Active Directory to automatically provision and de-provision user accounts to Peakon .
services: active-directory
author: twimmers
writer: twimmers
manager: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 11/21/2022
ms.author: thwimmer
---

# Tutorial: Configure Peakon for automatic user provisioning

The objective of this tutorial is to demonstrate the steps to be performed in Peakon  and Azure Active Directory (Azure AD) to configure Azure AD to automatically provision and de-provision users and/or groups to Peakon.

> [!NOTE]
>  This tutorial describes a connector built on top of the Azure AD User Provisioning Service. For important details on what this service does, how it works, and frequently asked questions, see [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](../app-provisioning/user-provisioning.md).
>
> This connector is currently in Preview. For more information about previews, see [Universal License Terms For Online Services](https://www.microsoft.com/licensing/terms/product/ForOnlineServices/all).

## Prerequisites

The scenario outlined in this tutorial assumes that you already have the following prerequisites

* An Azure AD tenant.
* [A Peakon tenant](https://www.workday.com/en-us/products/employee-voice/overview.html).
* A user account in Peakon  with Admin permissions.

> [!NOTE]
> This integration is also available to use from Azure AD US Government Cloud environment. You can find this application in the Azure AD US Government Cloud Application Gallery and configure it in the same way as you do from public cloud.

## Assigning users to Peakon

Azure Active Directory uses a concept called *assignments* to determine which users should receive access to selected apps. In the context of automatic user provisioning, only the users and/or groups that have been assigned to an application in Azure AD are synchronized.

Before configuring and enabling automatic user provisioning, you should decide which users and/or groups in Azure AD need access to Peakon. Once decided, you can assign these users and/or groups to Peakon by following the instructions here:

* [Assign a user or group to an enterprise app](../manage-apps/assign-user-or-group-access-portal.md)

## Important tips for assigning users to Peakon 

* It is recommended that a single Azure AD user is assigned to Peakon  to test the automatic user provisioning configuration. Additional users and/or groups may be assigned later.

* When assigning a user to Peakon, you must select any valid application-specific role (if available) in the assignment dialog. Users with the **Default Access** role are excluded from provisioning.

## Set up Peakon for provisioning

1.  Sign in to your [Peakon Admin Console](https://app.Peakon.com/login). Click on **Configuration**. 

	![Peakon Admin Console](media/Peakon-provisioning-tutorial/Peakon-admin-configuration.png)

2. 	Select **Integrations**.
	
	![Screenshot of the Configuration options with the Integrations option called out.](media/Peakon-provisioning-tutorial/Peakon-select-integration.png)

3.	Enable **Employee Provisioning**.

	![Screenshot of the Employee Provisioning section with the Enable option called out.](media/Peakon-provisioning-tutorial/peakon05.png)

4.	Copy the values for **SCIM 2.0 URL** and **OAuth Bearer Token**. These values will be entered in the **Tenant URL** and **Secret Token** field in the Provisioning tab of your Peakon application.

	![Peakon Create Token](media/Peakon-provisioning-tutorial/peakon04.png)

## Add Peakon from the gallery

To configuring Peakon  for automatic user provisioning with Azure AD, you need to add Peakon  from the Azure AD application gallery to your list of managed SaaS applications.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **New application**.
1. In the **Add from the gallery** section, type **Peakon**, select **Peakon** in the search box.
1. Select **Peakon** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.
	![Peakon  in the results list](common/search-new-app.png)

## Configuring automatic user provisioning to Peakon 

This section guides you through the steps to configure the Azure AD provisioning service to create, update, and disable users and/or groups in Peakon  based on user and/or group assignments in Azure AD.

> [!TIP]
> You may also choose to enable SAML-based single sign-on for Peakon, following the instructions provided in the [Peakon Single sign-on tutorial](peakon-tutorial.md). Single sign-on can be configured independently of automatic user provisioning, though these two features compliment each other.

### To configure automatic user provisioning for Peakon  in Azure AD:

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications**

	![Enterprise applications blade](common/enterprise-applications.png)

1. In the applications list, select **Peakon**.

	![The Peakon  link in the Applications list](common/all-applications.png)

3. Select the **Provisioning** tab.

	![Screenshot of the Manage options with the Provisioning option called out.](common/provisioning.png)

4. Set the **Provisioning Mode** to **Automatic**.

	![Screenshot of the Provisioning Mode dropdown list with the Automatic option called out.](common/provisioning-automatic.png)

5. Under the **Admin Credentials** section, input the **SCIM 2.0 URL** and **OAuth Bearer Token** values retrieved earlier in **Tenant URL** and **Secret Token** respectively. Click **Test Connection** to ensure Azure AD can connect to Peakon. If the connection fails, ensure your Peakon account has Admin permissions and try again.

	![Tenant URL + Token](common/provisioning-testconnection-tenanturltoken.png)

7. In the **Notification Email** field, enter the email address of a person or group who should receive the provisioning error notifications and check the checkbox - **Send an email notification when a failure occurs**.

	![Notification Email](common/provisioning-notification-email.png)

8. Click **Save**.

9. Under the **Mappings** section, select **Synchronize Azure Active Directory Users to Peakon**.

	![Peakon User Mappings](media/Peakon-provisioning-tutorial/Peakon-user-mappings.png)

10. Review the user attributes that are synchronized from Azure AD to Peakon  in the **Attribute Mapping** section. The attributes selected as **Matching** properties are used to match the user accounts in Peakon  for update operations. Select the **Save** button to commit any changes.

	![Peakon User Attributes](media/Peakon-provisioning-tutorial/Peakon-user-attributes.png)

12. To configure scoping filters, refer to the following instructions provided in the 		[Scoping filter tutorial](../app-provisioning/define-conditional-rules-for-provisioning-user-accounts.md).
	
	![Provisioning Scope](common/provisioning-scope.png)

15. When you are ready to provision, click **Save**.

	![Saving Provisioning Configuration](common/provisioning-configuration-save.png)

This operation starts the initial synchronization of all users and/or groups defined in **Scope** in the **Settings** section. The initial sync takes longer to perform than subsequent syncs, which occur approximately every 40 minutes as long as the Azure AD provisioning service is running. You can use the **Synchronization Details** section to monitor progress and follow links to provisioning activity report, which describes all actions performed by the Azure AD provisioning service on Peakon.

For more information on how to read the Azure AD provisioning logs, see [Reporting on automatic user account provisioning](../app-provisioning/check-status-user-account-provisioning.md).

## Connector limitations

* All custom user attributes in Peakon have to be extended from Peakon's custom SCIM user extension of `urn:ietf:params:scim:schemas:extension:peakon:2.0:User`.

## Additional resources

* [Managing user account provisioning for Enterprise Apps](../app-provisioning/configure-automatic-user-provisioning-portal.md)
* [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
## Next steps

* [Learn how to review logs and get reports on provisioning activity](../app-provisioning/check-status-user-account-provisioning.md)
