---
title: Configuración de la transferencia de archivos de Android
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

Como parte de Android 11, Google introdujo cambios significativos en el acceso al almacenamiento en un dispositivo desde las aplicaciones, lo que también afectó a la forma en que las empresas gestionan el envío de archivos a aplicaciones específicas en estos dispositivos. Teniendo en cuenta estos cambios, muchas grandes empresas se enfrentan a retos a la hora de distribuir archivos a dispositivos y aplicaciones a medida que los dispositivos se actualizan a Android 11 y versiones posteriores. Cualquier enfoque que dependa de API específicas de los proveedores de hardware limita a las empresas a la hora de tener el mismo enfoque en diferentes dispositivos de distintos fabricantes y versiones de SO.

Ivanti ha desarrollado una solución de transferencia de archivos que es agnóstica para la versión de Android y el proveedor de hardware. Esta solución se basa en la capacidad estándar de Android *Content-Provider* . *Content-Provider* permite a la aplicación Go de Ivanti generar una ubicación única en el dispositivo para cada archivo enviado a través de UEM.

La configuración de transferencia de archivos está disponible para dispositivos de Android en modo de dispositivo totalmente gestionado. Mediante esta configuración, el administrador puede proporcionar una opción para transferir archivos en el dispositivo para ser compartidos entre diferentes aplicaciones permitidas presentes en el mismo dispositivo. Otras aplicaciones pueden utilizar los archivos para lo que necesiten. Un ejemplo de uso es inicializar la configuración de la aplicación mediante JavaScript o mostrar información corporativa mediante PDF o vídeos. Cada archivo cargado en las configuraciones de transferencia de archivos de Ivanti es descargado por Ivanti Go cuando recibe la configuración correspondiente y el archivo asociado. El archivo se almacena de forma segura en Ivanti Go.

Otras aplicaciones no pueden acceder a este archivo de manera arbitraria.

Cada archivo descargado dentro del sandbox de la aplicación está referenciado por una ubicación única, también denominada *ContentURI* o *URI*. Los atributos personalizados se utilizan para mantener el valor ContentURI en el servidor para cada archivo en un dispositivo y pueden ayudar a los administradores a determinar la disponibilidad de un archivo en el dispositivo, formar grupos de dispositivos dinámicos, y son necesarios para comunicar ContentURI a la aplicación de destino utilizando la configuración de aplicaciones gestionadas, etc.

En el caso de aplicaciones que no sean de Ivanti, los administradores deben consultar a los desarrolladores de aplicaciones de terceros sobre su compatibilidad con este enfoque, comúnmente denominado "Consumir ContentURI basado en FileProvider".

**Requisitos previos**:

- Añade un nuevo atributo personalizado basado en el dispositivo que se utilizará para la operación de transferencia de archivos. Para cada configuración de transferencia de archivos, debe crearse un único atributo personalizado. Cada atributo de dispositivo personalizado puede almacenar únicamente el contentURI (ubicación del archivo) del dispositivo para un archivo por config.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuraciones** > **Agregar configuración** > **Transferencia de archivos**. Se abre la página **Crear configuración de transferencia de archivos** .
:::

:::WorkflowBlockItem
Introduzca un nombre para la configuración en el cuadro **Nombre**.
:::

:::WorkflowBlockItem
Introduzca una **Descripción** de la configuración.
:::

:::WorkflowBlockItem
**Establecimiento de la configuración**

En la sección **Archivo a transferir**, seleccione los archivos a transferir mediante la opción de arrastrar y soltar o navegando a través de la opción **Elegir archivo** . Por defecto, el límite máximo de tamaño de los archivos es de 50 MB.
:::

:::WorkflowBlockItem
Seleccione una o más de las opciones siguientes para **Descargar en los dispositivos** (opcional):\* **Permitir descarga en una red con contador**: seleccione esta opción para continuar descargando el archivo incluso en una red con contador.

- **Requerir carga**: seleccione esta opción para asegurarse de que el dispositivo se está cargando durante el proceso de transferencia de archivos.
- **Requerir dispositivo inactivo**: seleccione esta opción para mantener el dispositivo inactivo durante el proceso de transferencia de archivos.
:::

:::WorkflowBlockItem
Utilice una de las dos opciones siguientes para compartir un archivo con otras aplicaciones

- **Transferencia mediante la configuración de aplicaciones administradas de Android**: utilice esta opción solo si la aplicación de destino puede consumir URI de contenido mediante la Configuración de aplicaciones administradas.
- **Transferencia mediante intención en el dispositivo**: las intenciones son específicas de cada aplicación. Para compartir un archivo mediante esta opción, consulte la documentación de la aplicación de destino y proporcione información en la sección de intenciones que aparece a continuación. Intents permite a la aplicación Ivanti Go emitir un mensaje en el dispositivo una vez que el archivo está disponible para ser compartido con las aplicaciones.
:::
::::

### Transferencia mediante Configuración de aplicaciones administradas de Android

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
En el campo **Elegir un atributo personalizado basado en un dispositivo existente para compartir este archivo con otras aplicaciones**, introduzca un nombre de atributo existente, por ejemplo, **Custom-Filename**. Para obtener más información, consulte [**Asignar atributos personalizados a los dispositivos**](./Asignar_atributos_personalizados_a_los_dispositivos.md).
:::

:::WorkflowBlockItem
El nombre del atributo personalizado debe ser un atributo nuevo y único que se utilice exclusivamente para esta operación de transferencia de archivos. Cada atributo de dispositivo personalizado puede almacenar únicamente el contentURI (ubicación del archivo) del dispositivo para un archivo por config.

**Proporcione acceso a las siguientes aplicaciones o nombres de paquetes**: puede seleccionar nombres de aplicaciones en el selector Nombres de aplicaciones y añadir Nombres de paquetes.
:::

:::WorkflowBlockItem
Estos serán los únicos paquetes autorizados que podrán acceder al archivo.

- **Nombres de la aplicación**: puede seleccionar nombres de aplicaciones desde el selector Nombres de la aplicación.
- **Nombres de paquetes**: puede introducir los ID de grupo en esta zona, por ejemplo,com.mobileiron.filetransfer.android3.Separe los nombres de varios paquetes con punto y coma (;).
  Haga clic en **Guardar**. La nueva configuración de Transferencia de archivos aparece en la página Configuraciones.
:::
::::

### Configuración de la aplicación de destino

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione la aplicación de destino que recibirá el archivo.
3. Vaya a **Configuración de aplicaciones > Configuraciones gestionadas para Android**.
4. Cree una nueva configuración o utilice una configuración existente.
5. Una aplicación puede tener un ajuste como "Información de manifiesto" u otras propiedades en las que el administrador puede definir la variable de sustitución y comunicar la ubicación del archivo a la aplicación de destino. Para la aplicación Ivanti Velocity como ejemplo, en el cuadro de diálogo Configuración de aplicaciones > **Obtener configuraciones**&#xNAN;**> Campo Información del manifiesto**, introduzca la variable de sustitución. Por ejemplo, $Custom-File-Name$.
   Seleccione la distribución.
6. Haga clic en **Guardar**.

### Transferencia mediante intención en el dispositivo

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
En el campo **Elegir un atributo de dispositivo existente para pasar la ruta del archivo en los extras de intents,** introduzca un nombre de atributo personalizado nuevo, por ejemplo, deviceIntentURI.
:::

:::WorkflowBlockItem
Los atributos personalizados se utilizan para mantener el valor de ubicación (URI / ContentURI) en el servidor para cada dispositivo y pueden ayudar a los administradores a determinar la disponibilidad de un archivo en el dispositivo. Para obtener más información, consulte [**Asignar atributos personalizados a los dispositivos**](./Asignar_atributos_personalizados_a_los_dispositivos.md).

En el campo **Proporcionar acceso a un nombre de aplicación o paquete específico**, introduzca el **Nombre de la aplicación** o el **Nombre del pquete**, por ejemplo, Velocity.Estos serán los únicos paquetes autorizados que podrán acceder al archivo.
:::

:::WorkflowBlockItem
En la sección Intents-Standard, proporcione los detalles siguientes:
:::

:::WorkflowBlockItem
- **Tipo de operación**: en la lista desplegable, seleccione **Iniciar actividad** / **Iniciar servicio** u otra opción similar según la aplicación. Elija el valor correcto para este campo en función de la orientación del desarrollador de la aplicación de destino o consulte la documentación de la aplicación de destino.
- **Nombre de clase** (opcional): elija el valor correcto para este campo en función de la orientación del desarrollador de la aplicación de destino o consulte la documentación de la aplicación de destino.
- **Acción**: ajuste la acción a\:com.wavelink.nameofapp.action.INSTALL\_CONFIGo similar, según la aplicación.
- **Categoría**: introduzca valores separados por punto y coma (;).
- **Tipo de MIME** (opcional): en el servidor host del administrador, el archivo custom.mobileconfig debe ser configurado con un tipo MIME de application/x-apple-aspen-config para que el perfil MDM del dispositivo se descargue e instale en el dispositivo. Elija el valor correcto para este campo en función de la orientación del desarrollador de la aplicación de destino o consulte la documentación de la aplicación de destino.
- **Indicadores** (opcional): seleccione el número de indicadores a utilizar. Elija el valor correcto para este campo en función de la orientación del desarrollador de la aplicación de destino.
  Proporcione los valores **Intents-Extras** con KEY, TYPE y VALUE (opcional). Para parámetros más específicos, consulte la documentación de la aplicación OEM. Elija el valor correcto para este campo en función de la orientación del desarrollador de la aplicación de destino o consulte la documentación de la aplicación de destino.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::

:::WorkflowBlockItem
En la página Configuraciones, seleccione la nueva Configuración de transferencia de archivos y, a continuación, seleccione **Acciones** > **Aplicar a etiqueta**. Se abre el cuadro de diálogo **Aplicar a etiqueta** .
:::

:::WorkflowBlockItem
Seleccione la Etiqueta adecuada y haga clic en **Aplicar**.

La transferencia/compartición de archivos con otras aplicaciones solo puede verificarse recopilando registros de la aplicación de destino o del dispositivo.
:::
::::

### Verificación del estado de la descarga de archivos

Los atributos personalizados se utilizan para mantener el valor de ubicación (ContentURI) en el servidor para cada dispositivo y pueden ayudar a los administradores a determinar la disponibilidad de un archivo en el dispositivo.

**Procedimiento**

1. Vaya a **Dispositivos&#x20;**>**Dispositivos**.
2. Seleccione un dispositivo específico en el que se haya desplegado la configuración de transferencia de archivos.
3. En la página Detalles del dispositivo, seleccione el dispositivo y, a continuación, **Acciones** > **Forzar registro del dispositivo**.
4. En la pestaña Configuraciones, compruebe que la configuración de Transferencia de archivos se muestra con el estado **Aplicada**.
5. En la pestaña Atributos personalizados, compruebe que aparece el nombre del nuevo atributo personalizado (por ejemplo, "Custom-File-Name$") con su valor correspondiente. Esto proporciona la información sobre la ubicación de almacenamiento del archivo en el dispositivo y muestra que el archivo se ha descargado localmente en el dispositivo disponible dentro del sandbox de la aplicación Ivanti Go.
   La transferencia/compartición de archivos con otras aplicaciones solo puede verificarse recopilando registros de la aplicación de destino o del dispositivo.
