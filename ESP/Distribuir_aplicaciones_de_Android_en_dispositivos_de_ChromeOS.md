---
title: Distribuir aplicaciones de Android en dispositivos de ChromeOS
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

El administrador puede distribuir aplicaciones de Android desde el Catálogo de aplicaciones a los dispositivos de ChromeOS.

**Requisitos previos**

1. Se debe configurar Android Enterprise. Para obtener información sobre cómo configurar Android Enterprise, consulte [**Configurar Android Enterprise**](./Configurar_Android_Enterprise.md).
2. Las aplicaciones de Android se deben presentar en el Catálogo de aplicaciones.
3. Asegúrese de que el usuario del dispositivo de ChromeOS (Chromebook) forma parte de un Grupo de usuarios (también denominado Unidad organizativa) antes de distribuir aplicaciones de Android y configuración de ChromeOS Blueprint.

Una vez identificada la aplicación de Android, debe distribuir la aplicación siguiente el mismo proceso que siguió para distribuir cualquier otra aplicación. Cuando distribuya la aplicación de Android, asegúrese de seleccionar los Grupos de usuarios a los que desee distribuir la aplicación y realice una instalación silenciosa en el dispositivo.

Si su despliegue de aplicaciones de Android existente está establecido para que se distribuya a dispositivos/grupos de dispositivos o usuario, deberá cambiar la distribución para que se base den Grupos de usuarios. Esto puede afectar a los despliegues existentes si la aplicación ya se está usando. Se recomienda hacer esto primero en una aplicación completamente nueva.

Ajustes de instalación permite a los administradores controlar la instalación en segundo plano final y es necesario para forzar la aplicación en dispositivos de ChromeOS. Los Grupos de usuarios se deben seleccionar aquí.
