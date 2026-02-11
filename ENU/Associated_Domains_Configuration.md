---
title: Associated Domains Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

**License**: Gold

The Associated Domains configuration is a dictionary that maps apps to their associated domains. Associated domains can be used with features such as Extensible AppSSO, universal links, and Password AutoFill.

The Associated Domains settings are as follows:

| **Setting**            | What To Do                                                                                                                                                                                                                                                |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                   | Enter a name that identifies this configuration.                                                                                                                                                                                                          |
| Application Identifier | (Required) The app identifier to associate the domains with.                                                                                                                                                                                              |
| Associated Domains     | (Required) The domains to be associated with the app. Each string is in the form of "service\:domain". Domains should be fully qualified hostnames, like [**www.example.com**](http://www.example.com).                                                   |
| Enable Direct Download | If true, data for this domain should be downloaded directly instead of through a CDN. The entitlement value for this domain must be set to service\:domain?mode=managed or this value will be ignored. Available in macOS 11 and later.**Default**: false |
