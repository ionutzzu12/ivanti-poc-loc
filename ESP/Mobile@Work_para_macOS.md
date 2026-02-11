---
title: Mobile@Work para macOS
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Configuración de Mobile@Work para macOS y flujo de trabajo de la ejecución de secuencias de comandos**](./Mobile@Work_para_macOS.md)
- [**Crear una configuración de Mobile@Work para macOS**](./Mobile@Work_para_macOS.md)
- [**Habilitación de la incorporación de los usuarios para dispositivos macOS**](./Mobile@Work_para_macOS.md)
- [**Crear una configuración de secuencia de comandos de Mobile@Work para macOS**](./Mobile@Work_para_macOS.md)
- [**Realizar una desinstalación limpia de Mobile@Work para macOS**](./Mobile@Work_para_macOS.md)

Ivanti Neurons for MDM le permite crear sus propias secuencia de comandos de shell de macOS que luego pueden cargarse y Ivanti Neurons for MDMejecutarse en dispositivos macOS administrados. Para obtener información sobre cómo crear, cargar y administrar el repositorio de secuencias de comandos, consulte [**Todas las secuencias de comandos**](./Todas_las_secuencia_de_comandos.md).

Un usuario de dispositivos macOS puede iniciar el dispositivo que se va a retirar con Mobile\@Work para macOS 1.1 o posterior. La opción de retirar está disponible al hacer clic en **Desinstalar** en la pantalla Acerca de Mobile\@work. En Ivanti Neurons for MDM, puede verificar el estado del dispositivo en la página **Dispositivos** y en la página de detalles del dispositivo.

Mobile\@Work para macOS 1.5 o posterior abre Apps\@Work inmediatamente después del registro sin esperar a que se complete el registro de MDM.

En Mobile\@Work para macOS, haga clic en un mosaico de aplicación para mostrar la página Detalles de la aplicación para esa aplicación. La página incluye la descripción de la aplicación, las capturas de pantalla, las puntuaciones y las opiniones.

Mobile\@Work para macOS notifica al servidor de Ivanti Neurons for MDM si las aplicaciones internas macOS con marca registrada de Packager están o no instaladas en el informe del inventario.

**Requisitos previos**

En el [**App Catalog**](./Catálogo_de_aplicaciones.md), el cliente Mobile\@Work para macOS está disponible como aplicación corporativa. Antes de poder ejecutar secuencia de comandos de shell en dispositivos macOS, pida a los usuarios que registren sus dispositivos con Ivanti Neurons for MDM mediante Mobile\@Work para macOS.

**Procedimiento**

1. Descargue la aplicación Mobile\@Work para macOS. Está disponible como un archivo PKG en [**https://support.mobileiron.com/support/CDL.html**](https://support.mobileiron.com/support/CDL.html). Consulte [**este artículo del foro de clientes de Ivanti**](https://forums.ivanti.com/s/article/MobileIron-Downloads-credential-information) para obtener información sobre cómo obtener la credenciales para el sitio de descarga.
2. Cargue el archivo PKG de Mobile\@Work para macOS en un servidor seguro. Este nunca debe ser accesible para los usuarios de los dispositivos.
3. Comparta la URL del archivo de instalación de Mobile\@Work para macOS con los usuarios del dispositivo por correo electrónico o mensaje.
4. Pídales a los usuarios que hagan lo siguiente:1) Descargue e instale Mobile\@Work para macOS en el dispositivo.
   2\) Registrar los dispositivos con Ivanti Neurons for MDM utilizando Mobile\@Work para macOS.

## Configuración de Mobile\@Work para macOS y flujo de trabajo de la ejecución de secuencias de comandos

**Procedimiento**

1. Configure y distribuya una configuración de Mobile\@Work para macOS.
2. Configure y distribuya una configuración de script de Mobile\@Work para macOS para cargar el script Ivanti Neurons for MDM. Las secuencia de comandos están cifrados y firmados mediante certificado firmado, que es único para cada abonado. La clave para descifrar la secuencia de comandos se envía al dispositivo junto con la URL de descarga de la secuencia de comandos, que está cifrado y firmado.
3. Ivanti Neurons for MDM ejecuta las secuencias de comandos en dispositivos macOS mediante Mobile\@Work para macOS. Mobile\@Work para macOS sondea a Ivanti Neurons for MDM periódicamente para controlar si hay secuencias de comandos en espera de ejecución. En el caso de que haya alguna secuencia de comandosen la cola, Mobile\@Work descargaría y ejecutaría las secuencias de comandos en los dispositivos macOS según los ajustes que usted haya definido en Ivanti Neurons for MDM.
4. Mobile\@Work para macOS obtiene los resultados de la ejecución de la secuencia de comandos para Ivanti Neurons for MDM, y estos se muestran en los registros del dispositivo. Puede verificar los registros del dispositivo desde la página de detalles del dispositivo macOS, en la pestaña **Registros**.

## Crear una configuración de Mobile\@Work para macOS

Hay disponible una configuración predeterminada de Mobile\@Work para macOS. Sin embargo, no se distribuye a ningún dispositivo de forma automática.

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **work** en el campo de búsqueda y, a continuación, haga clic en la configuración **Mobile\@Work para macOS**.
4. Asigne un nombre a la configuración y descríbala.
5. Introduzca el **Tiempo máximo de ejecución** en segundos para especificar cuánto tiempo puede ejecutarse una secuencia de comandos. El valor predeterminado es de 60 segundos.
6. Introduzca el **Tamaño máximo de respuesta&#x20;**&#x65;n kilobytes (KB) para especificar el límite del tamaño de la salida de la secuencia de comandos devuelta a Ivanti Neurons for MDM. Es decir, los datos stdout o stderr devueltos al ejecutar la secuencia de comandos. El valor predeterminado es 1 KB.
7. Introduzca la **Frecuencia de conexión&#x20;**&#x65;n minutos para especificar con qué frecuencia debe la aplicación Mobile\@Work para macOS ingresar en Ivanti Neurons for MDM. El valor predeterminado es de 15 minutos.
8. (Opcional) Puede activar la incorporación de usuarios para dispositivos macOS mediante la sección [**Activación de la incorporación de usuarios para dispositivos macOS**](./Mobile@Work_para_macOS.md).
9. Haga clic en **Siguiente** para configurar los ajustes de distribución.1) Elija un nivel de distribución:
   2\) **Para todo el mundo:** la aplicación se añade a los dispositivos compatibles de todos los usuarios.
   3\) **A nadie:** la aplicación se almacena para distribuirse posteriormente.
   4\) **Distribución personalizada**: seleccione cualquiera de las siguientes opciones:\* **Usuarios/Grupos de usuarios**: la aplicación solo se distribuye a los usuarios o grupos de usuarios que usted elija.Haga clic en la pestaña **Usuarios** para seleccionar los usuarios.Haga clic en la pestaña **Grupos de usuarios** para seleccionar los grupos de usuarios.
   - **Dispositivos/Grupos de dispositivos:** la aplicación solo se distribuye a los dispositivos o grupos de dispositivos que usted elija.Haga clic en la pestaña **Dispositivos** para seleccionar el o los dispositivos.Haga clic en la pestaña **Grupos de dispositivos** para seleccionar los grupos de dispositivos.
10. Haga clic en **Listo**.

## Habilitación de la incorporación de los usuarios para dispositivos macOS

Puede habilitar la incorporación de usuarios a los dispositivos macOS durante el proceso automatizado de Inscripción de dispositivos, como sigue:

- Tan pronto como se completa la Inscripción de dispositivos, Mobile\@Work para macOS (se requiere la versión 1.68 o posterior) se inserta en el dispositivo junto con los perfiles, configuraciones y aplicaciones.
- El cliente Mobile\@Work para macOS y otras aplicaciones se insertan a los dispositivos solo si:\* Las aplicaciones son aplicaciones PKG internas o aplicaciones públicas de Apps and Books de Apple.
  - La configuración de la instalación silenciosa de las aplicaciones está ajustada en «true» (verdadero). El ajuste está disponible en la página **Aplicaciones** > [**Detalles de la aplicación**](./Configuración_de_aplicaciones.md) > **Configuración de la aplicación** > **Instalación en el dispositivo**.
  - La [**prioridad para las aplicaciones**](./Configuración_de_aplicaciones.md) se establece en Alta. De manera predeterminada, la prioridad de la aplicación de cliente de Mobile\@Work para macOS se establece en alta (y no se puede modificar), ya que **sin esta configuración, el proceso de incorporación de usuario podría fallar.**
  - Las aplicaciones están configuradas distribuirse a los dispositivos, grupos de usuarios o grupos de dispositivos.
- Una vez que Mobile\@Work para macOS se instala y registra, el dispositivo macOS entra en el modo kiosco (es decir, el usuario no tiene control sobre el dispositivo) hasta que se configuren e instalen los perfiles, configuraciones y aplicaciones restantes. El progreso se muestra en pasos.

Para versiones de Mobile\@Work para macOS 1.73 o posteriores, según sea compatible con Ivanti Neurons for MDM, se admiten las siguientes características adicionales:

- El proceso de incorporación del usuario se completa poco después de que se completa la Inscripción de dispositivos para un dispositivo. El proceso de incorporación de los usuarios no comenzará después de que expire la ventana de tiempo para activar la incorporación de los usuarios (generalmente 20 minutos después del registro del dispositivo) incluso si un administrador la activa en la configuración de Mobile\@Work. Esto impide que el dispositivo acceda en modo kiosco de incorporación del usuario cuando el dispositivo está en uso regular.
- El proceso de incorporación del usuario se muestra por pasos en el cliente Mobile\@Work para macOS. Las configuraciones se instalarán como parte del primer paso.
- Las aplicaciones de alta prioridad se instalarán inicialmente. Cada aplicación de alta prioridad contará como un paso. Las aplicaciones de propiedad de Packager no se cuentan como parte de los pasos.
- El resto de aplicaciones seguirán instalándose en segundo plano incluso después de que se haya completado la incorporación del usuario. Las aplicaciones se marcan como instaladas después de que la instalación se inicie en un dispositivo o después de que la aplicación se instale realmente en el dispositivo.
- Después de que se incorpore el usuario, usted puede ir a la página de detalles del dispositivo para verificar las configuraciones y aplicaciones que se han introducido en cada dispositivo. En los registros encontrará más información disponible.

**Procedimiento**

1. Cree una configuración de Mobile\@Work para macOS con [**Crear una configuración de Mobile@Work para macOS**](./Mobile@Work_para_macOS.md).
2. Seleccione la opción **Habilitar incorporación de usuario.**
3. Introduzca los siguientes detalles:\* **Valor de espera de la incorporación de los usuario**: introduzca el tiempo aproximado que tardará el dispositivo en instalar la aplicación y las configuraciones durante la configuración inicial del dispositivo. Por defecto, el proceso de incorporación del usuario en un dispositivo macOS caduca en 120 segundos, un tiempo que usted puede modificar según sea necesario.
   - **URL de la página de aterrizaje del usuario**: proporciona una URL de la página de aterrizaje que se mostrará al usuario una vez que se haya completado la incorporación.
4. Haga clic en **Siguiente** para configurar los ajustes de distribución.
5. Haga clic en **Listo**.

## Creación de una configuración de secuencia de comandos Mobile\@Work para macOS

Puede crear y distribuir múltiples configuraciones de secuencia de comandos de Mobile\@Work para macOS en los dispositivos. Con esta configuración, puede seleccionar una secuencia de comandos del repositorio (**Administrador >&#x20;**[**Todas las secuencia de comandos**](./Todas_las_secuencia_de_comandos.md)) para distribuirla a Mobile\@Work para macOS.

Puede programar ejecuciones de secuencia de comandos en dispositivos con Mobile\@Work para macOS 1.66 o versiones posteriores. Si programa la ejecución de una secuencia de comandos para que se ejecute en dispositivos con Mobile\@Work para versiones de cliente de macOS anteriores a la 1.66, la secuencia de comandos se ejecutará solo una vez. Si el cliente Mobile\@Work para macOS se actualiza de la versión 1.4 a la 1.66, todas las configuraciones del cliente macOS se redistribuirán a los dispositivos.

**Requisitos previos**

- Vaya a **Administración >&#x20;**[**Todas las secuencias de comandos**](./Todas_las_secuencia_de_comandos.md) para cargar y administrar secuencias de comandos que pueden utilizarse en esta configuración y distribuirse a los dispositivos.
- Configure y distribuya la configuración de Mobile\@Work para macOS en los dispositivos. De lo contrario, la configuración de la secuencia de comandos de Mobile\@Work para macOS tendrá el estado «Error».

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **work** en el campo de búsqueda y, a continuación, haga clic en la configuración de **Secuencia de comandos de Mobile\@Work para macOS**.
4. Asigne un nombre a la configuración y descríbala.
5. En el campo **Seleccionar secuencia de comandos**, introduzca el nombre de la secuencia de comandos que desea buscar y selecciónelo en la lista desplegable.
6. En la sección Entrada de la secuencia de comandos, se muestran las etiquetas de entrada de la secuencia de comandos y las variables de la secuencia de comandos asociadas a la misma. Si debe anularlas, introduzca variables de secuencias de comandos alternativas (por ejemplo, \{$userWorkEmailAddress}) y sus valores predeterminados alternativos (por ejemplo, [**john.doe@company.com**](mailto\:john.doe@company.com)).
7. En la sección Ejecución de la secuencia de comandos, seleccione una de las siguientes opciones de programación:\* Ejecutar una vez en la implementación
   - Ejecución periódica
8. Si selecciona Ejecución periódica, especifique la siguiente información detallada:\* Zona horaria a utilizar: seleccione la hora local o la hora UTC del dispositivo. La secuencia de comandos se ejecutará a la hora seleccionada en este campo.
   - La ejecución comienza el: seleccione la fecha de inicio.
   - La ejecución finaliza el: seleccione la fecha de fin (posterior o igual a la fecha de inicio).
   - Ejecutar secuencia de comandos: seleccione Diario o Semanal e introduzca las horas (en formato de 24 horas), minutos y días, según corresponda.
9. Haga clic en **Siguiente** para configurar los ajustes de distribución.
10. Haga clic en **Listo**.

## Realizar una desinstalación limpia de Mobile\@Work para macOS

Si activó la opción **Eliminar aplicaciones al desinscribirse**&#xNAN;**(disponible solo para aplicaciones gestionadas)** durante la instalación de Mobile\@Work para macOS y si inicia la eliminación del dispositivo desde el portal del administrador de Ivanti Neurons for MDM, la aplicación Mobile\@Work para macOS y la secuencia de comandos de desinstalación se eliminarán del dispositivo. Para evitar que los procesos y secuencias de comandos se ejecuten en el back-end, asegúrese de que -durante el registro del dispositivo de los nuevos usuarios o la eliminación de los usuarios existentes- se anule la selección de la opción desde el portal del administrador de Ivanti Neurons for MDM, para garantizar que el secuencia de comandos de desinstalación se ejecute y elimine los procesos y secuencias de comandos asociados del back-end.

**Procedimiento**

1. Inicie sesión en el portal del administrador de Ivanti Neurons for MDM
2. Vaya a **Aplicaciones** > **Mobile\@Work** > **Configuraciones de aplicaciones** > **Lista de resumen de configuraciones de aplicaciones** > **Ajustes de aplicaciones Apple** >**Ajustes de configuración de gestión de aplicaciones Apple**.
3. En la página de **ajustes de configuración**, desactive la siguiente opción:\* **Eliminar aplicaciones al cancelar la inscripción (Solo disponible para aplicaciones gestionadas)**.

**Temas relacionados:**

- [**Administrador > Todas las secuencias de comandos**](./Todas_las_secuencia_de_comandos.md)
