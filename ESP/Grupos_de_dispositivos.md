---
title: Grupos de dispositivos
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Añadir un grupo de dispositivos**](./Grupos_de_dispositivos.md)
- [**Eliminar un grupo de dispositivos**](./Grupos_de_dispositivos.md)
- [**Exportación de dispositivos a un archivo CSV**](./Grupos_de_dispositivos.md)

En la página **Grupos de dispositivos**, puede crear listas de dispositivos que desee tratar de la misma manera. Puede definir y asignar políticas y configuraciones en los grupos de dispositivos. Los siguientes grupos son los grupos de dispositivos predeterminados creados por Ivanti Neurons for MDM:

- Todos los dispositivos
- Dispositivos Android
- Dispositivos con Android Enterprise
- Dispositivos iOS
- Tipo de dispositivo (Apple)
- Dispositivos tvOS
- Dispositivos macOS
- Dispositivos de visionOS
- Dispositivos watchOS
- Dispositivos Windows

Los detalles de las aplicaciones asignadas a un grupo de dispositivos concreto se muestran en la pestaña **Aplicaciones** para el grupo de dispositivos específico.

El grupo de dispositivos tvOS es un subconjunto del grupo de dispositivos iOS. Por lo tanto, las configuraciones y políticas aplicadas al grupo tvOS podrían verse sobrescritas por las del grupo de dispositivos iOS.

## Añadir un grupo de dispositivos

Agregar un grupo de dispositivos no es aplicable a grupos de usuarios dinámicos.

Según el tipo de licencia que tenga, puede agregar un nuevo grupo de dispositivos basado en reglas para identificar los dispositivos con los criterios específicos. Los dispositivos que coinciden con las reglas se muestran bajo de la sección del generador de reglas. Las reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Las regla se pueden crear con los operadores siguientes:

- comienza con
- termina con
- contiene
- no contiene
- no comienza con
- no termina con
- es menor que
- es mayor que
- se encuentra en el intervalo
- es igual a
- no es igual a
- no está en blanco
- está en blanco

El Ivanti Neurons for MDM administrador muestra un número de grupos de usuarios duplicados y el número correspondiente de GUID para identificar los grupos duplicados, cuando se selecciona el atributo Nombre del grupo de usuarios en al generador de reglas. Además, una tabla bajo esta regla muestra la lista de los grupos de usuarios duplicados y sus detalles, como el Nombre del Grupo de Usuarios, el GUID, la Fuente y el nombre distinguido (DN).

**Licencia Bronze:**

Las funciones pueden identificar dispositivos siguiendo los siguientes criterios:

- Tipo de dispositivo
- SO - el sistema operativo (prerrellenado)
- Versión de SO
- SO con versión
- Grupo de usuarios

**Licencia Silver:**

Las funciones pueden identificar dispositivos siguiendo los siguientes criterios:

- Entra ID Inscrito
- Número alternativo de serie (Solo Android: aplicable a dispositivos Samsung en modo Administrador del dispositivo o Propietario del dispositivo)
- Dispositivo Android dedicado
- Compatible con Android Enterprise
- Dispositivo administrado de Android con perfil profesional
- Tipo de certificación SafetyNet de Android
- Android for Work habilitado
- Dispositivos Android administrados en el trabajo (Propietario del dispositivo) habilitados
- Perfil de Android for Work habilitado
- Perfil de trabajo de Android en el Dispositivo propiedad de la empresa habilitado
- Estado nativo de antiphishing
- Estado de antiphishing
- Estado de la VPN de antiphishing
- Preparado para APNS
- Dispositivo Apple Silicon
- Inscripción de dispositivos automatizada activada
- Identificador del dispositivo Azure
- Estado de cumplimiento del dispositivo Azure
- Código de estado del cliente de Azure
- Hora del informe de cumplimiento del dispositivo Azure
- Cifrado de BitLocker
- Sentry bloqueado
- Acceso bloqueado
- Token de Bootstrap disponible
- Tipo de aprovisionamiento en masa (Apple Configurator, Ninguno o Inscrito en la Inscripción de dispositivos automatizada)
- Operador
- Último ingreso del cliente
- Registrado con el cliente
- Cumplimiento
- Medida de cumplimiento bloqueada
- Nombre del país actual (seleccione el nombre del país actual de la lista desplegable)
- MMC actual
- MNC actual
- Atributo personalizado del dispositivo
- Atributo personalizado de LDAP
- Atributo personalizado del usuario
- Itinerancia de datos
- Dispositivo registrado
- Origen del dispositivo
- Tipo de dispositivo
- Nombre en pantalla
- Cifrado habilitado
- Particiones del disco duro
- Nombre del país de origen (seleccione el nombre del país de origen de la lista desplegable)
- MCC de origen
- MNC de origen
- IMEI
- IMEI2 (solo en dispositivos Android con doble puerto SIM y aplicable para dispositivos Android 8.0 o superior)
- Dirección IP
- Modo pantalla completa
- Último ingreso
- Solo MAM
- Fabricante
- Estado de activación del MTD
- SO
- Edición de SO
- Versión de SO
- SO con versión
- Propiedad
- N.º de teléfono
- Dirección IP pública (dispositivos Android o ChromeOS)
- En cuarentena
- Bloqueo de recuperación habilitado
- Itinerancia
- Estado de Secure Apps
- Número de serie
- Estado
- Supervisado
- Versión del sistema
- Capacidad total del dispositivo
- Memoria total MB
- Versión de TPM
- Desbloquear token disponible (iOS)
- Inscripción de usuarios activada
- Grupo de usuarios
- Itinerancia de voz
- Clave de recuperación personal de macOS en custodia
- Tipo de clave de recuperación de macOS

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en **Añadir**.
:::

:::WorkflowBlockItem
Introduzca un nombre para el grupo.
:::

:::WorkflowBlockItem
Introduzca una descripción opcional para el grupo.
:::

:::WorkflowBlockItem
Seleccione el tipo de grupo de dispositivos que desea crear:\* **Gestionado dinámicamente**: Utiliza reglas para definir qué dispositivos están en el grupo.

- **Gestionado manualmente**: Introduzca cada usuario cuyos dispositivos deben incluirse en el grupo.
:::

:::WorkflowBlockItem
Para grupos administrados dinámicamente:1) Cree una regla que defina el grupo.
2\) **Ejemplo**: SO es iOS

Haga clic en **+** para crear reglas adicionales, si fuera necesario.
3\) **Ejemplo**: El dispositivo es el iPhone 5S

Haga clic en **Cualquiera** si los dispositivos tienen que cumplir al menos una de las reglas.
4\) Haga clic en **Todas** si los dispositivos tienen que cumplir todas las reglas.
:::

:::WorkflowBlockItem
Para grupos administrados manualmente:
:::

:::WorkflowBlockItem
1. Escriba el nombre de un usuario cuyo dispositivo desee añadir.
2. Seleccione el dispositivo de la lista que se muestra.
3. Repita los pasos «a» y «b» hasta que todos los dispositivos aparezcan en la lista.
   Haga clic en **Guardar**.
:::
::::

## Eliminar un grupo de dispositivos

**Procedimiento**

1. Ir &#x61;**&#x20;Dispositivos**>**Grupos de dispositivos**.
2. Marque la casilla del grupo de dispositivos que desea eliminar.
3. Haga clic en **Eliminar Grupo de dispositivos**.

## Exportación de dispositivos a un archivo CSV

Puede exportar la información del dispositivo de un grupo de dispositivos específico mediante la opción **Exportar a CSV** desde la página **Grupos de dispositivos**.

**Procedimiento**

1. Ir &#x61;**&#x20;Dispositivos**>**Grupos de dispositivos**.
2. Seleccione todos o múltiples espacios para ver la información relacionada con espacios específicos.
3. Haga clic en el enlace del número de grupos de dispositivos. Se muestra la página Lista de dispositivos relacionada con el espacio seleccionado.
4. Haga clic en la opción **Exportar a CSV** para exportar la lista de dispositivos y detalles relacionados a un archivo CSV. Aparece un mensaje emergente que informa de que el informe de exportación tardará un tiempo en procesarse. Espere a que se complete la solicitud para enviar otra solicitud.
5. Haga clic en **Descargar**. Recibirá un correo electrónico con un enlace para descargar el informe.
6. (Opcional) Haga clic en **Eliminar&#x20;**&#x70;ara eliminar el informe.

Si no puede ver la página **Grupos de dispositivos**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md)

- Administración de dispositivos
- Dispositivo de solo lectura
