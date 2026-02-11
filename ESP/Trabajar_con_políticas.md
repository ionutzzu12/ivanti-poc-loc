---
title: Trabajar con políticas
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Aplicar las políticas**](./Trabajar_con_políticas.md)
- [**Medidas de cumplimiento**](./Trabajar_con_políticas.md)
- [**Encontrar una política existente**](./Trabajar_con_políticas.md)
- [**Añadir una política**](./Trabajar_con_políticas.md)
- [**Editar una política**](./Trabajar_con_políticas.md)
- [**Eliminar una política**](./Trabajar_con_políticas.md)

## Aplicar las políticas

Las Directivas definen los requisitos para los dispositivos, así como lo que pasará si un dispositivo no cumple con los requisitos. Cada política cuenta con una regla y una medida de cumplimiento (lo que sucede si se infringe la regla). Utilice la página **Políticas** para seleccionar, configurar y distribuir políticas.

Existen los siguientes tipos de políticas:

| **Tipo**               | **Qué hace**                                                                                                                                                                                                                                                                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Dispositivos afectados | Marca los dispositivos en los que se realizó un jailbreak (iOS) o se accedió a la raíz (Android).Para ver el motivo de la infracción por el que el sistema marcó un dispositivo Android como en riesgo debido a las violaciones de la seguridad de raíz:1) Haga clic en la pestaña **Políticas**. |

2. Haga clic en el enlace **Dispositivos en riesgo**.
3. Haga clic en la pestaña **Infracciones activas**.
4. Compruebe el motivo de la infracción en la columna Infracción.Para ver el motivo de la infracción por el que el sistema marcó un dispositivo Android como en riesgo debido a las violaciones de la seguridad de raíz:1) Haga clic en la pestaña **Políticas**.
5. Haga clic en el enlace **Dispositivos en riesgo**.
6. Haga clic en la pestaña **Infracciones activas**.
7. Compruebe el motivo de la infracción en la columna **Infracción**. Será uno de los motivos siguientes\:Prioridad (1 = la más alta)

   Infracción

   1	Plugin en riesgo
   2	Cliente manipulado
   3&#x9;

   Fabricante de dispositivos desconocido: desconocido


   4	Carpeta sospechosa detectada: \[ruta]
   5	Se ha encontrado un binario sospechoso en: \[ruta]
   6	La carpeta /data es navegable o la carpeta /data/data es navegable
   7	Se encontró /system/app/Superuser.apk
   8	El administrador del paquete ha sido vulnerado
   9	Se ha encontrado una aplicación sospechosa: \[package] |
   \| Protección de datos/Cifrado deshabilitado (solo macOS) | Marca los dispositivos macOS que no tienen habilitado ningún código de acceso o cifrado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
   \| Itinerancia internacional                              | Marca los dispositivos que podrían incurrir en cargos por itinerancia internacional. El estado se actualiza cuando el dispositivo ingresa.En iOS, el dispositivo utiliza la marca de itinerancia según lo establece y notifica iOS. La medida de cumplimiento solo se genera en la primera infracción.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
   \| MDM/Administración de dispositivos desactivada         | Si el dispositivo está desactivado para MDM, no será evaluado para ninguna otra política o procesamiento delta más de configuraciones o aplicaciones durante los ingresos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
   \| Fuera de contacto                                      | Marca los dispositivos que estuvieron fuera de contacto con Ivanti Neurons for MDM por el margen de tiempo determinado.Elija las acciones que quiere llevar a cabo si un dispositivo no ha ingresado durante un intervalo determinado de horas (2-3 a 23-24) o número de días.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
   \| Cliente MI fuera de contacto (solo iOS)                | Marca los clientes de Ivanti Neurons for MDM que estuvieron fuera de contacto con Ivanti Neurons for MDM por el margen de tiempo determinado.Elija las acciones que quiere llevar a cabo si el cliente no ha ingresado durante un intervalo determinado de horas (2-3 a 23-24) o número de días.Esto también es aplicable a los dispositivos registrados a través de iReg. Esta política marca el dispositivo como no cumplidor si no hay ningún cliente o si el cliente no ha ingresado durante un período de tiempo definido.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   \| [**Aplicaciones permitidas**](./Supervisar_y_controlar_las_aplicaciones_permitidas.md)            | Marca los dispositivos que infringen las reglas sobre qué aplicaciones están permitidas o son obligatorias.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   \| [**Política personalizada**](./Política_personalizada.md)            | Crea una política personalizada basada en condiciones y acciones relacionadas que usted especifique.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## Medidas de cumplimiento

Están disponibles las siguientes opciones de cumplimiento:

| Medida de cumplimiento       | Qué hace                                                                                                                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Supervisar                   | Etiqueta el dispositivo de la página Dispositivos de Ivanti Neurons for MDM. Esta acción está activada de forma predeterminada.                                                                   |
| Bloquear                    | Indica a Access o Sentry que deben bloquear un dispositivo si éste intenta acceder a un recurso a través de Sentry o Access después de incumplir la política en los detalles del último contacto. |
| Enviar un mensaje al usuario | - Etiqueta el dispositivo de la página Dispositivos de Ivanti Neurons for MDM.                                                                                                                    |

- Envía un correo electrónico al propietario del dispositivo.
- Además de las políticas existentes, ahora la opción "**Usar la plantilla de correo electrónico de la política de legalidad**" también está disponible para las políticas siguientes:
  - Protección/cifrado de datos deshabilitado
  - Itinerancia internacional
  - MDM/Administración de dispositivos desactivada
  - Fuera de contacto
  - Cliente MI fuera de contacto

:::Paragraph{indent="1"}
Envía una notificación push al dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
\| Cuarentena                                     | \* Elimina la mayoría de las configuraciones del dispositivo.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Excepciones: Configuraciones del código de acceso, Configuraciones de Wi-Fi para dispositivos de solo Wi-Fi, Configuraciones de restricciones (iOS).
:::

- Elimina todas la aplicaciones instaladas por Ivanti Neurons for MDM.
- Elimina todo el contenido distribuido por Ivanti Neurons for MDM, incluidos los archivos de iBook y ePub.
- Bloquea el acceso a los catálogos de Ivanti Neurons for MDM.
- Suspende los avisos para instalar aplicaciones adicionales.
- Bloquea el acceso a las aplicaciones habilitadas para AppConnect.
- Incluye compatibilidad para aplicaciones habilitadas para AppConnect.
- Si está activado, suspende las aplicaciones del área personal del dispositivo en cuarentena para indicar que el usuario del dispositivo tiene que atender los problemas de cumplimiento del dispositivo para que este vuelva a ser funcional. Compatible con los dispositivos Android 11+ provistos con el Perfil de trabajo en el Dispositivo propiedad de la empresa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Acciones de cuarentena adicionales (opcional): | **Poner las aplicaciones administradas en cuarentena**: elimina las aplicaciones administradas por Ivanti Neurons for MDM del dispositivo y permite la opción Bloquear nuevas descargas de aplicaciones para impedir que se puedan volver a instalar las aplicaciones en el dispositivo.Seleccione una de las siguientes opciones:\* **Todas las aplicaciones**
- **Eliminar todas las aplicaciones excepto las siguientes**: eliminar todas las aplicaciones excepto las que se añaden a la lista de aplicaciones.
- **Aplicaciones designadas:&#x20;**&#x61;ñada una o más aplicaciones por medio de búsqueda o de forma manual (utilizando la Id. de conjunto o el nombre del paquete). Haga clic en la pestaña **Ver aplicaciones** para ver la lista de aplicaciones añadidas. No se encuentra disponible la acción de cuarentena de la función predeterminada Bloquear acceso a la App Store.En algunos dispositivos, la acción de cuarentena no eliminará la aplicación del dispositivo debido a ciertas limitaciones del mismo.- **Bloquear la descarga de aplicaciones nuevas**: evita la descarga de aplicaciones nuevas en el dispositivo.Por defecto, esta opción está seleccionada (para las tres: Todas las aplicaciones, Quitar todas las aplicaciones excepto las siguientes y Aplicaciones designadas) y no se puede cancelar la selección. Esto impide que las aplicaciones se reinstalen en el dispositivo.**Eliminar configuraciones**: elimina las configuraciones de Ivanti Neurons for MDM del dispositivo.Seleccione una de las siguientes opciones:\* **Todas las configuraciones**
- **Configuraciones designadas:&#x20;**&#x73;eleccione una o más configuraciones de la lista o búsquelas. Haga clic en la pestaña **Configuraciones seleccionadas** para ver la lista de las configuraciones seleccionadas.**Forzar las configuraciones designadas**: distribuya las configuraciones designadas como parte del cumplimiento personalizado.Esta lista contiene configuraciones que cumplen los siguientes criterios:\* Configuración activada
- Configuración sin sistema
- Configuración apta para cuarentena
- Las configuraciones creadas en el espacio actual o delegadas desde el espacio predeterminadoPara obtener una lista de las configuraciones que no sean de cuarentena, consulte la sección [**Configuraciones que no son de cuarentena.**](./Trabajar_con_políticas.md)**Eliminar contenido**: elimina todo el contenido y los medios asociados a aplicaciones distribuidas por Ivanti Neurons for MDM del dispositivo.**Suspender aplicaciones del área personal**: suspende las aplicaciones del área personal del dispositivo en cuarentena para indicar que el usuario del dispositivo tiene que atender los problemas de cumplimiento del dispositivo para que este vuelva a ser funcional. Compatible con los dispositivos Android 11+ provistos con el Perfil de trabajo en el Dispositivo propiedad de la empresa. |

## Encontrar una política existente

Puede utilizar los filtros y la función de búsqueda de la página de Políticas para encontrar una o más políticas existentes.

Procedimiento

1. Vaya a **Políticas**.
2. Para filtrar una lista de configuraciones que cumplan ciertos criterios, haga clic en **Filtros**.
3. Seleccione uno o más criterios de filtros.
4. Para buscar una política existente por su nombre, introduzca el nombre de la política en el campo **Buscar**.

## Añadir una política

Procedimiento

1. Vaya a **Políticas**.
2. Haga clic en +**Añadir** (arriba a la derecha).
3. Seleccionar un tipo de política.
4. Complete los ajustes.
5. Seleccione los grupos de dispositivos en los que desea recibir esta política.Puede distribuir hasta un máximo de 100 archivos de configuración a la vez.
6. Haga clic en **Hecho**.

## Editar una política

Procedimiento

1. Vaya a **Políticas**.
2. Para la política requerida, haga clic en el icono **Editar** (lápiz) en la columna Acciones.
3. Realice los cambios.
4. Guarde los cambios.

## Eliminar una política

Procedimiento

1. Vaya a **Políticas**.
2. Para la política requerida, haga clic en el icono **Eliminar** en la columna Acciones.
3. Haga clic en **Sí** para confirmar.

Si no puede ver la página de las Políticas, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración de dispositivos
- Dispositivo de solo lectura
