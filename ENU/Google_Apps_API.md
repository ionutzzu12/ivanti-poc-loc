---
title: Google Apps API
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Google customers who use Single Sign On (SSO) to authenticate user access to Google Apps services may not be able to use Exchange to connect users to email, contacts, and calendar due to limitations in the protocol that prevent devices from supporting SSO-triggered redirects to external authentication services. This service addresses this condition by creating and managing account passwords for ActiveSync connectivity.

**Prerequisites**

Before attempting to configure the Google Apps API feature, you need:

- Admin access to an account on [**https://console.developers.google.com/**](https://console.developers.google.com/).
- Admin access to an account on [**https://admin.google.com**](https://admin.google.com).

## Enabling the Google Apps API feature

Procedure

1. Select **Admin > Google > Google Apps API**.
2. Click **Step 1: Google Dev** at the bottom of the rectangle on the left labeled 1.
3. The Step 1: Google Dev page appears.
   Follow the instructions that appear on the Step 1: Google Dev page, and then click **Done**.
4. Click **Step 2: Google Admin** at the bottom of the middle rectangle labeled 2.
5. The Step 2: Google Admin page appears.
   Follow the instructions that appear on the Step 2: Google Admin page, and then click **Done**.
6. Enter the Google Admin user name in the **Enter the Google Admin user name** field in the rectangle on the right labeled 3.
7. In the same rectangle, click **Choose File** to upload the JSON file you downloaded in Step 1.
8. Click **Save**.
9. If you cannot see the Google Apps API page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):
   - System Management
   - System Read Only
