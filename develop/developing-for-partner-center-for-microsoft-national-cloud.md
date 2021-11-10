---
title: Developing for Partner Center for Microsoft National Clouds
description: Partner Center SDK differences when developing for Partner Center for Microsoft National Clouds.
MS-HAID:
- 'pc\_apiv2.developing\_with\_different\_partner\_center\_versions'
- 'pc\_apiv2.developing\_for\_partner\_center\_for\_microsoft\_national\_cloud'
ms.date: 06/11/2019
ms.service: partner-dashboard
ms.subservice:  partnercenter-sdk
---

# Developing for Partner Center for Microsoft National Clouds

**Applies to**: Partner Center operated by 21Vianet | Partner Center for Microsoft Cloud Germany | Partner Center for Microsoft Cloud for US Government

Partner Center has one set of SDK documentation. However, some functionality might not be available in the versions of Partner Center for Microsoft National Clouds.

Developers need to consider changes to the SDK for the following versions of Partner Center:

- [Partner Center operated by 21Vianet](#partner-center-operated-by-21vianet)
- [Partner Center for Microsoft Cloud Germany](#partner-center-for-microsoft-cloud-germany)
- [Partner Center for Microsoft Cloud for US Government](#partner-center-for-microsoft-cloud-for-us-government)

Each Partner Center SDK article lists applicable Partner Center versions. Each managed reference article also lists applicable Partner Center versions in the **Requirements** section.

## Partner Center operated by 21Vianet

The differences for partners between *Partner Center* and *Partner Center operated by 21Vianet* are:

- You can't programmatically reset a password for a customer user or full partner user.

- Subscriptions to Azure aren't available.

- You can't manage the licenses for your customer's user. Instead, your customers must use the Office 365 admin center to manage their licenses.

- All support requests are managed through Partner Center operated by 21Vianet. Service requests and service updates don't apply.

## Partner Center for Microsoft Cloud Germany

> [!IMPORTANT]
> Based on the evolution in customers' needs, our cloud strategy for Germany will focus on delivery of the new cloud regions in Germany that are consistent with our global cloud offering. With this focus, we will no longer be accepting new customers or deploying any new services from the currently available Microsoft Cloud Germany. Existing customers can continue to use the current cloud services available today, which we'll maintain with necessary security updates.
>
> Moving forward, new customers have the option to use the currently available European regions or the new regions in Germany when they become available. For more information, see [Microsoft to deliver cloud services from new datacenters in Germany](https://news.microsoft.com/europe/2018/08/31/microsoft-to-deliver-cloud-services-from-new-datacentres-in-germany-in-2019-to-meet-evolving-customer-needs/).

The differences for partners between *Partner Center* and *Partner Center for Microsoft Cloud Germany* are:

- Partners can't create users for their customer's organization or assign roles.
  - Partners can read fields, but can't write or update them.
  - Partners must manually create or update their customers' users in the Office 365 admin center or through the Azure portal. See [Azure Active Directory Documentation](/azure/active-directory/).

- You can't manage the licenses for your customer's users using the Partner Center for Microsoft Cloud Germany portal or APIs. Instead, you must use the Office 365 admin center or Azure Active Directly Group license management (coming soon) to manage their licenses.
  - (Optional) you can use the Microsoft Graph API. See [Assign Licenses to a user](/graph/api/user-assignlicense). For Partner Center for Microsoft Cloud Germany, be sure to use the Graph endpoint `https://graph.cloudapi.de` instead of `https://graph.windows.net`.

- You can't programmatically reset a password for a customer user or full partner user. Use the Office 365 admin center or Azure portal. See [Reset the password for a user in Azure Active Directory](/azure/active-directory/fundamentals/active-directory-users-reset-password-azure-portal). For step 1, you must sign in to the Azure portal for Microsoft Cloud Germany.

- Developers must register their app ID manually to integrate Partner Center API/SDK functionality in their app for Partner Center for Microsoft Cloud Germany. For more information, see [Register app details for Partner Center for Microsoft National Cloud](create-apps-for-partner-center-for-microsoft-national-clouds.md).

## Partner Center for Microsoft Cloud for US Government

The differences for partners between *Partner Center* and *Partner Center for Microsoft Cloud for US Government* are:

- Office 365 subscriptions aren't currently available for Partner Center for Microsoft Cloud for US Government.

- Existing partners supporting Microsoft Cloud for US Government must create new accounts in Partner Center for Microsoft Cloud for US Government.

- Microsoft Cloud for US Government customers must transact with a single partner.
  - Multichannel and multipartner and request relationship with an existing customer within Microsoft Cloud for US Government scenarios don't apply. This limitation is because Office 365 isn't currently available.

- Partners can't create users for their customer's organization or assign roles.
  - Partners can read fields, but can't write or update them. Partners must manually create or update their customers' users in the Azure portal. See [Azure Active Directory Documentation](/azure/active-directory/).

- You can't programmatically reset a password for a customer user or full partner user. Use the Azure portal. See [Reset the password for a user in Azure Active Directory](/azure/active-directory/active-directory-users-reset-password-azure-portal). For step 1, you must sign in to the Azure portal for Microsoft Cloud for US Government.

- REST endpoints for Partner Center for Microsoft Cloud for US Government are the same as for Partner Center: `https://api.partnercenter.microsoft.com`.

- Developers must register their app ID manually to integrate Partner Center API/SDK functionality in their app for Partner Center for Microsoft Cloud for US Government. For more information, see [Register app details for Partner Center for Microsoft National Cloud](create-apps-for-partner-center-for-microsoft-national-clouds.md).
