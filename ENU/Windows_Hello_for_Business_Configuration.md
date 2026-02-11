---
title: Windows Hello for Business Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

This configuration allows the administrators to set-up Windows Hello in the devices. Setting up Windows Hello requires to set up a PIN to sign-in to the device.

Applicable to: Windows 10

Procedure**Procedure**

1. Go to Configurations > +Add.
2. Type windows in the search field, and then click the Windows Hello for Business configuration.
3. Enter a Name and Description of the configuration.
4. Toggle the Enable/Disable Windows Hello for Business for Windows 10 Devices to On.The toggle is set to On by default. Disabling Windows Hello for Business does not remove the PIN from the devices.
5. Set the PIN Complexity.
6. Select the required configurations:\* Requires a Trusted Platform Module (TPM) for Windows Hello for Business
   - Use Windows Hello for Business certificates as smart card certificates
   - Use of biometric gestures, such as face and fingerprint, as an alternative to the PIN gesture for Windows Hello for Business
   - Requires enhanced anti-spoofing for facial feature recognition on Windows Hello face authentication
   - Dynamic Lock
   - Enables users to sign-in with a FIDO2 security key.
7. Click Next.
8. Select Enable this configuration option.
9. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom.
10. Click Done.
