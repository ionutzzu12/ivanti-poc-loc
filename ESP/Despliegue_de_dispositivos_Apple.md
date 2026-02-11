---
title: Despliegue de dispositivos Apple
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM es compatible con la gestión de todos los dispositivos de Apple. Se trata de una solución integral para aprovisionar, gestionar, actualizar y proteger su flota, de manera que el usuario final vive la mejor experiencia de uso.

Esta sección contiene los siguientes temas:

- [**Instalación del certificado MDM de Apple**](./Despliegue_de_dispositivos_Apple.md)
- [**Inscripción de dispositivos Apple**](./Despliegue_de_dispositivos_Apple.md)
- [**Ivanti Go para clientes de iOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Gestión de aplicaciones para dispositivos Apple**](./Despliegue_de_dispositivos_Apple.md)
- [**Administrar configuraciones**](./Despliegue_de_dispositivos_Apple.md)
- [**Administración de actualizaciones de software**](./Despliegue_de_dispositivos_Apple.md)
- [**Configuración de dispositivos de iOS/iPadOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Configuración de dispositivos de watchOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Acciones de dispositivo compatibles con dispositivos watchOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Configuración de dispositivos visionOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Acciones de dispositivo compatibles con dispositivos visionOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Configuración de dispositivos de macOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Configuración de dispositivos TvOS**](./Despliegue_de_dispositivos_Apple.md)
- [**Soporte para la gestión de dispositivos declarativos (DDM)**](./Despliegue_de_dispositivos_Apple.md)

## Instalación del certificado MDM de Apple

Para administrar dispositivos de Apple, empiece por solicitar e instalar un certificado de Apple MDM para administrar dispositivos iOS. Renueve el certificado MDM de Apple una vez al año. (La cuenta de Apple que se usó para crear el certificado recibe una notificación de la web de Apple cuando se acerca la fecha de caducidad). Utilice la página Certificado de MDM para agregar o renovar este certificado.

Siga los pasos descritos en [**Instalar certificado MDM**](./Instalación_del_Certificado_MDM.md)

## Inscripción de dispositivos Apple

Puede elegir cualquiera de los métodos siguientes para inscribir dispositivos:

- [**Inscripción de dispositivos automatizada**](./Inscripción_de_dispositivos.md)
- [**Director de la escuela de Apple**](./Configurador_de_Apple.md)
- [**Configurador de Apple**](./Configurador_de_Apple.md)

## Ivanti Go para clientes de iOS

El siguiente paso es seleccionar el tipo de inscripción que su empresa permite para los dispositivos. Ivanti Neurons for MDM actualmente es compatible con:

- [**Registro de dispositivos (iOS, macOS y Android)**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md)
- [**Inscripción de usuarios en el Apple Business Manager**](./Inscripción_de_usuarios_en_el_Apple_Business_Manager.md)
- [**Inscripción de Usuario generada por cuenta**](<Account driven User Enrollment.htm>)
- [**Ajustes (Apple)**](./Ajustes__Apple_.md)

## Gestión de aplicaciones para dispositivos Apple

La página Catálogo de aplicaciones de Ivanti Neurons for MDM sirve como interfaz para que los administradores rijan su catálogo de aplicaciones de manera eficaz. Esta función abarca la organización de las aplicaciones móviles disponibles para los usuarios finales, y abarca tanto las tiendas de aplicaciones públicas como las destinadas a la distribución a través de Ivanti Neurons for MDM.

Aplicaciones compatibles:

La página Catálogo de aplicaciones agrega varios tipos de aplicaciones, incluidas aplicaciones de la AppStore pública, aplicaciones personalizadas, aplicaciones desarrolladas internamente, aplicaciones habilitadas para AppConnect, GoClient para iOS y M\@W para macOS, de manera que agilizan el proceso de importación para su posterior configuración y distribución.

En los dispositivos que funcionan con configuraciones de solo gestión de aplicaciones móviles (MAM), se pide a los usuarios de iOS que seleccionen un certificado de autenticación al acceder al catálogo de aplicaciones. Este paso de autenticación es crucial para garantizar el acceso a las aplicaciones de la lista y ajustarse a unas prácticas de seguridad sólidas.

Los MacBooks con chipset M1 de Apple ofrecen compatibilidad especializada con las aplicaciones VPP para iPhone y iPad dentro de \[Su producto de software]. En concreto, únicamente los administradores tienen autoridad para forzar aplicaciones VPP compatibles para iPhone y iPad, lo que impide que los usuarios las instalen directamente desde la aplicación.

Para obtener instrucciones de implementación detalladas y opciones de configuración, consulte la documentación completa disponible en la Guía del administrador y los recursos que figuran a continuación:

- [**Gestión de aplicaciones**](./Aplicaciones.md)
- [**Ajustes del catálogo de aplicaciones**](./Ajustes_del_catálogo.md)
- [**Configurar Apps y Books de Apple**](./Apps_and_Books_de_Apple.md)
- [**Tienda de aplicaciones corporativas de Apps@Work**](./Apps@Work__iOS__Android__Windows_y_macOS_.md)
- [**Restricciones de la AppStore de macOS**](./Restricciones_de_la_AppStore_de_macOS.md)

## Administrar configuraciones

Las configuraciones son conjuntos de ajustes que usted, como administrador, envía a los dispositivos. Por ejemplo, se pueden utilizar configuraciones para establecer los ajustes VPN y los requisitos del código de acceso en los dispositivos. Las configuraciones existentes en su sistema aparecerán en la página Configuraciones. Puede seleccionar varias configuraciones desde la página de Configuraciones y empujarlas a varios dispositivos a la vez. Estas configuraciones se pueden enviar a los spaces de dispositivos específicos y los dispositivos de otros spaces no se verán afectados. Las configuraciones se pueden enviar a un único espacio, a varios espacios o a todos los espacios a la vez.

La mayoría de las configuraciones en Ivanti Neurons for MDM son comunes a todas las plataformas. Para obtener más detalles sobre cómo trabajar con configuraciones, consulteTrabajar con configuraciones.

Algunas configuraciones solo son compatibles con plataformas específicas. Puede consultar la lista por plataforma compatible en Tipos de configuración

## Administración de actualizaciones de software

Puede empezar por establecer la configuración de Actualización de software para sus dispositivos iOS y macOS.

Al configurar una ventana programada para la actualización de software, el comando de actualización del sistema operativo se enviará cada hora al dispositivo para asegurarse de que la actualización no pierda la ventana. Según el comportamiento de Apple, cada vez que el dispositivo reciba la orden de actualización del sistema operativo, una ventana emergente notificará al usuario de la necesidad de actualizar. El usuario puede aplazarlo hasta tres veces. A la tercera vez, según el comportamiento de Apple, el dispositivo forzará la actualización.

Los dispositivos MacOS tienen algunas reglas específicas que se pueden aplicar. Consulte la configuración de las reglas de actualización de software macOS

### Comando de actualización del SO para iOS

También puede enviar una orden única de actualización a uno o varios dispositivos desde la Lista de dispositivos o desde la Página de dispositivos. Consulte el comando Programar actualización del SO.

## Configuración de dispositivos de iOS/iPadOS

Las siguientes configuraciones son compatibles con iOS/iPadOS:

- [**Restricciones de iOS/iPadOS**](./Restricciones_de_iOS.md)
- [**Configuración eSIM**](./Configuración_de_eSIM.md)\* [**Plan de conservación de datos**](./Borrar_un_dispositivo.md)
- [**Configuración de red móvil**](./Configuración_de_la_red_móvil.md)
- [**Activar Modo perdido**](./Administrar_dispositivos_en_el_modo_Perdido_de_Apple.md)
- [**Configurar un perfil de MDM en iOS**](./Configurar_un_perfil_de_MDM_en_iOS.md)
- [**Modo Single-App**](./Configurar_el_modo_Single_App_para_iOS.md)\* [**Modo aplicación única autónoma**](./Crear_configuración_en_modo_autónomo_de_una_única_aplicación.md)
- [**iPad compartido para negocios.**](./Dispositivos_iPad_compartidos_para_empresas.md)
- [**Configuración de educación**](./Educación.md)
- [**Configuración personalizada de iOS**](./Configuración_personalizada_iOS.md)
- [**Mensaje de la pantalla de bloqueo**](./Configuración_del_mensaje_de_la_pantalla_de_bloqueo.md)

## Configuración de dispositivos de watchOS

Ahora puede inscribir dispositivos Apple watchOS en Ivanti N-MDM mientras los vincula con los dispositivos iOS.

Esta función actualmente es compatible con: watchOS 10+.

ProcedureProcedimiento

1. Debe inscribir el dispositivo iOS 17+ supervisado.
2. Asigne la configuración de inscripción del Apple Watch al dispositivo iOS.
3. Ya puede emparejar su Apple Watch con el iPhone.

Puede emparejar el Apple Watch después de enviar la configuración del reloj al iPhone. No puede activar la gestión remota para un Apple Watch si la configuración del reloj se transfiere al iPhone después de que el Apple Watch se sincronice con él.

Las configuraciones siguientes son compatibles con los dispositivos watchOS:

- [**Cellular\_Configuration**](./Móvil.md)
- [**Configuración del certificado**](./Configuración_del_certificado.md)
- [**Transparencia del certificado**](./Transparencia_del_certificado.md)
- [**Identity\_Certificate\_Configuration**](./Certificado_de_identidad.md)
- [**Restricciones de iOS**](./Restricciones_de_iOS.md)
- [**Passcode\_Settings**](./Configuración_del_código_de_acceso.md)
- [**Per-App\_VPN\_Configuration**](./Configuración_de_VPN_por_aplicación.md)
- [**Wi-Fi\_Configuration**](./Configuración_de_Wi-Fi.md)

## Acciones de dispositivo compatibles con dispositivos watchOS

Las acciones siguientes del dispositivo son compatibles con los dispositivos watchOS:

- Borrar contraseña
- Bloquear el reloj de Apple
- Borrar Apple Watch
- Dar de baja el reloj Apple desde Ivanti Neurons for MDMAl desvincular el dispositivo iOS emparejado, el reloj se reiniciará y se desvinculará del dispositivo iOS.

## Configuración de dispositivos de macOS

Las siguientes configuraciones son compatibles con macOS:

- [**Restricciones de macOS**](./Restricciones_de_macOS.md)
- [**Configuración de dispositivos macOS**](./Configuración_de_dispositivos_macOS.md)
- [**Trabajar con scripts y el cliente Mobile@Work**](./Todas_las_secuencia_de_comandos.md)
- [**Configurar un perfil de MDM en macOS**](./Configurar_un_perfil_de_MDM_en_macOS.md)
- [**Configurar la contraseña del firmware**](./Establecer_la_contraseña_del_firmware.md)
- [**Activar FileVault**](./FileVault_2.md)\* [**Clave de recuperación de FileVault**](./Clave_de_recuperación_de_FileVault.md)
  - [**Configuración de opciones de FileVault**](./Configuración_de_opciones_de_FileVault.md)
- [**Plataforma y SSO extensible**](./Configuración_de_inicio_de_sesión_único.md)
- [**Active Directory macOS**](./Active_Directory__macOS_.md)
- [**Cortafuegos**](./Firewall_de_macOS.md)
- [**Ethernet**](./Configuración_de_Ethernet__macOS_.md)
- [**Creación de cuentas en Office 365**](./Creación_automática_de_cuentas_en_Office_365__macOS_.md)
- [**Extensiones del sistema de macOS**](./Configuración_de_las_extensiones_del_sistema_de_macOS.md)
- [**Restricciones de grabación en discos multimedia**](./Restricciones_de_grabación_en_disco_de_macOS.md)
- [**Ajustes de privacidad**](./Preferencias_de_privacidad__macOS_.md)

## Configuración de dispositivos TvOS

Las siguientes configuraciones son compatibles con tvOS:

- [**Configuración de Apple TV**](./Configuración_de_Apple_TV.md)
- [**Restricciones de Apple TV**](./Restricciones_de_iOS.md)
- [**Visualización de la sala de conferencias**](./Visualización_de_la_sala_de_conferencias.md)
- [**Duplicación AirPlay**](./Configuración_de_AirPlay.md)

## Configuración de dispositivos visionOS

Ahora puede inscribir dispositivos Apple visionOS en Ivanti Neurons for MDM.

Esta función actualmente es compatible con: visionOS 1.1+

Puede inscribir dispositivos visionOS utilizando uno de los siguientes métodos:

- [**Inscripción de dispositivos basada en cuenta**](<Account driven Device Enrollment.htm>)
- [**Inscripción de Usuario generada por cuenta**](<Account driven User Enrollment.htm>)
- [**Inscripción de dispositivos**](./Inscripción_de_dispositivos.md)

Las configuraciones siguientes son compatibles con los dispositivos visionOS:

- [**Configuración de CalDAV**](./Configuración_de_CalDAV.md)
- [**Configuración de CardDAV**](./Configuración_de_CardDAV.md)
- [**Configuración del certificado**](./Configuración_del_certificado.md)
- [**Configuración de comprobación de revocación de certificados**](./Configuración_de_comprobación_de_revocación_de_certificados.md)
- [**Transparencia del certificado**](./Transparencia_del_certificado.md)
- [**Creación de una configuración de proxy de DNS**](./Creación_de_una_configuración_de_proxy_de_DNS.md)
- [**DNS cifrado**](./DNS_cifrado.md)
- [**Configuración de correo electrónico**](./Configuración_de_correo_electrónico.md)
- [**Configuración de Exchange**](./Configuración_de_Exchange.md)
- [**Configuración de Google**](./Configuración_de_Google.md)
- [**Certificado de identidad**](./Certificado_de_identidad.md)
- [**Restricciones de iOS**](./Restricciones_de_iOS.md)
- [**Configuración de LDAP**](./Configuración_de_LDAP.md)
- [**Dominios administrados**](./Dominios_administrados.md)
- [**Configuración del relé de red**](./Configuración_del_relé_de_red.md)
- [**Configuración de VPN por aplicación**](./Configuración_de_VPN_por_aplicación.md)
- [**Configuración de inicio de sesión único**](./Configuración_de_inicio_de_sesión_único.md)
- [**Configuración del calendario suscrito**](./Configuración_del_calendario_suscrito.md)
- [**Configuración de VPN**](./Configuración_de_VPN.md)
- [**Filtro de contenido web**](./Filtro_de_contenido_web.md)
- [**Configuración de Wi-Fi**](./Configuración_de_Wi-Fi.md)

## Acciones de dispositivo compatibles con dispositivos visionOS

Las acciones siguientes del dispositivo son compatibles con los dispositivos visionOS:

- Borrar Apple Vision Pro
- Retirar Apple Vision Pro
- Desbloquear Apple Vision Pro

## Soporte para la gestión de dispositivos declarativos (DDM)

La gestión declarativa de dispositivos de Apple es un protocolo moderno de gestión que permite a los dispositivos gestionados aplicar de forma proactiva y autónoma sus propios ajustes de gestión con menos comunicación. La gestión declarativa de dispositivos se activa en los dispositivos recién inscritos durante la inscripción o durante el registro de los dispositivos ya inscritos.

La gestión declarativa de dispositivos se activa automáticamente en los dispositivos elegibles siguientes:

- Equipos con macOS 13 o posterior
- Dispositivos con iOS 15 o iPadOS 15 o posterior
- Los dispositivos inscritos a través de la inscripción de usuarios son compatibles con Declarative Device Management en iOS o iPadOS 16 o posterior.
- Dispositivos Apple TV con tvOS 16 o posterior
- Dispositivos Apple Watch con watchOS 10 o posterior
- Dispositivos Apple Vision Pro con visionOS 1.1 o posterior

Funciones de gestión declarativa compatibles actualmente:

- **Canales de estado**:\* Cambios en la versión del SO
  - Cumplimiento del código de acceso
  - Código de acceso presente
- **Configuraciones**:- Configuración de gestión declarativa

### Predicados en configuraciones DDM

Los predicados son expresiones en lenguaje Cocoa que pueden proporcionar flexibilidad y granularidad a la activación de una configuración un dispositivo. La expresión reside en el dispositivo y se aplicará cuando se cumplan las condiciones de este predicado. Hemos añadido una nueva función que permite crear, guardar y aplicar predicados a cualquier configuración de DDM.

La configuración de DDM muestra una nueva opción en la página Distribución para aplicar un Predicado. Puede encontrar los Predicados ya creados en la lista desplegable de esta sección.

Creación de un predicado

1. Vaya a **Administrador** > **Apple** > **Predicados**.
2. Haga clic en **Añadir**. ****Aparece en pantalla la ventana Crear predicados.
3. Introduzca la siguiente información:\* **Nombre**: nombre del predicado
   - **Descripción**: agregar alguna descripción relevante.
   - **Expresión de predicado**: expresión de predicado. Por ejemplo, @status(device.model.family) ==’iPad’.

::Image[]{src="Resources/Images/add_predicate1.png" signedSrc="Resources/Images/add_predicate1.png" size="68" caption alt isUploading="false" sha initialPath="Resources/Images/add_predicate1.png" githubPath="Resources/Images/add_predicate1.png" position="flex-start" indent="3"}

4. Haga clic en **Guardar**. Aparece un diálogo en la pantalla que confirma la creación del predicado.
5. Verifique la validez de la sintaxis de predicado actualizando la página y observando valores en el campo de estado (con valores: **Desconocido**, **En curso**, **Válido**, **No válido**).1) Haga clic en **Probar**. La ventana de **Probar predicado** aparece en la pantalla.
   2\) Introduzca la siguiente información:\* **Nombre**: predeterminado
   - **Expresión de predicado**: predeterminado
   - **Espacios**: espacio predeterminado
   - **Plataforma**: iOS/macOS
   - **Nombre del dispositivo**: relacionado con la expresión de predicado.El campo **Nombre del dispositivo** aparecerá bajo el campo **Plataforma** solo después de que se hayan seleccionado los campos **Espacios** y **Plataforma** en los desplegables.

::Image[]{src="Resources/Images/test_predicate2.png" signedSrc="Resources/Images/test_predicate2.png" size="64" caption alt isUploading="false" sha initialPath="Resources/Images/test_predicate2.png" githubPath="Resources/Images/test_predicate2.png" position="flex-start" indent="3"}

:::Paragraph{listStyleType="decimal" listStart="3" indent="2"}
Haga clic en **Probar predicado**.
:::

:::Paragraph{listStyleType="decimal" listStart="4" indent="2"}
Aparece un diálogo en la pantalla que confirma el inicio del predicado de prueba.
:::

:::Paragraph{listStyleType="decimal" listStart="5" indent="2"}
Actualice la página para encontrar el estado de la sintaxis de predicado.\* Para una expresión de predicado correcto, el estado cambia de **Desconocido** > **En curso** > **Válido**.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Para una expresión de predicado incorrecto, el estado cambia de **Desconocido** > **En curso** > **No válido**.
:::

6. Repita el procedimiento si desea crear varios predicados utilizando diferentes expresiones de predicado.

### Distribución de predicados para una configuración DDM

1. Cree una configuración compatible con DDM.
2. Configure el interruptor de palanca “Activación con predicados” en ON y use el botón para incluir los predicados (según sea necesario).

::Image[]{src="Resources/Images/predicates.png" signedSrc="Resources/Images/predicates.png" size="77" caption alt isUploading="false" sha initialPath="Resources/Images/predicates.png" githubPath="Resources/Images/predicates.png" position="flex-start"}

Para editar o eliminar un predicado, vaya a **Administrador** > **Apple** > **Predicados**. En esta página encontrará la lista de predicados disponibles. Haga clic en **Editar** para realizar cualquier cambio en el predicado existente y guardarlo. Del mismo modo, para eliminar un predicado existente, selecciónelo y haga clic en **Eliminar**.

No puede eliminar un predicado si está asociado a alguna configuración.

### Propiedades de administración para una configuración DDM

El administrador puede usar lo siguiente para crear predicados: 

- Variables de usuario y dispositivo
- Atributos del usuario
- Atributos del dispositivo

Ejemplo del uso de propiedades de gestión en predicados (atributos personalizados): 

Predicado para verificar si el nombre del usuario es "Prueba" @Property (UserFirstName) == 'Test'

### Más ejemplos

- Familia de hardware de un dispositivo: (Mac, iPhone, iPad, etc.)@status(device.model.family) =='iPad'Si cierto, el código de acceso está presente en el dispositivo. Si Falso, el código de acceso no está presente en el dispositivo.\@status(passcode.is-present)==true
- La familia del sistema operativo en uso en el dispositivo, como macOS o iOS.\@status(device.operating-system.family)=='iPadOS'
- La versión del sistema operativo en uso en el dispositivo, como 15.0\@status(device.operating-system.version)=='18.2'@status(device.operating-system.version)\<'18.3'@status(device.operating-system.version)>='18.2'
- Valor booleano que especifica el estado habilitado para la bóveda del archivo en el dispositivo\@status(diskmanagement.filevault.enabled)==true
- Ejemplo de propiedades de gestión (atributos personalizados)\:El predicado para verificar el nombre del usuario es "prueba"@property(userFirstName)=='test'
