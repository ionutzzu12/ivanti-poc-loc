---
title: Configurador de Apple
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Puede usar esta página para preparar Apple Configurator para configurar la administración de dispositivos de Ivanti Neurons for MDM en dispositivos iOS. Apple Configurator hace que sea muy fácil implementar los dispositivos iOS en grandes cantidades. Además, Configurator permite a los administradores tener los dispositivos iOS supervisados, lo que permite un mayor nivel de capacidades de configuración y administración. Para más información sobre Apple Configurator, diríjase a la Mac App Store.

Los pasos básicos son los siguientes:

1. Exporte el perfil de MDM desde el abonado de Ivanti Neurons for MDM.
2. Importe el perfil MDM al Configurator.
3. Utilice el Configurator para aplicar el perfil MDM a los dispositivos anclados.

## Definir un usuario predeterminado para los dispositivos

Los dispositivos configurados a través de Apple Configurator se asignan al usuario “nadie” en Ivanti Neurons for MDM a menos que elija un usuario diferente:

1. Haga clic en el campo **Asignar dispositivos configurados a**.
2. Comience a escribir el nombre de usuario del usuario de Ivanti Neurons for MDM que desee seleccionar.
3. Seleccione el nombre de usuario cuando aparezca en la lista desplegable.
4. Haga clic en **Guardar**.

## Instalar aplicaciones con Apple Configurator

Antes de usar Apple Configurator para instalar aplicaciones:

- El acceso a la app store de Apple está restringido por la configuración del dispositivo.
- La instalación de aplicaciones está permitida por la configuración del dispositivo.
- Apple Configurator debe estar instalado en el ordenador utilizado para configurar los dispositivos.

Para instalar aplicaciones con Apple Configurator:

::::WorkflowBlock
:::WorkflowBlockItem
En Ivanti Neurons for MDM, vaya a **Administración > Configurador de Apple**.
:::

:::WorkflowBlockItem
Cambie el interruptor de dispositivos de inscripción a ON (encendido).
:::

:::WorkflowBlockItem
Haga clic en una de las siguientes opciones:
:::

:::WorkflowBlockItem
- **Plist predeterminada del usuario**.
- **Plist de usuario específico**: introduzca el nombre de usuario o la identificación de correo electrónico del usuario específico.
  En Apple Configurator, vaya a **Preparar > Aplicaciones**.
:::

:::WorkflowBlockItem
Vaya a **Preparar > Ajuste y desactivar supervisión**.
:::

:::WorkflowBlockItem
Seleccione la opción **No actualizar nunca el dispositivo** en Actualizar iOS.
:::

:::WorkflowBlockItem
Haga clic **Preparar&#x20;**(en la parte inferior de Apple Configurator).Las aplicaciones estarán visibles en la lista de aplicaciones instaladas del dispositivo una vez que el dispositivo ingrese.
:::
::::

## Instalar aplicaciones con el servidor UEM

Para instalar aplicaciones con el servidor UEM:

1. Cargue una aplicación desde la tienda interna de la pestaña Aplicaciones.
2. Seleccione la aplicación.
3. Haga clic en la pestaña **Configuraciones de la aplicación**.
4. Seleccione **Instalar en dispositivo**.Complete los ajustes de la configuración.
5. Seleccione **Acciones > Forzar ingreso**.

## Qué necesita hacer el usuario final

Apple requiere que el usuario final inicie Go al menos una vez o la característica de Ubicación de Ivanti Neurons for MDM no funcionará correctamente. Esto es necesario para garantizar que el usuario final es consciente de que su localización está siendo objeto de un seguimiento.

**Precaución:** Si los dispositivos han sido implementados en modo Single-App mediante Configurator, este enfoque no será posible.

Si no puede ver la página **Instalar Apple Configurator**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Sistema de solo lectura
