---
title: Configuración de Google
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

La configuración de la cuenta de Google conecta dispositivos iOS 9.3.2 y visionOS 1.1 o Android 6.0+, o versiones más recientes compatibles, a cuentas de Google. Es necesario tener la versión corporativa de Android para las cuentas de Google. La configuración puede establecer varias direcciones de correo electrónico de Google y cualquier otro servicio de Google que el usuario habilite después de la autenticación.

**Procedimiento**

1. Vaya a **Configuración > +Añadir**.
2. Seleccione la configuración **Cuenta de Google**.
3. Introduzca un nombre para la configuración.
4. Introduzca una descripción.
5. En la sección Establecimiento de la configuración, especifique los demás ajustes según se describe en la siguiente tabla:

| **Ajuste**                              | **Qué hacer**                                                                                                                                                                                                                                                                                     |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **iOS 9.3.2+\*\*\*\*, Android 6.0+**    |                                                                                                                                                                                                                                                                                                   |
| Nombre                                  | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                                                                                                        |
| Descripción de la cuenta                | Introduzca el nombre en pantalla de la cuenta.                                                                                                                                                                                                                                                    |
| Nombre de la cuenta                     | Introduzca el nombre completo del usuario de la cuenta.                                                                                                                                                                                                                                           |
| Dirección de correo electrónico         | Introduzca la dirección de correo electrónico de Google de la cuenta.                                                                                                                                                                                                                             |
| VPN por aplicación                      | **Requisito previo**: configure Tunnel o cualquier configuración de VPN por aplicación, antes de configurar la VPN por aplicación en la configuración de la cuenta de Google.En el menú desplegable, seleccione la configuración VPN pre-configurada por aplicación.**Disponible para**: iOS 14+  |
| **iOS 10+**                             |                                                                                                                                                                                                                                                                                                   |
| **Reglas del servicio de comunicación** | Seleccione una aplicación predeterminada para realizar llamadas de audio a los contactos del sistema de Google seleccionando cualquiera de las siguientes opciones:\* **Desde el App Catalog y las aplicaciones del sistema**: busque la aplicación escribiendo las primeras letras de su nombre. |

:::Paragraph{listStyleType="disc" indent="2"}
**Introduzca la Id. del paquete (solo para aplicaciones de sistema de Apple)**: escriba la Id. del paquete de la aplicación del sistema. La Id. del paquete debe comenzar con «com.apple». |
:::

7. Haga clic en **Siguiente**.
8. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
   - Ningún dispositivo (predeterminada)
   - personalizada
9. Haga clic en **Hecho**.

Cuando la configuración de una cuenta de Google se aplica al dispositivo, el cliente Go solicita al usuario que iniciar sesión en sesión en Google.
