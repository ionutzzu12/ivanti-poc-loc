---
title: SCEP Configuration for External Certificate Authorities
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

This feature enables support for Simple Certificate Enrollment Protocol (SCEP) configuration for external certificate authorities for Windows 10 devices.

Delegation with custom distribution option is available for this configuration. For more information, see *Distributing the configuration* topic in [**Working with Configurations**](./Working_with_Configurations.md).

### Setup an External Certificate Authority

You must first setup an External CA. You can skip to the next section if you already have an External CA.

1. Go to **Admin >Infrastructure > Certificate Management**.
2. Click **+Add**.
3. Enter a name for the Certificate Authority.
4. Use the pull-down menu to select Microsoft as the **Certificate Authority Type**.
5. Enter the **SCEP URL**.
6. Enter the **Username** and **Password**.
7. Enter the **Challenge URL**.
8. Click **Save**.

### SCEP Configuration

Now you can proceed with the SCEP configuration.

1. Go to **Configuration > +Add**
2. Select the Windows icon.
3. Select **Identity Certificate** to go to the **Create Identity Certificate Configuration** page.
4. Enter a name for the configuration.
5. Select **Windows Config** from the list of SCEP configurations from the **Certificate Distribution** pull-down menu.
6. Select the External CA.
7. Enter the Certificate Distribution details.\* Enter the subject. For example: CN=$\{userEmailAddress}
   - Select the number of Retries from the **Retry** pulldown menu.
   - Select the number of seconds to wait before each entry from the **Retry delay** pulldown menu.
   - Select a key size from the **Key Length** pulldown menu.
   - Select at least one certificate usage option.
   - Enter the length of time in the **Validity** field and pulldown menu.
   - Enter the CA Thumbprint.
   - Go to the SCEP challenge URL copy the CA Thumbprint and paste it here or click **Create from Certificate**... to upload the certificate from which the CA Thumbprint can be created.
     Select at least one hashing algorithm from the **Hash Algorithm Family** options.
8. Click **Next**.
