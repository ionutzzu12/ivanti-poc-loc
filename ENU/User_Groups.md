---
title: User Groups
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Creating a dynamically managed user group**](./User_Groups.md)
- [**Creating a manually managed user group**](./User_Groups.md)
- [**Creating a user group from one of the duplicate user groups**](./User_Groups.md)
- [**Creating a user group by CSV file upload**](./User_Groups.md)

Create a user group so that you can assign apps and [**roles**](./User_Roles.md) to multiple users. For example, you might create a Managers group if you want all department managers to be administrators for apps and content.

You can create a user group to be managed in one of the following methods:

- **Dynamically Managed (Most Common):** Local and LDAP users are added/removed to/from a group dynamically based on certain rules and/or attributes.
- **Manually Managed (Limited purpose):** Add/remove users to/from a group manually. Manually managed groups are recommended only for testing purposes that require less permissions.

You can enter text in the **Search** field to display a list of all user groups whose names start with the entered text.

- The search results are displayed as a list of possible matches in real-time while text is being entered.
- Select the desired user group name from the list of possible matches for subsequent action.
- The search match is case insensitive.

## Creating a dynamically managed user group

The following procedure is not applicable to Dynamic User Groups.

**Procedure**

1. Click **+Add**.
2. Enter a user group name in the **Name** field.
3. (Optional) Click **Add Description** to add a description for the user group.
4. Click the **Dynamically Managed (Most Common)** option.
5. Set rules and/or attributes as per your requirements. The following are the available rule options:\* Custom LDAP Attribute
   - msExchPoliciesIncluded
   - msExchMailboxGrid
   - mailNickname
     Default LDAP Attribute
   - samAccountName
   - userPrincipalName
     Default User Attribute
   - email\_address
   - distinguished\_name
   - last\_name
   - display\_name
   - first\_name
   - User Group
   - Custom User Attribute
     User Group DN
   * User Group GUID
   * User Group Name
6. For each rule, select between local and LDAP users. You can include or exclude a sub-group by using the **User Group** filter criteria.
7. Add more rules by clicking the plus icon.You can set **ANY** or **ALL** conditional filters for the added rules.
8. Create a group of rules by clicking the hierarchical icon next to the plus icon.
9. Review the user group's rules and attributes in the text query displayed below the rules selection options.
10. In the **Results** section, review the user(s) details that match the configured criteria. When you add or modify a rule or an attribute you can observe that the matching users are displayed, if they exist.
11. Click **Save** to save the configured user group.

## Creating a manually managed user group

1. Click **+Add**.
2. Enter a group name.
3. (Optional) Click **Add Description** to add a description.
4. Select the **Manually Managed (Limited purpose)** option.
5. In the **Search Users** field, type the email address of each user to be included in the group.As you type, the matching users are found and displayed, if they exist.
6. Select the users you wish to add to the group. You may search and add more users as required.
7. Click **Save**.You can create a manually managed user group and then add this group to a dynamically managed user group. In such a scenario, editing the manually managed user group does not break the dynamically managed user group rule. You will not be able to delete a manually managed user group if it is added to a dynamically managed user group.

## Creating a user group from one of the duplicate user groups

Starting from Neurons for MDM 118 the Administrator portal displays the number of duplicate user groups and the corresponding number of GUIDs to identify duplicate groups, when the "User Group Name" attribute is selected in the rule builder. Also, a table under this rule displays the list of the duplicate user groups and their details such as User Group Name, GUID, Source, and distinguished name (DN).

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Log in to the Ivanti Neurons for MDM Administrator portal.
:::

:::WorkflowBlockItem
Go to **Users**, **User Groups**.
:::

:::WorkflowBlockItem
Click **+Add**. The Create User Group wizard opens.

1. Specify the name in the **Name** field.
2. Select **User Group Name** from the rule builder, select **is equal to**, select *one* of the duplicate group names.
3. Click the **+** plus icon to add more rules.
4. Select **User Group GUID**, **is equal to**.
5. Copy and paste the GUID from the table that displays the list of duplicate user group names and GUIDs. The result displays the associated users who will be added to the new group.
6. Click **Save**. The listed users are now added to the new user group that you created.
:::
::::

If you cannot perform tasks on the **Users Groups** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- System Management
- User Management

## Creating a user group by CSV file upload

The newly added function allows the administrators to create user groups and add users to the created groups using a CSV file.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Log in to the Ivanti Neurons for MDM Administrator portal.
:::

:::WorkflowBlockItem
Go to **Users**, **User Groups**.
:::

:::WorkflowBlockItem
Click **+Add**.
:::

:::WorkflowBlockItem
Select **Import User Groups from CSV**. The Import User Group wizard opens.

1. In the Download CSV section, click **Download CSV Template** to download the CSV template. Using the template, you can edit the file to create user groups and add the users to the new/existing user groups.
2. After editing and saving the CSV file, click **Choose a file** to upload the CSV file.
3. Click **Upload**. A confirmation on the successful upload is displayed.
:::
::::

| Property                     | Description                                                                                                                 |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| CSV File Size Limitation     | The maximum size of the CSV file for import is limited to 2MB.                                                              |
| CSV File Format Requirements | CSV files should contain exactly 2 columns: accountUid and groupName.\* Both accountUid and groupName values are mandatory. |

- Records failing to meet these criteria will be discarded during import.Admins can download a sample CSV file from the import section for reference.               |
  \| Error Handling During Import | If errors or failures occur during CSV import, an error file will be generated.\* Admins can download this error file to review failed CSV rows and understand the reasons for failure.
- The error file includes the specific CSV row that failed and provides an explanation for the failure. |
  \| Successful Import Conditions | Importing users to user groups is successful only when the user group is local and manually managed.\* The user must exist in the system for the import to be successful.                                                                                                                       |

### Conditions for Creating an User Group and Adding an User with a sample CSV file

Sample CSV file details-

**accountUid**: [**test\_user\_1@org.com**](mailto\:test_user_1@org.com)

**groupName**: test\_group\_1

| Conditions                  | Description                                                                                                                                                                                                                                                             |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Existing Group              | If the group test\_group\_1 already exists, the user [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) will be associated with the group.                                                                                                                        |
| Non-Existing Group          | If the group test\_group\_1 does not exist, a new group with the name test\_group\_1 will be created, and the user [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) will be associated with the group.                                                          |
| Non-Local Group             | If the group test\_group\_1 exists but is not a local group, this record will be included in the error CSV file with the reason 'Group is not Local.'                                                                                                                   |
| Non-Manually Managed Group  | If the group test\_group\_1 exists but is not a manually managed group, this record will be included in the error CSV file with the reason 'Group is not manually managed.'                                                                                             |
| Non-Existing User           | If the user [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) does not exist, this record will be included in the error CSV file with the reason 'User not found.'                                                                                               |
| Non-Existing User and Group | If both the user [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) and the group test\_group\_1 do not exist, a new group with the name test\_group\_1 will be created, and this record will be included in the error CSV file with the reason 'User not found.' |
