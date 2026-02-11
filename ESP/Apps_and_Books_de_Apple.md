---
title: Apps and Books de Apple
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Distribución de licencias de aplicaciones en varias cuentas de Apps and Books de Apple en un espacio**](./Apps_and_Books_de_Apple.md)
- [**Distribución de licencias basadas dispositivos y basadas en usuarios**](./Apps_and_Books_de_Apple.md)
- [**Uso de la opción de licencia basada en el dispositivo**](./Apps_and_Books_de_Apple.md)
- [**Uso de la opción de licencia basada en el usuario**](./Apps_and_Books_de_Apple.md)
- [**Añadir una aplicación de Apps and Books al catálogo**](./Apps_and_Books_de_Apple.md)
- [**Añadir cuentas de Apps and Books**](./Apps_and_Books_de_Apple.md)
- [**Actualización de un token seguro para Apps and Books**](./Apps_and_Books_de_Apple.md)
- [**Actualización de la prioridad de una cuenta de Apps and Books**](./Apps_and_Books_de_Apple.md)
- [**Eliminación de un token seguro de Apps and Books**](./Apps_and_Books_de_Apple.md)
- [**Distribuir licencias para una aplicación de Apps and Books del catálogo**](./Apps_and_Books_de_Apple.md)
- [**Ver licencias de aplicaciones por usuario**](./Apps_and_Books_de_Apple.md)
- [**Notificaciones de uso de licencias de Apps and Books**](./Apps_and_Books_de_Apple.md)
- [**Visualización del uso de licencias de Apps and Books**](./Apps_and_Books_de_Apple.md)
- [**Revocación de la licencia de Apps and Books para una aplicación**](./Apps_and_Books_de_Apple.md)
- [**Comportamiento de Apps and Books para dispositivos macOS y iOS**](./Apps_and_Books_de_Apple.md)
- [**Derecho de licencia de Apps and Books cuando un dispositivo cambia de espacio**](./Apps_and_Books_de_Apple.md)

**Licencia:** Silver

La pantalla **Apps and Books de Apple** solo está disponible si ha configurado Apps and Books de Apple en sus [**ajustes del app catalog**](./Ajustes_del_catálogo.md). Esta pantalla muestra las licencias de aplicaciones que se han comprado para dispositivos Apple a través de And Books de Apple y cuántas se han usado. Utilice esta pantalla para:

- seleccionar las aplicaciones de Apps and Books que se incluirán en su catálogo
- distribuir licencias para aplicaciones de Apps and Books

Para obtener más información sobre las aplicaciones de distribución con Apps and Books, consulte el artículo [**Ivanti Neurons for MDM: cómo distribuir aplicaciones con VPP**](https://forums.ivanti.com/s/article/MobileIron-Cloud-How-to-Distribute-Apps-with-VPP-3465) de la Comunidad de Ivanti.

Es posible que Books de Apple no esté disponible en todos los países o regiones. Para distribuir licencias para las aplicaciones mediante Apps and Books de Apple, debe introducir el sToken proporcionado por Apple.

## Distribución de licencias de aplicaciones en varias cuentas de Apps and Books de Apple en un espacio

- Si existe una misma aplicación en más de una cuenta de Apps and Books, la licencia se distribuirá desde la cuenta en el orden de prioridad de las cuentas.
- Si existe una misma aplicación en más de una cuenta de Apps and Books y si la licencia de la aplicación de la cuenta de Apps and Books con mayor prioridad se ha agotado, a dicha aplicación se le distribuirá una licencia desde la cuenta con la siguiente prioridad solo si el usuario o el dispositivo están presentes en la lista de distribución de licencias de la siguiente cuenta priorizada.
- La licencia no se revocará y reasignará al cambiar la prioridad de las cuentas de Apps and Books. A la aplicación se le distribuirá una licencia desde la primera cuenta. Si se han agotado las licencias en la primera cuenta, a la aplicación se le distribuirá una licencia desde la siguiente cuenta priorizada, y así sucesivamente.
- El usuario tiene la opción de revocar todas las licencias de una aplicación desde la página del App Catalog. Esta acción revocará la licencia de dicha aplicación desde todas las cuentas disponibles de Apps and Books.
- Las licencias reservadas tienen prioridad con respecto a las cuentas de Apps and Books.

## Distribución de licencias basadas dispositivos y basadas en usuarios

La licencia de una aplicación estará basada en dispositivos o en usuarios dependiendo de cómo lo asigne usted. Cuando asigna la licencia de la aplicación a un dispositivo, se convierte en una licencia basada en dispositivo. Cuando asigna la licencia de la aplicación a un usuario, se convierte en una licencia basada en el usuario.

Cuando se instala una aplicación de Apps and Books en un dispositivo, se distribuye una licencia o se publica un token para esa aplicación. Si no hay ninguna licencia disponible para la aplicación, el usuario tiene la opción de instalar y pagar la aplicación él mismo. Si ya se ha asignado a un usuario a una licencia basada en el usuario para la aplicación solicitada de Apps and Books, se instalará la aplicación utilizando la licencia existente basada en el usuario, el lugar de la licencia de Apps and Books.

En el caso de [**Shared iPads**](./Dispositivos_iPad_compartidos_para_empresas.md), Apps and Books se instalan según las licencias basadas en dispositivos, independientemente de si se seleccionan o no licencias basadas en dispositivos.

## Uso de la opción de licencia basada en el dispositivo

Con las licencias basadas en dispositivos, los usuarios no están obligados a inscribirse en Apps and Books. Las aplicaciones obligatorias se instalarán automáticamente. Los dispositivos corporativos supervisados no necesitan usar una Id. de Apple propiedad del departamento informático.

Durante el ingreso del dispositivo, el dispositivo es identificado por su número de serie y se instala la aplicación obligatoria si hay licencias disponibles. Si no hubiera licencias disponibles, la aplicación no se instala. Si la licencia para una aplicación está reservada, la asignación de licencia basada en dispositivo no se producirá durante la instalación de la aplicación.

Las actualizaciones de las aplicaciones implementadas utilizando licencias de Apps and Books basadas en el dispositivo están controladas por el administrador.

Para controlar cómo se va a actualizar una aplicación, en **Aplicaciones > App Catalog**, navegue hasta la pestaña **Configuraciones de aplicaciones/Instalar en dispositivo**. Ahí podrá seleccionar una actualización inmediata que se producirá la próxima vez que se ingrese el dispositivo o bien puede elegir que la aplicación se actualice automáticamente cuando haya disponibles nuevas versiones.

**Importante:**&#x61;ntes de asignar una licencia basada en dispositivo a una aplicación «business to business» (B2B) o de productividad, confirme con el desarrollador de la aplicación que esta sea apta para las licencias basadas en dispositivos.

## Uso de la opción de licencia basada en el usuario

La licencia basada en el usuario seguirá siendo válida para dicho usuario si tiene que pasar de un dispositivo a otro en caso de que el dispositivo se haya perdido o haya sido robado o si el usuario cambia a un dispositivo nuevo. Con las licencias basadas usuarios, el usuario debe inscribirse primero en Apps and Books de Apple. La inscripción es una acción manual que el usuario final debe completar en el Catálogo de aplicaciones. Las aplicaciones obligatorias de Apps and Books no se instalarán en el dispositivo hasta que el usuario se inscriba en Apps and Books.

Si la aplicación es una aplicación obligatoria de Apps and Books y la distribución de licencias está basada en el usuario:

- Las instalaciones de aplicaciones obligatorias no se producirán si el usuario no está inscrito en el programa Apps and Books.
- Se podrán instalar las aplicaciones obligatorias si el usuario está inscrito en el programa Apps and Books y si hay una licencia disponible.
- Si el usuario está inscrito en Apps and Books pero no hay ninguna licencia disponible, la aplicación no se instalará.

## Añadir una aplicación de Apps and Books al catálogo

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione una aplicación y haga clic en **Añadir al catálogo**. Haga clic en **Siguiente**.
3. Opcionalmente, puede añadir una descripción de la aplicación. Haga clic en **Siguiente**.
4. Seleccione una opción de distribución. Haga clic en **Siguiente**.
5. Haga clic en la pestaña **Configuración de la aplicación**.
6. Opcionalmente, puede seleccionar **Instalar en dispositivo**. Esta opción de configuración instalará la aplicación sin solicitar nada al usuario en dispositivos iOS supervisados.
7. Seleccione otras opciones de configuración si fuera necesario.

En la página de detalles del token seguro de Apps and Books, se muestran los siguientes detalles:

- Fecha de creación
- Ubicación (si el token contiene esta información)
- Fecha de caducidad

## Añadir cuentas de Apps and Books

Ivanti Neurons for MDM permite agregar varias cuentas de Apps and Books añadiendo varios tokens seguros de Apps and Books en un solo espacio.

Lleve a cabo los siguientes pasos para agregar un token seguro de Apps and Books en un espacio:

1. Vaya a **Aplicaciones > Apps and Books de Apple**.
2. Haga clic en **+Añadir sToken de Apps and Books**.
3. Introduzca un nombre y elija un archivo del token.
4. Opcionalmente, también puede deseleccionar la opción **Distribuir automáticamente aplicaciones de Apps and Books a todos los usuarios**. Esta opción está seleccionada de forma predeterminada, en cuyo caso se usa el grupo Todos los usuarios para distribuir las licencias en orden de llegada.
5. Opcionalmente, también puede seleccionar la opción **Borrar todos los datos de la licencia de Apps and Books anterior** para borrar todas las licencias de aplicaciones asociadas a este token.
6. Haga clic en **Guardar**.

Una vez que se haya añadido la cuenta, aparecerá en la tabla una lista de todas las cuentas de Apps and Books añadidas.

## Actualización de un token seguro para Apps and Books

**Procedimiento**

1. Vaya a **Aplicaciones > Apps and Books de Apple**.
2. Haga clic en el nombre de la cuenta de Apps and Books.
3. En la pestaña del token, haga clic en **Actualizar sToken** (archivo .stoken).
4. Introduzca el nombre del token y elija un archivo del token.
5. Opcionalmente, también puede deseleccionar la opción **Distribuir automáticamente aplicaciones de Apps and Books a todos los usuarios**. Esta opción está seleccionada de forma predeterminada, en cuyo caso se usa el grupo Todos los usuarios para distribuir las licencias en orden de llegada.
6. Opcionalmente, también puede seleccionar la opción **Borrar todos los datos de la licencia de Apps and Books anterior** para borrar todas las licencias de aplicaciones asociadas a este token.
7. Haga clic en **Actualizar**.

Desde la pestaña del token, haga clic en **Volver a sincronizar la información de uso de la licencia de Apps and Books** para realizar una sincronización completa de toda la información sobre aplicaciones y licencias del servicio de Apps and Books de Apple. Esta acción solo es necesaria si la información sobre la asignación de la licencia de Ivanti Neurons for MDM no es correcta. Esta falta de precisión puede deberse a las incoherencias de las API de Apps and Books de Apple.

## Actualización de la prioridad de una cuenta de Apps and Books

Los administradores pueden asignar una prioridad a cada cuenta de Apps and Books dentro de un espacio dependiendo de dónde se vayan a consumir las licencias. Las prioridades de las cuentas de Apps and Books se utilizan para tener un sistema predecible de distribución de licencias y para resolver conflictos cuando un usuario o dispositivo es apto para recibir una licencia de varias cuentas de Apps and Books para una misma aplicación.

**Procedimiento**

1. Vaya a **Aplicaciones > Apps and Books de Apple**.
2. Haga clic en **Editar prioridad** junto al nombre de cuenta de Apps and Books.
3. En la ventana Editar prioridad, seleccione una nueva prioridad.
4. Haga clic en **Guardar**.

## Eliminación de un token seguro de Apps and Books

La eliminación de un token seguro de Apps and Books es irreversible e implica su destrucción. Cuando se borra un token:

- Se eliminarán los tokens de las aplicaciones que tengan sus tokens reservados.
- Las aplicaciones que se pagaron se mantendrán en el catálogo y los usuarios pueden pagarlas por sí mismos.
- Las aplicaciones que instalaron los usuarios finales a través de la cuenta de Apps and Books corporativa tendrán que transferirse a cuentas personales si los usuarios desean usarlas. Los usuarios tienen un período de gracia de 30 días para hacerlo.

**Procedimiento**

1. Vaya a **Aplicaciones > Apps and Books de Apple**.
2. Haga clic en el nombre de la cuenta de Apps and Books.
3. En la pestaña Token, haga clic en **Eliminar**.
4. En la ventana Eliminación del token seguro de Apps and Books, seleccione la opción **Sí, eliminar el token seguro de Apps and Books** para confirmar.
5. Haga clic en **Eliminar**.

## Distribuir licencias para una aplicación de Apps and Books del catálogo

1. Seleccione **Aplicaciones > Apps and Books de Apple** en el menú principal.
2. Se muestra una lista de cuentas de Apps and Books. En cada cuenta, aparecerá una lista de aplicaciones compradas a través del programa Apps and Books.
   Seleccione una aplicación y haga clic en **Distribuir licencias**.
3. Elija una opción de distribución: **En orden de llegada**, **Reservada** o **No permitida** en la sección de licencias de Apps and Books.

## Ver licencias de aplicaciones por usuario

Se pueden ver las preferencias de licencias para sus usuarios usando la pestaña Uso de licencias.

1. Haga clic en la pestaña **Usuarios**.
2. Seleccione un usuario.
3. Haga clic en la pestaña **Uso de licencias**.
   Aparecerá una lista de aplicaciones con su tipo de licencia de Apps and Books y los detalles asignación de la licencia.

Para ver el uso de la licencia de cada aplicación por usuario:

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Usuarios** en el menú principal de Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Seleccione un usuario.
:::

:::WorkflowBlockItem
Aparecerá la pestaña **Dispositivos** de forma predeterminada.

Haga clic en la pestaña **Uso de licencias**.

Se mostrará una lista de todas las aplicaciones instaladas en el dispositivo del usuario, incluyendo el estado de la licencia. El número de serie del dispositivo aparece en la columna Tipo de licencia de Apps and Books para las licencias basadas en dispositivos.

- Nombre de la aplicación
- Versión de la aplicación
- Precio de la aplicación
- Fecha en que se asignó la aplicación
- Tipo de licencia de Apps and Books
- Acciones (estado de la licencia)
- Información de la plataforma para detalles de licencia.
:::
::::

También puede ver el uso de la licencia de Apps and Books de cada aplicación:

1. Vaya a **Aplicación > Catálogo de aplicaciones** en el menú principal de Ivanti Neurons for MDM.
2. Seleccione una aplicación.
3. Haga clic en la pestaña **Licencias de Apps and Books&#x20;**&#x73;i estuviera presente.
4. Haga clic en un nombre de cuenta. En esta pestaña solamente aparecerán las aplicaciones compradas a través del programa Apps and Books.
   Se muestra una pestaña independiente para cada tipo de licencia de Apps and Books.

| **Tipo de licencia y registro**                                                                                                                   | **Descripción**                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| En orden de llegada (FCFS, por sus siglas en inglés): tiene la posibilidad de seleccionar qué grupos de usuarios recibirán este tipo de licencia. | - Aplicaciones solicitadas por el usuario: son las aplicaciones que el usuario elige instalar. La licencia pasada en el usuario es la opción predeterminada. |

:::Paragraph{listStyleType="disc" indent="2"}
Aplicaciones obligatorias: son las aplicaciones necesarias y se instalan mediante la configuración del administrador utilizando el ajuste **Instalar en dispositivo**. Estas aplicaciones utilizan licencias basadas en dispositivos de forma predeterminada. |
\| Reservada                                                                                                                                         | Las licencias reservadas tienen prioridad sobre las licencias en orden de llegada. Aquí se pueden seleccionar a los usuarios o dispositivos que tendrán una licencia reservada para la aplicación.                                                                                                                                                                                                                           |
\| No permitida                                                                                                                                      | Introduzca los usuarios que no están autorizados a tener una licencia para esta aplicación. Estos usuarios podrán instalar la aplicación de todos modos, pero deberán comprarla.                                                                                                                                                                                                                                             |
\| Registro de actividad                                                                                                                             | Muestra al usuario, el tipo de licencia de Apps and Books asignada a él, la fecha en que se asignó y la última acción llevada a cabo sobre la licencia.                                                                                                                                                                                                                                                                      |
:::

Para ver el uso detallado de la licencia de cada aplicación por dispositivo:

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Dispositivos** en el menú principal de Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Seleccione un dispositivo.
:::

:::WorkflowBlockItem
Haga clic en la pestaña **Aplicaciones instaladas**.
:::

:::WorkflowBlockItem
Se mostrará una lista de todas las aplicaciones administradas instaladas en el dispositivo seleccionado, incluyendo el estado de la licencia.

- Nombre de la aplicación
- Versión de la aplicación
- Plataformas compatibles
- Origen de la aplicación
- Tamaño de la aplicación
- Tipo de licencia de Apps and Books
- Fecha de notificación (instalación) de las aplicaciones de iOS
  Busque las aplicaciones instaladas para el dispositivo de la siguiente manera:- Nombre de la aplicación
- ID de conjunto o paquete
:::
::::

## Notificaciones de uso de licencias de Apps and Books

Las notificaciones de Apps and Books le ayudan a realizar un seguimiento del uso de la licencia de Apps and Books. Los umbrales de las notificaciones se definen del siguiente modo:

- Se emite una notificación informativa cuando se han usado más del 50 % de las licencias.
- Se emite una notificación de advertencia cuando se han usado del 70 al 80 % de las licencias.
- Se emite una notificación crítica cuando se han usado del 90 al 100 % de las licencias.
- Las notificaciones se desactivan cuando el uso disminuye por debajo del 50 %.

Para ver la información sobre licencias de cada aplicación:

::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en **Aplicaciones > Apps and Books de Apple**.
:::

:::WorkflowBlockItem
Se mostrará la información sobre licencias, que incluye:

- Nombre de la aplicación.
- Precio de la aplicación.
- Número de licencias disponibles.
- Número de licencias canjeadas.
  Vaya a **Panel > Notificaciones** para ver los detalles de la notificación de una licencia.
:::

:::WorkflowBlockItem
Aparecerá la página de notificaciones.

Haga clic en el título de la notificación para ver los detalles. Fíjese en [**Panel**](./Panel.md) para ver las notificaciones disponibles.
:::
::::

### Notificaciones de uso de licencias de Apps and Books

| **Activación**  | **Gravedad** | **Tipo de notificación** | **Tipo de componente** |
| --------------- | ------------ | ------------------------ | ---------------------- |
| 50 % canjeadas  | Información  | Uso de licencias         | Apps and Books         |
| 70 % canjeadas  | Advertencia  | Uso de licencias         | Apps and Books         |
| 80 % canjeadas  | Advertencia  | Uso de licencias         | Apps and Books         |
| 90 % canjeadas  | Alerta       | Uso de licencias         | Apps and Books         |
| 100 % canjeadas | Alerta       | Uso de licencias         | Apps and Books         |

## Visualización del uso de licencias de Apps and Books

Los detalles de uso de la licencia específicos de un usuario se mostrarán en la tabla de uso de la licencia en la columna de licencias.

1. Haga clic en una aplicación.
2. Haga clic en la pestaña **Uso de licencias**.
3. Introduzca un nombre de usuario en el campo de búsqueda.

## Revocación de la licencia de Apps and Books para una aplicación

Las licencias de Apps and Books se revocan cuando:

- El dispositivo está inactivo (retirado o borrado).
- La aplicación Apps and Books se elimina.
- La licencia basada en dispositivos se revoca cuando se retira el dispositivo.
- El token de Apps and Books se elimina.

Para revocar una licencia de Apps and Books para una aplicación:

1. Seleccione la aplicación en **Aplicaciones > Catálogo de aplicaciones**.
2. Haga clic en la pestaña **Licencias de&#x20;****Apps and Books de Apple** si está presente.
3. Lleve a cabo una de las siguientes tareas:1) Haga clic en **Revocar todas las licencias&#x20;**&#x70;ara revocar todas las licencias de todos los usuarios o dispositivos.
   2\) Haga clic en la pestaña **Registro de actividad**. Utilice la columna **Acciones** para revocar licencias individuales usuario a usuario o dispositivo a dispositivo.

- En dispositivos iOS, Apple permite un período de gracia de 30 días para las aplicaciones de Apps and Books una vez que se haya revocado la licencia de Apps and Books. Por lo tanto, la aplicación «Apps and Books» sigue siendo instalable.
- En dispositivos macOS, una vez que la licencia de Apps and Books haya sido revocada, la aplicación seguirá en el dispositivo.

Para revocar una licencia de Apps and Books para un usuario:

1. Haga clic en una aplicación.
2. Haga clic en la pestaña **Uso de licencias**.
3. Haga clic en el vínculo **Revocar licencia** en el usuario cuyo acceso la licencia debe eliminarse.

Las licencias de Apps and Books se revocan automáticamente si se elimina al usuario o si este elimina el perfil MDM del dispositivo.

### Notificaciones de errores de autenticación de Apps and Books

Se pueden producir algunos errores de autenticación al utilizar el servicio de And Books de Apple. Estas notificaciones de errores de autenticación de Apps and Books son las siguientes:

| **Notificación de error**    | **Acción**                                                        |
| ---------------------------- | ----------------------------------------------------------------- |
| Token de Acción no válido    | Cargar un sToken válido de Apps and Books                         |
| Token caducado               | Genere un nuevo token en línea utilizando la cuenta de su empresa |
| El sToken ha sido revocado   | Cargar un Apps and Books válido                                   |
| Inicio de sesión obligatorio | Inicie sesión en el servicio de Apps and Books                    |

## Comportamiento de Apps and Books para dispositivos macOS y iOS

### Apps and Books para iOS

| **Acción**                                                                             | **Licencia basada en el dispositivo**                                                    | **Licencia basada en el usuario**                                                        |
| -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Eliminar la aplicación Apps and Books de la distribución para el usuario               | La aplicación está desinstalada en el dispositivo del usuario                            | La aplicación está desinstalada en el dispositivo del usuario                            |
| Anular la delegación de Apps and Books                                                 | La aplicación está desinstalada de todos los dispositivos en espacios no predeterminados | La aplicación está desinstalada de todos los dispositivos en espacios no predeterminados |
| Eliminar una aplicación de Apps and Books de un espacio predeterminado o personalizado | La aplicación está desinstalada de todos los dispositivos                                | La aplicación está desinstalada de todos los dispositivos                                |

### Apps and Books para macOS

| Acción                                                                                 | Licencia basada en el dispositivo                                                       | **Licencia basada en el usuario** |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------- |
| Eliminar la aplicación Apps and Books de la distribución para el usuario               | La aplicación no se desinstala en el dispositivo del usuario                            | N/A                               |
| Anular la delegación de Apps and Books                                                 | La aplicación no se desinstala de todos los dispositivos en espacios no predeterminados | N/A                               |
| Eliminar una aplicación de Apps and Books de un espacio predeterminado o personalizado | La aplicación no se desinstala de todos los dispositivos                                | N/A                               |

## Derecho de licencia de Apps and Books cuando un dispositivo cambia de espacio

Cuando se mueve un dispositivo a un espacio nuevo, se revoca la licencia de Apps and Books que se asigna al dispositivo o al propietario del dispositivo. A continuación, se asignará una nueva licencia de Apps and Books dependiendo de la disponibilidad en el nuevo espacio.

A continuación se describen las situaciones de derecho de licencia de Apps and Books:

| Situación                                                                                                                                                                                                                                              | Privilegio                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------- |
| Una licencia de Apps and Books se asigna a un dispositivo o propietario del dispositivo en el espacio de origen y hay disponible una licencia de Apps and Books para la misma aplicación en el espacio de destino.                                     | Asigne una licencia del token de Apps and Books en el espacio de destino. |
| Una licencia de Apps and Books se asigna a un dispositivo o propietario del dispositivo en el espacio de origen y no hay disponible una licencia de Apps and Books para la misma aplicación en el espacio de destino.                                  | Revoque la licencia del token de Apps and Books en el espacio de origen.  |
| No se asigna ninguna licencia de Apps and Books a un dispositivo o propietario del dispositivo en el espacio de origen y hay disponible una licencia de Apps and Books para cualquier aplicación de Apps and Books instalada en el espacio de destino. | Asigne una licencia del token de Apps and Books en el espacio de destino. |

Si no puede realizar las tareas en la página **Categorías de aplicaciones**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración de aplicaciones y contenido
