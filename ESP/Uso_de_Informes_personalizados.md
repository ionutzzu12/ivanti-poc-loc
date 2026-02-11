---
title: Uso de Informes personalizados
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

**Licencia**: Gold

La función Informes personalizados le permite personalizar y generar informes con diferentes métricas y plantillas listas para usarse. Debe tener la función de Administrador del sistema o Solo lectura del sistema para acceder a esta función. Actualmente puede crear un máximo de 40 informes.

Esta sección contiene los siguientes temas:

[**Generación de un informe**](./Uso_de_Informes_personalizados.md)

[**Llevar a cabo acciones en un informe**](./Uso_de_Informes_personalizados.md)

[**Ver información de los informes**](./Uso_de_Informes_personalizados.md)

## Generación de un informe

Puede programar y generar un informe desde el portal administrativo de Ivanti Neurons for MDM.

**Procedimiento**

:::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Panel&#x20;**>**&#x20;Informes**.
:::

:::WorkflowBlockItem
Haga clic en **Crear un informe** para visualizar la página Elija una plantilla para informes.
:::

:::WorkflowBlockItem
Elija una plantilla para su informe de la opciones que ha configurado.\* **Dispositivos bloqueados**: informe sobre los dispositivos que actualmente tienen el acceso bloqueado de Sentry.

- **Dispositivos**: informe sore los dispositivos de todas las particiones del sistema.
- **Infracciones de políticas**: informe sobre infracciones de políticas de su sistema.
- **Usuarios**: informe sobre los usuarios del sistema
- **Estado de caducidad de la contraseña del usuario**: informe sobre el estado de caducidad de la contraseña de los usuario del sistema.
- **Aplicaciones más instaladas**: informe sobre todas las aplicaciones de su sistema, ordenadas según el número de veces que se ha instalado cada aplicación.
- **Aplicaciones sin administrar**: informe sobre las aplicaciones sin administrar de su sistema.
- **Todas las aplicaciones**: informe de todas las aplicaciones de los dispositivos que administra usted.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**. Se muestra la página Detalles del informe.
:::

:::WorkflowBlockItem
Introduzca un **Nombre del informe**.
:::

:::WorkflowBlockItem
(Opcional) Introduzca una **Descripción** para el informe.
:::

:::WorkflowBlockItem
Seleccione **Rango de eventos** en las opciones siguientes\:Para informes existentes:
:::

:::WorkflowBlockItem
- **Todos los eventos**
- **Día anterior**
- **Semana anterior**
- **Mes anterior**
- **Rango anterior**: muestra el informe que se creó con el control deslizante de rangos desde la versión anterior del portal administrativo de Ivanti Neurons for MDM. Si el administrador selecciona y guarda alguna de las opciones anteriores para un informe, no se mostrará la opción Rango anterior. El valor de rango se puede ver en la página Resumen de informes.
  Para nuevos informes:
- **Todos los eventos**
- **Día anterior**
- **Semana anterior**
- **Mes anterior**
  Haga clic en **Siguiente**. Se muestra la página Datos del informe.
:::

:::WorkflowBlockItem
Haga clic en **Personalizar** para generar un informe personalizado\:En la página **Panel > Informes**, la columna Nombre de plantilla mostrará "personalizado" entre paréntesis para indicar que se trata de un informe personalizado.
:::

:::WorkflowBlockItem
Haga clic en **Personalizar columnas** para agregar, eliminar o cambiar el orden de las columnas en la sección **Columnas de informes**. También puede hacer clic sobre el nombre de la columna para eliminar la columna agregada.
:::

:::WorkflowBlockItem
(Opcional) utilice la casilla **Seleccionar todas las columnas** para seleccionar todas las columnas visualizadas de la lista.
:::

:::WorkflowBlockItem
Haga clic en **Restaurar valores predeterminados** para volver a las columnas generadas anteriormente. Para volver a las columnas sin ninguna personalización, puede elegir una de las plantillas de la página **Elija una platilla para informes**. Las columnas predeterminadas se indican con un icono de candado.
:::

:::WorkflowBlockItem
Cree filtro basados en reglas específicas de la sección **Filtro avanzado**.Todas las opciones de filtros no está disponible para todos los informes. Para obtener más información sobre la lista de filtros disponibles, consulte el tema [**Filtros**](./Uso_de_Informes_personalizados.md) bajo este proceso.Los siguientes atributos de nuevo hardware están disponibles para dispositivos de Windows cuando se crean informes: cifrado de BitLocker, Edición de SO, Versión del sistema, Fabricante de placa base, Producto de placa base, Estado de placa base, Fabricante de BIOS, Versión de BIOS, Particiones de disco duro, Tupo de unidad óptica, Nombre de CPU y Estado de CPU.
:::

:::WorkflowBlockItem
(Opcional) haga clic en el icono **+** para agregar otra regla o en el icono **Agregar grupo** para agregar otro grupo de reglas.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**. Se muestra la página Programa del informe.
:::

:::WorkflowBlockItem
Seleccione *uno* de los siguientes formatos para descargar el informe:
:::

::::WorkflowBlockItem
- **CSV**
- **PDF**
- **CSV y PDF**Para archivos de informes en PDF, se permiten hasta 10 columnas. En la sección Gráficos de informes, aparecerán los dos tipos de gráficos que se incluirán en los informes en PDF.El informe de **Todas las aplicaciones&#x20;**&#x65;s compatible solo con el formato CSV.
  Haga clic en **Programación automática** para configurar un informe que se ejecutará automáticamente mediante la configuración de la periodicidad. También puede hacer clic en **Manual** para ejecutar el informe una vez y que se envíe en un correo electrónico.::::WorkflowBlock

:::WorkflowBlockItem
* Seleccione *una* de las opciones de **Informes recurrentes**:- **Diario**
  - **Semanal**
  - **Mensualmente**
  - **Programa anterior**: para informes existentes
* Seleccione la **Fecha de inicio** y la **Fecha final** (opcional).
:::

\::::La opción Ejecutar ahora generará un informe puntual. Puede usar la misma plantilla para generar informes programados. En la página **Panel > Informes**, en las columnas Frecuencia y Próximo programado aparecerá el estado no programado de estos informes.
::::

:::WorkflowBlockItem
Haga clic en **Siguiente**. Se muestra la página Distribución del informe. Seleccione los destinatarios del informe.
:::

:::WorkflowBlockItem
(Opcional) agregue ID de correos electrónicos externos haciendo clic en el enlace **Agregar correo electrónico externo**.
:::

:::WorkflowBlockItem
Haga clic en **Hecho**. Aparece el **Resumen\*\*\*\*de distribución de informes**.
:::

:::WorkflowBlockItem
(Opcional) haga clic en **Editar** para modificar su informe.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::

:::WorkflowBlockItem
Haga clic en el icono de descarga para seleccionar el formato del informe. El destinatario del informe recibe un correo electrónico que contiene un botón de **Descargar informe** para descargar el informe.
:::
:::::

### Filtros

| Opciones de reglas                       | Descripción                                                                                                                                                                                |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Bloqueo de activación habilitado         | Reglas basada en el bloqueo de activación activada como **Sí** o **No**.Ejemplo de regla: 'El bloqueo de activación habilitado es igual a Sí'.                                             |
| Estado de la aplicación Tunnel           | Regla para el estado de la aplicación Tunnel como **BLOQUEAR** o **PERMITIR**.Ejemplo de regla: 'El estado de la aplicación Tunnel es igual a Bloquear'.                                   |
| **Nivel de batería**                     | Valor del nivel de batería del dispositivo.Ejemplo de regla: 'El nivel de batería es igual a 1080'.El valor introducido para el nivel de la batería debe ser en segundos.                  |
| **Último ingreso del cliente**           | Regla basada en el último ingreso del cliente dentro del rango de fecha.Ejemplo de regla: '«Último ingreso del cliente» está en el rango 02/04/2019 6:00:00 hasta el 05/04/2019 17:00:00'. |
| Estado del cumplimiento                  | Regla basada en el estado del cumplimiento como **Sí** o **No**.Ejemplo de regla: 'El estado del cumplimiento es igual a Sí'.                                                              |
| **Nombre del país actual**               | Introduzca el nombre del país actual.Ejemplo de regla: 'El estado del cumplimiento es igual a Francia'.                                                                                    |
| **MMC actual**                           | Regla basada en el código móvil del país.Ejemplo de regla: 'El MCC actual es igual a 410'.                                                                                                 |
| **MNC actual**                           | Regla basada en el código de red móvil actual.Ejemplo de regla: 'El MNC actual es igual a 06'.                                                                                             |
| **Inscripción de dispositivos activada** | Regla basada en la inscripción de dispositivos activada como **Sí** o **No**.Ejemplo de regla: '«Inscripción de dispositivos activada» es igual a Sí'.                                     |
| **Estado nativo de antiphishing**        | Seleccione cualquiera de las siguientes opciones de Estado nativo de antiphishing:\* es igual a                                                                                            |

- no es igual aLos valores posibles son:- No activado\* N/A
- Activado
- Desconocido                                                                                                            |
  \| **Estado de la VPN de antiphishing**               | Seleccione cualquiera de las siguientes opciones de Estado de la VPN de antiphishing:\* es igual a
- no es igual aLos valores posibles son:- No activado\* N/A
- Activado
- Desconocido                                                                                                         |
  \| **Inscrito en la Inscripción de dispositivos**     | Regla basada en «inscrito en la Inscripción de dispositivos» como **Sí** o **No**.Ejemplo de regla: «Inscrito en la inscripción de dispositivos es igual a Sí»                                                                                                                                |
  \| **Protección de datos**                            | Indica si la protección de datos está habilitada en el dispositivo. Los valores posibles son **Sí** y **No**.Ejemplo de regla: 'La protección de datos es igual a Sí'.                                                                                                                        |
  \| Itinerancia de datos activada                      | Regla basada en la itinerancia de datos activada como **Sí** o **No**.Ejemplo de regla: 'La itinerancia de datos activada es igual a Sí'.                                                                                                                                                     |
  \| **Estado del bloqueo del dispositivo**             | Regla basada en el estado del bloqueo del dispositivo.Ejemplo de regla: 'El estado de bloqueo del dispositivo es igual a Bloqueo'.                                                                                                                                                            |
  \| Id. de dispositivo                                 | Regla para una Id. específica del dispositivo dentro de un rango de varias Id. de dispositivos.Ejemplo de regla: 'La Id. del dispositivo es superior a 45'. x                                                                                                                                 |
  \| **MCC de origen**                                  | Regla basada en el código móvil del país de origen.Ejemplo de regla: 'El MCC de origen es igual a 310'.                                                                                                                                                                                       |
  \| **MNC de origen**                                  | Regla basada en el código de red móvil de origen.Ejemplo de regla: 'El MNC de origen es igual a 510'.                                                                                                                                                                                         |
  \| IMEI                                               | Regla para un valor de IMEI específico.Ejemplo de regla: 'El IMEI comienza por 9900'.                                                                                                                                                                                                         |
  \| Estado de la invitación                            | Seleccione cualquiera de las siguientes opciones de Estado de la invitación:\* Ninguno
- Pendiente
- Caducado
- **Completado**Ejemplo de regla: 'El estado de la invitación es igual a Pendiente'.                                                                                             |
  \| Servicio de Localizador habilitado                 | Regla basada en el servicio de localización activado como **Sí** o **No**.Ejemplo de regla: 'El servicio de localización activado es igual a Sí'.                                                                                                                                             |
  \| Estado de activación del MTD                       | Seleccione cualquiera de las siguientes opciones de Estado de la activación del MTD:\* es igual a
- no es igual aLos valores posibles son:\* N/A
- Error
- Pendiente
- Protegido                                                                                                                |
  \| **Estado de cuarentena**                           | Regla basada en el servicio de localización activado como **Sí** o **No**.Ejemplo de regla: 'El estado de cuarentena es igual a Sí'.                                                                                                                                                          |
  \| Registrado en                                      | Regla para seleccionar el rango de fecha y hora desde que se registró el dispositivo.Ejemplo de regla: '«Registrado el» está en el rango 03/10/2017 09:00:00 hasta el 20/10/2017 17:00:00'.                                                                                                   |
  \| Itinerancia                                        | Regla basada en la itinerancia como**Sí** o **No**.Ejemplo de regla: 'La itinerancia es igual a Sí'.                                                                                                                                                                                          |
  \| **Estado**                                         | Seleccione cualquiera de las siguientes opciones de Estado de la invitación:\* Activo
- Retirada pendiente
- Retirada enviado
- Retirado
- Retirada cancelada
- Borrado pendiente
- Borrado enviado
- Borrado
- Borrado canceladoEjemplo de regla: 'El estado es igual a «Retirada pendiente». |
  \| Itinerancia de voz activada                        | Regla basada en la itinerancia de voz activada como **Sí** o **No**.Ejemplo de regla: 'La itinerancia de voz activada es igual a Sí'.                                                                                                                                                         |
  \| Dirección MAC de Wi-Fi                             | Introduzca un valor de dirección Mac específico.Ejemplo de regla: 'La dirección Mac Wi-Fi no es igual a 00-14-22-01-23-45'.                                                                                                                                                                   |
  \| Copia de seguridad de iCloud habilitada            | Regla basada en la copia de seguridad de iCloud activada como **Sí** o **No**.Ejemplo de regla: 'La copia de seguridad de iCloud activada es igual a Sí'.                                                                                                                                     |
  \| Estado de activación de la cuenta de iTunes Store. | Regla basada en el estado de activación de la cuenta de iTunes Store como **Sí** o **No**.Ejemplo de regla: 'El estado de activación de la cuenta de iTunes Store no es igual a No'.                                                                                                          |
  \| **Tipo de plataforma**                             | Aplicable para el informe de Todas las aplicaciones.                                                                                                                                                                                                                                          |
  \| **Origen**                                         | Aplicable para el informe de Todas las aplicaciones.                                                                                                                                                                                                                                          |
  \| **Atributos personalizados**                       | Aplicable para el informe de Todas las aplicaciones.                                                                                                                                                                                                                                          |
  \| **Administrado**                                   | Aplicable para el informe de Todas las aplicaciones y de Aplicaciones más usadas.                                                                                                                                                                                                             |
  \| **Identificador de la aplicación**                 | Informe de todas las aplicaciones por defecto.                                                                                                                                                                                                                                                |
  \| **Meid**                                           | Aplicable para el informe de Aplicaciones sin administrar.                                                                                                                                                                                                                                    |

## Llevar a cabo acciones en un informe

Puede llevar a cabo varias acciones desde la página Informes programados.

**Procedimiento**

1. Vaya a **Panel&#x20;**>**&#x20;Informes**.
2. En la página **Mis informes programados**, haga clic en el menú desplegable de **Acciones**, y seleccione una de las opciones siguientes:| Opciones de acciones | Acción llevada a cabo               |
   \| -------------------- | ----------------------------------- |
   \| **Ver**              | Le permite ver el informe.          |
   \| **Editar**           | Le permite editar el informe.       |
   \| **Ejecutar ahora**   | Ejecuta el informe.                 |
   \| **Descargar CSV**    | Descarga el informe en formato CSV. |
   \| **Descargar PDF**    | Descarga el informe en formato PDF. |
   \| **Eliminar**         | Elimina el informe.                 |

## Ver información de los informes

Puede ver la información del informe y llevar a cabo algunas acciones en el informe creado.

**Procedimiento**

1. Vaya a **Panel&#x20;**>**&#x20;Informes**.
2. En la página **Mis informes programados**, haga clic en el nombre del informe para ver los detalles. Se abre la página del informe.
3. Seleccione una de las siguientes opciones| Opciones de acciones | Acción llevada a cabo                                                                                                                                                                                                                                                                                                                         |
   \| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Alternar**         | Le permite habilitar o deshabilitar el informe.                                                                                                                                                                                                                                                                                               |
   \| **Ejecutar ahora**   | Ejecuta el informe.                                                                                                                                                                                                                                                                                                                           |
   \| **Ver**              | Le permite ver los detalles del informe. Utilice el menú desplegable de Acciones para llevar a cabo cualquiera de las tareas siguientes:\* **Desactivar**
   - **Descargar el CSV/PDF más reciente&#x20;**(basado en el tipo de informe seleccionado, ya sea CSV, PDF o CSV & PDF, muestra la opción de Descargar)
   - **Historial**
   - **Eliminar** |
     \| **Eliminar**         | Elimina el informe.                                                                                                                                                                                                                                                                                                                           |

**Temas relacionados**:

- Para asignar una función personalizada a un usuario, consulte [**Asignar funciones**](./Asignar_funciones_a_usuarios.md).
- Consulte [**Funciones de usuario**](./Funciones_del_usuario.md) para ver una lista de funciones predeterminadas.
- [**Administración de funciones**](./Administración_de_funciones.md)
