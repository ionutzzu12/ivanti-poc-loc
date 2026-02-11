---
title: Play Integrity (Previously SafetyNet Attestation)
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

Play Integrity (Previously SafetyNet) helps in assessing the security and compatibility of Android devices using Google’s Play Integrity APIs. When configured, it allows you to analyze devices after a regular time interval in determining whether the device has been tampered or not.

Play Integrity is now supported on all Android versions.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
In the **Configuration** tab, click **+Add**.
:::

:::WorkflowBlockItem
Select **Play Integrity** configuration. The **Play Integrity Configuration** page is displayed.
:::

:::WorkflowBlockItem
In the **Name** field, type an appropriate name for the Play Integrity Configuration.
:::

:::WorkflowBlockItem
Click the +**Add Description** link to add a description for the configuration. This field is optional.
:::

:::WorkflowBlockItem
In the **Configuration Setup** section, type the minimum time interval (in hours) that should be applied for assessing the security and compatibility check on devices. The value should be between 1 to 24.
:::

:::WorkflowBlockItem
Click **Next** and select one of the following distribution options:
:::

:::WorkflowBlockItem
- All Devices
- No Devices(default)
- Custom
  Click **Done**.
:::
::::

When the Play Integrity and SafetyNet nonces will be sent to the device, Play Integrity nonce will be prioritized over the SafetyNet nonce.
