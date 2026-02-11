---
title: Resumen de nuevas funciones
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Esta sección ofrece un resumen de las nuevas funciones y mejoras disponibles en esta versión. También se proporcionan referencias a la documentación que describe estas características y mejoras, cuando están disponibles.

[**Características y mejoras generales**](./Resumen_de_nuevas_funciones.md)

[**Características de Android**](./Resumen_de_nuevas_funciones.md)

[**Funciones de iOS, macOS, watchOS, visionOS y tvOS**](./Resumen_de_nuevas_funciones.md)

## Características y mejoras generales

- **Límite mejorado para reglas y grupos de cuentas**: se han aumentado los límites para las evaluaciones de reglas y grupos de cuentas, estableciendo un máximo de 200 reglas. Esto puede resolver problemas causados por conjuntos de reglas extensos, prevenir fallos en la asignación de objetos y mejorar el rendimiento de las búsquedas elásticas.
- **Soporte de doble certificado para la comunicación Sentry-Tunnel**: Para mitigar las interrupciones del servicio causadas por la expiración de certificados, se ha introducido un nuevo campo **Agregar segundo certificado**. Esta mejora permite a los administradores cargar y vincular dos certificados, uno principal y otro secundario (de respaldo), a un perfil de Sentry. Adicionalmente, ahora se muestra la fecha de expiración de cada certificado, lo que permite un seguimiento proactivo y una renovación oportuna, garantizando una comunicación ininterrumpida entre Tunnel y Sentry.Para obtener más información, consulte [**Configurar AppTunnel**](./Configurar_AppTunnel.md).
- **Seguridad de exportación mejorada para Audit Trail**: la función de exportación de Audit Trail ahora es compatible con algoritmos de seguridad adicionales para las conexiones de SFTP:\* **Intercambio de claves**: se ha agregado compatibilidad para curve25519-sha256
  - **HMAC**: se ha agregado hmac-sha2-256 y hmac-sha2-512Estas mejoras aumentan la seguridad de la conexión. Para más información, véase [**Exportar trazas de auditorías**](./Exportar_trazas_de_auditorías.md).
- **Soporte de notificaciones para Sentry**: Ivanti Neurons for MDM ahora monitoriza periódicamente la disponibilidad de la conexión al servicio Sentry. Ivanti Neurons for MDM Muestra notificaciones de las versiones 10.4 de Sentry y de las nuevas versiones compatibles. Para obtener más información, consulte [**Trabajar con widgets**](./Trabajar_con_widgets.md).

## Características de Android

- **Soporte para ocultar y suspender aplicaciones**: desde la sección de Configuración de aplicaciones, ahora se pueden ocultar o suspender aplicaciones en dispositivos completamente gestionados.Para obtener más información, consulte [**Configuración de la aplicación**](<App Configuration.htm>).
- **Soporte para atributos de la segunda SIM en dispositivos Android**: el sistema ahora captura y muestra **Número de teléfono 2** e **ICCID 2** para dispositivos Android con doble SIM. Para dispositivos Android en versiones inferiores a 13, se mostrará NA para Número de teléfono 2 e ICCID2. En el caso de dispositivos en modo Perfil de Trabajo, el valor de ICICD2 también se mostrará como NA. Estos atributos son visibles en los detalles del dispositivo, la búsqueda avanzada y los informes personalizados en el modo de dispositivo completamente gestionado y en el modo de perfil de trabajo en dispositivos propiedad de la empresa.
- **Flujo de trabajo de despliegue de aplicaciones para Android Enterprise**: ahora los administradores pueden iniciar las instalaciones de aplicaciones mediante un flujo de trabajo paso a paso de App Catalog. El proceso incluye la entrega objetiva basada en la presencia de la aplicación, la selección de grupos de usuarios y la compatibilidad, con confirmación en tiempo real y visibilidad de las acciones a través de registros de auditoría. Para aplicaciones públicas y privadas, solo se puede desencadenar la instalación (no las actualizaciones) a través de esta interfaz.Para obtener más información, consulte [**Configuración de aplicaciones**](./Configuración_de_aplicaciones.md).

## Funciones de iOS, macOS, watchOS, visionOS y tvOS

- **Filtro DDM de Apple para ajustes de DDM**: se ha agregado un nuevo filtro **Apple DDM** (Gestión Declarativa de Dispositivos, por sus siglas en inglés) con la opción **Compatible** en **Configuraciones** > **Agregar configuración** para ayudar a identificar las configuraciones relacionadas con DDM más fácilmente en la IU. Esta mejora optimiza la experiencia del usuario al permitir una mejor distinción de los tipos de configuración de DDM.
- Para obtener más información, consulte [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).
  **Soporte para la configuración del filtro de contenido web en dispositivos macOS**: ahora la configuración del filtro de contenido Web es compatible con dispositivos macOS.Para más información, consulte [**Filtro de contenido web**](./Filtro_de_contenido_web.md).
- **Soporte para la configuración de certificados AppConnect en la aplicación Pulse Secure (iOS)**: la configuración de certificados AppConnect para el cliente Ivanti Secure Access (iOS) ahora es compatible en los ajustes de Ivanti Neurons for MDM. La sección "Configuración de certificados de AppConnect" es visible para el cliente de Ivanti Secure Access de la App Store (iOS) en Ivanti Neurons for MDM.
- **Gestión de versiones beta en el perfil de inscripción de dispositivos**: el perfil de inscripción de dispositivos ahora es compatible con la gestión de versiones beta en dispositivos iOS 17 y macOS 14. Se ha agregado un campo nuevo para programas beta en la selección **Requerir una versión de SO mínima para la inscripción** de dispositivos iOS y macOS. Para obtener información, consulte [**Inscripción de dispositivos**](./Inscripción_de_dispositivos.md).
- **Ver información de la plataforma para licencias**: ahora los administradores pueden ver la información de la plataforma para los detalles de las licencias en la página de detalles de VPP. Para obtener más información, consulte [**Apps and Books de Apple**](./Apps_and_Books_de_Apple.md).
- **Pestaña Soporte del cliente de Ivanti Go**: se ha cambiado el nombre de **Privacidad del cliente de Ivanti Go** a **Ajustes del cliente de Ivanti Go**. A new field **Enable Support Tab** is added in **Ivanti Go Client Settings Configuration**. Para obtener más información, consulte [**Ajustes del cliente de Ivanti Go**](./Ajustes_del_cliente_de_Ivanti_Go.md).
- **Soporte para Gestión de acceso de Apple**: Ivanti Neurons for MDM ahora es compatible con la **Gestión de acceso de Apple** para dispositivos supervisados y gestionados. Para obtener más información, consulte [**Administración de acceso de Apple**](./Administración_de_acceso_de_Apple.md).

## Características de Mobile Threat Defense

Mobile Threat Defense (MTD) protege los dispositivos administrados de las amenazas y vulnerabilidades móviles que afectan a dispositivos, redes y aplicaciones. Para obtener información sobre las funciones relacionadas con la MTD, según la versión actual, consulte la Guía de la solución de Mobile Threat Defense para su plataforma, disponible en la sección MOBILE THREAT DEFENSE en la página de [**documentación de productos**](https://www.ivanti.com/support/product-documentation) de Ivanti.

Cada versión de la «Guía de MTD» contiene todas las características de Mobile Threat Defense que se han probado totalmente a día de hoy y que están disponibles para su uso tanto en entornos de servidor como de cliente. Debido al desfase entre las versiones del servidor y del cliente, las nuevas versiones de la Guía de MTD están disponibles con la última versión de la serie cuando las características son totalmente funcionales.
