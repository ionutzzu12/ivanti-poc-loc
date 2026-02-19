---
title: Android File Transfer Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

As part of Android 11, Google made significant changes in storage access on a device from apps, which also impacted how enterprises manage to send files to specific apps on these devices. With these changes in mind, many large enterprises face challenges in distributing files to devices and apps as devices are upgrading to Android 11 and beyond. Any approach that is dependent on specific APIs from hardware vendors limits enterprises in having the same approach across different devices from different manufacturers and OS versions.

Ivanti developed a file transfer solution that is agnostic for the Android version and hardware vendor. This solution relies on Android’s standard *Content-Provider* capability. *Content-Provider* allows Ivanti's Go app to generate a unique on-device location for each file pushed via UEM.

The File Transfer Configuration is available for Android devices in Fully Managed device mode. Using this configuration, the administrator can provide an option to transfer files on the device to be shared between different allowed apps present on the same device. Other apps can use the files for whatever reason needed. An example use case is initializing app configuration using JavaScript or displaying corporate information using PDFs or videos. Every file uploaded into Ivanti's File Transfer configurations is downloaded by Ivanti Go when it receives the corresponding config and associated file. The file is securely stored within Ivanti Go.

Other apps cannot access this file arbitrarily.

Every downloaded file inside the app sandbox is referenced by a unique location, also referred to as *ContentURI* or *URI*. Custom Attributes are used to hold the ContentURI value on the server for every file on a device and can help administrators determine a file’s availability on device, form dynamic device groups, and are required to communicate ContentURI to target app using managed app configuration, etc.

For non-Ivanti apps, administrators should check with third-party app developers on their support for this approach which is commonly referred to as "Consuming FileProvider based ContentURI."

**Prerequisites**:

- Add a new device-based custom attribute to be used for File Transfer operation. For every File transfer configuration, a unique custom attribute should be created. Each custom device attribute can only store the contentURI (location of file) from device for one file per config.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configurations** > **Add Configuration** > **File Transfer**. The **Create File Transfer Configuration** page opens.
:::

:::WorkflowBlockItem
Enter a name for the configuration in the **Name** box.
:::

:::WorkflowBlockItem
Enter a **Description** of the configuration.
:::

:::WorkflowBlockItem
**Configuration Setup**

In the **File to Transfer** section, select the files to be transferred using the Drag and drop option or browsing through the **Choose File** option. By default, the maximum limit of file size is 50 MB.
:::

:::WorkflowBlockItem
Select one or more of the following **Download to device** options (optional):\* **Allow download over a metered network** - Select to continue downloading the file even on a metered network

- **Require charging** - Select to make sure that the device is charging during the file transfer process
- **Require device idle** - Select to keep the device idle during the file transfer process
:::

:::WorkflowBlockItem
Use one of the following two options to share a file with other apps

- **Transfer using Android Managed App Config**- Use this option only if the target app can consume Content URI using its Managed App Config.
- **Transfer using On-device Intent** - Intents are app-specific. To share a file using this option, see the target app's documentation and provide information in the intents section below. Intents allow Ivanti Go app to broadcast a message on the device once the file is available to be shared with the apps.
:::
::::

### Transfer using Android Managed App Config

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
In the **Choose an existing device based custom attribute to share this file with other apps** field, enter an existing attribute name, for example, **Custom-Filename**. For more information, see [**Assigning Custom Attributes to Devices**](./Assigning_Custom_Attributes_to_Devices.md).
:::

:::WorkflowBlockItem
The custom attribute name should be new, unique attribute solely used for this file transfer operation. Each custom device attribute can only store the contentURI (location of file) from device for one file per config.

**Provide access to the following apps and / or package names**: You can select app names from the App Names selector and add Package Names.
:::

:::WorkflowBlockItem
These will be the only authorized packages allowed to access the file.

- **App Names** - You can select app names from the App Names selector.
- **Package Names** - You can enter the Bundle IDs in this area, for example,com.mobileiron.filetransfer.android3.Separate multiple package names with semicolons(;).
  Click **Save**. The new File Transfer configuration appears on the Configurations page.
:::
::::

### Configuring the target app

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select the target app that will receive the file.
3. Navigate to **App Configurations > Managed Configurations for Android**.
4. Create a new configuration or use an existing configuration.
5. An app may have a setting such as "Manifest Info" or other properties where the administrator can define the substitution variable and communicate the location of the file to the target app. For Ivanti Velocity app as an example, in the App Configuration dialog box > **Fetch Configurations**&#xNAN;**> Manifest Info** field, enter the substitution variable. For example, $Custom-File-Name$.
   Select your distribution.
6. Click **Save**.

### Transfer using On-device Intent

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
In the **Choose an existing device attribute to pass file path in intents extras** field, enter a new custom attribute name, for example, deviceIntentURI.
:::

:::WorkflowBlockItem
Custom Attributes are used to hold the location (URI / ContentURI) value on the server for every device and can help administrators determine a file’s availability on device. For more information, see [**Assigning Custom Attributes to Devices**](./Assigning_Custom_Attributes_to_Devices.md).

In the **Provide access to specific app or package name** field, enter the **App Name** or the **Package Name**, for example, Velocity.These will be the only authorized packages allowed to access the file.
:::

:::WorkflowBlockItem
In the Intents-Standard section, provide the following details:
:::

:::WorkflowBlockItem
- **Operation Type** - From the drop-down list, select **Start Activity** / **Start Service** or other similar choice as per the app. Choose the right value for this field depending on the target app developer's guidance or refer to the target app documentation.
- **Class Name** (Optional) - Choose the right value for this field depending on the target app developer's guidance or refer to the target app documentation.
- **Action** - Set the action to\:com.wavelink.nameofapp.action.INSTALL\_CONFIGor similar, as per the app.
- **Category** - Enter values separated by a semicolon (;).
- **Mime Type** (Optional) - In the administrator's host server, the custom.mobileconfig file should be set with a MIME type of application/configuration so that the MDM profile for the device is downloaded and installed on the device. Choose the right value for this field depending on the target app developer's guidance or refer to the target app documentation.
- **Flags** (Optional) - Select the number of flags to be used. Choose the right value for this field depending on the target app developer's guidance.
  Provide the **Intents-Extras** values under KEY, TYPE, and VALUE (optional). For more specific parameters, see the OEM app documentation. Choose the right value for this field depending on the target app developer's guidance or refer to the target app documentation.
:::

:::WorkflowBlockItem
Click **Save**.
:::

:::WorkflowBlockItem
In the Configurations page, select the new File Transfer Configuration and then select **Actions** > **Apply to Label**. The **Apply To Label** dialog box opens.
:::

:::WorkflowBlockItem
Select the suitable Label and then click **Apply**.

Transferring /Sharing of file with other apps can only be verified by collecting logs from the target app or from the device.
:::
::::

### Verifying file download status

Custom Attributes are used to hold the location (ContentURI) value on the server for every file on each device and can help administrators determine a file’s availability on the device.

**Procedure**

1. Go to **Devices** > **Devices**.
2. Select a specific device the File Transfer configuration was deployed to.
3. In the Device Details page, select the device and then select **Actions** > **Force Device Check-in**.
4. Under the Configurations tab, check that the File Transfer configuration displays with the status as **Applied**.
5. Under the Custom Attributes tab, check that the name of the new custom attribute displays (for example, "Custom-File-Name$") with its related value. This provides the information about the storage location of the file on the device and showcases that file has been locally downloaded to the device available within the Ivanti Go app sandbox.
   Transferring /Sharing of file with other apps can only be verified by collecting logs from the target app or from the device.
