---
title: Configuración del Bloqueo de activación de Apple
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

**Licencia:** Silver

Esta sección contiene los siguientes temas:

- [**Activar el bloqueo de activación de iOS**](./Configuración_del_Bloqueo_de_activación_de_Apple.md)
- [**Activar la característica bloqueo de activación de Apple en los dispositivos supervisados**](./Configuración_del_Bloqueo_de_activación_de_Apple.md)
- [**Activar el bloqueo de activación de macOS**](./Configuración_del_Bloqueo_de_activación_de_Apple.md)
- [**Activar la característica bloqueo de activación de macOS en los dispositivos supervisados**](./Configuración_del_Bloqueo_de_activación_de_Apple.md)
- [**Usar el código de derivación del bloqueo de activación de iOS**](./Configuración_del_Bloqueo_de_activación_de_Apple.md)
- [**Quitar el código de derivación del bloqueo de activación de iOS**](./Configuración_del_Bloqueo_de_activación_de_Apple.md)

El Bloqueo de activación es una característica de Apple diseñada para impedir el uso de un dispositivo perdido o robado por parte de terceras personas. Después de que se activa «Buscar», se guarda en los servidores de activación de Apple una asignación entre esta cuenta de iCloud y el identificador de hardware de este dispositivo. Desde ese momento, nadie puede desactivar «Buscar», borrar el dispositivo o reactivarlo sin introducir la Id. de Apple y la contraseña existentes. Si una tercera persona ajena al usuario borra el dispositivo e intenta posteriormente reactivarlo y usarlo, se le pedirá la Id. de Apple y la contraseña en el Asistente de configuración.

Al desactivar el Bloqueo de activación no se desactivará esta característica en los dispositivos supervisados si el usuario final ha habilitado Encontrar mi dispositivo. El Asistente de configuración solicitará al usuario que realice alguna acción cuando el dispositivo sea restablecido o borrado de forma remota.

El Bloqueo de activación proporciona a los administradores más opciones para prevenir el robo de dispositivos supervisados. Sin embargo, la mayoría de los administradores corporativos tienden a dejar el Bloqueo de activación deshabilitado porque es una característica eminentemente de consumidor. La siguiente tabla resume las opciones para implementaciones corporativas:

| Tipo de dispositivo           | Resultado                                                                                            |
| ----------------------------- | ---------------------------------------------------------------------------------------------------- |
| Corporativo y con supervisión | - El Bloqueo de activación está habilitado de forma predeterminada en los dispositivos supervisados. |

- Los usuarios del dispositivo no pueden activar el Bloqueo de activación.                                                                                                                                                                                                                                                                   |
  \| Corporativo y no supervisado  | \* El Bloqueo de activación estará habilitado en cuanto el usuario final inicie sesión en iCloud con su Id. de Apple y active Encontrar mi dispositivo.
- Los servidores MDM, como Ivanti Neurons for MDM, no pueden controlar el Bloqueo de activación en dispositivos no supervisados. Los usuarios de dispositivos pueden bloquear la activación con sus credenciales personales, dejándole sin recursos en caso de que se vayan de la empresa. |

## Activar el bloqueo de activación de iOS

**Aplicable a:** dispositivos iOS 7+ supervisados

Esta configuración se aplicará a los dispositivos Supervisados (iOS 7 y posterior) que tengan habilitada la función [**Buscar**](https://www.apple.com/icloud/find-my/). Si un administrador u otro usuarios intenta Borrar, Activar o desactivar la opción Buscar mi dispositivo en el dispositivo, aparecerá la pantalla de Bloqueo de activación de Apple. Para proceder, deben introducirse las credenciales de iTunes o un código de derivación.

El código de derivación para los dispositivos supervisados se almacenará tras la activación y se puede ver en los detalles del dispositivo. El código de derivación se puede enviar de forma remota usando el comando «Quitar bloqueo de activación» para los dispositivos supervisados. No obstante, el código debe introducirse manualmente al reactivar un dispositivo o desactivar la función Encontrar mi dispositivo.

Solo se puede crear una configuración del bloqueo de activación para todos los espacios.

## Activar la característica bloqueo de activación de Apple en los dispositivos supervisados

**Procedimiento**

1. Habilite la función **Buscar** en su dispositivo.
2. Vaya a **Configuraciones**.
3. Seleccione la configuración del **Bloqueo de activación de Apple** en la lista de configuraciones existentes.
4. Haga clic en **Editar**.
5. En la sección iOS 7+ supervisado, haga clic en **Activar Bloqueo de activación**.
6. Haga clic en **Hecho**.
7. Registre el dispositivo.

## Activar el bloqueo de activación de macOS

**Aplicable a:** dispositivos macOS 10.15+ supervisados

Esta configuración se aplicará a los dispositivos supervisados con macOS 10.15 y posteriores. El bloqueo de activación en macOS solo es aplicable a los Mac que tienen un chip de seguridad Apple T2. En los dispositivos supervisados, ya sean actualizados o recién instalados, y en los dispositivos registrados que estén ahora mismo actualizados, el bloqueo de activación está desactivado de forma predeterminada. La activación de «Encontrar mi...» no activa automáticamente el bloqueo de activación en estos dispositivos

Si un administrador u otro usuarios intenta Borrar, Activar o desactivar la opción «Buscar» en el dispositivo, aparecerá la pantalla de Bloqueo de activación de Apple. Para proceder, deben introducirse las credenciales de iTunes o un código de derivación. El código de derivación para los dispositivos supervisados se almacenará tras la activación y se puede ver en los detalles del dispositivo. El código de derivación se puede enviar de forma remota usando el comando «Quitar bloqueo de activación» para los dispositivos supervisados. No obstante, el código debe introducirse manualmente al reactivar un dispositivo o desactivar la función «Buscar».

Solo se puede crear una configuración del bloqueo de activación para todos los espacios.

## Activar la característica bloqueo de activación de macOS en los dispositivos supervisados

**Procedimiento**

1. Habilite la función «Buscar» en su dispositivo.
2. Vaya a **Configuraciones**.
3. Seleccione la configuración del **Bloqueo de activación de Apple** en la lista de configuraciones existentes.
4. Haga clic en **Editar**.
5. En la sección macOS 10.15+ supervisado, haga clic en **Activar Bloqueo de activación**.
6. Haga clic en **Hecho**.
7. Registre el dispositivo.

## Usar el código de derivación del Bloqueo de activación de iOS

Cuando el dispositivo se ha borrado con el Bloqueo de activación de iOS habilitado, el código de activación se retiene en el servidor de activación de Apple y en la interfaz de administración de Ivanti Neurons for MDM.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Seleccione el dispositivo.
3. Haga clic en **Acciones > Borrar**. Puede que el dispositivo tarde algunos minutos en reiniciarse.
4. Cuando el dispositivo le solicite la Id. de Apple y la contraseña, deje vacío el campo de la **Id. de Apple**.
5. Introduzca el código de derivación en el campo de la **contraseña**.
6. Haga clic en **Siguiente**.  
7. Continúe con la configuración.

## Quitar el código de derivación del Bloqueo de activación de iOS

Cuando el bloqueo de activación de iOS está quitado de la interfaz de administración de Ivanti Neurons for MDM, el código de derivación se elimina del servidor de activación de Apple, pero sigue estando presente en los detalles del dispositivo de la interfaz de administración de Ivanti Neurons for MDM.

**Procedimiento**

1. Vaya a **Dispositivos**.  
2. Seleccione el dispositivo.
3. Seleccione **Configuraciones**.
4. Seleccione **Bloqueo de activación de Apple**.
5. Haga clic en **Editar**.
6. En la sección iOS 7+ supervisado, desactive **Activar Bloqueo de activación**.
7. Haga clic en **Hecho**.
8. Vaya a **Dispositivos**.  
9. Seleccione el dispositivo.
10. Haga clic en **Acciones > Borrar**. Puede que el dispositivo tarde algunos minutos en reiniciarse. El dispositivo ahora se puede ajustar con la nueva AppleID y contraseña del usuario. 
11. Continúe con la configuración.

El estado de Quitar bloqueo de activación de iOS aparece en la interfaz de la siguiente manera:

| Estado    | Resultado                                                                      |
| --------- | ------------------------------------------------------------------------------ |
| Pendiente | - El servidor está enviando el código de Borrar bloqueo de activación a Apple. |
| Enviado   | \* Apple confirmar la recepción del código de Quitar bloqueo de activación.    |
| Error     | - El servidor no pudo enviar el código a Apple.                                |

- Apple ha notificado un error. |
