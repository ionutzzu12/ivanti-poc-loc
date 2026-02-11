---
title: Deploying app dependencies
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

When you upload an in-house application bundle, Ivanti Neurons for MDM scans the application to identify dependencies. If any dependencies are found, it lists them in the third step of the Add App Wizard. For any application dependency, administrators can select to upload a dependency file. However, some applications might not install without uploading the dependency file.

The admin has an option to set app dependency when installing a particular app. In such a case, there can be one or more apps tagged with the main app. When a user tries to install the main app, the user will be notified about the dependent apps that will be installed with the main app.

This feature is supported on iOS, Android, Windows, and macOS devices.

Note the following points about application dependencies and prerequisites:

- The administrator can set the dependent applications that are prerequisites before an application can be installed on a device. A prerequisite application can be an in-house, public, private(Android), or VPP application.
- The count of prerequisite applications are now displayed in the Prerequisite Apps column in the App Catalog page. You can mouse over the number to view the list of prerequisite applications.
- A prerequisite application is downloaded directly once the main application is triggered for installation.
- If a main application is delegated, the associated prerequisite applications are auto-delegated.
- You cannot delete a prerequisite application from the app catalog until the prerequisite relationship is removed.
- Multiple versions of an application can have different prerequisite applications.
- The Audit Trails page logs the addition, removal, and auto-delegation of prerequisite applications for iOS, Android, and macOS.
- If the administrator or end-user installs an application that has prerequisite applications, the prerequisite applications are installed before the main application is installed. If a device check-in takes place before all the prerequisite applications are installed, all the prerequisite applications are uninstalled.

Although an application needs a dependency file, Ivanti Neurons for MDM does not require that you upload any of the files to deploy an app.

For Samsung devices, the admin should add prerequisite apps to the Kiosk Mode Allowed Apps list. The prerequisite apps added to the Allowed apps list do not get added to the Blacklisted apps list.

For non-Samsung devices, if the main app is added to the Kiosk Mode Allowed Apps list, the prerequisite app should run silently in the background. You can view the prerequisite app in kiosk mode only if the admin sets this app in kiosk mode.

**Windows devices** - If the Bridge app is a prerequisite app that is not distributed, and the main app is a .exe that is distributed silently. When the dependency is removed, the Bridge app will be uninstalled, but the .exe fails after this step. Admin should make sure that the Bridge app is not undistributed by default.

**Windows devices** - When the main app is non-silently distributed and the main app has a pre-requisite app with no distribution, the pre-requisite app installs first and is successful. However, in case the main app fails to install, then immediately the pre-requisite app uninstalls. Retry of failed main app happens only when the user triggers an install request.

## Adding an in-house application

1. Go to **Apps > App Catalog**.
2. Click **Add** .
3. Drag the app file to the dotted box, or click **Choose File** to select it from your file system and click **Confirm**.
4. Click **Next&#x20;**(lower right). Ivanti Neurons for MDM scans the app for dependency files and lists them in the **App Dependencies** table.
5. Review the app information and verify that you selected the correct app.
6. Click on the Upload icon in the **Actions** column. The **Upload Dependency** window is displayed.
7. Click **Choose file** to browse and locate a local copy of the file and click **Upload**.
8. Ivanti Neurons for MDM scans optional packages for the app, if any and lists them in the Optional Packages table. If listed, click on the Upload icon in the Actions column. The Upload Optional package window is displayed.
9. Review the app information and verify that you have selected the correct app.
10. Click **Choose file** to browse and locate a local copy of the file and click Upload.
11. Click **Next**.
12. (Optional) Add screenshots of the app and click **Next**
13. If the application requires other prerequisite applications.1) Select the option **On** from the **Prerequisite Apps** section.
    2\) Search for the prerequisite application under the **Add Apps** tab.
    3\) Select the applications.
    4\) Click **Save**.
14. Define app distribution and click **Next**.
15. Define the App Configuration section and click **Done**.The next time the devices sync with Ivanti Neurons for MDM, the app is deployed in the device along with the dependent files.You can add additional dependencies by clicking the Add Dependencies button. When uploaded, these additional dependencies are also listed under the App Dependencies table. The admin can also manually add optional package with content only type. This type of package is not version dependent.

## Adding a prerequisite app

You can add a prerequisite application to a main application. You can add different prerequisites for different versions of a main application. The App Catalog page provides you with the option to either keep the description, scripts, screenshots, distribution, app prerequisites, and app configurations the same as that of the existing application version or change the associated required applications. You cannot delete a prerequisite application without removing the association with the main application.

- The Audit Trail page now displays the supported prerequisite applications in specific fields as follows\:The Prerequisite Applications section for the supported iOS,Android, and macOS applications in the Audit Trails page displays the following fields:\* appVersionId
  - name
  - platformAppIdThe prerequisite applications that are auto-delegated or undelegated containing the following fields are displayed:\* dmPartitionDistributionType
  - dmPartitionDistributionReason

**Procedure**

1. Select an application from **App Catalog**.
2. Click **Edit**.
3. Scroll down to **App Delegation** and select the option **Delegate this app to all spaces**.
4. Click **Save**.If you delegate multiple applications, and choose to remove delegation from the main application, the prerequisite application is not removed from delegation automatically.
