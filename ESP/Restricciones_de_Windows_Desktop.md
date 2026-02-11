---
title: Restricciones de Windows Desktop
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Disponible para: Windows 10 Desktops**

Esta sección contiene los siguientes temas:

- [**Configuración de las restricciones para Windows Desktop**](./Restricciones_de_Windows_Desktop.md)
- [**Creación de una lista de permitidos para dispositivos de almacenamiento extraíbles**](./Restricciones_de_Windows_Desktop.md)

Los administradores puede controlar la información del sistema operativo en dispositivos administrados Windows 10 Desktop restringiendo el acceso del usuario a las siguientes áreas de un dispositivo:

- Panel de control
- Administrador de tareas
- Explorador de archivos
- Editor del registro

Las funciones anteriormente mencionadas permiten al usuario realizar una gran cantidad de cambios en su dispositivo. Mediante esta característica, los administradores pueden restringir el acceso a estos controles del nivel de sistema y, por ende, segurizar el acceso.

Esta característica requiere Bridge. Vaya a [**Ivanti Bridge**](./Ivanti_Bridge.md) para obtener más información.

## Configuración de las restricciones para Windows Desktop

**Procedimiento**

1. Vaya a **Configuración > +Añadir**.
2. Seleccione la configuración **Restricciones de escritorio de Windows**.
3. Introduzca un nombre para la configuración.
4. Introduzca una descripción.
5. En la sección Establecimiento de la configuración, especifique los demás ajustes según se describe en la siguiente tabla.| **Ajuste**                                    | **Qué hacer**                                                                                                                                                                                                                                                                                         |
   \| --------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Administrador de tareas**                   | Seleccione la casilla **Denegar acceso** para el ajuste al que se debe negar el acceso.                                                                                                                                                                                                               |
   \| **Panel de control**                          |                                                                                                                                                                                                                                                                                                       |
   \| **Editor del registro**                       |                                                                                                                                                                                                                                                                                                       |
   \| **Explorador de archivos**                    | Seleccione la casilla **Restringir capacidades** para restringir las funciones del Explorador de archivos. Ejemplo: desinstalación de la opción «Conectar a unidad de red».Haga clic en el enlace proporcionado para ver la lista de funciones que están restringidas.                                |
   \| **Almacenamiento extraíble**                  |                                                                                                                                                                                                                                                                                                       |
   \| Acceder al modo para almacenamiento extraíble | \* **Restringir acceso de lectura**: esta opción impide cualquier acceso y es la configuración más restrictiva.
   - **Restringir acceso de escritura**: esta opción permite un acceso limitado, pero impide la eliminación no autorizada de datos o la posibilidad de añadir virus, etc. al dispositivo. |
6. Haga clic en **Siguiente**.
7. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
   - Ningún dispositivo (predeterminada)
   - personalizada
8. Haga clic en **Hecho**.Para que la configuración entre totalmente en vigor, el dispositivo debe reiniciarse después de haber aplicado dicha configuración.

## Creación de una lista de permitidos para dispositivos de almacenamiento extraíbles

Si desea crear una lista de permitidos de dispositivos de almacenamiento permitidos, complete primero los siguientes pasos.

- Conecte a un PC los dispositivos de almacenamiento USB que desea permitir.
- Abra el Administrador de dispositivos y haga clic en el controlador USB.
- Observe los ajustes de cada controlador para ver la información sobre el dispositivo.
- Almacene la información del dispositivo que usará para crear su lista de permitidos.

Para crear una lista de permitidos para dispositivos de almacenamiento extraíbles:

**Procedimiento**

1. En la página de configuración de **Restricciones de escritorio de Windows**, haga clic en **+Añadir**, en la sección **lista de permitidos de Almacenamiento extraíble**.
2. En la ventana **Agregar ID de hardware**, introduzca la ID de hardware para uno o más dispositivos que desee eliminar de la lista Permitir y bloquear como dispositivos de almacenamiento.
3. Haga clic en **Añadir las Id. de hardware**. La lista de las Id. de hardware que están en la lista de permitidos aparecerán en la sección **lista de permitidos de Almacenamiento extraíble autorizado**.Para editar o eliminar la identificación de un equipo de la lista, seleccione la opción Editar o Eliminar en la columna **Acciones**.Para que la configuración entre totalmente en vigor, el dispositivo debe reiniciarse después de haber aplicado dicha configuración.
