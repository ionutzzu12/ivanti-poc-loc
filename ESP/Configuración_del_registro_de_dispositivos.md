---
title: Configuración del registro de dispositivos
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

La configuración de Registro de dispositivos le permite activar los registros de red y seguridad en dispositivos Android.

### Creación de la configuración del registro de dispositivos

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Seleccione **Configuraciones**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir**.
:::

:::WorkflowBlockItem
En el campo de búsqueda,escriba **Registro de dispositivos** y seleccione la configuración.
:::

:::WorkflowBlockItem
Introduzca un nombre y describa la configuración.
:::

:::WorkflowBlockItem
En la sección **Ajustes de configuración**, seleccione una opción o ambas:
:::

:::WorkflowBlockItem
- Activar el registro de red
- Registro de informes de seguridad
  Para obtener información sobre las versiones de Android compatibles con el registro de seguridad y de red, consulte las tablas en **Matriz de registro de seguridad** a continuación.

En la sección **Uso de la aplicación**, seleccione la opción **Activar la recopilación de datos de uso de la aplicación** para recopilar información sobre el uso de datos. Para activar esta opción es necesario que el usuario autorice la recopilación de datos de uso en el dispositivo.
:::

:::WorkflowBlockItem
- Recopilar datos de uso de aplicaciones: seleccione esta opción para recopilar los datos de uso de las aplicaciones del catálogo de aplicaciones.
  Los datos de uso de la aplicación se recopilan una vez al día y muestran el uso del día anterior. No se informa del uso actual. Se solicitará a los usuarios finales que den su permiso para recuperar esta información. Algunos fabricantes de dispositivos pueden permitir la concesión previa de este permiso en dispositivos totalmente gestionados mediante OEMConfig (configuraciones gestionadas). Esta función requiere una licencia de Secure UEM Premium.

Algunos fabricantes de dispositivos pueden permitir la concesión previa de este permiso en dispositivos totalmente gestionados mediante OEMConfig (configuraciones gestionadas).
:::

:::WorkflowBlockItem
Haga clic en **Siguiente** para configurar los ajustes de distribución.
:::

:::WorkflowBlockItem
Haga clic en **Hecho**.
:::
::::

**Matriz de informes de seguridad**

| Tipo de dispositivo                                                                | Versiones compatibles de Android |
| ---------------------------------------------------------------------------------- | -------------------------------- |
| Dispositivos gestionados para el trabajo y Work Managed Device Non-GMS mode (AOSP) | 7, 8, 9, 10, 11, 12, 13          |
| Dispositivos administrados con perfil profesional                                  | 8, 9, 10                         |
| Perfil de trabajo                                                                  | N/A                              |
| Perfil de trabajo en el Dispositivo propiedad de la empresa                        | 11, 12, 13                       |

**Matriz de registros de red**

| Tipo de dispositivo                                                                | Versiones compatibles de Android |
| ---------------------------------------------------------------------------------- | -------------------------------- |
| Dispositivos gestionados para el trabajo y Work Managed Device Non-GMS mode (AOSP) | 8, 9, 10, 11, 12, 13             |
| Dispositivos administrados con perfil profesional                                  | 8, 9, 10                         |
| Perfil de trabajo                                                                  | 12, 13                           |
| Perfil de trabajo en el Dispositivo propiedad de la empresa                        | 12, 13                           |

Después de instalar la Configuración de registro de dispositivos en el dispositivo, el usuario recibe una notificación con información sobre la Administración de dispositivos y el registro de redes. Haga clic en **Aceptar** para confirmar la notificación.

### Solicitar registros de depuración

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Inicie sesión en el Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Vaya a **Dispositivos&#x20;**>**Detalles del ispositivo**.
:::

:::WorkflowBlockItem
Desde la sección **Información general**, haga clic en el botón con tres puntos verticales que aparece junto al botón de **Forzar contacto**.
:::

:::WorkflowBlockItem
Seleccione **Solicitar registros de Debug**.
:::

:::WorkflowBlockItem
Seleccione una de las dos opciones siguientes:

- Excluir informe de errores: cuando se selecciona esta opción y se hace clic en Siguiente, aparece en la pantalla una ventana de confirmación. Haga clic en **Solicitar registros de depuración**. Los usuarios no deben dar consentimiento para esta opción y estos registros excluirán la notificación de errores para los dispositivos Android seleccionados.
- Incluir informe de errores: cuando se selecciona esta opción y se hace clic en Siguiente, aparece en la pantalla una ventana de confirmación. Haga clic en **Solicitar registros de depuración**. Los usuarios deben dar el consentimiento para compartir un informe de errores. En el caso de dispositivos Android, se avisará a los usuarios de que deben enviar los informes del dispositivo, que deben incluir informes de errores.
:::
::::
