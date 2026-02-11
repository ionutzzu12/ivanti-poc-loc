---
title: Cellular Private Network Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM enables the Cellular Private Network configuration payload to provide device information on private network deployments, including geographical location, preference over Wi-Fi, and network deployment type.

**Applicable to**

iOS 17.0 through the most recently released version as supported by Ivanti Neurons for MDM.

**Procedure**

1. Go to **Configurations** > **+Add**.
2. Search and select the **Cellular Private Network** configuration.
3. Configure the **Cellular Private Network** settings as per the following table:| **Setting**                 | **Description**                                                                                                                                                                                |
   \| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Name**                    | Enter a name that identifies this configuration.                                                                                                                                               |
   \| **Description**             | Enter a description that clarifies the purpose of this configuration.                                                                                                                          |
   \| **Cellular Data Preferred** | Select the check box to enable and use cellular data over Wi-Fi.                                                                                                                               |
   \| **NR Standalone**           | Select the check box if the cellular data network has NR 5G Standalone.                                                                                                                        |
   \| **Data Set Name**           | Specify the Data Set Name that identifies with this configuration.                                                                                                                             |
   \| **Version Number**          | Specify the Version Number for the data set to track the system updates.                                                                                                                       |
   \| **GeoFences**               | Specify the Latitude, Longitude, and Radius for each Geo ID to deploy a private network in a geographical location.You can create a list of up to one thousand geofences for private networks. |
4. Click **Next** to configure the distribution settings.
5. Select one of the distribution options to set up the **Cellular Private Network** configuration. For more information about configuring distribution options, see [**Working with Configurations**](./Working_with_Configurations.md).
6. Click **Done**.
