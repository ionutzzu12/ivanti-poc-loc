---
title: Introducción a los dispositivos
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Administrar dispositivos**](./Introducción_a_los_dispositivos.md)
- [**Llevar a cabo acciones en un dispositivo**](./Introducción_a_los_dispositivos.md)
- [**Ajustar la zona horaria de un dispositivo**](./Introducción_a_los_dispositivos.md)
- [**Enumerar los dispositivos por criterios**](./Introducción_a_los_dispositivos.md)
- [**Mostrar información detallada sobre los dispositivos**](./Introducción_a_los_dispositivos.md)
- [**Asigne en masa o cambie los usuarios o atributos personalizados en los dispositivos**](./Introducción_a_los_dispositivos.md)
- [**Exportación de dispositivos a un archivo CSV**](./Introducción_a_los_dispositivos.md)
- [**Buscar registros de un dispositivo**](./Introducción_a_los_dispositivos.md)

Cada entrada de la página **Dispositivos&#x20;**&#x72;epresenta un dispositivo móvil que se registró en Ivanti Neurons for MDM y muestra información importante acerca de este. La página de la lista de dispositivos muestra los dispositivos con información como:

- Nombre
- Dirección de correo electrónico
- N.º de teléfono
- SO
- Tipo de dispositivo
- Estado
- Último ingreso
- Recuento de infracciones
- Espacio
- Propietario legal (para iPad compartidos)

La dirección IP de Wi-Fi se comunica al servidor de Ivanti Neurons for MDM. Cualquier cambio en la dirección IP se comunica en cada registro. La dirección IP conforme al RGPD está disponible como opción en la página de la lista de dispositivos y en la página de detalles del dispositivo. Esta función requiere que los dispositivos se registren a través de Go 5.5 para iOS o versiones posteriores y Go 72 o versiones posteriores para Android, según lo admita Ivanti Neurons for MDM.

A medida que se añaden nuevos campos del RGPD (como la dirección IP y la ID de eSIM) a lo largo de las versiones de Ivanti Neurons for MDM, los administradores que han configurado el RGPD tendrán que editar el perfil del RGPD si desean ocultar los nuevos campos.

El identificador de equipos (EID) se muestra como atributo de iOS cuando una lista de dispositivos se exporta al formato de hoja de cálculo (CSV). El EID y el EID móvil (MEID) (cuando están presentes) están prefijados por una cadena EID o MEID, respectivamente.

El servidor de Ivanti Neurons for MDM no puede gestionar el procesamiento del mismo dispositivo con identificadores de diferentes clientes y registrados en distintos abonados. El servidor solamente puede gestionar la instancia donde está el mismo dispositivo con diferentes identificadores de clientes y registrados en el mismo abonado.

## Administrar dispositivos

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a **Dispositivos**.
3. Seleccione uno o más dispositivos.
4. Seleccione una acción en la lista desplegable de **Acciones**.

La siguiente tabla detalla las acciones disponibles desde la página Dispositivos:

| **Categoría** | **Acción**        |
| ------------- | ----------------- |
| Común         | - Añadir al grupo |

- Desbloqueo de AppConnect>
- Asignar atributos personalizados
- [**Asignar al usuario**](./Asignar_un_dispositivo_a_un_nuevo_usuario.md)
- Sincronización con el estado de compatibilidad del dispositivo
- Desactivar Escritorio remoto
- Activar Escritorio remoto
- Activar/desactivar Bluetooth
- [**Forzar ingreso**](./Forzar_el_ingreso_de_un_dispositivo.md)
- [**Bloquear**](./Bloquear_un_dispositivo.md)
- Eliminar atributos personalizados
- Reiniciar/apagar
- Sincronización con el estado de compatibilidad del dispositivo
- [**Eliminar un dispositivo**](./Retirar_un_dispositivo.md)
- [**Enviar mensaje**](./Enviar_un_mensaje.md)
- Establecer propiedad
- [**Desbloquear**](./Desbloquear_un_dispositivo.md)
- [**Borrar**](./Borrar_un_dispositivo.md) |
  \| iOS           | \* [**Asignar al propietario legal**](./Dispositivos_iPad_compartidos_para_empresas.md) (Solo para iPad compartidos)
- Reinstalar aplicaciones del sistema iOS
- Establecer zona horaria                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
  \| macOS         | - Establecer contraseña automática del administrador de macOS
- Establecer/cambiar contraseña del firmware
- Configurar/cambiar el bloqueo de recuperación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| Android       | \* Entrar en modo kiosko
- Salir del modo Pantalla completa                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| Windows       | Secuencias de comandos y Acciones a través de Ivanti Bridge                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

## Llevar a cabo acciones en un dispositivo

El menú Acciones (botón de elipsis) le permite llevar a cabo varias acciones en un dispositivo seleccionado.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en el nombre del dispositivo. Se abre la página de información del dispositivo.
:::

:::WorkflowBlockItem
Haga clic en Acciones (menú elipsis) para realizar una de las siguientes acciones de dispositivos:

- Cambiar nombre del dispositivo
- Eliminar dispositivo
- Editar Pertenencia al grupo
- Activar/desactivar Bluetooth
- Secuencias de comandos y Acciones a través de Ivanti Bridge
- Extraer el registro de Ivanti Bridge
- [**Renunciar a la propiedad**](./Renuncia_de_la_propiedad_de_un_dispositivo.md)
- Solicitar registros de depuración
- Reiniciar/apagar dispositivo
- Retirar
- Establecer propiedad
- Configurar/cambiar el bloqueo de recuperación
- Borrar
- Sincronización con el estado de compatibilidad del dispositivo
:::
::::

## Ajustar la zona horaria de un dispositivo

**Aplicable a:** dispositivos iOS 14.0+ y tvOS 14.0+

Esta acción no requiere servicios de localización. La acción del dispositivo de zona horaria también se muestra en la página de detalles del dispositivo. Los cambios de zona horaria realizados en el dispositivo también se reflejarán en el servidor de Ivanti Neurons for MDM.

Esta acción del dispositivo desencadena un error si la restricción **Forzar fecha y hora automáticos** está habilitada en la [**Configuración de restricciones para iOS.**](./Restricciones_de_iOS.md)

**Procedimiento**

1. Seleccione uno o más dispositivos.
2. Haga clic en **Acciones** > **Establecer la zona horaria** para los dispositivos seleccionados.
3. Ingrese la cadena de zona horaria con el formato de identificación de zona horaria de Olson. Por ejemplo, Pacífico/A mitad de camino.
4. Haga clic en **Establecer zona horaria**.

## Enumerar los dispositivos por criterios

Puede usar la barra de navegación lateral de Filtros para buscar y ver dispositivos específicos de toda la lista de dispositivos. Utilice la lista desplegable Espacio para seleccionar todos los espacios o espacios específicos para ver los dispositivos y la información relacionada. También puede buscar dispositivos utilizando la versión de visualización o la versión del paquete. La página Dispositivos muestra tanto la versión del paquete como la versión de visualización de los dispositivos.

Cuando se navega por la página de Grupos de dispositivos y hace clic en el número que se lista en **N.º de dispositivos** o bien, desde la página **Inventario de aplicaciones** haciendo clic en el enlace del recuento instalado en la columna **N.º instalado**, se muestra un mensaje que indica el nombre del espacio para el que se enumeran los dispositivos en la página.

## Mostrar información detallada sobre los dispositivos

Haga clic en el enlace de la columna Nombre de una entrada para visualizar la página Detalles del dispositivo: la página Detalles del dispositivo contiene varias pestañas donde se organiza la siguiente información:

- **Descripción general**: en la siguiente tabla se enumeran todos los detalles que aparecen en la pestaña Descripción general:

| Nombre de la sección | Descripción                 |
| -------------------- | --------------------------- |
| **General**          | - Ubicación del dispositivo |

:::Paragraph{listStyleType="disc" indent="2"}
Fabricante
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dirección MAC de Wi-Fi
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dirección WiFi-IP (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Anclado a la red - (dispositivos iOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Tiene batería: (solo para macOS 13.3+)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dirección IP
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dirección IP pública: muestra la dirección IP del dispositivo para Android o ChromeOS. Si el dispositivo se conecta a una VPN o a un servidor proxy, muestra la dirección IP de la proxy WAN.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Número de modelo: (macOS 13.3+ e iOS 16.4+)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Número de serie
:::

:::Paragraph{listStyleType="disc" indent="2"}
Número alternativo de serie (dispositivos Android): número de serie específico del fabricante aplicable a dispositivos Samsung en modo Administrador del dispositivo o Propietario del dispositivo.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Uso del almacenamiento - Almacenamiento utilizado (excepto Windows) y almacenamiento interno disponible en los dispositivos
:::

:::Paragraph{listStyleType="disc" indent="2"}
Batería disponible (Android) 
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado de batería (Android): cargando, descargando, completa y no cargando
:::

:::Paragraph{listStyleType="disc" indent="2"}
Carga restante estimada de la batería (Windows)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Tiempo de ejecución estimado de la batería (Windows)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Actualización disponible (macOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Nombre de la actualización disponible (macOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Versión de SO
:::

:::Paragraph{listStyleType="disc" indent="2"}
Versión de compilación del SO
:::

:::Paragraph{listStyleType="disc" indent="2"}
Versión de generación suplementaria
:::

:::Paragraph{listStyleType="disc" indent="2"}
Suplemento SO/Versión Extra
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dispositivo Apple Silicon
:::

:::Paragraph{listStyleType="disc" indent="2"}
Versión de firmware
:::

:::Paragraph{listStyleType="disc" indent="2"}
Origen del dispositivo
:::

:::Paragraph{listStyleType="disc" indent="2"}
Propietario legal
:::

:::Paragraph{listStyleType="disc" indent="2"}
Modo multiusuario
:::

:::Paragraph{listStyleType="disc" indent="2"}
Zona horaria
:::

:::Paragraph{listStyleType="disc" indent="2"}
Actualización del sistema (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Versión de la revisión de Zebra (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Última Id. de Hotfix (dispositivos Windows)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Última instalación de Hotfix el (dispositivos Windows)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
\| **Ajustes**                                                        | \* Nombre del dispositivo
:::

:::Paragraph{listStyleType="disc" indent="2"}
Identificador del dispositivo
:::

:::Paragraph{listStyleType="disc" indent="2"}
GUID de dispositivo
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dispositivo de la Inscripción de dispositivos (dispositivos Apple)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Inscrito en la inscripción de dispositivos (dispositivos Apple)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Inscripción de dispositivos automatizada activada
:::

:::Paragraph{listStyleType="disc" indent="2"}
Inscrito en la Inscripción de dispositivos automatizada
:::

:::Paragraph{listStyleType="disc" indent="2"}
Inscrito en la inscripción de usuarios (dispositivos Apple)
:::

:::Paragraph{listStyleType="disc" indent="2"}
ID de Apple administrada registrada (dispositivos Apple)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Grupos de dispositivos
:::

:::Paragraph{listStyleType="disc" indent="2"}
Idioma
:::

:::Paragraph{listStyleType="disc" indent="2"}
Identificadores de dispositivos MDM
:::

:::Paragraph{listStyleType="disc" indent="2"}
Id. del cliente del dispositivo
:::

:::Paragraph{listStyleType="disc" indent="2"}
Versión de la aplicación del cliente
:::

:::Paragraph{listStyleType="disc" indent="2"}
Id. de paquete de la aplicación del cliente
:::

:::Paragraph{listStyleType="disc" indent="2"}
Registrado con el cliente
:::

:::Paragraph{listStyleType="disc" indent="2"}
Identificadores de dispositivos EAS
:::

:::Paragraph{listStyleType="disc" indent="2"}
Bloqueo de activación habilitado
:::

:::Paragraph{listStyleType="disc" indent="2"}
Gestión declarativa de Apple activada
:::

:::Paragraph{listStyleType="disc" indent="2"}
Código de derivación del Bloqueo de activación
:::

:::Paragraph{listStyleType="disc" indent="2"}
Condiciones del servicio
:::

:::Paragraph{listStyleType="disc" indent="2"}
Propiedad
:::

:::Paragraph{listStyleType="disc" indent="2"}
Cuenta de iTunes activa
:::

:::Paragraph{listStyleType="disc" indent="2"}
Servicio de localización de dispositivo activado
:::

:::Paragraph{listStyleType="disc" indent="2"}
En cuarentena
:::

:::Paragraph{listStyleType="disc" indent="2"}
Sentry bloqueado
:::

:::Paragraph{listStyleType="disc" indent="2"}
Acceso bloqueado
:::

:::Paragraph{listStyleType="disc" indent="2"}
Medida de cumplimiento bloqueada
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compatible con APNS
:::

:::Paragraph{listStyleType="disc" indent="2"}
Modo supervisado (dispositivos iOS y macOS): identifica un dispositivo supervisado. El dispositivo mantiene el control directo del equipo informático. El modo supervisado permite funciones adicionales de los dispositivos (por ejemplo, implementaciones de servicios de campo, dispositivos de puntos de venta al por menor), dispositivos «en préstamo» utilizados en la hostelería y servicios, y dispositivos compartidos entre los alumnos de un aula de laboratorio.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Borrar PIN: haga clic en **Ver** para mostrar el PIN.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Usuario administrador de macOS gestionado (dispositivos macOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado del cifrado del dispositivo (dispositivos macOS)\* Cifrado de FileVault habilitado
:::

:::Paragraph{listStyleType="disc" indent="3"}
Clave de recuperación personal utilizada
:::

:::Paragraph{listStyleType="disc" indent="3"}
Clave de recuperación institucional utilizada
:::

:::Paragraph{listStyleType="disc" indent="2"}
Token de Bootstrap disponible
:::

:::Paragraph{listStyleType="disc" indent="2"}
Protección de la integridad del sistema habilitada
:::

:::Paragraph{listStyleType="disc" indent="2"}
Contraseña del firmware\* Contraseña
:::

:::Paragraph{listStyleType="disc" indent="3"}
Cambio pendiente
:::

:::Paragraph{listStyleType="disc" indent="3"}
Estado del comando
:::

:::Paragraph{listStyleType="disc" indent="3"}
Permitir la opción ROM
:::

:::Paragraph{listStyleType="disc" indent="2"}
Bloqueo de recuperación\* Contraseña
:::

:::Paragraph{listStyleType="disc" indent="3"}
Bloqueo de recuperación habilitado
:::

:::Paragraph{listStyleType="disc" indent="2"}
Detalles de los ajustes de cortafuegos (dispositivos macOS)\* Firewall habilitado
:::

:::Paragraph{listStyleType="disc" indent="3"}
Bloquear todo lo entrante
:::

:::Paragraph{listStyleType="disc" indent="3"}
Modo sigiloso
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado del cortafuegos de la aplicación (dispositivos macOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado del firewall (dispositivos Windows)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Última copia de seguridad en iCloud (dispositivos iOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Período de gracia del bloqueo del código de acceso (dispositivos iOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Id. de Android
:::

:::Paragraph{listStyleType="disc" indent="2"}
Nivel de revisión de la seguridad de Android (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Modo kiosco (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Tipo de certificación SafetyNet de Android (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compatible con Android Enterprise (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Habilitado para la versión corporativa de Android (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compatible con Samsung SAFE (dispositivos Android)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dispositivos Android administrados en el trabajo (Propietario del dispositivo) habilitados
:::

:::Paragraph{listStyleType="disc" indent="2"}
Perfil de trabajo de Android en el Dispositivo propiedad de la empresa habilitado
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado nativo de antiphishing
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado de antiphishing
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado de la VPN de antiphishing
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dispositivo administrado de Android con perfil profesional
:::

:::Paragraph{listStyleType="disc" indent="2"}
Se habilitó el bloqueo del Perfil de trabajo de Android en el Dispositivo propiedad de la empresa
:::

:::Paragraph{listStyleType="disc" indent="2"}
Help\@Work disponible
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compatible con Zebra
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado de Secure Apps
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado del cifrado de Secure Apps
:::

:::Paragraph{listStyleType="disc" indent="2"}
Modo de cifrado de Secure Apps
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compatible con FCM
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado de activación del MTD |
\| **Protección de la información de Windows (dispositivos Windows)** | - WIP
:::

:::Paragraph{listStyleType="disc" indent="2"}
Bloqueador de aplicaciones configurado
:::

:::Paragraph{listStyleType="disc" indent="2"}
Ajustes de EDP obligatorios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
\| **Telefonía&#x20;**&#x20;                                               | **Suscripciones a servicios para dispositivos**- Teléfono
:::

:::Paragraph{listStyleType="disc" indent="2"}
Tecnología de telefonía móvil
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMSI
:::

:::Paragraph{listStyleType="disc" indent="2"}
ICCID
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMEI
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMEI 2 - (solo en dispositivos Android con un puerto SIM doble. Aplicable a Android 8.0 o posterior)
:::

:::Paragraph{listStyleType="disc" indent="2"}
MEID
:::

:::Paragraph{listStyleType="disc" indent="2"}
Ubicación del dispositivo
:::

:::Paragraph{listStyleType="disc" indent="2"}
Operador
:::

:::Paragraph{listStyleType="disc" indent="2"}
MCC de origen
:::

:::Paragraph{listStyleType="disc" indent="2"}
MNC de origen
:::

:::Paragraph{listStyleType="disc" indent="2"}
Nombre del país actual
:::

:::Paragraph{listStyleType="disc" indent="2"}
Nombre del país de origen
:::

:::Paragraph{listStyleType="disc" indent="2"}
Tecnología de telefonía móvil
:::

:::Paragraph{listStyleType="disc" indent="2"}
Itinerancia
:::

:::Paragraph{listStyleType="disc" indent="2"}
Operador actual
:::

:::Paragraph{listStyleType="disc" indent="2"}
MMC actual
:::

:::Paragraph{listStyleType="disc" indent="2"}
MNC actual
:::

:::Paragraph{listStyleType="disc" indent="2"}
Itinerancia de datos
:::

:::Paragraph{listStyleType="disc" indent="2"}
Itinerancia de vozEn los dispositivos iOS compatibles estas propiedades se muestran para varias suscripciones de servicio activo eSIM.**Suscripciones a servicios SIM**- Versión de ajuste del operador
:::

:::Paragraph{listStyleType="disc" indent="2"}
Red de ajuste del operador
:::

:::Paragraph{listStyleType="disc" indent="2"}
MMC actual
:::

:::Paragraph{listStyleType="disc" indent="2"}
MNC actual
:::

:::Paragraph{listStyleType="disc" indent="2"}
Identificador eSIM
:::

:::Paragraph{listStyleType="disc" indent="2"}
ICCID
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMEI
:::

:::Paragraph{listStyleType="disc" indent="2"}
Datos preferidos
:::

:::Paragraph{listStyleType="disc" indent="2"}
Voz preferida
:::

:::Paragraph{listStyleType="disc" indent="2"}
Etiqueta
:::

:::Paragraph{listStyleType="disc" indent="2"}
ID de etiqueta
:::

:::Paragraph{listStyleType="disc" indent="2"}
Número de teléfono
:::

:::Paragraph{listStyleType="disc" indent="2"}
Ranura SIM
:::

:::Paragraph{listStyleType="disc" indent="2"}
En itinerancia
:::

:::Paragraph{listStyleType="disc" indent="2"}
Abonado Red portadora                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
\| **Cumplimiento de los dispositivos Azure**                         | \* Identificador del dispositivo Azure
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado de cumplimiento del dispositivo Azure
:::

:::Paragraph{listStyleType="disc" indent="2"}
Código de estado del cliente de Azure
:::

:::Paragraph{listStyleType="disc" indent="2"}
Hora del informe de cumplimiento del dispositivo Azure
:::

:::Paragraph{listStyleType="disc" indent="2"}
UPN del usuario del dispositivo de Azure Intune                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
\| **Conformidad de dispositivos de Google BeyondCorp**               | - Identificador del dispositivo
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado del compatibilidad
:::

:::Paragraph{listStyleType="disc" indent="2"}
Hora del informe de compatibilidad
:::

:::Paragraph{listStyleType="disc" indent="2"}
Usuario                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
\| **Información de batería**                                         | \* Nivel de batería: muestra el nivel de carga actual de la batería, tal y como ha informado el SO de Android
:::

:::Paragraph{listStyleType="disc" indent="2"}
Condición de la batería: como han informado los dispositivos Android, Mac e iOS.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Estado de carga de la batería: como ha informado SO de Android
:::

:::Paragraph{listStyleType="disc" indent="2"}
Porcentaje de integridad de la batería (específico de OEM): la integridad de la batería en porcentaje para los fabricantes de los dispositivos compatibles, como Zebra
:::

:::Paragraph{listStyleType="disc" indent="2"}
Fecha de fabricación de la batería (OEM): la fecha de fabricación de la batería de los fabricantes de dispositivos compatibles, como Zebra
:::

:::Paragraph{listStyleType="disc" indent="2"}
Ciclos de carga de la batería (OEM): número de ciclos completados en total para los fabricantes de dispositivos compatibles, como Zebra                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
**Configuraciones**: muestra los detalles de las configuraciones aplicadas. Para obtener más información, consulte [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md)
:::

- **Aplicaciones instaladas**: Muestra los detalles de las aplicaciones que están instaladas en el dispositivo. La fecha de instalación de la versión actual de la aplicación instalada se muestra en la columna **Fecha de la aplicación notificada** . Busque las aplicaciones instaladas para el dispositivo de la siguiente manera:\* Nombre de la aplicación
  - ID de conjunto o paqueteLa fecha de instalación de las aplicaciones de los dispositivos que salen de la cuarentena es la fecha en que el dispositivo se retira de la cuarentena.En el caso de los dispositivos Android Enterprise, también puedes ver los detalles de uso de las aplicaciones instaladas ordenadas por Día, Semana, Mes o Año. Para ver esta información, debe haber seleccionado la opción **Activar la recopilación de datos de uso de la aplicación** disponible en la sección **Configuración** , y luego puede seleccionar las opciones **Uso de la aplicación: Día**, **Uso de la aplicación: Semana**, **Uso de la aplicación: Mes**, **Uso de la aplicación: Año** para ver los detalles de uso de la aplicación.
- **Aplicaciones disponibles**: muestra los detalles de las aplicaciones que están disponibles para el dispositivo. Buscar a las aplicaciones disponibles para el dispositivo de la siguiente manera:\* Nombre de la aplicación
  - ID de conjunto o paqueteEn la columna **Configuración de aplicaciones**, al seleccionar **Nombre de configuración**, se le dirigirá a la pestaña **Configuración de aplicaciones** del catálogo de aplicaciones para que revise las opciones de configuración de la aplicación. Si es necesario, puede modificar la configuración de la aplicación para el dispositivo en la página **Resumen de configuración de la aplicación** . Para obtener más información sobre cómo configurar una aplicación, consulte [**Configuración de aplicaciones**](./Configuración_de_aplicaciones.md).En la columna **Configuración de aplicaciones**, al seleccionar **Nombre de configuración**, se le dirigirá a la pestaña **Configuración de aplicaciones** del catálogo de aplicaciones para que revise las opciones de configuración de la aplicación. Si es necesario, puede modificar la configuración de la aplicación para el dispositivo en la página **Resumen de configuración de la aplicación** . Para obtener más información sobre cómo configurar una aplicación, consulte [**Configuración de aplicaciones**](./Configuración_de_aplicaciones.md).Asegúrese de recordar el nombre y el tipo de la configuración de la aplicación específica para el dispositivo asignado en la página **Configuración de aplicaciones**.La columna **Estado** indica el estado de instalación de la aplicación en el dispositivo. El estado de instalación de la aplicación solo se captura para las aplicaciones gestionadas. El estado de instalación de las aplicaciones no gestionadas se muestra como No instalado. Debe convertir la aplicación en Gestionada para ver el estado correcto de la instalación.
- **Aplicaciones de AppConnect**: información de las aplicaciones AppConnect instaladas.
- **Políticas**: detalles de las políticas aplicadas . Para los dispositivos en riesgo, compruebe el motivo de la infracción en la columna Infracción. Si se accedió a la raíz del dispositivo, el sistema mostrará el motivo en la columna **Infracción**:| Prioridad (1 = la más alta) | Infracción                                                         |
  \| --------------------------- | ------------------------------------------------------------------ |
  \| 1                           | Plugin en riesgo                                                   |
  \| 2                           | Cliente manipulado                                                 |
  \| 3                           | Fabricante de dispositivos desconocido: desconocido                |
  \| 4                           | Carpeta sospechosa detectada: \[ruta]                              |
  \| 5                           | Se ha encontrado un binario sospechoso en: \[ruta]                 |
  \| 6                           | La carpeta /data es navegable o la carpeta /data/data es navegable |
  \| 7                           | Se encontró /system/app/Superuser.apk                              |
  \| 8                           | El administrador del paquete ha sido vulnerado                     |
  \| 9                           | Se ha encontrado una aplicación sospechosa: \[package]             |
- **Certificados**: detalles de los certificados instalados.Para ver el uso del certificado, vea la columna Tipo de uso. Si el certificado es específico para el dispositivo, mostrará el tipo de uso como 'dispositivo'. Si el certificado es específico para el usuario, mostrará el tipo de uso como 'usuario'.
- **Sentry** - información sobre Sentry (asociaciones ActiveSync)
- **Atributos** - atributos personalizados y atributos del dispositivo
- **Usuarios**: muestra la lista de usuarios activos para el dispositivo MacOS supervisado.La pestaña **Usuarios** se ha mejorado y se muestra la identificación de Apple administrado como un hipervínculo, y al hacer clic se redirige a la página de detalles de la cuenta de usuario en el iPad compartido.
- **Registros**: consulte y personalice los filtros de los dispositivos. Puede hacer lo siguiente desde Filtros:\* Seleccione el nombre de la acción para filtrar los dispositivos en función de las acciones de la aplicación.
  - Seleccione Estado.
  - Especifique la Fecha de inicio y la Fecha final.
- **Hardware** - detalles del inventario de hardware (sistema, placa base, BIOS, disco duro, CD ROM, procesador y memoria física)

## Asigne en masa o cambie los usuarios o atributos personalizados en los dispositivos

Puede utilizar la función Asignación en masa a través del icono de carga para cargar un archivo CSV para asignar o cambiar los usuarios y/o los atributos personalizados en los dispositivos en masa.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Desde la página Dispositivos, haga clic en el icono **Asignación en masa a través de la carga** (junto al botón Acciones).
:::

:::WorkflowBlockItem
(Opcional) Haga clic en **Descargar plantilla** para guardar un archivo de plantilla CSV que puede editar y cargar.
:::

:::WorkflowBlockItem
Cuando el archivo CSV esté listo, haga clic en **Elegir archivo** para explorar la localización del archivo CSV o arrastre y suelte el archivo CSV en la sección Datos del archivo.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones:
:::

:::WorkflowBlockItem
- **Forzar la asignación (sobrescritura) de todos los atributos aunque se encuentre algún valor existente.**
- **Sobrescribir solo si el valor está vacío y omitir atributos con valores existentes.**
  Haga clic en **Cargar**.
:::
::::

## Exportación de dispositivos a un archivo CSV

Puede exportar la información del dispositivo de un dispositivo específico mediante la opción **Exportar a CSV** desde la página **Dispositivos**.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Seleccione todos o múltiples espacios para ver la información relacionada con espacios específicos.
3. Haga clic en el enlace del número de dispositivos. Se muestra la página Lista de dispositivos relacionada con el espacio seleccionado.
4. Haga clic en la opción **Exportar a CSV** para exportar la lista de dispositivos y detalles relacionados a un archivo CSV. Aparece un mensaje emergente que informa de que el informe de exportación tardará un tiempo en procesarse. Espere a que se complete la solicitud para enviar otra solicitud. Cuando el informe está listo, recibirá un mensaje que le indicará que debe descargar o eliminar el informe.
5. Haga clic en **Descargar**. Usted también recibirá un correo electrónico con un enlace para descargar el informe.
6. (Opcional) Haga clic en **Eliminar&#x20;**&#x70;ara eliminar el informe.

## Buscar registros de un dispositivo

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Dispositivos&#x20;**>**&#x20;Dispositivos**, haga clic en el enlace de la columna **Nombre** de una entrada.
:::

:::WorkflowBlockItem
Haga clic en la pestaña **Registros**.
:::

:::WorkflowBlockItem
Utilice los filtros Acción, Estado, Fecha de inicio y Fecha de fin para restringir los dispositivos mostrados. Puede hacer lo siguiente desde Filtros:1) Seleccione el nombre de la acción para filtrar los dispositivos en función de las acciones de la aplicación.
2\) Seleccione Estado.
3\) Especifique la Fecha de inicio y la Fecha final.
:::

:::WorkflowBlockItem
La columna Detalles del dispositivo muestra el estado de la aplicación de la siguiente manera\:Para todos los dispositivos, el estado muestra los siguientes detalles:\* Nombre de la aplicación, versión de la aplicación, paquete o ID del paquete

- Estado de la instalación
- Cualquier error y la razón del errorPor ejemplo - appOrConfigName=Nombre:\<app name>;Identificador=\<bundleid>;iTunesStoreId:\<itunesid>;Estado:\<status or error reason from Apple>versión: \<app version>

Para los dispositivos Windows, el estado muestra los siguientes detalles:

- Incluye el ID del paquete, el estado y los errores.Por ejemplo:
- Para el tipo: inventario y estado de la aplicación: reconocer. Muestra: appType
- Para el tipo: inventario y estado de la aplicación: envío. No muestra nada
- Para el tipo: instalación/desinstalación y el estado: correcto/incorrecto/envío: muestra Incluir ID de paquete o ID de paquete, estado, nombre, versión y errores.
:::
::::

Si no puede ver la página **Dispositivos**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración de dispositivos
- Dispositivo de solo lectura
