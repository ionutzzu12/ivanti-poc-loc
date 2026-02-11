---
title: Administrador > Microsoft Azure > Office 365 App Protection
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

**Licencia: Gold**

Puede configurar políticas de protección de aplicaciones de Office 365 para ayudarle a proteger los datos de su empresa. Estas políticas aplican los controles de Prevención de pérdida de datos (DLP, en inglés) para las aplicaciones de Microsoft Office 365 que utilizan API de Microsoft Graph. Algunas de estas API de Graph permiten a los administradores garantizar la protección de las aplicaciones nativas de iOS y Android que aprovechan el SDK de Graph.

Utilice esta función para reforzar políticas como las siguientes:

- Impedir que los usuarios puedan imprimir desde aplicaciones de Office 365.
- Evitar compartir datos con el exterior desde las aplicaciones de Office 365.
- Obligar el uso del PIN para las aplicaciones de Office 365.
- Desactivar la sincronización de contactos desde las aplicaciones de Office 365.

## Requisitos previos para usar la protección de aplicaciones de Office 365

Antes de hacer uso de la protección de aplicaciones de Office 365, debe tener:

- Una licencia válida de MobileIron
- La función de protección de aplicaciones de Office 365 está habilitada en Ivanti Neurons for MDM
- Una suscripción a Intune o a Microsoft EMS que incluya Intune.\* Cada uso al que se aplica la política requiere una licencia, pero para habilitar y probar la integración se requiere solo una licencia.
- Una suscripción válida a Office Enterprise o Business con acceso a aplicaciones de Office 365 en un dispositivo móvil.
- Una o varias aplicaciones de Office 365.
- Sincronice sus usuarios de Active Directory con su Entra ID.
- Un Drive for Business instalado en los dispositivos para proteger los datos en Word, Excel y PowerPoint. Esto no es obligatorio.
- Acceso al portal Microsoft Azure ([**https://portal.azure.com/**](https://portal.azure.com/)) para configurar las políticas de protección de las aplicaciones de Intune.
- Aplicación Intune Company Portal instalada en dispositivos Android.Los usuarios de dispositivos no están obligados a iniciar sesión, pero esta aplicación debe estar instalada en el dispositivo para proteger los datos del mismo. La protección se aplicará cuando el usuario inicie sesión en la aplicación.

## Registrar MobileIron como aplicación de Azure

Este apartado describe cómo registrar y almacenar sus credenciales de abonado de Azure con el software Ivanti Neurons for MDM y administrar de forma remota las políticas de protección de aplicaciones en la nube de Microsoft Azure para aplicaciones de Office 365 de Android y iOS. Aunque no es necesario, se pueden abrir dos navegadores para realizar los pasos de los siguientes procedimientos. Con el primer navegador deberá iniciar sesión en el portal de Microsoft Azure. Con el segundo navegador deberá iniciar sesión en el portal de administración Ivanti Neurons for MDM.

### Procedimiento del portal de Microsoft Azure

Microsoft puede cambiar la interfaz de usuario del portal Azure de vez en cuando. Estas instrucciones dan por hecho que usted está familiarizado con Microsoft Portal Azure y puede hacer los ajustes necesarios cuando registre MobileIron como una aplicación Azure.

::::WorkflowBlock
:::WorkflowBlockItem
Abra el primer navegador e inicie sesión en el portal de Microsoft Azure ([**https://portal.azure.com/**](https://portal.azure.com/)).
:::

:::WorkflowBlockItem
Haga clic en **Registros de aplicaciones** en el panel izquierdo.
:::

:::WorkflowBlockItem
Haga clic en **+Registro de nueva aplicación**.
:::

:::WorkflowBlockItem
Introduzca la siguiente información para registrar MobileIron como aplicación de Azure.
:::

:::WorkflowBlockItem
- **Nombre:** escriba un nombre para la aplicación de MobileIron. (Este campo debe tener al menos 4 caracteres).
- **Tipo de aplicación:** seleccione Aplicación web/API.
- **URL de inicio de sesión:** introduzca la URL a la que acceden los usuarios de los dispositivos para iniciar sesión en MobileIron (obligatorio).
  Haga clic en **Crear** en la parte inferior del panel para añadir la aplicación y volver a la página de inicio de Azure.
:::

:::WorkflowBlockItem
Haga clic en la aplicación de MobileIron recientemente creada en la página de inicio de Azure.
:::

:::WorkflowBlockItem
Vuelva a la página de inicio de Azure para asignar permisos a la aplicación de MobileIron Azure.
:::

:::WorkflowBlockItem
Para establecer los permisos de API necesarios para la aplicación MobileIron recién creada, haga clic en el nombre de la aplicación en Registros de aplicaciones.
:::

:::WorkflowBlockItem
Haga clic en **Permisos de API** > **Añadir un permiso**.
:::

:::WorkflowBlockItem
En la sección **Microsoft Graph > Permisos delegados > Aplicaciones de administración de dispositivos**, seleccione el permiso **DeviceManagementApps.Read.All** y haga clic en **Guardar**. De forma predeterminada, se activará el permiso user.Read para la aplicación.
:::

:::WorkflowBlockItem
Para conceder el acceso, haga clic en **Otorgar consentimiento del administrador para MobileIron**.
:::

:::WorkflowBlockItem
Realice el siguiente procedimiento para el portal de administración de Ivanti Neurons for MDM.
:::
::::

### Procedimiento para el portal administrativo de Ivanti Neurons for MDM

::::WorkflowBlock
:::WorkflowBlockItem
Abra el segundo navegador e inicie sesión en el portal de administración Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Vaya a **Administrador > Microsoft Azure > Office 365 App Protection**.
:::

:::WorkflowBlockItem
Pegue la **ID de la aplicación** en el portal de administración Ivanti Neurons for MDM .
:::

:::WorkflowBlockItem
**Procedimiento**

1. Vaya al portal de Azure.
2. Seleccione la aplicación de MobileIron >**&#x20;Propiedades**.
3. Copie el **Id. de la aplicación**.
4. Vuelva a **Administrador > Microsoft Azure > Office 365 App Protection** en el Portal de administración.
5. Péguelo en el campo **Id. de la aplicación**.
   Pegue el **Secreto de la aplicación** (secreto del cliente) en el Portal de administración Ivanti Neurons for MDM .
:::

:::WorkflowBlockItem
**Procedimiento**

1. Vaya al portal de Azure.
2. Seleccione la aplicación de MobileIron.
3. Haga clic en **Claves** e introduzca un nombre en la **Descripción de la clave** y seleccione un tiempo-período de caducidad en **Duración**.
4. Haga clic en **Guardar** y copie el valor **Clave**.
5. Vuelva a **Administrador > Microsoft Azure > Office 365 App Protection** en el Portal de administración.
6. Péguelo en el campo **Secreto de la aplicación**.
   Pegue el **Id. del abonado** en el portal de administración Ivanti Neurons for MDM .
:::

:::WorkflowBlockItem
**Procedimiento**

1. Vaya al portal de Azure.
2. Haga clic en Entra ID en el panel izquierdo y luego en Propiedades.
3. Copie el Id. de Directory.
4. Vuelva a **Administrador > Microsoft Azure > Office 365 App Protection** en el Portal de administración.
5. Péguelo en el campo **Id. del abonado**.
   Introduzca su **Nombre de usuario** y **Contraseña** de administrador de Intune.
:::

:::WorkflowBlockItem
- La cuenta Azure debe tener derechos de administración global o derechos limitados de administración + de administración del servicio de Intune.
- Ivanti recomienda crear una cuenta local Azure con solo los derechos de administración del servicio de Intune. Las cuentas de usuario que se federan a un proveedor de identidad no son compatibles con Microsoft para la autenticación con las API de Graph.
  Haga clic en **Autenticar y Guardar**.

Si la fecha introducida es incorrecta, aparecerá un mensaje de error.
:::
::::

## Políticas para la protección de aplicaciones de Office 365

Después de configurar las credenciales de Microsoft Graph, vaya a **Aplicaciones > Protección de la aplicación Office 365** para añadir nuevas políticas de protección de aplicaciones de Office 365 para dispositivos iOS o Android para diferentes grupos de usuarios.

Las políticas se enumeran en la página **Aplicaciones > Protección de aplicaciones de Office 365**, en la pestaña **Políticas de aplicaciones**. Esta lista de políticas ofrece detalles tabulares como la marca de hora actualizada, la plataforma, aplicaciones asignadas y grupos de usuarios implementados.

### Añadir una política de protección de aplicaciones de Office 365 para dispositivos iOS

Procedimiento

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
:::

:::WorkflowBlockItem
Haga clic en **Políticas de aplicaciones > + Añadir**.
:::

:::WorkflowBlockItem
Introduzca un **Nombre** y una **Descripción** opcional para la política.
:::

:::WorkflowBlockItem
En Elegir SO, haga clic en **iOS**.
:::

:::WorkflowBlockItem
En **Reubicación de los datos**, seleccione una opción de los siguientes ajustes y opciones:\* Impedir copias de seguridad de iTunes y iCloud

- Permitir que la aplicación transfiera datos a otras aplicaciones: Todas las aplicaciones (predeterminado), Aplicaciones administradas por políticas, Ninguna
- Permitir que la aplicación reciba datos de otras aplicaciones: Todas las aplicaciones (predeterminado), Aplicaciones administradas por políticas, Ninguna
- Impedir la función «Guardar como»
- Restringir las funciones de cortar, copiar y pegar con otras aplicaciones: Cualquier aplicación (predeterminado), Bloqueado, Aplicaciones administradas por políticas, Política administrada con función «pegar en»
- Restringir el contenido web que se mostrará en el navegador administrado
- Cifrar datos de las aplicaciones: Cuando el dispositivo está bloqueado (predeterminado), Cuando el dispositivo está bloqueado y hay archivos abiertos, Después del reinicio del dispositivo, Usar ajustes del dispositivo
- Desactivar la sincronización de contactos
- Desactivar la impresión
:::

:::WorkflowBlockItem
En **Acceso**, seleccione una opción de los siguientes ajustes y opciones:
:::

:::WorkflowBlockItem
- Requerir un PIN para el acceso
- Número de intentos permitidos antes de restablecer el PIN (valor predeterminado: 5 intentos)
- Permitir un PIN simple
- Longitud del PIN (valor predeterminado: 4)
- Permitir huella digital en lugar de PIN (iOS 8+)
- Desactivar el PIN de la aplicación cuando el PIN del dispositivo está administrado
- Requerir credenciales corporativas para acceder
- Bloquear aplicaciones administradas para que no puedan ejecutarse en dispositivos con «jailbreaks» y descifrados.
- Volver a comprobar los requisitos de acceso después de (minutos)
  - Tiempo de espera: debe ser un valor entre 1 y 65535 (valor predeterminado: 30)
  - Período de gracia sin conexión: debe ser un valor entre 1 y 65535 (valor predeterminado: 720)
  - Intervalo sin conexión (días) antes de borrar los datos de la aplicación: debe ser un valor entre 1 y 65535 (valor predeterminado: 90)
    Requerir un sistema operativo mínimo de iOS
- Requerir un sistema operativo mínimo de iOS (solo advertencia)
- Requiere una versión mínima de la aplicación
- Requerir una versión mínima de la aplicación (solo advertencia)
- Requiere una versión mínima de SDK de la política de protección de aplicaciones de Intune
  Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione y asigne las aplicaciones en las que se implementará esta política.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione los grupos de usuarios en los que se aplicará esta política.
:::

:::WorkflowBlockItem
Haga clic en **Hecho**.
:::
::::

### Añadir una política de protección de aplicaciones de Office 365 para dispositivos Android

**Procedimiento**

1. Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
2. Haga clic en **Políticas de aplicaciones > + Añadir**.
3. Introduzca un **Nombre** y una **Descripción** opcional para la política.
4. En Elegir SO, haga clic en **Android**.
5. En **Reubicación de los datos**, seleccione una opción de los siguientes ajustes y opciones:\* Impedir copias de seguridad de Android
   - Permitir que la aplicación transfiera datos a otras aplicaciones: Todas las aplicaciones (predeterminado), Aplicaciones administradas por políticas, Ninguna
   - Permitir que la aplicación reciba datos de otras aplicaciones: Todas las aplicaciones (predeterminado), Aplicaciones administradas por políticas, Ninguna
   - Impedir la función «Guardar como»
   - Restringir las funciones de cortar, copiar y pegar con otras aplicaciones: Cualquier aplicación (predeterminado), Bloqueado, Aplicaciones administradas por políticas, Política administrada con función «pegar en»
   - Restringir el contenido web que se mostrará en el navegador administrado
   - Cifrar datos de las aplicaciones
   - Desactivar el cifrado de aplicaciones cuando está activado el cifrado de dispositivos
   - Desactivar la sincronización de contactos
   - Desactivar la impresión
6. En **Acceso**, seleccione una opción de los siguientes ajustes y opciones:\* Requerir un PIN para el acceso
   - Número de intentos permitidos antes de restablecer el PIN (valor predeterminado: 5 intentos)
   - Permitir un PIN simple
   - Longitud del PIN (valor predeterminado: 4)
   - Permitir huella digital en lugar de PIN (Android 6+)
   - Desactivar el PIN de la aplicación cuando el PIN del dispositivo está administrado
   - Requerir credenciales corporativas para acceder
   - Bloquear aplicaciones administradas para que no puedan ejecutarse en dispositivos con «jailbreaks» y descifrados.
   - Volver a comprobar los requisitos de acceso después de (minutos)\* Tiempo de espera: debe ser un valor entre 1 y 65535 (valor predeterminado: 30)
     - Período de gracia sin conexión: debe ser un valor entre 1 y 65535 (valor predeterminado: 720)
     - Intervalo sin conexión (días) antes de borrar los datos de la aplicación: debe ser un valor entre 1 y 65535 (valor predeterminado: 90)
   - Bloquear captura de pantalla y asistente de Android
   - Requerir un sistema operativo mínimo de Android
   - Requerir un sistema operativo mínimo de Android (solo advertencia)
   - Requiere una versión mínima de la aplicación
   - Requerir una versión mínima de la aplicación (solo advertencia)
   - Requiere una versión mínima de SDK de la política de protección de aplicaciones de Intune
7. Haga clic en **Siguiente**.
8. Seleccione las aplicaciones en las que se implementará esta política.
9. Haga clic en **Siguiente**.
10. Seleccione los grupos de usuarios en los que se aplicará esta política.
11. Haga clic en **Hecho**.

### Modificar una política de protección de aplicaciones de Office 365

Procedimiento

1. Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
2. Haga clic en **Políticas de aplicaciones**.
3. Haga clic en el nombre de la política que desee modificar.
4. En la página de detalles de la política, haga clic en **Editar**.
5. Modifique los ajustes de configuración de la política.
6. Haga clic en **Siguiente**.
7. Modifique la lista de aplicaciones en las que se aplicará esta política.
8. Haga clic en **Siguiente**.
9. Modifique los grupos de usuarios en los que se aplicará esta política.
10. Haga clic en **Hecho**.

### Eliminar una política de protección de aplicaciones de Office 365

Procedimiento

1. Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
2. Haga clic en **Políticas de aplicaciones**.
3. En la columna **Acciones**, haga clic en el icono de eliminar que hay junto al nombre de la política que desea eliminar.
4. Haga clic en **Sí** para confirmar.

## Configuraciones de las aplicaciones de Office 365

Vaya a la página **Aplicaciones > Protección de aplicaciones de Office 365**, en la pestaña **Configuración de aplicaciones**, para añadir, modificar o eliminar las configuraciones de aplicaciones de Office 365 para diferentes grupos de usuarios. En las configuraciones de estas aplicaciones, los administradores pueden añadir una lista de pares clave/valor. y asignar las configuraciones a una o más aplicaciones de Office 365. La pestaña Configuración de aplicaciones enumera las configuraciones con detalles tabulares como la marca de hora actualizada, las aplicaciones asignadas y el estado de la implementación.

### Añadir una configuración de las aplicaciones de Office 365

Procedimiento

1. Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
2. Haga clic en **Configuración de aplicaciones > + Añadir**.
3. Introduzca un **Nombre** y una **Descripción** opcional para la configuración.
4. Introduzca los pares clave/valor.
5. Haga clic en **Siguiente**.
6. Seleccione las aplicaciones en las que se implementará esta configuración.
7. Haga clic en **Siguiente**.
8. Seleccione los grupos de usuarios en los que se aplicará esta configuración.
9. Haga clic en **Hecho**.

### Modificar una configuración de las aplicaciones de Office 365

Procedimiento

1. Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
2. Haga clic en **Configuración de aplicaciones**.
3. Haga clic en el nombre de la configuración que desee modificar.
4. En la página de detalles de configuración, haga clic en **Editar**.
5. Alternativamente, también puede hacer clic en las pestañas **Distribución de aplicaciones** o **Distribución de grupo de usuarios**. Haga clic en **Editar** para modificar solo esos ajustes y haga clic en **Guardar**.
6. Modifique los ajustes de configuración.
7. Haga clic en **Siguiente**.
8. Modifique la lista de aplicaciones en las que se aplicará esta configuración.
9. Haga clic en **Siguiente**.
10. Modifique los grupos de usuarios en los que se aplicará esta configuración.
11. Haga clic en **Hecho**.

### Eliminar una configuración de las aplicaciones de Office 365

Procedimiento

1. Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
2. Haga clic en **Configuración de aplicaciones**.
3. En la columna **Acciones**, haga clic en el icono de eliminar que hay junto al nombre de la configuración que desea eliminar.
4. Haga clic en **Sí** para confirmar.

## Usuarios que infringen el cumplimiento de las aplicaciones de Office 365

Los administradores pueden revisar la lista de usuarios y sus dispositivos en cuanto al no cumplimiento. Utilice esta página para borrar cualquier aplicación de Office 365 en dichos dispositivos marcados.

### Borrar aplicaciones de Office 365

Procedimiento

1. Vaya a **Aplicaciones > Protección de aplicaciones de Office 365**.
2. Haga clic en **Usuarios que infringen el cumplimiento**.
3. Lleve a cabo una de las siguientes acciones:\* Seleccione a los usuarios de la lista y haga clic en **Borrar aplicaciones de Office 365**.
   - Haga clic en el nombre del usuario para visualizar la lista de dispositivos que tienen aplicaciones que infringen el cumplimiento. En la columna **Acción**, haga clic en el icono **Borrar aplicaciones de Office 365** que hay junto a un dispositivo específico.
   - Haga clic en el nombre del usuario para visualizar la lista de dispositivos que tienen aplicaciones que infringen el cumplimiento. Haga clic en el nombre de un dispositivo específico para ver las aplicaciones enumeradas con Id. del conjunto/nombres de paquetes y los motivos marcados. Haga clic en **Borrar aplicaciones de Office 365**.
4. Haga clic en **Sí** para confirmar la acción.

Alternativamente, lleve a cabo los siguientes pasos:

1. Vaya a **Usuarios.**
2. Haga clic en el nombre del usuario para visualizar la página de detalles del usuario.
3. Haga clic en **Acción >&#x20;****Borrar aplicaciones de Office 365**.
4. Seleccione los dispositivos de los que hay que borrar aplicaciones de Office 365.
5. Haga clic en **Aceptar** para confirmar la acción.

### Cancelar solicitudes de borrado de aplicaciones de Office 365

Procedimiento

1. Vaya a **Usuarios.**
2. Haga clic en el nombre del usuario para visualizar la página de detalles del usuario.
3. Haga clic en la pestaña **Protección de Office 365**.
4. Desde el cuadro desplegable **Seleccionar tipo de informe**, seleccione el informe **Solicitudes de borrado** para visualizar la información correspondiente.
5. Seleccione los dispositivos en los que hay que cancelar solicitudes de borrado. Solo se pueden seleccionar dispositivos con estado «Borrado pendiente».
6. Haga clic en **Cancelar borrado**.
7. Haga clic en **Aceptar** para confirmar la acción.

## Informes de aplicaciones para los usuarios con la Protección de aplicaciones de Office 365

Los administradores pueden seleccionar uno de los siguientes informes para revisar la lista de usuarios con Protección de aplicaciones de Office 365 e información relacionada:

- Informe de política de aplicaciones
- Informe de configuración de aplicaciones
- Borrar solicitudes

La información en los Informes de aplicaciones incluye el Id. del conjunto/nombre del paquete, Nombre del dispositivo, Tipo de dispositivo, Políticas o Configuraciones (implementadas en el dispositivo, Estado (Sincronizado, Sincronizado pero desactualizado o No sincronizado) y la hora del Último ingreso. La información de los Informes de aplicaciones se puede exportar a un archivo CSV para consultarla o analizarla posteriormente.

La información del informe de Solicitudes de borrado incluye en Nombre en pantalla, Nombre del usuario, Nombre del dispositivo, Tipo de dispositivo y Estado de borrado (Borrado pendiente o Borrado completo).

Realice los siguientes pasos para ver uno de los informes:

1. Vaya a **Usuarios.**
2. Haga clic en el nombre del usuario para visualizar la página de detalles del usuario.
3. Haga clic en la pestaña **Protección de Office 365**.
4. Desde el cuadro desplegable **Seleccionar tipo de informe**, seleccione uno de los informes para visualizar la información correspondiente.
5. (Opcional) Desde la página de informes de Solicitudes de borrado, seleccione los dispositivos en los que hay que cancelar solicitudes de borrado y haga clic en **Cancelar borrado**. Solo se pueden seleccionar dispositivos con estado «Borrado pendiente».
6. (Opcional) Haga clic en **Exportar a CSV&#x20;**&#x70;ara descargar el contenido del informe en un archivo CSV para consultarlo o analizarlo posteriormente.
