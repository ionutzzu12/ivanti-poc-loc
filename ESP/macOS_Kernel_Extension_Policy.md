---
title: macOS Kernel Extension Policy
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS 10.13.2 or or supported newer versions.

Controls restrictions and settings for loading user-approved Kernel Extensions.

## Creating a macOS Kernel Extension Policy configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **kernel** in the search field, and then click the **macOS Kernel Extension Policy** configuration.
4. Name and describe the configuration.
5. Select the **Allow User Overrides** option to allow users to approve additional kernel extensions not explicitly allowed by the following configuration.
6. In the Allowed Team Identifiers and Kernel Extensions section, click **+ Add** to add allowed team identifiers and kernel extensions. A kernel extension is the bundle identifier of a package. For each team identifier, you can add several validly signed kernel extension names in the pop-up window.
7. Click  **Add**.
8. Click **Next** to configure the distribution settings.
9. Click **Done**.
