---
title: Trabajar con configuraciones
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Filtrar el modo en que se muestran las configuraciones**](./Trabajar_con_configuraciones.md)
- [**Añadir una configuración**](./Trabajar_con_configuraciones.md)
- [**Distribución de la configuración**](./Trabajar_con_configuraciones.md)
- [**Enviar configuraciones a varios dispositivo**](./Trabajar_con_configuraciones.md)
- [**Excluir configuraciones**](./Trabajar_con_configuraciones.md)
- [**Enviar una configuración excluida**](./Trabajar_con_configuraciones.md)
- [**Exportar configuraciones**](./Trabajar_con_configuraciones.md)
- [**Importar configuraciones**](./Trabajar_con_configuraciones.md)
- [**Editar una configuración**](./Trabajar_con_configuraciones.md)
- [**Eliminar configuraciones**](./Trabajar_con_configuraciones.md)
- [**Programar las actualizaciones de las aplicaciones internas**](./Trabajar_con_configuraciones.md)

Las configuraciones son conjuntos de ajustes que usted, como administrador, envía a los dispositivos. Por ejemplo, se pueden utilizar configuraciones para establecer los ajustes VPN y los requisitos del código de acceso en los dispositivos. Las configuraciones existentes en su sistema aparecerán en la página Configuraciones. Puede seleccionar varias configuraciones desde la página de Configuraciones y empujarlas a varios dispositivos a la vez. Estas configuraciones se pueden enviar a los spaces de dispositivos específicos y los dispositivos de otros spaces no se verán afectados. Las configuraciones se pueden enviar a un único espacio, a varios espacios o a todos los espacios a la vez.

Hay muchos [**tipos de configuraciones**](./Tipos_de_configuración.md)disponibles. Se pueden dividir a las siguientes categorías básicas:

- seguridad
- recursos del usuario
- acceso a la red de la empresa
- red móvil
- otras (más configuraciones)

Puede llevar a cabo las siguientes acciones en la mayoría de las configuraciones:

- añadir
- editar
- duplicar
- eliminar
- excluir una o más configuraciones de un dispositivo específico
- insertar una o más configuraciones en un dispositivo específico

Algunas configuraciones tienen acciones restringidas:

- Algunas configuraciones no se pueden añadir ni duplicar. El Bloqueo de activación de iOS es un ejemplo de este tipo de configuración. Por lo tanto, estas configuraciones no estarán entre los mosaicos que aparecen al añadir una configuración. Estas configuraciones aparecerán solo en la página Configuraciones.
- Las configuraciones definidas por el sistema no pueden ser editadas ni borradas. SCEP para inscripción en iOS es un ejemplo de este tipo de configuración.
- Algunas configuraciones se pueden marcar para que no se puedan eliminar o reinstalar en un dispositivo. Estas configuraciones no se pueden excluir ni insertar en el dispositivo.

## Filtrar el modo en que se muestran las configuraciones

Al mostrar la página **Configuraciones**, aparecen enumeradas todas las configuraciones. Para limitar esta lista a ciertas configuraciones, utilice el filtro (panel izquierdo) en SO y Tipo de configuración. Por ejemplo, para limitar la lista y que aparezcan solo las configuraciones de macOS, seleccione **macOS** en la sección **SO**.

Se puede ver la configuración en todos o en varios dispositivos espaciales seleccionando varios espacios de la lista desplegable. Cuando arrastra el cursor sobre las configuraciones que se muestran, aparece una ventana emergente con una lista de los espacios. Puede hacer clic en un espacio para mostrar la página de detalles de la configuración.

Aplicar el filtro **compatible** de **Apple DDM** para identificar con facilidad las configuraciones relacionadas con DDM y mejorar la diferenciación entre tipos de configuración.

Para buscar una configuración existente por su nombre, introduzca el nombre de la configuración en el campo **Buscar**.

Desde la publicación de la versión 81 de Ivanti Neurons for MDM, los administradores globales pueden delegar en los administradores de espacio la edición del Certificado de identidad generado dinámicamente para todos los dispositivos y para la opción de distribución personalizada.

## Añadir una configuración

Esta opción solo se habilita si se selecciona un espacio único en la lista desplegable.

Puede distribuir hasta un máximo de 100 archivos de configuración a la vez.

**Procedimiento**

1. Haga clic en **Añadir**.
2. Seleccione el tipo de configuración que desea crear.
3. Haga clic en **Siguiente**.
4. Si no desea que esta configuración quede inmediatamente habilitada, deseleccione la opción **Habilitar esta configuración**.
5. Seleccione un nivel de distribución para la configuración:\* **Todos los dispositivos**: distribuir la configuración a todos los dispositivos disponibles. Para delegar configuraciones entre espacios, seleccione una de las siguientes opciones:- **No aplicar a los otros espacios**.
   - Para delegar configuraciones en los espacios, seleccione **Resumen de distribución**>**&#x20;Aplicar a todos los dispositivos en los espacios de otros dispositivos**.\* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores del espacio delegados editen la distribución para el espacio específico.
   - **Sin dispositivos** : seleccione esta configuración para la distribución en un momento posterior.
   - **Predeterminada** : se definen conjuntos específicos de grupos de dispositivos a los que se enviará esta configuración. Para delegar configuraciones entre espacios, seleccione una de las siguientes opciones:\* **No aplicar a los otros espacios**.
     - **Resumen de la distribución&#x20;**>**&#x20;Aplicar a los dispositivos de otros espacios**.\* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores delegados del espacio editen la distribución para el espacio específico.

:::Paragraph{indent="2"}
El administrador puede utilizar la opción de distribución Personalizada para distribuir la configuración Personalizada a Dispositivos, Grupos de dispositivos, Usuarios y Grupos de usuarios. La asignación o distribución de configuraciones a Usuarios o Grupos de Usuarios no está disponible para las siguientes configuraciones:
:::

:::Paragraph{listStyleType="disc" indent="3"}
Android Enterprise: perfil de trabajo (Android for Work)
:::

:::Paragraph{listStyleType="disc" indent="3"}
Android Enterprise: dispositivo administrado en el trabajo (Android for Work)
:::

:::Paragraph{listStyleType="disc" indent="3"}
Android Enterprise: dispositivo administrado con perfil de trabajo/perfil de trabajo en dispositivo de la empresa
:::

:::Paragraph{listStyleType="disc" indent="3"}
Dispositivos Android gestionados para el trabajo (propietario del dispositivo) para dispositivos con modo no GMS para el dispositivo administrado en el trabajo (AOSP)
:::

6. Si su servicio tiene espacios definidos, especifique si la configuración debe aplicarse a los demás espacios y la prioridad.
7. Haga clic en **Hecho**.

Para configuraciones que ejecutan un comando para el dispositivo en lugar de instalar un perfil en el dispositivo, los detalles de configuración no mostrarán la configuración como aplicada a ningún dispositivo.

## Distribución de la configuración

Los administradores globales pueden delegar en los administradores de espacio la edición del Certificado de identidad generado dinámicamente para todos los dispositivos y para la opción de distribución personalizada. Para los certificados generados dinámicamente, puede seleccionar opcionalmente la opción **Permitir que esta configuración esté disponible en todos los** espacios. Esta opción hace que los certificados de identidad generados dinámicamente estén disponibles en todos los espacios y puedan utilizarse en Exchange, Wi-Fi, VPN y cualquier otra configuración aplicable, incluidas las configuraciones de aplicaciones gestionadas. Esta opción se puede usar en situaciones en las que solo es necesario distribuir el Certificado de identidad dinámicamente generado a los dispositivos (en espacios no predeterminados) como parte de configuraciones asociadas y no como configuración individual.

Procedimiento

1. Especifique los campos de configuración utilizando la información especificada en la tabla para la configuración individual según corresponda.
2. Haga clic en **Siguiente**.
3. Seleccione la opción **Habilitar esta configuración**.
4. (Opcional) **Permitir que esta configuración esté disponible en todos los espacios**.
5. Seleccione una de las siguientes opciones de distribución:\* **Todos los dispositivos**. Seleccione una de las siguientes opciones:- **No aplicar a los otros espacios**.
   - **Aplicar a todos los dispositivos de otros espacios**.
   - **Aplicar a todos los dispositivos de otros espacios de dispositivos como prioridad más alta**. (Esto solo es puede aplicar a la configuración Wi-Fi).
   - **Aplicar a todos los dispositivos de otros espacios de dispositivos como prioridad más baja**. (Esto solo es puede aplicar a la configuración Wi-Fi).\* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores delegados del espacio editen la distribución para el espacio específico.
   - **Ningún dispositivo** (predeterminada)
   - **Personalizar**Seleccione una de las siguientes opciones:\* **No aplicar a los otros espacios**.
     - **Aplicar a todos los dispositivos de otros espacios**.
     - **Aplicar a todos los dispositivos de otros espacios de dispositivos como prioridad más alta**. (Esto solo es puede aplicar a la configuración Wi-Fi).
     - **Aplicar a todos los dispositivos de otros espacios de dispositivos como prioridad más baja**. (Esto solo es puede aplicar a la configuración Wi-Fi). \* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores delegados del espacio editen la distribución para el espacio específico.Independientemente de los espacios, el certificado de identidad generado dinámicamente puede configurarse en todos los espacios, distribuirse a todos los dispositivos y aplicarse a todos los dispositivos en otros espacios de dispositivos.
6. Haga clic en **Hecho**.

## Enviar configuraciones a un dispositivo

Si desea reinstalar cualquiera de las configuraciones excluidas en un dispositivo, puede insertar las configuraciones.

**Procedimiento**

1. Vaya a **Dispositivos&#x20;**>**Dispositivos**.
2. Haga clic en el nombre del dispositivo para visualizar la página de detalles.
3. Vaya a **Configuraciones**.
4. Seleccione las casillas de verificación para seleccionar las configuraciones específicas que se enviarán al dispositivo.
5. Haga clic en **Insertar perfiles**.
6. Para insertar una sola configuración, haga clic en **Empujar** en la columna **Acciones**.

## Enviar configuraciones a varios dispositivo

Puede seleccionar varias configuraciones desde la página de Configuraciones y empujarlas a varios dispositivos a la vez.

**Procedimiento**

1. Inicie sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a **Configuraciones**.
3. Marque las casillas para seleccionar las configuraciones específicas.
4. Haga clic en **Acciones**, seleccione **Empujar las configuraciones seleccionadas** a los dispositivos. Se abre el asistente de inserción de configuraciones y se muestran todas las configuraciones y sus estados de inserción.
5. Haga clic en **Empujar configuración(es) válida(s)**. Las configuraciones se transfieren a todos los dispositivos de forma masiva. Las configuraciones excluidas para dispositivos específicos en la pestaña **Dispositivos** > **Configuraciones** no se transfieren.

## Excluir configuraciones

Algunas configuraciones previamente distribuidas se pueden eliminar manualmente de un dispositivo excluyéndolas.

**Procedimiento**

1. Vaya a **Dispositivos&#x20;**>**Dispositivos**.
2. Haga clic en el nombre del dispositivo para visualizar la página de detalles.
3. Vaya a **Configuraciones**.
4. Marque las casillas para seleccionar las configuraciones específicas.
5. Haga clic en **Excluir perfiles**.
   Para excluir una sola configuración, haga clic en **Excluir** bajo la columna **Acciones**. Las configuraciones seleccionadas aparecen ahora en la pestaña Configuraciones excluidas.

## Enviar una configuración excluida

**Procedimiento**

1. Vaya a **Dispositivos&#x20;**>**Dispositivos**.
2. Haga clic en el nombre del dispositivo para visualizar la página de detalles.
3. Vaya a **Configuraciones&#x20;**> **excluidas**.
4. Seleccione una o más configuraciones para insertarlas en el dispositivo.
5. Haga clic en **Insertar perfiles**.
6. Para insertar una sola configuración, haga clic en **Empujar** en la columna **Acciones**.

## Exportar configuraciones

Puede exportar los detalles de las configuraciones seleccionadas o todas las configuraciones de los espacios seleccionados a archivos individuales.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Marque las casillas para seleccionar las configuraciones específicas.
3. Haga clic en **Acciones&#x20;**>&#x20;**&#xA0;Exportar todas las configuraciones seleccionadas con detalles**. Si desea exportar todas las configuraciones, seleccione **Exportar todas las configuraciones con detalles**.Se incluye un conjunto de archivos YAML en un archivo .ZIP. El informe incluye detalles de todas las configuraciones existentes en los espacios seleccionados.

### Exportar todas las configuraciones

Exporte sus archivos de configuración para enviarlos al soporte técnico y que puedan utilizarlos como herramienta de ayuda para el diagnóstico. Puede exportar un único archivo de configuración como archivo de formato Yaml o exportar todas sus configuraciones a un archivo .zip. Puede exportar archivos de distintos puntos de la página Configuración, dependiendo de qué configuraciones desee exportar.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Marque las casillas para seleccionar las configuraciones específicas.
3. Haga clic en **Acciones&#x20;**>&#x20;**&#xA0;Exportar todas las configuraciones seleccionadas con detalles**. Si desea exportar todas las configuraciones, seleccione **Exportar todas las configuraciones con detalles**.Se incluye un conjunto de archivos YAML en un archivo .ZIP. El informe incluye detalles de todas las configuraciones existentes en los espacios seleccionados.

### Exportar una configuración personalizada

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Haga clic en **+****Añadir** para seleccionar una configuración.
3. Siga los pasos para personalizar la configuración.
4. Haga clic en **Siguiente**.
5. Elija un nivel de distribución.
6. Haga clic en **Hecho**.
7. Seleccione la configuración que acaba de crear de la lista de la página **Configuración**.
8. Haga clic en el menú desplegable **Acciones** y en **Exportar.******
   **\&#xA;**&#x53;e descargará un archivo con el nombre de la configuración y uno con marca de hora \_aaaammdd.yaml en su dispositivo.&#x20;**&#xA0;**

### Exportar una configuración existente

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Seleccione una configuración existente.
3. Haga clic en el menú desplegable **Acciones** y, a continuación, en **Exportar**.Se descargará un archivo con el nombre de la configuración y uno con marca de hora \_yyyymmdd.yaml en su dispositivo.

## Importar configuraciones

Puede importar un archivo YAML que contiene los detalles de configuración. Para editar una configuración, puede editar los detalles del archivo YAML, seleccione una configuración e importe el archivo y aparecerán los valores de actualización de la configuración. Si se selecciona más de una configuración o espacio, se deshabilita el botón Importar. Si se selecciona un tipo de archivo incorrecto, aparece un mensaje de error. Si selecciona un archivo YAML que contiene información distinta a la requerida para una configuración, aparecerá un mensaje de error.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Seleccione una configuración, haga clic en **Importar**, en **Seleccionar archivo**, seleccione el archivo YAML y haga clic en **Importar**. Se importa el archivo YAML con los detalles de configuración.

## Creación de una configuración mediante un archivo YAML

Puede crear una configuración desde un archivo YAML. Las especificaciones relacionadas con la distribución no forman parte del archivo YAML. La distribución está ajustada por defecto como Ningún dispositivo.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Haga clic en **Importar**, en **Seleccionar archivo**, seleccione el archivo YAML y haga clic en **Importar**. Se importa el archivo YAML con los detalles de configuración. La página de Crear configuración se abre y se muestran todos los detalles que se agregaron al archivo YAML.
3. Seleccione *uno* de los tipos de distribución:\* **Todos los dispositivos**
   - **Ningún dispositivo**
   - **Personalizado**
4. Verifique los detalles de la configuración y seleccione *una* de las siguientes opciones de Resumen de distribución\:El resumen de distribución no está disponible para todas las configuraciones.\* **No aplicar a otros espacios**
   - **Aplicar a los dispositivos de otros espacios**
5. Si el nuevo nombre de la configuración coincide con el nombre de una configuración existente, aparecerá un mensaje de error, haga clic en **Aceptar**, en **Atrás** y cambie el nombre de la configuración.
6. Haga clic en **Siguiente** y, luego, haga clic en **Hecho**.

## Editar una configuración

Puede abrir una configuración y editar directamente los detalles de la misma, o importar un archivo YAML con todos los detalles necesarios. Si se selecciona más de una configuración o espacio, se deshabilita el botón Importar.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Seleccione y abra una configuración, haga clic en el icono editar (lápiz) y edite la configuración.
3. Como alternativa, desde la página de editar configuración, haga clic en el icono **Importar**, seleccione el archivo YAML y haga clic en **Importar**. La página de Editar configuración se abre y se muestran todos los detalles que se agregaron al archivo YAML.
4. Verifique los detalles de la configuración y seleccione una de las siguientes opciones de Resumen de distribución\:El resumen de distribución no está disponible para todas las configuraciones.\* **No aplicar a los otros espacios**.
   - **Aplicar a los dispositivos de otros espacios**
     La distribución está ajustada por defecto como Ningún dispositivo.
5. Haga clic en **Hecho**.

## Eliminar configuraciones

Puede eliminar las configuracionesseleccionadas.

**Procedimiento**

1. Marque las casillas para seleccionar las configuraciones específicas.
2. Seleccione **Acciones&#x20;**>**&#x20;Eliminar**.

## Programar las actualizaciones de las aplicaciones internas

Ivanti Neurons for MDM actualiza automáticamente las aplicaciones internas cuando se registra un dispositivo. Ahora los administradores pueden programar aplicaciones internas basándose en la zona horaria del servidor. La aplicación se actualizará solo cuando el dispositivo se registre dentro de la hora programada. De forma predeterminada, la programación de las actualizaciones de las aplicaciones está desactivada.

Esta configuración se puede aplicar solo para las actualizaciones, no para una nueva instalación. Puede utilizar el comando Enviar instalación/actualización para anular la programación de la actualización automática de las aplicaciones de iOS. Si la actualización automática está activada a nivel de aplicación o de catálogo, tendrá prioridad frente a la Configuración de aplicaciones programada y la aplicación se actualizará inmediatamente después de su conexión.

La configuración se puede aplicar solo a los siguientes tipos de aplicaciones:

- Aplicaciones internas de iOS.
- Aplicaciones internas de Android que sólo están en modo DO.
- aplicaciones de macOS con formato .pkg y .MIP.
- Aplicaciones de Windows.

**Requisitos previos**

Asegúrese de que se cumplen los siguientes requisitos previos para que la configuración funcione como se espera:

- La aplicación debe estar gestionada para iOS y Android. Para macOS, la aplicación puede estar en estado gestionado o no gestionado.
- Asegúrese de que la opción Instalar en el dispositivo en la Configuración de la aplicación está activada.
- El dispositivo debe estar registrado durante la hora programada.

**Procedimiento**

1. Inicie sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a **Configuraciones**.
3. Haga clic en **Añadir**. Se abre la página de Añadir Configuración.
4. Busque la **Aplicación actualización automática**. Se abre la página Crear configuración de actualización automática de aplicaciones.
5. Especifique un nombre en el campo **Nombre**.
6. En la sección **Ajuste de configuración** seleccione la **zona horaria** en la lista desplegable.
7. Seleccione la **Hora de inicio** en la lista desplegable y, a continuación, seleccione la **Duración** en la lista desplegable.
8. Haga clic en **Siguiente**.
9. Seleccione el usuario y el grupo de dispositivos necesarios y, a continuación, haga clic en la casilla **Habilitar esta configuración**.
10. Haga clic en **Hecho**. La configuración se aplica, la aplicación ahora se actualizará sólo en el horario especificado.

Si no puede ver la página de Configuraciones, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración de dispositivos
- Dispositivo de solo lectura

**Temas relacionados:**

- [**Espacios**](./Administrar_espacios.md)
