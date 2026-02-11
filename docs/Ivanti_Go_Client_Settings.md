---
title: Ivanti Go Client Settings
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

Configure the collection of anonymous end-user data, including device and usage information, to help identify product issues and ensure high service quality. This setting also enables support contact configuration options.

**Applicable to:**

- Mobile\@Work for macOS 1.67 or supported newer versions.
- Go for iOS 3.5.0 or supported newer versions.

## Creating a Ivanti Go Client Settings configuration

**Procedure**

1. Go to **Configurations** > **Add Configuration** > **Ivanti Go Client Settings**. The **Create Ivanti Go Client Settings Configuration** page appears.
2. Enter a name for the configuration in the **Name** box.
3. Enter a **Description** of the configuration.
4. Under **Location based Wakeups**, select the **Enable SLC** option. The significant-change location service offers a more power-friendly alternative to deliver location updates to the Go for iOS app only when the user’s position changes by a significant amount, after a minimum of 15 minutes (default interval). If this service is enabled, then on location change the Go app wakes up in the background and checks in.
5. Under **Data Collection via Analytics for Clients**, select the **Enable Analytics** option if it has been disabled. By default, this option is enabled.
6. Click **Next** to configure the distribution settings.
7. Click **Done**.

## Configure Setup for Support Tab

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configurations** > **Add Configuration** > **Ivanti Go Client Settings**. The **Create Ivanti Go Client Settings Configuration** page appears.
:::

:::WorkflowBlockItem
Enter a name for the configuration in the **Name** box.
:::

:::WorkflowBlockItem
Enter a **Description** of the configuration.
:::

:::WorkflowBlockItem
In the **Configure Setup for Support Tab** section, click **Enable Support Tab**.
:::

:::WorkflowBlockItem
Ensure the Ivanti Go Client version is 118.0.0 or above to enable the Support Tab.Devices with earlier versions will not display or support this feature.

In the **Support Contact Configuration** section, provide the following details:\* **Tab Name** - Enter the name of the tab displayed in the Ivanti app navigation. The default value is 'Support'. (Maximum length: 10 characters)

- **End User Instructions** - Enter the instructions on how to use the support contacts. (Maximum length: 40 characters)
- **Choose Number of Contacts** - Select the number of contacts from the drop down. Default is 1 (Maximum numbers: 5)\* **Enter Field Name** - Enter the contact name. (Maximum length: 20 characters)
  - **Enter Phone Number** - Enter a valid phone number. (Maximum length: 10 characters)
:::

:::WorkflowBlockItem
- **Email Address** - Enter the email where you can send emails for support. (Maximum length: 40 characters)You must enter a valid email address in the format [**alias@domainname.com**](mailto\:alias@domainname.com)
- **Choose Number of URLs** - Select the number of URLs from the drop down. Default is 1. (Maximum numbers: 5)\* **Enter Field Name** - Enter the URL name. (Maximum length: 20 characters)
  - **Enter URL** - Enter a valid URL. (Maximum length: 20 characters)
- **Additional Information** - Enter any additional support-related messages you want to display here. (Maximum length: 120 characters)
  Click **Next** to configure the distribution settings.
:::

:::WorkflowBlockItem
Click **Done**.
:::
::::
