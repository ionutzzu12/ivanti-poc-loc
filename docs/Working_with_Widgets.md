---
title: Working with Widgets
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Adding a widget**](./Working_with_Widgets.md)
- [**Arranging the widgets**](./Working_with_Widgets.md)
- [**Editing a widget**](./Working_with_Widgets.md)
- [**Reviewing notifications**](./Working_with_Widgets.md)
- [**Reports**](./Working_with_Widgets.md)
- [**Audit Trails**](./Working_with_Widgets.md)

The dashboard shows important statistics about registered devices and users. Each section on the dashboard is called a widget. For each widget, you define:

- the category of data displayed (such as devices or users)
- how the data is grouped (such as by OS version or model)
- how the data is filtered (such as displaying only iOS devices)
- how the data is displayed (such as the pie chart or bar chart)

## Adding a widget

1. Click **Add** (upper right).
2. Assign a name to the widget.
3. Select a data category.
4. Complete the filtering options as they display.
5. Select the default display type (pie chart, bar chart, line graph).
6. Click **Done**.

## Arranging the widgets

Widgets always display three to a row. However, you can change the order in which the widgets are displayed:

1. Click **Arrange** (upper right).
2. Drag the boxes into the order in which the widgets should appear.
3. Click **OK**.

## Editing a widget

1. Click the settings icon for the widget (upper right).
2. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/gPJDxgXlmW-XhaYj36hCk_editdash.png" alt caption}
   Select **Edit**.
3. Make your changes.
4. Click **Done**.

## Reviewing notifications

Click the bell icon (top right) or go to **Dashboard > Notifications** page to review notifications and take actions where necessary based on the following criteria:

- Component Type
  - APP
  - LDAP
  - Entra ID
  - Device Allowlist
  - Apps and Books
  - iOS
  - Android
  - macOS
  - visionOS
  - watchOS
  - Tenant
  - CA
  - Connector
  - Sentry
  - Device Enrollment Server Token
    Notification Type
  - Expiration
  - Data Sync
  - Usage Limit
  - Admin Action
  - Server Authentication Error
  - Validation Error
  - Status Change
    Severity
  - Cleared
  - Information
  - Critical
  - Warning

Admins can select the APP component to quickly review all app-specific notifications on the Notifications page and also in the bell notification section. If there are new permissions to be accepted for Google Play apps, then the admins can accept them upon clicking the notifications rather than visiting each app page to review and accept the permissions.

Ivanti Neurons for MDM customers/tenants will get the Android Go app approval notifications even though the Android Go app is not imported into the App Catalog.

### Reviewing user password expiration and ID change notifications

Admins can review the upcoming password expiration in the **Notifications** page. They are also notified of the password expirations from two weeks to one day in advance, including links to CSV report files containing the list of corresponding users. After the password expires, notifications will no longer be generated.

Admins can also review a notification that lists the users whose IDs (UIDs) were detected to have changed during the last LDAP sync.

Clearing a notification

You can manually clear these notifications of any severity whenever required from the **Notifications** page.

1. In the **Notifications** page, click on the icon in the **Actions** column for the notification you wish to clear. The **Confirm Clear Notification** window is displayed.
2. Click **Clear Notification**. When cleared, the status of notification changes to **Cleared** in the **Status** column.The total count of the notifications that are cleared are displayed in the **Notifications** page.

## Reports

On the **Dashboard > Reports** page, you can access the data in your Unified endpoint management (UEM) system. For example, administrators can add information such as Device Space Name and Device Custom Attributes to reports using the corresponding filter option while creating Devices and Blocked Devices reports. Accordingly, these reports have columns for Device Space Name and Device Custom Attributes respectively. Custom Device Attributes are available under filtering options while creating a report. Administrators can pick from the list of custom device attribute keys used for devices and select the available operators.

Starting with Ivanti Neurons for MDM 76, the operators for all the report templates have standard operators. The operators of the following templates are standardized in this release:

- Dashboard> Reports> Create Report

The following is the workflow of a report:

1. Choose - select from a predefined report template.
2. Define Scope - set the period of time for report data.
3. Set Details - name and customize your report.
4. Run or schedule - run the report immediately or create a schedule.
5. Share - specify who will receive your report.

**Related topics**:

- [**Dashboard > Reports (Scheduled)**](./Using_Scheduled_Reports.md)
- [**Dashboard > Reports (Custom)**](./Using_Custom_Reports.md)

**Quick Search:** Navigate to the Reports tab. The quick search field lets you search from the following columns, it lets you search even if you include space or special characters:

- NAME
- DESCRIPTION
- TEMPLATE NAME

## Audit Trails

Audit Trails is a chronological set of records which captures activities performed on all entities within Ivanti Neurons for MDM - by all actors including administrators, end-users and by various components of the system itself. Starting with Ivanti Neurons for MDM release 80, Audit Trails is enabled by default for all tenants. The tenant can opt-in or out of Device Check-in Audit Trails. For the tenants that were enabled with Audit Trails prior to R80, the check-in events stay enabled. For all other tenants' devices, the check-in trails are disabled. When you re-register an Android device, the Audit Trails page displays the currently registered device status as Re-Registration Device Action performed and the previous entry as Retired Device Action performed. For more information, see [**Device Registration (iOS, macOS, and Android)**](./Device_Registration__iOS__macOS__and_Android_.md).

The following activities are tracked:

- Adding, retiring, wiping, deleting, and updating devices
- Force Check-in on devices
- Changing device ownership
- Creating, updating, and deleting user setting (Device Registration, Device Limit, and Terms of Service settings)
- Locking and unlocking devices
- Creating, editing, deleting and prioritizing configurations
- Creating, editing, and deleting policies
- Changes in the distribution group of configurations.
- Creating, editing, and deleting a user (does not include LDAP user creation).
- Creating, editing, and deleting a user group.
- Creating, editing, and deleting distribution filters.
- Creating, editing, and deleting LDAP server.
- Synchronizing with LDAP server in the following scenarios:\* LDAP Sync Start
  - LDAP Sync Success
  - LDAP Sync Discard (occurs when the number of users deletion exceeds the configured threshold value).
  - LDAP Sync Partial Discard (occurs when there are failed entries during sync)
  - LDAP Server added
  - LDAP Server edited
  - LDAP Server deleted
  - LDAP Server Sync started
  - LDAP Server Sync failed
  - LDAP Server Sync completed
- Creating, editing, and deleting apps.
- Creating, editing, and deleting app configurations.
- Creating, editing, and deleting [**scripts**](./All_Scripts.md).
- Deleting Admin LDAP entity.
- Modifying LDAP preferences.
- Uploading LDAP certificate.
- Application icon change.

### Enabling Audit Trails

You need to turn on the Audit Trails feature to capture activities performed within Ivanti Neurons for MDM.

1. Select **Admin > Infrastructure > Audit Trails**. The **Audit Trails** page is displayed.
2. Click **Enable Audit Trails**. The **Enable Audit Trails?** window is displayed to confirm your action to enable Audit Trails.
3. In the **Enable Audit Trails?** window, click **Enable Audit Trails**.You will not be able to disable the Audit Trails feature after you enable it. To disable, contact support.
4. In the **Export Audit Trails** field, slide the toggle bar to **ON** to configure the export of Audit Trails. Audit Trails export is used to export and upload all the Audit Trails information to a specific server location. The Audit Trails export is performed through SSH File Transfer Protocol (SFTP). The server should be accessible from the default port. Users can configure Audit Trails export settings to get archives of Audit Trails automatically uploaded to a specific location on a daily basis. For more information, see [**Exporting Audit Trails**](./Exporting_Audit_Trails.md).

### Viewing Audit Trail activities

You can view the tracked activities in the **Audit Trails** page under **Dashboard**. If a row item extends beyond the default column width and is hidden due to the column border, an ellipsis is displayed, and when you mouse-over on the ellipsis the complete row item is displayed as a tooltip.

The following details are displayed in this view:

| Column name   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name          | Name of the device or the name of the user setting. For example, for device activities, it displays the device name. Clicking the hyperlink navigates to the activity details page.If there is a user associated with the device, the device owner user name is also displayed under the device name.Clicking the **Go to Device** link icon next to the name of the device to navigates to the device details page. In the Device Details page, you can click on the **Go to Audit Trails** hyperlink to view the activity details page for Audit Trails. |
| Type          | Type of activity that is triggered.Example: 'Account' for a login activity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Category      | The category of the activity.Example: Config, Policy.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Last Activity | The activity that was last performed.Example: Create, Delete.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Last User     | The user who performed the activity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Performed At  | The date and time of the performed activity is visible in only 24 hour format.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

**Activity details view**

The Activity Details View (inner layer) is accessed by clicking on the link under the **Name** column in the Entities View and it lists all historical activity trails concerning that entity. The following details are displayed in this view. If a row item extends beyond the default column width and is hidden due to the column border, an ellipsis is displayed, and when you mouse-over on the ellipsis the complete row item is displayed as a tooltip.

| Column name                  | Description                                                                                                        |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Time of Action**           | The duration lapsed from the time the action was performed.                                                        |
| **Activity**                 | Describes the specific action performed.Example: App added to App Catalog.                                         |
| **Performed By**             | The user who performed the activity.                                                                               |
| **Changes - Before & After** | Click the icon to view the Audit Trail comparison details in the **Audit Trails Changes - Before & After** window. |

The following details appear in the **Audit Trails Changes - Before & After** window.

| Column name   | Description                                                         |
| ------------- | ------------------------------------------------------------------- |
| **Attribute** | Displays the name of the modified attribute.Example: **createdAt**. |
| **Before**    | Attribute values before the action was performed.                   |
| **After**     | Attribute values after the action was performed.                    |

Using the **Customize columns** setting icon displayed on top right of the column header, you can select or unselect the checkbox for the relevant column name to display/hide the columns in the list view.

### Filtering Audit Trail activities

Using the **Filters** option you can filter and view the list of Audit Trail activities. The following are the available filtering options:

| Filtering Options                               | Description                                                                                                                                                                                                                                                                                                                                                                      |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Filter by Date Range**                        | Select the date range from the Start Date and End Date fields. When the range is selected, the list of Audit Trail activities performed within the selected date range are listed. This filter option is available in any of the view options (Grouped or Expanded).Only a maximum of 15 days is allowed to be selected as the date range with the end date as the current date. |
| **Category**(Applicable only in Expanded  View) | Select the category from the following options:\* Policy                                                                                                                                                                                                                                                                                                                         |

- Device Management
- User Management
- User Setting Management
- LDAP
- Config
- Admin Portal Access
- App Management
- **Azure Device Compliance**The Category column is hidden by default in expanded view.                                                                                                           |
  \| **Type**(Applicable only in Expanded  View)     | Select the following **Entity type** options:\* **Account**
- **Device**
- **Registration Auth**
- **Device Limit**
- **Terms of service**
- **Compliance Report**The Type column is hidden by default in expanded view.                                                                                                                                                          |
  \| **Activity**(Applicable only in Expanded View)  | Select the specific activities you wish to view. The following are the options:\* **Delete**
- **Distribution Update**
- **Force Checkin**
- **Clear config Error**
- **Retire**
- **Login**
- **Update**
- **Update Owner**
- **Wipe**
- **Lock**
- **Update Intune Compliance**                                                                                                 |
  \| **Name**(Applicable only in Expanded  View)     | Filter by the name of the device or the name of the user setting.                                                                                                                                                                                                                                                                                                                |
  \| Performed By                                    | Filters by the users who performed the action.                                                                                                                                                                                                                                                                                                                                   |
  \| Status                                          | Filters by the login status.The following are the options:\* **Success**
- **Failure**                                                                                                                                                                                                                                                                                            |

The order of display is based on the time when the activity was performed.

Using the **Customize columns** setting icon appearing on the top right of the column header, you can select or unselect the checkbox against the relevant column name to show/hide the columns in the list view.

By default, the pages lists 50 activities are listed in the page. If there are more than 50 activities, you can click **Next** button at the bottom of the page to view more activities. Alternatively, you can also click the relevant display option in the **Show** field located at the bottom of the page. For example, click **100** to display the list of most recent 100 activities.

### Searching for Audit Trail activities

Using the Search field, you can find and view the list of Audit Trail activities based on the keyword entered. Currently, when you perform a quick search the whole string is indexed including the property names. Starting with Ivanti Neurons for MDM 76, only property values are indexed. Users need not provide details keys present under the details column while performing quick search. The keyword entered can be the values applicable to any of the following columns:

- **Activity** (device name or the user name)
- **Type**
- **Category**
- **Performed By**
- **Details**

The values in the Activity column are not searchable.

The displayed result will also include the Audit Trail activities having any part of the column values matching with the entered keyword.

## Using Advanced Search for Audit Trails

You can use the Advanced Search option to search for audit trails based on rules to identify and view the activities with specific criteria. The rule options can be nested together using the ANY (OR) or ALL (AND) options. You can use the following attributes to perform the search:

- **Activity**
- **Category**
- **Created At**
- **Performed By**
- **Performed On**
- **Status**
- **Type**

The activities matching the rules are displayed below the section. The rules can be constructed using the following operators:

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

**Procedure**

1. From the Audit Trails page, click the **Advanced Search** link.
2. Click **Any** if the activities need to match at least one of the rules, or Click **All** if the activities need to match all the rules.
3. Select the attribute and the relevant operators to create a rule that defines the search criteria.
4. (Optional) Click **+** to create additional rules, if needed.
5. (Optional) Click **Save** to save the query.
6. Click **Search**. The list of audit trail activities matching the search criteria are displayed on the page.
7. (Optional) You can also delete the saved query.

## Exporting Audit Trails to a CSV file

You can export the Audit Trail records using the Export to CSV option from the Audit Trails page.

**Procedure**

1. Go to **Dashboard&#x20;**>**&#x20;Audit Trails**.
2. Click the **Actions** drop-down menu and select **Export to CSV** option. Alternatively, you can filter by date range before you select the Export to CSV option.A pop-up message appears that the export report would take some time to process. Wait for the request to complete before you submit another request.
3. Click **Download**. You will receive an email containing a link to download the report.
4. (Optional) Click **Delete&#x20;**&#x74;o delete the report.

If you cannot see the **Dashboard** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- System Management
- System Read Only
