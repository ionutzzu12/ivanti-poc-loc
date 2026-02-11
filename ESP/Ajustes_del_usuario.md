---
title: Ajustes del usuario
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Editar el ajuste predeterminado**](./Ajustes_del_usuario.md)
- [**Añadir un ajuste personalizado**](./Ajustes_del_usuario.md)
- [**Eliminar un ajuste personalizado**](./Ajustes_del_usuario.md)
- [**Configurar los ajustes para registros de nuevos dispositivos**](./Ajustes_del_usuario.md)
- [**Configurar el límite de dispositivos por usuario**](./Ajustes_del_usuario.md)
- [**Configurar el límite de borrado de dispositivos**](./Ajustes_del_usuario.md)
- [**Ajustes del usuario**](./Ajustes_del_usuario.md)
- [**Configurar la autenticación del Portal de autoservicio**](./Ajustes_del_usuario.md)
- [**Establecer la complejidad de la contraseña**](./Ajustes_del_usuario.md)
- [**Definir los Términos del servicio**](./Ajustes_del_usuario.md)
- [**Configurar los correos electrónicos con los recordatorios de invitaciones para el usuario**](./Ajustes_del_usuario.md)
- [**Configuración de los correos electrónicos de confirmación de registro del usuario**](./Ajustes_del_usuario.md)
- [**Configurar el ajuste del horario de trabajo del usuario**](./Ajustes_del_usuario.md)
- [**Configurar el ajuste de autenticación del Portal de administración**](./Ajustes_del_usuario.md)

Los ajustes del usuario definen las opciones de registro de los dispositivos. Hay diferentes tipos:

- **Ajuste de registro de dispositivos**: establece la autenticación por contraseña, PIN o ambos; tipo de Apple Enrollment y propiedad del dispositivo.
  - Anteriormente, si se configuraba SAML auth/IdP, la autenticación SAML se utilizaba tanto para el registro de dispositivos como para la autenticación del portal. A partir de la versión 79.1, se ha habilitado un interruptor para elegir diferentes métodos de autenticación para el acceso al Portal de administración y el Registro de dispositivos. El interruptor solo es aplicable para el registro de dispositivos.Esta funcionalidad no es compatible con el tipo de autenticación de PIN solamente.
    **Ajuste de Límite de dispositivos**: establece el número de dispositivos que puede registrar un usuario.
- **Ajuste de límite de borrado**: establece el límite del número máximo de dispositivos que se pueden borrar de una vez.
- **Ajuste de autenticación del portal de autoservicio:** Establezca el tipo de autenticación de la contraseña para el portal de autoservicio.
- **Ajuste de complejidad de la contraseña**: establece parámetros sobre complejidad de la contraseña y políticas para las cuentas locales que se utilizan para registrar dispositivos y acceder a los portales de autoservicio y del administrador.
- **Ajuste de las Condiciones del servicio:** establece las condiciones de servicio que se muestran al usuario en cada registro del dispositivo.
- **Ajuste del Recordatorio de invitación para el usuario:** establece las fechas y frecuencia para enviar correos electrónicos con recordatorios de invitaciones para el usuario.
- **Ajuste de confirmación del registro del usuario:** controla la capacidad de enviar el correo electrónico de confirmación de registro del usuario. Consulte [**Configuración y uso de los correos electrónicos de confirmación de registro**](./Configuring_registration_confirmation_emails.md)para ver una descripción general de la solución y [**Configuración de los correos electrónicos de confirmación de registro del usuario**](./Ajustes_del_usuario.md) a continuación, para ver instrucciones específicas sobre los ajustes del usuario.
- **Ajuste del horario de trabajo del usuario:**&#x63;ontrola la capacidad de configurar un horario de trabajo del usuario que bloquee toda la comunicación de Sentry con los dispositivos administrados durante las horas prescritas no laborables. Muy útil para usuarios en regiones con leyes de desconexión laboral.
- **Ajustes de autenticación del portal de administración:** controla si Ivanti Neurons for MDM le solicita al administrador solo la contraseña o la contraseña y el PIN.

Puede editar los ajustes predeterminados para el grupo **Todos los usuarios** o añadir ajustes personalizados y asignarlos a otros grupos de usuarios.

## Editar el ajuste predeterminado

Haga clic en el vínculo **Editar** en el ajuste que tiene el icono de bloqueo. No se puede eliminar un ajuste predeterminado.

## Añadir un ajuste personalizado

Haga clic en el vínculo **Añadir ajuste para grupos específicos de usuarios**.

## Eliminar un ajuste personalizado

Haga clic en el icono x.

## Configurar los ajustes para registros de nuevos dispositivos

Puede configurar la versión mínima de SO, el tipo de autenticación y la propiedad del dispositivo para registros de nuevos dispositivos. La URL de inscripción de dispositivos generada en las versiones anteriores de Ivanti Neurons for MDM dejará de funcionar en la versión actual. El administrador deberá regenerar la URL de inscripción de dispositivos para el registro el dispositivo.

**Registro de dispositivos de la lista de permitidos**

- La opción de registrar un dispositivo en una lista de permitidos solamente está disponible en la configuración de usuario predeterminada y no en la configuración de usuario personalizada. Puede cargar un archivo CSV utilizando la plantilla que contiene los números de serie y los atributos de dispositivo personalizados que se utilizan para incluir en la lista de permitidos algunos dispositivos. Puede incluir uno o más atributos de dispositivo personalizados existentes para crear la lista de permitidos. Esto le permitirá asignar atributos a grupos de dispositivos o espacios después del registro.
- Para crear atributos personalizados, vaya a **Administrador >&#x20;**[**Atributos**](./Atributos.md). Los dispositivos iOS y macOS no pueden registrarse a través de iReg si la función de lista de permitidos está activada y el número de serie del dispositivo no se menciona en el archivo CSV. Si el archivo CSV contiene un número de serie duplicado, se considerará la última entrada del archivo CSV y los atributos de dispositivo personalizados asociados con esa entrada se considerarán para la asignación de dispositivo durante el registro.
- Si la opción **Lista de dispositivos permitidos** está activada, solo los dispositivos incluidos en dicha lista podrán registrarse en Ivanti Neurons for MDM. Esta función solo es aplicable a los dispositivos que se registran a través del proceso de registro basado en web. Esto no afectará a los dispositivos que ya estén registrados en Ivanti Neurons for MDM. Después del registro, si el número de serie del dispositivo se elimina del archivo CSV, el dispositivo no se retirará. El usuario mencionado en el archivo CSV es opcional y se asignará solamente si el usuario se menciona en el archivo CSV y es un usuario válido.
- Si desea cargar un nuevo archivo CSV, puede eliminar el archivo CSV existente y cargar el nuevo archivo. Las listas de permitidos solo son compatibles con iReg y si en caso de que se requiera el cliente Go, opte por el registro sin contacto. Para que funciones como AppConnect y Threat Defense funcionen, el cliente Go debe estar instalado en el sistema. Como no se admite el registro en la aplicación, el usuario puede primero registrar el dispositivo a través de iReg, y más tarde, se puede insertar la aplicación Go en los dispositivos desde el catálogo de aplicaciones. Cuando el usuario acepte la instalación de la aplicación, el dispositivo será un dispositivo gestionado y todas las funciones seguirán funcionando después del registro. La configuración «zero-touch» no puede utilizarse en los dispositivos en que el estado de AppConnect es Activo o Inactivo. Solo puede utilizarse cuando el estado de AppConnect es Ninguno. El estado de AppConnect se mantiene como Ninguno hasta que se inicia el cliente Go en el dispositivo después de registrarse a través de iReg.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Inicie sesión en Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Vaya a **Usuarios** > **Ajustes de usuario.**
:::

:::WorkflowBlockItem
En **Ajustes del registro de dispositivos**, haga clic en **+agregar ajuste para grupos de usuarios específicos**.
:::

:::WorkflowBlockItem
Edite el ajuste predeterminado **Tipo de autenticación del registro de dispositivos** o añada uno nuevo.
:::

:::WorkflowBlockItem
Introduzca un nombre en el campo **Nombre**.
:::

:::WorkflowBlockItem
(Opcional) Introduzca una descripción del ajuste.
:::

:::WorkflowBlockItem
En la sección **Ajustes de SO**, defina la versión mínima del SO para iOS, macOS o Windows:
:::

:::WorkflowBlockItem
Seleccione el botón de alternar **Habilitar la versión mínima** y seleccione una versión de SO de la lista desplegable.

El ajuste Habilitar la versión mínima no es aplicable para registros del dispositivo DEP.

Para **Android**:
:::

:::WorkflowBlockItem
- Active la opción **Revisión de seguridad mínima** (solo Android) y especifique el período seleccionando el tipo de duración de las siguientes opciones de la lista desplegable:
  - **día(s)**
  - **mes(es)**
  - **año(s)**
    Active la opción **Lista de permitidos/lista de bloqueados del fabricante** y seleccione cualquiera de las siguientes opciones:
  - **Crear una lista de permitidos**- para permitir que solo se registren los dispositivos de estos fabricantes.
  - **Crear una lista de bloqueados**- para impedir que se registren los dispositivos de estos fabricantes.
    Para añadir a un fabricante:
    1. Haga clic en **Añadir fabricante**.
    2. Escriba el nombre del fabricante en el campo **Nombre del fabricante**.
    3. Haga clic en **Guardar**. El nombre del fabricante añadido aparecerá en la tabla.El nombre del fabricante distingue entre mayúsculas y minúsculas. Para editar o borrar el nombre de un fabricante añadido, haga clic en la opción **Editar** o **Eliminar** del fabricante.
       En la sección Inscripción de Apple, seleccione el Tipo de inscripción de Apple:
:::

:::WorkflowBlockItem
- **Inscripción de dispositivos**
- **Inscripción de usuarios**- predeterminado, la inscripción de usuarios se aplica a los dispositivos iOS y iPadOS.
- (Opcional) **Incluir dispositivo macOS (macOS 10.15+)**: seleccione esta opción para que la Inscripción de usuarios sea aplicable también a los dispositivos macOS.
  En la sección **Método de invitación de registro (solo iOS y Android)**, habilite **Registro solo MAM**.Esta opción debería estar habilitada para los registros de dispositivos «MAM only» y, cuando se habilita, los usuarios son redirigidos a la App Store pública para que descarguen la aplicación del cliente de AppStation.
:::

:::WorkflowBlockItem
En la sección **Tipo de autenticación de registro de dispositivos**, seleccione una de las opciones siguientes de tipo de registro desde el desplegable **Seleccionar tipo de registro**. Si utiliza la Inscripción de dispositivos, asegúrese de que la configuración de Inscripción de dispositivos coincide con su elección.
:::

:::WorkflowBlockItem
- **Solo contraseña**
- **Solo PIN** Cuando selecciona esta opción, se bloquea el botón de alternar Omitir la autenticación de registro de dispositivos IdP.
- **Contraseña y PIN**
  Los usuarios todavía pueden recibir un PIN para completar la activación de la cuenta.
  Esta configuración afecta tanto al registro normal como al registro de Inscripción de dispositivos.

Para PIN, especifique lo siguiente. Durante el registro del dispositivo, el usuario puede hacer clic en **Reenviar PIN** si fuera necesario.
:::

:::WorkflowBlockItem
- **Vigencia del PIN**: durante cuánto tiempo será válido el PIN (1-30 días)
- **Longitud del PIN**: el número de caracteres (4-12)
- **Permitir que el usuario solicite un nuevo PIN**: (cuando lo olvide o caduque)
  Opcionalmente, también puede activar los **Ajustes del propietario del dispositivo** y, a continuación, hacer clic en **Propiedad del usuario** o **Propiedad de la empresa**. Este ajuste cambia la clasificación del dispositivo durante el proceso de registro.
:::

:::WorkflowBlockItem
- Si los **Ajustes del propietario del dispositivo&#x20;**&#x65;stán activados y el administrador ha marcado el dispositivo como Propiedad del usuario, el usuario tendrá la opción de marcar el dispositivo como Propiedad del usuario o Propiedad de la empresa durante la inscripción de dispositivos y también desde el portal de autoservicio. Para los dispositivos con inscripción de usuarios, los ajustes predeterminados de propietario del dispositivo serán «Propiedad del usuario», independientemente de lo que elija el administrador.
- Para dispositivos supervisados, el ajuste de propietario del dispositivo será «Propiedad de la empresa».
  :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/NBVjyZuI1J-Q3Pyc6eTyP_r35deviceownershipusersettings001.png" alt caption}
  Haga clic en **Añadir+** para un grupo de usuarios, como mínimo, en el que desee distribuir el ajuste.
:::

:::WorkflowBlockItem
([**&#x20;Características a pedido**](./Características_a_petición.md) solo para dispositivos iOS y macOS). También puede activar la opción **Lista de permisos de dispositivos** para permitir el registro del dispositivo basado en los números de serie de la lista de permisos.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**. Se abre la página de Distribución de ajustes del usuario.
:::

:::WorkflowBlockItem
Seleccione la distribución del grupo de usuarios.
:::

:::WorkflowBlockItem
Haga clic en **Hecho**.
:::

:::WorkflowBlockItem
Enviar una invitación a los usuario. Para obtener más información, consulte [**Invitar a usuarios**](./Invitar_a_usuarios.md).
:::
::::

Tenga en cuenta los puntos siguientes:

Si el dispositivo de un usuario se registra solo mediante la opción PIN, el usuario recibe un correo electrónico con la confirmación del registro con un PIN de autenticación.

- Se envía un PIN a la Id. de correo electrónico del usuario.
- El usuario introduce el PIN en la página de registro del dispositivo.
- Si el PIN es correcto, el usuario es redirigido para completar el proceso de registro.

Para usuarios configurados con [**Proveedor de identidad**](./Configurar_el_proveedor_de_identidades.md) (IdP) basado en SAML, Ivanti Neurons for MDM es compatible con la autenticación basada en PIN mientras registra el dispositivo. El Tipo de autenticación del registro de un dispositivo debe ser PIN y contraseña. La característica de PIN y contraseña actúa como autenticación de dos factores para mayor seguridad. En este caso, cuando un usuario intenta registrar un dispositivo:

- Se envía un PIN a la Id. de correo electrónico del usuario.
- El usuario introduce el PIN en la página de registro del dispositivo.
- Si el PIN es correcto, el usuario será redirigido a la página de inicio de sesión de IdP, donde el usuario debe introducir el nombre de usuario y la contraseña de IdP.
- Si las credenciales de IdP son correctas, el usuario es redirigido al dispositivo para completar el proceso de registro.

## Configurar el límite de dispositivos por usuario

**Procedimiento**

1. Edite el ajuste predeterminado **Límite de dispositivos** o añada uno nuevo.
2. (Opcional) Haga clic en **+ Agregar configuración para grupos de usuarios específicos** para configurar el límite de dispositivos para grupos de usuarios específicos.
3. Edite o asigne un nombre para identificar el ajuste.
4. Escriba una descripción opcional del ajuste.
5. En el menú desplegable **Número máximo de dispositivos activos**, seleccione el límite de dispositivos Apple activos.
6. En el menú desplegable **Número máximo de dispositivos Apple watchOS para emparejar con un iPhone**, seleccione el límite de dispositivos Apple watchOS activos para emparejar con el iPhone.
7. (Opcional) Si **+ Agregar configuración para grupos de usuarios específicos** está seleccionado, haga clic en **Siguiente** y seleccione al menos un grupo de usuarios para la distribución de esta configuración.
8. Haga clic en **Hecho**.

## Configurar el límite de borrado de dispositivos

**Procedimiento**

1. Edite el ajuste predeterminado del **Límite del borrado de dispositivos**.
2. Active la opción **Habilitar el límite de borrado para todos los usuarios (incluidas las funciones predeterminadas)**.
3. En el campo **Número máximo de dispositivos que un usuario puede borrar a la vez**, escriba el número máximo de dispositivos que se pueden borrar a la vez. El valor predeterminado es 1. Puede establecer un valor máximo de 200 como límite de borrado de dispositivos.
4. Haga clic en **Hecho**.

## Configurar la autenticación del Portal de autoservicio

**Procedimiento**

1. Edite el ajuste predeterminado **autenticación del Portal de autoservicio** o añada uno nuevo haciendo clic en el **ajuste +Añadir para grupos de usuarios específicos**.
2. Edite o asigne un nombre para identificar el ajuste.
3. Escriba una descripción opcional del ajuste.
4. Seleccione un **Tipo de autenticación del Portal de autoservicio** del menú desplegable. Puede ser una de las siguientes opciones:\* Contraseña
   - Certificado
5. Haga clic en **Siguiente**.
6. Seleccione uno o más grupos de usuarios para los que se puede distribuir esta configuración.
7. Haga clic en **Hecho**.

## Establecer la complejidad de la contraseña

Puede establecer parámetros sobre complejidad de la contraseña y políticas para las cuentas locales que se utilizan para registrar dispositivos y acceder a los portales de autoservicio y del administrador.

La longitud, características y políticas de la contraseña establecidas a continuación definen la seguridad de una contraseña.

También definen la dificultad que tendrá el usuario para seleccionar una contraseña válida. Si usa una cuenta local para sus usuarios finales y desea tener contraseñas seguras para acceder al portal del administrador, considere la posibilidad de emplear un PIN para registrar el dispositivo con el objetivo de que la complejidad de la contraseña no interfiera con el registro del dispositivo. Utilice el ajuste de tipo «Autenticación del registro de dispositivos» para seleccionar el modo de autenticación para el registro del dispositivo en **Ajustes del usuario > Ajuste del registro de dispositivos**.

**Procedimiento**

1. Edite los ajustes predeterminados de la **Complejidad de la contraseña**.
2. Defina los siguientes ajustes de complejidad de la contraseña:| **Ajuste**                                    | **Qué hacer**                                                                                                                                                                                    |
   \| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   \| Longitud mínima de la contraseña              | Mueva el control deslizante para especificar la longitud mínima de una contraseña con el objetivo de impedir que el usuario cree contraseñas breves e inseguras.El número oscila entre 8 y 32.   |
   \| Características obligatorias                  | Especifique la cantidad de caracteres de la contraseña que deben cumplirse al seleccionar una contraseña. El mínimo de características que deben cumplirse es 3 (4 para los clientes federales). |
   \| Caracteres especiales (símbolos) obligatorios | Especifique la cantidad de caracteres no alfanuméricos que debe contener una contraseña.                                                                                                         |
   \| Caracteres en mayúscula obligatorios          | Especifique la cantidad de caracteres alfabéticos en mayúscula que debe contener una contraseña.                                                                                                 |
   \| Caracteres en minúsculas obligatorios         | Especifique la cantidad de caracteres alfabéticos en minúscula que debe contener una contraseña.                                                                                                 |
   \| Caracteres numéricos obligatorios             | Especifique la cantidad de caracteres numéricos minúscula que debe contener una contraseña.                                                                                                      |
   \| **Validaciones de la contraseña**             |                                                                                                                                                                                                  |
   \| Secuencia numérica permitida                  | Seleccione la cantidad de números repetidos en una secuencia.Por ej.: 123.                                                                                                                       |
   \| Repetición de caracteres permitida            | Seleccione la cantidad de caracteres alfabéticos repetidos.Por ej.: bbc.                                                                                                                         |
3. Establezca las siguientes políticas sobre contraseñas para personalizar el comportamiento.| **Ajuste**                                      | **Qué hacer**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
   \| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Historial de contraseñas conservado             | Mueva el control deslizante para seleccionar la cantidad de contraseñas nuevas que deben asociarse a la cuenta de un usuario antes de poder usar una contraseña antigua.El número oscila entre 3 y 36.                                                                                                                                                                                                                                                                                                                                                                                      |
   \| Período de caducidad de la contraseña           | Mueva el control deslizante para seleccionar la duración de la caducidad de la contraseña en días.El número oscila entre 30 y 365 días.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   \| Tiempo de espera por inactividad                | Mueva el control deslizante para especificar el tiempo que un usuario puede estar inactivo antes del tiempo de sesión de un portal de administración o de un portal de autoservicio.El número oscila entre 5 y 60 (minutos).                                                                                                                                                                                                                                                                                                                                                                |
   \| Hubo un error en el umbral de inicios de sesión | Mueva el control deslizante para seleccionar la cantidad de intentos de inicio de sesión fallidos que se pueden hacer antes de que el bloqueo de cuenta tenga lugar a los 5 minutos.El número oscila entre 2 y 5.Cuando el número de intentos fallidos esté dentro del límite, se le muestra un mensaje al usuario sobre el bloqueo e indicándole que intente iniciar sesión más tarde.Cuando el número de intentos fallidos supere el límite, se le muestra un mensaje al usuario sobre el bloqueo e indicándole que intente iniciar sesión después de un tiempo determinado (en minutos). |
4. Haga clic en **Hecho**. Si ha cambiado el ajuste predeterminado de Complejidad de la contraseña, la contraseña antigua de la cuenta local existente seguirá siendo la misma. Una vez que caduque, se solicitará al usuario que renueve la contraseña. Para los administradores que estén intentando iniciar sesión en el Portal de administración, pueden contactar con el Soporte técnico, que les dará pautas para restablecer la contraseña.Al registrar un dispositivo, el enfoque recomendado es usar el modo de registro solo PIN.

## Definir los Términos del servicio

**Procedimiento**

1. Cree un nuevo ajuste de los **Términos de servicio**.
2. Asigne un nombre para identificar el ajuste.
3. Escriba una descripción opcional del ajuste.
4. Seleccione **Avisar al usuario**... opción.
5. Escriba un título y el texto para mostrar.
6. Haga clic en **Añadir+** para un grupo de usuarios, como mínimo, en el que desee distribuir el ajuste.
7. Haga clic en **Guardar**.

Una vez que acepte, las condiciones de servicio no se pueden eliminar. No obstante, puede desactivar los avisos para un nuevo registro si desmarca la opción **Avisar al usuario**... opción.

## Configurar los correos electrónicos con los recordatorios de invitaciones para el usuario

Los administradores pueden fomentar las inscripciones a los dispositivos utilizando este ajuste para enviar correos electrónicos con los recordatorios de invitaciones para usuarios.

**Procedimiento**

1. Edite un **ajuste de recordatorio de invitación para el usuario** existente o añada uno nuevo.
2. Edite o asigne un nombre para identificar el ajuste.
3. Escriba una descripción opcional del ajuste.
4. Asegúrese de que la opción **Recordatorios de invitación para el usuario** esté activada.
5. E el campo Definir fechas de inicio y fin, elija cuando quiere empezar a enviar recordatorios por correo electrónico y dejar de hacerlo.La cantidad máxima de correos electrónicos que se pueden enviar es de 30. Para restablecer este límite, el administrador debe volver a enviar la invitación.
6. En el campo Definir la frecuencia, elija la frecuencia con la que desea enviar recordatorios por correo electrónico.
7. Haga clic en **Siguiente**.
8. Seleccione una distribución para esta configuración.
9. Haga clic en **Hecho**.

## Configuración de los correos electrónicos de confirmación de registro del usuario

Los administradores pueden enviar correos electrónicos a los nuevos usuarios que hayan completado el registro.

**Procedimiento**

1. Edite un **ajuste de confirmación de registro del usuario** existente o añada uno nuevo.
2. Edite o asigne un nombre para identificar el ajuste.
3. Escriba una descripción opcional del ajuste.
4. Asegúrese de que esté activada la opción **Enviar un correo electrónico de confirmación cuando el registro de usuario se realice correctamente**.
5. Haga clic en **Siguiente**.
6. Seleccione una distribución para esta configuración.
7. Haga clic en **Hecho**.

## Configurar el ajuste del horario de trabajo del usuario

Los administradores pueden configurar un horario de trabajo del usuario para usuarios que bloquee toda la comunicación de Sentry con los dispositivos administrados durante las horas prescritas no laborables. Es muy útil para usuarios en regiones con leyes de desconexión laboral.

**Procedimiento**

1. Seleccione **Usuarios**.
2. Seleccione **Ajustes del usuario**.
3. En la sección, **Ajuste para grupos específicos de usuarios** seleccione **+Añadir ajuste para grupos específicos de usuarios**.
4. Introduzca un nombre para el ajuste.
5. Active el ajuste.
6. Seleccione la zona horaria.
7. Configure las horas durante las cuales Ivanti Neurons for MDM bloqueará el protocolo de Exchange ActiveSync, las aplicaciones habilitadas para AppConnect para AppConnect y las aplicaciones administradas.
8. Haga clic en **Siguiente**.
9. Configure la distribución y, a continuación, haga clic en **Hecho**.

Los cambios aplicados pueden tardar hasta 1 hora y 15 minutos en tener efecto en el dispositivo.

## Configurar el ajuste de autenticación del Portal de administración

Los administradores pueden ajustar el tipo de autenticación para autenticar el inicio de sesión del usuario. Este ajuste controla si al administrador se le pedirá solo la contraseña o la contraseña y el PIN.

**Procedimiento**

1. Edite un **Ajuste de autenticación del portal de administración** existente o añada uno nuevo.
2. Edite o asigne un nombre para identificar el ajuste.
3. Escriba una descripción opcional del ajuste.
4. En el **Tipo de autenticación del portal de administración**, seleccione cualquiera de las siguientes opciones:| **Opción**                                        | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   \| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Contraseña**                                    | Seleccione esta opción para autenticar el inicio de sesión solo mediante contraseña.Los usuarios todavía pueden recibir un PIN para completar la activación de la cuenta.                                                                                                                                                                                                                                                                                                                                                                                                    |
   \| **Contraseña y PIN**                              | Seleccione esta opción para autenticar el inicio de sesión mediante contraseña y PIN.Al seleccionar esta opción se muestran los siguientes campos:\* **Vigencia del PIN**: seleccione de la lista desplegable la duración en minutos de la vigencia del PIN. Los minutos deben estar en un intervalo de 1 a 15.
   - **Longitud del PIN**: seleccione de la lista desplegable la longitud de caracteres del PIN. La longitud del PIN debe estar en un intervalo de 4 a 12.Esta opción es aplicable solo para las cuentas locales y no para las cuentas de administrador de LDAP. |
     \| **Permitir que el usuario solicite un nuevo PIN** | Seleccione esta opción para permitir a los usuarios que soliciten un nuevo PIN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
5. Haga clic en **Siguiente**.
6. Seleccione una distribución para esta configuración.
7. Haga clic en **Hecho**.

Para usuarios configurados con [**Identity Provider**](./Configurar_el_proveedor_de_identidades.md) (IdP),Ivanti Neurons for MDMbasado en SAML, admite la autenticación mediante PIN en el portal de administración. El Tipo de autenticación del portal de administración debe ser PIN y contraseña. Esta característica actúa como autenticación de dos factores para mayor seguridad. En este caso, cuando dicho usuario intente iniciar sesión en el portal:

- Se envía un PIN a la Id. de correo electrónico del usuario.
- El usuario introduce el PIN en la página de inicio de sesión del portal de administración.
- Si el PIN es correcto, el usuario será redirigido a la página de inicio de sesión de IdP, donde el usuario debe introducir el nombre de usuario y la contraseña de IdP.
- Si las credenciales de IdP son correctas, el usuario será redirigido al portal del administrador.

Al iniciar sesión en el portal del administrador, el usuario puede hacer clic en **¿Olvidó su contraseña?** para restablecerla. En la siguiente pantalla, el usuario puede introducir una nueva contraseña y el PIN (que se le pedirá en función de la configuración del modo de autenticación de usuario anterior) enviado a la dirección de correo electrónico del usuario. Haga clic en **Reenviar PIN** si fuera necesario. El usuario debe esperar 15 minutos entre solicitudes de contraseña olvidada.

Cuando esta configuración se distribuye a los dispositivos, un intento de inicio de sesión consecutivo sin éxito (valor predeterminado: 5 intentos) por parte de un usuario que utilice una contraseña o un PIN provocará el bloqueo de la cuenta y se mostrará un mensaje al usuario durante el bloqueo.
