---
title: Finding and Filtering Users
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Searching a user**](./Finding_and_Filtering_Users.md)
- [**Using Advanced Search for users**](./Finding_and_Filtering_Users.md)
- [**Loading the Search queries for users**](./Finding_and_Filtering_Users.md)
- [**Filtering Users**](./Finding_and_Filtering_Users.md)

## Searching a user

Once you have added many users, it can be helpful to use filters or searches to quickly locate a user entry.

**Procedure**

1. Go to **Users**.
2. Type characters in the search box.

## Using Advanced Search for users

You can use the Advanced Search option to search for users based on rules to identify and view the users with specific criteria. The rule options can be nested together using the ANY (OR) or ALL (AND) options. The users matching the rules are displayed below the section. The rules can be constructed using the following operators:

- begins with
- ends with
- contains
- does not contain
- does not begin with
- does not end with
- is less than
- is greater than
- is in range
- is equal to
- is not equal to

Starting from Neurons for MDM 118 the Ivanti Neurons for MDM Administrator displays the number of duplicate user groups and the corresponding number of GUIDs to identify duplicate groups, when the User Group Name attribute is selected in the rule builder. Also, a table under this rule displays the list of the duplicate user groups and their details such as User Group Name, GUID, Source, and distinguished name (DN).

**Procedure**

1. From the Users page, click the **Advanced Search** link.
2. Click **Any** if the users need to match at least one of the rules, or Click **All** if the users need to match all the rules.
3. Create a rule that defines the search criteria, such as User Group, Custom User Attribute and Custom LDAP Attribute.
4. (Optional) Click + to create additional rules, if needed.
5. (Optional) Click **Save** to save the query.
6. Click **Search**. The list of users matching the search criteria are displayed in the page.

## Loading the Search queries for users

**Procedure**

1. From the Users page, click the **Advanced Search** link.
2. Click the 'Folder' icon. The **Advanced Search** window is displayed. The list of the created Search queries are displayed in the **Loaded Query** section. The following details are displayed in this section:\* **Query Name** - The name of the loaded query.
   - **Query Content** - Displays the content on the rules defining the search query.
   - **Actions** - Select the action to be performed on the query.
3. Click **Load Query** in the **Actions** column to view the list of users matching the criteria defined in the loaded query.To delete a loaded query, click the Delete icon.

## Filtering Users

The Filters side navigation bar lists various sections that help you to search for a specific user from the entire list of users. The Manage Filters wizard contains the list of all the sections that you can select to display in the Filters navigation bar.

**Procedure**

1. Go to **Users**.
2. Click the relevant check boxes from the sections that are listed in the Manage Filters wizard. You can search from the following sections:\* Administrators
   - Google Status
   - Invite Status
     - Completed (The user received it and responded.)
     - Expired (The user did not respond in time.)
     - Not Invited (You have not invited this user.)
     - Pending (Pending user response.)
       Password Expiration- Expires (users with password expiration option set to finite date.)
     - Never (users with password expiration option set to never.)
   - User Group (Select the user groups of interest.)
   - User Source\* LDAP
     - Entra ID
     - Roster
     - Salesforce
     - Local
   - Sync\* Direct Sync - Lists the users that were directly synced from the LDAP server
     - No Sync - Lists the users that were removed from the LDAP server
     - Indirect Sync - Lists the users that were indirectly synced from the LDAP server
     - N/A
3. (Optional) Click **Restore Defaults** to restore the selection to the default filters. The Filters navigation bar displays the selected sections. If you clear all the check boxes from the Manage Filters wizard, the Filters side navigation bar displays all the sections.
4. Click anywhere outside the Manage Filters wizard to exit the wizard.
5. Click the x icon to close the Filters side navigation bar and click **Filters** to reopen the side navigation bar.
