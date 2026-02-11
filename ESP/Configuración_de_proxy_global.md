---
title: Configuración de proxy global
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Licencia**: Silver

Mediante la configuración de proxy global se ajustan los dispositivos para que redireccionen el tráfico HTTP a un servidor proxy. La siguiente lista enumera los ajustes de proxy global:

| **Ajuste**                                                   | Qué hacer                                                                                                                                                                                                                                                                                                 |
| ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre                                                       | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                                                                                                                |
| Descripción                                                  | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                                                                                                                               |
| Tipo                                                         | Seleccione **Manual** o **Automática**. Si selecciona **Manual**, necesitará el nombre de host y el puerto del servidor proxy y, opcionalmente, el nombre de usuario y la contraseña para el servidor proxy. Si selecciona **Automática**, puede introducir una URL de autoconfiguración del proxy (PAC). |
| Nombre de host y puerto                                      | Si ha seleccionado **Manual**, introduzca el nombre de host y número de puerto para el servidor proxy.                                                                                                                                                                                                    |
| Usuario                                                      | (Opcional) Nombre de usuario para acceder al servidor proxy.\*                                                                                                                                                                                                                                            |
| Contraseña                                                   | (Opcional) Contraseña para acceder al servidor proxy.                                                                                                                                                                                                                                                     |
| URL de la PAC                                                | (Opcional) Si ha seleccionado **Automática**, puede introducir la URL del archivo PAC que define la configuración del proxy. Si deja en blanco este ajuste, el dispositivo utiliza el protocolo de autodescrubrimiento del proxy web (WPAD) para descubrir proxies.                                       |
| Permitir la conexión directa si no se puede acceder a la PAC | (iOS 7 y posterior) Seleccione para permitir una conexión directa si el dispositivo no puede acceder al archivo PAC por cualquier motivo.                                                                                                                                                                 |
| Permitir la omisión del proxy para acceder a redes cautivas  | (iOS 7 y posterior) Seleccione para permitir la omisión del proxy para visualizar la página de inicio de sesión para una red cautiva.                                                                                                                                                                     |

Escriba $ para ver una lista de [**variables&#x20;**](./Variables.md)compatibles, si las hubiera, para este campo.
