---
title: Synchronizing and fetching app feedback
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

You can send a request to an app installed on Android devices to get the details of the current app configuration status of the app. When a request is sent, you receive app configuration feedback report for the device.

**Procedure**

1. Go to **Devices**.
2. Click on the device for which you want to send the request.
3. Click **Actions**.
4. Select **Sync and fetch App feedback**.The request is sent to sync and fetch the app configuration feedback. The App Feedback Last Sync field beside Client Last Check-in field will get updated.
5. In the **Installed Apps** tab, click **View Details** link for the app in the **App feedback** column. The **App Feedback** Window is displayed.**Key** - Provides detailed information and provides placement of reported settings (in the Managed app config of the app) based on the feedback received from apps.**Time Stamp** - Time and date of the Key.**Severity** - Specifies the severity of the key. Example: 'Info', 'Error'.**Message** - Type of message received from app config feedback. Example: 'Failure'.**Data** - Details of the data received from app config feedback.

### Viewing app config feedback from the App Catalog

You can view app configuration feedback report for the particular app from the App Catalog.

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select a app for which you wish to view the details.
3. Click the **App Config Feedback** tab. The **Device Count** column displays the number of devices (hyperlink) for each key of the app configuration feedback report.
4. Click on the number of devices hyperlink to view the details of the devices. For example, by clicking on hyperlink 5, displays the details of 5 devices. The following details are displayed for the combination of 'Key' and 'Severity', which is displayed above the table:**Email Address** - specifies the username. Clicking the username link navigates to **Installed Apps** tab under **Devices> Device Detail**.**Device Type** - specifies the device model.**OS** - Android OS version number.**Serial Number** - Serial number of the device.**Time Stamp** - Time and date it was last updated.**Message** - Type of message received from app config feedback. Example: 'Failure'.**Data** - Details of the data received from app config feedback.

You can view the app config feedback error notifications for the Android device by clicking the bell icon (top right) or in the **Dashboard > Notifications** page. Clicking the notification link navigates to **App Config Feedback** tab and view the app feedback report.

The app config feedback report will be removed and will not be displayed when the device is wiped or retired. Background job that runs every 24 hours purges data older than 7 days.
