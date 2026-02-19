---
title: Certificate Preference
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS 10.12 or supported newer versions.

Identify a Certificate preference item in the user's keychain that references a Certificate payload included in the same profile.

This configuration is used to bind a certificate to either an email address or a URL. After you bind a certificate to an email address, the Mail app will use it for that email account. If an SSL Certificate for a website is not trusted, adding a Certificate preference will ensure that the browser does not prompt you with a warning message when you try to access the website.

## Creating an Certificate Preference configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **preference** in the search field, and then click the **Certificate Preference** configuration.
4. Name and describe the configuration.
5. In the Configuration Setup section, in the **Name** field, enter an email ID or a name for which a preferred certificate is requested.
6. In the **Certificate UUID** field, select a certificate.
7. Click **Next** to configure the distribution settings.
8. Click **Done**.

**Related topics:**

- [**Identity Preference**](./Identity_Preference.md)
