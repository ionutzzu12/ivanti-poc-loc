---
title: Ajustes de borrado del dispositivo
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

El borrado del dispositivo automatiza el ciclo de vida del dispositivo para los que están sin usar. Puede retirar los dispositivos que no se hayan conectado durante el número de días que especifique. Puede eliminar los dispositivos que se hayan retirado durante el número de días que especifique. La página de Audit Trails captura los ajustes Retirar dispositivo, Eliminar dispositivo y Eliminar dispositivo borrado.

La tabla siguiente proporciona información sobre los dispositivos Android que admiten la configuración de borrado de dispositivos:

| Modo                                                                                           | Retirar en caso de incumplimiento | Eliminar retirados | Forzar la retirada del dispositivo pendiente de retirada. | Eliminar borrados | Eliminar pendientes de borrado |
| ---------------------------------------------------------------------------------------------- | --------------------------------- | ------------------ | --------------------------------------------------------- | ----------------- | ------------------------------ |
| Perfil de trabajo de Android (propietario del perfil)                                          | **SÍ**                            | **SÍ**             | **SÍ**                                                    | **NO**            | **NO**                         |
| Perfil Administrador del dispositivo/ Trabajo en Dispositivo propiedad de la empresa           | **SÍ**                            | **SÍ**             | **SÍ**                                                    | **SÍ**            | **SÍ**                         |
| Dispositivo administrado de trabajo/Dispositivo administrado con Android con perfil de trabajo | **NO**                            | **NO**             | **NO**                                                    | **SÍ**            | **SÍ**                         |

**Requisitos previos**

Para acceder a esta configuración, debe tener permisos de Rol de administración del sistema.

## Retirar dispositivos

**Procedimiento**

|   | 1. | Vaya a **Administrador** > **Sistema** > **Limpieza de dispositivos**. Se abre la página Borrado de dispositivos. |
| - | -- | ----------------------------------------------------------------------------------------------------------------- |

|   | 2. | Seleccione **Retirar dispositivo**. |
| - | -- | ----------------------------------- |

|   | 3. | Utilice la tabla **Retirar dispositivos** para especificar los detalles. |
| - | -- | ------------------------------------------------------------------------ |

|   | 4. | Haga clic en **Mostrar la lista de dispositivos que no han contactado**. Muestra la lista de dispositivos que no se han comprobado en un número de días especificado. |
| - | -- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

|   | 5. | Haga clic en **Retirar dispositivos ahora**, alternativamente, puede programar la retirada del dispositivo. |
| - | -- | ----------------------------------------------------------------------------------------------------------- |

|   | 6. | El portal administrativo de Ivanti Neurons for MDM retirará los dispositivos especificados. |
| - | -- | ------------------------------------------------------------------------------------------- |

|   | 7. | Haga clic en **Guardar** para guardar sus ajustes. |
| - | -- | -------------------------------------------------- |

|   | 8. | (Opcional) Si actualiza los valores, puede hacer clic en **Restablecer** para restablecer los ajustes a sus valores iniciales. |
| - | -- | ------------------------------------------------------------------------------------------------------------------------------ |

### Retirar dispositivos

| Campo                                                                 | Descripción                                                                                                                                                                |
| --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Retire los dispositivos que no se han comprobado en más de (días)** | Días: 30 días por defecto, 365 días es el número máximo de días permitido.                                                                                                 |
| **Número máximo de dispositivos para Retirar en cada sesión**         | Seleccione 100, 500 o 1000 (Predeterminado: 100).                                                                                                                          |
| **Retirar automáticamente dispositivos según un calendario**          | Marque la casilla para retirar dispositivos según un calendario preestablecido.                                                                                            |
| **Retirar la configuración programada**                               | Seleccione una de las siguientes opciones para establecer la frecuencia de retirada:\* **Diariamente:&#x20;**&#x65;stablecer para retirar los dispositivos todos los días. |

- **Semanal:&#x20;**&#x65;specifique el día de la semana para programar la retirada.
- **Mensual:&#x20;**&#x63;onfigurar para retirar los dispositivos el primer día de cada mes. |

## Eliminar dispositivos retirados

**Procedimiento**

1. Vaya a **Administrador** > **Sistema** > **Limpieza de dispositivos**. Se abre la página Borrado de dispositivos.
2. Seleccione **Eliminar dispositivos retirados**.
3. Utilice la tabla **Eliminar dispositivos retirados** para especificar los detalles.
4. Haga clic en **Mostrar lista de dispositivos retirados**. Muestra la lista de dispositivos que se han retirado durante un número de días especificado.
5. Haga clic en **Eliminar dispositivos retirados ahora**, alternativamente, puede programar la eliminación del dispositivo.
6. El portal administrativo de Ivanti Neurons for MDM eliminará los dispositivos especificados.
7. Haga clic en **Guardar** para guardar sus ajustes.
8. (Opcional) Si actualiza los valores, puede hacer clic en **Restablecer** para restablecer los ajustes a sus valores iniciales.

### Eliminar dispositivos retirados

| Campo                                                                    | Descripción                                                                                                                                                                |
| ------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Elimine los dispositivos que se han retirado hace más de (días)**      | Días: 30 días por defecto, 365 días es el número máximo de días permitido.                                                                                                 |
| **Número máximo de dispositivos Retirados para eliminar en cada sesión** | Seleccione 100, 500 o 1000 (Predeterminado: 100)                                                                                                                           |
| **Borrar automáticamente dispositivos retirados según un calendario**    | Marque la casilla para retirar dispositivos según un calendario preestablecido.                                                                                            |
| **Eliminar la configuración programada**                                 | Seleccione una de las siguientes opciones para establecer la frecuencia de borrado:\* **Diariamente:&#x20;**&#x65;stablecer para eliminar los dispositivos todos los días. |

- **Semanal:&#x20;**&#x65;specifique el día de la semana para programar el borrado.
- **Mensual:&#x20;**&#x63;onfigurar para borrar los dispositivos retirados el primer día de cada mes. |

### Eliminar dispositivos borrados

**Procedimiento**

1. Vaya a **Administrador** > **Sistema** > **Limpieza de dispositivos**. Se abre la página Borrado de dispositivos.
2. Seleccione **Eliminar dispositivos borrados**.
3. Utilice la tabla **Eliminar dispositivos borrados** para especificar los detalles.
4. Haga clic en **Mostrar lista de dispositivos borrados**. Muestra la lista de dispositivos que se han retirado durante un número de días especificado.
5. Haga clic en **Eliminar dispositivos borrados ahora**, alternativamente, puede programar el borrado del dispositivo.
6. El portal administrativo de Ivanti Neurons for MDM eliminará los dispositivos especificados.
7. Haga clic en **Guardar** para guardar sus ajustes.
8. (Opcional) Si actualiza los valores, puede hacer clic en **Restablecer** para restablecer los ajustes a sus valores iniciales.

### Eliminar dispositivos borrados

| Campo                                                                   | Descripción                                                                                                                                                                         |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Elimine los dispositivos que se han borrado hace más de (días)**      | Días: 30 días por defecto, 365 días es el número máximo de días permitido.                                                                                                          |
| **Número máximo de dispositivos borrados para eliminar en cada sesión** | Seleccione 100, 500 o 1000 (Predeterminado: 100)                                                                                                                                    |
| **Eliminar automáticamente dispositivos borrados según un calendario**  | Seleccione la casilla de verificación para eliminar los dispositivos borrados según un calendario preestablecido.                                                                   |
| **Eliminar la configuración programada borrada**                        | Seleccione una de las siguientes opciones para establecer la frecuencia de borrado:\* **Diariamente:&#x20;**&#x65;stablecer para eliminar los dispositivos borrados todos los días. |

- **Semanal:&#x20;**&#x65;specifique el día de la semana para programar el borrado.
- **Mensual:&#x20;**&#x63;onfigurar para borrar los dispositivos retirados el primer día de cada mes. |

## Eliminar dispositivos pendientes de borrado

**Procedimiento**

1. Vaya a **Administrador** > **Sistema** > **Limpieza de dispositivos**. Se abre la página Borrado de dispositivos.
2. Seleccione **Eliminar dispositivos pendientes de borrado**.
3. Utilice la tabla **Eliminar dispositivos pendientes de borrados** para especificar los detalles.
4. Haga clic en **Mostrar lista de dispositivos borrados**. Muestra la lista de dispositivos que se van ha borrar durante el número de días especificado.
5. Haga clic en **Eliminar dispositivos pendientes de borrados ahora**, alternativamente, puede programar el borrado del dispositivo.
6. El portal administrativo de Ivanti Neurons for MDM eliminará los dispositivos especificados.
7. Haga clic en **Guardar** para guardar sus ajustes.
8. (Opcional) Si actualiza los valores, puede hacer clic en **Restablecer** para restablecer los ajustes a sus valores iniciales.

### Eliminar dispositivos pendientes de borrado

| Campo                                                                                | Descripción                                                                                                                                                                                       |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Elimine los dispositivos que llevan más de (días) pendientes de borrado**          | Días: 30 días por defecto, 365 días es el número máximo de días permitido.                                                                                                                        |
| **Número máximo de dispositivos pendientes de borrado para eliminar en cada sesión** | Seleccione 100, 500 o 1000 (Predeterminado: 100)                                                                                                                                                  |
| **Eliminar automáticamente dispositivos pendientes de borrado según un calendario**  | Seleccione la casilla de verificación para eliminar los dispositivos borrados según un calendario preestablecido.                                                                                 |
| **Eliminar la configuración programada pendiente de borrado**                        | Seleccione una de las siguientes opciones para establecer la frecuencia de borrado:\* **Diariamente:&#x20;**&#x65;stablecer para eliminar los dispositivos pendientes de borrados todos los días. |

- **Semanal:&#x20;**&#x65;specifique el día de la semana para programar el borrado.
- **Mensual:&#x20;**&#x63;onfigurar para borrar los dispositivos pendientes de borrar el primer día de cada mes. |

## Retirar el dispositivo pendiente de retirada.

**Procedimiento**

1. Vaya a **Administrador** > **Sistema** > **Limpieza de dispositivos**. Se abre la página Borrado de dispositivos.
2. Seleccione **Retirar el Dispositivo pendiente de retirada**.
3. Utilice la tabla **Retirar dispositivos pendientes** para especificar los detalles.
4. Haga clic en **Mostrar lista de dispositivos pendientes de retirada**. Muestra la lista de dispositivos que se van a retirar durante un número de días especificado.
5. Haga clic en **Forzar la retirada de Dispositivos pendientes de retirada ahora**. También puede programar la retirada de los dispositivos pendientes.
6. El portal administrativo de Ivanti Neurons for MDM retirará los dispositivos especificados.
7. Haga clic en **Guardar** para guardar sus ajustes.
8. (Opcional) Si actualiza los valores, puede hacer clic en **Restablecer** para restablecer los ajustes a sus valores iniciales.

### Retirar el dispositivo pendiente de retirada.

| Campo                                                                                      | Descripción                                                                                                                                                                          |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Retirar los dispositivos pendientes de retirada que no se han registrado más de (días)** | Días: 30 días por defecto, 365 días es el número máximo de días permitido.                                                                                                           |
| **Número máximo de dispositivos pendientes de retirada para Retirar en cada sesión**       | Seleccione 100, 500 o 1000 (Predeterminado: 100)                                                                                                                                     |
| **Retirar automáticamente los dispositivos pendientes de retirada según un calendario**    | Seleccione la casilla para retirar dispositivos pendientes según un calendario preestablecido.                                                                                       |
| **Retire la configuración programada pendiente de retirada**                               | Seleccione una de las siguientes opciones para establecer la frecuencia de borrado:\* **Diariamente:&#x20;**&#x65;stablecer para retirar los dispositivos pendientes todos los días. |

- **Semanal:&#x20;**&#x65;specifique el día de la semana para programar la retirada.
- **Mensual:&#x20;**&#x63;onfigurar para retirar los dispositivos el primer día de cada mes. |
