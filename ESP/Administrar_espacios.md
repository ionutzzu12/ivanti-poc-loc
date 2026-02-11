---
title: Administrar espacios
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Los espacios le permiten designar los grupos de dispositivos que administrarán los diferentes administradores (administración delegada). El administrador de un espacio puede definir las configuraciones y políticas que se aplican a los dispositivos de un espacio. Después de crear los espacios, puede asignar cada uno de ellos al administrador relevante o adecuado. No puede editar o eliminar el espacio predeterminado.

El usuario solo puede ver los espacios asignados y no todos los espacios disponibles. Desde ahora, este ajuste se aplica únicamente a módulos de **Dispositivos**, **Grupos de dispositivos**, **Aplicaciones**, **Inventarios de aplicaciones**, **Contenido**, **Configuraciones**, **Políticas** y **Administración de certificados**. Los espacios seleccionados en la lista de Spaces mientras se visualiza cualquiera de estos módulos se guardan como selección predeterminada preferida del administrador para ese módulo. Estas preferencias no solo se guardan en la sesión de inicio de sesión actual, sino también en las sesiones futuras.

Los espacios que cree heredarán todas las configuraciones del espacio predeterminado. Por lo tanto, cualquier configuración que cree posteriormente en el espacio predeterminado puede aplicarse a los demás espacios. No obstante, los cambios realizados en una configuración existente no se heredan.

Los espacios que cree solamente recibirán copias de las políticas existentes en el espacio predeterminado en ese momento. Cualquier política que cree posteriormente en el espacio predeterminado solo se aplicará a este.

Cree las reglas que definirán qué dispositivos están en el espacio. Estas reglas se pueden filtrar usando los operadores correspondientes, como «comienza con», «termina con», «contiene», «no contiene», «no comienza con», «no termina con», «es menor que», «es mayor que», «está en el intervalo», «es igual a» y «no es igual a». Las reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Se puede revisar la precisión de las reglas utilizando el texto que aparece al final de dichas reglas.

El portal del Administrador de Ivanti Neurons for MDM muestra el número de grupos de usuarios duplicados y el correspondiente número de GUID para identificar los grupos duplicados, cuando se selecciona el atributo Nombre del grupo de usuarios en el generador de reglas. Además, una tabla bajo esta regla muestra la lista de los grupos de usuarios duplicados y sus detalles, como el Nombre del Grupo de Usuarios, el GUID, la Fuente y el nombre distinguido (DN).

Las reglas pueden identificar los dispositivos según:

- Entra ID Inscrito
- Compatible con APNS
- Número alternativo de serie (Solo Android: aplicable a dispositivos Samsung en modo Administrador del dispositivo o Propietario del dispositivo)
- Segmentación de red 5G de Android habilitada
- Android Enterprise: modo no GMS para el dispositivo administrado en el trabajo (AOSP) activado
- Dispositivo Android dedicado
- Compatible con Android Enterprise
- Dispositivo administrado de Android con perfil profesional
- Tipo de certificación SafetyNet de Android
- Android for Work habilitado
- Dispositivos Android administrados en el trabajo (Propietario del dispositivo) habilitados
- Perfil de Android for Work habilitado
- Perfil de trabajo de Android habilitado en dispositivos que son propiedad de la empresa habilitados
- Estado nativo de antiphishing
- Estado de antiphishing
- Estado de la VPN de antiphishing
- Inscrito en la Inscripción de dispositivos automatizada
- Autopilot inscrito
- Código de estado del cliente de Azure
- Hora del informe de cumplimiento del dispositivo Azure
- Estado de cumplimiento del dispositivo Azure
- Identificador del dispositivo Azure
- Sentry bloqueado
- Acceso bloqueado
- Token de Bootstrap disponible
- Tipo de provisión masiva (Apple Configurator, Ninguno o Inscripción de dispositivos automatizada realizada)
- Operador
- Último ingreso del cliente
- Registrado con el cliente
- Cumplimiento
- Medida de cumplimiento bloqueada
- Nombre del país actual (seleccione el nombre del país de la lista desplegable)
- MMC actual
- MNC actual
- Atributo personalizado del dispositivo
- Atributo personalizado de LDAP
- Atributo personalizado del usuario
- Itinerancia de datos
- Origen del dispositivo
- Tipo de dispositivo
- Tipo de dispositivo (Apple)
- Nombre en pantalla
- Cifrado habilitado
- Nombre del país de origen (seleccione el nombre del país de origen de la lista desplegable)
- MCC de origen
- MNC de origen
- IMEI
- IMEI2 (solo en dispositivos Android con doble puerto SIM y aplicable para dispositivos Android 8.0 o superior)
- Dirección IP
- Modo pantalla completa
- Último ingreso
- Modo perdido habilitado
- Solo MAM
- Fabricante
- Estado de activación del MTD
- Modo multiusuario
- SO
- Versión de SO
- SO con versión
- Propiedad
- N.º de teléfono
- En cuarentena
- Bloqueo de recuperación habilitado
- Itinerancia
- Estado de Secure Apps
- Número de serie
- Estado
- Supervisado
- Versión de generación suplementaria
- Suplemento SO/Versión Extra
- Desbloquear token disponible (iOS)
- Inscripción de usuarios inscritos
- Grupo de usuarios
- Nombre de usuario
- Itinerancia de voz
- Clave de recuperación personal de macOS en custodia
- Tipo de clave de recuperación de macOS

Estas reglas están disponibles solo para la licencia **Silver** y superiores.

## Crear un espacio

**Procedimiento**

1. Vaya a **Administrador >&#x20;****Espacios**.
2. Haga clic en **Administrar**.
3. Haga clic en **Crear nuevo espacio**.
4. Haga clic en **Vista previa** para ver qué dispositivos se asignarán al espacio.
5. Haga clic en **Guardar** cuando esté satisfecho con los dispositivos del espacio.Para borrar, haga clic en el icono Eliminar del espacio creado.

## Priorizar espacios

Ivanti Neurons for MDM evalúa los espacios en orden de aparición. Para cambiar el orden, haga clic en las flechas que hay en la esquina superior derecha de la definición del espacio.

::Image[]{src="partitionarrows.png" signedSrc="partitionarrows.png" size="10" caption alt isUploading="false" sha initialPath="partitionarrows.png" githubPath="partitionarrows.png" position="flex-start"}

## Asignar un administrador a un espacio

**Procedimiento**

1. Vaya a **Usuarios.**
2. Busque el usuario que va a ser el administrador.
3. Haga clic en el vínculo del usuario para mostrar los detalles.
4. Seleccione **Acciones > Asignar funciones**.
5. Seleccione **Administración de dispositivos**.
6. En **Administración de dispositivos**, seleccione el espacio para este administrador.
7. Haga clic en **Hecho**.

Cuando este administrador inicie sesión, solo serán visibles los dispositivos, configuraciones y políticas del espacio asignado.

## Duplicar una configuración o política

Dentro de un espacio, se puede duplicar una configuración o política si necesita duplicarlas con algunas diferencias. También puede asociar las configuraciones o políticas duplicadas a diferentes grupos de dispositivos. Se pueden duplicar todas las políticas dentro de un espacio. También se pueden duplicar todas las configuraciones dentro de un espacio, excepto el Certificado de identidad provisto por el usuario y Threat Defense. Las siguientes configuraciones también pueden duplicarse en los distintos espacios desde el espacio predeterminado:

- Restricciones de iOS
- Clip web
- Certificado
- Código de acceso
- SCEP (iOS y Windows)
- Certificado de identidad (generado dinámicamente)
- el nombre de una configuración o tipo de política debe ser único dentro de un mismo espacio. Se pueden duplicar todas las demás propiedades de una configuración o política.
- Además, las configuraciones pueden duplicarse en todos los espacios a los que usted tiene acceso como administrador. No es necesario ser el Administrador global para poder duplicar una configuración.

## Duplicar una configuración o política

**Procedimiento**

1. Vaya a **Configuraciones** o **Políticas**, dependiendo de lo que desee duplicar.
2. Haga clic en el enlace para que la configuración o política muestre los detalles.
3. Haga clic en el icono **Duplicar**.
4. En la ventana emergente, introduzca un **Nombre** y, opcionalmente, una **Descripción**.
5. Haga clic en **Siguiente**.
6. Modifique la configuración o la política según sus requisitos.
7. Haga clic en **Siguiente**.
8. Configure la distribución.
9. Haga clic en **Hecho**.
