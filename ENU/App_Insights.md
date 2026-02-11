---
title: App Insights
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Viewing app distribution**](./App_Insights.md)
- [**Viewing app details**](./App_Insights.md)
- [**Adding single app distribution charts**](./App_Insights.md)
- [**Adding a unmanaged iOS apps chart**](./App_Insights.md)
- [**Adding top 10 installed managed apps**](./App_Insights.md)
- [**Adding top 5 rated in-house apps**](./App_Insights.md)

App Insights is a feature in the Dashboard that helps you to view and analyze the following app distribution:

- In-house app distribution requiring installation
- Public app distribution requiring installation
- Unmanaged iOS apps
- Top10 installed managed apps
- Top 5 Rated In-House Apps

Analysis of top 5 apps requiring installation: These are In-House or Public apps that have been distributed to a large number of users but have proportionately low installation rates. The Unmanaged iOS apps chart provides information on the unmanaged apps on devices. You will have the ability to see the list of unmanaged apps, on what devices they are installed, and take action to convert the app to a managed app. These are the app distributions that require an administrator's attention or action to improve the distribution. These charts represent the devices that already have the app installed. The doughnut chart provides a high-level overview of the distribution of public and in-house apps which not only helps in analyzing the number of devices requiring app installation, but also allows you to further drill down to get more app specific information by clicking on a specific region of the chart. Additionally, you can also add a single distribution chart that represent a version specific distribution for a single app.

The dashboard only shows information about devices that are checked in the last 15 days.

## Viewing app distribution

In the **Apps** page under **Dashboard**, you can view the following charts:

- In-house app distribution requiring install
- Public app distribution requiring install
- Unmanaged iOS apps

The charts for 5 in-house apps, 5 public and Unmanaged iOS apps are displayed by default. The graphs are ordered left to right starting with the app with the highest uninstalled rate.

The doughnut charts display 2 colors to represent the installation status. The blue color represents the number of devices where the app is installed. The red color represents the number of devices that requires installation. The count of devices are displayed if you hover over each color region.

You can delete a chart by clicking the delete option on top right corner of the chart.

## Viewing app details

The center of the doughnut chart also displays the number of devices that requires installation. Example: 750/1000 which means 750 out of 1000 devices requires installation.

The doughnut charts display 3 colors to represent the distribution of the app.

- The blue color represents represents the number of devices where the app is installed. Clicking the blue region in the chart navigates to the **Devices** page. In the **Devices** page, the **App Version** column displays the installed app version and the date when the app was installed.You can also view devices based on the installed app versions by selecting the options from the **Versions** section in the left panel.
- The red color represents the number of devices requiring app installation. Clicking the red region in the chart navigates to the **Devices** page. In the **Devices** page, you can view devices that requires installation of the app.

An app icon is displayed in the center of the chart. When the icon is clicked, it navigates to the app details page under **Apps> App Catalog**.

In this page, click the **Devices with App installed** tab to view the list of devices for the selected app.

Click the **Devices without App installed** tab to view the list of devices not installed for the selected app.

## Adding single app distribution charts

You can add a single distribution doughnut charts for a specific version of an app in the Apps page. The red color represents the list of eligible devices that should have the app installed. These charts graphically represent the following details of the distribution of apps:

- Devices installed with a specified version of the app
- Devices installed with other versions of the app
- Devices that are not installed with the app

**Procedure**

1. Click **+Add** in the **Apps** page. The **Add App Chart** window is displayed.
2. In the **Chart type** drop-down list select **Single App Distribution**.
3. Select the checkbox for the list of apps for which you wish to view the single app distribution chart.You can alternatively, search for a specific app by typing the app name in the Search for Apps field.
4. Click **Add Chart**. The single app distribution charts are displayed in the Apps page.You can select a maximum of 9 apps from the list.

The center of the chart displays the number of devices that are installed with the specified app version.

Example: 5/10 which indicates that 5 out of 10 devices are installed with the specified app version.

The doughnut charts displays 3 colors to represent the distribution of the app.

- The green color represents the number of devices where the specific version of the app is installed. Clicking the green region in the chart navigates to the **Devices** page that displays the list of devices installed with the specified version of the app. You can also view devices based on other installed app versions by selecting the options from the **AppVersion** section in the left panel.
- The light green color represents the number of devices where other versions of the app is installed. Clicking the light green region in the chart navigates to the **Devices** page that displays the list of devices installed with other versions of the app. You can also view devices based on other installed app versions by selecting the version options from the **AppVersion** section in the left panel.
- The red color represents the number of devices where the app is not installed. The count of devices are displayed if you hover over each color region. Clicking the red region in the chart navigates to the **Devices** page where you can view the devices that are not installed with the app. The left panel also displays the date from when the app is available in the app catalog.

An app icon is displayed in the center of the chart. When the icon is clicked, it navigates to the app details page under **Apps> App Catalog**. In this page, click the **Devices with App installed** tab to view the list of devices for the selected app. Click the **Devices without App installed** tab to view the list of devices not installed for the selected app.

You can delete a chart, by clicking the delete option on top right corner of the chart.

## Adding a unmanaged iOS apps chart

You can identify and view the list of unmanaged apps by adding the unmanaged iOS apps chart to the Apps page. This chart appears automatically when an administrator adds an unmanaged iOS app to the catalog. The administrator can delete or add this chart as needed.

**Procedure**

1. Click **+Add** in the **Apps** page. The **Add App Chart** window is displayed.
2. In the **Chart type** drop-down list select **Unmanaged iOS Apps**.
3. Click **Add Chart**. The unmanaged iOS apps chart is displayed in the **Apps** page.

The chart displays the number of apps in the app catalog that are unmanaged. The bottom of the chart displays 3 columns with the following details:

- **Devices with unmanaged iOS apps** - Indicates the number of unmanaged iOS apps. Click the link to view the list of devices with unmanaged apps in the Devices with unmanaged iOS apps window.
- **Total apps in app catalog** - Displays the total number of apps available in the app catalog.
- **Unmanaged iOS apps (%)** - indicates the unmanaged iOS apps in percentage.

If an app is already installed from iTune App Store, you can convert the app and its data to a managed app.To convert such app to a mananged app:

1. Click the number link in the **Devices with unmanaged iOS apps column**. The **Unmanaged iOS apps** window is displayed.
2. Select one or more unmanaged apps from the list and click on the number link under unmanaged iOS apps. The selected apps will be converted to managed apps and the status will be updated in the next device check-in.You can export the data on the unmanaged apps in CSV format by clicking the **Export to CSV** link.

## Adding top 10 installed managed apps

You can identify and view the list of top 10 installed managed apps using a Top 10 Installed Managed Apps chart in the Apps page. The administrator can delete or add this chart as and when required.

By default, Top 10 installed managed apps chart is available in **Apps** page. If the chart is deleted, the Admin can add it from the **Apps** page.

**Procedure**

1. Click **+Add** in the **Apps** page. The **Add App Chart** window is displayed.
2. In the **Chart type** drop-down list select **Top 10 Installed Managed Apps**.
3. Click **Add Chart**. The Top 10 Installed Managed Apps chart is displayed in the **Apps** page.

You can view the top 10 installed managed apps based on the category selected under the **Show** drop-down list. The available categories are:

- **All Apps** (selected by default)
- **In-House Apps**
- **Public Apps**

Each bar in the chart is displayed in represent each specific app and the name of the app is also displayed. Hover over each bar to view the platform (Android, iOS or Windows) and the number of devices installed with the app.

Clicking the bar of a specific app navigates to the **Devices** page that displays the details of the device(s) installed with the app. The left panel in the Devices page indicates the number of devices installed with the app. Clicking the X button in the left panel navigates back to the **Apps** page in Dashboard.

You can delete the chart by clicking the delete option on the top right corner of the chart.

## Adding top 5 rated in-house apps

You can identify and view the list of top 5 rated In-house apps using the Top 5 Rated In-house Apps chart in the Apps page. The administrator can delete or add this chart as and when required.

By default, the Top 5 Rated In-house apps chart is available in **Apps** page. If the chart is deleted, the Admin can add it from the **Apps** page.

**Procedure**

1. Click **+Add** in the **Apps** page. The **Add App Chart** window is displayed.
2. In the **Chart type** drop-down list select **Top 5 Rated In-house Apps**.
3. Click **Add Chart**. The Top 5 Rated In-house Apps chart is displayed in the **Apps** page.

This chart represent the data via a logo for the App, with the star rating for that App. The star rating is represented by star images, along with the integer representation (maximum rating as 5). The number of users who have rated the App is also displayed.

The number of ratings for an app is not just devices restricted to that administrator and space but its is based on ratings from all users of the app. The rating is the average of all the ratings for that app given by different users who viewed that app from Apps\@Work on their registered devices.

Clicking the specific app navigates to the **App details** page that displays specific details of the app.

You can delete the chart by clicking the delete option on the top right corner of the chart.
