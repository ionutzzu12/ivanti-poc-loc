---
title: Printer Settings
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM allows you to create printer profiles and add them to devices. This feature requires Bridge. See [**Bridge**](./Ivanti_Bridge.md) for details.

When the printer profile is sent to the device, the printer must be active, otherwise the device cannot discover it.

**To set Printer Settings configuration for a Windows device:**

1. Go to **Configuration > +Add**.
2. Select **Printer Settings** configuration.
3. Enter a name for the configuration.
4. Select the **Windows** option.
5. In the **Configuration Setup** section, configure the following settings:| **Setting**                  | What To Do                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
   \| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Name**                     | Enter a name that identifies this configuration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
   \| **Description**              | Enter a description that clarifies the purpose of this configuration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   \| **Windows Printer Settings** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
   \| **Shared Print er**          | If the **Shared Printer** option is selected, the printer will be shared with other devices.Configure the following fields:**Name**: Enter the name of the printer configuration.**Description**: Enter a description of the printer.**Print Server**: Enter the IP address of the print server.**Shared printer name**: Enter the printer name.                                                                                                                                                                                                                                                   |
   \| **Network-attached printer** | When the **Network-attached** option is selected, the printer can be accessed only by devices within the attached network. Configure the following fields:**Name**:Enter the name of the printer configuration**Description**:Enter a description of the printer.**Print Name**: Enter the name of the printer in the network.**Printer host address**: Enter the host IP address of the printer.**Printer port number**: Select the port number of the network printer.**Printer driver name**: Enter the name of the printer driver.**Printer driver URL**: Enter the URL of the printer driver. |
6. Click **Next**.
7. Select one of the following distribution options:\* All Devices
   - No Devices(default)
   - Custom
8. Click **Done**.

**To set Printer Settings configuration for a macOS device**:

1. Go to **Configuration > +Add**.
2. Select **Printer Settings** configuration.
3. Enter a name for the configuration.
4. Select the **macOS** option.
5. In the **Create Printer Configuration** section, configure the following settings:| **Setting**             | What To Do                                                                                                                                                                                      |
   \| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Name                    | Enter a name that identifies this configuration.                                                                                                                                                |
   \| Description             | Enter a description that clarifies the purpose of this configuration.                                                                                                                           |
   \| **Configuration Setup** | Update the following fields to set-up printer for macOS devices:\* Allow Local Printers
   - Default Printer Display Name
   - Footer Font Name
   - Footer Font size
   - User Printer List
     - Add Printer |
6. Click **Next**
7. Select one of the following distribution options:\* All Devices
   - No Devices(default)
   - Custom
8. Click **Done**.
