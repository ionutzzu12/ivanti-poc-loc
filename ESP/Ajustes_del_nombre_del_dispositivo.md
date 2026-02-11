---
title: Ajustes del nombre del dispositivo
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

## Licencia: Silver

Una configuración de nombre de dispositivo predeterminado le permite crear una nueva configuración que se envía al dispositivo en el nivel de registro o tras el registro y permite asignar un nombre al dispositivo.ç El administrador puede definir los nombres de dispositivos predeterminados solo para **dispositivos de iOS 8 supervisados**. Puede usar las siguientes variables para construir el nombre del dispositivo:

- Número de serie del dispositivo
- IMEI del dispositivo
- Modelo del dispositivo
- Ivanti Neurons for MDM Nombre de usuario (solo usuario locales)
- Unidad organizativa (OU) de LDAP
- Nombre común (CN) de LDAP

Por ejemplo, introduciría $\{NSdispositivo}-$\{OUusuario} para los nombres de dispositivos que comiencen por el número de serie del dispositivo y terminen con la organización del usuario, según se define en el LDAP.

**Ajustes predeterminados del nombre del dispositivo (para iOS)**

| **Ajuste**             | Qué hacer                                                                                                                                                                                                                                                                  |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre                 | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                                                                                 |
| Descripción            | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                                                                                                |
| Nombre del dispositivo | Introduzca el formato del nombre del dispositivo predeterminado, incluido el dispositivo disponible y los atributos de LDAP.\*Si el nombre resultante del dispositivo tiene más de 63 caracteres, se acortará para garantizar que aparece correctamente en el dispositivo. |
| Descripción            | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                                                                                                |

Escriba $ para ver una lista de [**variables&#x20;**](./Variables.md)compatibles, si las hubiera, para este campo.

**Ajustes del nombre del dispositivo (Android)**

El nombre del dispositivo Android se puede recuperar con Go app. Cuando el administrador genera el informe de Detalles del dispositivo, se muestra el nombre del dispositivo real en lugar del nombre del modelo o del fabricante del dispositivo. En caso de que el usuario cambie el nombre del dispositivo, el nuevo nombre se mostrará la siguiente vez que se genere el informe. El nombre de dispositivo respectivo se puede ver en **Dispositivos** > **Ajustes** > **Nombre del dispositivo**.
