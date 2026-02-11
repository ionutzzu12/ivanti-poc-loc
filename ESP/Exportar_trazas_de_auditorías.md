---
title: Exportar trazas de auditorías
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Exportar Audit Trails es una característica que se usa para exportar y cargar toda la información sobre Audit Trails a un servidor específico. El servidor debe ser accesible desde el puerto predeterminado. Los usuarios pueden configurar los ajustes de esta opción para que las trazas de auditorías se suban diariamente, de forma automática, a una ubicación específica.

La exportación de Audit Trails es compatible con los servidores SFTP basados en Linux y en Windows.

Para configurar los ajustes de la exportación de trazas de auditorías:

1. Seleccione **Administrador > Infraestructura > trazas de auditorías**. Aparecerá la página **Trazas de auditorías**.
2. En la página **Trazas de auditorías**, haga clic en **ACTIVAR** para activar la exportación de trazas de auditorías.
3. En la sección **Exportar**, actualice los siguientes campos:

| **Característica**         | **Descripción**                                                                                                              |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Formato de exportación** | Seleccione cualquiera de los siguientes formatos en los que desee exportar los datos de las trazas de auditorías:\* **JSON** |

:::Paragraph{listStyleType="disc" indent="2"}
**CEF** (formato de evento común)El mensaje del registro CEF contiene los siguientes valores predeterminados:\* Versión: número de versión del formato CEF. v25 es la versión actual compatible.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Proveedor del dispositivo: Ivanti Inc
:::

:::Paragraph{listStyleType="disc" indent="3"}
Producto del dispositivo: Ivanti Neurons for MDM
:::

:::Paragraph{listStyleType="disc" indent="3"}
Versión del dispositivo: última versión de Ivanti Neurons for MDM al momento de generar el evento.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Id. de clase de evento del dispositivo: Id. única de la entidad por traza
:::

:::Paragraph{listStyleType="disc" indent="3"}
Nombre: nombre de la entidad y acción por traza. Ejemplo: ajustes de la configuración de distribución de promociones, Crear.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Severidad: indica la importancia del evento. Ejemplo: baja.El mensaje del registro CEF también contiene los campos de la extensión, que son una recopilación de los siguientes pares de valores de clave:\* CS1 y etiqueta CS1: metadatos de trazas de auditorías tales como creadoEn, TipoDeEntidad, NombreDeEntidad y TipoDeAcción
:::

:::Paragraph{listStyleType="disc" indent="3"}
CS2 y etiqueta CS2: información de los participantes.
:::

:::Paragraph{listStyleType="disc" indent="3"}
CS3 y etiqueta CS3: estado previo a la acción.
:::

:::Paragraph{listStyleType="disc" indent="3"}
CS4 y etiqueta CS4: estado posterior a la acción.En la exportación de CEF, si alguno de los campos (por ejemplo, claves CS3 o CS4) exceden los límites especificados, el valor actual se reemplaza por el texto "El valor de esta clave excede la longitud permitida para la clave de diccionario asignada". |
\| **Servidor**                           | Introduzca el nombre del servidor al que se van a exportar las trazas de auditorías.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
\| **Usuario**                            | Introduzca el nombre de usuario para iniciar sesión en el servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
\| **Contraseña**                         | Introduzca la contraseña de inicio de sesión del servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
\| **Ruta del servidor**                  | Introduzca la ruta del servidor. Asegúrese de que la ruta proporcionada existe en el servidor. Ejemplo: /Usuarios/Prueba/Exportación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
\| **Algoritmo de intercambio de claves** | Seleccione la lista de algoritmos de intercambio de claves para exportar las trazas de auditorías para la configuración de SFTP de salida.Los siguientes algoritmos de intercambio de claves están seleccionados por defecto:\* **diffie-hellman-group-exchange-sha1**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**diffie-hellman-group14-sha1**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**curve25519-sha256**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**diffie-hellman-group-exchange-sha256** (seleccionado por defecto)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
\| **Cifrados**                           | Seleccione la lista de cifrados de encriptación para exportar el registro de auditorías para la configuración de SFTP de salida. Los siguientes cifrados de cifrado están seleccionados por defecto:\* **aes128-ctr**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**aes192-ctr**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**aes256-ctr** (seleccionado por defecto)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
\| **HMAC**                               | Seleccione la lista de algoritmos de HMAC para exportar las trazas de auditorías para la configuración de SFTP de salida.\* hmac-sha1 (seleccionado por defecto)
:::

:::Paragraph{listStyleType="disc" indent="2"}
hmac-sha2-256
:::

:::Paragraph{listStyleType="disc" indent="2"}
hmac-sha2-512                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
los campos mencionados anteriormente serán de solo lectura si ya se han configurado. Para editar los campos ya configurados deberá hacer clic en el botón **Editar**. Si el administrador ya había configurado la exportación a SFTP, después de la actualización se seleccionarán todos los Algoritmos de claves.
:::

:::Paragraph{indent="1"}
Haga clic en **Probar conexión y continuar** para probar la conexión del servidor y guardar la configuración de las exportaciones de las trazas de auditorías.
Los archivos de las trazas de auditorías guardados están disponibles en formato JSON en un archivo .zip.
Verifique los ajustes de configuración en todos los campos antes de guardar los ajustes de exportación de las Trazas de auditoría. Si alguno de los valores de campo introducidos no es válido, aparecerá un mensaje de error.
:::
