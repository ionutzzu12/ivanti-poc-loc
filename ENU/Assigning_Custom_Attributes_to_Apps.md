---
title: Assigning Custom Attributes to Apps
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

After you create custom attributes, you can assign them to one or more applications. Each attribute has a corresponding value that you can use for tasks such as creating application groups. For more information about managing attributes, see [**Attributes**](./Attributes.md).

## Create and assign a custom attribute for an individual application

You can assign a custom attribute to a single application.

Procedure

1. Log in to the Administrative Portal.
2. Navigate to **Apps** > **App Catalog**.
3. Select an application and click **Attributes**.
4. Click **+Add New** select a value from the **Attribute Name** drop-down menu.
5. Specify the attribute value in the **Value** field.
6. Click **Save**. The custom attribute is added to the application.

## Assign custom attribute to multiple applications

You can assign custom attributes to one or more applications. When you select multiple applications, the custom attribute is applied to every version of the application. You can select a specific application, go to the Attributes tab and change the custom attribute details for a specific application version.

Procedure

1. Log in to the Administrative Portal.
2. Navigate to **Apps** > **App Catalog**.
3. Select check boxes for one or more applications.
4. Click **Actions**.
5. Select **Assign Custom Attributes**. The Assign Custom Attributes to Apps wizard appears.
6. Select *one* of the following options:\* Force assign (overwrite) all attributes even if any existing values are found.
   - Overwrite only if value is empty, and skip attributes with existing values.
7. Select the check boxes for one or more attributes.
8. Specify the value in the Value fields (empty values are not allowed).
9. Click **Assign**. The custom attribute is assigned to all the versions of the selected applications.
10. (Optional)If you want to change the custom attribute for a single application version, select the application version from the version drop-down and click Edit.

The **Custom Apps Attributes** with their values can be used for creating reports and for exporting to CSV format from the **Device Details&#x20;**&#x70;age.
