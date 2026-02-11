---
title: Administrador- Android Enterprise
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

Licencia: Silver

- Las aplicaciones de productividad Ivanti, Inc que tienen habilitado Android Enterprise, como Email+, Docs\@Work y Web\@Work requieren una licencia Gold.
- Tunnel para Android Enterprise requiere una licencia Platinum.

Android Enterprise habilita el uso y configuración de aplicaciones de Android Enterprise. Los usuarios de Android Enterprise pueden ver e instalar aplicaciones desde el catálogo de aplicaciones y a través de Google Play.

Si es un cliente nuevo, la distribución de la aplicación se establece por dispositivo de manera predeterminada. Esta configuración no se puede cambiar. Los clientes que hayan actualizado pueden elegir entre la distribución de aplicaciones por usuario o por dispositivo. Además, para los clientes que hayan actualizado, la distribución por usuario se selecciona de manera predeterminada. Muchos usuarios tienen varios dispositivos. Si un usuario tiene varios dispositivos, cuando la distribución de aplicaciones se establece por dispositivo, puede crear un conjunto diferente de aplicaciones disponibles en cada dispositivo.

Esta sección contiene los siguientes temas:

- [**Configurar Android Enterprise**](./Administrador-_Android_Enterprise.md)
- [**Configurar el modo Perfil de trabajo de Android Enterprise**](./Administrador-_Android_Enterprise.md)

## Configurar Android Enterprise

::::WorkflowBlock
:::WorkflowBlockItem
En el portal de Ivanti Neurons for MDM, haga clic en **Administrador > Google > Android Enterprise**.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones:
:::

:::WorkflowBlockItem
- **Cuenta de Google Play administrada:** para las empresas que no sean suscriptoras de G Suite, este método permite a los usuario inscribirse en Android Enterprise sin enviar información personal (direcciones de correo electrónico a Google). Ivanti Neurons for MDM aprovisionará y administrará a los usuarios automáticamente con Google. Se le pedirá que autorice Android Enterprise con una cuenta de administrador de Google.
- **Cuenta de Google administrada:** para las empresas que sean suscriptoras de G Suite, este método permite a sus usuario inscribirse en Android Enterprise con sus cuentas de Google. Cada usuario debe tener una cuenta de Google para inscribirse en Android Enterprise.
  Siga las instrucciones que aparecen en pantalla para completar el proceso de configuración:
:::

:::WorkflowBlockItem
Para el método automático, haga lo siguiente:

- Habilite su API de UEM y cree sus credenciales de empresa.
- Inscríbase en Google autorizando al propietario de la integración. Esta debe ser una cuenta del departamento informático en lugar de una cuenta personal.
- Defina su credencial arrastrando y soltando su ID de cliente JSON de la cuenta de servicio.
  Para el método alternativo, haga lo siguiente:
- Consulte el ID de CLIENTE de la sección siguiente y agréguelo a Google Admin.
- Busque su token de MDM en Google Admin y la cuenta de servicio de la consola de Google Cloud.
- En Ivanti Neurons for MDM, introduzca el token de MDM, el dominio de empresa de Google y la dirección de correo electrónico de administrador de empresa para conectarse al servicio de Google.
- En Ivanti Neurons for MDM, arrastre y suelte su ID de cliente de JSON de la cuenta de servicio.
- En Ivanti Neurons for MDM, autorice a Ivanti Neurons for MDM para ver o administrar los Usuarios de Google haciendo clic en **Autorizar**.
:::
::::

La interfaz de usuario de Ivanti Neurons for MDM le guiará por estos pasos.

### ID de CLIENTE para vincular Ivanti Neurons for MDM con la cuenta administrada de Google

Agregue la identificación del cliente como **140561810807-tiiglke17laibbrt5darupmvo4ae7cbj.apps.googleusercontent.com** en la consola de administración para vincular el abonado de Ivanti Neurons for MDM con la cuenta de Google administrada.

## Configurar el modo Perfil de trabajo de Android Enterprise

1. En el portal de Ivanti Neurons for MDM, vaya a **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Seleccione **Bloqueo y kiosco: configuración de Android Enterprise**.
4. Introduzca un nombre y descripción para la configuración.
