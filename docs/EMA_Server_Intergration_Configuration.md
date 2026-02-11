---
title: EMA Server Intergration Configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

The EMA Server Integration configuration allows Windows 10 devices to link to the configured Intel EMA server. To link devices to the configured Intel EMA server, you should provide the installation directory of the original EMA agent and upload the EMA agent .msh file from the new EMA server.

This feature requires Bridge. See [**Bridge**](./Ivanti_Bridge.md) for details.

**Procedure**

1. Go to **Configuration > +Add**.
2. Select **EMA Server Integration** configuration.
3. Enter the name for the configuration.
4. In the Configuration Setup section, click **Choose File** to select the EMA agent .msh file.The msh file is an agent policy file that can be downloaded from the EMA server.
5. In the Original **EMA Agent Installation directory** field, type the location where the original EmaAgent.exe file is installed.
6. Click **Next**.
7. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom
8. Click **Done**.
