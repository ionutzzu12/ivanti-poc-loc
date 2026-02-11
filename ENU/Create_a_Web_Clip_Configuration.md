---
title: Create a Web Clip Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

A web clip is a shortcut to a website or web page from an iOS device. Use a web clip configuration to create standard web clips on devices. You can add a web clip icon to your iOS device that will launch a specific website. Web Clips help you to quickly find and use bookmarks on the home screens of your devices. You can also control some of the parameters of the Mobile Safari viewing experience for the site.

Delegation with custom distribution option is available for this configuration. For more information, see *Distributing the configuration* topic in [**Working with Configurations**](./Working_with_Configurations.md).

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Click **Configurations**.
3. Click +**Add**.
4. Search and select the Web Clip configuration.
5. Configure the settings on this page. Refer to the table in the topic **Web Clip Configuration Settings** for guidance on the values.
6. Click **Next** to configure the distribution settings.
7. Select **Custom** and then select **Devices/ Device Groups**.
8. Click **Done**.

## Web Clip Configuration Settings

The following table lists the Web Clip Configuration settings:

| **Setting**                              | What To Do                                                                                                                                           |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                                 | Enter a name that identifies this configuration.                                                                                                     |
| **Description**                          | Enter a description that clarifies the purpose of this configuration.                                                                                |
| **Label**                                | Enter the text that you want to display below the shortcut on the device screen.\*                                                                   |
| **URL**                                  | Enter the URL that the web clip will access.\*                                                                                                       |
| **Removable**                            | Select the check box to allow the device user to delete the web clip.                                                                                |
| **Icon**                                 | Drag the icon file to the dotted box, or click **Choose File** to select it from your file system.                                                   |
| **Precomposed Icon**                     | Select to eliminate the special effects added by more recent versions of Safari.                                                                     |
| **Full Screen**                          | Select to display the web clip in full-screen mode instead of as content in a browser.                                                               |
| **Ignore Manifest Scope**                | Select to allow navigation to an external website without displaying the Safari browser. This option has no effect when Full Screen is not selected. |
| **Target Application Bundle Identifier** | The application bundle identifier that specifies the application that opens the URL. **Example**: com.google.chrome.ios                              |

Type $ to see a list of supported [**variables**](./Variables.md), if available, for this field.

**Related topics:**

- [**Multi-user Secure Sign-in for iOS**](./Multi-user_Secure_Sign-in_for_iOS.md)
