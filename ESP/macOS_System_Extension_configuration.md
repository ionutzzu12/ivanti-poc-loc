---
title: macOS System Extension configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

System Extension configuration allows installation of extension types like Driver Extension, Network Extension and Endpoint Security Extension, without kernel-level access.

**Procedure**

**Applicable to**: macOS 10.15+

1. Go to **Configurations** > **+Add**.
2. Type **extension** in the search field, and then click the **System Extensions** configuration.
3. Enter a **Name** and **Description** of the configuration.
4. Under **Allowed System Extensions**, **+Add** the **Allowed Team Identifiers** and **Allowed System Extensions**.
5. Under **Allowed System Extensions Types**, **+Add** the **Allowed Team Identifiers** and **Allowed System Types**.
6. Check **Allow user overrides** option.
7. Click **Next**.
8. Select **Enable this configuration** option.
9. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom.
10. Click **Done**.In macOS 12, RemovableSystemExtensions allows application to deactivate their system extension without administrator approval during application uninstallation.
