---
title: Privacy Preference (macOS)
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS 10.14 or supported newer versions.

Configure which applications are allowed to gain access to system services, system files, and system resources. This configuration controls the settings on a macOS device under System Preferences > Security & Privacy > Privacy.

## Creating a Privacy Preference configuration

Procedure

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **privacy** in the search field, and then click the **Privacy Preference** configuration.
4. Name and describe the configuration.
5. Navigate to one of the applications listed on the page. See [**Apple documentation**](https://developer.apple.com/documentation/devicemanagement/privacypreferencespolicycontrol/services) for related information.1) For macOS 10.14+, the applications and settings available for configuration include:\* Accessibility - Specifies the policies for the app via the Accessibility subsystem.
   - Address Book - Specifies the policies for contact information managed by the Contacts.app.
   - Apple Events - Specifies the policies for the app sending restricted AppleEvents to another process.
   - Calendar - Specifies the policies for calendar information managed by the Calendar.app.
   - Camera - A system camera. Access to the camera cannot be given in a profile; it can only be denied.
   - Microphone - A system microphone. Access to the microphone cannot be given in a profile; it can only be denied.
   - Photos - The pictures managed by the Photos app in \~/Pictures/.photoslibrary.
   - Post Event - Specifies the policies for the application to use CoreGraphics APIs to send CGEvents to the system event stream.
   - Reminders - Specifies the policies for reminders information managed by the Reminders app.
   - System Policy (All Files) - Allows the application access to all protected files, including system administration files.
   - System Policy (Admin Files) - Allows the application access to some files used in system administration.

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
For macOS 10.15+, the applications and settings available for configuration include:\* File usage - Allows a File Provider application to know when the user is using files managed by the File Provider.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Listen Event from all processes - Allows the application to use CoreGraphics and HID APIs to listen to (receive) CGEvents and HID events from all processes. Access to these events cannot be given in a profile; it can only be denied. Uncheck the Allowed option.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Access Media Library - Allows the application to access Apple Music, music and video activity, and the media library.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Screen Capture of the system display - Allows the application to capture (read) the contents of the system display. Access to the contents cannot be given in a profile; it can only be denied. Uncheck the Allowed option.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Recognize and send speech data to Apple - Allows the application to use the system Speech Recognition facility and to send speech data to Apple.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Access files in the user's Desktop folder - Allows the application to access files in the user's Desktop folder.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Access files in the user's Documents folder - Allows the application to access files in the user's Documents folder.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Access files in the user's Downloads folder - Allows the application to access files in the user's Downloads folder.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Access files on network volumes - Allows the application to access files on network volumes.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Access files on removable volumes - Allows the application to access files on removable volumes.
:::

6. For each application you want to configure, click **Actions > Add**.
7. Enter the values for the following identity dictionary keys:\* Identifier - Name of the settings. For example: "us.zoom.ZoomPresence."
   - Identifier Type - Select either Bundle ID or Path. For example: "Bundle ID."
   - Code Requirement - Specify the value for Bundle ID or Path. For example: "identifier "us.zoom.ZoomPresence" and anchor apple generic."
   - Static Code (True or False)
   - Allowed (True or False)
   - Comment
8. Click **Save**.
9. (Optional) Under any application, click **Actions > Delete** to remove any existing privacy preference settings.
10. Click **Next** to configure the distribution settings.
11. Click **Done**.
