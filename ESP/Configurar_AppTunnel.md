---
title: Configurar AppTunnel
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

AppTunnel protege los datos de las aplicaciones al proporcionar seguridad en las sesiones «aplicación por aplicación» entre el contenedor de cada aplicación y la red corporativa.

Esta sección contiene los siguientes temas:

- [**Configurar el Sentry para que use AppTunnel con certificados**](./Configurar_AppTunnel.md)
- [**Carga de certificados Sentry**](./Configurar_AppTunnel.md)
- [**Configurar que las aplicaciones usen AppTunnel**](./Configurar_AppTunnel.md)
- [**Acerca del nombre de servicio de AppTunnel**](./Configurar_AppTunnel.md)

## Configurar el Sentry para que use AppTunnel con certificados

Cuando instala por primera vez Standalone Sentry, también se instala un certificado autofirmado. Ivanti recomienda encarecidamente que sustituya el certificado predeterminado por un certificado de terceros de confianza pública.

**Requisitos previos**

- AppTunnel depende de la versión más reciente compatible con el Sentry. Complete la instalación del Sentry antes de iniciar las tareas de configuración de AppTunnel.
- Si desea usar una identidad SCEP:\* Añada una [**Entidad de Certificación**](./Gestión_de_certificados.md) local o externa. Es necesaria una instalación de Conector.
  - Añada una configuración del certificado de identidad de la aplicación. Esta es la distribución dinámica que usará cuando configure AppTunnel.

Puede configurar ActiveSync o AppTunnel mediante certificados X.509 para que la autenticación utilice los servidores Sentry asignados a un perfil.

**Procedimiento**

1. Vaya a **Administrador > Sentry**.
2. Haga clic en **+ Añadir perfil de Sentry**.
3. Haga clic en **ActiveSync y/o AppTunnel con certificados**.
4. Haga clic en **Siguiente**.
5. Use las directrices que aparecen en la siguiente tabla para completar la página de **Ajustes globales**.| Tabla: Ajustes globales para Administración > Sentry                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   \| --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Ajuste                                                                                  | **Qué hacer**                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   \| **Nombre**,                                                                             | Introduzca un nombre que identifique a este perfil.                                                                                                                                                                                                                                                                                                                                                                                                                 |
   \| **Descripción**                                                                         | Introduzca una descripción que explique la finalidad de este perfil.                                                                                                                                                                                                                                                                                                                                                                                                |
   \| **Nombre de host y puerto externos**                                                    | Introduzca el nombre de host y el puerto del Sentry.                                                                                                                                                                                                                                                                                                                                                                                                                |
   \| **Modo de autenticación del dispositivo**                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   \| **Utilizar un único certificado para la autenticación en dos fases**                    | Seleccione esta opción para usar un único certificado para la autenticación. Si todavía no tiene un [**certificado cargado**](./Configuración_del_certificado.md), puede hacerlo en el área que se muestra debajo de la opción seleccionada.                                                                                                                                                                                                                               |
   \| **Seleccionar certificado**                                                             | Para cargar un certificado de grupo necesario para la autenticación del dispositivo:1) Haga clic en **Añadir**. Aparecerá la ventana **Añadir certificado**.
   2\) Escriba el nombre del certificado en el campo **Nombre del certificado**.
   3\) Escriba la contraseña que protege el archivo PKCS12.
   4\) Haga clic en **Elegir archivo** para cargar el certificado de grupo. Asegúrese de que el formato del archivo sea en .p7b, .p12, .pfx, .pem, .der, .crt o .cer. |
   \| **Activar la lista de revocación de certificados (CRL)**                                | Seleccione esta opción para validar los certificados presentados por el dispositivo junto a la lista de revocación de certificados (CRL) publicada por la EC.                                                                                                                                                                                                                                                                                                       |
   \| **Comportamiento predeterminado de los dispositivos no administrados**                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   \| **Permitir que los dispositivos no administrados reciban correos electrónicos y datos** | Seleccione esta opción si no quiere bloquear el acceso a los datos para los dispositivos que no estén administrados con Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                |
6. Haga clic en **Siguiente**.
7. En la página de **Configuración del servidor sentry**, configure los campos siguientes:

| Tabla: Configuración del servidor de Sentry para Administrador > Sentry |                                                                                  |
| ----------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Ajuste                                                                  | Qué hacer                                                                        |
| **Protocolo de escucha**                                                | Seleccione cualquiera de las siguientes opciones del protocolo:\* **Solo HTTPS** |

:::Paragraph{listStyleType="disc" indent="2"}
**Solo HTTP**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**HTTPS y HTTP**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
\| **Puerto HTTPS**                                                        | Introduzca el número de puerto Https. Este campo no se mostrará si el protocolo de escucha está seleccionado como Solo HTTP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
\| **Puerto HTTP**                                                         | Introduzca el número de puerto HTTP. Este campo no se mostrará si el protocolo de escucha está seleccionado como Solo HTTPS.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
\| **Certificado/clave del servidor TLS del Sentry**                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
\| **Utilizar el certificado autofirmado de Sentry**                       | Seleccione esta opción para usar el certificado autofirmado creado por el servicio Ivanti Neurons for MDM y se le enviará a Sentry como parte de este perfil. Este certificado se utiliza para la comunicación entre Sentry y los dispositivos móviles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
\| **Añadir**                                                              | Para cargar su propio certificado necesario para la autenticación del dispositivo:1) Haga clic en **Añadir**. Aparecerá la ventana **Añadir certificado**.Podrá ver esta opción solo cuando anule la selección de la opción **Utilizar el certificado autofirmado de Sentry**.
:::

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
Escriba el nombre del certificado en el campo **Nombre del certificado**.
:::

:::Paragraph{listStyleType="decimal" listStart="3" indent="2"}
Escriba la contraseña que protege el archivo PKCS12.
:::

:::Paragraph{listStyleType="decimal" listStart="4" indent="2"}
Haga clic en **Elegir archivo** para cargar el certificado. Asegúrese de que el archivo esté en formato .p12.
:::

:::Paragraph{listStyleType="decimal" listStart="5" indent="2"}
Haga clic en **Añadir**.Todos los certificados del servidor TLS cargados (incluidos los cargados desde la página principal de Sentry y desde otros perfiles) se muestran en la sección Certificado/certificado/clave del servidor TLS del Sentry. Para seleccionar el certificado TLS necesario para la autenticación, haga clic en el botón de radio que hay junto al certificado. |
\| **Agregar un segundo certificado**                                      | Seleccione para activar el segundo certificado. Una vez que el certificado principal caduque, Sentry cambiará automáticamente al certificado de respaldo sin intervención del administrador.Tunnel ya almacena ambos certificados y puede coincidir con cualquiera de ellos, asegurando una conectividad ininterrumpida.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
\| **Protocolos**                                                          | Seleccione los protocolos de entrada y salida necesarios.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
\| **Conjuntos de cifrado**                                                | Los cifrados se utilizan en la comunicación cifrada SSL con el Sentry. Normalmente se prefieren cifrados fuertes. Puede que los dispositivos más antiguos necesiten cifrados débiles. El cifrado fuerte se selecciona de manera predeterminada. Seleccione los cifrados adicionales que desee utilizar. Se debe seleccionar, al menos, un cifrado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
Haga clic en **Siguiente**.
:::

9. Añada al menos uno de los servicios que se muestran.
10. Haga clic en **Guardar**.

Una vez que haya registrado el Sentry, este se mostrará en la página de Sentry en la sección de Servidores Sentry no configurados. Para asignarle un perfil al Sentry, haga clic en **Asignar** en la columna **Acciones**.

## Carga de certificados Sentry

Ivanti Neurons for MDM carga los certificados del servidor TLS y los certificados de grupo cuando se crea un perfil de Sentry. También puede cargar estos certificados desde la página **Sentry**, en la sección **Certificados Sentry**.

Ivanti Neurons valida los certificados de Sentry durante la carga, y devuelve los siguientes tipos de información según las condiciones que se han encontrado en los certificados:

| Condición                                                                                                                                         | Tipo de información |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| El certificado de hoja no contiene una cadena a ninguna autoridad de certificación o no hay una autoridad de certificación en el archivo cargado. | Error               |
| No hay disponible ninguna autoridad de certificación de raíz.                                                                                     | Advertencia         |
| La autoridad de certificación de raíz no ha aprobado la autoridad de certificación intermedia para el certificado de hoja.                        | Advertencia         |

Ivanti Neurons for MDM también valida con las reglas de [**este artículo**](https://support.apple.com/en-us/HT210176).

**Procedimiento**

1. En la sección **Certificados de servidor TLS**, haga clic en **Añadir**. Aparecerá la ventana **Añadir certificado**.
2. Escriba el nombre del certificado en el campo **Nombre del certificado**.
3. Escriba la contraseña que protege el archivo PKCS12.
4. Haga clic en **Seleccionar archivo** para cargar el certificado de grupo. Asegúrese de que el formato del archivo sea .p7b, .p12, .pfx, .pem, .der, .crt o .cer.
5. Haga clic en **Añadir**. El certificado cargado aparecerá en la tabla.
6. Para eliminar el certificado del servidor TLS, haga clic en el icono Eliminar en la columna **Acciones**.

Si el certificado del servidor TLS se usa en algún perfil de Sentry, no podrá eliminar el certificado. Si se realiza la acción a eliminar, se mostrará un mensaje de error.

### Certificados de Añadir grupo

**Procedimiento**

1. En la sección **Certificados de grupo**, haga clic en **Añadir**. Aparecerá la ventana **Añadir certificado**.
2. Escriba el nombre del certificado en el campo **Nombre del certificado**.
3. Escriba la contraseña que protege el archivo PKCS12.
4. Haga clic en **Seleccionar archivo** para cargar el certificado de grupo. Asegúrese de que el formato del archivo sea .p7b, .p12, .pfx, .pem, .der, .crt o .cer.
5. Haga clic en **Añadir**.

Para eliminar el certificado de grupo cargado, haga clic en el icono Eliminar en la columna **Acciones**.

### Editar el certificado raíz de Sentry

Como administrador tiene la opción de editar la distribución de la configuración del Certificado Raíz Sentry. También puede proporcionar permiso de edición al administrador del espacio personalizado delegando la configuración a otros espacios.

1. Vaya a **Configuraciones**.
2. Busque el **certificado raíz de Sentry**.
3. Haga clic en el icono editar.
4. Seleccione las casilla de verificación que correspondan con los Dispositivos o Grupos de dispositivos a los que desee distribuir los certificados. También puede desmarcar las casillas de verificación que correspondan a los Dispositivos o Grupos de dispositivos.
5. Seleccione una de las opciones siguientes de la sección Resumen de distribución según corresponda:\* **No aplicar a otros espacios**
   - **Aplicar a los dispositivos de otros espacios**
6. (Opcional) Haga clic en la casilla **Permitir que el administrador del espacio edite la distribución**.
7. Haga clic en **Guardar**.
8. Aparece un mensaje de advertencia. Haga clic en **Sí** para confirmar.

## Configurar que las aplicaciones usen AppTunnel

Para las últimas instrucciones de Sentry, visite [**Documentación del producto**](https://help.ivanti.com#116) y haga clic en Sentry. Seleccione el documento apropiado para su versión de Sentry.

## Acerca del nombre de servicio de AppTunnel

El servicio de AppTunnel define el servicio «back-end» al que se conecta una aplicación AppConnect.

Para obtener las instrucciones más recientes, visite [**Documentación del producto**](https://help.ivanti.com) y seleccione los documentos que correspondan a sus versiones de[**&#x20;Sentry**](https://help.ivanti.com/#116) y [**AppConnect**](https://help.ivanti.com/#103).
