---
title: Catálogo de aplicaciones
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Licencias para las características de las aplicaciones**](./Catálogo_de_aplicaciones.md)
- [**Alternar entre la vista de lista y de cuadrícula**](./Catálogo_de_aplicaciones.md)
- [**Añadir una aplicación de la Google Play Store para Android Enterprise**](./Catálogo_de_aplicaciones.md)
- [**Añadir una aplicación desde una store pública**](./Catálogo_de_aplicaciones.md)
- [**Añadir una aplicación interna**](./Catálogo_de_aplicaciones.md)
- [**Delegar permisos de dispositivos delegados para aplicaciones internas de Android Enterprise**](./Catálogo_de_aplicaciones.md)
- [**Mostrar el estado del perfil de aprovisionamiento para las aplicaciones internas de iOS**](./Catálogo_de_aplicaciones.md)
- [**Actualizar el perfil de aprovisionamiento para las aplicaciones internas de iOS**](./Catálogo_de_aplicaciones.md)
- [**Implementar aplicaciones internas en Google Play**](./Catálogo_de_aplicaciones.md)
- [**Añadir una aplicación web para dispositivos con Android Enterprise**](./Catálogo_de_aplicaciones.md)
- [**Añadir una aplicación web para dispositivos iOS**](./Catálogo_de_aplicaciones.md)
- [**Uso de la búsqueda avanzada**](./Catálogo_de_aplicaciones.md)
- [**Exportación de aplicaciones a un archivo CSV**](./Catálogo_de_aplicaciones.md)

Utilice la página del catálogo de aplicaciones para administrar su catálogo de aplicaciones. El catálogo de aplicaciones enumera las aplicaciones móviles que ha puesto disponibles para sus usuarios. Estas incluyen aplicaciones que los usuarios pueden descargar desde tiendas de aplicaciones públicas y aplicaciones que pretende distribuir mediante de Ivanti Neurons for MDM (aplicaciones internas). Las aplicaciones con AppConnect activado, GoClient para iOS y M\@W para macOS también están disponibles como aplicaciones de empresa en la página Catálogo de aplicaciones, de manera que se simplifica el proceso de importación para configuración y distribución. En dispositivos «MAM only», a los usuarios de iOS se les solicitará que seleccionen el certificado para autenticar el acceso a estas aplicaciones cuando abran el Catálogo de aplicaciones.

Los MacBooks con chipset M1 de Apple admiten aplicaciones VPP para iPhone y iPad. Solo el administrador puede enviar las aplicaciones VPP de iPhone y iPad compatibles. Esta opción no está disponible para que los usuarios la instalen desde el Catálogo de aplicaciones.

En el caso de los abonados de Ivanti Neurons for MDM con dispositivos Android, si Android Enterprise no está habilitado a finales de marzo de 2021, los administradores no podrán buscar aplicaciones con los nombres. La comunicación sobre este cambio se muestra con un mensaje de banner cuando se accede a la página del App Catalog. Este mensaje de banner se seguirá mostrando hasta que se active Android Enterprise en estos abonados y hasta que no se seleccione la opción "No volver a mostrar esto".

- el método de instalación silenciosa de aplicaciones no está disponible para las aplicaciones macOS públicas. Las aplicaciones macOS también se pueden implementar a través del Apps and Books de Apple mediante licencias basadas en dispositivos y mediante el método de instalación silencioso de aplicaciones en las inscripciones.
- Mientras se carga la aplicación Go al servidor de Ivanti Neurons for MDM, si debe seleccionar la opción **Convertir en aplicación administrada**, también debe activar la opción **Instalar en dispositivo**.
- App Catalog y la instalación de aplicaciones no son compatibles con dispositivos Sonim XP5S.
- Android no permite desinstalar las aplicaciones con privilegios de administrador activos. Para desinstalar la aplicación, vaya a **Ajustes del dispositivo > Seguridad > Administradores de dispositivos**, y desactive los privilegios del Administrador del dispositivo. A continuación, desinstale la aplicación.
- Si la aplicación está comprimida u oculta, no se podrán cargar las aplicaciones internas de Android.
- Las aplicaciones públicas no son compatibles con [**iPads compartidos**](./Dispositivos_iPad_compartidos_para_empresas.md).
- Debido a una limitación de Apple, para las aplicaciones Business-to-Business (B2B) disponibles en el Catálogo de aplicaciones, las descripciones y capturas de pantalla de las aplicaciones no están disponibles en la pestaña Detalles.
- Cuando se busca una aplicación en el Catálogo de aplicaciones o en el portal administrativo, los resultados de la búsqueda se basan en el **Nombre de la aplicación**, **Comentario**, **Descripción**, **Versión en pantalla** y **Novedades**. Si los datos de la aplicación buscada coinciden con cualquiera de estos campos, se mostrarán como resultado de búsqueda.

## Licencias para las características de las aplicaciones

Las siguientes características del catálogo de aplicaciones requieren licencias adicionales:

- Instalación/desinstalación silenciosa de aplicaciones: licencia Silver
- Configuración por aplicación: licencia Gold
- Configuración personalizada de AppConnect: licencia Gold
- Configuración personalizada de [**Android Enterprise**](./Configurar_Android_Enterprise.md): Silver license

Si el dispositivo Android está en modo kiosco:

Solo pueden instalarse aplicaciones internas mientras el dispositivo esté en modo kiosco. Puede instalar aplicaciones públicas, pero el dispositivo debe salir del modo kiosco antes de que puedan instalarse las aplicaciones. Además, se pueden limitar la cantidad de aplicaciones disponibles para usarse en dispositivos en el modo kiosco a solamente las aplicaciones que su empresa haya aprobado o puesto en la lista de permitidos. En dispositivos que usen Android 4.1, si una aplicación aprobada inicia una aplicación no incluida en la lista de permitidos, esa aplicación se iniciará y después se minimizará rápidamente. En dispositivos que usen Android 5,0, la aplicación no aprobada iniciada desde una aplicación que está en la lista de permitidos seguirá sin estar disponible.

## Alternar entre la vista de lista y de cuadrícula

Haga clic en el icono Lista o Cuadrícula en la parte derecha de la pantalla del catálogo de aplicaciones.

::Image[]{src="cloudr38grid001.png" signedSrc="cloudr38grid001.png" size="46" caption alt isUploading="false" sha initialPath="cloudr38grid001.png" githubPath="cloudr38grid001.png" position="flex-start"}

## Añadir una aplicación de la Google Play Store para Android Enterprise

- Se puede agregar una aplicación desde Google Play Store al catálogo de aplicaciones y ponerla a disposición de los usuarios. Para añadir una aplicación desde la Google Play Store en Android Enterprise, es necesario aprobar la aplicación para que pueda incluirse en el catálogo de aplicaciones.
- El diseño de Google Play Store para los dispositivos Android Enterprise tiene una página de inicio -para los dispositivos migrados- que se gestiona desde el Core y tiene un enlace rápido a Ivanti Neurons for MDM, que muestra todas las aplicaciones que se gestionan desde Ivanti Neurons for MDM. Al migrar dispositivos Android Enterprise de Core a Ivanti Neurons for MDM, solo las aplicaciones comunes entre el catálogo de aplicaciones de Core e Ivanti Neurons for MDM aparecen en el perfil de trabajo de Google Play Store del dispositivo. Puede hacer clic en el botón Ivanti Neurons for MDM para ver la lista de todas las aplicaciones que están disponibles en el catálogo de aplicaciones de Ivanti Neurons for MDM.

El diseño de Google Play Store para los dispositivos Android Enterprise tiene una página de inicio -para los dispositivos migrados- que se gestiona desde el Core y tiene un enlace rápido a Ivanti Neurons for MDM, que muestra todas las aplicaciones que se gestionan desde Ivanti Neurons for MDM. Al migrar dispositivos Android Enterprise de Core a Ivanti Neurons for MDM, solo las aplicaciones comunes entre el catálogo de aplicaciones de Core e Ivanti Neurons for MDM aparecen en el perfil de trabajo de Google Play Store del dispositivo. Puede hacer clic en el botón de Ivanti Neurons for MDM para ver todas las aplicaciones que hay disponibles en el catálogo de aplicaciones de Ivanti Neurons for MDM.

**Requisito previo**

- Se debe habilitar Android Enterprise para acceder y añadir aplicaciones de Google Play store al App Catalog.

ProcedureProcedimiento

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Haga clic en **Añadir** (arriba a la izquierda).Seleccione Google Play de la lista desplegable para buscar una aplicación en la Google Play Store. Google Play iFrame se muestra cuando Android Enterprise está inscrito.
3. Busque la aplicación en el campo de búsqueda y haga clic en la aplicación.
4. Una aplicación aprobada se puede desaprobar más adelante haciendo clic en **DESAPROBAR**.

| Opción                                                                                 | Descripción                                                                                                                                                                             |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Ajustes de aprobación**                                                              |                                                                                                                                                                                         |
| Mantener la aprobación cuando la aplicación solicite nuevos permisos                   | Permite a los usuario instalar aplicaciones actualizadas                                                                                                                                |
| Revocar la aprobación de la aplicación cuando esta aplicación solicite nuevos permisos | Desinstala la aplicación de la store hasta que se vuelva a aprobar.                                                                                                                     |
| **Ajustes de aprobación**                                                              |                                                                                                                                                                                         |
| Añadir suscriptor                                                                      | Introduzca la dirección de correo electrónico para añadir suscriptores a las notificaciones por correo electrónico cuando las aplicaciones que haya aprobado soliciten nuevos permisos. |
| Haga clic en **Hecho**.                                                                |                                                                                                                                                                                         |

## Añadir una aplicación desde una store pública

Se puede añadir una aplicación desde una store pública al catálogo de aplicaciones y ponerla disponible para los usuarios.

**Procedimiento**

::::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Aplicaciones > Catálogo de aplicaciones**.
:::

:::WorkflowBlockItem
Haga clic en **Añadir**.
:::

:::WorkflowBlockItem
Elija la aplicación que desea:1) Seleccione la app store pública.
2\) Introduzca el nombre de la aplicación.
3\) Seleccione la aplicación de la lista.
4\) Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Describa la aplicación para los usuarios:1) Añada o elimine categorías.
2\) Introduzca una descripción opcional.
3\) Haga clic en **Siguiente**.
:::

:::::WorkflowBlockItem
Defina la distribución de aplicaciones:

::::WorkflowBlock
:::WorkflowBlockItem
Seleccione una opción de distribución.
:::

:::WorkflowBlockItem
Amplíe la sección **Opciones avanzadas y configuración de aplicaciones**.
:::

:::WorkflowBlockItem
Siga las siguientes pautas para completar las opciones:

| **Ajuste**              | Qué hacer                                                                                                                                                                                                                                                                                                                                 |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Instalar en dispositivo | Seleccione esta opción para iniciar la instalación inmediatamente después del registro. Se solicitará al usuario que confirme la instalación de la aplicación, excepto en las siguientes situaciones:\* El dispositivo es un dispositivo iOS supervisado para las instalaciones de nuevas aplicaciones y actualizaciones de aplicaciones. |

- El dispositivo es un dispositivo iOS no supervisado para actualizaciones de aplicaciones.
- Los usuarios que se hayan inscrito en el programa Apps and Books.
- El dispositivo es un dispositivo Samsung Knox y se ha seleccionado la opción de instalación silenciosa que aparece a continuación.En el caso de aplicaciones públicas iOS, cuando se instalan por primera vez en el dispositivo, App Catalog muestra el botón 'Reinstalar', que permite al usuario volver a instalar la aplicación.la reinstalación se realiza si la versión de la aplicación es diferente a la versión de la app store de iOS. |
  \| No mostrar la aplicación en el App Catalog del usuario final                                                      | Seleccione esta opción si no desea que el usuario vea la aplicación en el catálogo de aplicaciones del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| Establecer la prioridad de instalación de las aplicaciones                                                        | Seleccione Alta, Media o Baja para establecer la prioridad de la instalación de la aplicación durante la incorporación del usuario. Solo se instalan las aplicaciones de alta prioridad durante la incorporación del usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Suspender una segunda inserción de la aplicación después de un número determinado de intentos fallidos (solo iOS) | Ponga el interruptor de conmutación en ON para suspender la segunda inserción de la aplicación después de un número determinado de intentos fallidos de reinserción pulsación utilizando los siguientes ajustes:**Dejar de insertar después de**: introduzca el número de intentos fallidos de reinserción después de los cuales debe dejarse de intentar la inserción. Los valores introducidos deben estar entre **1** y **999\*\*\*\*intentos fallidos y volver a intentarlo después**: introduzca el número de horas necesarias después de la reinserción fallida para volver a intentarlo. Los valores introducidos deben ser estar entre **3** y **48** horas.                                                                                                                                                                                                                                                                                           |
  \| (Solo Android) Instalar de forma silenciosa en dispositivos Samsung Knox                                          | Esta opción no es aplicable a las aplicaciones públicas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| (Solo iOS y macOS) Activar la VPN por aplicación para esta aplicación                                             | Seleccione esta opción para usar una [**Configuración de VPN por aplicación**](./Configuración_de_VPN_por_aplicación.md) con esta aplicación.Seleccione la configuración VPN por aplicación para usarla de la lista desplegable.Para macOS, seleccione solo la configuración de VPN por aplicación de Tunnel.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  \| (Solo iOS) Impedir la copia de seguridad de iCloud e iTunes                                                       | Seleccione esta opción para evitar que se haga una copia de seguridad en iCloud e iTunes de los datos relacionados con esta aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| (Solo iOS) Eliminar aplicaciones dadas de baja                                                                    | Seleccione esta opción para eliminar esta aplicación una vez que el dispositivo ya no esté siendo administrado por Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| (Solo iOS) Configuración personalizada AppConnect                                                                 | En la aplicación habilitada para AppConnect, introduzca las claves y valores que especifican sus preferencias de configuración personalizada. Consulte la documentación de la aplicación para ver las claves disponibles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| iOS 7+ Ajustes de la aplicación administrada                                                                      | Introduzca las claves y valores definidos para esta aplicación a modo de aplicación administrada por iOS 7+. Consulte la documentación de la aplicación para ver información sobre las claves compatibles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  Las aplicaciones de [**Android Enterprise**](./Configurar_Android_Enterprise.md) tendrán opciones distintas.

Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione una opción de promoción:
:::

:::WorkflowBlockItem
- No destacadas
- Lista de destacadas
- Banner destacado
- Si selecciona Banner destacado especifique los siguientes detalles:1) **Título**: especifique el título de la aplicación
  2\) **Descripción**: especifique los detalles de la aplicación
  3\) **Estilo de banner**: seleccione un color de banner
  Haga clic en **+ Añadir descripción** para introducir una breve descripción de la configuración.
:::

:::WorkflowBlockItem
Opcionalmente, puede cambiar la distribución de la configuración.
:::

:::WorkflowBlockItem
Haga clic en **Hecho** para guardar la configuración de la aplicación.
:::

:::WorkflowBlockItem
Haga clic en **Hecho**.
:::
::::
:::::
::::::

Cuando se busca una aplicación de Windows en el Catálogo de aplicaciones, se puede buscar la aplicación que más coincide mediante las opciones **Nombre de la aplicación** o **ID de AppStore** en la lista desplegable:

- **Nombre de la aplicación**: seleccione esta opción para proporcionar el nombre de la aplicación
- **ID de AppStore**: seleccione esta opción para proporcionar la ID de AppStore

La búsqueda de aplicaciones de Windows Store admite aplicaciones de Win32 Store.

Asegúrese de que la herramienta Winget está disponible en el dispositivo para gestionar las aplicaciones de Win32 Store.

## Añadir una aplicación interna

Puede cargar una aplicación interna al catálogo de aplicaciones con los siguientes formatos de archivo. Si el archivo es grande puede tardar varios minutos en cargarse. El número de versiones de aplicaciones internas está limitado a 100. Si se supera ese número, el sistema Ivanti Neurons for MDM purga las versiones más antiguas de la aplicación. El estado de la carga y purga de la aplicación aparece en una lista y es visible desde la página de Registros de Auditoría.

El inventario de aplicaciones MIP devuelto por Mobile\@Work puede ser incorrecto para algunas aplicaciones. Mobile\@Work puede fallar al detectar el estado de instalación de las aplicaciones que no están instaladas en la ubicación predeterminada. Para tales aplicaciones, agregar la secuencia de comandos de detección ayudará a identificar el estado correcto de la aplicación en el dispositivo. Mobile\@Work determina la presencia de la aplicación si el código de salida de la secuencia de comandos de detección es 0. Para cualquier otro código de salida, la aplicación se determinará como no instalada. En función de las aplicaciones detectadas, Mobile\@Work prepara el informe de inventario para el dispositivo.

- IPA (iOS)
- MIP (aplicación Packager de macOS)
- PKG (macOS)
- APK (Android)
- APPX, APPXBUNDLE, EXE y MSI (Windows)

Mobile\@Work para macOS solo puede detectar solicitudes de instalación correctas en las aplicaciones PKG con secuencias de comandos o DMG con PKG con secuencias de comandos. No informará si la aplicación ha sido borrada o si las secuencias de comandos instalados han sido eliminados. Por tanto, el servidor Ivanti Neurons for MDM no podrá reenviar un comando de instalación. Si se pierde la conexión mientras descarga las aplicaciones, vuelva a intentarlo y haciendo un ingreso. Para las aplicaciones MIP, aun en el caso de que la aplicación se haya eliminado del dispositivo instalado a través de las PKG con secuencias de comandos o DMG con PKG con secuencias de comandos, Mobile\@Work no instalará la aplicación MIP si el acceso a las PKG existe en la carpeta de entradas del dispositivo del cliente.

**Procedimiento**

:::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Aplicaciones > Catálogo de aplicaciones**.
:::

:::WorkflowBlockItem
Haga clic en **Añadir** (arriba a la izquierda).
:::

:::WorkflowBlockItem
Arrastre el archivo de la aplicación hasta el cuadro punteado o haga clic en **Elegir archivo** para seleccionarlo del sistema de archivos y haga clic en **Confirmar**.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente** (abajo a la derecha).
:::

::::WorkflowBlockItem
Describa la aplicación para usuarios y configure los requisitos previos de la misma:::::WorkflowBlock

:::WorkflowBlockItem
Añada [**categorías**](./Categorías.md).
:::

:::WorkflowBlockItem
Al añadir un paquete macOS, si el archivo del paquete contiene más de una aplicación (por ejemplo, paquetes de Microsoft Office y Cisco AnyConnect), se usarán las aplicaciones principales seleccionadas para identificar que el paquete se ha instalado. La VPN por aplicación, si está configurada, se aplicará a estas aplicaciones.
:::

:::WorkflowBlockItem
Introduzca una descripción opcional.
:::

:::WorkflowBlockItem
**Código de producto MSI**: cuando cargue aplicaciones MSI, el código de producto de la aplicación MSI se rellena automáticamente en este campo.
:::

:::WorkflowBlockItem
Debe seleccionar la opción "He marcado el código de producto MSI" para asegurarse de que el GUID correcto esté relleno.

**URL de anulación:** introduzca una anulación de URL de origen de la aplicación opcional para permitir la descarga de la aplicación desde un origen diferente o para permitir la obtención de archivos grandes, como archivos multimedia para instalar Microsoft Office desde una red local (HTTP y HTTPS). Esta opción requiere acceso a una red interna segura y la sincronización manual de un servidor alternativo donde estén almacenadas las aplicaciones. No introduzca un valor a menos que haya establecido la infraestructura necesaria. Puede editar este valor mientras se editan los ajustes de la aplicación para esa aplicación específica.\* Para aplicaciones de iOS, las URL de reemplazo de aplicaciones debe tener formato HTTP o HTTPS.

- Para aplicaciones de Android y macOS, las URL de reemplazo de aplicaciones solo deben tener formato HTTPS.
- Para aplicaciones de macOS, la URL debe terminado con la extensión .pkg.
:::

:::WorkflowBlockItem
**Línea de comandos** (Solo aplicaciones MSI Windows de 32 bits): introduzca un conmutador de línea de comandos opcional para especificar la información adicional que no sea parte del paquete mientras se implementan los archivos MSI. Por ejemplo, para escribir registros de la instalación en un archivo de salida, se puede introducir "/log output.txt" en este campo. De este modo, se creará el archivo output.txt en la carpeta C:\Windows\System32. Por defecto, la opción de la línea de comandos /qn para la instalación silenciosa se rellena automáticamente durante la carga de la aplicación MSI.
:::

:::WorkflowBlockItem
El nombre del paquete de la aplicación MSI que se va a cargar no se debe añadir como parte de los argumentos de la línea de comandos. Si se añade, la carga se restringirá hasta que el nombre del paquete de la aplicación se elimine de los argumentos de la línea de comandos. En el enlace adicional se proporciona una lista de todas las opciones admitidas de la línea de comandos. Este enlace será visible en el modo Visualización y Edición de la aplicación.

.EXE for Win32: se instalan a través de Bridge mediante el modo de administrador de PowerShell. La función de Bridge se usará automáticamente si está disponible.
:::

:::WorkflowBlockItem
- Actualice la versión para mantener la coherencia entre la **Versión en pantalla** y la **Versión del paquete**
- Ubicación del instalador (.EXE)
- Parámetros de la línea de comandos del instalador: el obligatorio un argumento para ejecutar de forma silenciosa al archivo (por ejemplo, /SILENT o /VERYSILENT).
- Ejecutar instalador como usuario: para instalar usando las credenciales del usuario, seleccione la opción «Ejecutar como usuario».
  Para aplicaciones de Win32 Store: se instalan a través de Bridge mediante el modo de administrador de PowerShell.
:::

:::WorkflowBlockItem
Configure las aplicaciones con requisitos previos para las aplicaciones Packager de macOS (opcional). Consulte Comprender las aplicaciones internas de Packager para macOS para conocer información general acerca de la funcionalidad de las aplicaciones con requisitos previos.
:::

:::WorkflowBlockItem
**URL de inicio**: ingrese en la URL personalizada para iniciar la aplicación en AppStation. Solo es necesario cuando agregue aplicaciones que no son de AppConnect en un entorno «MAM only» con AppStation y solo es aplicable en aplicaciones iOS.
:::

:::WorkflowBlockItem
Configure la pestaña [**delegación de aplicaciones**](./Delegar_aplicaciones.md).
:::

:::WorkflowBlockItem
Una vez que delega una aplicación con requisitos previos y esta se convierte en aplicación con requisitos previos del espacio no predeterminado, no se puede dejar de delegar esa aplicación a menos que elimine primero la relación de requisito previo.

Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**.
:::

\::::
::::

:::WorkflowBlockItem
(Opcional) Añada capturas de pantalla de la aplicación.
:::

:::WorkflowBlockItem
(Opcional) Añada o sustituya los iconos de la aplicación (aplicaciones para iOS, macOS y Windows).
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Para las aplicaciones Packager de macOS, defina o seleccione las secuencias de comandos de instalación que se ejecutarán antes y/o después de la instalación de la aplicación. Seleccione uno o ambos de los siguientes secuencias de comandos escribiendo en el cuadro de búsqueda o haciendo clic en el enlace para ver la lista de secuencias de comandos. Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
- **Secuencias de comandos de preinstalación**: introduzca el nombre de la secuencia de comandos para seleccionar la secuencia de comandos que se ejecutará antes de la instalación de la aplicación. Las secuencia de comandos de preinstalación se ejecutarán o volverán a ejecutarse hasta que se reciba del cliente el estado de éxito de la ejecución de la secuencia de comandos. Solo después de eso, se envía el comando de instalación de la aplicación. Puede ver el estado de ejecución de ka secuencia de comandos en la página de detalles del dispositivo en la pestaña **Registros**.
- **Secuencias de comandos de preinstalación**: introduzca el nombre de la secuencia de comandos para seleccionar la secuencia de comandos que se ejecutará antes de la instalación de la aplicación.
- **Secuencias de comandos de desinstalación**: introduzca el nombre de la secuencia de comandos que el servidor envía a un dispositivo cuando detecta que una aplicación ya no se distribuye al dispositivo.
- **Secuencias de comandos de detección**: ingrese el nombre de la secuencia de comandos que el servidor envía a un dispositivo para detectar una aplicación. El resultado de la secuencia de comandos de detección de la aplicación anula el resultado del inventario predeterminado de la aplicación en el dispositivo. Independientemente de si la aplicación se distribuye al dispositivo o no, la secuencia de comandos de detección de todas las aplicaciones se enviará al dispositivo para evaluar la existencia de las aplicaciones en el dispositivo.
  A continuación se muestra una secuencia de comandos de detección de muestra:
  \#!/bin/bashapp\_name="Name of the App"count="$(system\_profiler SPApplicationsDataType | grep "$app\_name" -c)"echo "$app\_name count $count"if \[ $count -ge 1 ]thenecho "$app\_name is installed"elseecho "$app\_name is not installed"exit 1fiexit 0
  Puede crear secuencias de comandos en la página de **Administración >&#x20;**[**Todas las secuencias de comandos**](./Todas_las_secuencia_de_comandos.md). Si actualiza la aplicación, puedes elegir copiar las secuencias de comandos de la aplicación anterior y ejecutar las secuencias de comandos de la aplicación actualizada. Si omite esta sección, puede configurar las secuencias de comandos editando la aplicación más tarde.

Defina la distribución de aplicaciones:
:::

::::WorkflowBlockItem
1. Seleccione una opción de distribución.
2. Amplíe la sección **Opciones avanzadas y configuración de aplicaciones**.
3. Siga las siguientes pautas para completar las opciones:

| **Ajuste**              | Qué hacer                                                                                                                                                                                                                                                 |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Instalar en dispositivo | Seleccione esta opción para iniciar la instalación inmediatamente después del registro. Se solicitará al usuario que confirme la instalación de la aplicación, excepto en las siguientes situaciones:\* El dispositivo es un dispositivo iOS supervisado. |

:::Paragraph{listStyleType="disc" indent="2"}
El dispositivo es un dispositivo Samsung Knox y se ha seleccionado la opción de instalación silenciosa que aparece a continuación.                                                                                                                                                                                                                                                                    |
\| No mostrar la aplicación en el App Catalog del usuario final                                                      | Seleccione esta opción si no desea que el usuario vea la aplicación en el catálogo de aplicaciones del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
\| Establecer la prioridad de instalación de las aplicaciones                                                        | Seleccione Alta, Media o Baja para establecer la prioridad de la instalación de la aplicación durante la incorporación del usuario. Solo se instalan las aplicaciones de alta prioridad durante la incorporación del usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
\| Suspender una segunda inserción de la aplicación después de un número determinado de intentos fallidos (solo iOS) | Ponga el interruptor de conmutación en ON para suspender la segunda inserción de la aplicación después de un número determinado de intentos fallidos de reinserción pulsación utilizando los siguientes ajustes:**Dejar de insertar después de**: introduzca el número de intentos fallidos de reinserción después de los cuales debe dejarse de intentar la inserción. Los valores introducidos deben estar entre **1** y **999\*\*\*\*intentos fallidos y volver a intentarlo después**: introduzca el número de horas necesarias después de la reinserción fallida para volver a intentarlo. Los valores introducidos deben ser estar entre **3** y **48** horas. |
\| (Solo Android) Instalar de forma silenciosa en dispositivos Samsung Knox                                          | Seleccione esta opción si no desea que se solicite al usuario que confirme la instalación en dispositivos Samsung KNOX.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
\| (Solo iOS y macOS) Activar la VPN por aplicación para esta aplicación                                             | Seleccione esta opción para usar una [**Configuración de VPN por aplicación**](./Configuración_de_VPN_por_aplicación.md) con esta aplicación.Seleccione la configuración VPN por aplicación para usarla de la lista desplegable.Para macOS, seleccione solo la configuración de VPN por aplicación de Tunnel.                                                                                                                                                                                                                                                                                                                                                                   |
\| (Solo iOS) Impedir la copia de seguridad de iCloud e iTunes                                                       | Seleccione esta opción para evitar que se haga una copia de seguridad en iCloud e iTunes de los datos relacionados con esta aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
\| (Solo iOS) Eliminar aplicaciones dadas de baja                                                                    | Seleccione esta opción para eliminar esta aplicación una vez que el dispositivo ya no esté siendo administrado por Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
\| (Solo iOS) Configuración personalizada AppConnect                                                                 | En la aplicación habilitada para AppConnect, introduzca las claves y valores que especifican sus preferencias de configuración personalizada. Consulte la documentación de la aplicación para ver las claves disponibles.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
\| iOS 7+ Ajustes de la aplicación administrada                                                                      | Introduzca las claves y valores definidos para esta aplicación a modo de aplicación administrada por iOS 7+. Consulte la documentación de la aplicación para ver información sobre las claves compatibles.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
Haga clic en **Siguiente**.
Seleccione una opción de promoción:
:::
::::

:::WorkflowBlockItem
- No destacadas
- Lista de destacadas
- Banner
  Haga clic en **Hecho**.
:::
:::::

### Comprender las aplicaciones internas de Packager de macOS

A la hora de importar aplicaciones internas de Packager de macOS, el administrador puede activar

::Image[]{src="Resources/Images/1.png" signedSrc="Resources/Images/1.png" size="10" caption alt isUploading="false" sha initialPath="Resources/Images/1.png" githubPath="Resources/Images/1.png" position="flex-start"}

, la función de aplicaciones con requisitos previos, para buscar

::Image[]{src="Resources/Images/2.png" signedSrc="Resources/Images/2.png" size="10" caption alt isUploading="false" sha initialPath="Resources/Images/2.png" githubPath="Resources/Images/2.png" position="flex-start"}

y seleccionar

::Image[]{src="Resources/Images/3.png" signedSrc="Resources/Images/3.png" size="10" caption alt isUploading="false" sha initialPath="Resources/Images/3.png" githubPath="Resources/Images/3.png" position="flex-start"}

, las aplicaciones con requisitos previos que deben instalarse en los clientes antes de poder instalar la aplicación que el administrador está importando.

::Image[]{src="Resources/Images/62_mip005.png" signedSrc="Resources/Images/62_mip005.png" size="57" caption alt isUploading="false" sha initialPath="Resources/Images/62_mip005.png" githubPath="Resources/Images/62_mip005.png" position="flex-start"}

Una vez importada, la aplicación interna Packager de macOS aparecerá en el app catalog con el

::Image[]{src="Resources/Images/MIPBadge.png" signedSrc="Resources/Images/MIPBadge.png" size="10" caption alt isUploading="false" sha initialPath="Resources/Images/MIPBadge.png" githubPath="Resources/Images/MIPBadge.png" position="flex-start"}

identificador debajo

::Image[]{src="Resources/Images/1.png" signedSrc="Resources/Images/1.png" size="10" caption alt isUploading="false" sha initialPath="Resources/Images/1.png" githubPath="Resources/Images/1.png" position="flex-start"}

. A continuación podrá usar los ajustes de la columna,

::Image[]{src="Resources/Images/2.png" signedSrc="Resources/Images/2.png" size="10" caption alt isUploading="false" sha initialPath="Resources/Images/2.png" githubPath="Resources/Images/2.png" position="flex-start"}

, para añadir la columna APLICACIONES CON REQUISITOS PREVIOS (PREREQUISITE APPS),

::Image[]{src="Resources/Images/3.png" signedSrc="Resources/Images/3.png" size="10" caption alt isUploading="false" sha initialPath="Resources/Images/3.png" githubPath="Resources/Images/3.png" position="flex-start"}

, con el fin de ver rápidamente las aplicaciones que tienen dependencias, es decir, las que tienen requisitos previos.

- Puede buscar y seleccionar aplicaciones de tipo MIP, no MIP y aplicaciones públicas (Apps and Books y aplicaciones públicas de la App Store de macOS) como aplicaciones con requisitos previos.
- Los usuarios deben aceptar la licencia de Apps and Books para que las aplicaciones con requisitos previos de Apps and Books se instalen de forma silenciosa.
- Para las aplicaciones públicas con requisitos previos que no sean de Apps and Books, los administradores deben distribuir explícitamente las aplicaciones públicas y el usuario debe instalarlas. Hay que importar las aplicaciones públicas (de Apps and Books y que no sean de Apps and Books) en el App Catalog para que puedan aparecer en la lista de aplicaciones con requisitos previos. La columna «Origen» indica el tipo de aplicación con requisitos previos.
- El ingreso de MDM es obligatorio para instalar una aplicación interna que no sea MIP que tenga aplicaciones con requisitos previos que no sean de MIP.
- Los usuarios deben instalar manualmente aplicaciones públicas con requisitos previos que no sean de Apps and Books.
- Si se elimina el token de Apps and Books o si la licencia ha caducado, no se instalarán las aplicaciones de Apps and Books seleccionadas como aplicaciones con requisitos previos y, por ende, tampoco la aplicación principal. El administrador debe seguir la práctica recomendada para informar a los usuarios con antelación para las aplicaciones de Apps and Books en cualquiera de estos casos.

::Image[]{src="Resources/Images/62_mip010.png" signedSrc="Resources/Images/62_mip010.png" size="54" caption alt isUploading="false" sha initialPath="Resources/Images/62_mip010.png" githubPath="Resources/Images/62_mip010.png" position="flex-start"}

Las aplicaciones con requisitos previos también están disponibles como aplicaciones independientes para que el usuario las descargue cuando se distribuyan explícitamente. Si el usuario intenta desinstalar una aplicación con requisitos previos:

- Asegúrese de que la aplicación necesaria se instala de nuevo en el siguiente registro del dispositivo.
- La aplicación con requisitos previos se desinstalará si no hay ninguna aplicación principal dependiente en el mismo dispositivo.
- Si la aplicación con requisitos previos no se ha distribuido explícitamente, se desinstalará junto con la aplicación principal.
- Si la aplicación con requisitos previos se ha distribuido explícitamente, se mantendrá en el dispositivo.
- Si la aplicación con requisitos previos tiene una aplicación dependiente, se mantendrá en el dispositivo.

**Desactivar la función de aplicaciones con requisitos previos**

Cuando interactúe con aplicaciones que tienen dependencias y aplicaciones con requisitos previos, p. ej. al actualizar, borrar o delegar dichas aplicaciones, encontrará mensajes del sistema que le informarán de cómo la dependencia o el requisito previo de la aplicación puede afectar a las acciones que usted va a realizar. Por ejemplo, cuando intente desactivar la función «Aplicaciones con requisitos previos» para una aplicación, aparecerá el siguiente mensaje:

::Image[]{src="Resources/Images/62mip_turnoffporompt001.png" signedSrc="Resources/Images/62mip_turnoffporompt001.png" size="34" caption alt isUploading="false" sha initialPath="Resources/Images/62mip_turnoffporompt001.png" githubPath="Resources/Images/62mip_turnoffporompt001.png" position="flex-start"}

- Si desactiva la función «Aplicaciones con requisitos previos» para una aplicación, desaparecerán los detalles sobre las aplicaciones con requisitos previos. Esto incluye la delegación automática y la no delegación de las aplicaciones con requisitos previos de los subespacios.
- En Apps\@Work, el botón de instalación no aparecerá para las aplicaciones dependientes cuyas aplicaciones con requisitos previos no estén ya instaladas en el cliente receptor.
- En los dispositivos de los usuarios, cuando un usuario intenta instalar una aplicación interna con dependencias, se instalarán primero las aplicaciones con requisitos previos (si no están ya instaladas) y, a continuación, la aplicación principal. Este proceso podrá tardar algunos minutos. Al usuario le aparecerá un listado de aplicaciones dependientes junto con el estado de su instalación.

**Delegación y no delegación de las aplicaciones con requisitos previos de los espacios**

- Las aplicaciones con requisitos previos vinculadas a una aplicación (la aplicación principal) se delegan automáticamente cuando la aplicación principal se delega a un subespacio.
- Si la aplicación principal no está delegada a un subespacio, las aplicaciones con requisitos previos tampoco lo estarán en los casos en los que las aplicaciones con requisitos previos no estén explícitamente distribuidas. De todos modos, en las aplicaciones con requisitos previos que están vinculadas a más de una aplicación principal no se podrá cancelar la delegación.
- Si las aplicaciones con requisitos previos están explícitamente delegadas, entonces no se puede cancelar su delegación automáticamente.

## Delegar permisos de dispositivos delegados para aplicaciones internas de Android Enterprise

Se pueden asignar permisos delegados a aplicaciones internas que se pueden aplicar a dispositivos gestionados por Android Enterprise y dispositivos AMA.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Aplicaciones > Catálogo de aplicaciones**.
:::

:::WorkflowBlockItem
En el **App Catalog**, seleccione la aplicación para la que desee delegar permisos de dispositivos.
:::

:::WorkflowBlockItem
Haga clic en la pestaña **Configuraciones de la aplicación**.
:::

:::WorkflowBlockItem
En Permisos delegados (aplicación interna Android Enterprise), seleccione los permisos necesarios para las aplicaciones:
:::

:::WorkflowBlockItem
Solo la implementación de COSU usa AMAPI. Consulte la sección AMAPI para obtener más información.

- **Configurar permisos del tiempo de ejecución de aplicaciones de terceros**
- **Ocultar y suspender aplicaciones de terceros**
- **Administrar certificados**
- **Gestionar las configuraciones de las aplicaciones**
- **Administrar el bloqueo de la desinstalación de aplicaciones**
- **Gestionar la habilitación de aplicaciones del sistema**
- **Administrar la selección de certificados** (no compatible con el modo AMAPI)
- **Administrar la retención de aplicaciones no instaladas** (no compatible con el modo AMAPI)
- **Gestionar la recopilación de redes** (compatible solo con una aplicación a la vez)
- **Gestión de la recopilación de registros de seguridad** (compatible solo con una aplicación a la vez)
- **Administrar la instalación de aplicaciones existentes** (no compatible con el modo AMAPI)
- **Instalar y eliminar paquetes** (no compatible con el modo AMAPI)
  La opción Instalar y desinstalar paquetes está disponible en todos los dispositivos que admiten el modo propietario del dispositivo Android (7.0 o posterior). Hay otros permisos delegados que solamente son aplicables a Android 8.0 o posterior.

Configure las opciones de distribución seleccionando entre **A todas las personas con la aplicación**, **A nadie** o **Personalizado**.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::
::::

## Mostrar el estado del perfil de aprovisionamiento para las aplicaciones internas de iOS

Mostrar el perfil del estado de aprovisionamiento de la página del Catálogo de aplicaciones para las aplicaciones internas de iOS. La información sobre herramientas que hay junto al nombre del perfil muestra el número de días que quedan para que el perfil caduque. Este estado puede resultar útil para comprobar cuándo van a caducar los perfiles de aprovisionamiento para las aplicaciones internas.

Este estado es útil para solucionar problemas de aplicaciones que no se instalan porque el perfil va a caducar. Si no hay un perfil de aprovisionamiento adecuado, las aplicaciones se instalan pero no se abrirán ni se iniciarán.

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Haga clic en el icono del engranaje que hay en la parte superior derecha para que aparezcan las columnas.
3. Seleccione **Perfil de aprovisionamiento&#x20;**&#x70;ara ver la columna de la lista de aplicaciones en la página del App Catalog.

Los detalles del Perfil de aprovisionamiento también están disponibles en la página de detalles de la aplicación, bajo la sección Ajustes del perfil de aprovisionamiento.

## Actualizar el perfil de aprovisionamiento para las aplicaciones internas de iOS

El perfil de aprovisionamiento se aplica a una aplicación interna específica de iOS. Los detalles del perfil de aprovisionamiento de una aplicación están disponibles en la página de detalles de la aplicación. Es necesario tener un perfil de aprovisionamiento que no haya caducado para iniciar una aplicación interna iOS en el dispositivo. Si ha caducado, se puede actualizar el perfil de aprovisionamiento cargando el perfil de la página de detalles de la aplicación.

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Haga clic en la aplicación para la que es necesaria la actualización del perfil de aprovisionamiento. Aparecerá la página de detalles de la aplicación.
3. Haga clic en **Editar**.
4. En la sección **Perfil de aprovisionamiento**, haga clic en **Elegir archivo**.
5. Seleccione el archivo de perfil de aprovisionamiento (extensión de archivo .mobileprovision) que desea actualizar y haga clic en **Guardar**.

## Implementar aplicaciones internas en Google Play

Cargue las aplicaciones internas en el canal privado de Google Play e impórtelas a Ivanti Neurons para MDM para su despliegue en dispositivos con Android Enterprise.

**Procedimiento**

1. Inicie sesión en la consola de aplicaciones privadas de Google: [**https://play.google.com/apps/publish**](https://play.google.com/apps/publish).
2. Haga clic en **Todas las aplicaciones** en el menú de la izquierda.
3. Haga clic en **Crear nueva aplicación** e introduzca un nombre para dicha aplicación.
4. Haga clic en **Cargar APK** para cargar el archivo .apk que ha generado.
5. Haga clic en **Listado de tiendas**:\* Introduzca una breve descripción y una descripción completa.
   - Cargue la captura de pantalla para todas las pestañas.
   - Cargue un icono de alta resolución.
   - Cargue un icono gráfico de características (graphic.png).
   - Introduzca la información obligatoria para Categorización, Detalles de contacto y Política de privacidad.
   - Complete el cuestionario de calificación de la aplicación.
6. Haga clic en **Precios y distribución**.  Si ya ha introducido toda la información obligatoria, aparecerá «Listo para publicarse» en la parte superior de la pantalla.
7. Vaya a la pestaña Aplicaciones de Ivanti Neurons for MDM.
8. Haga clic en **Actualizar catálogos disponibles** para sincronizar sus aplicaciones privadas.pueden pasar varias horas hasta que su aplicación se publique.

## Añadir una aplicación web para dispositivos con Android Enterprise

Una aplicación web es un enlace a cualquier sitio web, que se instala en el dispositivo en forma de acceso directo. Las aplicaciones web funcionan del mismo modo que cualquier otra aplicación, lo cual significa que se puede distribuir siguiendo los mismos criterios que una aplicación. Aparece en el catálogo de aplicaciones y la pueden instalar los usuarios del mismo modo que cualquier otra aplicación. No obstante, las aplicaciones web puede que tengan una sola versión y que no se admita la instalación silenciosa. Las aplicaciones web utilizan clips web y se instalan en el dispositivo como configuraciones, pero funcionan como aplicaciones.

Configure un clip web como aplicación en el catálogo de aplicaciones para que la aplicación web esté disponible para los usuarios en el catálogo de aplicaciones. El clip web se puede definir como una configuración, pero esta solo la puede distribuir el administrador. Los usuarios pueden optar por instalar la aplicación web en sus dispositivos o no hacerlo, mientras que no pueden rechazar la configuración del clip web.

En Android Enterprise, una aplicación web es una forma incrustada de aplicación web que se ejecuta sobre Google Chrome dentro del perfil de trabajo. Puede combinarse con una VPN o soluciones SSO en Android Enterprise. Después de crear una aplicación web, la aplicación funciona como cualquier otra aplicación de Android, que usted podrá distribuir según sea necesario. Las aplicaciones web requieren que Chrome esté instalado en el Perfil de trabajo del Dispositivo propiedad de la empresa para poder ejecutarse.

Si hay algún problema con el uso de esta función, los administradores pueden ponerse en contacto con la [**asistencia técnica**](./Abrir_un_tique_de_asistencia.md).

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Aplicaciones > Catálogo de aplicaciones**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir** (arriba a la izquierda).
:::

:::WorkflowBlockItem
Seleccione **Google Play** de la lista desplegable para buscar una aplicación en la Google Play Store. Google Play iFrame se muestra si Android Enterprise está inscrito.
:::

:::WorkflowBlockItem
Haga clic en **Aplicaciones web**.

::Image[]{src="Resources/Images/web-apps-google-play.png" signedSrc="Resources/Images/web-apps-google-play.png" size="50" caption="Añadir aplicaciones web para dispositivos con Android Enterprise" alt="Añadir aplicaciones web para dispositivos con Android Enterprise" isUploading="false" sha initialPath="Resources/Images/web-apps-google-play.png" githubPath="Resources/Images/web-apps-google-play.png" position="flex-start"}
:::

:::WorkflowBlockItem
Describa la aplicación para los usuarios:

::Image[]{src="Resources/Images/web-apps-google-play-details.png" signedSrc="Resources/Images/web-apps-google-play-details.png" size="47" caption="Detalles de la aplicación web" alt="Detalles de la aplicación web" isUploading="false" sha initialPath="Resources/Images/web-apps-google-play-details.png" githubPath="Resources/Images/web-apps-google-play-details.png" position="flex-start"}
:::

:::WorkflowBlockItem
1. Título o nombre de la aplicación.
2. URL de la aplicación.
3. Tipo de visualización para la aplicación web.
4. Icono de carga, que puede ser una imagen PNG o JPEG cuadrada de 512px.
   Haga clic en **Crear**. Espere a que la aplicación se publique en iFrame. Esto puede tardar algunos minutos. Puedes cerrarla y volver más tarde.
:::

:::WorkflowBlockItem
Una vez que la aplicación web esté publicada, importe la aplicación al app catalog para su distribución. Haga clic en el icono de la aplicación web.
:::

:::WorkflowBlockItem
Desplácese hacia abajo y haga clic en **Seleccionar**.
:::

:::WorkflowBlockItem
Añada categorías y una descripción opcional.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones para la delegación de aplicaciones:
:::

:::WorkflowBlockItem
- Delegar esta aplicación a todos los espacios.
- No delegar esta aplicación a todos los espacios.
  Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione una opción de distribución para la aplicación.
:::

:::WorkflowBlockItem
Haga clic en **Finalizar**.
:::
::::

Después de añadir una aplicación web, puede editarla siempre que lo necesite. Para hacerlo:

1. En la página **App Catalog**, haga clic en el nombre de la aplicación web existente.
2. Haga clic en **Editar** para editar los campos de la aplicación web.

## Añadir una aplicación web para dispositivos iOS

Una aplicación web es un enlace a cualquier sitio web, que se instala en el dispositivo en forma de acceso directo. Las aplicaciones web funcionan del mismo modo que cualquier otra aplicación, lo cual significa que se puede distribuir siguiendo los mismos criterios que una aplicación. Aparece en el catálogo de aplicaciones y la pueden instalar los usuarios del mismo modo que cualquier otra aplicación. No obstante, las aplicaciones web puede que tengan una sola versión y que no se admita la instalación silenciosa. Las aplicaciones web utilizan clips web y se instalan en el dispositivo como configuraciones, pero funcionan como aplicaciones.

Configure un clip web como aplicación en el catálogo de aplicaciones para que la aplicación web esté disponible para los usuarios en el catálogo de aplicaciones. El clip web se puede definir como una configuración, pero esta solo la puede distribuir el administrador. Los usuarios pueden optar por instalar la aplicación web en sus dispositivos o no hacerlo, mientras que no pueden rechazar la configuración del clip web.

Si hay algún problema con el uso de esta función, los administradores pueden ponerse en contacto con la [**asistencia técnica**](./Abrir_un_tique_de_asistencia.md).

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Aplicaciones > Catálogo de aplicaciones**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir** (arriba a la izquierda).
:::

:::WorkflowBlockItem
Haga clic en **Aplicaciones web**.
:::

:::WorkflowBlockItem
Describa la aplicación para los usuarios:
:::

:::WorkflowBlockItem
1. Nombre de la aplicación.
2. URL de la aplicación.
3. Tipo de plataforma.
4. Icono de la aplicación.
5. Añada o elimine categorías.
6. Pantalla completa: seleccione esta opción para que la aplicación web se muestre a pantalla completa.
7. Extraíble: seleccione esta opción para hacer que la aplicación web sea extraíble.
8. Haga clic en **Siguiente**.
   Seleccione una de las siguientes opciones para la delegación de aplicaciones:
:::

:::WorkflowBlockItem
- Delegar esta aplicación a todos los espacios.
- No delegar esta aplicación a todos los espacios.
  Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione una opción de distribución para la aplicación.
:::

:::WorkflowBlockItem
Haga clic en **Finalizar**.
:::
::::

### Edición de una aplicación web

Después de añadir una aplicación web, puede editarla siempre que lo necesite.

**Procedimiento**

1. En la página **App Catalog**, haga clic en el nombre de la aplicación web existente.
2. Haga clic en **Editar** para editar los campos de la aplicación web.

## Implementar lentamente las aplicaciones

El ajuste de implementación lenta permite a los administradore implementar automática y gradualmente la nueva versión de las aplicaciones en los dispositivos. La opción Utilizar el método de distribución de implementación lenta está disponible cuando se instala la siguiente versión de la aplicación. El portal administrativo de Ivanti Neurons for MDM le permite editar aplicaciones aun cuando la implementación lenta esté pausada.

Una vez que se establece la implementación lenta para una versión, se aplica para las siguientes con el mismo porcentaje que se estableció la última vez. Puede pausar la distribución de una aplicación si la distribución está configurada al 100 %. Sin embargo, si establece el objetivo de distribución al 100 %, debe establecer manualmente el porcentaje de objetivo de distribución para la siguiente versión, ya que la interfaz de usuario restablece el porcentaje al 0% .

**Procedimiento**

|   | 1. | Vaya a **App Catalog**, **Aplicaciones**, y seleccione una de las opciones de modo de distribución. |
| - | -- | --------------------------------------------------------------------------------------------------- |

|   | 2. | Seleccione la opción **% de dispositivos en el resumen de la selección (implementación lenta)**. |
| - | -- | ------------------------------------------------------------------------------------------------ |

|   | 3. | **Desde la configuración de implementación lenta**, arrastre el control deslizante en **Especificar el % objetivo de distribución**. |
| - | -- | ------------------------------------------------------------------------------------------------------------------------------------ |

|   | 4. | Haga clic en **Confirmar** y, luego, haga clic en **Hecho**. Se muestra el estado de la última versión de la aplicación. La página del App Catalog indica el estado de IMPLEMENTACIÓN LENTA en la tabla. |
| - | -- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

Si no puede realizar las tareas en la página **App Catalog**, puede ser que no tenga los permisos necesarios. Necesita el rol de Administración de aplicaciones y contenido.

## Uso de la búsqueda avanzada

Puede utilizar la opción de Búsqueda avanzada para buscar una aplicación en función de reglas para identificar y ver las aplicaciones con criterios específicos. Estas reglas se pueden crear usando los operadores correspondientes, como «igual a», «es menor que», «es mayor que», «está igual que» y «no es igual que». Las opciones de reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Las aplicaciones que coinciden con las reglas se muestran debajo de la sección.

Los valores de los atributos personalizados que se usan en Buscar distinguen entre mayúsculas y minúsculas.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Desde la página del Catálogo de aplicaciones, haga clic en el enlace **Búsqueda avanzada**. Se abre el asistente de Búsqueda avanzada.
:::

:::WorkflowBlockItem
Haga clic en una de las siguientes opciones:
:::

:::WorkflowBlockItem
- **Cualquiera**: si las aplicaciones deben cumplir al menos una de las reglas
- **Todas**: si las aplicaciones deben cumplir todas la regla
  Para crear una regla que defina los criterios de búsqueda, seleccione una de las opciones siguientes y seleccione la acción asociada adecuada:- AppConnect activado
- Valoración media
- ID de paquete
- Categoría
- Coste
- Atributos personalizados
- Fecha en que se agregó a AppCatalog
- Fecha de modificación
- Distribución de dispositivos
- Distribución de grupos de dispositivos
- Tipo de dispositivo
- Distribución de grupo
- Versión de SO mínima
- Nombre
- Plataforma de SO
- Perfil de aprovisionamiento
- Tamaño
- Fuente
- Distribución de usuarios
- Nombre de los grupos de usuarios
- Versión
:::

:::WorkflowBlockItem
(Opcional) Haga clic en **+** para crear reglas adicionales, si fuera necesario.
:::

:::WorkflowBlockItem
Haga clic en **Buscar**. Se muestra la lista de aplicaciones que coinciden con los criterios de búsqueda.
:::
::::

### Carga de las consultas de búsqueda

Puede ver la lista de consultas de búsqueda guardadas.

**Procedimiento**

1. Haga clic en Búsqueda avanzada y luego en el icono de la carpeta. La lista de las consultas de búsqueda creadas se muestra en la sección **Cargar consulta** y se muestran los detalles siguientes:\* **Nombre de la consulta**: el nombre de la consulta cargada.
   - **Contenido de la consulta** muestra el contenido de las reglas que definen la consulta de búsqueda.
   - **Acciones**: seleccione la acción que se realizará en la consulta.
2. Haga clic en **Cargar consulta** en la columna **Acciones** para ver la lista de aplicaciones que coinciden con los criterios definidos en la consulta cargada.
3. Haga clic en **Eliminar** para borrar una consulta guardada.

## Exportación de aplicaciones a un archivo CSV

Puede exportar las aplicaciones mediante la opción Exportar a CSV de la página App Catalog.

**Procedimiento**

1. Vaya a **Aplicaciones** > **Catálogo de aplicaciones**.
2. Haga clic en la opción **Exportar a CSV** para exportar la lista de aplicaciones y detalles relacionados a un archivo CSV.Solo se incluyen las aplicaciones que figuran en el espacio seleccionado, y todos los resultados paginados se compilan en un único archivo.El uso de filtros o resultados de búsqueda exportará solo las aplicaciones relevantes.
3. Aparecerá un mensaje con los botones **Continuar** y **Cancelar** que indicará si se ha iniciado el proceso de exportación y que en breve estará disponible un informe.
4. Haga clic en **Continuar** y espere a que se complete la solicitud para enviar otra.
5. Aparecerá un mensaje que indica que **App Catalog: le informe CSV ha finalizado** con los botones **Descargar** y **Eliminar**.
6. Haga clic en **Descargar** para descargar el informe.
7. (Opcional) Haga clic en **Eliminar&#x20;**&#x70;ara eliminar el informe.

La opción **Exportar a CSV** se volverá a activar solo después de seleccionar la opción **Descargar** o **Eliminar**.

Si hay varias versiones de una aplicación, se mostrará una entrada por cada versión.

**Temas relacionados**

- [**Funciones del usuario**](./Funciones_del_usuario.md)
- [**Eliminar aplicaciones del App Catalog**](./Eliminar_aplicaciones_del_App_Catalog.md)
