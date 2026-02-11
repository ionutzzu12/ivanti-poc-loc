---
title: Configuración de aplicaciones
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Licencias para las características de las aplicaciones**](./Configuración_de_aplicaciones.md)
- [**Pasos de la configuración comunes a múltiples aplicaciones**](./Configuración_de_aplicaciones.md)
- [**Ocultar o suspender aplicaciones (solo Android)**](./Configuración_de_aplicaciones.md)
- [**Configuración del relé de red**](./Configuración_de_aplicaciones.md)
- [**Configuración de la segmentación celular 5G**](./Configuración_de_aplicaciones.md)
- [**Distribución de aplicaciones mediante la configuración del filtro de contenidos web**](./Configuración_de_aplicaciones.md)
- [**Distribución de aplicaciones mediante proxy DNS**](./Configuración_de_aplicaciones.md)

La configuración de aplicaciones le permite personalizar la instalación, promoción y distribución de cada aplicación que instala en sus dispositivos de usuario. Las aplicaciones pueden ser sus propias aplicaciones internas, aplicaciones de una tienda pública o aplicaciones de Ivanti Neurons for MDM. Tiene la flexibilidad de implementar las aplicaciones para muchos usuarios y grupos diferentes con nombres y configuraciones exclusivos específicamente adaptados a cada destinatario. El número de versiones de aplicaciones internas está limitado a 100. Si se supera ese número, el sistema Ivanti Neurons for MDM purga las versiones más antiguas de la aplicación. El estado de la carga y purga de la aplicación aparece en una lista y es visible desde la página de Registros de Auditoría.

Al cambiar los valores de la configuración de aplicaciones para una aplicación en concreto en el App Catalog o en el perfil administrado de configuración de aplicaciones, será necesario introducir una o dos veces hasta que el dispositivo reciba los nuevos valores de configuración.

## Licencias para las características de las aplicaciones

Las siguientes características requieren licencias adicionales:

- Instalación/desinstalación silenciosa de aplicaciones: licencia Silver
- Configuración por aplicación: licencia Gold
- Configuración personalizada de AppConnect: licencia Gold

los paquetes de aplicaciones múltiples requieren una buena administración de grupos, ya que el sistema operativo Windows podría no definir los futuros tipos de dispositivos. En tal caso, la única forma de instalar la versión correcta de la aplicación es que el administrador utilice el grupo correcto para la aplicación correcta.

## Pasos de la configuración comunes a múltiples aplicaciones

Lleve a cabo estos pasos primero y, a continuación, proceda con los pasos de la configuración para cada aplicación que desee implementar. Puede diseñar múltiples configuraciones de la misma aplicación y darle a cada una un nombre exclusivo. Cada configuración puede tener su propia distribución y niveles de promoción para adaptarse a su estrategia de implementación. El número de versiones de aplicaciones internas está limitado a 100. Si se supera ese número, el sistema Ivanti Neurons for MDM purga las versiones más antiguas de la aplicación. El estado de la carga y purga de la aplicación aparece en una lista y es visible desde la página de Registros de Auditoría. Puede instalar una aplicación en un máximo de 100 usuarios, grupos de usuarios, dispositivos o grupos de dispositivos a la vez. Puede seleccionar una aplicación para agregarla al catálogo de aplicaciones. Ivanti Neurons for MDM tiene un proceso asincrónico para enviar comandos de solicitudes de instalación/actualización para aplicaciones de iOS. Cuando utiliza el comando Enviar instalación/Actualizar solicitud, el portal administrativo de Ivanti Neurons for MDM muestra un mensaje que el:

- el proceso continuará ejecutándose en segundo plano
- proceso completo
- estado independientemente de que el proceso se complete correctamente o con errores

**Procedimiento**

1. Vaya a **Aplicaciones > App Catalog** y haga clic en **+Añadir**.
2. Use el menú desplegable para seleccionar la App Store, Google Play o su app store interna y elija la aplicación que desea añadir al catálogo.Dependiendo de su acuerdo de licencia, es posible que también tenga disponibles aplicaciones para añadir al catálogo.
3. Opcionalmente, puede editar la Categoría de la aplicación.
4. Opcionalmente, puede añadir una breve descripción de la aplicación en el campo **Descripción**.
5. Haga clic en **Siguiente**.
6. Elija un nivel de distribución para la configuración de la aplicación:\* **Para todo el mundo:** la aplicación se añade a los dispositivos compatibles de todos los usuarios.
   - **A nadie:** la aplicación se almacena para distribuirse posteriormente.
   - **Distribución personalizada**: seleccione cualquiera de las siguientes opciones:\* **Usuarios/Grupos de usuarios**: la aplicación solo se distribuye a los usuarios o grupos de usuarios que usted elija.Haga clic en la pestaña **Usuarios** para seleccionar los usuarios.Haga clic en la pestaña **Grupos de usuarios** para seleccionar los grupos de usuarios.
     - **Dispositivos/Grupos de dispositivos:** la aplicación solo se distribuye a los dispositivos o grupos de dispositivos que usted elija.Haga clic en la pestaña **Dispositivos** para seleccionar el o los dispositivos.Haga clic en la pestaña **Grupos de dispositivos** para seleccionar los grupos de dispositivos.
7. Haga clic en **Siguiente**.

### Configurar opciones de instalación

Puede seleccionar las opciones de configuración de la instalación.

**Procedimiento**

1. Haga clic en **Ajustes de instalación de la configuración de la aplicación** o haga clic en el icono **+** para añadir otra configuración para ver la página **Establecimiento de la configuración**.
2. Introduzca un nombre para la configuración en el campo **Nombre**.
3. Opcionalmente, puede añadir una breve descripción de la configuración de la instalación en el campo **Descripción**.
4. Seleccione la opción **Configuración de instalación del dispositivo**.
5. Seleccione una de las siguientes opciones:\* **Requerir instalación en el dispositivo**
   - **Instalar solo en el momento del registro del dispositivo**
6. Seleccione la opción **No requerir una versión específica de la aplicación** para evitar degradar una aplicación ya instalada a una versión inferior. Esta opción solo está disponible para las aplicaciones modernas.
7. Seleccione las siguientes opciones:1) - **Instalar de forma silenciosa en el espacio de trabajo Samsung Knox y en dispositivos Zebra** (solo Android)
   - **No mostrar la aplicación en el Catálogo de aplicaciones del usuario final**.
   - **No instale la aplicación en dispositivos recién inscritos**: los dispositivos existentes no se verán afectados y seguirán mostrando la aplicación en el catálogo de aplicaciones del dispositivo.\* Para cualquier dispositivo recién inscrito en esta distribución, la aplicación no aparecerá en la lista ni se enviará.
     - Si el administrador activa un comando de envío de instalación/actualización, el comando se enviará al dispositivo.
   - **Modo de actualización de aplicaciones** (compatible también con dispositivos AMAPI). (Solo Android)Utilice esta opción para actualizar una aplicación a la última versión utilizando uno de los tres modos siguientes:- **Predeterminado**: se selecciona este modo una vez que selecciona la opción Modo de actualización de la aplicación. En este modo, la actualización se produce en un plazo de 24 horas desde que empieza a estar disponible la aplicación.- **Posponer 90 días:** si selecciona este modo de actualización, puede posponer las actualizaciones de la aplicación durante 90 días. Después de 90 días, las aplicaciones se actualizan automáticamente en función de otros ajustes realizados en la configuración de Google Play administrada.\* **Alta prioridad**: si selecciona este modo de actualización y el dispositivo del usuario está conectado, la aplicación se actualiza inmediatamente una vez que esté disponible en la Google Play Store.
   - **Establezca la prioridad de instalación de la aplicación**: consulte el tema Configuración de la prioridad de la aplicación para obtener más información.
8. En los dispositivos Android, las actualizaciones de las aplicaciones se permiten mediante la opción Actualización automática, incluso sin seleccionar la opción Instalación en segundo plano. El administrador puede controlar las actualizaciones de las aplicaciones que no son obligatorias o de las aplicaciones autoinstaladas por el usuario.
   Es posible que se encuentre con opciones adicionales de configuración, dependiendo de la aplicación que elija. Estas opciones pueden incluir la posibilidad de añadir múltiples pares de clave y valor. En dichos casos, haga clic en **+ Añadir** para introducir los pares clave/valor. Para obtener más información, consulte **Agregar una aplicación desde un almacén público** de [**Catálogo de aplicaciones**](./Catálogo_de_aplicaciones.md).
9. (macOS 11+) Seleccione las opciones para instalar y configurar las aplicaciones como aplicaciones gestionadas:\* **Instalar como aplicación administrada**
   - **Convertir en Aplicación administrada**En macOS 12.0+, la compatibilidad con Managed App está disponible en los dispositivos inscritos por el usuario.

## Ocultar o suspender aplicaciones (solo Android)

Para dispositivos Android en los siguientes modos: **perfil de trabajo**, **dispositivo completamente gestionado**, **dispositivo completamente gestionado con perfil de trabajo** y **perfil de trabajo en dispositivo propiedad de la empresa**, ahora es posible ocultar o suspender aplicaciones después de la instalación.

**Procedimiento**

|   | 1. | Instale una o más aplicaciones en el dispositivo para el que desee aplicar la acción Ocultar o Suspender. |
| - | -- | --------------------------------------------------------------------------------------------------------- |

|   | 2. | Crear una configuración de App Control y agregar las aplicaciones gestionadas a la lista Ocultar o Suspender. |
| - | -- | ------------------------------------------------------------------------------------------------------------- |

|   | 3. | Aplicar los cambios al dispositivo. |
| - | -- | ----------------------------------- |

Si una aplicación está presente tanto en la lista de Ocultar como en la lista de Suspender, entonces la aplicación será ocultada, ya que la lista de Ocultar tendrá prioridad.

### Configurar la prioridad de la aplicación

Se puede definir el orden en que se reciben las aplicaciones en el dispositivo cuando se registra por primera vez (concretamente, dentro de los primeros 20 minutos después de la fecha y hora de registro) y se insertan las aplicaciones necesarias para instalarlas. Puede priorizar la descarga de aplicaciones específicas antes que otras aplicaciones. Por ejemplo, se puede priorizar la descarga de las aplicaciones Tunnel y Email antes que otras aplicaciones no tan importantes. Esta función es aplicable tanto a las aplicaciones públicas como privadas. Las aplicaciones con requisitos previos se insertan antes que las aplicaciones dependientes.

Esta función es compatible con dispositivos iOS (excepto AppStation para iOS), Android (excepto Android para empresas), macOS (aplicaciones PKG internas y aplicaciones Apple Apps y Books) y Windows.

Esta función está disponible para los nuevos dispositivos de registro. Por defecto, todas las aplicaciones tienen prioridad Media. Durante este proceso, el usuario puede seleccionar instalar manualmente cualquier aplicación del catálogo, aunque esa aplicación competirá por los recursos para instalarse y puede ponerse en cola antes que las aplicaciones de alta prioridad.

En cuanto a las aplicaciones de Windows, la aplicación Bridge tiene mayor prioridad que las demás aplicaciones.

Consulte la sección anterior, «Configurar opciones de instalación» para conocer el procedimiento para establecer la prioridad de una aplicación mediante la opción **Establecer la prioridad de instalación de las aplicaciones**. Puede establecer una prioridad Alta, Media o Baja para una aplicación. Las aplicaciones con la misma prioridad se instalarán sin ningún orden en particular. La prioridad de las aplicaciones no se utiliza durante las actualizaciones de la aplicación, cuando el usuario ya tiene la aplicación instalada.

### Seleccionar los ajustes de configuración de Administración de aplicaciones de Apple

estos ajustes se aplicarán únicamente a esta aplicación e invalidará cualquier ajuste global seleccionado en **Aplicaciones > Ajustes del catálogo**. Para seleccionar los ajustes de **Administración de aplicaciones de Apple**:

**Procedimiento**

1. Haga clic en **Ajustes de aplicaciones Apple** o haga clic en el icono **+** para añadir otra configuración para ver la página **Ajustes de la configuración**.
2. Introduzca un nombre para la configuración en el campo **Nombre**.
3. Introduzca una breve descripción para la configuración en el campo **Descripción**.
4. Seleccione o cancele la selección de una o más de la siguientes opciones de los **Ajustes de administración de Apple**:\* **Impedir la copia de seguridad de iCloud e iTunes**
   - **Eliminar aplicaciones dadas de baja**
   - (iOS 14.0+) **Permitir la eliminación y descarga de esta aplicación**: puede anular la selección de esta opción para evitar que un usuario elimine o descargue una aplicación administrada.
   - (Opcional) Agregue una **Configuración de la aplicación administrada Apple**
5. Haga clic en **Actualizar**.

### Seleccionar niveles de promoción de aplicaciones

Puede establecer el nivel de promoción de la aplicación.

**Procedimiento**

1. Haga clic en **Ajustes de configuración de la distribución de promociones** o haga clic en el icono **+** para añadir otra configuración para ver la página **Configuración de promociones**.
2. Haga clic en **Editar**.
3. Introduzca un nombre para los ajustes de configuración de la distribución de promociones en el campo **Nombre**.
4. Opcionalmente, puede añadir una breve descripción de la configuración en el campo **Descripción**.
5. Seleccione el nivel de promoción que desea que reciba la aplicación: **No destacada**, **Lista destacada** o use un **Banner destacado**. Si elige la opción **No destacada**, la aplicación no aparecerá en la lista.
6. Si selecciona Banner destacado especifique los siguientes detalles:1) **Título**: especifique el título de la aplicación
   2\) **Descripción**: especifique los detalles de la aplicación
   3\) **Estilo de banner**: seleccione un color de banner
7. Haga clic en **+ Añadir descripción** para introducir una breve descripción de la configuración.
8. Opcionalmente, puede cambiar la distribución de la configuración.
9. Haga clic en **Hecho** para guardar la configuración de la aplicación.

### Configurar reglas de tráfico de AppTunnel

Use la configuración de AppTunnel para definir las reglas de tráfico con el fin de permitir el acceso a los servicios usando Sentry:

Para obtener información acerca de cómo añadir una configuración de AppTunnel, consulte en “Cómo añadir una configuración de AppTunnel” en la *Guía de AppConnect para Ivanti Neurons for MDM*.

### Configuración de una aplicación administrada

**Procedimiento**

1. Haga clic en el icono **+** para abrir la página de configuración.
2. Haga clic en **+ Añadir descripción** para introducir una breve descripción de la configuración.
3. Haga clic en **+ Añadir** para introducir una clave y un valor.
4. Elija un nivel de distribución.
5. Haga clic en **Siguiente**.

### Configurar una VPN para cada aplicación utilizando la VPN por aplicación

**Procedimiento**

1. Haga clic en el icono **+** para abrir la página de configuración.
2. Introduzca un nombre para la VPN de esta aplicación en el campo **Nombre**.
3. Haga clic en **+ Añadir descripción** para introducir una breve descripción de la configuración.
4. Haga clic en la opción **Activar VPN por aplicación para esta aplicación** y seleccione una configuración de VPN por aplicación disponible.
5. (Opcional) Para las aplicaciones de macOS, introduzca la cadena **Requisito designado** en el formato, identificador "\\%s\\". Por ejemplo, el identificador «com.google.Chrome». Use este campo para habilitar una aplicación de paquete múltiple de macOS para usar una VPN por aplicación como Tunnel.
6. Elija cómo **Distribuir la configuración de esta aplicación**.
7. Haga clic en **Siguiente**.

### Uso de la configuración de la aplicación administrada Apple

Mediante la configuración de la aplicación administrada Apple, se pueden configurar ajustes específicos para la aplicación administrada instalada. Es posible que la aplicación tenga algunos parámetros de la configuración implementados o restringidos por el desarrollador. En aplicaciones con dichas restricciones, puede ocurrir que las opciones de configuración sea limitadas. Puede configurar las aplicaciones administradas de Apple.

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione una aplicación.
3. Haga clic en la pestaña **Configuraciones de la aplicación**.
4. Haga clic en **Configuración de la aplicación administrada Apple** o haga clic en el botón **+**.En la Configuración de la aplicación administrada Apple, ya existen algunos ajustes predeterminados de la configuración.
5. Haga clic en **Añadir** para añadir otra configuración, si fuera necesario. Opcionalmente, haga clic en el nombre de la configuración para editar la configuración.
6. En **Fuente de configuración**, seleccione cualquiera de las opciones de **Tipo de fuente**.\* **Comunidad de AppConfig**: esta opción está disponible solo para aquellas aplicaciones que tienen una especificación de la configuración de la aplicación disponible en el repositorio de la comunidad. Si esta opción está disponible, aparece seleccionada de forma predeterminada.
   - **Usar especificación .xml**&#xNAN;**:** seleccione esta opción para subir el esquema de la aplicación para insertar una versión concreta de la configuración de la aplicación. Haga clic en **Seleccionar archivo** para cargar el archivo .xml. Asegúrese de que el archivo .xml contenga la Id. y la versión del paquete. Se mostrará un mensaje de error si la Id. del paquete del archivo no coincide con la Id. del paquete de la aplicación.
   - **Ninguno**: seleccione esta opción si no desea aplicar ningún esquema para la aplicación. Esta opción está seleccionada de forma predeterminada si la opción **Comunidad de AppConfig** no está disponible.El archivo .xml cargado aparece en la sección **Fuente de configuración**. Haga clic en el icono Eliminar para borrar el archivo .xml cargado.
7. En los **Ajustes de la aplicación administrada Apple**, puede configurar las opciones de configuración para introducir pares de valores clave.- Haga clic en **Añadir** para agregar los siguientes pares de valores clave a la configuración de aplicaciones administradas para recuperar la identidad del nombre de registro por parte del cliente Go durante iReg o la Inscripción de dispositivos de Apple.Puede seleccionar los tipos de datos (String, Integer, Boolean, Long Float, Double, Date, String Array, Integer Array, Double Array, Float Array, Long Array) para los pares de valor-clave.Añada los siguientes pares de valores clave a la configuración de aplicaciones administradas para recuperar la identidad del nombre de registro por parte del cliente Go durante iReg o la Inscripción de dispositivos de Apple:

| **Clave**                                                                                                                                                                                                                               | **Valor**                                                 | **Tipo**          |                                                                                                                                                                                                                                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| registration.username                                                                                                                                                                                                                   | $\{userEmailAddress}                                      | CADENA            |                                                                                                                                                                                                                                                                                                                                       |
| registration.token                                                                                                                                                                                                                      | $\{zeroTouchClientRegistrationNonce}                      | STRING            |                                                                                                                                                                                                                                                                                                                                       |
| registration.token.expirationSeconds                                                                                                                                                                                                    | $\{zeroTouchClientRegistrationNonceExpiresAtSeconds}      | CADENA            |                                                                                                                                                                                                                                                                                                                                       |
| registration.url                                                                                                                                                                                                                        | $\{clientRegistrationUrl}                                 | CADENA            |                                                                                                                                                                                                                                                                                                                                       |
| Añada los siguientes pares de valores clave a la configuración de la aplicación gestionada para recuperar la identidad del nombre de registro por parte del agente mac (Mobile\@Work) durante iReg o Inscripción de dispositivos Apple: |                                                           |                   |                                                                                                                                                                                                                                                                                                                                       |
| **Clave**                                                                                                                                                                                                                               | **Valor**                                                 | **Tipo**          |                                                                                                                                                                                                                                                                                                                                       |
| ---------------------                                                                                                                                                                                                                   | --------------------------------------------------------- | --------          |                                                                                                                                                                                                                                                                                                                                       |
| ClientRegistrationUrl                                                                                                                                                                                                                   | $\{clientRegistrationUrl}                                 | CADENA            |                                                                                                                                                                                                                                                                                                                                       |
| Token                                                                                                                                                                                                                                   | $\{zeroTouchMacOSClientRegistrationNonce}                 | CADENA            |                                                                                                                                                                                                                                                                                                                                       |
| TokenExpiresAt                                                                                                                                                                                                                          | $\{zeroTouchMacOSClientRegistrationNonceExpiresAtSeconds} | CADENA            |                                                                                                                                                                                                                                                                                                                                       |
| Si el usuario final finaliza la aplicación Ivanti Go, haga clic en **Editar** para configurar la aplicación para que realice una de las siguientes acciones:                                                                            |                                                           |                   |                                                                                                                                                                                                                                                                                                                                       |
| Clave                                                                                                                                                                                                                                   | Valor                                                     | Tipo              |                                                                                                                                                                                                                                                                                                                                       |
| ---------------------------------------------------------------------------                                                                                                                                                             | ----------------------------                              | ----------------- |                                                                                                                                                                                                                                                                                                                                       |
| Para mostrar la notificación por defecto utilice los siguientes valores:                                                                                                                                                                |                                                           |                   |                                                                                                                                                                                                                                                                                                                                       |
| enableAppTerminationNotification                                                                                                                                                                                                        | Cierto/Falso O 1/0                                        | Booleano O Cadena |                                                                                                                                                                                                                                                                                                                                       |
| Para Mostrar una notificación personalizada utilice los siguientes valores:                                                                                                                                                             |                                                           |                   |                                                                                                                                                                                                                                                                                                                                       |
| appTerminationNotificationMessage                                                                                                                                                                                                       | Notificaciones personaizadas                              | Cadena            |                                                                                                                                                                                                                                                                                                                                       |
| enableAppTerminationNotification                                                                                                                                                                                                        | Cierto/Falso O 1/0                                        | Booleano O Cadena | \* **Usar .plist**:los archivos .plist contienen múltiples pares de valores clave para cargarse en masa. Haga clic en **Seleccionar archivo** para cargar el archivo .plist. Los datos .plist validados se mostrarán en la tabla **Ajustes de la aplicación administrada Apple**.Las plists con diccionarios anidados no son válidas. |

8. Haga clic en **Actualizar** para guardar los cambios.

## Configuración del relé de red

Para que el tráfico de red de su aplicación sea más privado y seguro sin conectarse a una VPN. Para más información, consulte [**Configuración del relé de red**](./Configuración_del_relé_de_red.md).

1. Haga clic en el icono **+ Relé de red** para abrir la página de configuración.
2. Introduzca un nombre para el **Relé de red** de esta aplicación en el campo Nombre.
3. Haga clic en + **Añadir descripción** para introducir una breve descripción de la configuración.
4. Haga clic en la opción **Activar relé de red** de esta aplicación y seleccione una configuración disponible de **Relé de red**.
5. Elija cómo **Distribuir** la configuración de esta aplicación.
6. Haga clic en **Siguiente**.

## Configuración de la segmentación celular 5G

La compatibilidad de la segmentación de red 5G móvil permite que las aplicaciones gestionadas individualmente se asignen a una segmentación de red que proporciona una capacidad y características de red específicas para optimizar la experiencia de la aplicación. La asignación se realiza mediante el nuevo atributo de aplicación **CellularSliceUUID** en el comando de instalación de la aplicación MDM o en la configuración declarativa de la aplicación. El valor de la cadena de la porción de red que debe introducirse en la clave lo debe proporcionar el operador de soporte.

La segmentación de la red 5G no se utilizará si la aplicación específica o todo el dispositivo están configurados para utilizar una VPN.

ProcedureProcedimiento

1. Vaya a **Aplicaciones > Catálogo de aplicaciones > Configuración de aplicaciones >****Segmentación 5G móvil** y haga clic en **Agregar**.
2. En la **Ajuste de la configuración**, actualice los siguientes campos:\* Nombre
   - Seleccione la opción **Habilitar la segmentación de red 5G**
   - Elija la categoría de aplicación **DNN** o **Categoría de aplicación** (según el proveedor de red)
3. Elija un nivel de distribución para la configuración de la aplicación:
4. Haga clic en **Guardar**.

## Distribución de aplicaciones mediante la configuración del filtro de contenidos web

Puede utilizar la configuración del Filtro de contenido web para distribuir una aplicación en lugar de un servidor proxy DNS. Después de crear la configuración del Filtro de Contenido Web, puede añadir la configuración a una aplicación para su distribución. Para obtener más información sobre la configuración del Filtro de contenido Web, consulte [**Filtro de contenido web**](./Filtro_de_contenido_web.md).

**Procedimiento**

1. Vaya a **Aplicaciones** > **Catálogo de aplicaciones**.
2. Seleccione una aplicación.
3. Haga clic en **Siguiente**.
4. Seleccione la opción de delegación y haga clic en **Siguiente**.
5. Seleccione las opciones de distribución y haga clic en **Siguiente**.
6. Seleccione **Configuración del filtro de contenidos web** y haga clic en el icono **+**.
7. Especifique el **Nombre**.
8. Seleccione la casilla **Habilitar filtro de contenido web para esta aplicación**.
9. Seleccione el filtro de contenido web en el menú desplegable.
10. Elija un nivel de distribución para la configuración de la aplicación:1) **Para todo el mundo:** la aplicación se añade a los dispositivos compatibles de todos los usuarios.
    2\) **A nadie:** la aplicación se almacena para distribuirse posteriormente.
    3\) **Distribución personalizada**: seleccione cualquiera de las siguientes opciones:\* **Usuarios/Grupos de usuarios**: la aplicación solo se distribuye a los usuarios o grupos de usuarios que usted elija.Haga clic en la pestaña **Usuarios** para seleccionar los usuarios.Haga clic en la pestaña **Grupos de usuarios** para seleccionar los grupos de usuarios.
    - **Dispositivos/Grupos de dispositivos:** la aplicación solo se distribuye a los dispositivos o grupos de dispositivos que usted elija.Haga clic en la pestaña **Dispositivos** para seleccionar el o los dispositivos.Haga clic en la pestaña **Grupos de dispositivos** para seleccionar los grupos de dispositivos.
11. Haga clic en **Siguiente**.
12. Haga clic en **Hecho**. La aplicación seleccionada se distribuye a los usuarios específicos a través de la configuración del Filtro de Contenido Web.

## Distribución de aplicaciones mediante proxy DNS

Puede utilizar la configuración del proxy DNS para distribuir la aplicación. Después de crear la configuración del proxy DNS, puede añadir la configuración a una aplicación para su distribución. Para obtener más información sobre la configuración del proxy DNS, consulte [**Creación de una configuración de proxy de DNS**](./Creación_de_una_configuración_de_proxy_de_DNS.md).

**Procedimiento**

1. Vaya a **Aplicaciones** > **Catálogo de aplicaciones**.
2. Seleccione una aplicación.
3. Haga clic en **Siguiente**.
4. Seleccione la opción de delegación y haga clic en **Siguiente**.
5. Seleccione las opciones de distribución y haga clic en **Siguiente**.
6. Seleccione **Configuración del Proxy DNS** y haga clic en el icono **+**.
7. Especifique el **Nombre**.
8. Marque la casilla **Habilitar Proxy DNS para esta aplicación**.
9. Seleccione Proxy DNS en el menú desplegable.
10. Elija un nivel de distribución para la configuración de la aplicación:1) **Para todo el mundo:** la aplicación se añade a los dispositivos compatibles de todos los usuarios.
    2\) **A nadie:** la aplicación se almacena para distribuirse posteriormente.
    3\) **Distribución personalizada**: seleccione cualquiera de las siguientes opciones:\* **Usuarios/Grupos de usuarios**: la aplicación solo se distribuye a los usuarios o grupos de usuarios que usted elija.Haga clic en la pestaña **Usuarios** para seleccionar los usuarios.Haga clic en la pestaña **Grupos de usuarios** para seleccionar los grupos de usuarios.
    - **Dispositivos/Grupos de dispositivos:** la aplicación solo se distribuye a los dispositivos o grupos de dispositivos que usted elija.Haga clic en la pestaña **Dispositivos** para seleccionar el o los dispositivos.Haga clic en la pestaña **Grupos de dispositivos** para seleccionar los grupos de dispositivos.
11. Haga clic en **Siguiente**.
12. Haga clic en **Hecho**. La aplicación seleccionada se distribuye a los usuarios específicos a través de la configuración del Proxy DNS.

### Ajustes de Clonar la configuración de una aplicación

Puede clonar los Ajustes de configuración de una aplicación administrada para que los mismos ajustes se puedan aplicar en otros dispositivos. Incluso puede cambiar el nombre y realizar algunos cambios en los ajustes clonados.

**Android**

Puede clonar los Ajustes de configuración en dispositivos Android.

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione una aplicación desde la que desee clonar los ajustes de configuración.
3. Haga clic en **Configuraciones de aplicaciones**.
4. En la sección **Resumen de configuraciones de aplicaciones**, encontrará la lista de configuraciones (**Configuraciones administradas para Android**, **Instalar en el dispositivo**, **Promoción**, **Permisos delegados del dispositivo** y **Versión de Google Play**) disponible para dispositivos de Android.
5. Haga clic en cualquiera de las configuraciones disponibles.
6. En **Acciones**, haga clic en **Clonar** para iniciar el proceso de clonación.
7. Por defecto, el nombre de la configuración clonada será \<Copy of the Cloned Configuration name>. No obstante, puede modificar el nombre si introduce un nombre e su elección en el cuadro **Nombre**.
8. (Opcional) Introduzca algún texto sobre los ajustes clonados en el cuadro **Descripción**.
9. Haga clic en **Continuar**.

Aparece una ventana de confirmación que indica que se ha completado la clonación de los ajustes de configuración de la aplicación. Puede ver la versión clonada en el Resumen de configuración de aplicaciones y en la aplicación clonada.

**iOS**

Puede clonar los Ajustes de configuración de aplicaciones administradas en dispositivos iOS.

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione una aplicación desde la que desee clonar los ajustes de configuración.
3. Haga clic en **Configuraciones de aplicaciones**.
4. En la sección **Resumen de configuraciones de aplicaciones**, encontrará la lista de configuraciones (**Instalar en el dispositivo**, **Ajustes de aplicaciones de Apple**, **Promoción**, **Configuración personalizada de AppConnect**, **Túnel de aplicaciones**, **Configuración de aplicaciones administradas de Apple** y **VPN por aplicación**) disponibles para dispositivos de iOS.
5. Haga clic en la configuración requerida que desee clonar.
6. En **Acciones**, haga clic en **Clonar** para iniciar el proceso de clonación.
7. Por defecto, el nombre de la configuración clonada será \<Copy of the Cloned Configuration name>. No obstante, puede modificar el nombre si introduce un nombre e su elección en el cuadro **Nombre**.
8. (Opcional) Introduzca algún texto sobre los ajustes clonados en el cuadro **Descripción**.
9. Seleccione una fuente de configuración de la lista **Tipo de fuente**.
10. En la sección **Ajustes de aplicaciones administradas de Apple**, introduzca **Clave**, **Valor** y seleccione **Tipo** en la lista.Para obtener información sobre **Clave**, **Valor** y **Tipo**, consulte **Uso de la configuración de aplicaciones administradas de Apple**.
11. Haga clic en **Continuar**.Aparece una ventana de confirmación que indica que se ha completado la clonación de los ajustes de configuración de la aplicación. Puede ver la versión clonada en la sección **Configuración de aplicaciones administradas de Apple**.

**Windows**

Puede clonar los Ajustes de configuración de aplicaciones en dispositivos Windows. 

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione una aplicación desde la que desee clonar los ajustes de configuración.
3. Haga clic en **Configuraciones de aplicaciones**.
4. En la sección **Resumen de configuraciones de aplicaciones**, encontrará la configuración de **Instalar en el dispositivo** y **Promoción**.
5. Haga clic en la configuración requerida que desee clonar.
6. En **Acciones**, haga clic en **Clonar** para iniciar el proceso de clonación.
7. Por defecto, el nombre de la configuración clonada será \<Copy of the Cloned Configuration name>. No obstante, puede modificar el nombre si introduce un nombre e su elección en el cuadro **Nombre**.
8. (Opcional) Introduzca algún texto sobre los ajustes clonados en el cuadro **Descripción**.
9. Haga clic en **Continuar**.

Aparece una ventana de confirmación que indica que se ha completado la clonación de los ajustes de configuración de la aplicación. Puede ver la versión clonada en el Resumen de configuración de aplicaciones y en la aplicación clonada.

### Elegir las aplicaciones de Windows 10 para su catálogo interno

Elija las aplicaciones que va a añadir a su catálogo de aplicaciones internas. Las aplicaciones internas, de Microsoft Store y de Microsoft for Business son compatibles con Windows 10. Windows 10 implementa el cumplimiento directamente en el dispositivo de acuerdo con las aplicaciones que decida permitir o no permitir.

El intervalo de ingresos predeterminado de Windows 10 es de una vez cada 60 minutos. Es recomendable realizar un ingreso forzado del dispositivo para obtener una actualización del estado del dispositivo y la aplicación.

Se admiten las siguientes acciones:

- Cargar nuevas aplicaciones
- Instalación silenciosa
- Instalar manualmente desde Apps\@Work
- Añadir una versión nueva de la aplicación
- Eliminar una aplicación

Se admiten los siguientes formatos:

- APPX
- APPXBUNDLE
- Win32 ajustado en MSI - aplicación Win32 previamente empaquetada
- MSIX (compatible con dispositivos RS5 y posteriores a Windows 10)
- .EXE (con bridge)

La aplicación **Ivanti Neurons Agent** está disponible en el **Catálogo de aplicaciones** de dispositivos **Windows**. El administrador puede desplegar la aplicación **Ivanti Neurons Agent** como una aplicación interna y esta aplicación se puede distribuir de igual manera en los dispositivos Windows.

### Configurar aplicaciones de Windows 10

**Procedimiento**

1. Haga clic en **Dispositivos** en la barra de navegación principal.
2. Seleccione un dispositivo Windows 10 con el que se haya inscrito en Ivanti Neurons for MDM.
3. Haga clic en **Aplicaciones > Catálogo de aplicaciones**.
4. Seleccione una aplicación.
5. Utilice el menú desplegable **Acciones** para añadir la aplicación o eliminarla de su catálogo.Opcionalmente, también puede añadir una versión nueva de la aplicación.\* Haga clic en el menú desplegable **Acciones**.
   - Seleccione **Añadir nueva versión**.
   - Vaya el catálogo y seleccione una nueva versión de la aplicación.
   - Haga clic en **Actualizar y guardar** para ver la pantalla de información de la aplicación.
6. Utilice el menú desplegable **Versión** para elegir qué versión desea utilizar.
7. Haga clic en **Editar** para comenzar a modificar los detalles.\* Edite la **Categoría**, si fuera necesario.
   - Ingrese una **Descripción**, si fuera necesario.
   - Añada capturas de pantalla si fuera necesario.
8. Haga clic en **Guardar**.
9. Haga clic en la pestaña **Distribución** y luego en **Editar** para comenzar a modificar el nivel de distribución.
10. Haga clic en **Guardar**.
11. Haga clic en la pestaña **Configuraciones de aplicaciones** para ver un resumen de la configuración actual.
12. Introduzca, si fuera necesario, una descripción de la aplicación.
13. Haga clic en **Instalar en el dispositivo** en la página de resumen de Configuraciones de aplicaciones.El valor predeterminado es la instalación silenciosa y no puede modificarse
14. Haga clic en **Promoción** en el panel de navegación de la izquierda y, luego, haga clic en **Ajustes de configuración de distribución de promoción** para cambiar el nivel de promoción.\* Haga clic en **Editar** para comenzar a modificar los ajustes del nivel de promoción.
    - Introduzca un nombre para la configuración.
    - Introduzca una descripción para la configuración.
    - Seleccione un nivel de promoción.
    - Haga clic en **Actualizar** para guardar los cambios.
15. Haga clic en la pestaña **Opiniones** para ver información sobre las opiniones.Exporte, si fuera necesario, los datos de las opiniones a una hoja de cálculo.

### Editar los ajustes de configuración de aplicaciones de Windows 10

**Procedimiento**

1. Haga clic e&#x6E;**&#x20;Políticas > Configuración**.
2. Haga clic en **+Agregar**.
3. Seleccione **Control de aplicaciones de Windows** para ver la pantalla **Crear configuración de control de aplicaciones de Windows**.
4. Ingrese un **Nombre** y una **Descripción** para la configuración.
5. Defina el tipo de aplicación del siguiente modo:\* Permitidas (en la lista de permitidos) - solo se permiten estas aplicaciones. Estas aplicaciones se instalan de forma silenciosa si no están ya presentes en el dispositivo.
   - No permitidas (en la lista de bloqueados) - si están presentes en el dispositivo, estas aplicaciones se bloquearán cuando se inicien.
6. Especifique las definiciones de Reglas para el Tipo de aplicación e Identificador de aplicaciones.
7. Haga clic en **Buscar aplicaciones** para ver la pantalla **Buscar aplicaciones de Windows 10**.
8. Introduzca el nombre de la aplicación que desea buscar en la Windows Store.
9. Seleccione la aplicación de entre las opciones mostradas para añadirla al Identificador de aplicaciones.
10. Opcionalmente, también puede usar el menú desplegable «Tipo de aplicación» para definir una ruta en el identificador de aplicaciones con el fin de permitir o no permitir ciertas aplicaciones utilizando dicha ruta especificada o para bloquear todas las aplicaciones instaladas en dicha ruta.El tipo de aplicación **Editor/Iguales PFN** se aplica a dispositivos Windows 10+ y admite PFN. **EXE/Win32 es igual a**.
11. Haga clic en **Siguiente**.
12. Elija un nivel de distribución.\* **Todos los dispositivos**.
    - **No hay dispositivos**.
    - **Personalizado** - para introducir los usuarios o grupos que recibirán la aplicación.
13. Haga clic en **Listo**.
14. Puede editar las definiciones de Regla para seleccionar un Tipo de aplicación y especificar el Identificador de aplicaciones.\* Haga clic en el menú desplegable **Acciones**.
    - Seleccione **Añadir nueva versión**.
    - Seleccione una versión nueva de la aplicación.
    - Haga clic en **Actualizar y guardar** para ver la pantalla de **información de la aplicación**.

### Configuración de Reiniciar dispositivo después de la opción de instalación de Windows.

Puede configurar un dispositivo para que se reinicie después de instalar una aplicación mediante la opción **Reiniciar dispositivo tras la instalación**.

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione cualquier aplicación específica de Windows en la lista.
3. Vaya a **Configuración de aplicaciones > Instalar en dispositivo > Instalar el ajuste de configuración de la aplicación**.
4. Haga clic en **Editar** y ajuste la opción de **Reiniciar el dispositivo tras la instalación** como ACTIVO.
5. Seleccione una de las siguientes opciones de programación en la que desea reiniciar el dispositivo:| **Ajuste**                          | **Qué hacer**                                                                                                                    |
   \| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
   \| **Justo después de la instalación** | Seleccione esta opción para reiniciar el dispositivo poco después de instalar la aplicación.                                     |
   \| **A determinadas horas del día**    | Seleccione esta opción para reiniciar el dispositivo a una hora específica después de instalar la aplicación.                    |
   \| **Tras unos minutos**               | Seleccione esta opción para reiniciar el dispositivo **15**, **30**, **60** o **120** minutos después de instalar la aplicación. |
6. Haga clic en **Actualizar**.El dispositivo se reiniciará a la hora programada.

En el caso de las aplicaciones públicas y de las aplicaciones de Microsoft Store for Business (MSB), debe establecer el ajuste **Instalar silenciosamente en dispositivos de Windows** como ACTIVO desde la sección **Configuración de aplicaciones**.

### Instalación de aplicaciones con Apps\@Work

Para instalar una aplicación usando Apps\@Work:

1. Haga clic en la aplicación **Apps\@Work**.La dirección de correo electrónico y la URL del servidor de su administrador está previamente rellenadas en el diálogo de inicio de sesión de Apps\@Work.
2. Introduzca su contraseña y haga clic en «Iniciar sesión» para mostrar la página de las aplicaciones.
3. Seleccione una aplicación para instalarla. No podrá instalar aplicaciones con dependencias en aplicaciones con requisitos previos si estas últimas aplicaciones no están ya instaladas en el cliente.Para Apps\@Work en dispositivos iOS, también tiene la opción de hacer clic en el botón **Instalar todo** para instalar todas las aplicaciones. Esta opción está disponible en las pantallas **Nuevos lanzamientos**, **Aplicaciones destacadas** y **Categorías**.las aplicaciones de Apps and Books no se instalarán si no se acepta previamente la licencia de la aplicación Apps and Books.
4. Haga clic en **Actualizar y guardar** para ver la pantalla de **información de la aplicación**.

### Instalación de aplicaciones y actualizaciones para dispositivos de Android Enterprise

Los administradores pueden publicar una aplicación en el catálogo para acceso general y, al mismo tiempo, implementarla en un dispositivo específico para su uso inmediato. Esto permite a los usuarios recibir la aplicación directamente, mientras esta sigue estando disponible en el catálogo para que otros la instalen según sea necesario.

Para instalar aplicaciones y actualizaciones

1. Vaya a **Aplicaciones > Apps Catalog**.
2. Elija la aplicación que desea.
3. Haga clic en **Acciones** en la pantalla **Detalles**. Se muestra la opción **Enviar solicitud de instalación/actualización**.
4. Haga clic en Enviar solicitud de instalación/actualización. Se muestra el cuadro de diálogo **Enviar solicitud de instalación/actualización**.
5. Lleve a cabo la acción siguiente de **Enviar notificaciones de instalar y actualizar a los dispositivos de esta aplicación**:\* Seleccione la casilla **Enviar solicitud para aplicación nueva (se aplica a los dispositivos que aún no tienen instalada la aplicación)** para instalar la aplicación nueva.
   - Seleccione la casilla **Enviar solicitud para actualizaciones (aplicable a dispositivos que tienen la aplicación instalada pero está disponible una actualización)** para actualizar una aplicación instalada.
6. Lleve a cabo la siguiente acción en **Seleccionar usuarios para enviar solicitudes**:\* Haga clic en **Todos** para distribuir la configuración a todos los usuarios compatibles. La aplicación aparece en su App Catalog.
   - Haga clic en **Personalizado** para definir el grupo de usuarios o el usuario que verá la aplicación en App Catalog.La distribución Enviar solicitud de instalación/actualización\* forma parte del proceso de distribución de aplicaciones.La configuración que elijas en la pantalla **Distribución** determinará qué dispositivos recibirán la aplicación.

Aparece una ventana de confirmación que indica que se ha completado la instalación de la aplicación.

Los cambios de nuevas instalaciones o actualizaciones se muestran en **Tablero de resultados** > **Audit Trails**.

Para aplicaciones públicas y privadas, la opción **Enviar solicitud para actualizaciones (aplicable a dispositivos que tienen la aplicación instalada pero está disponible una actualización)** se encuentra deshabilitada. Solo se permiten solicitudes de **Enviar solicitud para una nueva aplicación**.

**Temas relacionados:**
