---
title: 'Tutorial: Azure Active Directory integration with Greenhouse'
description: Learn how to configure single sign-on between Azure Active Directory and Greenhouse.
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
# Tutorial: Azure Active Directory integration with Greenhouse

In this tutorial, you'll learn how to integrate Greenhouse with Azure Active Directory (Azure AD). When you integrate Greenhouse with Azure AD, you can:

* Control in Azure AD who has access to Greenhouse.
* Enable your users to be automatically signed-in to Greenhouse with their Azure AD accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Greenhouse single sign-on (SSO) enabled subscription.

> [!NOTE] 
> This integration is also available to use from Azure AD US Government Cloud environment. You can find this application in the Azure AD US Government Cloud Application Gallery and configure it in the same way as you do from public cloud. 

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Greenhouse supports **SP and IDP** initiated SSO.

## Adding Greenhouse from the gallery

To configure the integration of Greenhouse into Azure AD, you need to add Greenhouse from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **New application**.
1. In the **Add from the gallery** section, type **Greenhouse** in the search box.
1. Select **Greenhouse** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)


## Configure and test Azure AD SSO for Greenhouse

Configure and test Azure AD SSO with Greenhouse using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Greenhouse.

To configure and test Azure AD SSO with Greenhouse, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
2. **[Configure Greenhouse SSO](#configure-greenhouse-sso)** - to configure the Single Sign-On settings on application side.
    1. **[Create Greenhouse test user](#create-greenhouse-test-user)** - to have a counterpart of Britta Simon in Greenhouse that is linked to the Azure AD representation of user.
3. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **Greenhouse** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

	![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, enter the values for the following fields:

    a. In the **Identifier** text box, type the value:
    `greenhouse.io`

    b. In the **Reply URL** text box, type a URL using the following pattern: 
    `https://<COMPANYNAME>.greenhouse.io/<ENTITY ID>/users/saml/consume`

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type the URL:
    `https://app.greenhouse.io`

	> [!NOTE]
	> The value is not real. Update the value with the actual Reply URL. Contact [Greenhouse Client support team](https://www.greenhouse.io/contact) to get the value. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

4. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, click **Download** to download the **Federation Metadata XML** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

6. On the **Set up Greenhouse** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)


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

In this section, you'll enable B.Simon to use single sign-on by granting access to Greenhouse.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **Greenhouse**.
1. In the app's overview page, select **Users and groups**.
1. Select **Add user/group**, then select **Users and groups** in the **Add Assignment** dialog.
   1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
   1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
   1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Greenhouse SSO

1. In a different web browser window, sign into Greenhouse website as an administrator.

1. Go to the **Configure > Dev Center > Single Sign-On**.

    ![screenshot for the sso page](./media/greenhouse-tutorial/configure.png)

1. Perform the following steps in the **Single Sign-On** page.

    ![screenshot for the sso configuration page](./media/greenhouse-tutorial/sso-page.png)

    a. Copy **SSO Assertion Consumer URL** value, paste this value into the **Reply URL** text box in the **Basic SAML Configuration** section.

    b. In the **Entity ID/Issuer** textbox, paste the **Azure AD Identifier** value which you copied previously.

    c. In the **Single Sign-On URL** textbox, paste the **Login URL** value which you copied previously.

    d. Open the downloaded **Federation Metadata XML** into Notepad and paste the content into the **IdP Certificate Fingerprint** textbox.

    e. Select the **Name Identifier Format** value from the dropdown.

    f. Click **Begin Testing**.

    >[!NOTE]
    >Alternatively you can also upload the **Federation Metadata XML** file by clicking on the **Choose File** option.

### Create Greenhouse test user

In order to enable Azure AD users to log into Greenhouse, they must be provisioned into Greenhouse. In the case of Greenhouse, provisioning is a manual task.

>[!NOTE]
>You can use any other Greenhouse user account creation tools or APIs provided by Greenhouse to provision Azure AD user accounts. 

**To provision a user accounts, perform the following steps:**

1. Log in to your **Greenhouse** company site as an administrator.

2. Go to the **Configure > Users > New Users**
   
    ![Users](./media/greenhouse-tutorial/create-user-1.png "Users")

4. In the **Add New Users** section, perform the following steps:
   
    ![Add New User](./media/greenhouse-tutorial/create-user-2.png "Add New User")

    a. In the **Enter user emails** textbox, type the email address of a valid Azure Active Directory account you want to provision.

    b. Click **Save**.    
   
      >[!NOTE]
      >The Azure Active Directory account holders will receive an email including a link to confirm the account before it becomes active.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application**, this will redirect to Greenhouse Sign on URL where you can initiate the login flow.  

* Go to Greenhouse Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application**, and you should be automatically signed in to the Greenhouse for which you set up the SSO 

You can also use Microsoft My Apps to test the application in any mode. When you click the Greenhouse tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Greenhouse for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).



## Next steps

Once you configure Greenhouse you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
