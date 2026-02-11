---
title: Configuración de los perfiles de Windows Autopilot
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Windows Autopilot es una característica de Microsoft que ayuda a los administradores a configurar y pre-configurar nuevos dispositivos para que estén listos para la empresa. La función de Autopilot ayuda a un aprovisionamiento rápido, fiable y sin problemas de los dispositivos Windows Desktop o HoloLens2. Además, la función Autopilot ayuda a realizar las siguientes tareas:

- Unir automáticamente dispositivos a Entra ID (Entra ID)
- Inscribir automáticamente los dispositivos en los servicios MDM
- Crear y auto-asignar dispositivos a grupos de configuración basados en el perfil del dispositivo
- Personalizar la experiencia de inscripción
- Aplicar configuraciones y políticas
- Instalar aplicaciones esenciales

### Requisitos previos

Para utilizar la página Windows Autopilot, revise los pasos para socios de Ivanti Neurons for MDM y los requisitos de licencia de Azure. Asegúrese de que se cumplen los siguientes requisitos previos para que la función Autopilot funcione como se espera:

- **Licencias de Azure para requisitos de Autopilot**: compruebe los "Requisitos de licencia de Windows Autopilot".
- **Registro de dispositivos Azure Windows Autopilot**: compruebe la "Descripción general del registro de Windows Autopilot".
- **Distribuidores que añaden dispositivos a la cuenta del cliente**: marque la opción "Usar perfiles de Windows Autopilot en dispositivos nuevos para personalizar la experiencia inicial del cliente".

### Requisitos adicionales

1. Integre los abonados de Entra ID e Ivanti Neurons for MDM. Para obtener más información, consulte [**Configuración con Microsoft Azure**](./Configuración_con_Microsoft_Azure.md).
2. Asegúrese de que dispone de una cuenta de administrador en Ivanti Neurons for MDM y Entra ID.
3. Para aprovechar los perfiles de despliegue automático, cree un usuario falso para el registro de dispositivos de despliegue automático sin usuario en Ivanti Neurons for MDM.
4. Cree y sincronice un usuario ficticio, fooUser\@Entra IDDominioPrimario.com desde Entra ID DominioPrimario.No se necesitan licencias de Microsoft para crear y sincronizar un usuario ficticio.
5. La página "Nombres de dominio personalizados" en Entra ID muestra el dominio primario de su entorno Entra ID.
6. Asegúrese de que el usuario puede inscribir dispositivos y no está deshabilitado. Por ejemplo, si el dominio principal es contoso.com, el usuario resultante será [**fooUser@contoso.com**](mailto\:fooUser@contoso.com). Si el dominio principal es contoso.onmicrosoft.com, el usuario resultante será [**fooUser@contoso.onmicrosoft.com**](mailto\:fooUser@contoso.onmicrosoft.com).
7. Para aprovisionar al usuario con SCIM en Ivanti Neurons for MDM, edite los detalles del usuario en Entra ID y añada la dirección de correo electrónico. Generalmente, la dirección de correo electrónico será la misma que el UPN.
8. Asegúrese de que todos los usuarios, incluido fooUser, estén presentes en Azure y en Ivanti Neurons for MDM.
9. Los administradores pueden crear perfiles de Autopilot mediante Microsoft Store for Business o Ivanti Neurons for MDM. Para crear perfiles utilizando administradores de Ivanti Neurons for MDM se requieren permisos de administrador de Entra IDmin Global e Intune.Los administradores necesitan Azure P1 o P2 y se necesitan licencias Ivanti Neurons for MDM Secure UEM o Secure UEM Premium. La licencia de Intune no es necesaria para los administradores.En Neurons for MDM, la función de creación de perfiles de autopilot aprovecha las API de Microsoft Graph para autopilot, que aún están en fase beta.

### Modos de inscripción del Autopilot

Después de asociar los dispositivos con un grupo de perfiles de usuario específico, basado en el uso del dispositivo, puede configurar el modo de inscripción del Autopilot para permitir a los usuarios comenzar rápidamente con su dispositivo. Ivanti Neurons for MDM ofrece los siguientes modos de inscripción del Autopilot:

- Modo de auto-despliegue
- Impulsado por el usuario (modo preaprovisionado)
- Impulsado por el usuario

**Modo Autopilot de despliegue automático**: el modo Autopilot de despliegue automático de dispositivos garantiza un despliegue sin problemas de un dispositivo de empresa para un usuario evitando la configuración inicial del dispositivo y enviando todos los archivos de configuración necesarios para que el dispositivo se ponga en marcha de forma segura. Este modo asegura el hardware, conecta el dispositivo a la red de la empresa, inscribe el dispositivo al Entra ID (ID de Entra), el servicio MDM, y al portal del administrador de Ivanti Neurons for MDM usando un ID de usuario ficticio y todos los archivos de configuración necesarios son empujados al dispositivo antes de que el usuario inicie sesión. Después de que los archivos de configuración obligatorios se empujan al dispositivo, el dispositivo se reinicia y muestra la pantalla de inicio de sesión para que el usuario de la empresa comience. Puede utilizar el modo de auto-despliegue para un dispositivo que puede ser utilizado como un Kiosko o un dispositivo firmado digitalmente.

**Modo de perfil de preaprovisionamiento impulsado por el usuario**: Una vez que el administrador crea un perfil de preaprovisionamiento impulsado por el usuario, el administrador asigna el perfil a un grupo de usuarios, y el ID de hardware del dispositivo se carga y se asigna al grupo Entra ID. El dispositivo se asociará al perfil de pre-aprovisionamiento impulsado por el usuario. Este modo lo utiliza el administrador para configurar un dispositivo antes de entregarlo al usuario de la empresa.

**Procedimiento**

Siga los pasos para el despliegue preaprovisionado:

1. Conecte el nuevo dispositivo de hardware a la LAN y pulse cinco veces el botón de Windows.
2. El dispositivo muestra una pregunta. Seleccione la opción de aprovisionamiento del autopilot de Windows y haga clic en Continuar. El Entra ID detecta el modo de perfil de preaprovisionamiento dirigido por el usuario, y todos los ajustes básicos de configuración se despliegan en el dispositivo. Se muestra la pantalla de configuración del autopilot de Windows.
3. Haga clic en Continuar. El dispositivo progresa y asegura el hardware, conecta el dispositivo a la red de la empresa, inscribe el dispositivo al Entra ID (ID de Entra), el servicio MDM, y al portal del administrador de Ivanti Neurons for MDM usando un ID de usuario ficticio y todos los archivos de configuración necesarios son empujados al dispositivo y aparece un mensaje de confirmación.
4. Ahora puede entregar el dispositivo al usuario. Cuando el usuario inicia sesión en el dispositivo, el ID de usuario se registra en el portal del administrador de Ivanti Neurons for MDM con los detalles del dispositivo.

- Las siguientes configuraciones se transfieren automáticamente antes de que el usuario inicie sesión en el dispositivo:\* Certificado de identidad
  - Wi-Fi
  - Windows Hello para empresas
  - Restricciones de Windows

El resto de configuraciones se encuentran en estado Pendiente y se envían después de que el usuario inicie sesión en el dispositivo mediante una dirección de correo electrónico.

Durante el proceso de inscripción de Autpilot en los modos de autoimplantación e impulsado por el usuario (preaprovisionamiento), las aplicaciones .MSI y .EXE asignadas se instalarán en el dispositivo para completar el proceso de inscripción. Al instalar las aplicaciones .MSI y .EXE durante el proceso de inscripción en Autopilot, si las aplicaciones informan o no lo hacen durante la instalación, el proceso de Autopilot se completará y se activará el botón Volver a sellar.

## Creación de perfiles de usuario de Windows Autopilot

Después de configurar la Fuente de Usuario Entra ID (Entra ID) y sincronizar los usuarios y grupos de usuarios Entra ID con el inquilino Ivanti Neurons for MDM, puede crear los perfiles de Autopilot.

**Procedimiento**

1. Inicie sesión en el portal del administrador de Ivanti Neurons for MDM
2. Vaya a **Administrador > Microsoft Azure > Administración de dispositivos de Windows**.Si no está configurada la Fuente de Usuario de Entra ID, el botón **Agregar** estará desactivado. Debe configurar la Fuente de usuario mediante la opción de **Administración de dispositivos de Windows** presente en la sección de **Microsoft Azure**.
3. Haga clic en **Añadir**.Aparecerá en pantalla la página de **Añadir Perfil de Autopilot de Windows**.
4. Introduzca un nombre de perfil en la casilla **Nombre**.
5. Complete la **Configuración del perfil** utilizando la tabla a continuación de este procedimiento.
6. Haga clic en **Siguiente**.Aparecerá en pantalla una nueva página con todos los grupos de dispositivos Entra ID.
7. Seleccione uno o más Grupos de Dispositivos Entra ID a los que se debe asignar el Perfil del Autopilot.
8. También puede crear un Grupo de Dispositivos Entra ID y asignar el Perfil de Autopilot a este grupo recién creado. Consulte para obtener más información.
   Si desea asignar el Perfil de Autopilot a todos los Grupos Entra ID, seleccione la opción **Asignar a todos los Grupos Entra ID**.No se puede asignar más de un perfil a "Todos los grupos" debido a una limitación de Microsoft.
9. Haga clic en **Hecho**.

| Ajuste                  | Descripción                                                                                    |
| ----------------------- | ---------------------------------------------------------------------------------------------- |
| **Tipo de dispositivo** | Seleccione una de las dos opciones siguientes en función del dispositivo:\* **PC con Windows** |

- **HoloLens** : Cuando se selecciona esta opción, el modo de despliegue predeterminado debe establecerse en el modo de **auto-despliegue**.En raras ocasiones, al inscribir dispositivos HoloLens 2 mediante el uso de Autopilot, la inscripción podría quedarse atascada en la pantalla "Configurar el dispositivo para el trabajo". En este caso, el usuario debe apagar y encender el dispositivo pulsando el botón de encendido. A continuación, el dispositivo muestra la pantalla de inicio de sesión, en la que el usuario debe introducir las credenciales de Entra ID para completar la inscripción. |
  \| **Modo de despliegue**                                     | - **Auto-despliegue**: En este modo, el despliegue del dispositivo ocurre con poca o ninguna participación manual.
- **Dirigido al usuario** \:Los administradores pueden utilizar esta opción para seleccionar el modo de inscripción para configurar un nuevo dispositivo para el usuario antes de entregar el dispositivo al usuario.                                                                                                                                                                                                                                                                                                                                                                     |
  \| **Tipo de cuenta de usuario**                              | \* **Administrador**: Seleccione esta opción si el usuario necesita un control total una vez desplegado el dispositivo.
- **Estándar**: Seleccione esta opción si el usuario necesita autorización a las opciones básicas una vez desplegado el dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| **Idioma**                                                 | De forma predeterminada, el idioma será el específico del sistema operativo. Puede cambiar a un idioma diferente de la lista.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| **Convertir todos los dispositivos asignados a Autopilot** | Seleccione esta opción para convertir todos los dispositivos del grupo asignado al Autopilot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| **Permitir el aprovisionamiento previo**                   | Seleccione esta opción para registrar los dispositivos para el Autopilot utilizando el proceso de registro normal. Esta opción no está disponible cuando se selecciona la opción de **auto-aprovisionamiento**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| **Configurar automáticamente el teclado**                  | Seleccione **Sí** para omitir la selección del teclado en caso de que la opción **Idioma** esté configurada con un valor diferente al predeterminado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| **Nombre de la plantilla del dispositivo**                 | Introduzca un nombre de plantilla para utilizar durante el proceso de inscripción del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| **Términos de licencia del software de Microsoft**         | Puede mostrar u ocultar esta opción sólo en el modo de despliegue dirigido por el usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| **Ajustes de privacidad**                                  | Puede mostrar u ocultar esta opción sólo en el modo de despliegue dirigido por el usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| **Cambiar las opciones de la cuenta**                      | Puede mostrar u ocultar esta opción sólo en el modo de despliegue dirigido por el usuario y cuando el tipo de cuenta de usuario es de tipo estándar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Administrador de dispositivos Windows**

El administrador puede configurar la función de Autopilot en un abonado mediante la nueva opción de Administración de dispositivos de Windows. Esta opción facilita la integración con Ivanti Neurons for MDM si el usuario dispone de un entorno Entra ID.

Para acceder a esta opción, **Administrador** > **Microsoft Azure** > **Administración de dispositivos de Windows**.

Esta integración da permiso a Ivanti Neurons for MDM para que administre dispositivos, perfiles de Autopilot, comprobar el cumplimiento de dispositivos de Windows y para validar el abonado de Azure.

**Temas relacionados**

- [**TenantLockdown CSP**](./TenantLockdown_CSP.md)

## Creación de grupos de dispositivos de Entra ID

El administrador puede crear Grupos de Dispositivos de Entra ID, como y cuando sea necesario, desde la sección Grupos de Dispositivos de Entra ID. La validación del inquilino de Entra ID debe haber sido configurada en la sección Cumplimiento de Dispositivos para crear Grupos de Dispositivos de Entra ID.

**Procedimiento**

1. Vaya a **Administración** > **Microsoft Azure** > **Grupos de dispositivos de Entra ID&#x20;**.
2. Aparecerá en pantalla la página **Grupos de dispositivos de Entra ID**.
   Haga clic en **ADD**.
3. La página **Ajustes del grupo** aparece en la pantalla.
   Proporcione los siguientes detalles:\* Nombre del grupo
   - Descripción del grupo
   - Tipo de pertenencia\* Dispositivo estático: el administrador obtendrá la lista de dispositivos estáticos en la ventana **Asignar pertenencias a grupos**. Seleccione los dispositivos necesarios y haga clic en **Guardar**.
     - Dispositivo dinámico: el administrador debe proporcionar determinados criterios en la ventana de **Consulta dinámica**.

Se creará el nuevo Grupo de Dispositivos de Entra ID y el administrador podrá añadir dispositivos al grupo recién creado.

Después de crear un grupo dinámico, los dispositivos se listarán en la pestaña Dispositivos del grupo de dispositivos específico transcurrido un tiempo.

## Edición de dispositivos Autopilot

Los usuarios pueden editar los dispositivos Autopilot desde el portal administrativo de Ivanti Neurons for MDM

**Requisitos previos**

Asegúrese de que se cumplan los siguientes requisitos previos:

- El usuario IT Admin debe tener permisos Azure Global Admin e Intune Admin.
- Solo se puede establecer un nombre de usuario si el usuario está configurado.
- Una vez establecido, el nombre del dispositivo no se puede anular.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Inicie sesión en el portal administrativo de Ivanti Neurons for MDM
:::

:::WorkflowBlockItem
Ir a**Administración** > **Windows** > **Autopilot**. Los dispositivos Autopilot se enumeran en la pestaña Dispositivos de Autopilot.
:::

:::WorkflowBlockItem
Hacer clic en **Editar** (icono de lápiz). Aparece la página de edición.
:::

:::WorkflowBlockItem
Modifique los siguientes detalles:
:::

:::WorkflowBlockItem
- **Usuario**
- **Nombre fácilmente recordable por el usuario**
- **Nombre del dispositivo**
- **Etiqueta de grupo**
  Haga clic en **Guardar**. Los detalles del dispositivo se actualizan.
:::
::::

## Eliminación de dispositivos Autopilot

Los usuarios pueden eliminar los dispositivos Autopilot desde el portal administrativo de Ivanti Neurons for MDM.

1. Inicie sesión en el portal administrativo de Ivanti Neurons for MDM
2. Ir a**Administración** > **Windows** > **Autopilot**. Los dispositivos Autopilot se enumeran en la pestaña Dispositivos de Autopilot.
3. Haga clic en **Eliminar**. Los detalles del dispositivo se eliminan.
