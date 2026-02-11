---
title: Multi-user Secure Sign-in for iOS
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

The Multi-user web clip allows users to log in and log out of iOS devices that are registered on Ivanti Neurons for MDM. When a user logs in for the first time, the profiles, apps, and configurations that are associated with that user are pushed to the device. When they have finished their work, they can open the web clip and select the "log out" function, which assigns the device to the Nobody User and removes the profiles, apps, and configurations associated to the user that had originally logged in, as long as the configurations and apps are not being distributed to the Nobody User. After a log out, the web clip resets so that the next user can log in and receive their custom configurations, apps, and policies. Device supervision is not required to use the multi-user secure sign-in feature. See the Support knowledge base article, [**Ivanti Neurons for MDM: Multi-user secure sign-in for iOS**](https://forums.ivanti.com/s/article/MobileIron-Cloud-Multi-user-secure-sign-in-for-iOS-5948), for a deeper look at the multi-user sign-in feature.

**Applicable to:** iOS devices (Not applicable to User Enrolled devices)

This section contains the following topics:

- [**Supported credentials**](./Multi-user_Secure_Sign-in_for_iOS.md)
- [**Understanding the Nobody User**](./Multi-user_Secure_Sign-in_for_iOS.md)
- [**Signing in to a device**](./Multi-user_Secure_Sign-in_for_iOS.md)
- [**Signing out of a device**](./Multi-user_Secure_Sign-in_for_iOS.md)

## Supported credentials

User name and password must be used to log into the Multi-user secure web clip. PIN based registration is not supported with the Multi-user secure web clip.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configurations**.
:::

:::WorkflowBlockItem
Click **Multi-user Secure Sign-in for iOS**. You may need to use the search functionality to find it if there are multiple pages of configurations. This configuration is not accessed by selecting **+Add**.
:::

:::WorkflowBlockItem
Click **Edit Distribution**, or the associated icon to distribute the web clip to the appropriate Device Group.

::Image[]{src="Resources/Images/74EditDistribution.png" signedSrc="Resources/Images/74EditDistribution.png" size="25" caption alt isUploading="false" sha initialPath="Resources/Images/74EditDistribution.png" githubPath="Resources/Images/74EditDistribution.png" position="flex-start"}

If you want to distribute it to a User Group, you can create a dynamic Device Group that is tied to a User Group.
:::

:::WorkflowBlockItem
Select one of the following distribution options, remembering that you must always distribute the web clip to the Nobody User, or the Device Group with which Nobody User is associated. This does not happen by default, so make sure that you are distributing it to the Nobody User.
:::

:::WorkflowBlockItem
- All Devices
- No Devices (default)
- Custom
  Click **Save**.
:::
::::

## Understanding the *Nobody* User

When a device has been logged out through the web clip, it remains enrolled with Ivanti Neurons for MDM to a special user called the Nobody User. If you want to remove apps and configurations from the device when a User logs out, you must make certain that those apps and configurations are not distributed to the Nobody User. If you want certain configurations, such as Wi-Fi, to remain on the device when a user signs out of the Secure Sign-In web clip, then you must ensure that those configurations are also distributed to the Nobody User.

::Image[]{src="Resources/Images/74Nobody.png" signedSrc="Resources/Images/74Nobody.png" size="35" caption alt isUploading="false" sha initialPath="Resources/Images/74Nobody.png" githubPath="Resources/Images/74Nobody.png" position="flex-start"}

This means that you must pay attention to User Groups and Device Groups to which you distribute apps and configurations. If you are distributing an app to Everyone, and you want it to be removed when a user signs out of the device, then the best practice is to create a User Group that does not include the Nobody User. Custom attributes make it much easier to create a group of users that are "multiusers," and another User group that consists only of the Nobody User. You can create a User Attribute from Admin> System > Attributes called "Multiuser owner" and then assign the value of "Yes" or "True" to the Nobody User. You can then create User Groups and Device Groups based on the value of the attribute.

## Signing in to a device

A user can sign in to an iOS device and assign the device to self. After logging in, all relevant applications, policies, configurations, and certificates are pushed to the device.

For security reasons, iDP user must re-authenticate every time they log in, even if they are already signed on to the device.

## Signing out of a device

A user can sign out of his/her iOS device after usage. After signing out, the applications, policies, configurations, and certificates are removed from the device, leaving the device in the state that it was in prior to the user sign-in. Then, the device is available for sign-in by another user.

Logout from all the Microsoft Apps before logging out from Multi-user Web Clip.
