---
title: Certificate Revocation Checking Configuration
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

This configuration allows the administrators to check an array of certificates revoked from a device. Administrators can specify a certificate authority (CA) which allows the configuration to enable revocation checking for all the certificates which are linked to that CA.

Applicable to: iOS 14.2+ and visionOS 1.1+

**Procedure**

1. Go to Configurations > +Add.
2. Type certificate in the search field, and then click the Certificate Revocation Checking configuration.
3. Enter a Name and Description of the configuration.
4. Select algorithm as SHA 256 and enter the Hash of the root certificate.In Hash, you have to enter a Base64 encoded (binary) SHA-256 hash of the certificate’s public key. See [**Apple documentation**](https://support.apple.com/en-us/HT209143) for the available trusted root certificates for Apple operating systems. You can add multiple root certificates in this configuration.
5. Click Next.
6. Select Enable this configuration option.
7. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom.
8. Click Done.
