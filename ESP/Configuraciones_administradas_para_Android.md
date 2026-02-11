---
title: Configuraciones administradas para Android
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Utilizar las configuraciones administradas para Android Enterprise**](./Configuraciones_administradas_para_Android.md)
- [**Restricciones y permisos de aplicaciones para aplicaciones internas**](./Configuraciones_administradas_para_Android.md)
- [**Configuración de Gmail con Android Enterprise**](./Configuraciones_administradas_para_Android.md)

Si Ivanti Neurons for MDM tiene habilitado Android Enterprise, la configuración de Android Enterprise estará disponible para usarse por aplicación.

## Utilizar las configuraciones administradas para Android Enterprise

::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en **Aplicaciones**.
:::

:::WorkflowBlockItem
Haga clic en **Catálogo de aplicaciones**.
:::

:::WorkflowBlockItem
Seleccione una aplicación para la que realizar la configuración de Android Enterprise.
:::

:::WorkflowBlockItem
Haga clic en **Configuraciones de aplicaciones**.
:::

:::WorkflowBlockItem
Haga clic en **Configuraciones administradas para Android**.
:::

:::WorkflowBlockItem
Introduzca un nombre para la configuración.
:::

:::WorkflowBlockItem
Opcionalmente, también puede añadir una descripción.
:::

:::WorkflowBlockItem
Utilice los campos Configuraciones administradas para configurar los comportamientos de las configuraciones administradas:
:::

:::WorkflowBlockItem
| **Ajuste**                                                            | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| --------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bloqueo de la aplicación para que no comparta widgets en los perfiles | Permite impedir que las aplicaciones compartan widgets en los perfiles solo si la aplicación no se ha instalado de forma silenciosa. Deje desactivada esta opción para permitir que las aplicaciones de confianza instaladas en el perfil de Android Enterprise muestren widgets en la pantalla de inicio, para que los usuarios puedan acceder a la información sin tener que iniciar sesión.                                                                                                                                                                                                                              |
| Bloqueo del usuario para que no pueda desinstalar la aplicación       | Habilite esta opción para evitar que el usuario desinstale la aplicación luego de que Ivanti Neurons for MDM ha instalado la aplicación de forma silenciosa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Código de la versión mínima                                           | Establezca un código de versión mínima necesaria para que la aplicación anule el comportamiento de actualización predeterminado. Si el código de la versión de la aplicación instalada actualmente en el dispositivo es anterior al código de la versión mínima especificada, la aplicación se actualiza inmediatamente a la última versión.                                                                                                                                                                                                                                                                                |
| Lanzamiento automático al instalarlo                                  | Seleccione esta opción si desea iniciar una aplicación automáticamente después de su instalación. Esta funcionalidad solo está disponible si la aplicación está recién instalada en el dispositivo y no para una actualización de versión. En el caso del Perfil de trabajo y del Perfil de trabajo en los dispositivos propiedad de la empresa, la aplicación Go debe estar activa y en primer plano.Debido a las limitaciones de Android 10+, solo se lanzará una aplicación si el usuario pulsa varias aplicaciones en el caso del Perfil de trabajo y el Perfil de trabajo en los dispositivos propiedad de la empresa. |

### Configuración de dominios administrados

El administrador puede controlar los campos de configuración de la aplicación que se pueden enviar a los dispositivos o que no se deben enviar. En general, los valores predeterminados se establecen cuando se envían las configuraciones a distintos dispositivos. En la sección Configuraciones administradas, del ajuste **Forzar en el dispositivo**, seleccione **Forzar todos los ajustes** o **Forzar solo los ajustes con valores definidos**.

Cada configuración administrada para Android Enterprise muestra un botón que habilita los certificados para cada campo de texto. Al pulsarlo, se reemplaza dicho campo por una lista desplegable de certificados. Cuando esta opción está configurada, los certificados se aplican de forma silenciosa sin interacción alguna por parte del usuario.Un campo habilitado para certificado existente puede cambiarse a habilitado para texto, haciendo clic en el mismo botón junto al campo. Un campo habilitado para texto cambiado a campo habilitado para certificado puede volver a cambiarse a campo habilitado para texto, haciendo clic en el mismo botón. (Los campos desplegables predeterminados no pueden revertirse a campos habilitados para texto).

Si no hay certificados de Id. configurados en el dispositivo abonado, cuando se cambia de texto a desplegable con el botón de habilitar certificados, la única opción que se mostrará en la lista desplegable será «Ninguno».

Haga clic en **Administrar permisos** para seleccionar y configurar los permisos del tiempo de ejecución para las aplicaciones creadas con API 23+ o posterior y Android 6.0+.Solo se incluyen para seleccionar los permisos peligrosos aplicables a la aplicación específica. La lista completa de los permisos peligrosos (como leer sus contactos, encontrar cuentas en el dispositivo, escribir registros de llamadas, etc.) están enumerados en [**https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups.**](https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups)
:::

:::WorkflowBlockItem
- Los permisos se aplican solamente cuando la aplicación los solicita.
- Los permisos no se aplican si los usuarios los han aceptado o denegado previamente.
  Algunos de los derechos que puede asignar a cada permiso son los siguientes:
- Concesión automática
- Denegación automática. Utilice este ajuste con precaución
- Predeterminado/global
  Configure las opciones de distribución seleccionando entre **A todas las personas con la aplicación**, **A nadie** o **Personalizado**.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::
::::

### Nuevos ajustes de configuración

Cuando se actualiza la versión de una aplicación y si hay algún cambio en las configuraciones existentes, aparece el botón **Actualizar a las funciones más recientes** después de editar la página Detalles de configuración.

1. Haga clic en **Actualizar a las funciones más recientes**.Aparece un mensaje de advertencia en la pantalla que indica que pasar a las funciones más recientes impedirá que los usuarios accedan a las versiones anteriores de la aplicación. El mensaje de advertencia recomienda pasos para integrar la última versión de la aplicación sin problemas.
2. Haga clic en **Siguiente**.
3. Aparece en pantalla la ventana **Ajustes de nuevas configuraciones**.
4. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/O2G-ej0nANAeWEfhWrW_Y_newconfigurationsettings.png" alt caption}
   La ventana **Ajustes de la nueva configuración** enumera distintos ajustes que existían con la configuración, y el estado de cada ajuste después de la actualización. La ventana Nueva configuración enumera todas las restricciones de la base de datos y el esquema de Google enumerará el siguiente estado:
   •Agregado
   •Eliminado
   •Modificado
   Seleccione la casilla de verificación y haga clic en **Aceptar** para continuar con la actualización.
   Aparece un mensaje de confirmación en la pantalla de que la configuración se ha actualizado correctamente con las últimas funciones. Ahora puede distribuir y guardar las configuraciones para que los cambios surtan efecto.

## Restricciones y permisos de aplicaciones para aplicaciones internas

El administrador puede establecer algunas restricciones de aplicaciones y restringir o dar permisos para aplicaciones internas. Esta función solo estaba disponible para aplicaciones públicas. Pero esta función se ha ampliado ahora a las aplicaciones internas.

El administrador debe volver a cargar las aplicaciones internas para que las funciones de **Restricción de aplicaciones** y **Permisos** estén disponibles en sus aplicaciones. Se recomienda eliminar la aplicación existente antes de cargar una nueva versión.

**Procedimiento**

1. Vaya a **Aplicaciones** > **Catálogo de aplicaciones**.
2. Seleccione una aplicación **Interna** de la lista.
3. Haga clic en **Configuraciones de aplicaciones**.
4. Haga clic en **Configuraciones administradas para Android**.
5. Haga clic en **Añadir**.
6. Aparece en pantalla la sección **Restricciones de la aplicación**.
   Introduzca los valores necesarios para las restricciones disponibles.
7. Seleccione **Administrar permisos**.
8. La ventana **Permisos seleccionados** aparecen en la pantalla.
   Seleccione los permisos necesarios de la lista y haga clic en **Seleccionar**.
9. En la sección **Permisos de tiempo de ejecución**, ajuste los valores de los permisos seleccionados.
10. En la sección **Distribuir la configuración de esta aplicación**, elija una de las opciones siguientes **Distribución de aplicaciones**:\* **A todas las personas con la aplicación**
    - **A nadie**
    - **Personalizado**
11. Haga clic en **Guardar**.
    Las restricciones y permisos seleccionados se aplicarán en las aplicaciones internas.

## Configuración de Gmail con Android Enterprise

Puede implementar Gmail en dispositivos con Android Enterprise si ha configurado Ivanti Neurons for MDM para Android Enterprise. Para configurar Gmail con Android Enterprise

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione la aplicación de Gmail para la que realizar la configuración de Android Enterprise. Aparece la sección Establecimiento de la configuración.
3. Introduzca un nombre para la configuración.
4. Opcionalmente, también puede añadir una descripción.
5. Utilice los campos **Configuraciones administradas** para configurar los comportamientos de las configuraciones administradas:

Las opciones **Ampliar todo** y **Contraer todo** están solo disponibles para restricciones anidadas o de jerarquía.

| Ajuste                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Enviar al dispositivo**                       | Enviar todos los ajustes: seleccione esta opción para habilitar todas la alternancias, incluidas aquellas sin valoresEnviar solo los ajustes con valores definidos: seleccione esta opción para habilitar todas la alternancias con los valores definidos y deshabilite las alternancias para ajustes sin valoresEn muchos casos, los ajustes predeterminados ya están disponibles. No obstante, el administrador puede seleccionar los ajustes de configuración de las aplicaciones requeridas o editar las variables que se deben enviar a los dispositivos. |
| **Dirección de correo electrónico**             | Ingrese variables de sustitución para definir la dirección de correo electrónico. Normalmente se suele introducir $emailaddress$. Los UEM pueden usar este campo para sacar las credenciales de usuario del Active Directory.                                                                                                                                                                                                                                                                                                                                  |
| **Nombre del host o host**                      | Introduzca el nombre de host del servidor Active Sync, como hostname.company.com:443/path.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Nombre de usuario**                           | Utilice la variable para el nombre de usuario de Active Directory del usuario que se puede especificar como un nombre de usuario directo (janedoe) o un valor de plantilla ($username$).                                                                                                                                                                                                                                                                                                                                                                       |
| **Tipos de autenticación**                      | Seleccione la lista de strings que contienen los tipos de autenticación permitidos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **SSL obligatorio**                             | Cuando se selecciona, permite y requiere SSL en números de puerto utilizados con nombre de host.                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Confiar en todos los certificados**           | Seleccione esta opción solamente si desea que la aplicación acepte automáticamente certificados que no sean de confianza. Utilice esta opción solo para la depuración o el desarrollo cuando trabaje en un entorno de pruebas.                                                                                                                                                                                                                                                                                                                                 |
| **Alias del certificado de inicio de sesión**   | Ingrese el alias para el certificado de inicio de sesión utilizado para los servidores ActiveSync.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Permitir cuentas no administradas**           | Seleccione esta opción para permitir a los usuarios añadir o eliminar cualquier cuenta de Exchange que no sea la cuenta especificada en esta configuración administrada.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Firma predeterminada del correo electrónico** | Ingrese la secuencia que conforma la firma de correo electrónico predeterminada que se agregará al final del texto de todos los mensajes de correo electrónico salientes.                                                                                                                                                                                                                                                                                                                                                                                      |
| **Ventana de sincronización predeterminad**     | Ingrese el valor de 0 a 5 que representa el período para la sincronización con EAS (Sincronización activa de Exchange).                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Haga clic en **Siguiente**.                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

7. Configure las opciones de distribución seleccionando entre **A todas las personas con la aplicación**, **A nadie** o **Personalizado**.
8. Haga clic en **Guardar**.
