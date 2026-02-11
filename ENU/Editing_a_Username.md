---
title: Editing a Username
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

When you add a user, the text you enter for the email address is automatically listed for the username, as well. In most cases, you should leave the default username in place because:

- A username in the format of an email address is required.
- It is convenient to use the username [**variable**](./Variables.md) in configurations, though the email address can also be used.

The only time to edit a username is in the rare event of a conflict with an existing username, because usernames must be unique across the entire device management system. A conflict might happen, for example, if two departments in an organization sign up for the device management system.

## If a username conflict happens

If you cannot add a user because of a username conflict, enter a different username using the format of an email address. The email address does not have to correspond to an actual email account. For example, you can change the following email address:

[**ksmith@mycompany.com**](mailto\:ksmith@mycompany.com)

to

[**ksmith21@mycompany.com**](mailto\:ksmith21@mycompany.com)

If you edit the username, then any configurations that include the username as a variable will not work for this user. Create alternate configurations that use the email address variable, instead.
