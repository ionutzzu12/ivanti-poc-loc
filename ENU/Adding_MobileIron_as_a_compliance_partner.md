---
title: Adding MobileIron as a compliance partner
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

**Prerequisites**

- installed a Microsoft Intune license. See [**Apply the Intune license to device users**](./Apply_the_Intune_license_to_device_users.md).
- users created in Microsoft Azure
- groups created in Microsoft Azure

Procedure

1. Login into: [**https://endpoint.microsoft.com**](https://endpoint.microsoft.com/).
2. In the left panel of the Microsoft Endpoint Manager admin center page, click on Tenant Administrator. Click Connectors and Tokens > Partner Compliance Management.

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_01.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_01.png" size="54" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_01.png" githubPath="Resources/Images/AAD_Add MI as comp partner_01.png" position="flex-start" indent="2"}

1. To the right of the Search field, click + Add compliance partner.

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_02.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_02.png" size="65" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_02.png" githubPath="Resources/Images/AAD_Add MI as comp partner_02.png" position="flex-start" indent="2"}

1. In the Basics tab, select MobileIron Device Compliance Cloud from the drop-down of the Compliance partner field.

::Image[]{src="Resources/Images/AAD_compliance partner.png" signedSrc="Resources/Images/AAD_compliance partner.png" size="70" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_compliance partner.png" githubPath="Resources/Images/AAD_compliance partner.png" position="flex-start" indent="2"}

1. In the Platform field, select iOS or Android and then click Next.
2. Click the Assignments tab. In the Assign to drop-down, select the user / group of device users the compliance status is for. Select the user / group that has the license.

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_04.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_04.png" size="19" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_04.png" githubPath="Resources/Images/AAD_Add MI as comp partner_04.png" position="flex-start" indent="2"}

1. Select Next.
2. Click Create. The new compliance partner appears on the Partner compliance management page.

::Image[]{src="Resources/Images/AAD_completed Conn with Azure.png" signedSrc="Resources/Images/AAD_completed Conn with Azure.png" size="63" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_completed Conn with Azure.png" githubPath="Resources/Images/AAD_completed Conn with Azure.png" position="flex-start" indent="2"}
