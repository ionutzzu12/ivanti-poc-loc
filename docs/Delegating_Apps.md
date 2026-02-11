---
title: Delegating Apps
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

App delegation allows a Global Admin to partition and independently manage apps in Ivanti Neurons for MDM. The Global Admin can centrally source and distribute public and in-house apps while maintaining the separation and control provided by delegated Spaces.

By centrally distributing an app, the Global Admin can predefine the management behavior of the app through app configurations as well as the apps' distribution rules. The app can then be delegated and made available in the App Catalog of the delegated Space.

The delegated app is then distributed to users within a given delegated Space. When applications are delegated, access to those applications can be assigned to a subset of Delegated Administrators, thus distributing admin responsibilities.

App delegation requires one or more Delegated Spaces to be defined first. When an application is delegated it is assigned to all Spaces. App delegation Space is classified into:

- Default Space
- Delegated Spaces

## Adding an app to a delegated Space

An application can be added to a Delegated Space by a Delegated or a Global Admin. The app appears only in the App Catalog of the Delegated Space where it was added. If you add a previously delegated app from Default Space to a Delegated Space, it will result in an error. In this case, inheritance for the app must be first disabled in the Default Space so that it can be added to a Delegated Space. For more information, see **Adding a configuration** in [**Working with Configurations**](./Working_with_Configurations.md).

## App distribution in a delegated Space

When an app is delegated from the Default Space, its Distribution rules are inherited. This app will be distributed to all the devices assigned to the Delegated Space which match the Distribution rules for the app.

The global administrators can delegate space administrators to edit the Dynamically Generated Identity Certificate for All Devices and for the Custom distribution option.

The distribution changes are applicable only to the specific space. All other spaces continue to inherit the default space distribution settings.

App approval settings for Android apps: App approval settings per space for Android apps is not supported. Apps approved in custom space take effect in all the spaces.

Existing Android catalog apps: On tenants where public Android apps have already been added in default space, apps need to be undelegated before that public app can be added in another non-default space.
