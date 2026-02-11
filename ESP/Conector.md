---
title: Conector
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

**Licencia:&#x20;**&#x53;ilver

El conector de Ivanti Neurons for MDM proporciona acceso desde su servicio de Ivanti Neurons for MDM a los recursos corporativos, como un servidor LDAP o una Entidad de certificación (EC). Configure un Conector por cada recurso al que desee acceder.

Si utiliza Microsoft Active Directory o un servidor LDAP alojado en Amazon Web Services (AWS), podrá alojar el conector de Ivanti Neurons for MDM en AWS. No es necesario un Conector local.

Conector se actualiza automáticamente a la última versión del software.

Para obtener la Guía de instalación del conector de Ivanti Neurons for MDM más reciente, visite [**https://help.ivanti.com/#106**](https://help.ivanti.com/#106) y busque "Conector".

## Opciones de alojamiento del Conector

Puede alojar el conector de Ivanti Neurons for MDM de forma local su centro de datos o en Amazon Web Services (AWS):

- Aloje el Conector en AWS si está usando Microsoft Active Directory alojado en AWS o Microsoft Active Directory autoadministrado en AWS. En este caso, no necesitará tener un Conector local.
- Para acceder a los recursos locales, como un servidor LDAP o una EC, establezca el Conector de forma local.

### Alojar el Conector en AWS

Los clientes pueden alojar Conector en AWS para usarlo con las siguientes opciones de Microsoft Active Directory alojadas en AWS:

- Servicio del directorio de AWS para Microsoft Active Directory
- Microsoft Active Directory administrado por el cliente en el PCV de Amazon

Para ver más información sobre el Servicio de directorio de AWS para Microsoft Active Directory, consulte [**https://aws.amazon.com/directoryservice**](https://aws.amazon.com/directoryservice). Consulte la documentación de AWS sobre cómo alojar Microsoft Windows Server y Active Directory en un PCV de Amazon. El conector de Ivanti Neurons for MDM es compatible con Windows Server 2012, 2012 R2, 2015.

### Ajuste del AMI del conector MDM de Ivanti Neurons for MDM en AWS

Para ajustar el AMI del conector de Ivanti Neurons for MDM:

1. Inicie sesión en AWS con las credenciales de administrador.
2. En la página de servicios de AWS, seleccione **EC2** en **Compute**.
3. Expanda **Imágenes** y seleccione **AMI** en el panel izquierdo.
4. Seleccione **Imágenes públicas** del menú desplegable en el panel derecho.
5. Busca el Conector de Ivanti Neurons for MDM mediante palabras clave como "mobileiron-kocab".
6. Selecciona la última versión del Conector de la lista y haga clic en **Iniciar**.
7. Siga las instrucciones para instalar el Conector en la sección, "Desplegar el conector de Ivanti Neurons for MDM en AWS" de la *Guía de instalación del conector de Ivanti Neurons for MDM* disponible en [**https://help.ivanti.com/mi/help/en\_us/cld/**](https://help.ivanti.com/mi/help/en_us/cld/)*\<version>*/inst/default.htm, donde *version* es la versión del Conector de Ivanti Neurons for MDM que vaya a instalar. Por ejemplo, para la versión 74 del conector de Ivanti Neurons for MDM, la guía está disponible en [**https://help.ivanti.com/mi/help/en\_us/cld/**](https://help.ivanti.com/mi/help/en_us/cld/)**74**/inst/default.htm.

### Alojar el Conector de forma local

Para alojar un conector de Ivanti Neurons for MDM en las instalaciones de su centro de datos, haga clic en **Descargar conector** para descargar e instalar el conector de Ivanti Neurons for MDM. Extraiga el contenido del paquete descargado y siga las instrucciones de configuración de la Guía de instalación del conector de Ivanti Neurons for MDM que se incluye en el paquete.

## Acceder a los registros del Conector

Puede acceder a los registros del Conector desde el servicio de Conector para ayudarle a solucionar problemas relacionados con el Conector. Debe tener la función de Administrador del sistema o Solo lectura del sistema.

1. Vaya &#x61;**&#x20;Administrador > Conector** para ver la página del Conector.La interfaz del Connector muestra el estado del Conector (Activado o Desactivado), el Nombre del conector, la Conexión (Conectado o No conectada), Número de versión, Nivel de registro, Acciones (Desactivar o Eliminar el Conector).
2. Use el menú desplegabl&#x65;**&#x20;Nivel de registro&#x20;**&#x70;ara elegir un nivel.Los niveles de registro disponibles aparecen en el menú desplegable ordenados desde el nivel de registro más inferior hasta el más elevado:\* Error
   - Advertencia
   - Información
   - Depurar
   - RastrearEl nivel de información es el ajuste del nivel de registro predeterminado. Si elige otro nivel de registro, aparecerá un icono giratorio de sincronización

::Image[]{src="Sync_icon.png" signedSrc="Sync_icon.png" size="10" caption alt isUploading="false" sha initialPath="Sync_icon.png" githubPath="Sync_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
que indicará que se está obteniendo información en el nivel de registro que ha seleccionado. El nivel de registro se restablecerá en el nivel de información después de una hora. El nivel de seguimiento es el ajuste del nivel de registro más elevado. Utilice este nivel para recopilar todos los mensajes en todos los demás niveles. El icono de sincronización se muestra durante toda la duración de la solicitud.
:::

3. Si fuera necesario, mantenga el puntero sobre el icono Sincronizar

::Image[]{src="Sync_icon.png" signedSrc="Sync_icon.png" size="10" caption alt isUploading="false" sha initialPath="Sync_icon.png" githubPath="Sync_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
para ver el icono Cancelar
:::

::Image[]{src="Cancel_icon.png" signedSrc="Cancel_icon.png" size="10" caption alt isUploading="false" sha initialPath="Cancel_icon.png" githubPath="Cancel_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
. Haga clic en el icono Cancelar para cancelar el cambio de nivel de registro.
:::

4. Mantenga el puntero sobre el icono Solicitar para ver la información de la solicitud. Haga clic en el icono Solicitar

::Image[]{src="Fetch_icon.png" signedSrc="Fetch_icon.png" size="10" caption alt isUploading="false" sha initialPath="Fetch_icon.png" githubPath="Fetch_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
para solicitar los archivos de la carpeta del registro actual en un archivo .zip.Los archivos del registro se añadirán a un archivo .zip cuando se haga una solicitud. Cuando se hace una solicitud, el archivo .zip de la solicitud anterior se elimina.
:::

5. Si fuera necesario, mantenga el puntero sobre el icono Solicitar

::Image[]{src="Fetch_icon.png" signedSrc="Fetch_icon.png" size="10" caption alt isUploading="false" sha initialPath="Fetch_icon.png" githubPath="Fetch_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
y se convertirá en el icono Cancelar
:::

::Image[]{src="Cancel_icon.png" signedSrc="Cancel_icon.png" size="10" caption alt isUploading="false" sha initialPath="Cancel_icon.png" githubPath="Cancel_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
. Haga clic en el icono Cancelar para detener la solicitud.Cuando se cancela una solicitud antes de completarse, el icono Descargar
:::

::Image[]{src="Download_icon.png" signedSrc="Download_icon.png" size="10" caption alt isUploading="false" sha initialPath="Download_icon.png" githubPath="Download_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
no se mostrará debido a que el archivo de registro .zip anterior se eliminó del servidor. Los archivos de registro originales del Conector siguen estando disponibles para la solicitud.
:::

6. Haga clic en el icono Descargar

::Image[]{src="Download_icon.png" signedSrc="Download_icon.png" size="10" caption alt isUploading="false" sha initialPath="Download_icon.png" githubPath="Download_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
cuando la solicitud se haya completado para descargar el archivo de registro .zip que contiene los archivos de registro obtenidos durante la última solicitud.El nombre del archivo de registro tendrá el siguiente formato: kocab.log. El nombre del archivo zip que se descarga consta del nombre del servidor, la versión de conexión y una marca de tiempo que incluye el día, el mes, el año y la hora del día en el formato: \<Connector\_Hostname>\<Connector\_Version>\_\<TimeStamp>.zip. El nombre del archivo de registro archivado está en el siguiente formato: kocab.aaaa-mm-dd.0.log.gz.
:::

7. Opcionalmente, también puede usar el menú desplegable **Acciones** para Desactivar o Eliminar el Conector.

Si no puede ver la página **Conector**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Sistema de solo lectura
