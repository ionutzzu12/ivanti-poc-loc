---
title: Distribution Filters
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Configuring the distribution filters**](./Distribution_Filters.md)
- [**Configuring the distribution filters for delegated administrator**](./Distribution_Filters.md)

Use Distribution Filters to limit the apps available for installation. Distribution filters enable you to display only the apps in the app catalog that are applicable to the device.

**License**: Silver

These filters are available by default:

- **Android enterprise Enabled Apps** - limits app distribution to Android enterprise enabled devices only.
- **iPad Only Apps&#xA0;**- limits app distribution to iPad devices only.
- **iPhone Only Apps&#xA0;**- limits app distribution to iPhone devices only.

## Configuring the distribution filters

1. Go to **Apps > Distribution Filter**.The default app filters and any created app filters are listed here.
2. Click **+Add** to access the **Create Distribution Filter** dialog.
3. Enter a name and description in the appropriate fields.
4. Select rule definitions .These rules can be constructed using the applicable operators, including the "contains", "is less than", "is greater than", "is in range", "is equal to", and "is not equal to" operators. The rules can be nested together using the ANY (OR) or ALL (AND) options. App distribution filters are as follows:\* Access Blocked
   - APNS Capable
   - Android managed Device with Work Profile
   - Android Work Enabled
   - Android Work Managed Devices (Device Owner) Enabled
   - Android Work Profile on Company Owned Device Enabled
   - Client Last Check-in
   - Client Registered
   - Compliance
   - Compliance Action Blocked
   - Current Country Name
   - Current MCC
   - Current MNC
   - Custom Device Attribute
   - Custom LDAP Attribute
   - Custom User Attribute
   - Custom IDP Attribute
   - Device Type
   - Home Country Name
   - Home MCC
   - Home MNC
   - IMEI
   - IMEI2 (only on Android devices with a dual SIM port and applicable for Android 8.0 or higher devices)
   - Kiosk Mode
   - Manufacturer
   - OS Version
   - Ownership
   - Phone#
   - Roaming
   - Secure Apps Status
   - Supervised
   - Sentry Blocked
   - User Enrollment Enrolled
   - Automated Device Enrollment Enrolled
5. Click **Create Distribution Filter**.
6. If needed, select a custom filter  to update.1) Click **Edit** to display the **Update Distribution Filter** page.
   2\) Enter a name and description in the appropriate fields.
   3\) Use the pull-down menus to define rules for the filter.
   4\) Click **Update Distribution Filter**.
7. Select an app.
8. On the App Detail page and select the **Distribution** tab.
9. Click **Edit**.
10. Choose an App Distribution option :\* **Everyone**
    - **No one**
    - **Custom**The Distribution Filter section is visible only if **Everyone** or the **Custom** distribution option is selected.
11. Choose a distribution filter option:1) Enter a filter name in the **Search the existing distribution filters**... field to locate a filter that has already been created.
    2\) Click **+Add Distribution filter** to add a new filter.

Distribution filters can be created or assigned to an app before it's added to the catalog. Changes made to the Distribution Filters will impact the distribution of apps which are using that filter (in all Spaces).

When the filter is set and if the **Allow app installation on M1 Devices upon distribution** is enabled the result populates macOS M1 devices. iOS VPP app will be available for all mac devices if **Allow app installation on M1 Devices upon distribution** is enabled and the Distribution Filter is either **Everyone** or **Custom**. Distribution filters of macOS related attributes are not supported for iOS apps.

## Configuring the distribution filters for delegated administrator

Delegated Administrator can manage and edit created filters that were added to individual apps during the distribution process in delegated Space. However, the Delegated Administrator cannot use distribution filters created in Default Space in any other Space, but can use them for delegated apps.

Delegated Administrator can create, manage, and edit distribution filters in specific Space they have access to. The distribution filter is available only in the Space it was created it. App distribution filters cannot be delegated.  

When a Delegated Administrator with App and System Management role adds an app using distribution filter in delegated Space can see the device details for devices in his Space and for the devices in other Spaces.

User with System management or System read only role will not be able to create, update, or delete distribution filters in any Space.

Delegated Administrator with App and Content manager role might not have access to the distribution filter. Due to which you cannot:

- Create apps using distribution filters. This happens when you are logged in as a Delegated Administrator and add an app.
- Delegated Administrator with only System Read-Only role or higher can add apps with distribution filter. A Delegated Administrator without System management role can add apps without distribution filter.

The Delegated Administrator can filter Delegation Status in App catalog by selecting the following options:

- Delegated
- Not-Delegated
