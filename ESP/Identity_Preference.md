---
title: Identity Preference
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS 10.12 or supported newer versions.

Identify an Identity Preference item in the user's keychain that references an identity payload included in the same profile.

On a macOS device, an Identity Preference allows you to choose the identity (key-value pair) you want to use with a website. Once you have pushed an Identity Preference (which consists of the URL and identity) to the device, it is listed in **Keychain access > All Items** (the "Kind" will be "Identity Preference"). The next time you try to connect to that URL from Safari, the device will present the configured certificate.

Ivanti Neurons for MDM creates a default system Identity Preference configuration with a payload for the AppStore URL and the certificate to use.

While accessing the macOS App Catalog using Safari on macOS 10.12 and later versions, the user will get a system password prompt to cache the identity certificate. Users need to select ‘Always allow’ for the first time to avoid subsequent prompts while accessing the macOS App Catalog.

Safari with macOS version less than 10.12 and other browsers will show certificate and system password prompts while accessing the macOS App Catalog on a new browser session from macOS devices.

## Creating an Identity Preference configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **preference** in the search field, and then click the **Identity Preference** configuration.
4. Name and describe the configuration.
5. In the Configuration Setup section, in the **Name** field, enter an email ID, a DNS host name, or a name that uniquely identifies the service.
6. In the **Certificate UUID** field, select a certificate.
7. Click **Next** to configure the distribution settings.
8. Click **Done**.

**Related topics:**

- [**Certificate Preference**](./Certificate_Preference.md)
