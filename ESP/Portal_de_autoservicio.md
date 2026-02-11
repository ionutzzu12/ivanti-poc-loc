---
title: Portal de autoservicio
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

La invitación a registrarse incluye también un vínculo al Portal de autoservicio. Los usuarios finales pueden usar este portal para realizar las siguientes tareas:

- Bloquear
- Desbloquear
- Ver ubicación (si está activada en la[**&#x20;configuración de privacidad**](./Configuración_de_privacidad.md))
- Borrar
- Retirar
- Cambiar la información de la cuenta (nombre, contraseña, dirección de correo electrónico)
- Forzar ingreso
- Añadir certificados de cifrado y firma

Para registrar dispositivos adicionales, los usuarios finales deben hacer clic en el vínculo del portal del registro que aparece en el Portal de autoservicio.

Si los usuarios finales pierden la URL para el Portal de autoservicio, envíelos a [**https://mydevices.mobileiron.com/user/login.html**](https://mydevices.mobileiron.com/user/login.html). Para los usuarios de iOS, considere la posibilidad de crear una [**Configuración del clip web**](./Crear_una_configuración_de_Web_Clip.md) para el Portal de autoservicio.

## Cargar certificados de firma y cifrado

Puede permitir que los usuarios finales carguen sus certificados de firma y cifrado en el portal de autoservicio dentro de la configuración de Certificados proporcionados por el usuario. Este ajuste se puede configurar mediante la configuración de Certificados proporcionados por el usuario. Una vez configurado, los usuarios finales pueden cargar sus certificados de firma y cifrado de correos electrónicos.

1. En la pestaña **Mis certificados**, haga clic en **Añadir certificado**. Aparecerá la ventana **Añadir certificado**.
2. Actualice los siguientes campos:|                      |                                                                                                                                                                                                                                                                                                                                                                            |
   \| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Nombre del campo     | Descripción                                                                                                                                                                                                                                                                                                                                                                |
   \| Tipo de certificado  | Seleccione el tipo de certificado a cargar. Existen las siguientes opciones:\* **Certificado de cifrado**
   - **Certificado de firma**Estas opciones son creadas desde el Portal de administración deIvanti Neurons for MDM. Consulte [**Configuración del certificado de identidad**](./Certificado_de_identidad.md) para obtener más información. |
     \| Certificado a cargar | Haga clic en **Elegir archivo** para seleccionar el archivo del certificado que se va a cargar.Asegúrese de que el archivo esté en formato PKCS12.                                                                                                                                                                                                                         |
     \| Contraseña           | Escriba la contraseña utilizada para el archivo.                                                                                                                                                                                                                                                                                                                           |
3. Haga clic en **Cargar**.

Una vez cargado, podrá ver la lista de certificados en una tabla que muestra los siguientes detalles.

| Nombre del campo       | Descripción                                                                                                           |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Nombre del certificado | Especifica el tipo de certificados, ya sea de **cifrado** o de **firma**.                                             |
| Emitido por            | Los detalles de los certificados emitidos.                                                                            |
| Cargado el             | La fecha en que se cargó el certificado.                                                                              |
| Fecha de caducidad     | L fecha de caducidad del certificado.                                                                                 |
| Acciones               | Puede llevar a cabo las siguientes acciones:\* **Editar certificado**: se pueden editar los detalles del certificado. |

- **Borrar clave privada**: borra la clave privada del paquete del certificado(PKCS#12).
- **Eliminar certificado**: se elimina el certificado del servidor de Ivanti Neurons for MDM. |

Cuando el usuario carga la configuración de un certificado, el servidor vuelve a insertar la configuración que está utilizando ese certificado.

si un usuario elimina y borra la clave privada, no se volverán a insertar las configuraciones.
