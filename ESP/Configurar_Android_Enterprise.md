---
title: Configurar Android Enterprise
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene el siguiente tema:

- [**Dispositivos compatibles**](./Configurar_Android_Enterprise.md)
- [**Conectar Ivanti Neurons for MDM con Android Enterprise**](./Configurar_Android_Enterprise.md)
- [**Obtener sus credenciales de Android Enterprise**](./Configurar_Android_Enterprise.md)
- [**Añadir su token de MDM de Android Enterprise a Ivanti Neurons for MDM**](./Configurar_Android_Enterprise.md)
- [**Sincronización de usuario entre Ivanti Neurons for MDM y Google**](./Configurar_Android_Enterprise.md)
- [**Usuarios de Active Directory/LDAP**](./Configurar_Android_Enterprise.md)
- [**Usuarios locales**](./Configurar_Android_Enterprise.md)
- [**Despliegue de Android Enterprise en dispositivos compatibles**](./Configurar_Android_Enterprise.md)
- [**Eliminar los dispositivos registrados**](./Configurar_Android_Enterprise.md)
- [**Instalar el dispositivo**](./Configurar_Android_Enterprise.md)
- [**Confirmar la instalación**](./Configurar_Android_Enterprise.md)
- [**Instalar las aplicaciones Android Enterprise**](./Configurar_Android_Enterprise.md)
- [**Configuración de Aplicaciones corporativas**](./Configurar_Android_Enterprise.md)

**Licencia**: Silver

Android Enterprise es un programa que ofrece Google y que permite a los administradores de movilidad:

- Separar los datos profesionales y personales
- Asegurar y administrar aplicaciones corporativas
- Controlar aplicaciones del sistema (como la Cámara y Galería)
- Aprovisione centralmente y configure las aplicaciones del contenedor de Android Enterprise
- Evitar pérdida de datos (captura de pantalla)

Puede configurar Ivanti Neurons for MDM como el servidor de UEM que administra Android Enterprise. Android Enterprise requiere al menos Android 3.0. Hay dos configuraciones compatibles para Android Enterprise: Propietario del dispositivo y Perfil administrado: perteneciente a un empleado.

## Dispositivos compatibles

Ivanti Neurons for MDM actualmente, es compatible con Android Enterprise solo en dispositivos que utilicen Android 5.0 y en los que el fabricante haya habilitado Android Enterprise. Android Enterprise es necesario para el modo kiosko en los dispositivos con Android 5.0.

**Requisito previo**

Si todavía no ha registrado su dominio con Google, primero debe inscribirse en el programa en el sitio web de Google:

[**https://admin.google.com.**](https://admin.google.com/)

Durante este proceso, usted:

- Reclamará un dominio (debe coincidir con el dominio para las direcciones de correo electrónico del usuario)
- Recibirá un token
- Descargará una Id. de cliente JSON

Ambos elementos son necesarios cuando se ajusta Android Enterprise en Ivanti Neurons for MDM.

Tras el proceso, recibirá un correo electrónico con instrucciones para verificar que el dominio que ha reclamado es suyo.

**Si la empresa ya ha usado este nombre de dominio** para registrarse en Google Apps for Work, consulte [**https://support.google.com/work/android/answer/6174062**](https://support.google.com/work/android/answer/6174062) para obtener información sobre cómo habilitar Android Enterprise.

## Conectar Ivanti Neurons for MDM con Android Enterprise

Una vez haya iniciado sesión en Android Enterprise, ajuste Ivanti Neurons for MDM como servidor UEM.

## Obtener sus credenciales de Android Enterprise

**Procedimiento**

1. Vaya a **Administrador > Android Enterprise**.
2. Haga clic en **Consola de Google Developers**.
3. Haga clic en el primer enlace que aparezca para ir hasta la consola de Google Developers.
4. Seleccione **Crear un proyecto** del menú desplegable.
5. Introduzca un nombre para el proyecto.
6. Acepte los términos de servicio.
7. Haga clic en **Crear**.
8. Haga clic en **API**.
9. Seleccione las **API**.
10. Escriba **emm** en el campo de búsqueda para encontrar la EMM de Google Play.
11. Haga clic en el enlace de la **API de EMM de Google Play** .
12. Haga clic en **Habilitar API**.
13. Haga clic en **Credenciales**.
14. Seleccione **Cuenta de servicio** el.
15. Haga clic en **Crear** para guardar el archivo JSON.

## Añadir su token de MDM de Android Enterprise a Ivanti Neurons for MDM

**Procedimiento**

1. Inicie sesión en [**https://admin.google.com**](https://admin.google.com/).
2. Haga clic en **Seguridad**.
3. Si no ve los Ajustes de Android Enterprise, haga clic en **Mostrar más**.
4. Seleccione **Ajustes de Android Enterprise**.
5. En **Administrar el proveedor de administración de movilidad empresarial**, copie el token de MDM.
6. Volver al portal de Ivanti Neurons for MDM.
7. Haga clic en **Listo**.
8. En el cuadro 2, pegue el token de MDM que acaba de copiar.
9. En el campo **Dominio**, ingrese el dominio que le reclamó a Google.
10. Haga clic en **Elegir archivo** y cargue el archivo JSON que descargó.
11. Haga clic en **Conectar**.Aparece el mensaje **Conectado a Google** cuando se logra la conexión correcta.
12. En la caja 3, haga clic en **Autorizar** para indicar que desea dar acceso a Ivanti Neurons for MDM a sus datos de usuario de Google.
13. Haga clic en **Aceptar**.Se muestra el mensaje **Conectado a usuarios** en el portal de Ivanti Neurons for MDM.

## Sincronización de usuario entre Ivanti Neurons for MDM y Google

Antes de desplegar Android Enterprise en los usuarios de Android que se administran en Ivanti Neurons for MDMIvanti Neurons for MDM, cada usuario debe tener un registro correspondiente en el Portal de administración de Google. Los pasos necesarios para sincronizar la información del usuario entre Ivanti Neurons for MDM y el portal de administración de Google dependen de que haya ajustado una integración con los servicios del directorio de su empresa (AD/LDAP).

## Usuarios de Active Directory/LDAP

Si tiene configurada una integración AD/LDAP con Ivanti Neurons for MDM, debe usar la sincronización del directorio de aplicaciones de Google para configurar una integración de AD/LDAP con el portal administrativo de Google. Consulte [**https://support.google.com/a/answer/106368?hl=en**](https://support.google.com/a/answer/106368?hl=en) para obtener más información.

## Usuarios locales

Si ha creado usuarios solo locales en Ivanti Neurons for MDM y no pretende integrarlo con un servicio de directorio, complete los pasos siguientes para sincronizar esos usuario con el portal administrativo de Google.

**Procedimiento**

1. Inicie sesión en el portal de administración de Google en [**https://admin.google.com**](https://admin.google.com/).
2. Haga clic en **Usuarios**.
3. Haga clic en el icono **Añadir usuario** o **Añadir varios usuarios** situado en la esquina inferior derecha.
4. Para cada usuario de Ivanti Neurons for MDM que utilizará Android Enterprise, agregue un usuario de Google con el mismo nombre de usuario y dirección de correo electrónico que el usuario de Ivanti Neurons for MDM.
5. En el portal de Ivanti Neurons for MDM por cada usuario de Ivanti Neurons for MDM que se agregó al portal de administración de Google\:a. Haga clic en el enlace del nombre del usuario de la pestaña Usuarios para mostrar la página de detalles del usuario.b. Seleccione **Sincronizar el usuario con el directorio de usuarios de Google.**&#x63;. Haga clic en **Sincronizar con el directorio de usuarios de Google**.d. Confirme que Google Status está listado como Habilitado.

## Despliegue de Android Enterprise en dispositivos compatibles

Son necesarias dos configuraciones para desplegar Android Enterprise:

- Android Enterprise: la configuración de un perfil de trabajo en un dispositivo de la empresa activa Android Enterprise.
- Una configuración de Bloqueo y Kiosko define las restricciones de Android Enterprise que se van a aplicar.

## Eliminar los dispositivos registrados

En escenarios de BYOD, trasladar de un perfil de Administrador de dispositivos a uno profesional de Android Enterprise en un dispositivo propiedad de la empresa no requiere que se retiren y se vuelvan a inscribir los dispositivos. El borrado o retirada del dispositivo solo son necesarios para pasar del modo Administrador del dispositivo al de Propietario del dispositivo.

Cuando se selecciona un dispositivo inscrito en modos Propietario del dispositivo / Propietario de perfil mejorado / Propiedad de la empresa activados de manera personal para la acción Retirar, aparece una ventana emergente en la pantalla que indica que "El comando Retirar no es compatible con los dispositivos que son propiedad de la empresa".

## Instalar el dispositivo

**Procedimiento**

1. En el portal de Ivanti Neurons for MDM, vaya a **Configuraciones**.
2. Haga clic en **Android Enterprise: perfil de trabajo**.
3. Haga clic en **Editar**.
4. Haga clic en **Siguiente**.
5. Seleccione **Todos los dispositivos** o **Personalizado**.
6. Si seleccionó **Personalizado**, busque y seleccione los grupos de dispositivos que deberían recibir los ajustes de Android for Work.
7. Haga clic en **Listo**.
8. Haga clic en **Volver a la lista** (esquina superior izquierda).
9. Haga clic en **+Agregar**.
10. Haga clic en **Bloqueo y kiosko: Android Enterprise**.
11. En el campo **Nombre**, ingrese el texto que identifica la configuración.
12. En **Elegir tipo de bloqueo**, seleccione **Perfil de trabajo**.
13. Seleccione los ajustes de bloqueo que desee aplicar a los dispositivos de destino.
14. Haga clic en **Siguiente**.
15. Seleccione **Todos los dispositivos** o **Personalizado**.
16. Si seleccionó Personalizado, busque y seleccione los grupos de dispositivos que deberían recibir los ajustes de Android Enterprise.
17. Haga clic en **Listo**.

No se pueden realizar cambios en el perfil resultante una vez que haya sido implementado. En lugar de esto, debe crear una nueva configuración de Android Enterprise y desplegarla.

## Confirmar la instalación

Puede confirmar que Android Enterprise se ha desplegado de las maneras siguientes:

- En **Usuarios > Usuarios**, encuentre la entrada para un usuario determinado y, a continuación, compruebe que el **Estado de Google** esté **Habilitado**.
- En **Dispositivos > Dispositivos,** haga clic en el enlace de un dispositivo, y a continuación compruebe que el estado de **Android Enterprise** es **Habilitado**.

El **Estado de Google** del usuario debe aparecer como **Habilitado**. Si no está Habilitado, el usuario no podrá registrar los dispositivos.

Para empresas que no estén suscritas a GSuite, el método de Cuentas de Google Play administradas permite a los usuarios inscribirse con Android Enterprise. Si Android Enterprise se configuró como Cuentas de Google Play administradas, el usuario no se mostrará como **Estado de Google: Habilitado** hasta que se haya registrado el dispositivo de Android Enterprise. Consulte [**Cuentas de Google Play administradas**](./Cuentas_administradas_de_Google_Play__cuentas_con_Android_Enterprise_.md) para obtener más información sobre las cuentas de Google Play administradas.

## Instalar las aplicaciones Android Enterprise

Cualquier aplicación desarrollada para Android Enterprise puede incluir las opciones que puede configurar a través de Ivanti Neurons for MDM.

**Procedimiento**

1. En el portal de Ivanti Neurons for MDM, vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Encuentre la aplicación en la Google Play Store.
3. Haga clic en la entrada de la aplicación.
4. Acepte los permisos en nombre de los usuarios de Android Enterprise.
5. Haga clic en **Siguiente**.
6. Seleccione una opción de distribución.
7. Amplíe **Opciones avanzadas y configuración de aplicaciones**.
8. Siga las siguientes pautas para completar las opciones:

| Ajuste                                                           | Descripción                                                                                                                                                                                                                                                                                                                                              |
| ---------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Instalar en dispositivo**                                      | Seleccione esta opción para iniciar la instalación inmediatamente después del registro. Se pedirá al usuario que confirme la instalación de la aplicación, excepto cuando el dispositivo sea un dispositivo Samsung Knox y se haya seleccionado la opción de instalación silenciosa que figura a continuación.                                           |
| **No mostrar la aplicación en el App Catalog del usuario final** | Seleccione esta opción si no desea que el usuario vea la aplicación en el catálogo de aplicaciones del dispositivo.                                                                                                                                                                                                                                      |
| **Instalar de forma silenciosa en dispositivos Samsung Knox**    | Seleccione esta opción si no desea que se solicite al usuario que confirme la instalación en dispositivos Samsung KNOX.                                                                                                                                                                                                                                  |
| **Establecer la prioridad de instalación de las aplicaciones**   | Para las aplicaciones de Android Enterprise, puede priorizar la descarga de aplicaciones específicas antes que otras aplicaciones. Por ejemplo, se puede priorizar la descarga de las aplicaciones Tunnel y Email antes que otras aplicaciones no tan importantes. A continuación se enumeran las opciones de nivel de prioridad disponibles:\* **Alto** |

:::Paragraph{listStyleType="disc" indent="2"}
Media (seleccionada por defecto)
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Baja**Este ajuste se puede aplicar en aplicaciones internas, públicas, privadas y de Web. Las aplicaciones internas se instalan a través del cliente y las públicas y privadas se instalan a través de Google. La prioridad de las aplicaciones se aplica solo a las aplicaciones que se instalan a través del mismo canal. |
\| **Instalar solo cuando esté conectado a Wi-Fi**                  | Seleccione esta opción para instalar la aplicación solo cuando el dispositivo esté conectado a la Wi-Fi.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
\| **Instalar solo cuando esté cargando**                           | Seleccione esta opción para instalar la aplicación solo cuando la carga del dispositivo esté en curso.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
\| **Instalar solo cuando esté inactivo**                           | Seleccione esta opción para instalar la aplicación solo cuando el dispositivo esté inactivo (no utilizado activamente por el usuario).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
\| **Lanzamiento automático al instalarlo**                         | Seleccione esta opción para iniciar una app automáticamente después de su instalación. Esta funcionalidad solo está disponible si la aplicación está recién instalada en el dispositivo y no para una actualización de versión.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
Haga clic en **Siguiente**.
:::

10. Seleccione una opción de promoción.
11. Haga clic en **Hecho**.

## Configuración de Aplicaciones corporativas

Las aplicaciones de Android Enterprise están disponibles en la sección de Aplicaciones de empresa del catálogo de aplicaciones, incluidas las aplicaciones siguientes.

- [**Divide Productivity**](./Desplegar_Divide_Productivity_con_Android_Enterprise.md)
- Correo electrónico+
- Túnel
- Gmail
