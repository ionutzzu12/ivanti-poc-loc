---
title: Ajustes del catálogo
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Cambiar los ajustes de administración de aplicaciones de Apple**](./Ajustes_del_catálogo.md)
- [**Ajuste de región predeterminada de la App Store**](./Ajustes_del_catálogo.md)
- [**Activar/desactivar las actualizaciones de aplicaciones iOS**](./Ajustes_del_catálogo.md)
- [**Activar/desactivar las puntuaciones y opiniones de las aplicaciones**](./Ajustes_del_catálogo.md)
- [**Cargar o actualizar un sToken de Apps and Books de iOS/macOS (licencia: Gold)**](./Ajustes_del_catálogo.md)
- [**Eliminar un sToken de Apps and Books de iOS/macOS de su servicio de Ivanti Neurons for MDM**](./Ajustes_del_catálogo.md)

En la página **Aplicaciones** > **Ajustes del catálogo**, configure las preferencias que quiera aplicar en todas las aplicaciones del catálogo de aplicaciones. Puede hacer lo siguiente:

- Incluir actualizaciones de aplicaciones durante el ingreso del dispositivo
- Impedir la copia de seguridad en iCloud e iTunes (solo en iOS)
- Establecer la región predeterminada de la app store (Apple y Microsoft)
- Eliminar aplicaciones de iOS cuando el dispositivo deja de estar inscrito
- Habilitar Ivanti Neurons for MDM "Calificaciones y opiniones"
- Cargar los tokens de iOS y macOS Apps and Books (requiere licencia de Gold)

## Cambiar los ajustes de administración de aplicaciones de Apple

Todos estos ajustes se aplicarán a todas las aplicaciones a no ser que se haya creado una configuración de la administración de aplicaciones para aplicaciones individuales.

::::WorkflowBlock
:::WorkflowBlockItem
Seleccione o quite la marca de selección de una o más de las siguientes casillas:
:::

:::WorkflowBlockItem
- **Actualizar aplicaciones durante el ingreso del dispositivo** (opción seleccionada de forma predeterminada)
- **Impedir la copia de seguridad de iCloud e iTunes**
- **Eliminar aplicaciones dadas de baja**
  Haga clic en **Guardar**.
:::
::::

## Notificaciones

::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en la lista desplegable de **Generar una notificación del sistema cuando las nuevas versiones de la aplicación estén disponibles en la tienda de Apple y en la tienda de Google**, y seleccione una de las opciones siguientes:
:::

:::WorkflowBlockItem
- **Una vez a la semana**
- **Una vez al día**
  Haga clic en la lista desplegable de **Generar notificaciones de usuario final para las nuevas actualizaciones de la aplicación disponibles en AppCatalog**, y seleccione una de las opciones:
- **Una vez a la semana**
- **Una vez al día**
:::
::::

## Ajuste de región predeterminada de la App Store

En los ajustes del App Catalog, establezca la región predeterminada para las app stores de Apple y Microsoft.

1. En la sección Región predeterminada de App Store:\* Seleccione la **Región de la App Store de Apple**.
   - Seleccione la **Región de la App Store de Microsoft**.
2. Seleccione o deseleccione la opción de utilizar la última región seleccionada de la App Store como región predeterminada para cada administrador. Si se selecciona esta opción, la región de la app store se establecerá como la región que cada administrador seleccionó por última vez y anulará las configuraciones anteriores. Si es la primera vez que un administrador utiliza esta función, las regiones predeterminadas de la app store se establecerán en los ajustes anteriores de este procedimiento.
3. Haga clic en **Guardar**.

## Activar/desactivar las actualizaciones de aplicaciones iOS

::::WorkflowBlock
:::WorkflowBlockItem
Seleccione o quite la marca de la casilla **Actualizar las aplicaciones durante la conexión del dispositivo.**
:::

:::WorkflowBlockItem
- Esta opción está seleccionada de forma predeterminada.
- Cuando se quita la marca de selección, los ingresos de dispositivo (incluidos los ingresos forzados por parte del administrador) no incluirán las actualizaciones de las aplicaciones.
- No obstante, el usuario puede actualizar manualmente la aplicación haciendo clic en la acción Forzar ingreso en el catálogo de aplicaciones del dispositivo.
- Las instalaciones de nuevas aplicaciones y todas las demás configuraciones y ajustes se actualizarán durante el ingreso del dispositivo.
  Haga clic en **Guardar**.
:::
::::

En el caso de una aplicación administrada, el administrador puede hacer clic en el botón **Actualizar** que está en la página de detalles de la aplicación para actualizar manualmente la aplicación a la última versión de la App Store.

En el dispositivo de un usuario, el usuario puede hacer clic en el botón **Forzar ingreso** que está en el menú del App Catalog para dejar que se produzcan el ingreso del dispositivo y las actualizaciones de la aplicación a la vez que otras configuraciones y actualizaciones.

Todos estos ajustes juntos permiten que los usuarios finales puedan elegir cuándo se actualizan sus aplicaciones:

- Espere hasta estar conectado a una red Wi-Fi para evitar el consumo de datos.
- Evite quedar bloqueado, en un momento poco oportuno, mientras la aplicación se está actualizando.

## Activar/desactivar las puntuaciones y opiniones de las aplicaciones

Esto permitirá a los usuarios puntuar y opinar sobre las aplicaciones y a los otros usuarios leer dichas opiniones.

1. Seleccione o quite la marca de selección en **Habilitar puntuaciones y opiniones en el catálogo de aplicaciones del usuario final**.
2. Haga clic en **Guardar**.

El formato del sToken de Apps and Books ha cambiado. En lugar de la cadena de caracteres de versiones anteriores, ahora es una cadena de caracteres almacenada en un archivo de texto con formato de archivo vpptoken. Cargue este archivo directamente en la consola de administración para procesarlo. La página de la cuenta de Apps and Books se ha actualizado para mostrar el nombre de la organización de Apps and Books y las fechas de vencimiento.

## Cargar o actualizar un sToken de Apps and Books de iOS/macOS (licencia: Gold)

1. Seleccione **Añadir sToken de Apps and Books**.
2. Introduzca un nombre para el archivo sToken en el campo **Alias**.
3. Arrastre y suelte el archivo del sToken hasta el área especificada o haga clic en **Elegir archivo** para navegar hasta el archivo del sToken.
4. Haga clic en **Guardar&#x20;**&#x6F;, si está actualizando un archivo de sToken, haga clic e&#x6E;**&#x20;Actualizar**.
5. Vaya a la página [**Apps and Books de Apple**](./Apps_and_Books_de_Apple.md) para visualizar las aplicaciones asociadas a este token.

Si los tokens de Apps y libros se reservaron para usuarios individuales en una versión anterior de Ivanti Neurons for MDM, debe verificar que sigan reservados para esos usuarios y, en caso de ser necesario, reservarlos nuevamente.

## Eliminar un sToken de Apps and Books de iOS/macOS de su servicio de Ivanti Neurons for MDM

Puede revocar una aplicación que el usuario ya no necesite y volver a reasignarla según sea necesario. Si la aplicación se implementó como aplicación administrada con MDM para iOS/macOS, tendrá la opción de desinstalar la aplicación y todos los datos inmediatamente.

1. Seleccione una aplicación para desinstalarla.
2. Haga clic en **Eliminar**.Aparecerá un diálogo de advertencia.
3. Opcionalmente, puede conceder al usuario un período de gracia de 30 días para:\* Guardar sus datos.
   - Comprar una copia personal de la aplicación.
   - Transferir las aplicaciones que instaló con esta cuenta de Apps and Books a sus cuentas personales para seguir usándolas.

Si no puede realizar las tareas en la página **Ajustes de catálogo**, puede ser que no tenga los permisos necesarios. Necesita tener el siguiente [**rol**](./Funciones_del_usuario.md):

- Administración de aplicaciones y contenido
