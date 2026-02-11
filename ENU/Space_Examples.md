---
title: Space Examples
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

This topic provides examples related to how spaces can be used by administrators.

## Administrator per location

ACME, Inc. has offices in North America and Europe. Due to language and time zone issues, ACME wants an administrator in the US to manage North American devices and an administrator in Germany to manage European devices.

To set up these Spaces, ACME made these changes:

1. Created a user group in Ivanti Neurons for MDM for users in Europe.
2. Created a user group in Ivanti Neurons for MDM for users in North America.
3. Created a Europe Space with the following rule:
4. User Group = Europe
   Created a North America Space with the following rule:
5. User Group = North America
   Assigned the Device Management role for each Space to the proper administrator.

ACME now has the following Spaces:

- Europe
- North America
- Default

## Administrator per OS per location

ACME has decided that only Android experts should administer Android devices. One Android expert has been added to the North American organization, and one has been added to the European organization. So two new Spaces are needed.

To add the Spaces, ACME made these changes:

1. Created a Europe-Android Space with the following rules:
2. User Group = Europe
   OS = Android
   Created a North America-Android Space with the following rules:
3. User Group = North America
   OS = Android
   Assigned the Device Management role for each Space to the proper administrator.

ACME now has the following Spaces:

- Europe-Android
- North America-Android
- Europe
- North America
- Default

## Administrator for executives

ACME's executives have decided that they want special service from a special administrator. Only the most important executives are on this list.

To add this Space, ACME made these changes:

1. Created an Executives Space with the following rules:
2. Username = [**jdoe@acme.com**](mailto\:jdoe@acme.com)
   Username = [**gkunz@acme.com**](mailto\:gkunz@acme.com)
   Username = [**prizzo@acme.com**](mailto\:prizzo@acme.com)
   Username = [**fvanhoff@acme.com**](mailto\:fvanhoff@acme.com)
   Moved the Space to the top of the list in the **Space** page.
3. Otherwise, executives with Android devices would have the wrong administrator.
   Assigned the Device Management role for the Space to the special administrator.

ACME now has the following Spaces:

- Executives
- Europe-Android
- North America-Android
- Europe
- North America
- Default

## Administrator for all other devices

When ACME opens a new office in Japan, the added devices will be assigned to the administrator of the default Space until someone creates a Japan Space.
