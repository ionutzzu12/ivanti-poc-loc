---
title: Start menu and Taskbar
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

You can define the Start menu layout for your users to define applications that are safe to use and remove applications that are not required. The Windows 10 and 11 versions support different features, as the Start menu layouts are different.

To set Start menu and Taskbar configuration:

1. Go to **Configuration > +Add**.
2. Select **Windows Start Menu & Task Bar** configuration.
3. Enter a name for the configuration.
4. Select the Windows-specific version.
5. **Windows 10 devices**:
   In the **Configuration Setup** section, configure the following settings:|                          |                                                                                           |
   \| ------------------------ | ----------------------------------------------------------------------------------------- |
   \| Setting                  | What To Do                                                                                |
   \| **Name**                 | Enter a name that identifies this configuration.                                          |
   \| **Description**          | Enter a description that clarifies the purpose of this configuration.                     |
   \| **Select Golden Device** | Select the Windows 10 device that has the apps provisioned in its Start menu and Taskbar. |
6. Click **Fetch Start Menu Layout from Device** and configure the following options.

| Setting                           | What To Do                                                                  |
| --------------------------------- | --------------------------------------------------------------------------- |
| **Start menu and Taskbar Layout** | Select the any of the following options for hiding the list of apps.\* None |

:::Paragraph{listStyleType="disc" indent="2"}
Hide all apps list
:::

:::Paragraph{listStyleType="disc" indent="2"}
Hide all apps list, and disable "Show app list in Start menu" in Settings app
:::

:::Paragraph{listStyleType="disc" indent="2"}
Hide all apps list, remove all apps button, and disable "Show app list in Start menu" in Settings app |
\| **Start menu layout**                                                      |                                                                                                                                                                                                                                                                                         |
\| **Customize Start menu**                                                   | Click **Yes** to customize Start menu and layout parameters.                                                                                                                                                                                                                            |
\| **Taskbar**                                                                |                                                                                                                                                                                                                                                                                         |
\| **Customize Taskbar**                                                      | Click **Yes** to customize Taskbar                                                                                                                                                                                                                                                      |
\| **Remove existing pinned Taskbar shortcuts before adding the custom ones** | Click **Yes** to remove the existing pinned Taskbar shortcut before adding the custom Taskbar.                                                                                                                                                                                          |
\| **App Type**                                                               | Specifies the type of app.                                                                                                                                                                                                                                                              |
\| **App**                                                                    | Specifies the ID of the app.                                                                                                                                                                                                                                                            |
\| **Restore**                                                                | Click the **Restore** link to restore the Taskbar from the original Golden device taskbar.Click and drag the arrow icon in the row to move the position(up or down)the specific row\.Click the delete icon to delete the row\.Click the **Add New** button to add a new row.             |
:::

8. **Windows 11 devices**
   In the **Configuration Setup** section, configure the following settings:|                                   |                                                                                                                                                                                                                                                                                                 |
   \| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Setting                           | What To Do                                                                                                                                                                                                                                                                                      |
   \| **Name**                          | Enter a name that identifies this configuration.                                                                                                                                                                                                                                                |
   \| **Description**                   | Enter a description that clarifies the purpose of this configuration.                                                                                                                                                                                                                           |
   \| **Select Golden Device**          | Select the Windows 11 device that has the apps configured in the PINNED section of its Start menu.                                                                                                                                                                                              |
   \| **Start Menu and Taskbar Layout** |                                                                                                                                                                                                                                                                                                 |
   \| **Start menu and Taskbar Layout** | Select one of the following options to view the search option in the taskbar:\* **Hide**
   - **Search Icon**
   - **Search Icon and Label**
   - **Search Box (Default)**                                                                                                                                |
     \|                                   | Select the checkbox **Hide Task View** to hide the task view.                                                                                                                                                                                                                                   |
     \| **Most Used Apps**                | Select one of the following options to configure the most used apps in the Start menu:\* **Don’t enforce visibility of list of most used apps in Start.**
   - **Force showing of list of most used apps in Start.**
   - **Force hiding of list of most used apps in Start.**                         |
     \|                                   | The checkbox **Allow Pinning to Task bar** is selected by default.                                                                                                                                                                                                                              |
     \|                                   | Select the checkbox **Hide Recommended Section** to hide all the recommended sections.Due to a vendor issue, the **Hide Recommended Section** checkbox will not have a visible impact on the device even after the user logs off or logs in. Currently, you can't hide the Recommended section. |
     \| **Taskbar**                       |                                                                                                                                                                                                                                                                                                 |
     \| **App Type**                      | Select one of the following options to specify the type of app:\* **App User Model ID**
   - **Desktop Application Link Path**                                                                                                                                                                      |
     \| **App**                           | Specifies the ID or path of the app.                                                                                                                                                                                                                                                            |
     \| **Restore**                       | Click the **Restore** link to restore the Taskbar from the original Golden device taskbar.Click and drag the arrow icon in the row to move the position (up or down) the specific row\.Click the delete icon to delete the row\.Click the **Add New** button to add a new row.                  |
9. Click **Fetch Start Menu Layout from Device**.
10. After fetching settings from the Golden Device, all apps configured in the PINNED section of the start menu will be displayed for the administrator to review.
    Click **Next** and distribute the configuration to all the applicable device and user groups.
    Due to a vendor issue, when the configuration is undistributed, Pinned apps will remain as originally configured. However, when a new configuration is distributed, the previous layout will be overridden, and the new layout will be applied.
