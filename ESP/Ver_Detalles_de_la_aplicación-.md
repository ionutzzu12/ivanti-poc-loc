---
title: Ver Detalles de la aplicación
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Puede explorar los detalles desde el App Catalog hasta la aplicación en cualquiera de las aplicaciones del catálogo. En la página de detalles de la aplicación, se muestran los detalles de las aplicaciones como «Mostrar versión» (por ejemplo, 1.5.0), «Versión del paquete» (por ejemplo, 1.5.0.42) y «Versión mínima del sistema operativo obligatoria» (por ejemplo, 5.0 para Android).

Las aplicaciones que no cumplan con la versión especificada en el campo Versión mínima del sistema operativo obligatoria no se muestran en el catálogo de Apps\@Work. Por lo tanto, estas aplicaciones no están disponibles para su distribución a los dispositivos. El campo Versión mínima del sistema operativo obligatoria también se muestra como parte de las [**Trazas de auditoría**](./Panel.md) para las aplicaciones.

**Procedimiento**

1. Haga clic en **Aplicaciones**.
2. Haga clic en **Catálogo de aplicaciones**.
3. Seleccione la aplicación.

Aparece la ventana Detalles de la aplicación.

Para aplicaciones internas de iOS, puede comprobar la **Fecha de caducidad del perfil de aprovisionamiento** en la página de detalles de la aplicación.

La información de la aplicación muestra **Permitir instalación de aplicaciones en dispositivos M1 tras la distribución** como opción para todas las aplicaciones VPP de iOS e iPadOS. El administrador debe habilitar la opción **Permitir la instalación de la aplicación en dispositivos M1 al momento de la distribución** solo para aplicaciones VPP de iOS o iPad que se pueden instalar en el dispositivo M1 macOS. Solo después de habilitar esta opción, el administrador puede ver los dispositivos M1 macOS durante la instalación de la aplicación. La configuración de la aplicación administrada es compatible con aplicaciones VPP de iOS en dispositivos M1 Mac.

Para las aplicaciones de la AppStore de iOS, **Sincronizar nueva versión** comprueba y sincroniza las actualizaciones de las aplicaciones desde la iTunes Store. La versión actualizada de la aplicación se muestra en un plazo de 12 a 24 horas en función del calendario de sincronización de la aplicación.

Se añade un botón de activación para **Aplicaciones de requisitos previos** en detalles del Dispositivo. Los administradores pueden seleccionar esta opción y añadir aplicaciones como requisitos previos de una aplicación principal.

Tras distribuir una aplicación a distintos dispositivos, el estado de distribución de la aplicación se puede ver en la pestaña **Resumen de dispositivos**. La pestaña Resumen de dispositivos también contiene información sobre el número de dispositivos aptos, el número de dispositivos en los que se instaló la aplicación, el número de dispositivos en los que la instalación de la aplicación está pendiente y el número de dispositivos en los que falló la instalación de la aplicación. El número de dispositivos en estos cuadros se basa en los dispositivos que tienen Instalación obligatoria de aplicaciones, por lo que los administradores pueden realizar un seguimiento del despliegue inicial en las aplicaciones obligatorias.

Para conocer el número general de aplicaciones (incluidas las instaladas por el usuario), utilice la búsqueda en el Inventario de aplicaciones.

Las aplicaciones excluidas del dispositivo tienen pendiente el estado de distribución.

En la siguiente tabla se enumeran las razones por las que falla la instalación de aplicaciones en aplicaciones de iOS/OSX:

| Motivo                     | Descripción                                                                                                                                                    |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AppAlreadyInstalled        | "Aplicación ya instalada".                                                                                                                                     |
| AppStoreDisabled           | "La tienda de aplicaciones está desactivada".                                                                                                                  |
| CouldNotVerifyAppID        | "No se ha podido verificar el ID de la aplicación".                                                                                                            |
| Error                      | "La instalación de la aplicación ha fallado con un error desconocido".                                                                                         |
| ManagedButUninstalled      | "La aplicación está administrada, pero el usuario la ha eliminado. Cuando se instale de nuevo la aplicación (incluso por el usuario), se volverá a gestionar". |
| ManagementRejected         | "El usuario ha rechazado la conversión de una aplicación no administrada a una aplicación administrada".                                                       |
| NotAnApp                   | "El comando InstallApplication se rechaza debido a un identificador de aplicación no válido que resuelve un activo que no es una aplicación."                  |
| NotSupported               | "La aplicación no es compatible".                                                                                                                              |
| Otros                      | "Motivo para los nuevos errores añadidos".                                                                                                                     |
| PurchaseMethodNotSupported | "Para iOS 7 y posteriores, la aplicación no se puede instalar debido a un método de compra no válido (aplicable solo a aplicaciones VPP)."                     |
| UserInstalledApp           | "El usuario ha instalado la aplicación antes de que pudiera tener lugar la instalación de la aplicación administrada".                                         |
| UserRejected               | "El usuario rechazó la sugerencia de instalar la aplicación".                                                                                                  |
| UpdateRejected             | "El usuario rechazó la sugerencia de actualizar la aplicación".                                                                                                |

En la siguiente tabla se enumeran las razones por las que falla la instalación de aplicaciones en Android:

| Motivo                  | Descripción                                                                                                                                                          |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| USER\_INSTALLED         | "Ya se ha instalado en el dispositivo (fuera de MDM)".                                                                                                               |
| UNSUPPORTED             | "No compatible"                                                                                                                                                      |
| USER\_REJECTED\_INSTALL | "El usuario ha rechazado la instalación de la aplicación".                                                                                                           |
| ERROR\_INSTALL          | "Se ha detectado un error al intentar instalar; falló".                                                                                                              |
| UNRECOGNIZED            | "El artículo no se encuentra o ya no se rastrea (por ejemplo, error/desinstalado del dispositivo y eliminado del rastreo)".                                          |
| UNSUPPORTED\_INSTALL    | "Actualizado para cliente Android 3.0/servidor 22.0.0: es necesario un estado específico para realizar un seguimiento de la instalación frente a la desinstalación." |
| OCULTA                  | "Durante la cuarentena, se enviará el estado OCULTO/DESINSTALADO. Unquarantine debería volver a "instalardo".                                                        |
| OTROS                   | "Motivo para los nuevos errores añadidos".                                                                                                                           |

Para dispositivos Windows, si la aplicación está configurada para instalarse en segundo plano, en la Configuración de la aplicación, el Resumen de dispositivos muestra el número de dispositivos aptos, instalados, pendientes o fallidos para la aplicación.

## Visualización de la información del inventario de aplicaciones desde la página de detalles de la aplicación

Para ver la información del inventario de aplicaciones, haga clic en **Ver inventario de aplicaciones (todas las versiones)** para ver en **Dispositivos > Inventario de aplicaciones** una lista filtrada por ID de agrupación de esa aplicación.

![](<Resources/Images/Viewing App Details.png>)
