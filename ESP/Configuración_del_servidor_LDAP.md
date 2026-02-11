---
title: Configuración del servidor LDAP
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

## Licencia: Silver

Configurar un servidor LDAP y un Conector le permite importar usuarios y grupos desde su directorio corporativo. Una vez que haya instalado al menos un Conector, puede añadir uno o más servidores LDAP.

Añadir servidores LDAP significa configurar:

- la *conexión* al servidor LDAP
- los *términos de búsqueda* necesarios para ver los datos del directorio de destino
- la parte del directorio que desea *importar*
- si desea *invitar a los usuarios* automáticamente en la parte del directorio seleccionada

Una vez que haya añadido un servidor LDAP, puede regresar a esta página para [**editar la información del servidor LDAP**](./Configuración_del_servidor_LDAP.md) o [**cambiar los usuarios LDAP seleccionados**](./Configuración_del_servidor_LDAP.md).

los usuarios LDAP se deben importar después de configurar un usuario LDAP. Consulte [**Importar usuarios LDAP**](./Configuración_del_servidor_LDAP.md).Los nombres de usuario de LDAP, al igual que los nombres de usuario locales, deben ser exclusivos internacionalmente. Le rogamos que verifique que los usuarios no tengan ya una cuenta local con el mismo nombre de usuario o, en el caso de organizaciones con más de un abonado, que el nombre de usuario no haya sido ya asociado con otro abonado.

## Añadir un servidor LDAP

Procedimiento

::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en **+Añadir servidor**.
:::

:::WorkflowBlockItem
Proporcione la siguiente información:
:::

:::WorkflowBlockItem
| **Ajuste**         | Qué hacer                                                                                                                                                                           |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre             | Introduzca un nombre que identifique este servidor.                                                                                                                                 |
| Descripción        | Introduzca una descripción que explique el objetivo de este servidor.                                                                                                               |
| URL del directorio | Introduzca la dirección URL para el directorio. Utilice uno de los siguientes formatos\:ldap\://dirección IP oldaps\://dirección IP oEjemplo: ldap\://miservidor1.miempresa.com:389 |
| Id. de Usuario     | Introduzca la Id. de usuario para una cuenta que tenga las siguientes características:\* que esté administrada por un servidor LDAP                                                 |

- que se pueda enlazar con el servidor LDAP y buscar los subárboles para el usuario, el grupo y la unidad organizativaEsta es, por lo general, una cuenta con Credenciales de administrador de directorio (DN o nombre distintivo y contraseña). |
  \| Contraseña           | Introduzca la contraseña para la cuenta.                                                                                                                                                                                                                                                                                                                                            |
  \| Confirmar contraseña | Vuelva a introducir la contraseña para la cuenta.                                                                                                                                                                                                                                                                                                                                   |
  \| Tipo de directorio   | Seleccione el tipo de directorio de la lista de directorios compatibles.\* Microsoft Active Directory
- Abrir LDAP
- Otro (compatible con OpenLDAP)                                                                                                                                                                                                                                  |
  Haga clic en **Probar conexión y continuar.**
:::

:::WorkflowBlockItem
Este paso valida la información que ha proporcionado hasta el momento.

- Si se comprueba que la información es válida, el servicio recupera el contexto de nomenclatura LDAP, que será utilizado para rellenar algunos de los campos de la página siguiente.
- Si la URL de LDAP no se puede conectar, puede continuar con los siguientes pasos. No obstante, pero esto podría provocar una funcionalidad limitada hasta que la conexión se haya solucionado.
  Complete el resto de ajustes:
:::

:::WorkflowBlockItem
| Ajuste                                                                         | Qué hacer                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| URL de conmutación por error del directorio                                    | Introduzca la dirección URL para el directorio secundario. Utilice el siguiente formato\:ldap\://dirección IP oEjemplo: ldap\://miservidor2.miempresa.com:389                                                                                                                                                                                                                                                                                                                                                                 |
| Intervalo de sincronización                                                    | Introduzca el período de tiempo que debe pasar entre cada intento de sincronización de los datos LDAP desde el servidor LDAP. El valor predeterminado es de 15 minutos. Considere aumentar el intervalo una vez que haya sincronizado correctamente todos los datos del LDAP de destino y confirmado que su configuración LDAP cumple con sus necesidades.                                                                                                                                                                    |
| [**Habilitar Descartar sincronización**](./Configuración_del_servidor_LDAP.md) | Seleccione esta opción para descartar la sincronización de datos LDAP automáticamente si el conjunto de datos cargados disminuye significativamente. Esta opción garantiza que el comportamiento anormal en la parte del sistema de LDAP no dará lugar a molestas actualizaciones innecesarias en el servicio ni a la eliminación de configuraciones desde los dispositivos registrados. Asegúrese de que esta opción no está seleccionada si tiene previstos grandes cambios en su configuración LDAP o en el servidor LDAP. |
| Activar este servidor LDAP                                                     | Seleccione esta opción para utilizar este servidor LDAP con su servicio. Desactive este ajuste si desea retirar este servidor LDAP o ponerlo fuera de servicio. Aunque haya configurado una conmutación para casos de error a un segundo servidor LDAP que sustituiría automáticamente este servidor, utilizar esta opción le permite planificar el futuro y evitar una breve falta de conectividad durante la conmutación por error.                                                                                         |
| Se invitará automáticamente a todos los usuarios cuando se importen.           | Seleccione esta opción para enviar invitaciones automáticamente a los usuarios una vez que se hayan importado del servidor LDAP.                                                                                                                                                                                                                                                                                                                                                                                              |
| Actualizar certificado de EC                                                   | Haga clic en **Seleccionar archivo** para cargar el certificado TLS emitido por la EC instalada en este servidor LDAP. Puede subir varios certificados de EC.                                                                                                                                                                                                                                                                                                                                                                 |
| Obtener referencias                                                            | Se aplica solo si está utilizando un dominio de múltiples bosques. Esta opción indica si quiere utilizar controladores de dominio adicionales cuando el controlador del dominio de destino no disponga de una copia del objeto solicitado.\* Seleccione **Continuar** si quiere utilizar referencias.                                                                                                                                                                                                                         |

- Seleccione **Ignorar** si no quiere utilizar controladores de dominio alternativos.
- **Iniciar** tiene el mismo efecto actualmente que **Ignorar**.Seleccionar **Continuar** retrasa la autenticación LDAP.                                                                                                                                                                                                                                                                  |
  \| Tiempo de espera de la búsqueda de resultados                                   | Aumente el tiempo de espera si observa problemas de rendimiento o resultados incompletos cuando realiza búsquedas en los datos sincronizados desde el servidor LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| Contador de la búsqueda de resultados                                           | Configure el número máximo de registros que debe devolver el servidor LDAP al mismo tiempo. Las situaciones que pueden requerir cambiar este ajuste para mejorar el rendimiento incluyen:\* El servidor LDAP está situado lejos o está detrás de un enlace de latencia alta. En este caso, los resultados de las búsquedas grandes tardarán más en ser recuperados que los de las búsquedas pequeñas, por lo que la definir un conjunto más pequeño le permite ver los subconjuntos de datos actualizados con mayor rapidez.
- El LDAP es muy grande y cada búsqueda le devuelve un volumen de resultados enorme. En este caso, si el rendimiento no constituye un problema, definir conjuntos de resultados más grandes haría posible encontrar todos los datos con menos búsquedas. |
  Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Utilice las siguientes directrices para configurar la integración con el servidor LDAP:
:::

:::WorkflowBlockItem
| **Ajuste**                   | Qué hacer                                                                                                                                                                                                                    |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Formato de miembro del grupo | Seleccione **DN** o **UID** para indicar si quiere utilizar en su búsqueda un nombre distintivo o la Id. del usuario.                                                                                                        |
| *Atributos de búsqueda OU*   | Especifique los criterios para la búsqueda en el nivel de unidad organizativa.                                                                                                                                               |
| DN base                      | Introduzca el nombre distintivo para comenzar un nivel en el que quiere que su búsqueda comience o tenga la raíz. Su selección determinará los valores predeterminados para otros campos, que puede cambiar si es necesario. |
| GUID de objeto               | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP. Este atributo identifica de forma única una unidad organizativa a través del tiempo y a través de los cambios de nombre de OU.        |
| Nombre del atributo          | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                       |
| Descripción                  | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                       |
| DN de atributo               | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                       |
| Filtro de búsqueda           | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                       |
| Ámbito de búsqueda           | Seleccione la parte de la jerarquía LDAP que desea como destino:\* **Base** (solo el nivel de entrada en la base de búsqueda)                                                                                                |

- **Nivel uno** (el nivel por debajo de la base de búsqueda)
- **Subárbol** (el subárbol en el árbol de información de directorio bajo el DN base de búsqueda)                                                                                                                                                                                                                                                                                         |
  \| *Atributos de búsqueda de usuarios* | Especifique los criterios para buscar usuarios en un nivel concreto del directorio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| DN base                             | Introduzca el nombre distintivo del nivel en el que quiere comenzar a buscar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
  \| UID de atributo                     | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| GUID de objeto                      | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP. Este atributo identifica de forma única un usuario a través del tiempo y a través de los cambios de nombre del usuario.                                                                                                                                                                                                                                                                                                                                                                      |
  \| DN de atributo                      | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Nombre                              | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Apellidos                           | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Nombre en pantalla                  | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Dirección de correo electrónico     | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Nombre principal                    | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Configuración regional              | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Miembro de                          | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Filtro de búsqueda                  | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Ámbito de búsqueda                  | Seleccione la parte de la jerarquía LDAP que desea como destino:\* **Base** (solo el nivel de entrada en la base de búsqueda)
- **Nivel uno** (el nivel por debajo de la base de búsqueda)
- **Subárbol** (el subárbol en el árbol de información de directorio bajo el DN base de búsqueda)                                                                                                                                                                                                                                                                                         |
  \| Id. de Apple administrada           | Seleccione sincronizar la ID de Apple administrada para los usuarios de LDAP.\* **Ninguna**
- **Patrón**:
  - **Dirección de correo electrónico del usuario**
  - **userUPN**
    Opcionalmente, seleccione la opción **Incluir el subdominio "appleid»** para evitar conflictos con los ID de Apple existentes.                                                                                                                                                                                                                                                                       |
    \| +Añadir atributo personalizado      | (Opcional) Especifique hasta 7 atributos de usuario personalizados que desee aplicar a la administración de dispositivos desde su servicio de directorio. Cada atributo puede estar referenciado por $\{attributeName} en los campos de configuración que admitan variables.**Importante:** el uso de esta opción requiere una implementación uniforme de los atributos personalizados en los servidores LDAP. Si un servidor LDAP incluido en la implementación no usa este atributo, es posible que las características dependientes de este atributo no funcionen como deberían. |
    \| *Atributos de búsqueda de grupos*   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
    \| DN base                             | Introduzca el nombre distintivo del nivel en el que quiere comenzar a buscar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
    \| GUID de objeto                      | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP. Este es el atributo que identifica de forma exclusiva a un usuario a través del tiempo y a través de los cambios de nombre del usuario.                                                                                                                                                                                                                                                                                                                                                      |
    \| DN de atributo                      | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| Nombre del atributo                 | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| Descripción                         | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| Miembro                             | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| Filtro de búsqueda                  | Si es necesario, cambie el valor predeterminado para que coincida con su entorno LDAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| Ámbito de búsqueda                  | Seleccione la parte de la jerarquía LDAP que desea como destino:\* **Base** (solo el nivel de entrada en la base de búsqueda)
- **Nivel uno** (el nivel por debajo de la base de búsqueda)
- **Subárbol** (el subárbol en el árbol de información de directorio bajo el DN base de búsqueda)                                                                                                                                                                                                                                                                                         |
  Haga clic en **Examinar**o en**Buscar**.
:::

:::WorkflowBlockItem
Confirme que su configuración le devuelve los datos esperados.
:::

:::WorkflowBlockItem
Puede realizar esto examinando o buscando un elemento conocido en el directorio.

Haga clic en **Siguiente**.
:::
::::

## Eliminar un atributo personalizado de LDAP

Puede eliminar un atributo personalizado de LDAP y quitar sus valores de los usuarios asociados.

Procedimiento

1. Vaya a **Administrador > Atributos**.
2. En la sección **Atributos personalizados**, haga clic en el enlace **Eliminar** junto al atributo de LDAP que se quiere eliminar. Se mostrará una ventana de confirmación.
3. Haga clic en **Eliminar&#x20;**&#x70;ara confirmar la eliminación.El botón **Eliminar** está deshabilitado de manera predeterminada. Deberá seleccionar la casilla de la opción **Entiendo que eliminar un atributo personalizado no puede revertirse** para habilitar el botón **Eliminar**.

## Editar la información del servidor LDAP

Procedimiento

1. Vaya a **Administrador > LDAP.**
2. En la entrada del servidor LDAP, seleccione el icono **Editar** de la columna **Acciones** para ver la página Conectar al servidor LDAP.
3. Realice los cambios necesarios.
4. Haga clic en **Probar conexión y continuar.**&#x53;i la URL de LDAP no se puede conectar, puede continuar con los siguientes pasos. No obstante, pero esto podría provocar una funcionalidad limitada hasta que la conexión se haya solucionado.
5. Haga clic en **Examinar**o en**Buscar**.
6. Confirme que su configuración le devuelve los datos esperados.Puede realizar esto examinando o buscando un elemento conocido en el directorio.
7. Haga clic en **Hecho**.

## Importar usuarios LDAP

Procedimiento

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Usuarios.**
:::

:::WorkflowBlockItem
Haga clic en **+Añadir > Invitar a usuarios de LDAP.**
:::

:::WorkflowBlockItem
Haga clic en **Seleccionar usuarios** en la entrada del servidor LDAP.
:::

:::WorkflowBlockItem
En la página Añadir usuarios de LDAP, introduzca el nombre del usuario, grupo u OU en el campo de búsqueda.
:::

:::WorkflowBlockItem
Para añadir nuevos usuarios o grupos, haga clic en **+Añadir** junto a la entrada que desee añadir.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Elija si desea o no enviar la invitación.
:::

:::WorkflowBlockItem
- No invitar a ningunoPara enviar las invitaciones más tarde, vaya a **Usuarios > Usuarios** y seleccione **Acciones > Enviar invitación** para enviar las invitaciones.
- Invitar a todos
  Haga clic en **Hecho**.
:::
::::

## Actualizar los usuarios, grupos o unidades organizativas seleccionadas

Procedimiento

1. Vaya a **Administrador > LDAP.**
2. En la entrada del servidor LDAP, seleccione el icono **Administrar usuarios** de la columna **Acciones** para ver la página Añadir usuarios de LDAP.
3. Para añadir nuevos usuarios o grupos, introduzca el nombre del usuario o grupo en el campo de búsqueda.
4. Haga clic en **+Añadir** junto a la entrada que desea añadir.
5. Para eliminar a un usuario, grupo u OU, haga clic en el icono de eliminar que hay junto a la entrada que se borrar.
6. Haga clic en **Hecho**.

## Habilitar la notificación Descartar sincronización de LDAP

Habilitar la opción Descartar sincronización de LDAP ayuda a prevenir cortes de electricidad provocados por cambios a gran escala no intencionados en su entorno de LDAP.

Procedimiento

1. Vaya a **Administrador > LDAP.**
2. En la entrada del servidor LDAP, seleccione el icono **Editar** de la columna **Acciones** para ver la página Conectar al servidor LDAP.
3. Marque la casilla **Activar Descartar sincronización**.
4. Introduzca un valor para el porcentaje de datos LDAP que se han vuelto a cargar y provocar así que se descarte la sincronización.
5. Haga clic en **Probar conexión y continuar.**&#x53;i la URL de LDAP no se puede conectar, puede continuar con los siguientes pasos. No obstante, pero esto podría provocar una funcionalidad limitada hasta que la conexión se haya solucionado.
6. Haga clic en **Hecho**.
7. Haga clic en el icono **Sincronizar ahora** en la entrada del servidor LDAP.Cuando el diferencial de cambio que se sincronizará de LDAP a Ivanti Neurons for MDM cae por debajo del porcentaje de descarte establecido, se generará una notificación de ADVERTENCIA. Cuando los cambios se reviertan a un valor inferior al porcentaje establecido, la notificación aparecerá DESACTIVADA.

| Activación                                | Gravedad    | Tipo de notificación    | Tipo de componente | Componente               |
| ----------------------------------------- | ----------- | ----------------------- | ------------------ | ------------------------ |
| Descartar sincronización de LDAP          | Advertencia | Sincronización de datos | LDAP               | Nombre del servidor LDAP |
| Restauración de la sincronización de LDAP | Información | Sincronización de datos | LDAP               | Nombre del servidor LDAP |

La notificación Descartar sincronización parcial se genera cuando uno o más registros del usuario no se sincroniza desde el LDAP. En este caso, se incluye un archivo CSV como archivo adjunto con una lista de usuarios que no se han sincronizado. Si se descartó a algún usuario porque se haya omitido un atributo, también se incluirá una lista de atributos omitidos en el archivo CSV exportado.

## Sincronizar los cambios desde el servidor LDAP

En la página de LDAP, haga clic en el icono **Sincronizar ahora** en la entrada del servidor LDAP.

Si el nombre de la pantalla es de más de 128 caracteres, la sincronización LDAP ignorará dicho usuario y procede con otros usuarios o grupos de usuarios sincronizar.

## Solucionar problemas de conectividad del servidor LDAPS

Si tiene problemas al conectarse al servidor LDAPS (LDAP a través de SSL), es posible que tenga algún problema con el certificado.

Para solucionar el problema:

- Verifique que no está utilizando un certificado de firma automática en el servidor LDAPS.
- Verifique que el certificado LDAPS no haya caducado ni haya sido revocado. Compruebe también que el nombre de host coincida.

Tras verificarlo, espere la sincronización automática de LDAP o sincronícelo manualmente yendo al icono **Administrador > LDAP > Sincronizar ahora&#x20;**&#x64;e la entrada del servidor LDAP.

Si no puede ver la página de LDAP, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Sistema de solo lectura
