---
title: Finding and Filtering Devices
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Searching a device**](./Finding_and_Filtering_Devices.md)
- [**Filtering devices**](./Finding_and_Filtering_Devices.md)
- [**Using Advanced Search**](./Finding_and_Filtering_Devices.md)
- [**Loading the search queries**](./Finding_and_Filtering_Devices.md)

## Searching a device

The Ivanti Neurons for MDM administrative portal displays the number of duplicate user groups and the corresponding number of GUIDs to identify duplicate groups, when the User Group Name attribute is selected in the rule builder. Also, a table under this rule displays the list of the duplicate user groups and their details such as User Group Name, GUID, Source, and distinguished name (DN).

**Procedure**

1. Go to **Devices**.
2. Type device name in the **Search** field. All the devices that contain the characters are listed.

## Filtering devices

The Filters side navigation bar lists various sections that help you to search for a specific device from the entire list of devices. The Manage Filters wizard contains the list of all the sections that you can select to display in the Filters navigation bar.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Devices**.
:::

:::WorkflowBlockItem
Click the relevant check boxes from the sections that are listed in the Filters side navigation bar.**Example**:
:::

:::WorkflowBlockItem
- From the **User Enabled** section, select **Yes** to display only those devices for which the users are in enabled state.
- If you have assigned custom attributes to devices, you can filter devices based on those attributes by clicking the settings (cog) icon.
- From the **Status** section, select **Retired** and **iOS** to display only retired iOS devices.
  (Optional) Click **Restore Defaults** to restore the selection to the default filters. The Filters navigation bar displays the selected sections. If you clear all the check boxes from the Manage Filters wizard, the Filters side navigation bar displays all the sections.
:::

:::WorkflowBlockItem
Click anywhere outside the Manage Filters wizard to exit the wizard.
:::

:::WorkflowBlockItem
(Optional) Click the x icon to close the Filters side navigation bar and click **Filters** to reopen the side navigation bar.
:::
::::

:::Paragraph{listStyleType="disc" indent="2"}
If you use any of the stop words that are listed in the stopwords.txt file, which is part of the Apache SOLR server configuration, the words will not be indexed, as a result the entities that contain the stop words will not be displayed in the search results.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Examples of entities-devices, users, groups, attributes, applications, certificates, audit trails, content, and notification modules.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Examples of stop words-a, an, if, be, into, and so on.
:::

## Using Advanced Search

You can use the Advanced Search option to search for a device based on rules to identify and view the devices with specific criteria. The rules can be constructed using the applicable operators, including the "begins with", "ends with", "contains", "does not contain", "does not begin with", "does not end with", "is less than", "is greater than", "is in range", "is equal to", and "is not equal to" operators. The rule options can be nested together using the ANY (OR) or ALL (AND) options. The devices matching the rules are displayed below the section.

The Ivanti Neurons for MDM administrative portal displays the number of duplicate user groups and the corresponding number of GUIDs to identify duplicate groups, when the User Group Name attribute is selected in the rule builder. Also, a table under this rule displays the list of the duplicate user groups and their details such as User Group Name, GUID, Source, and distinguished name (DN).

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
From the Devices page, click the **Advanced Search** link. The Advance Search wizard opens.
:::

:::WorkflowBlockItem
Click one of the following options:
:::

:::WorkflowBlockItem
- **Any**-if the devices must match at least one of the rules
- **All**-if the devices must match all the rules
  Create a rule that defines the search criteria. **Example**: APNS Capable is equal to Yes.
:::

:::WorkflowBlockItem
(Optional) Click **+** to create additional rules.
:::

:::WorkflowBlockItem
Click **Search**. The list of devices matching the search criteria are displayed.
:::
::::

:::Paragraph{listStyleType="disc" indent="2"}
For iOS 14.0+ devices, the eSIM ID (EID) of a device is available in the device details page. The eSIM ID (EID) allows the carriers to assign the SIM to a specific device. The eSIM ID (EID) field is GDPR-compliant.
:::

:::Paragraph{listStyleType="disc" indent="2"}
As new GDPR fields (such as IP Address and eSIM ID) are added over Ivanti Neurons for MDM releases, the admins who have already configured GDPR must edit the GDPR profile if they want to hide the new fields.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Advance Search shows the status of the recovery lock of a device.
:::

## Loading the search queries

You can view the list of saved search queries.

**Procedure**

1. Click Advanced search and then click the folder icon. The list of the created search queries are displayed in the **Loaded Query** section and the following details are displayed:\* **Query Name** - The name of the loaded query.
   - **Query Content** - Displays the content on the rules defining the search query.
   - **Actions** - Select the action to be performed on the query.
2. Click **Load Query** in the **Actions** column to view the list of devices matching the criteria defined in the loaded query.
3. Click **Delete&#x20;**&#x74;o delete a loaded query.
