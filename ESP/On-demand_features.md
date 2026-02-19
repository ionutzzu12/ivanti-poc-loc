---
title: On-demand features
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM includes certain on-demand features that are disabled by default. Such features may have some impact on performance and may not yet be fully ready for deployment in production.

Administrators can contact [**Support**](./Opening_a_Support_Ticket.md) if they are interested in enabling one or more on-demand features on their tenant(s) devices that are disabled by default.

The following table includes the list of documented on-demand features:

| **Feature**         | **Description**                            | **Platform(s)** | **License**    |
| ------------------- | ------------------------------------------ | --------------- | -------------- |
| Windows 10 features | Features applicable to Windows 10 devices. | Windows 10      | - Legacy: Gold |

- Current: Secure EUMSee [**Packages**](./Packages.md) for more information about legacy and current offerings. |
  \| App catalog URL copy to clipboard                                              | Provides the ability for the administrators to copy the app catalog URL to clipboard for apps. This URL can be distributed to the users via email. If the user clicks the link from a registered device, the app catalog with the app will be opened in the browser, where the user can choose to install the app.The administrators are responsible for restricting the distribution of this URL to the intended users. | \* iOS
- macOS                          | NA (Tenant specific)                                                                                                      |
  \| Set up a web clip as an app                                                    | Set up a [**web clip**](./App_Catalog.md) as an app in the app catalog to make the web application available in the app catalog for the users. The web clip can be defined as a configuration, but a configuration can only be pushed by the admin. Users can choose to install the web application on their devices or opt out, whereas users have no option to opt out of a web clip configuration.                         | iOS                                    | NA (Tenant specific)                                                                                                      |
  \| Turn on registration of Allowlisted devices                                    | Allow device registration based on Allowlisted serial numbers in Users > [**User Settings**](./User_Settings.md) > Default Device Registration Setting.                                                                                                                                                                                                                                                                       | - iOS
