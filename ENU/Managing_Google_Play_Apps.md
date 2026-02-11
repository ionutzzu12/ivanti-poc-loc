---
title: Managing Google Play Apps
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

You can define which binary from the Google Play app that should be deployed to specific groups or individuals.This deployment is applicable to Android enterprise deployments. The app developer must also Allowlist your organization to be able to deploy alpha or beta channel apps.

1. Click **Apps**.
2. In the **App Catalog** select an app for which to configure the Google Play release configuration.
3. Click **App Configurations** tab.
4. Click **Google Play Release**.
5. Google Release configuration is only applied for Android enterprise apps. By default, Production option is applied if Google release configuration is not selected for newly added apps.
   Click **Add**.
6. Provide a name for the configuration.
7. Optionally, provide a description.
8. Select an option from the drop-down list to select the binary that will be available to users and devices receiving this app. The options are:\* Production
   - Alpha
   - Beta
     Production option is applied by default for apps which are already pushed to the device.
9. Configure the distribution options, selecting from **Everyone with App**, **No One**, or **Custom**.
10. **Custom** distributes the app within the user group along with device filter.
    Click **Save**.

## Prioritizing multiple release configuration

When multiple Google Release configurations are added, you can prioritize the order in which the Google Release configuration should be applied.

1. In **App Configurations**, click **Prioritize Configs**.
2. This button is displayed only when multiple configurations are listed
   From the listed configurations, drag and drop the configuration that should be applied in priority to the top of the list.
3. Click **Update**.
   When the top prioritized configuration is deleted, the configuration that was earlier listed below gets the top priority.
