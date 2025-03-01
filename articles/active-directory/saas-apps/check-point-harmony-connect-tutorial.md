---
title: 'Tutorial: Azure Active Directory single sign-on (SSO) integration with Check Point Harmony Connect'
description: Learn how to configure single sign-on between Azure Active Directory and Check Point Harmony Connect.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 11/21/2022
ms.author: jeedes

---

# Tutorial: Azure Active Directory single sign-on (SSO) integration with Check Point Harmony Connect

In this tutorial, you'll learn how to integrate Check Point Harmony Connect with Azure Active Directory (Azure AD). When you integrate Check Point Harmony Connect with Azure AD, you can:

* Control in Azure AD who has access to Check Point Harmony Connect.
* Enable your users to be automatically signed-in to Check Point Harmony Connect with their Azure AD accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Check Point Harmony Connect single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Check Point Harmony Connect supports **SP** initiated SSO.
> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.


## Adding Check Point Harmony Connect from the gallery

To configure the integration of Check Point Harmony Connect into Azure AD, you need to add Check Point Harmony Connect from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **New application**.
1. In the **Add from the gallery** section, type **Check Point Harmony Connect** in the search box.
1. Select **Check Point Harmony Connect** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)


## Configure and test Azure AD SSO for Check Point Harmony Connect

Configure and test Azure AD SSO with Check Point Harmony Connect using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Check Point Harmony Connect.

To configure and test Azure AD SSO with Check Point Harmony Connect, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Check Point Harmony Connect SSO](#configure-check-point-harmony-connect-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Check Point Harmony Connect test user](#create-check-point-harmony-connect-test-user)** - to have a counterpart of B.Simon in Check Point Harmony Connect that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **Check Point Harmony Connect** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, enter the values for the following fields:

	In the **Sign on URL** text box, type the URL:
    `https://cloudinfra-gw.portal.checkpoint.com/api/saml/sso`

1. Check Point Harmony Connect application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![image](common/default-attributes.png)

1. In addition to above, Check Point Harmony Connect application expects few more attributes to be passed back in SAML response which are shown below. These attributes are also pre populated but you can review them as per your requirements.
	
	| Name |  Source Attribute|
	| ---------------- | --------- |
	| groups | user.groups |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

1. On the **Set up Check Point Harmony Connect** section, copy the appropriate URL(s) based on your requirement.

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

In this section, you'll enable B.Simon to use single sign-on by granting access to Check Point Harmony Connect.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **Check Point Harmony Connect**.
1. In the app's overview page, select **Users and groups**.
1. Select **Add user/group**, then select **Users and groups** in the **Add Assignment** dialog.
   1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
   1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
   1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Check Point Harmony Connect SSO

1. Log in to your Check Point Harmony Connect website as an administrator.

1. Click **SETTINGS**, then go to the **Identity Provider** and click on **CONNECT NOW**.

	![screenshot for identity provider.](./media/check-point-harmony-connect-tutorial/identity-provider.png)

1. Select **Microsoft Azure AD** as your identity provider and click **NEXT**.

	![screenshot to select identity provider.](./media/check-point-harmony-connect-tutorial/select-identity-provider.png)

1. On the **Verify Domain** page, enter your organization domain and enter this generated DNS record to your DNS server as TXT record, click **NEXT**.

	![screenshot for Domain value.](./media/check-point-harmony-connect-tutorial/domain.png)

1. In the Allow Connectivity page, perform the following steps:

	![screenshot for Allow Connectivity page.](./media/check-point-harmony-connect-tutorial/allow-connectivity.png)

	a. Copy **ENTITY ID** value, paste this value into the **Identifier** text box in the **Basic SAML Configuration** section.

	b. Copy **REPLY URL** value, paste this value into the **Reply URL** text box in the **Basic SAML Configuration** section.

	c. Click **NEXT**.

1. In the **Configure Metadata** page, upload the **Federation Metadata XML** that you downloaded from your Azure portal.

1. In the **CONFIRM IDENTITY PROVIDER** page, click **Add** to complete the configuration.

### Create Check Point Harmony Connect test user

1. Log in to your Check Point Harmony Connect website as an administrator.

1. Go to the **Policy** -> **Access Control** and create a **new rule** and click on **(+)** to add **New User**. 

	![screenshot for create new user.](./media/check-point-harmony-connect-tutorial/add-new-user.png)

1. In the **ADD USER** window, enter the Name and User Name in their respective text boxes and click **ADD**.

	![screenshot for create user.](./media/check-point-harmony-connect-tutorial/add-user.png)

## Test SSO 

To test the Check Point Harmony Connect, go to their Authentication service and authenticate using test account which you have created in the **Create an Azure AD test user** section.

## Next steps

Once you configure Check Point Harmony Connect you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
