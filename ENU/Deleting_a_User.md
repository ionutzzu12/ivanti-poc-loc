---
title: Deleting a User
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**What happens when you delete a local user**](./Deleting_a_User.md)
- [**What about LDAP users?**](./Deleting_a_User.md)

**Procedure**

1. Go to **Users > Users**.
2. Select the entry for the user.
3. Click **Actions** (upper right).
4. Select **Delete**.

When an Ivanti Neurons for MDM Administrator or Partner Administrator attempts to delete a Partner Administrator, Ivanti Neurons for MDM displays a message conveying that a Partner Administrator must perform this operation on the Service Provider Portal.

If a user has some devices associated with their account, first you must retire and delete the devices and then delete the user. If user has no devices the user information can be deleted when the user is deleted.

## What happens when you delete a local user

- All information related to a deleted user is deleted from the system.
- Devices associated with the user are retired.
- Content uploaded by the user remains.
- No further device registrations are allowed for the user's account.

## What about LDAP users?

- If the LDAP server has been disabled, an LDAP user cannot be permanently deleted. The next sync of LDAP data will restore a deleted LDAP user.
- If the LDAP server or group has been deleted, the LDAP users become local users and can be deleted.
- When a user is deleted from LDAP, it will not be deleted from Cloud. The sync status will switch to "NO\_SYNC", but the user will not be removed.
