---
title: Uso de Microsoft Azure
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM se puede configurar con Microsoft Azure para una inscripción perfecta de los usuarios en sus dispositivos de escritorio de Windows y tabletas con Windows 10. Siga los siguientes pasos para configurar y conectar sus instancias.

Esta sección contiene los siguientes temas:

- [**Configurar una cuenta de Entra ID**](./Uso_de_Microsoft_Azure.md)
- [**Creación de usuarios en Entra ID**](./Uso_de_Microsoft_Azure.md)
- [**Conexión de Entra ID a UEM para dispositivos Windows 10**](./Uso_de_Microsoft_Azure.md)
- [**Compatibilidad con varios usuario para dispositivos de Windows**](./Uso_de_Microsoft_Azure.md)

## Configurar una cuenta de Entra ID

Para configurar Entra ID:

1. Vaya a [**https://azure.microsoft.com/en-in/pricing/purchase-options/**](https://azure.microsoft.com/en-in/pricing/purchase-options/) para comprar su cuenta Azure.
2. Utilice su cuenta de Hotmail o Outlook.com existente o cree una cuenta nueva y regístrese como nuevo usuario.
3. Compre una cuenta Azure mediante alguna de las opciones de pago y siga los pasos de verificación.
4. Pida a Microsoft que incluya en la lista permitida al abonado de Ivanti Neurons for MDM.
5. Utilice la misma cuenta de Hotmail u Outlook.com que utilizó en el paso 2 para iniciar sesión en Entra ID en [**https://manage.windowsazure.com/**](https://manage.windowsazure.com/)[**https://manage.windowsazure.com/**](https://manage.windowsazure.com/) como administrador.
6. Vaya a la pestaña **Dominio**.Se creará un valor predeterminado del dominio, TestMiBGLRoutlook.onmicrosoft.com, para su cuenta y cualquier usuario creado pertenecerá a este dominio. Si fuera necesario, puede volver a crear un dominio personalizado.

## Creación de usuarios en Entra ID

Para crear usuarios en Entra ID:

1. Vaya a Active Directory - > **Directorio predeterminado -> Usuarios**.
2. Seleccione la opción Añadir usuario -> Seleccione Nuevo usuario en su organización.
3. Introduzca que el nombre de usuario. Haga clic en Siguiente **(->)**.Aparece la página **Perfil del usuario**.
4. Añada la información del usuario como su nombre, apellidos y nombre en pantalla.
5. Utilice el menú desplegable para asignar la función adecuada al usuario.
6. Genere la contraseña temporal.Se pedirá al usuario que cambie esta contraseña la primera vez que inicie sesión.

## Conexión de Entra ID a UEM para dispositivos Windows 10

Para conectar Entra ID a UEM:

1. Vaya a **Administración** > **Microsoft Azure > Windows Enrollment And Compliance Using Entra ID**.
2. Complete los pasos de configuración de UEM descritos en la sección, [**Configuración de la gestión del endpoint unificado de Entra ID de Windows 10**](./Configuración_de_la_gestión_del_endpoint_unificado_de_Entra_ID_de_Windows_10.md)
3. Complete la configuración de [**Asignación de la aplicación Entra ID UEM**](./Asignación_de_la_aplicación_Entra_ID_UEM.md) en el portal de Azure.
4. En el Portal de administración Ivanti Neurons for MDM, escriba el nombre de dominio de su cuenta Entra ID y haga clic en Conectar portal Azure y, a continuación, seleccione la casilla de verificación.
5. Después de iniciar sesión correctamente, acepte el consentimiento que permite que la aplicación Validación del abonado de MobileIron AD verifique que su aplicación de UEM en Ivanti Neurons for MDM esté configurada. Aparecerá un mensaje que indica que la conexión es correcta.

### Microsoft Passport for Work para dispositivos Windows 10

Microsoft Passport for Work se reemplaza con Windows Hello para empresas. Para obtener más información, consulte [**Configuración predeterminada de Windows Hello para empresas**](./Configuración_predeterminada_de_Windows_Hello_para_empresas.md).

### Inscripción en Entra ID del dispositivo Windows

**Requisitos previos**

Los usuarios deben registrarse en Ivanti Neurons for MDM.

Conecte su dominio para inscribir al usuario en sus dispositivos Windows 10+.

1. Haga clic en **Unirse a Entra ID**.
2. Introduzca el nombre de usuario y la contraseña.
3. Haga clic en **Iniciar sesión**.
4. Acepte el EULA.
5. Haga clic en **Crear PIN**.\* Si ha habilitado la complejidad del PIN de Microsoft Passport for Work, se le solicitará que configure un PIN complejo de acuerdo con la política configurada.
   - Entra ID autentica al usuario y descarga un JWT (JSON Web Token) al dispositivo.
   - El dispositivo ya está inscrito.
   - Se contactará con el usuario a través del dispositivo para la verificación.
6. Introduzca y confirme el PIN.
7. Haga clic en **Aceptar**.

## Compatibilidad con varios usuario para dispositivos de Windows

Ivanti Neurons for MDM admite capacidades multiusuario para los dispositivos inscritos en Entra ID de Windows 10. Esta función incluyen poder insertar algunos perfiles como de VPN, Wi-Fi, perfiles predeterminados de cliente de correo electrónico y certificados en un usuario individual y no un dispositivo. También admite la distribución de aplicaciones internas y públicas para el usuario que ha iniciado sesión. Cada vez que un nuevo usuario Entra ID se conecta a un dispositivo, Ivanti Neurons for MDM evalúa no solo el dispositivo, sino también al usuario. Si el usuario es nuevo, Ivanti Neurons for MDM actualiza el dispositivo para ese usuario. Si el usuario es un usuario existente en el dispositivo, se evaluará cualquier cambio en el dispositivo y en los ajustes del usuario que tengan que actualizarse desde la última vez que inició sesión.

Los detalles del usuario Entra ID que ha iniciado sesión en el dispositivo se notifican en el portal de administración de Ivanti Neurons for MDM. Cuando el usuario cierra sesión en el dispositivo y el segundo usuario inicia sesión en el dispositivo, los detalles del segundo usuario se actualizan en la página de detalles del dispositivo.

## Usar Microsoft Store para empresas con UEM

Microsoft Store para empresas es un portal proporcionado por Microsoft como parte de Azure. Los administradores pueden acceder a este portal y comprar las aplicaciones y distribuirlas a todos los dispositivos administrados. Ivanti Neurons for MDM se puede configurar con Microsoft Store for Business para administrar aplicaciones desde el portal de administración de Ivanti Neurons for MDM mediante la configuración de los pasos siguientes.    

### Paso 1: Registro de la aplicación Entra ID en el Portal de Microsoft Azure

1. Abra el primer navegador e inicie sesión en el portal de Microsoft Azure ([**https://portal.azure.com/**](https://portal.azure.com/)[**https://portal.azure.com/**](https://portal.azure.com/)).
2. Haga clic en **Registros de aplicaciones** en el panel izquierdo.
3. Haga clic en **+Registro de nueva aplicación**.
4. Introduzca la siguiente información para registrar MobileIron como aplicación de Azure:\* **Nombre:** escriba un nombre para la aplicación de MobileIron. (Este campo debe tener al menos 4 caracteres).
   - **Tipo de aplicación:** seleccione Aplicación web/API.
   - **URL de inicio de sesión:** introduzca la URL a la que acceden los usuarios de los dispositivos para iniciar sesión en MobileIron (obligatorio).
5. Haga clic en **Crear** para añadir la aplicación y volver a la página de inicio de Azure.
6. Vaya a Ajustes y cree una nueva clave.

### Paso 2: Añadir la aplicación como herramienta de administración

1. En los ajustes de Microsoft Store para empresas, haga clic en Administrar
2. ajustes de distribución.
3. En la herramienta Añadir administración, active la aplicación creada.

### Conexión de la cuenta en el Portal de administración

1. Vaya a **Administrador > Microsoft Azure > Microsoft Store para empresas**.
2. En el paso 1, **Registrar la aplicación Entra ID**, seleccione la casilla **Sí, he completado este paso**.
3. En el Paso 2, **Añadir herramienta de administración**, seleccione la casilla **Sí, completé este paso**.
4. En el Paso 3, Conexión de la cuenta, actualice los siguientes campos:\* Dominio de Entra ID
   - Identificador de la aplicación
   - Clave de la aplicación
   - Intervalo de sincronización (horas)
5. Haga clic en **Conectar**. Verá un mensaje que confirma que la tienda de MobileIron para empresas se ha configurado correctamente.
6. Haga clic en **Sincronizar aplicación**. Cuando se sincroniza correctamente, el estado se muestra como **Aplicaciones sincronizadas correctamente**.

Cuando la Microsoft Store para aplicaciones se envía al dispositivo, los detalles de la aplicación están disponibles en la pestaña **Aplicaciones instaladas** en los detalles del dispositivo. Cada aplicación de Microsoft Store para empresas notificada desde el dispositivo, puede identificarse como **Microsoft Store para empresas** en la columna **Origen**.
