---
title: Añadir el usuario de una API para operaciones de Cisco ISE
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Puede agregar un usuario de API con el rol "Operaciones de Cisco ISE” que permite a Cisco ISE interactuar con la API de Cisco ISE en Ivanti Neurons for MDM. Después de crear este usuario, se utilizan sus credenciales de Cisco ISE para autenticar las llamadas API en Ivanti Neurons for MDM. Estas API permiten a Cisco ISE obtener información sobre el dispositivo, realizar acciones sobre el dispositivo (como por ejemplo un borrado total, borrado corporativo y bloqueo del PIN) y enviar mensajes a los dispositivos.

el usuario de la API no podrá acceder al portal de administración. Este usuario es solo para habilitar el uso de la API.

solo al Superadministrador de un abonado se le asigna la función de Operaciones de Cisco ISE de forma predeterminada. El Superadministrador debe elegir explícitamente a los demás usuarios del sistema que deben tener esta función y asignársela. Los usuarios asignados a la función de Operaciones de Cisco ISE pueden, por su parte, asignar la función a otros usuarios adecuados en el sistema.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en la pestañ&#x61;**&#x20;Usuarios**.
:::

:::WorkflowBlockItem
:inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/Ta2A_aCJRGg8Xqpt8nFSA_r36addapiuser001.png" alt caption}
Haga clic en **Añadir**.
:::

:::WorkflowBlockItem
Seleccione **Usuario de API**.
:::

:::WorkflowBlockItem
Complete el formulario resultante con la información del usuario:
:::

:::WorkflowBlockItem
- Dirección de correo electrónico
- Nombre
- Apellidos
  El campo del nombre de usuario muestra la dirección de correo electrónico que ha introducido. En la mayoría de los casos, no debe editar este campo predeterminado. Consulte [**Cuándo editar un nombre de usuario**](./Editar_un_nombre_de_usuario.md).

Si desea cambiar el nombre en pantalla de este usuario, edite el texto predeterminado en el campo **Nombre en pantalla**.
:::

:::WorkflowBlockItem
Asigne una contraseña introduciéndola en los campos **Contraseña** y **Confirmar contraseña**.
:::

:::WorkflowBlockItem
Deje seleccionada la función **Operaciones de gestión de API de Cisco ISE** en la sección **Asignar funciones**.
:::

:::WorkflowBlockItem
Haga clic en **Hecho** para añadir al usuario.
:::
::::

Si no puede realizar las tareas en la página **Usuarios**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Administración de usuarios
