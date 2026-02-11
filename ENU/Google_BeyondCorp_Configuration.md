---
title: Google BeyondCorp Configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM can be integrated with Google BeyondCorp for conditional access. Ivanti Neurons for MDM sends device compliance status signal to Google BeyondCorp. This ensures that only compliant devices under N-MDM can access Google workspace applications.

Prerequisites

- For Ivanti Neurons for MDM, you must have an Ivanti Professional Plus / Premium license.
- For Google, you must have the BeyondCorp Enterprise, Google Workspace Enterprise or Cloud Identity Premium license.

Procedure (Google)

1. Login to the **Google Admin console** with admin credentials.
2. Go to **Devices** > **Mobile & Endpoints** > **Settings** > **Third-party integrations**.

::Image[]{src="Resources/Images/googlebc1.png" signedSrc="Resources/Images/googlebc1.png" size="27" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc1.png" githubPath="Resources/Images/googlebc1.png" position="flex-start" indent="2"}

3. Click **Security and MDM partners** > **Manage**.

::Image[]{src="Resources/Images/googlebc2.png" signedSrc="Resources/Images/googlebc2.png" size="26" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc2.png" githubPath="Resources/Images/googlebc2.png" position="flex-start" indent="2"}

4. In the **Manage Partner Connections** window, select **Ivanti**.

::Image[]{src="Resources/Images/googlebc3.png" signedSrc="Resources/Images/googlebc3.png" size="23" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc3.png" githubPath="Resources/Images/googlebc3.png" position="flex-start" indent="2"}

5. Click **Open Connection**.You will be redirected to the Ivanti Neurons for MDM login page; enter the tenant admin credentials. Once you log in to the tenant, you will see that **Google BeyondCorp** is enabled and linked to your Google account automatically.
6. In the Google Admin Console, go to **Security** > **Context-Aware Access** > **Access levels**.

::Image[]{src="Resources/Images/googlebc5.png" signedSrc="Resources/Images/googlebc5.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc5.png" githubPath="Resources/Images/googlebc5.png" position="flex-start" indent="2"}

7. Click **Create Access Level**.In the Create Access Level window, under the Context conditions section, click **ADVANCED** and provide the required information.

::Image[]{src="Resources/Images/googlebc7.png" signedSrc="Resources/Images/googlebc7.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc7.png" githubPath="Resources/Images/googlebc7.png" position="flex-start" indent="2"}

8. Go to **Security** > **Context Aware Access** > **Access level**, select the application for which you would like to assign the policy.

::Image[]{src="Resources/Images/googlebc9.png" signedSrc="Resources/Images/googlebc9.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc9.png" githubPath="Resources/Images/googlebc9.png" position="flex-start" indent="2"}

9. Click **Assign**.
10. From the **Select access levels** window, select the policies you want to assign and click **Save**.

::Image[]{src="Resources/Images/googlebc11.png" signedSrc="Resources/Images/googlebc11.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc11.png" githubPath="Resources/Images/googlebc11.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
Once the above setup is complete, you can create the partner device compliance configuration using **Google BeyondCorp**.
:::

**Procedure (**&#x49;vanti Neurons for MD&#x4D;**)**:

1. Go to **Configurations** > **Add Configuration**.
2. Select **Partner Device Compliance** configuration.
3. The Create Partner Device Compliance configuration page appears on the screen.
   Enter a name for the configuration.
4. Under the Choose Partner list, select **Google BeyondCorp**.
5. The Configuration Setup section appears on the screen. Make sure the Report Compliance Status for iOS and Android devices option is set to ON.
   Click **Next**.
6. Select **Enable this configuration**.
7. Select **Custom** as distribution option
8. Select **Users/User Groups** under the **Custom Distribution** Option.
9. Under the **Select below to distribute this configuration** section, select users/user groups from the list.
10. Click **Done**.
