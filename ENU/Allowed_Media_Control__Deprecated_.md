---
title: Allowed Media Control (Deprecated)
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**License:** Gold

Allowed Media Control configuration manages mounting, unmounting, and eject on logout for various physical media in macOS.

You can set the following options:

| Setting                                                                                                                                          | What To Do                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------- |
| Name                                                                                                                                             | Enter a name that identifies this configuration.                      |
| Description                                                                                                                                      | Enter a description that clarifies the purpose of this configuration. |
| **Configuration Setup**                                                                                                                          |                                                                       |
| **Mount control for media types**                                                                                                                |                                                                       |
| Turn on the mount control for each media type and set the mount settings. If you turn off the mount control, then OS default setting will apply. |                                                                       |
| **Media Type**                                                                                                                                   | **Mount Settings**                                                    |
| - CD                                                                                                                                             |                                                                       |

- DVD
- BD                                                                                                                                                                                                            | \* Read-only with authentication
- Deny Mount
- Eject Media            |
  \| - Blank CD
- Blank DVD
- Bland BD
- DVD-RAM
- Disk Image
- Internal Hard Disk
- External Hard Disk
- Network Disk                                                                                                          | \* Read-only
- Deny Mount
- Eject Media
- Authenticate                 |
  \| - External Hard Disk includes USB HDD, USB Flash Drive storage, and SD-Cards.
- Read-only media such as CD, DVD, and BD are mounted as read-only by default.                                                               |                                                                       |
  \| **Unmount control for media types**                                                                                                                                                                                        |                                                                       |
  \| Turn on the unmount control for each media type and set the unmount settings. If you turn off the Unmount control, then OS default setting will apply. Exercise caution when you set Deny Unmount setting for media types. |                                                                       |
  \| **Media Type**                                                                                                                                                                                                             | **Mount Settings**                                                    |
  \| \* CD
- DVD
- BD
- Blank CD
- Blank DVD
- Bland BD
- DVD-RAM
- Disk Image
- Internal Hard Disk
- External Hard Disk
- Network Disk                                                                                          | - Deny Unmount
- Authenticate                                         |
  \| **Eject on logout settings**                                                                                                                                                                                               |                                                                       |
  \| Media types to be ejected automatically when the user logs out.                                                                                                                                                            |                                                                       |
  \| **Media Type**                                                                                                                                                                                                             |                                                                       |
  \| \* CD
- DVD
- BD
- Blank CD
- Blank DVD
- Bland BD
- DVD-RAM
- Disk Image
- External Hard Disk
- Network Disk                                                                                                               |                                                                       |

## Distributing the configuration

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Set the options using the preceding table.
:::

:::WorkflowBlockItem
Click **Next**.
:::

:::WorkflowBlockItem
Select the **Enable this configuration** option.
:::

:::WorkflowBlockItem
Select one of the following distribution options:
:::

:::WorkflowBlockItem
- All Devices
- No Devices (default)
- Custom
  Click **Done**.
:::
::::
