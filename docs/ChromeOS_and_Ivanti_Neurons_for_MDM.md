---
title: ChromeOS and Ivanti Neurons for MDM
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

ChromeOS is a Linux-based operating system created and distributed by Google. Ivanti Neurons for MDM supports devices working on Android, Windows, iOS, and macOS. This support has now been extended to ChromeOS devices as well. Ivanti Neurons for MDM provides a unified and simple mobility management solution for configuring and managing your ChromeOS devices. Ivanti provides a unified, simple, and feature-rich solution for ChromeOS devices similar to the admin workflows that are available for iOS, Android, Windows, and Mac on Ivanti Neurons for MDM. The administrator can simply connect Ivanti Neurons for MDM with their Google Cloud (also referred to as Google Admin console) using a simple integration from **Admin > Google > ChromeOS Management**.

### Prerequisites

1. Must have a managed Google Admin account.
2. The LDAP users and OUs must be imported on Google Admin Console. Ivanti Neurons for MDM supports only OUs imported from an LDAP source. Local OUs are not supported.
3. The administrator must have synchronized the organization units (user groups) into the Ivanti Neurons for MDM. This can be done by configuring the LDAP server and adding the organization units.

### Authorizing Google

The ChromeOS devices available on the Google Admin console cannot be registered directly on the Ivanti Neurons for MDM. Instead, these devices are registered with Google and information about these devices is synced between Google and Ivanti Neurons for MDM. The administrator must authorize Google to import the devices and perform other actions like assigning apps, configurations, etc.

**Procedure**

1. Go to **Admin -> Google > ChromeOS Management**.
2. Click **Authorize Google**.
3. Select the Google Admin account that you want to authorize.
4. Click **Continue** to accept the permissions to provide the required services.
   The **ChromeOS successfully setup** confirmation appears on the screen. You can also find the domain information below the confirmation.

### Syncing ChromeOS devices from Google

The administrator must sync the ChromeOS devices from the Google Admin console. When using the Google Admin console to access the ChromeOS devices for the first time, the administrator must manually sync the devices using the Sync Now option from the ChromeOS Management page.

After syncing the devices manually for the first time, the subsequent syncs will happen automatically on an hourly basis.

### Deleting the Google Admin Console integration with Ivanti Neurons for MDM

Delete integration revokes the OAuth token we received from Google to access Google resources. It deletes the ChromeOS devices, inventory associated with Blueprint config and app config, and the enrollment metadata. The Blueprint configuration and uploaded apps will not be deleted.

In case the tenant enrollment is not deleted, you can raise a ticket to check the issue.

**Procedure**

1. Go to **Admin -> Google > ChromeOS Management**.
2. Under the ChromeOS Ivanti Neurons for MDM Registration section, Click **Delete**.
   A pop up appears on the screen indicating whether you want to proceed with the Delete operation, and all the devices associated with this integration will be deleted. Select **Ok**.
