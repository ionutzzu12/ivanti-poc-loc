---
title: Inscripción en masa de Ivanti
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

El administrador puede inscribir múltiples dispositivos de Windows con un usuario genérico (a través de ppkg) que comienza con el prefijo **windows-bulkenroll**, y luego realiza la asignación del usuario.

**Requisitos previos:**

- En el Ivanti Neurons for MDM, cree una cuenta de usuario con prefijo como **windows-bulkenroll**. Por ejemplo, **windows-bulkenroll**[**-user1@abc.com**](mailto:-user1@abc.com), **windows-bulkenroll**[**-user2@abc.com**](mailto:-user2@abc.com).

**Creación del paquete PPKG con Diseñador de configuración de Windows**

::::WorkflowBlock
:::WorkflowBlockItem
Descargue e instale el **Ddiseñador de configuración de Windows**.
:::

:::WorkflowBlockItem
Crear nuevo proyecto.
:::

:::WorkflowBlockItem
Haga clic en **Aprovisionar escritorio**.
:::

:::WorkflowBlockItem
Introduzca el nombre del proyecto y seleccione una ruta.
:::

:::WorkflowBlockItem
En la sección **configurar el dispositivo**, introduzca el nombre del dispositivo.
:::

:::WorkflowBlockItem
En la sección **Configuración de red**, introduzca el nombre de la red (para configurar la red, si es necesario o se puede deshabilitar).
:::

:::WorkflowBlockItem
En la sección **Gestión de la cuenta**, seleccione **Inscribirse en el administrador local**. Introduzca **Nombre de usuario** y **Contraseña**, y haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
En la sección **Agregar aplicaciones**, haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
En la sección **Agregar certificados**, seleccione **Switch al editor avanzado** y haga clic en **proceder** > **Sí**.
:::

:::WorkflowBlockItem
Vaya a **RuntimeSettings** > **Inscripciones en el lugar de trabajo**. Introduzca **UPN** (el mismo usuario creado en Ivanti Neurons for MDM en la sección de requisitos previos). Seleccione las siguientes opciones:
:::

:::WorkflowBlockItem
- AuthPolicy: OnPremise
- DiscoveryServiceFullUrl: Introduzca la URL Leo
- Secreto: introduzca la contraseña
  Haga clic en **Archivo** > **Guardar**.
:::

:::WorkflowBlockItem
Haga clic en **Exportar** > **Paquete de aprovisionamiento**.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente** en las pantallas siguientes y haga clic en **Generar**.

El archivo ppkg se guarda en la ubicación especificada.
:::
::::

**Dispositivo de provisión en modo OOBE con PPKG**

Provise los dispositivos con el archivo del paquete PPKG recién creado de la sección anterior. Una vez que el dispositivo se inscribe y el registro sea exitoso, encontrará la entrada del dispositivo en el servidor MDM con el usuario que tiene prefijo como **windows-bulkenroll**.

**Asignar dispositivo al usuario**

1. En la página de dispositivos, haga clic en el usuario que tiene un prefijo como **windows-bulkenroll**.
2. Haga clic en **Asignar a usuario**. Se abre la ventana Asignación a la ventana de usuario.
3. Seleccione o busque el dispositivo de la lista.
4. Seleccione el dispositivo requerido.
5. Haga clic en **Asignar a usuario**. El dispositivo seleccionado se asignará al usuario.

Cuando el usuario inicia sesión en el dispositivo por primera vez, el cambio de contraseña es imprescindible.

La opción de asignación a la opción de usuario solo está disponible para los dispositivos inscritos a granel Ivanti.

Solo las configuraciones y aplicaciones de alcance del dispositivo funcionarán para los dispositivos inscritos en esta categoría. Las configuraciones y aplicaciones de alcance del usuario no son compatibles.
