---
title: Inscripción de usuarios en el Apple Business Manager
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Requisitos para habilitar la inscripción de usuarios**](./Inscripción_de_usuarios_en_el_Apple_Business_Manager.md)
- [**Prioridad de los registros**](./Inscripción_de_usuarios_en_el_Apple_Business_Manager.md)
- [**Diferencia entre la inscripción de MDM estándar y la Inscripción de usuarios**](./Inscripción_de_usuarios_en_el_Apple_Business_Manager.md)
- [**Diferencia entre la Inscripción de usuarios y la Inscripción de dispositivos**](./Inscripción_de_usuarios_en_el_Apple_Business_Manager.md)
- [**Conectar Ivanti Neurons for MDM con Apple Business Manager**](./Inscripción_de_usuarios_en_el_Apple_Business_Manager.md)

**Disponible para**:

- Los dispositivos no supervisados con iOS 13.0 hasta la última versión admitida por Ivanti Neurons for MDM.
- Dispositivos con macOS 10.15 o versiones más recientes compatibles Ivanti Neurons for MDM.

Apple Business Manager es un lugar donde los equipos informáticos automatizan la implementación de dispositivos, compran y distribuyen contenido y gestionan las funciones en sus organizaciones. Apple Business Manager implementa la Inscripción de Usuarios; una opción de inscripción diseñada para las empresas que quieren pasarse al modelo «BYOD» (Bring Your Own Device). La Inscripción de usuarios es una versión modificada del protocolo MDM con un enfoque mucho mayor en la privacidad del usuario, implementada con el nivel de seguridad que las empresas necesitan.

Inscripción de usuarios permite a los administradores hacer lo siguiente:

- Instalar y desinstalar aplicaciones administradas
- Instalar y desinstalar las configuraciones de red
- Instalar una VPN parcial con alcance para las aplicaciones y cuentas administradas
- Requerir el uso de una contraseña

## Requisitos para habilitar la inscripción de usuarios

A continuación figuran los requisitos para permitir la inscripción de usuarios. Si alguna de estas no se cumple, el tipo de inscripción será «inscrito en el dispositivo».

- Un dispositivo no supervisado con iOS 13.0 hasta la última versión compatible con Ivanti Neurons for MDM o un dispositivo con macOS 10.15 o versiones más recientes compatibles Ivanti Neurons for MDM.
- El ajuste del usuario para el campo Tipo de inscripción de Apple debe establecerse como «Inscripción de usuarios».
- Una cuenta de Apple Business Manager.
  - La cuenta de licencia de aplicaciones de Apple debe ser parte de la misma cuenta de Apple Business Manager.
  - Dentro de Apple Business Manager, si tiene un cuenta en Ubicaciones, debe tener Apps y Books que coincida con la misma ubicación. Puede que deba añadir una nueva ubicación (p. ej.: Costa Oeste).
    ID de Apple administrada: la ID de Apple administrada que se asociará a cada dispositivo inscrito.
  - Esta ID de Apple administrada proporciona autenticación para la gestión y licencias de MDM.
  - Cuando la MDM rechaza aplicaciones y medios, las licencias de Apple necesarias se asignan a la ID de Apple administrada asociada al dispositivo.
  - Como parte del cumplimiento con el RGPD, las ID de Apple administradas ahora se enmascaran en la lista de usuarios y en las páginas de detalles de usuario considerando el ID de Apple como los datos de usuario.
  - Las ID de Apple administradas las usó por primera vez Apple School Manager y ahora las usa Apple Business Manager para la inscripción de usuarios.
    El ID de Apple administrada del dispositivo y el token de ubicación de Apps and Books deben ser de la misma organización de la cuenta de Apple Business Manager.
    Si son diferentes, se muestra una notificación en el Portal de Administración de Ivanti Neurons for MDM cuando se produce un error en la asignación de licencia para una aplicación.
    Microsoft Entra ID configurado para autenticación federada o un ID de Apple creado manualmente en Apple Business Manager con un dominio validado.
  - Para obtener instrucciones sobre el uso de la Autenticación federada, consulte la [**Guía del usuario de Apple Business Manager**](https://business.apple.com/) en el sitio web de Apple. Es necesario iniciar sesión.
    Los usuarios de dispositivos que estén sincronizados con LDAP deben asignarse a una función de administración de dispositivos y asociarse a una ID de Apple administrada.

En la página de la lista [**Usuarios**](./Usuarios.md) y en la página de la lista [**Dispositivos**](./Dispositivos.md), se puede agregar la columna ID de Apple administrada para que se muestre a todos los usuarios. En la página de la lista [**Dispositivos**](./Dispositivos.md), puede agregar la columna Inscripción de usuarios inscritos para mostrar el estado de los dispositivos con Inscripción de usuarios. Además, las exportaciones de usuarios y dispositivos incluyen estas columnas en los archivos CSV.

## Prioridad de los registros

- La inscripción de usuarios se admite a través del cliente Go para iOS e iReg. Apple ya no admite la inscripción de usuarios a través de Ivanti Go para iOS e iReg. [**Inscripción de usuario basada en cuenta**](<Account driven User Enrollment.htm>) solo está disponible en la cuenta profesional o educativa del dispositivo.
- La Inscripción de dispositivos automatizada y Apple Configurator siempre estarán inscritos en el dispositivo.
- Si se aplica la configuración MAM a un dispositivo, el registro MAM tiene prioridad sobre la Inscripción de usuarios.
- Si se cumplen tanto los requisitos de auth-only como de Inscripción de usuarios, la Inscripción de usuarios tiene prioridad.
- Si usted vuelve a inscribir un dispositivo desde Go para el cliente iOS, el tipo de inscripción será la misma que el tipo del registro del dispositivo, independientemente del cambio en el tipo de inscripción de Ivanti Neurons for MDM. Por ejemplo, si se inscribió un dispositivo por el usuario, cambie el tipo a Inscripción de dispositivos en Ivanti Neurons for MDM y vuelva a inscribir el dispositivo desde el cliente Go. El dispositivo seguirá estando inscrito por el usuario y no por el dispositivo.

## Diferencia entre la inscripción de MDM estándar y la Inscripción de usuarios

En esta sección se explica la diferencia entre la inscripción estándar de MDM y la inscripción de usuarios en el Apple Business Manager.

### Inscripción de MDM estánda

La siguiente lista indica lo que un servidor Ivanti Neurons for MDM puede hacer en una inscripción estándar de MDM, pero no podrá hacer en el modo Inscripción de usuarios.

El servidor MDM:

- No puede borrar el dispositivo.
- No ve las aplicaciones personales que el usuario del dispositivo ha instalado en el mismo.
- No puede convertir las aplicaciones instaladas por el usuario en aplicaciones gestionadas por MDM.
- No es posible borrar la clave de acceso del dispositivo (por ej. desbloquear el dispositivo).
- No puede establecer un largo y complejo requisito de código de acceso al dispositivo.
- No puede configurar un dispositivo VPN o proxy Wi-Fi, ni puede hacer ninguna gestión de la funcionalidad móvil.
- No puede ver los identificadores del dispositivo como el UDID, el número de serie o el IMEI.
- No puede aplicar muchas restricciones en todo el dispositivo (como la restricción de la clasificación del contenido de la aplicación), bloquear iCloud y aplicar cualquiera de las restricciones supervisadas.

### Inscripción de usuarios en el Apple Business Manager

En la Inscripción de usuarios, el servidor MDM puede hacer todo lo necesario para administrar las aplicaciones, cuentas y datos de la empresa.

Con la Inscripción de usuarios se puede:

- Instalar aplicaciones internas o aplicaciones a través de licencias de Apps and Books del usuario (Apple).
  - Las licencias se aplican por orden de llegada y las consumen las ID de Apple administradas.
  - La licencia consumida por una aplicación instalada en un dispositivo con Inscripción de usuarios será diferente de la licencia consumida por la misma aplicación instalada en el dispositivo con inscripción de dispositivos.
  - Compruebe el tipo de licencia para las aplicaciones de Apple Apps y Books en una página de detalles del usuario a través de la pestaña Uso de licencia; se mostrará el Tipo de inscripción como Inscripción de usuario o Inscripción de dispositivo.
    Aplicar los ajustes de la carga útil del código de acceso. Por ejemplo,
  - allowSimple = false
  - forcePIN = true
  - minLength = 6
    Consultar datos relacionados con aplicaciones, certificados y perfiles gestionados por la empresa.
- Configurar una VPN por aplicación para aplicaciones, correo, contactos y calendarios que han sido instalados por MDM.
- Aplicar algunas restricciones, como «abrir en» administrado, contactos administrados, datos administrados en la pantalla de bloqueo y otras tantas.

Los datos de la empresa se almacenan en un volumen separado del Sistema de Archivos de Apple (APFS), que se crea en el momento de la inscripción, y se codifica por separado de los datos de usuario del dispositivo. Este volumen contiene datos almacenados por aplicaciones gestionadas; notas de la empresa; documentos de la unidad iCloud Drive de la empresa; entradas del Llavero de la empresa; adjuntos y cuerpos de correo gestionados y adjuntos del calendario. Anular la incripción de MDM destruye el volumen y las claves.

Todas las aplicaciones de terceros solo pueden ser aplicaciones personales o aplicaciones administradas a través de Ivanti Neurons for MDM. El servicio MDM no puede empezar a administrar aplicaciones que el usuario del dispositivo ya ha instalado. En este caso, el administrador deberá solicitar al usuario del dispositivo que elimine la aplicación personal antes de instalar la aplicación a través de MDM. El servicio MDM no puede empezar a administrar aplicaciones que el usuario ya ha instalado. Sin embargo, algunas aplicaciones de sistema como Notas y Archivos serán compatibles tanto con las cuentas de trabajo como con las personales.

### Inscripción de usuarios para dispositivos macOS

La inscripción del usuario es compatible con dispositivos con macOS 10.15 o versiones más recientes compatibles Ivanti Neurons for MDM.

- Mobile\@Work para macOS no es compatible con los dispositivos inscritos en la Inscripción de usuarios de macOS.
  - Incluso si la aplicación se distribuye al dispositivo con Inscripción de usuarios de macOS, la aplicación no se insertará al dispositivo desde MDM.
  - Por lo tanto, las funciones de Mobile\@Work, como la administración de secuencias de comandos y la gestión de aplicaciones para las aplicaciones de Packager (MIP) no son compatibles con los dispositivos inscritos en la Inscripción de usuarios de macOS.
    Dependencia de las aplicaciones y cambios de comportamiento en los dispositivos macOS con Inscripción de usuarios.
  - En los dispositivos macOS con Inscripción de usuarios, la dependencia de las aplicaciones funciona en base al mejor esfuerzo, ya que la MDM no conoce (no puede confirmar) el estado de la instalación de las aplicaciones con requisitos previos antes de distribuir la aplicación principal.
  - Las aplicaciones y configuraciones se pueden distribuir a los usuarios y grupos de usuarios que pertenezcan a los dispositivos macOS con Inscripción de usuarios. Sin embargo, las aplicaciones siempre muestran el botón **Instalar** en lugar de «Instalado» porque la MDM no puede mostrar el estado de la instalación de las aplicaciones en los dispositivos macOS inscritos en la Inscripción de usuarios.
  - Las aplicaciones instaladas se indican como Aplicaciones solicitadas en la página **Dispositivos > Inventario de aplicaciones**, ya que los dispositivos macOS inscritos en la Inscripción de usuarios no notifican al servidor Ivanti Neurons for MDM si las aplicaciones están instaladas o no en el informe del inventario.
    En el filtro de distribución para las aplicaciones, los atributos Inscrito en la Inscripción de dispositivos e Inscrito en la Inscripción de dispositivos automatizada se pueden utilizar para la distribución personalizada, según sea necesario.
- Las licencias basadas en el usuario se admiten mediante ID de Apple administradas para instalar aplicaciones de Apple Apps y Books. No se permiten las licencias basadas en dispositivos. El catálogo de aplicaciones solo muestra las aplicaciones de Apple Apps y Books.
- No todas las configuraciones, políticas y acciones están permitidas. Véase la lista completa de las configuraciones y políticas que figuran a continuación de este procedimiento.
  - Si se distribuyen configuraciones no admitidas a un dispositivo macOS inscrito en la Inscripción de usuarios, no se distribuirán ni se aplicarán al dispositivo y pueden mostrar un mensaje como «Restricciones - este no es un tipo de solicitud válida».
  - Del mismo modo, las acciones de los dispositivos de administración no admitidas se informarán en la IU de Ivanti Neurons for MDM.
  - Los informes no admitidos no los enviará Ivanti Neurons for MDM.

A continuación se indican las configuraciones y políticas no admitidas para ser distribuidas a los dispositivos macOS inscritos en la Inscripción de usuarios:

- Código de acceso
- Túnel
- Tunnel (a petición)
- Configuraciones de VPN
- Creación automática de cuentas en Office 365
- Política de extensiones del kernel de macOS
- Preferencia de privacidad
- Restricciones de macOS
- Actualizaciones de software
- AirPrint
- Privacidad del cliente de MI
- FileVault 2
- Clave de recuperación de FileVault
- Cortafuegos
- Regla de políticas del sistema
- Preferencia de certificado
- Control de políticas del sistema
- Políticas del sistema administradas
- Restricciones de la AppStore de macOS
- Restricciones de grabación en disco de macOS
- Ajustes del Finder de macOS
- Mobile\@Work para macOS
- Mobile\@Work para secuencias de comandos de macOS
- Control multimedia permitido
- Servidor de zona horaria
- Política de aplicaciones permitidas

## Diferencia entre la Inscripción de usuarios y la Inscripción de dispositivos

En esta sección se explica la diferencia entre la Inscripción de usuarios y la Inscripción de dispositivos.

La Inscripción de usuarios se aplica a los dispositivos con iOS 13.0 y macOS 10.15 hasta la última versión compatible. Los dispositivos anteriores a iOS 13.0 y macOS 10.15 se considerarán con «inscripción de dispositivos» independientemente de si el usuario del dispositivo ha sido habilitado para la Inscripción de usuarios o no.

La inscripción de usuarios para Apple Business Manager no permite borrar o desbloquear. Sin embargo, el portal del usuario seguirá teniendo esas opciones disponibles aunque no funcionen.

| Inscripción de usuarios comparada con la Inscripción de dispositivos                                                                                      |                                 |                                                                      |                                                                                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Funcionalidad                                                                                                                                             | Inscripción de usuarios         | Mobile Application Management (Gestión de Aplicaciones Móviles, MAM) | Inscripción de dispositivos                                                                                                                                               |
| Borrar el dispositivo y ver las aplicaciones personales del usuario                                                                                       | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)                                          | ![](Resources/Images/Check.svg)                                                                                                                                           |
| Convertir de administrado a no administrado o viceversa                                                                                                   | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)                                          | ![](Resources/Images/Check.svg)                                                                                                                                           |
| Borrar el código de acceso del dispositivo, configurar una VPN en todo el dispositivo o el proxy Wi-Fi o gestionar la funcionalidad móvil                 | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)                                          | ![](Resources/Images/Check.svg)                                                                                                                                           |
| Ver los identificadores del dispositivo como el número de serie, IMEI                                                                                     | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)                                          | ![](Resources/Images/Check.svg)                                                                                                                                           |
| Aplicar restricciones supervisadas                                                                                                                        | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)                                          | :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/9MGkOZSM7OxFYFPjee254_check.svg" alt caption}(Solo dispositivos supervisados) |
| Puede instalar y configurar aplicaciones y cuentas                                                                                                        | ![](Resources/Images/Check.svg) | ![](Resources/Images/Check.svg)                                      | ![](Resources/Images/Check.svg)                                                                                                                                           |
| Puede configurar una VPN por aplicación, correo, contactos y calendarios que se hayan instalado por MDM                                                   | ![](Resources/Images/Check.svg) | ![](Resources/Images/X.svg)                                          | ![](Resources/Images/Check.svg)                                                                                                                                           |
| Puede aplicar algunas restricciones, como «abrir en» administrado, contactos administrados, datos administrados en la pantalla de bloqueo y otras tantas. | ![](Resources/Images/Check.svg) | ![](Resources/Images/X.svg)                                          | ![](Resources/Images/Check.svg)                                                                                                                                           |
| Puede consultar datos relacionados con aplicaciones, certificados y perfiles gestionados por la empresa.                                                  | ![](Resources/Images/Check.svg) | ![](Resources/Images/X.svg)                                          | ![](Resources/Images/Check.svg)                                                                                                                                           |

## Conectar Ivanti Neurons for MDM con Apple Business Manager

En esta sección se describe cómo activar la Inscripción de usuarios para Apple Business Manager.

**Requisitos previos**

- Debe tener una cuenta de Apple Business Manager. Véase [**https://business.apple.com/**](https://business.apple.com/).
- Debe solicitar e instalar un [**certificado MDM**](./Instalación_del_Certificado_MDM.md) de Apple para administrar los dispositivos iOS.

### Creación de usuarios locales para permitir la Inscripción de usuarios

En esta sección se explica la creación de usuarios locales y LDAP y la configuración de la Inscripción de usuarios para los dispositivos de Apple sin supervisión. La Inscripción de usuarios no funcionará en dispositivos supervisados o en dispositivos inscritos en la Inscripción de dispositivos de Apple.

### Crear un grupo de usuarios administrado manualmente (estático)

Este es un procedimiento de una sola vez. Si ya ha creado este grupo, pase a la sección «Crear usuarios para la Inscripción de usuarios».

**Procedimiento**

1. Vaya a Usuario&#x73;**>**[**Grupos de usuarios**](./Grupos_de_usuarios.md).
2. Cree un grupo de usuarios (estático) administrado manualmente, como el Grupo de Inscripción de usuarios, para añadir usuarios con el tipo de registro del dispositivo como Inscripción de usuarios.
3. Haga clic en **Guardar**.

### Crear un ajuste de tipo de registro de dispositivos

Este es un procedimiento de una sola vez. Si ya ha creado este grupo, pase a la sección «Crear usuarios para la Inscripción de usuarios». Para los dispositivos inscritos en la inscripción de usuarios, la configuración predeterminada del Propietario del dispositivo será «Propiedad del usuario».

**Procedimiento**

1. Vaya a **Usuarios >&#x20;**[**Ajustes del usuario**](./Ajustes_del_usuario.md).
2. En la sección Ajuste del registro de dispositivos, haga clic en el ajuste **+ Añadir para grupos de usuarios específicos**.
3. Cree un nuevo ajuste, como el Registro IU, para los usuarios con el tipo de registro del dispositivo como Inscripción de usuarios.
4. En la sección Inscripción de Apple, seleccione **Inscripción de usuarios** como el Tipo de inscripción de Apple.
5. Haga clic en **Siguiente**.
6. En la página Distribución de ajustes del usuario, seleccione el grupo de usuarios recién creado, como el Grupo de Inscripción de usuarios.
7. Haga clic en **Hecho**.

### Crear un usuario local para la Inscripción de usuarios

Como requisito previo, cree un grupo de usuarios administrado manualmente y un ajuste de registro de dispositivos para la Inscripción de usuarios.

**Procedimiento**

1. Vaya a [**Usuarios**](./Usuarios.md).
2. Haga clic en + **Añadir** > **Un solo usuario**.
   Introduzca la nueva información de usuario y añádala al grupo de usuarios recién creado, como el Grupo de Inscripción de usuarios. Para más información, consulte *Agregar un usuario* en el tema [**Usuarios**](./Usuarios.md) .

### Importación de usuarios LDAP para habilitar la Inscripción de usuarios

**Requisitos previos**

- Como requisito previo, establezca un conector Ivanti Neurons for MDM para acceder a los recursos de [**LDAP**](./Configuración_del_servidor_LDAP.md).
- Asegúrese de que el ajuste **ID administrador de Apple** está establecido en **Patrón** (dirección de correo electrónico del usuario). Asegúrese de que el patrón de la ID de Apple administrada sea único. De lo contrario, la cuenta no se actualizará con la ID de Apple administrada si ya existe la misma ID de Apple administrada en otra cuenta.
- (Opcional), incluir el subdominio "appleid" para evitar conflictos con los ID de Apple existentes.
- Puede importar usuarios desde LDAP e invitarlos a la Inscripción de usuarios. Los usuarios de LDAP importados tendrán sus ID de Apple administradas sincronizadas con Ivanti Neurons for MDM, lo cual es un requisito para la inscripción de usuarios.

**Procedimiento**

1. Vaya a **Usuarios.**
2. Haga clic en **+Añadir > Invitar a usuarios de LDAP.**
3. Haga clic en **Seleccionar usuarios** en la entrada del servidor LDAP.
4. En la página Añadir usuarios de LDAP, introduzca el nombre del usuario, grupo u OU en el campo de búsqueda.
5. Para añadir nuevos usuarios o grupos, haga clic en **+Añadir** junto a la entrada que desee añadir.
6. Haga clic en **Hecho**.

### Importación de usuarios de Entra ID para habilitar la Inscripción de usuarios

Como requisito previo, conecte Ivanti Neurons for MDM con Microsoft Entra ID (Entra ID).

Puede invitar a usuarios de Entra ID para la Inscripción de Usuarios. Los usuarios de Entra ID importados tendrán sus ID de Apple administradas sincronizadas con Ivanti Neurons for MDM, lo cual es un requisito para la inscripción de usuarios.

Procedimiento

1. Vaya a **Administrador >&#x20;**[**Fuente de usuario de Entra ID**](./Conecte_Ivanti_Neurons_for_MDM_con_Entra_ID_User_Source.md).
2. Edite los ajustes.
3. Seleccione **Activar este Entra ID**.
4. En el ajuste de ID administrada de Apple, seleccione una o más de la siguientes opciones:\* **Patrón**- **Dirección de correo electrónico del usuario**: asegúrese de que el patrón de la ID de Apple administrada sea único. De lo contrario, la cuenta no se actualizará con la ID de Apple administrada si ya existe la misma ID de Apple administrada en otra cuenta.
   - Como alternativa, seleccione **userUPN**.
5. (Opcional), incluir el subdominio "appleid" para evitar conflictos con los ID de Apple existentes.
6. Seleccione **Invitar automáticamente a los usuarios importados desde Entra ID**. A los usuarios importados desde Entra ID a Ivanti Neurons for MDM se les invita automáticamente a registrarse por correo electrónico.
7. Haga clic en **Guardar**.

### Instrucciones del usuario del dispositivo para registrarse mediante la inscripción de usuarios

En esta sección se describen las acciones que el usuario del dispositivo debe realizar para registrar la Inscripción de usuarios de Apple.

**Procedimiento**

1. En el dispositivo iOS que desee registrar, abra el correo electrónico de invitación que contiene el enlace y un texto que guía al usuario final a un enlace de registro como mobileiron.com/go.
2. Abre el enlace de registro en Safari.
3. Aparecerá la página de inicio de sesión. El usuario del dispositivo debe iniciar la sesión con sus credenciales de usuario local o LDAP.
   Aparecerá la página de registro aparece con un mensaje que dice que ya se descargó el perfil.
   Pulse Ajustes. Aparecerá la página Ajustes.
4. Pulse Inscribirse en \[nombre de su empresa].
5. Aparecerá la página Inscripción del usuario.
6. Pulse Inscribir mi \[Su dispositivo]. Por ejemplo, pulse Inscribir mi iPhone.
   Si pulsa Cancelar y eliminar perfil, tendrá que empezar de nuevo el proceso de registro.
   Se le presentará un inicio de sesión para la cuenta de Apple o su cuenta Federada. Introduzca la contraseña de su ID de Apple administrada. (La ID de Apple administrada aparecerá en la parte superior de su página de inicio de sesión).
   Puede que se le presente la opción de seguir con la sesión iniciada, haga una selección.
   Una página mostrará el mensaje «Inscripción correcta».

### Uso de registros de dispositivos para la resolución de problemas

Para solucionar los errores o problemas de un dispositivo con Inscripción de usuarios, comience por revisar los registros del dispositivo.

**Procedimiento**

1. Vaya a Dispositivos.
2. Haga clic en el dispositivo para visualizar la página de detalles del dispositivo. Puede verificar los campos Inscrito en la inscripción de usuarios e ID de Apple administrada registrado.
3. Seleccione la pestaña Registros.
4. En la región Filtros, limite los registros del dispositivo utilizando filtros basados en nombres de acciones (como Finalizar la compra, Nombre del dispositivo, Definir token de arranque, Obtener token de arranque, etc.), estado, fecha de inicio y fecha de fin.
5. En la columna Acciones, haga clic en el icono del ojo para mostrar los detalles del registro del dispositivo, como la ID de inscripción.
6. Haga clic en **Aceptar**.
