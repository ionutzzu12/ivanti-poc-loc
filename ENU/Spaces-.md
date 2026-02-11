---
title: Spaces
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

License: Silver

Spaces are used to separate a Unified endpoint management (UEM) system into independently managed entities for the purpose of delegated administration. Spaces can be created to reflect an organizational hierarchy. Ivanti Neurons for MDM supports single-level delegation with a central management entity referred to as a Default Space and a number of subordinate management entities referred to as Delegated Spaces. Every UEM system is created with a Default Space.

The Spaces page and the associated options are hidden for converged tenants who have access to both Ivanti Neurons for UEM and Ivanti Neurons for MDM.

A Space allows for delegated administration of the following system components. Users and User Groups currently cannot be delegated.

- Devices
- Configurations
- Policies
- Device Groups
- Applications
- An App Catalog
- An Apple Apps and Books Token

When an administrator logs in to the Ivanti Neurons for MDM Admin Portal on a tenant with at least a single Delegated Space, the administrator is presented with the Admin Portal login promo pop-up. The promo pop-up will not be displayed after delegated space creation and during user login if a delegated space is already created.

## Roles for global and delegated Space administrators

An admin user with the appropriate roles to access the Default Space is referred to as a Global Admin. Access to the Default Space can be read-only or read-write access. A Global Admin with the appropriate Administrative Roles can create Delegated Spaces and assign Delegated Admins to manage them. A Delegated Admin can be assigned to manage one or more Delegated Spaces.

The Spaces that a given administrator can access are listed in the Spaces selector drop-down in the upper left-hand corner of the Devices and Apps tabs. To view and manage a Space, use the Spaces drop-down to switch to the desired Space.

A Global Admin has visibility and control over all Delegated Spaces in addition to the Default Space. A Delegated Admin has visibility and control over only the Spaces which are assigned to them by a Global Admin. A Global Admin maintains central control over Delegated Spaces while a Delegated Admin has autonomy to manage the Spaces that have been delegated to them. This level of autonomy is determined by whether delegation is inherited or copied from the Default Space.

The following are the different user roles and the tasks that they can perform:

### Inherited app in a delegated Space

- Existing Ratings or Reviews at time of delegation are inherited and visible to users in Del Space, including author username.
- Delegated Administrator cannot delete Ratings/Reviews for an inherited app.
- Delegated Administrator can export Ratings/Reviews for an inherited app.
- Users in Delegated Spaces can add Ratings/Reviews to inherited app.
- Users in Delegated Spaces can view Ratings/Reviews added by Users in Del Spaces, including author username.

### App in a delegated Space (added, not inherited)

- Only Global Admin can enable or disable Reviews from **Apps > Catalog Settings > Ratings & Reviews**.
- Users in Delegated Space can add Ratings/Reviews.
- Delegated Administrator can Delete reviews added by users in the same Delegated Space.
- Users in other Delegated Spaces, including Default, cannot view Ratings or Reviews added by Users in each Delegated Spaces.
- Delegated Administrator can export reviews added by all users, including usernames.

### Delegated app in a default Space

- Global Admin can delete Ratings or Reviews added by a user in a Delegated Space.
- Global Admin can export all Ratings or Reviews including those added by users in Delegated Spaces.
- Users in Default Space can view Ratings or Reviews added by users in Delegated Spaces, including username.

## Priority of a delegated Space

The Default Space in an UEM System always has the lowest priority. The priority of a Delegated Space relative to other Delegated Spaces is set by the Global Admin and can be changed at any time. Delegated Spaces are listed rank ordered, from highest priority to lowest on the Spaces page under the Admin tab in the Admin Portal.

## Delegation through inheritance or copy

A key concept in delegated administration is whether a system component is inherited or copied from the default Space.
