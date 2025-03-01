---
title: 'Tutorial: Azure Active Directory integration with Corptax'
description: Learn how to configure single sign-on between Azure Active Directory and Corptax.
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
# Tutorial: Azure Active Directory integration with Corptax

In this tutorial, you learn how to integrate Corptax with Azure Active Directory (Azure AD).
Integrating Corptax with Azure AD provides you with the following benefits:

* You can control in Azure AD who has access to Corptax.
* You can enable your users to be automatically signed-in to Corptax (Single Sign-On) with their Azure AD accounts.
* You can manage your accounts in one central location.

If you want to know more details about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](../manage-apps/what-is-single-sign-on.md).
If you don't have an Azure subscription, [create a free account](https://azure.microsoft.com/free/) before you begin.

## Prerequisites

To configure Azure AD integration with Corptax, you need the following items:

* An Azure AD subscription. If you don't have an Azure AD environment, you can get a [free account](https://azure.microsoft.com/free/)
* Corptax single sign-on enabled subscription

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.

* Corptax supports **SP** initiated SSO

## Adding Corptax from the gallery

To configure the integration of Corptax into Azure AD, you need to add Corptax from the gallery to your list of managed SaaS apps.

**To add Corptax from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon.

	![The Azure Active Directory button](common/select_azuread.png)

2. Navigate to **Enterprise Applications** and then select the **All Applications** option.

	![The Enterprise applications blade](common/enterprise_applications.png)

3. To add new application, click **New application** button on the top of dialog.

	![The New application button](common/add_new_app.png)

4. In the search box, type **Corptax**, select **Corptax** from result panel then click **Add** button to add the application.

	![Corptax in the results list](common/search_new_app.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with Corptax based on a test user called **Britta Simon**.
For single sign-on to work, a link relationship between an Azure AD user and the related user in Corptax needs to be established.

To configure and test Azure AD single sign-on with Corptax, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Configure Corptax Single Sign-On](#configure-corptax-single-sign-on)** - to configure the Single Sign-On settings on application side.
3. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Create Corptax test user](#create-corptax-test-user)** - to have a counterpart of Britta Simon in Corptax that is linked to the Azure AD representation of user.
6. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on.

To configure Azure AD single sign-on with Corptax, perform the following steps:

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **Corptax** application integration page, select **Single sign-on**.

    ![Configure single sign-on link](common/select_sso.png)

1. On the **Select a Single sign-on method** dialog, select **SAML/WS-Fed** mode to enable single sign-on.

    ![Single sign-on select mode](common/select_saml_option.png)

1. On the **Set up Single Sign-On with SAML** page, click **Edit** icon to open **Basic SAML Configuration** dialog.

	![Edit Basic SAML Configuration](common/edit_urls.png)

1. On the **Basic SAML Configuration** section, perform the following steps:

    ![Corptax Domain and URLs single sign-on information](common/sp_intiated.png)

    In the **Sign-on URL** text box, type a URL:
    `https://asp.corptax.com`

1. On the **Set up Single Sign-On with SAML** page, In the **SAML Signing Certificate** section, click **Download** to download **Federation Metadata XML** and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

### Configure Corptax Single Sign-On

To configure single sign-on on **Corptax** side, you need to send the downloaded **Federation Metadata XML** to [Corptax support team](https://connect.corptax.com/). They set this setting to have the SAML SSO connection set properly on both sides.

### Create an Azure AD test user

The objective of this section is to create a test user called Britta Simon.

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

In this section, you enable Britta Simon to use Azure single sign-on by granting access to Corptax.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **Corptax**.

	![Enterprise applications blade](common/enterprise_applications.png)

2. In the applications list, type and select **Corptax**.

	![The Corptax link in the Applications list](common/all_applications.png)

3. In the menu on the left, select **Users and groups**.

    ![The "Users and groups" link](common/users_groups_blade.png)

4. Click the **Add user** button, then select **Users and groups** in the **Add Assignment** dialog.

    ![The Add Assignment pane](common/add_assign_user.png)

5. In the **Users and groups** dialog select **Britta Simon** in the Users list, then click the **Select** button at the bottom of the screen.

6. If you are expecting any role value in the SAML assertion then in the **Select Role** dialog select the appropriate role for the user from the list, then click the **Select** button at the bottom of the screen.

7. In the **Add Assignment** dialog, click the **Assign** button.

### Create Corptax test user

In this section, you create a user called Britta Simon in Corptax. Work with [Corptax support team](https://connect.corptax.com/) to add the users in the Corptax platform. Users must be created and activated before you use single sign-on.

### Test single sign-on

In this section, you test your Azure AD single sign-on configuration using the Access Panel.
When you click the Corptax tile in the Access Panel, you should be redirected to the below Corptax page- 

![image](media/corptax-tutorial/corptaxlogin.png)

In **Environment** text box, type your appropriate environment, you should be automatically signed in to the Corptax for which you set up SSO. For more information about the Access Panel, see [Introduction to the Access Panel](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Additional Resources

- [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](./tutorial-list.md)

- [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)

- [What is Conditional Access in Azure Active Directory?](../conditional-access/overview.md)