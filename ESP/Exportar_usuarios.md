---
title: Exportar usuarios
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Como administrador, puede exportar una lista de usuarios desde Ivanti Neurons for MDM.

Por motivos de seguridad, cuando se exporta el PIN de registro del dispositivo del usuario a un archivo CSV, el PIN se enmascarará como '****' en lugar del PIN real.

**Procedimiento**

1. Vaya a **Usuarios > Usuarios**.
2. Seleccione uno o más usuarios de la lista.
3. Haga clic en **Exportar a CSV**.

Verá una ventana emergente que le informará de que el informe exportado tardará un tiempo en procesarse. Una vez enviada la solicitud, debe esperar a que se complete la solicitud para enviar otra solicitud. Cuando el informe esté listo, recibirá un mensaje que le indicará que debe descargar o eliminar el informe generado. Usted también recibirá un correo electrónico con un enlace para descargar el informe.

Los detalles de los atributos **Usuario personalizado** y **LDAP** también se pueden exportar a un archivo CSV junto con otros detalles.

Cuando se agrega un usuario con un valor de campo que contiene los caracteres +,-,= o @, los datos del usuario del archivo CSV exportado añadirán automáticamente un prefijo al campo con una comilla única (') o un símbolo de barra (|) además de una barra diagonal inversa (\\). Esto se hace para evitar la vulnerabilidad de inserción en Excel.
