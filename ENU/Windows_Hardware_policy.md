---
title: Windows Hardware policy
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Keeping a regular check on the hardware inventory will determine if a hardware item is added, copied, removed, replaced or moved on a Windows 10 device. Using Windows Hardware policy, you can select the type(s) of hardware to monitor, and the actions to be taken when changes in hardware on a device are detected.

1. Go to **Policies**.
2. Click **+Add**.
3. Select **Windows Hardware**.
4. Provide a name for the hardware policy.
5. Click **+ Add Description** to enter additional details if desired.
6. In the **Define Hardware Rules** section, configure the following options:

| Option              | Description                                                        |
| ------------------- | ------------------------------------------------------------------ |
| **Hardware Object** | Select the type of hardware from the following options:\* **BIOS** |

:::Paragraph{listStyleType="disc" indent="2"}
**Hardware Drive**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**CD-ROM Drive**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Processor**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Physical Memory**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
\| **Change Event**    | Select the type of hardware event(s) that should be checked:\* **Add**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Copy**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Remove**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Replace**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Move**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
\| **Choose Actions**  | Select the type of action to be taken:\* **Do Nothing**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Send Notification**: Select any of the following options:\* **Send Email Notification** - Type the subject and body in the **Email message** section to send notification.
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Send Push Notification** - Type the push notification message.
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Send Both** - Type the email message and push notification message.
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Wait**: From the drop-down list, select the number of days/hours to wait.\* **1** to **31** for **Days**.
:::

:::Paragraph{listStyleType="disc" indent="3"}
**1** to **24** for **Hours**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Quarantine** - Select any of the following quarantine options:**Optional Additional Quarantine Actions**\* **Quarantine Managed Applications** - Select **All Applications** or **Designated Applications** (search and select the app name in the Search field).
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Block New App Downloads** - Blocks download of apps to the device. Select **All Applications** or **Designated Applications** (search and select the app name in the Search field).
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Remove Configurations** - Removes configurations from the device. Select **All Configurations** or **Designated Configurations** (search and select the configuration in the Search field).
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Remove Content** - Removes all content associated with apps distributed from the device.**Default Quarantine Actions**\* **Block App Store Access**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Block Content Store Access**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Block AppConnect**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Block AppTunnel**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Block ActiveSync**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Block**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Retire**This action cannot be undone.To add or delete a compliance action click the 'plus' or 'minus' icon. |
Click **Next**.
:::

8. Select one of the following distribution options:\* **All Devices**
   - **No Devices(default)**
   - **Custom**
9. Click **Done**.
