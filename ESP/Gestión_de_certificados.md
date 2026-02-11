---
title: Gestión de certificados
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

## Licencia: Silver

Usar la autenticación de certificados es una forma efectiva de asegurar sus dispositivos móviles. Los certificados son más seguros que las contraseñas y, además, le permiten utilizar una sola credencial para proteger las VPN, redes inalámbricas, correo electrónico, etc. Si su organización tiene acceso a una entidad de certificación externa, puede utilizar un Conector para acceder a ella. Si su organización no tiene acceso a una entidad de certificación, puede utilizar Ivanti Neurons for MDM como entidad de certificación. También puede utilizarla como entidad de certificación intermediaria para otras entidades de certificación. Los certificados generados por Ivanti Neurons for MDM se denominan certificados de autofirmados.

- Los certificados SHA1 se dejan de utilizar mientras se crean los certificados de identidad. Puede elegir otros algoritmos. Si los certificados anteriores usaban SHA-1, puede usarse el mismo algoritmo SHA-1 mientras se actualizan los certificados. Si los certificados anteriores usaban un algoritmo posterior a SHA-1, no está permitido cambiar a SHA-1.
- Durante la configuración de la entidad de certificación local o externa, seleccione la opción **Identidades del caché en&#x20;**&#x49;vanti Neurons for MDM para almacenar los certificados con el servicio de Ivanti Neurons for MDM. Borre el caché para generar los certificados, según sea necesario.
- Los certificados se reemitirán implícitamente.
- Para lograr un sistema más eficiente, los certificados de las configuraciones creadas por un administrador se generan sin conexión, usando una cola FIFO. Durante el período en que las configuraciones se están generando sin conexión, el estado de la configuración será **Generación de certificados pendiente** en la columna **Estado**, en la pestaña **Configuraciones** de la págin&#x61;**&#x20;Detalles del dispositivo**. Tras generar los certificados, las configuraciones se cambian al estado **Instalación pendiente** y se insertan, junto con los certificados, en los dispositivos a través de ingresos forzados automáticos.
- Todos los certificados de la Entidad de certificación, incluido el certificado firmado por las Entidades de Certificación externas DigiCert PKI Platform o GlobalSign, se revocan cuando se retira o borra un dispositivo y cuando los certificados se regeneran.

Como administrador, puede generar certificados Ivanti Neurons for MDM para un inicio de sesión con tarjeta inteligente y para Id. de objetos del cliente (OID). Puede generar certificados para las siguientes opciones de autenticación:

•Autenticación de cliente - habilitada de modo predeterminado.

•IPSEC - opcional, el administrador puede habilitarlo.

•Inicio de sesión con tarjeta inteligente - opcional, el administrador puede habilitarlo.

•OID personalizados - opcional, el administrador puede habilitarlos.

Esta función sólo es aplicable a las siguientes autoridades de certificación:

• Entidad de Certificación local

•Entidad de certificación intermedia

•Entidad de certificación externa: configure las políticas de aplicación de la plantilla de CA en el servidor NDES para que admita IPSEC, Inicio de sesión con tarjeta inteligente y OID personalizados.

En los modos Administración de dispositivos, Estación de aplicaciones u otros modos de empresa que no sean Android, la gestión de certificados no es compatible con los dispositivos Samsung que utilizan las API de Samsung. Se recomienda verificar la transición a Android Keystore basándose en la recomendación de Samsung.

Para obtener más información, consulte [**Configuración del certificado**](./Configuración_del_certificado.md).

## Conectarse a una autoridad de certificación distinta a SCEP local.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Instale y configure un Conector (**Administrador > Conector**). Para obtener más información, consulte [**Conector**](./Conector.md).
:::

:::WorkflowBlockItem
Vaya a **Administración** > **Infraestructura** > **Administración de certificados**.
:::

:::WorkflowBlockItem
Haga clic en **Agregar** en la sección **Entidad de certificación**.
:::

:::WorkflowBlockItem
Seleccione **Agregar una autoridad de certificación de SCEP local** y haga clic en **Continuar:**
:::

:::WorkflowBlockItem
Introduzca un nombre que identifique la configuración.
:::

:::WorkflowBlockItem
Seleccione uno de los siguientes tipos de Entidad de Certificación:
:::

:::WorkflowBlockItem
- Microsoft
- EJBCA
- Servidor SCEP genéricoLa opción del servidor SCEP genérico puede usarse con la mayoría de los servidores SCEP que tengan una contraseña estática de comprobación.
  Complete el formulario que aparece.
:::

:::WorkflowBlockItem
Haga clic en **Hecho**.
:::
::::

## Crear una entidad de certificación externa

Elija esta opción si desea emplear una Entidad de Certificación de terceros.

**Procedimiento**

1. En la página **Administración de certificados**, haga clic en **Añadir** en la sección **Entidad de Certificación**.
2. En la página Añadir entidad de certificación, en Crear una Entidad de Certificación externa, haga clic en **Continuar**.
3. Seleccione la plataforma GlobalSign o DigiCert PKI como entidad de certificación externa.
4. Complete los campos restantes del formulario que aparece.
5. Haga clic en **Hecho**.

### Ver un certificado de la entidad de certificación externa

Puede ver los detalles de un certificado y cargar el certificado raíz intermedio/alternativo para que esta entidad de certificación sustituya la copia almacenada existente.

**Procedimiento**

1. En **Entidad de Certificación** en la página **Administración de certificados**, haga clic en **Acciones** junto a la entidad de certificación externa y, a continuación, haga clic en **Ver certificado**. Aparecerá la ventana **Ver certificado**.
2. En la ventana **Ver certificado**, haga clic en **Cargar certificado**. Aparecerá la ventana **Cargar certificado: EC externa**.
3. Haga clic en **Elegir archivo** para seleccionar el certificado que se va a cargar.
4. Haga clic en **Hecho**.

## Crear una Entidad de Certificación intermedia

- Si necesita un certificado, genere una CSR y envíesela a la entidad firmante. Una vez que reciba el certificado de la entidad firmante, cárguelo.
- Si ya tiene el certificado necesario, cárguelo.

### Generar una CSR (solicitud de firma del certificado)

**Procedimiento**

1. En la sección **Entidad de Certificación** que hay en la página **Administración de certificados**, haga clic en **Añadir**.
2. En la sección Añadir entidad de certificación, en Crear una Entidad de Certificación intermedia, haga clic en **Generar CRS**.
3. Complete el formulario que aparece.
4. Haga clic en **Generar**.
5. Copie el contenido que hay entre COMENZAR SOLICITUD DE CERTIFICADO y FINALIZAR SOLICITUD DE CERTIFICADO en un archivo de texto.
6. Cargue el archivo de texto a la entidad de certificación.
7. Haga clic en **Hecho**.

### Cargar el certificado firmado

Una vez que reciba el certificado firmado de la entidad de certificación, puede cargarlo.

**Procedimiento**

1. En la sección **Entidad de Certificación** de la página **Administración de certificados**, encuentre la entrada de la CSR que ha generado.
2. En esa sección, seleccione **Acciones > Cargar nuevo certificado firmado**.
3. Haga clic en **Elegir archivo**.
4. Seleccione el nuevo certificado firmado.
5. Haga clic en **Hecho**.

### Cargar un certificado existente

Este tema describe cómo cargar un certificado firmado.

**Procedimiento**

1. En la sección **Entidad de Certificación** que hay en la página **Administración de certificados**, haga clic en **Añadir**.
2. En la sección Añadir entidad de certificación, en Crear una Entidad de Certificación intermedia, haga clic en **Cargar identidad existente**.
3. En el campo **Nombre**, introduzca un nombre para este certificado que sea diferente a los demás.
4. Haga clic en **Cargar**.
5. Seleccione el certificado.
6. Introduzca la contraseña para el certificado.
7. Haga clic en **Cargar**.

### Ver un certificado de la entidad de certificación intermedia

Puede ver los detalles de un certificado y obtener la URL de la CRL (lista de revocación de certificados) de la entidad de certificación.

**Procedimiento**

1. En la sección **Entidad de Certificación**, haga clic en **Acciones** junto a la entidad de certificación y, a continuación, haga clic en **Ver certificado**. Aparecerá la ventana **Ver certificado**.
2. En la ventana **Ver certificado**, puede ver la URL en el campo **URL de CRL**.
3. Haga clic en **Copiar** para copiar esa URL en un portapapeles y pegarla en otra aplicación. Esta URL se puede usar para configurar Office 365 de modo que acepte certificados emitidos por la entidad de certificación.

## Crear una Entidad de Certificación independiente

Elija esta opción si quiere crear una Entidad de certificación nueva y completamente independiente (local y autofirmada).

**Procedimiento**

1. En la sección **Entidad de Certificación** que hay en la página **Administración de certificados**, haga clic en **Añadir**.
2. En la página Añadir Entidad de Certificación, en Crear una Entidad de Certificación independiente, haga clic en **Continuar**.
3. Complete el formulario que aparece.
4. Haga clic en **Generar**.

### Configure el período de caducidad de la entidad de certificación independiente.

Puede configurar el período de caducidad de la entidad de certificación (local) independiente. De forma predeterminada, la vida útil del certificado es de 30 años.

**Procedimiento**

1. En la sección **Entidad de Certificación** en la página **Administración de certificados**, haga clic en **Acciones** junto a la entidad de certificación independiente.
2. Haga clic en **Editar**.Aparecerá la ventana **Editar entidad de certificación**.
3. En la sección Plantilla de certificado de cliente, en el campo **Vida útil del certificado**, introduzca el nuevo período de caducidad en días.
4. Haga clic en **Guardar**.

Puede recibir notificaciones y correos electrónicos (si está habilitado opcionalmente) cuando los certificados emitidos por una autoridad de certificación local estén a punto de caducar o ya hayan caducado.

- Notificación en los días de caducidad del certificado: las notificaciones se generan a intervalos predeterminados durante un margen de caducidad del certificado. La primera notificación se produce 365 días antes de la caducidad, seguida de notificaciones adicionales que ocurren 180 días, 60 días, 45 días y 7 días antes de la caducidad. Recibirá esta notificación hasta que reemplace el certificado yendo a **Administrador > Administración de certificados > Acciones > Cargar nuevo certificado firmado**.
- Notificación en el certificado caducado - Usted recibe una notificación cuando el certificado caduca. Tendrá que reemplazar el certificado para reanudar el servicio normal.
- Notificación cuando se carga un nuevo certificado válido: la notificación se enviará cuando se cargue el nuevo certificado firmado.

### Ver un certificado de la entidad de certificación independiente

Puede ver los detalles de un certificado y obtener la URL de la CRL (lista de revocación de certificados) de la entidad de certificación local.

**Procedimiento**

1. En la sección **Entidad de certificación**, en la página **Administración de certificados**, haga clic en **Acciones** junto a la entidad de certificación local y haga clic en **Ver certificado**. Aparecerá la ventana **Ver certificado**.
2. En la ventana **Ver certificado**, puede ver la URL en el campo **URL de CRL**.
3. Haga clic en **Copiar** para copiar esa URL en un portapapeles y pegarla en otra aplicación. Esta URL se puede usar para configurar Office 365 de modo que acepte certificados emitidos por la entidad de certificación local.

## Visualización de la vida útil de una CRL de una entidad de certificación

Puede ver y editar la vida útil de la CRL de una entidad de certificación local o intermedia.

**Procedimiento**

1. En la sección **Entidad de certificación**, en la página **Administración de certificados**, haga clic en **Acciones** junto a la entidad de certificación local y haga clic en **Editar**. Aparecerá la ventana **Editar entidad de certificación**.
2. En la ventana **Editar entidad del certificado**, puede ver el valor de vida de la CRL. El valor predeterminado mínimo es de 24 horas. El valor máximo que se puede introducir es 10 950 horas.
3. Edite el valor del ciclo de vida de la CRL y haga clic en **Guardar**.

## Crear una Entidad de Certificación en la nube

Elija esta opción si desea emplear una Entidad de Certificación en Cloud.

**Procedimiento**

1. Vaya a **Administración** > **Infraestructura** > **Administración de certificados**.
2. En la página **Gestión de certificados**, que hay en la página **Autoridad de certificación**, haga clic en **Agregar**.
3. En la página **Agregar autoridad de certificación**, que hay en **Conectar a una Autoridad de certificación de confianza pública en la nube**, haga clic en **Continuar**.
4. Introduzca un nombre en la casilla **Nombre**.
5. Seleccione la Autoridad de certificación en la nube de las siguientes opciones:\* **Atos IDnomic CMS**
   - **Plataforma DigiCert One PKI**
   - **Plataforma DigiCert PKI**
   - **Confiar**
   - **GlobalSign**
6. Introduzca la URL básica y cargue los datos del certificado.
7. Haga clic en **Hecho**.

## Uso de la búsqueda avanzada en los certificados

Puede utilizar la opción de Búsqueda avanzada para buscar certificados emitidos en función de reglas para identificar y ver los certificados con criterios específicos. Estas reglas se pueden crear usando los operadores correspondientes, como «comienza con», «termina con», «contiene», «no contiene», «no comienza con», «no termina con», «es menor que», «es mayor que», «está en el intervalo», «es igual a» y «no es igual a». Las opciones de reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Los certificados emitidos que coincidan con las reglas se mostrarán debajo de la sección. A partir de Ivanti Neurons for MDM versión 76, los operadores de todas las plantillas de administración de certificados tienen operadores estándar. Los operadores de las siguientes plantillas están estandarizados en esta versión:

- Administrador > Administración de certificados > Certificados emitidos > Búsqueda avanzada

### Búsqueda avanzada en los certificados emitidos

**Procedimiento**

1. En la sección de **Certificados emitidos** de la página **Gestión de certificados**, haga clic en el enlace **Búsqueda avanzada**.
2. Haga clic en **Cualquiera** si los usuarios deben coincidir con al menos una de las reglas o en **Todas** si los certificados deben coincidir con todas las reglas.
3. Cree una regla que defina los criterios de búsqueda para los siguientes atributos:\* **EC**
   - **Nombre de la configuración**
   - **Caducidad**1
   - **Es una clave privada**
   - **SO**
   - **Número de serie**
   - **Estado**
   - **Tipo de uso**
   - **Usuario**
4. (Opcional) Haga clic en + para crear reglas adicionales, si fuera necesario.
5. (Opcional) Haga clic en **Guardar** para guardar la consulta.
6. Haga clic en **Buscar**. En la página se muestran la lista de usuarios que coinciden con los criterios de búsqueda.

### Búsqueda avanzada en los certificados proporcionados por el usuario

**Procedimiento**

1. En la sección **Certificados proporcionados por el usuario** de la página **Administración de certificados**, haga clic en el enlace **Búsqueda avanzada**.
2. Haga clic en **Cualquiera** si los usuarios deben coincidir con al menos una de las reglas o en **Todas** si los certificados deben coincidir con todas las reglas.
3. Cree una regla que defina los criterios de búsqueda para los siguientes atributos:\* **Nombre del certificado**
   - **Fecha de caducidad**
   - **Emitido por**
   - **Cargado el**
4. (Opcional) Haga clic en + para crear reglas adicionales, si fuera necesario.
5. (Opcional) Haga clic en **Guardar** para guardar la consulta.
6. Haga clic en **Buscar**. En la página se muestran la lista de usuarios que coinciden con los criterios de búsqueda.

## Cargando las consultas de búsqueda de los certificados emitidos

Para ver la lista de consultas de búsqueda guardadas.

**Procedimiento**

1. En la sección de **Certificados emitidos** de la página **Gestión de certificados**, haga clic en el enlace **Búsqueda avanzada**.
2. Haga clic en el icono «Carpeta». Aparecerá la ventana **Búsqueda avanzada**. La lista de las consultas de búsqueda creadas se muestra en la sección **Cargar consulta**. En esta sección se muestran los siguientes detalles:\* **Nombre de la consulta**: el nombre de la consulta cargada.
   - **Contenido de la consulta** muestra el contenido de las reglas que definen la consulta de búsqueda.
   - **Acciones**: seleccione la acción que se realizará en la consulta.
3. Haga clic en **Cargar consulta** en la columna **Acciones** para ver la lista de certificados emitidos que coinciden con los criterios definidos en la consulta cargada.Para borrar una consulta cargada, haga clic en el icono «Borrar».

Haga clic en **Exportar a CSV** para descargar el contenido del informe de los resultados de búsqueda en un archivo CSV para consultarlo o analizarlo posteriormente.

### Ver el período de vencimiento de los certificados emitidos

En la sección **Certificados emitidos**, en la columna **Caduca (en días)** se pueden ver los días que faltan para que venza el certificado si la caducidad se produce dentro de los próximos 30 días. Si el certificado ya había caducado en los últimos 30 días, en la columna **Caduca (en días)** para el certificado se mostrará el número de días que han transcurrido desde la fecha de caducidad.

Para obtener más información, consulte [**Configuración de SCEP para entidades de certificación externas**](./Configuración_de_SCEP_para_Entidades_de_Certificación_externas.md).

## Exportar a CSV

Puede exportar los certificados a un archivo CSV para consultar más adelante o para realizar análisis.

Procedimiento

1. En la página **Administración de certificados**, vaya a una de las pestañas siguientes.\* **Autoridad de certificados**
   - **Certificados emitidos**
   - **Certificados proporcionados por el usuario**
2. Haga clic en **Exportar a CSV**.
3. Haga clic en **Descargar**.
4. (Opcional) Haga clic en **Eliminar&#x20;**&#x70;ara eliminar el informe.
