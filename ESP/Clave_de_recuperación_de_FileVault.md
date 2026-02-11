---
title: Clave de recuperación de FileVault
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

**Licencia:** Gold

La configuración de las claves de recuperación de FileVault determina la redirección y custodia de las claves de recuperación de FileVault a un servidor corporativo.

La configuración de la exclusión y reinserción de la clave de recuperación de File Vault está deactivada cuando un dispositivo macOS deja de enviar la clave de recuperación al volver a insertar la configuración.

Puede personalizar las siguientes opciones:

| **Ajuste**                                                            | **Descripción**                                                                                                                                                                                |
| --------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre                                                                | Introduzca un nombre que identifique a esta configuración.                                                                                                                                     |
| Descripción                                                           | Introduzca una descripción que explique la finalidad de esta configuración (opcional).                                                                                                         |
| Ajustes de configuración para macOS \<10.13                           |                                                                                                                                                                                                |
| Guarde la clave de recuperación del abonado de Ivanti Neurons for MDM | Seleccione esta opción para permitir que Ivanti Neurons for MDM almacene las claves en su abonado. Cuando sea necesario, la clave se puede descifrar desde la página Detalles del dispositivo. |
| Redirigir URL al servidor                                             | Introduzca los siguientes ajustes:\* Introduzca la **URL de redirección** a la que deben enviarse las claves de recuperación de FDE en lugar de a Apple. La URL debe comenzar con https\://.   |

- Seleccione un Certificado de la lista desplegable. Solamente es compatible el formato de certificado PKCS1. |
  \| Ajustes de configuración para macOS 10.13+                            |                                                                                                                                                                                                                                                                                                           |
  \| Ubicación                                                             | (Obligatorio) Introduzca una breve descripción de la localización donde se custodiará la clave de recuperación. Este texto se insertará en el mensaje que va a ver el usuario cuando active FileVault.                                                                                                    |
  \| Clave del dispositivo                                                 | (Opcional) Introduzca una cadena que se debe incluir en el texto de ayuda si el usuario parece haber olvidado la contraseña.                                                                                                                                                                              |
