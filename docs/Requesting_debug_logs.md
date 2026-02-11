---
title: Requesting debug logs
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

You can send a request to iOS, macOS, and Android work managed devices to retrieve debug logs for troubleshooting device issues. Using the "Request debug logs" command in the Devices page, the actions and success or failure of an event is captured in the audit logs.

This feature requires the following clients:

- iOS devices require Go 5.3.0 for iOS or supported newer versions. For devices that are migrated from Ivanti EPMM to Ivanti Neurons for MDM, this feature requires Mobile\@Work 12.2.0 for iOS or supported newer versions.
- macOS devices requires Mobile\@Work 1.5 for macOS or supported newer versions.
- Android work managed devices require Go 65 for Android or supported newer version.

**Procedure**

1. Go to **Devices > Devices**.
2. Select the device and click the device name link to go to the Device details page.
3. Click the

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
icon.
:::

4. Select **Request debug logs**  and click **OK**.

When the request is sent and when the logs are ready at the device, a notification is sent to the admin and is displayed in device logs. The device logs can also be downloaded by clicking the link.
