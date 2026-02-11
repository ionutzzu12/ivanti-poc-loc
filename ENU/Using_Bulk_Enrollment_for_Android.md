---
title: Using Bulk Enrollment for Android
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

The bulk enrollment feature enables you to quickly register multiple Android devices with Ivanti Neurons for MDM.

License: Silver

Perform the following tasks before using bulk enrollment:

1. Install Android SDK, which includes the Android Debug Bridge (adb), on the computer used to register the devices.For more information about the Android Debug Bridge, see: [**http://developer.android.com/tools/help/adb.html**](http://developer.android.com/tools/help/adb.html).
2. Enable USB debugging.The procedure to enable USB debugging on Android devices varies depending on the Android release. See: [**http://developer.android.com/tools/device.html**](http://developer.android.com/tools/device.html) for information on enabling USB debugging.
3. Install the Go client on each device.
4. Connect the devices via USB cable to the provisioning computer to be used to register them.

The Go can be started and registered to a server using the Android Debug Bridge (adb) shell. The Android Debug Bridge is a tool that can be used from the command line in Windows, or in the Terminal utility in iOS. It enables you to communicate with a connected Android device. From the adb shell the command format is:

\> adb shell

$ am start -a android.intent.action.MAIN -d "mirp\://na1.mobileiron.com?key=value\&key=value" -n com.mobileiron.anyware.android/com.mobileiron.polaris.manager.ui.StartActivity

 The Registration Protocol (**mirp**) is used to encode relevant data for registration.

Valid keys and values are:

| Key        | Value                                                                                                                                                                                                                                                                                                                                              |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| user       | User's email address that would have been typed into the username field if using iReg.Required.                                                                                                                                                                                                                                                    |
| password   | User's password                                                                                                                                                                                                                                                                                                                                    |
| pin        | Registration pin for the user                                                                                                                                                                                                                                                                                                                      |
| quickStart | **When set to TRUE:** the splash screen will show, but not as long. On the Welcome screen, when the spinner changes to the Continue button, the screen will automatically move on without having to tap Continue. Also, this streamlined provisioning flow occurs across all devices:\* The privacy and shortcut prompts for the user are skipped. |

- On zebra devices, the client shall grant admin privileges to itself without a user prompt. Requires a minimum version of Zebra MX 4.3.**When set to FALSE:** the splash screen will show as usual and the user will need to tap Continue on the Welcome screen. Optional, defaults to FALSE. |

Use of  a password, pin, or token is required to use bulk enrollment.

This  example command specifies a server, user, password, pin, and quickstart:

am start -a android.intent.action.MAIN -d "mirp\://ppp183.auto.mobileiron.com?user=[**miadmin@auto0001.mobileiron.com**](mailto\:miadmin@auto0001.mobileiron.com)\&password=P@$$W0R3\&pin=12345\&quickStart=true" -n com.mobileiron.anyware.android.qa/com.mobileiron.polaris.manager.ui.StartActivity

**Sample bulk enrollment script**

You can use this script as an example to use when designing your own bulk enrollment script. This sample script registers all devices attached to the provisioning machine with the same user and password.

for i in \`adb devices | grep -v devices |

do

 echo "Registering $i"

 adb -s $i shell "am start -a android.intent.action.MAIN -d \\"mirp\://\<servername?user=user email addresspassword=password

done

**Potential Error messages**

Here are some potential errors that you may encounter using bulk enrollment.:

| Error                             | Resolution                                                                                   |
| --------------------------------- | -------------------------------------------------------------------------------------------- |
| mirp scheme not found             | Example command using a mirp scheme: am start -a android.intent.action.MAIN -d "xxxmirp\://? |
| URL is invalid                    | Occurs if no data string is sent at all. Verify that the URL is correct.                     |
| No server information found       | Server information missing or improperly entered.                                            |
| No user information found         | Verify that user key was entered.                                                            |
| No password/pin information found | Verify that a pin OR password key was entered.                                               |

When there are multiple profiles created for Bulk Enrollment:

- A natively enrolled fully managed Android Enterprise device receives the custom attribute that was created with the first profile.
- When migrating devices, if the device is present in a bulk enrollment profile, the custom attributes defined for the migrating device in the bulk enrollment profile will be applied to the device on migration. This behavior is the same for the migrated fully managed Android Enterprise devices because it receives the custom attribute of the 1st profile.

Also, all the profiles created for that particular device are seen as active.
