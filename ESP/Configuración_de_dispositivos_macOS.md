---
title: Configuración de dispositivos macOS
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Este es un resumen que ofrece una lista de procedimientos frecuentes y otro contenido relacionado con la configuración de dispositivos macOS en Ivanti Neurons for MDM Puede acceder a todos los temas de macOS en la *Guía para el administrador de&#x20;*&#x49;vanti Neurons for MDM.

Contenido

- [**Registro de dispositivos**](./Configuración_de_dispositivos_macOS.md)
- [**Configuración de la plantilla de invitación de usuarios**](./Configuración_de_dispositivos_macOS.md)
- [**Configuración de funciones Zero Sign-on**](./Configuración_de_dispositivos_macOS.md)
- [**Configuración de Mobile@Work para el cliente macOS**](./Configuración_de_dispositivos_macOS.md)
- [**Configuración de secuencias de comandos de shell en macOS**](./Configuración_de_dispositivos_macOS.md)
- [**Configuración de ajustes de macOS**](./Configuración_de_dispositivos_macOS.md)
- [**Configuración de directivas de macOS**](./Configuración_de_dispositivos_macOS.md)
- [**Verificación de informes y otra información**](./Configuración_de_dispositivos_macOS.md)

## Registro de dispositivos

La mayoría de los usuarios comienzan por registrar un dispositivo. Para iniciar el proceso de registro, puede hacerlo de cualquiera de las siguientes formas:

- Envíe una invitación a uno o más usuario (registro de iReg). Para obtener más información, consulte el tema *Registro de dispositivos de macOS* en la sección [**Registro de dispositivos**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md).
- [**Inscripción de dispositivos**](./Inscripción_de_dispositivos.md) e [**Inscripción de usuarios en Apple Business Manager**](./Inscripción_de_usuarios_en_el_Apple_Business_Manager.md)

Para obtener más información, consulte en [**Registro de dispositivo**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md).

## Configuración de la plantilla de invitación de usuarios

Puede personalizar la invitación por correo electrónico del usuario final para que la apariencia le resulte más familiar a sus usuarios finales. Para obtener más información, consulte [**Plantillas de correo electrónico de personalización de marca**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md).

Puede personalizar el proceso de registro del dispositivo con nombres y logotipos que sus usuarios reconocerán. Para obtener más información, consulte [**Personalización de marca dispositivos**](./Marca_del_usuario.md).

Para obtener más información, consulte [**Configuración y uso de correos electrónicos de confirmación del registro**](./Configuring_registration_confirmation_emails.md).

## Configuración de funciones Zero Sign-on

Para la documentación relacionada con Zero Sign-on, consulte «Zero Sign-on con Access» en la *Guía de Access*.

Para la inscripción automática de Zero Touch, consulte el paso 13 del tema [**Ajustes de usuario**](./Ajustes_del_usuario.md) en la sección Configurar los ajustes para registrar dispositivos nuevos.

## Configuración de Mobile\@Work para el cliente macOS

Mobile\@Work para macOS proporciona lo siguiente:

- Prestaciones de secuencia de comandos en dispositivos macOS
- Catálogo de aplicaciones para usuarios finales
- Notificaciones «push»
- Pantalla de Incorporación del usuario (bienvenido/estado) para los registros de la inscripción de dispositivos automatizada

Antes de forzar Mobile\@Work en los usuarios finales, asegúrese de que [**Mobile@Work for macOS Configuration.htm**](./Mobile@Work_para_macOS.md)[**Mobile@Work para macOS**](./Mobile@Work_para_macOS.md) se ha creado y de que está ajustado para que se distribuya en los equipos de macOS de destino.

Puede habilitar la incorporación de usuarios a los dispositivos macOS durante el proceso automatizado de [**Inscripción de dispositivos**](./Inscripción_de_dispositivos.md). Tan pronto como se completa la Inscripción de dispositivos, Mobile\@Work para macOS se inserta en el dispositivo junto con los perfiles, configuraciones y aplicaciones.

## Configuración de secuencias de comandos de shell en macOS

Ivanti Neurons for MDMle permite crear sus propias secuencias de comandos de shell de macOS que luego pueden cargarse y Ivanti Neurons for MDMejecutarse en dispositivos macOS administrados. Se pueden configurar las secuencia de comandos utilizando la configuración de secuencia de comandos de Mobile\@Work para macOS. Mobile\@Work para macOS regresa los resultados de ejecución de la secuencia de comandos a Ivanti Neurons for MDM, y estos se muestran en los registros del dispositivo. Puede verificar los registros del dispositivo desde la página de detalles del dispositivo macOS, en la pestaña **Registros**. Para obtener más información sobre cómo crear, cargar y administrar el repositorio de secuencias de comandos, consulte [**Todas las secuencias de comandos**](./Todas_las_secuencia_de_comandos.md).

Antes de poder ejecutar las secuencias de comandos de shell en dispositivos macOS, asegúrese de que los usuarios dispongan de la aplicación Mobile\@Work para macOS en sus dispositivos y tengan una configuración de Mobile\@Work para macOS insertada en sus dispositivos. Las secuencias de comandos se pueden ejecutar una vez o de manera recurrente. Las secuencias de comando de Ivanti Neurons for MDM también permiten que los administradores recopilen información de un dispositivo y, a continuación se la almacene en Ivanti Neurons for MDM como atributo personalizado. Por ejemplo, si necesita saber cuál es la versión de Java de un dispositivo macOS, puede recopilar esta información y almacenarla individualmente por cada dispositivo en un atributo personalizado del dispositivo. Para obtener más información, consulte *Cómo crear una configuración de secuencia de comandos Mobile\@Work para macOS* en [**Mobile@Work para macOS.**](./Mobile@Work_para_macOS.md)

## Configuración de ajustes de macOS

Las [**Configuraciones**](./Configuraciones.md) son conjuntos de ajustes que se envían a los dispositivos. Por ejemplo, se pueden usar configuraciones para establecer los ajustes VPN y los requisitos del código de acceso en estos dispositivos. Utilice la página **Configuraciones** para seleccionar, configurar y distribuir configuraciones. Hay muchos [**tipos de configuraciones**](./Tipos_de_configuración.md) disponibles. En esta [**página**](./Tipos_de_configuración.md), puede ver una lista de las configuraciones disponibles de macOS, incluidas las siguientes:

- [**Wi-Fi**](./Configuración_de_Wi-Fi.md)
- [**Código de acceso**](./Configuración_del_código_de_acceso.md)
- [**VPN**](./Configuración_de_VPN.md)
- [**DNS cifrado**](./DNS_cifrado.md)
- [**FileVault 2**](./FileVault_2.md)
- [**Clave de recuperación de FileVault**](./Clave_de_recuperación_de_FileVault.md)
- [**Firewall de macOS**](./Firewall_de_macOS.md)
- [**Restricciones de macOS**](./Restricciones_de_macOS.md)
- [**Restricciones de la AppStore de macOS**](./Restricciones_de_la_AppStore_de_macOS.md)
- [**Ajustes del Finder de macOS**](./Ajustes_del_Finder_de_macOS.md)
- [**Política de extensiones del kernel de macOS**](./Política_de_extensiones_del_kernel_de_macOS.md)
- [**Active Directory (macOS)**](./Active_Directory__macOS_.md)
- [**Creación automática de cuentas en Office 365(macOS)**](./Creación_automática_de_cuentas_en_Office_365__macOS_.md)

Puede utilizar [**configuraciones predeterminadas**](./Configuración_personalizada.md) para importar y distribuir un archivo de configuración predeterminada.

## Configuración de directivas de macOS

Las [**Directivas**](./Políticas.md) definen los requisitos para los dispositivos, así como lo que pasará si un dispositivo no cumple con los requisitos. Cada política cuenta con una regla y una medida de cumplimiento (lo que sucede si se infringe la regla). Utilice la página **Políticas** para seleccionar, configurar y distribuir políticas. La protección de datos/cifrado desactivado y [**Aplicaciones permitidas**](./Supervisar_y_controlar_las_aplicaciones_permitidas.md) son directivas relacionadas con macOS. Puede utilizar [**Directivas personalizadas&#x20;**](./Política_personalizada.md)según el dispositivo y los atributos del usuario, los criterios de la sección, los valores y las medidas de cumplimiento que se especifiquen.

## Distribución de aplicaciones para macOS

Ivanti Neurons for MDM es compatible con la distribución de [**aplicaciones&#x20;**](./Catálogo_de_aplicaciones.md)macOS mediante el protocolo MDM de Apple y la aplicación Mobile\@Work. Los administradores pueden optar por utilizar uno o ambos de los siguientes enfoques:

- Protocolo MSM de Apple: Los administradores pueden cargar únicamente formatos PKG específicos (formato de distribución) como aplicaciones internas y también pueden distribuir aplicaciones desde Mac App Store (se incluye el soporte para licencias de Apps and Books de Apple). Sin embargo, este enfoque no permite que los administradores distribuyan DMG y otros formatos PKG.
- Mobile\@Work for macOS app - As a way to distribute apps to users, administrators can use MobileIron Packager (MIP) app to convert any PKG, DMG or .app files to an MIP file. Cargue el archivo MIP a Ivanti Neurons for MDM como aplicación interna.

Puede descargar el servicio Mac Packager de Ivanti Neurons for MDM desde las descargas de software de MobileIron.

Los administradores pueden utilizar Mobile\@Work para distribuir aplicaciones internas que están en formato DMG, PKG o .app. Para las aplicaciones que solo están disponibles en Mac App Store, los administradores pueden continuar usando las prestaciones de MDM, que incluyen las prestaciones de las licencias de Apps and Books de Apple.

## Verificación de informes y otra información

El [**Panel**](./Panel.md) muestra importantes estadísticas sobre los dispositivos registrados y los usuarios. Cada sección del panel se llama widget.

Puede verificar la información adicional de la siguiente manera:

- Revisar notificaciones: Vaya a la página **Panel > Notificaciones** (o haga clic en el icono de la campana \[esquina superior derecha]) para revisar las notificaciones y lleve a cabo acciones cuando sea necesario.
- Informes: Vaya a la página **Panel > Informes** para acceder a los datos de su sistema de administración unificada de dispositivos de trabajo (UEM, Unified Endpoint Management).
- Audit Trails: vaya a la página **Panel > Audit Trails** para acceder a los conjuntos de registros cronológicos que guardan la actividad realizada en todas las entidades de Ivanti Neurons for MDM. Para habilitar esta función, vaya a la página **Administrador > Infraestructura > trazas de auditorías** y haga clic en **Habilitar trazas de auditoría**.
