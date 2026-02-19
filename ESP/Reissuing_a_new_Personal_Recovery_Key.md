---
title: Reissuing a new Personal Recovery Key
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS devices with Mobile\@Work for macOS 1.66 or supported newer versions.

When migrating from other MDM solutions to Ivanti Neurons for MDM, administrators can request the OS to reissue a new Personal Recovery Key (PRK) upon enrollment if a PRK was previously issued prior to enrollment. This enables the key to be stored in Ivanti Neurons for MDM.

You can view the Audit Trails log entries for the PRK activities as follows:

1. Go to **Dashboard > Audit Trails**.
2. In the Type filter, select **Personal Recovery Key**.PRK entries will be displayed in the Device Management category and activities such as "Personal Recovery Key viewed."

**Prerequisite**

Distribute the following configurations to the devices before performing this procedure:

- Mobile\@Work for macOS configuration.
- FileVault Recovery Key configuration.

**Procedure**

1. Contact [**Support**](./Opening_a_Support_Ticket.md) to request the script to generate new PRK on the device.
2. Create a device custom attribute with the name "deviceprk" which is used in the script.
3. Upload the script to the repository in **Admin > All Scripts**. While doing so, select the "deviceprk" custom attribute.
4. Create a dynamic device group for devices for which PRK was not retrieved from the old MDM solution. Select the device group rules as follows: "**Platform=macOS** and **Encryption Enabled is equal to Yes** and **macOS Personal Recovery Key escrowed is equal to No** and **macOS Recovery Key Type is equal to Personal**."
5. Create a Mobile\@Work for macOS Script configuration in which you can select the PRK script from the repository. Distribute the configuration to the new device group.
6. Schedule the script to run once a day or as desired. This script will ask for user password on every run. By default, the timeout period for the script execution is 60 seconds. It is recommended to extend the timeout period in the corresponding Mobile\@Work for macOS configuration by setting the **Max Run Time** field to 300 seconds.

- The decrypted key is available from the device details page of a device in the Device Encryption Status section. Click **View** next to the FileVault Encryption Enabled field.
- On obtaining the PRK, the device moves out of the device group. Hence, the script configuration will not be applicable anymore and will be deleted from the device.
- After the MDM retrieves the recovery key of a device using the script, the script will be uninstalled from the device.

Related topics:

- [**Attributes**](./Attributes.md)
- [**All Scripts**](./All_Scripts.md)
- [**Device Groups**](./Device_Groups.md)
- [**Mobile@Work for macOS**](./Mobile@Work_for_macOS.md)
