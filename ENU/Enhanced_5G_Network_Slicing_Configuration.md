---
title: Enhanced 5G Network Slicing Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

Ivanti neurons for MDM provides enhanced 5G network slicing configuration to set up 5G network slices for android which allows mobile network operators to allocate dedicated 5G network segments, or "slices," for grouping different applications with similar needs like low latency or high bandwidth in a specific slice for better optimization of network resources. This enables MDM administrators and network providers to manage slices directly for better app performance.

## Key Features

1\. **Dedicated Network**: Instead of all applications sharing the single network slice, network slicing enables different apps to use their own network slice tailored to their specific requirements

2\. **Customization**: The admin can configure how apps are assigned to specific network slices according to their individual requirements—for instance, ensuring low latency for real-time communication apps or high bandwidth for streaming services like YouTube. A slice intended for high-performance gaming may prioritize low latency, whereas one for media streaming would be optimized for high bandwidth.

3\. **Partner Involvement**: This feature often requires collaboration with network providers who define these slices and inform MDM admins about list of slices and its significance.

## Creating an Enhanced 5G Network Slicing Configuration

### Procedure

1\. **Add Configuration**

- Navigate to **Configurations >> +Add**. The **Add Configuration** page is displayed.
- Enter **Enhanced Network Slicing** in the search bar to configure Enhanced Network Slicing. The **Create Enhanced Network Slicing Configuration** page is displayed.
- Click **+Add Description** to enter a description of the configuration.

2\. **Configure Application**

- Under **Configuration Setup >> App Catalog**, enter the desired application name.
- Click **Add Manually** if the application is not available in the Play Store or App Store.
- Enter **Package ID** and select appropriate **Network Slice** from the drop down menu.
- Select the desired slice from **Select Slice** drop-down.
- Click **Add**. The application will now appear in the **Configure Network Slices** under the selected network slice.
- To remove an application, click **Remove** under the **Configure Network Slice** section.

3\. **Distribute Configuration**

- Click **Next**, select or deselect the "**Enable this configuration**" check box, choose a distribution option (All Devices, No Devices, or Custom),
- Click **Done** to complete the configuration.

## Enhanced Network Slicing Configuration for Lockdown & Kiosk

Creating a Enhanced 5G Network Slicing Configuration allows you to configure devices to operate in a restricted manner, ensuring that users only have access to specified applications and settings.

Under the following lockdowns, there is an "**Enable 5G network slicing**" checkbox:

- **Work Profile**- On employee-owned devices with a Work Profile configured using Android Enterprise version 12.0, the "Enable 5G Network Slicing" checkbox can be found under**Configuration Setup > Work Profile Lockdown Settings**.
- **Managed Device with work profile / Work Profile on Company owned devices** - Under Managed Device with work profile/ Work Profile on Company owned devices with Android 12.0 versions we have "Enable 5G network slicking" checkbox.

This is a legacy setting that permits the devices to use of 5G network slicing. Its correlation to the new Enhanced 5G Network Slicing configuration is as follows:

If any of the above lockdowns are applied to a device and the *Enable 5G network slicing* option is **not** selected, the *Enhanced 5G Network Slicing* configuration will fail with an error.

### Examples

- **Case 1**: If device lockdown is not distributed and enhanced network slicing configuration is distributed, the enhanced configuration will activate.
- **Case 2**: If device lockdown is distributed but the 5G check box is not selected (false), the enhanced 5G network configuration will error out.
- **Case 3**: If enhanced network slicing is distributed first, followed by the device lockdown with the check box enabled, enhanced network slicing configuration will keep working. Otherwise, it will error out.

## Configuration Details:

- If the device lockdown is distributed and the enhanced network slicing configuration is pushed /distributed, users must ensure that the Enable 5G network slicing check box is enabled to prevent errors.
- If the check box is not enabled and the configuration is sent, it will error out on the device.
