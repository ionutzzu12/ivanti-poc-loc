---
title: Administración de acceso de Apple
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

**Requisitos previos**:

- Verifique y bloquee el dominio en Apple Business Manager o Apple School Manager.
- Configure al menos un servidor MDM desde las organizaciones de Apple Business Manager o Apple School Manager, donde las ID gestionadas de Apple se presentan en el Ivanti Neurons for MDM.

Iniciar sesión con un ID de Apple administrado permite a las empresas controlar los servicios y funciones de Apple que pueden utilizar los usuarios.

En Apple Business Manager o Apple School Manager, la configuración **Permitir cuentas de Apple administradas** controla dónde los usuarios pueden iniciar sesión con sus ID de Apple administrados. Los administradores pueden configurar esta opción para restringir el inicio de sesión a dispositivos gestionados o supervisados, o permitirlo en cualquiera de los dispositivos.

- **Cualquier dispositivo** (predeterminado): los usuarios pueden iniciar sesión con su ID administrada de Apple en cualquier dispositivo, independientemente de que la gestione una solución MDM.
- **Solo dispositivos administrados**: los usuarios solo pueden iniciar sesión en dispositivos gestionados por una solución MDM que admita el endpoint de Get Token.
- **Solo dispositivos supervisados**: los usuarios solo pueden iniciar sesión en dispositivos que estén supervisados (y gestionados) por una solución MDM que sea compatible con el endpoint Get Token.

Estas configuraciones forman parte de la gestión más amplia de "Administración de acceso" para los Servicios de Apple dentro de Apple Business Manager y Apple School Manager.

Con mayor seguridad, restringir el inicio de sesión a dispositivos gestionados o supervisados puede mejorar la seguridad de los datos al garantizar que la información relacionada con el trabajo solo sea accesible en dispositivos controlados.

El inicio de sesión en una Cuenta de Apple Administrada fallará si hay cero o múltiples organizaciones de servidores MDM de **Inscripción de Dispositivos** presentes en la pestaña de Inscripción de Dispositivos, y el administrador configura la opción **Permitir Cuenta de Apple Administrada** (disponible en **Gestión de Acceso** > **Servicios de Apple**) en "Solo Dispositivos Supervisados" o "Solo Dispositivos Administrados" en Apple Business Manager o Apple School Manager.

Los dispositivos no podrán iniciar sesión si la cuenta de **Apple Administrada** no está presente en el servidor MDM de Inscripción de Dispositivos Ivanti Neurons for MDM.
