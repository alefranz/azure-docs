---
title: 'Tutorial: Azure Active Directory single sign-on (SSO) integration with BlogIn'
description: Learn how to configure single sign-on between Azure Active Directory and BlogIn.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 11/21/2022
ms.author: jeedes
---

# Tutorial: Azure Active Directory single sign-on (SSO) integration with BlogIn

In this tutorial, you'll learn how to integrate BlogIn with Azure Active Directory (Azure AD). When you integrate BlogIn with Azure AD, you can:

* Control in Azure AD who has access to BlogIn.
* Enable your users to be automatically signed-in to BlogIn with their Azure AD accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* BlogIn single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* BlogIn supports **SP and IDP** initiated SSO.
* BlogIn supports **Just In Time** user provisioning.
* BlogIn supports [Automated user provisioning](blogin-provisioning-tutorial.md).

## Add BlogIn from the gallery

To configure the integration of BlogIn into Azure AD, you need to add BlogIn from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **New application**.
1. In the **Add from the gallery** section, type **BlogIn** in the search box.
1. Select **BlogIn** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

## Configure and test Azure AD SSO for BlogIn

Configure and test Azure AD SSO with BlogIn using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in BlogIn.

To configure and test Azure AD SSO with BlogIn, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure BlogIn SSO](#configure-blogin-sso)** - to configure the single sign-on settings on application side.
    1. **[Create BlogIn test user](#create-blogin-test-user)** - to have a counterpart of B.Simon in BlogIn that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **BlogIn** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you want to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.blogin.co/`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.blogin.co/sso/saml/callback`

1. Click **Set additional URLs** and perform the following step if you want to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.blogin.co/`

	> [!NOTE]
	> These values are not real. Update these values with the actual Identifier, Reply URL, and Sign-on URL. You can get the exact values for these fields on the **Settings** page on BlogIn (**User Athentication** tab > **Configure SSO and User Provisioning**). Alternatively, you can contact [BlogIn Client support team](mailto:support@blogin.co) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. BlogIn application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![image](common/default-attributes.png)

1. In addition to above, BlogIn application expects few more attributes to be passed back in SAML response which are shown below. These attributes are also pre populated but you can review them as per your requirements.
	
	| Name | Source Attribute |
	| ------ | --------- |
	| title |user.jobtitle |
	

1. On the **Set up single sign-on with SAML** page, In the **SAML Signing Certificate** section, click copy button to copy **App Federation Metadata Url** and save it on your computer.

	![The Certificate download link](common/copy-metadataurl.png)

### Create an Azure AD test user

In this section, you'll create a test user called B.Simon.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [User Administrator](../roles/permissions-reference.md#user-administrator).
1. Browse to **Identity** > **Users** > **All users**.
1. Select **New user** > **Create new user**, at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Display name** field, enter `B.Simon`.  
   1. In the **User principal name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Select **Review + create**.
1. Select **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use single sign-on by granting access to BlogIn.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **BlogIn**.
1. In the app's overview page, select **Users and groups**.
1. Select **Add user/group**, then select **Users and groups** in the **Add Assignment** dialog.
   1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
   1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
   1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure BlogIn SSO

To configure single sign-on on **BlogIn** side login to your BlogIn account and follow these steps:

1. Go to **Settings** > **User Authentication** > **Configure SSO & User provisioning**.
2. On the next screen, change Single Sign-On status to **On** and choose a custom name for the SSO login button that will be displayed on the login screen.

3. If you saved the **App Federation Metadata Url** in the last step of the previous section, choose the configuration method **Metadata URL** and paste **App Federation Metadata Url** into the Metadata URL field. Otherwise, change the Configuration method to **manual**, manually populate **Identity Provider SSO URL (Login URL)** and **Identity Provider Issuer (entity ID)**, and upload the **Certificate (base64)** you got from Azure AD.

4. Choose the default user role for new users joining BlogIn using SSO.

5. Select **Save changes**.

For a more detailed explanation of setting up SSO on BlogIn, see [How to set up SSO for Microsoft Azure AD on BlogIn](https://blogin.co/blog/how-to-set-up-single-sign-on-sso-for-microsoft-azure-active-directory-azure-ad-267/). Feel free to contact the [BlogIn support team](mailto:support@blogin.co) at any time if you have any questions or need help.

### Create BlogIn test user

In this section, a user called B.Simon is created in BlogIn. BlogIn supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in BlogIn, a new one is created after authentication.

BlogIn also supports automatic user provisioning, you can find more details [here](./blogin-provisioning-tutorial.md) on how to configure automatic user provisioning.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application**, this will redirect to BlogIn Sign on URL where you can initiate the login flow.  

* Go to BlogIn Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application**, and you should be automatically signed in to the BlogIn for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the BlogIn tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the BlogIn for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Next steps

Once you configure BlogIn you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
