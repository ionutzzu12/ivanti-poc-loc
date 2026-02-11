---
title: Configuring LDAP server
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

## License: Silver

Configuring an LDAP server and a Connector enables you to import users and groups from your corporate directory. After you have installed at least one Connector, you can add one or more LDAP servers.

Adding an LDAP server means configuring:

- the *connection* to the LDAP server
- the *search terms* necessary to view the target directory data
- the portion of the directory to *import*
- whether to automatically *invite users* in the selected portion of the directory

After you have added an LDAP server, you can return to this page to [**edit the LDAP server information**](./Configuring_LDAP_server.md) or [**change the LDAP users selected**](./Configuring_LDAP_server.md).

LDAP users must be imported after configuring an LDAP user. See [**Importing LDAP users**](./Configuring_LDAP_server.md).LDAP usernames, just like local usernames, must be globally unique. Please verify that users do not already have a local account with the same username, or, for organizations with more than one tenant, that the username has not already been associated with another tenant.

## Adding an LDAP server

Procedure

::::WorkflowBlock
:::WorkflowBlockItem
Click **+Add Server**.
:::

:::WorkflowBlockItem
Provide the following information:
:::

:::WorkflowBlockItem
| **Setting**   | What To Do                                                                                                                                                 |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name          | Enter a name that identifies this server.                                                                                                                  |
| Description   | Enter a description that clarifies the purpose of this server.                                                                                             |
| Directory URL | Enter the URL for the directory. Use one of the following formats\:ldap\://IP address orldaps\://IP address orExample: ldap\://myserver1.mycompany.com:389 |
| User ID       | Enter the user ID for an account with the following characteristics:\* managed by the LDAP server                                                          |

- can bind to the LDAP server and search the subtrees for user, group, and organizational unitThis is generally an account with Directory Administrator Credentials (DN or Distinguished Name and password). |
  \| Password         | Enter the password for the account.                                                                                                                                                                                                                                                                           |
  \| Confirm Password | Re-enter the password for the account.                                                                                                                                                                                                                                                                        |
  \| Directory Type   | Select the type of directory from the list of supported directories.\* Microsoft Active Directory
- Open LDAP
- Other (Open LDAP compatible)                                                                                                                                                                   |
  Click **Test Connection and Continue**.
:::

:::WorkflowBlockItem
This step validates the information you have provided so far.

- If the information proves valid, then the service retrieves the LDAP naming context, which it uses to fill in some of the fields on the next page.
- If the LDAP URL fails to connect, you can proceed with the next steps. However, this may result in limited functionality until the connection is resolved.
  Complete the remaining settings:
:::

:::WorkflowBlockItem
| Setting                                                 | What To Do                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Directory Failover URL                                  | Enter the URL for the secondary directory. Use the following format\:ldap\://IP address orExample: ldap\://myserver2.mycompany.com:389                                                                                                                                                                                                                                                                                   |
| Sync Interval                                           | Enter the period of time between each attempted synchronization of LDAP data from the LDAP server. The default value is 15 minutes. Consider increasing the interval after you have successfully synchronized all target LDAP data and confirmed that your LDAP setup meets your needs.                                                                                                                                  |
| [**Enable Sync Discard**](./Configuring_LDAP_server.md) | Select to automatically discard the LDAP sync data if the reloaded data set declines significantly. This option ensures that abnormal behavior on the part of the LDAP system will not result in unnecessary, disruptive updates on the service and removal of configurations from registered devices. Make sure this option is not selected if you plan to make major changes in your LDAP setup or on the LDAP server. |
| Enable this LDAP Server                                 | Select to use this LDAP server with your service. Clear this setting if you want to retire this LDAP server or take it out of service. Though a configured failover to a second LDAP server would automatically replace this server, using this option enables you to plan ahead and avoid a brief lack of connectivity during failover.                                                                                 |
| Automatically invite users whenever they are imported   | Select to automatically send invites to the users when they are imported from the LDAP server.                                                                                                                                                                                                                                                                                                                           |
| Upload CA Certificate                                   | Click **Choose File** to upload the TLS certificate issued by the CA installed on this LDAP server. You can upload multiple CA certificates.                                                                                                                                                                                                                                                                             |
| Chase Referrals                                         | Applies only if you are using a multi-forested domain. This option indicates whether you want to use alternate domain controllers when the targeted domain controller does not have a copy of the requested object.\* Select **Follow** if you want to use referrals.                                                                                                                                                    |

- Select **Ignore** if you do not want to use alternate domain controllers.
- **Throw** currently has the same effect as **Ignore**.Selecting **Follow** delays LDAP authentication.                                                                                                                                                                                       |
  \| Search Results Timeout                                           | Increase this timeout if you observe performance issues or incomplete results when browsing the data synchronized from the LDAP server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
  \| Search Results Count                                             | Set to the maximum number of records that should be returned from the LDAP server at one time. Scenarios that might require changing this setting to improve performance include:\* The LDAP server is located far away or behind a high latency link. In this case, large search results will take longer to retrieve than small ones, so defining a smaller set enables you to see subsets of updated data more quickly.
- The LDAP is massive, and every search returns a huge results set. In this case, if performance is not an issue, defining a larger results set would make it possible to return all of the data with fewer searches. |
  Click **Next**.
:::

:::WorkflowBlockItem
Use the following guidelines to configure the integration with the LDAP server:
:::

:::WorkflowBlockItem
| **Setting**            | What To Do                                                                                                                                                                                                |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Group Member Format    | Select **DN** or **UID** to indicate whether to use the distinguished name or the user ID in your search.                                                                                                 |
| *OU Search Attributes* | Specify criteria for searching at the organizational unit level.                                                                                                                                          |
| Base DN                | Enter the distinguished name for the starting level at which you want your search to be rooted or begin. Your selection determines defaults for several other fields, which you can change, if necessary. |
| Object GUID            | If necessary, change the default value to match your LDAP environment. This is the attribute that uniquely identifies an organizational unit across time and across OU name changes.                      |
| Attribute Name         | If necessary, change the default value to match your LDAP environment.                                                                                                                                    |
| Description            | If necessary, change the default value to match your LDAP environment.                                                                                                                                    |
| Attribute DN           | If necessary, change the default value to match your LDAP environment.                                                                                                                                    |
| Search Filter          | If necessary, change the default value to match your LDAP environment.                                                                                                                                    |
| Search Scope           | Select the portion of the LDAP hierarchy to target:\* **Base** (only the level of the search base entry)                                                                                                  |

- **One Level** (the level beneath the search base)
- **Subtree** (the subtree in the directory information tree beneath the search base DN)                                                                                                                                                                                                                                                     |
  \| *User Search Attributes*  | Specify criteria for searching users in a given directory level.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
  \| Base DN                   | Enter the distinguished name for the starting level you want to search.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Attribute UID             | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Object GUID               | If necessary, change the default value to match your LDAP environment. This is the attribute that uniquely identifies an user across time and across user name changes.                                                                                                                                                                                                                                                                                                                                  |
  \| Attribute DN              | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| First Name                | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Last Name                 | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Display Name              | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Email Address             | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Principal Name            | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Locale                    | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Member Of                 | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Search Filter             | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Search Scope              | Select the portion of the LDAP hierarchy to target:\* **Base** (only the level of the search base entry)
- **One Level** (the level beneath the search base)
- **Subtree** (the subtree in the directory information tree beneath the search base DN)                                                                                                                                                                                                                                                     |
  \| Managed Apple ID          | Choose to sync Managed Apple ID for the LDAP users.\* **None**
- **Pattern&#x20;**-
  - **User email address**
  - **userUPN**
    Optionally, select the **Include "appleid" subdomain** option to avoid conflict with existing Apple IDs.                                                                                                                                                                                                                                                                 |
    \| +Add Custom Attribute     | (Optional) Specify up to 7 custom user attributes from your directory service that you want to apply to device management. Each attribute can then be referenced by $\{attributeName} in configuration fields that support variables.**Important:** Use of this option requires consistent implementation of custom attributes across LDAP servers. If an LDAP server included in your implementation does not use this attribute, then features dependent on this attribute might not work as expected. |
    \| *Group Search Attributes* |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
    \| Base DN                   | Enter the distinguished name for the starting level you want to search.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
    \| Object GUID               | If necessary, change the default value to match your LDAP environment. This is the attribute that uniquely identifies a group across time and across group name changes.                                                                                                                                                                                                                                                                                                                                 |
    \| Attribute DN              | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
    \| Attribute Name            | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
    \| Description               | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
    \| Member                    | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
    \| Search Filter             | If necessary, change the default value to match your LDAP environment.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
    \| Search Scope              | Select the portion of the LDAP hierarchy to target:\* **Base** (only the level of the search base entry)
- **One Level** (the level beneath the search base)
- **Subtree** (the subtree in the directory information tree beneath the search base DN)                                                                                                                                                                                                                                                     |
  Click **Browse** or **Search**.
:::

:::WorkflowBlockItem
Confirm that your configuration returns the expected data.
:::

:::WorkflowBlockItem
You can do this by browsing or searching for a known item in the directory.

Click **Next**.
:::
::::

## Deleting a custom LDAP attribute

You can delete a custom LDAP attribute and remove its values from the associated users or devices.

Procedure

1. Go to **Admin > Attributes**.
2. In the **Custom Attributes** section click on the **Delete** link next to the LDAP attribute that should be deleted. A confirmation window is displayed.
3. Click **Delete** to confirm deletion.that the **Delete** button is disabled by default. You should select the check box in the **I understand that deleting a Custom Attribute cannot be reversed** option to enable the **Delete** button.

## Editing the LDAP server information

Procedure

1. Go to **Admin > LDAP**.
2. In the LDAP server entry, select the **Edit** icon from the **Actions** column to view the Connect LDAP Server page.
3. Make the necessary changes.
4. Click **Test Connection and Continue**.If the LDAP URL fails to connect, you may proceed with the next steps. However, this may result in limited functionality until the connection is resolved.
5. Click **Browse** or **Search**.
6. Confirm that your configuration returns the expected data.You can do this by browsing or searching for a known item in the directory.
7. Click **Done**.

## Importing LDAP users

Procedure

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Users**.
:::

:::WorkflowBlockItem
Click **+Add > Invite Users from LDAP**.
:::

:::WorkflowBlockItem
Click **Select Users** in the LDAP server entry.
:::

:::WorkflowBlockItem
In the Add LDAP Users page, enter the name of the user, group, or OU in the search field.
:::

:::WorkflowBlockItem
To add new users or groups, click **+Add** next to the entry you want to add.
:::

:::WorkflowBlockItem
Click **Next**.
:::

:::WorkflowBlockItem
Choose whether or not to send the invitation:
:::

:::WorkflowBlockItem
- Invite NoneTo send the invites later, go to **Users > Users** and select **Actions > Send Invite** to send the invitations.
- Invite All
  Click **Done**.
:::
::::

## Updating the users, groups, or organizational units selected

Procedure

1. Go to **Admin > LDAP**.
2. In the LDAP server entry, select the **Manage Users** icon  from the **Actions** column to view the Add LDAP Users page.
3. To add new users or groups, enter the name of the user or group in the search field.
4. Click **+Add** next to the entry you want to add.
5. To remove a user, group, or OU, click the remove icon next to the entry you want to delete.
6. Click **Done**.

## Enabling LDAP Sync Discard Notification

Enabling LDAP sync discard notification helps prevent outages caused by unintended large scale changes to the LDAP environment.

Procedure

1. Go to **Admin > LDAP**.
2. In the LDAP server entry, select the **Edit** icon from the **Actions** column to view the Connect LDAP Server page.
3. Check the **Enable Sync Discard** check box.
4. Enter a value for the percentage of reloaded LDAP data to trigger sync discard.
5. Click **Test Connection and Continue**.If the LDAP URL fails to connect, you can proceed with the next steps. However, this might result in limited functionality until the connection is resolved.
6. Click **Done**.
7. Click the **Sync Now** icon in the LDAP server entry.When the change difference to be synced from LDAP to Ivanti Neurons for MDM falls above the set discard percentage, a WARNING notification is generated. When the changes are reverted to a value below the set percentage, the notification is CLEARED.

| Trigger            | Severity | Notification Type | Component Type | Component        |
| ------------------ | -------- | ----------------- | -------------- | ---------------- |
| LDAP Sync Discard  | Warn     | Data Sync         | LDAP           | LDAP server name |
| LDAP Sync Restored | Info     | Data Sync         | LDAP           | LDAP server name |

The Partial Sync Discard Notification is generated when one or more user records fail to sync from LDAP. In this case, a CSV file is included as an attachment with a list of users that failed to sync. If a user was discarded due to missing attributes, the list of missing attributes is also included in the exported CSV file.

## Synchronizing changes from the LDAP server

In the LDAP page, click the **Sync Now** icon in the LDAP server entry.

If the display name is more than 128 characters, the LDAP sync will ignore such a user and proceeds with other users or user groups sync.

## Troubleshooting Connectivity to the LDAPS Server

If you encounter issues connecting to the LDAPS (LDAP over SSL) server, you may be experiencing an issue with the certificate.

To resolve the issue:

- Verify that you are not using a self-signed certificate on the LDAPS server.
- Verify that the LDAPS certificate has not expired or been revoked. Also check for a hostname mismatch.

After verifying, wait for the automatic LDAP sync, or manually sync using the **Admin > LDAP > Sync Now** icon in the LDAP server entry.

If you cannot see the LDAP page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- System Management
- System Read Only
