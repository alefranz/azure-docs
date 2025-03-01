---
title: Azure Active Directory SSO integration with Oracle Access Manager for Oracle Retail Merchandising
description: Learn how to configure single sign-on between Azure Active Directory and Oracle Access Manager for Oracle Retail Merchandising.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: how-to
ms.date: 02/07/2023
ms.author: jeedes

---

# Azure Active Directory SSO integration with Oracle Access Manager for Oracle Retail Merchandising

In this article, you'll learn how to integrate Oracle Access Manager for Oracle Retail Merchandising with Azure Active Directory (Azure AD). When you integrate Oracle Access Manager for Oracle Retail Merchandising with Azure AD, you can:

* Control in Azure AD who has access to Oracle Access Manager for Oracle Retail Merchandising.
* Enable your users to be automatically signed-in to Oracle Access Manager for Oracle Retail Merchandising with their Azure AD accounts.
* Manage your accounts in one central location.

You'll configure and test Azure AD single sign-on for Oracle Access Manager for Oracle Retail Merchandising in a test environment. Oracle Access Manager for Oracle Retail Merchandising supports only **SP** initiated single sign-on.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Prerequisites

To integrate Azure Active Directory with Oracle Access Manager for Oracle Retail Merchandising, you need:

* An Azure AD user account. If you don't already have one, you can [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* One of the following roles: Global Administrator, Cloud Application Administrator, Application Administrator, or owner of the service principal.
* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Oracle Access Manager for Oracle Retail Merchandising single sign-on (SSO) enabled subscription.

## Add application and assign a test user

Before you begin the process of configuring single sign-on, you need to add the Oracle Access Manager for Oracle Retail Merchandising application from the Azure AD gallery. You need a test user account to assign to the application and test the single sign-on configuration.

### Add Oracle Access Manager for Oracle Retail Merchandising from the Azure AD gallery

Add Oracle Access Manager for Oracle Retail Merchandising from the Azure AD application gallery to configure single sign-on with Oracle Access Manager for Oracle Retail Merchandising. For more information on how to add application from the gallery, see the [Quickstart: Add application from the gallery](../manage-apps/add-application-portal.md).

### Create and assign Azure AD test user

Follow the guidelines in the [create and assign a user account](../manage-apps/add-application-portal-assign-users.md) article to create a test user account called B.Simon.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, and assign roles. The wizard also provides a link to the single sign-on configuration pane. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides). 

## Configure Azure AD SSO

Complete the following steps to enable Azure AD single sign-on.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](../roles/permissions-reference.md#cloud-application-administrator).
1. Browse to **Identity** > **Applications** > **Enterprise applications** > **Oracle Access Manager for Oracle Retail Merchandising** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** textbox, type a URL using the following pattern: ` https://<SUBDOMAIN>.oraclecloud.com/`

    b. In the **Reply URL** textbox, type a URL using the following pattern: `https://<SUBDOMAIN>.oraclecloud.com/v1/saml/<UNIQUEID>`

    c. In the **Sign on URL** textbox, type a URL using the following pattern:
    ` https://<SUBDOMAIN>.oraclecloud.com/`
    
    >[!NOTE]
    > These values are not real. Update these values with the actual Identifier, Reply URL and Sign on URL. Contact [Oracle Access Manager for Oracle Retail Merchandising support team](https://www.oracle.com/support/advanced-customer-services/cloud/) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. Your Oracle Access Manager for Oracle Retail Merchandising application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows an example for this. The default value of **Unique User Identifier** is **user.userprincipalname** but Oracle Access Manager for Oracle Retail Merchandising expects this to be mapped with the user's email address. For that you can use **user.mail** attribute from the list or use the appropriate attribute value based on your organization configuration.

	![image](common/default-attributes.png)

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

## Configure Oracle Access Manager for Oracle Retail Merchandising SSO

To configure single sign-on on Oracle Access Manager for Oracle Retail Merchandising side, you need to send the downloaded Federation Metadata XML file from Azure portal to [Oracle Access Manager for Oracle Retail Merchandising support team](https://www.oracle.com/support/advanced-customer-services/cloud/). They set this setting to have the SAML SSO connection set properly on both sides.

### Create Oracle Access Manager for Oracle Retail Merchandising test user

In this section, you create a user called Britta Simon at Oracle Access Manager for Oracle Retail Merchandising. Work with [Oracle Access Manager for Oracle Retail Merchandising support team](https://www.oracle.com/support/advanced-customer-services/cloud/) to add the users in the Oracle Access Manager for Oracle Retail Merchandising platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

* Click on **Test this application**, this will redirect to Oracle Access Manager for Oracle Retail Merchandising Sign-on URL where you can initiate the login flow. 

* Go to Oracle Access Manager for Oracle Retail Merchandising Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the Oracle Access Manager for Oracle Retail Merchandising tile in the My Apps, this will redirect to Oracle Access Manager for Oracle Retail Merchandising Sign-on URL. For more information, see [Azure AD My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Additional resources

* [What is single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
* [Plan a single sign-on deployment](../manage-apps/plan-sso-deployment.md).

## Next steps

Once you configure Oracle Access Manager for Oracle Retail Merchandising you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).
