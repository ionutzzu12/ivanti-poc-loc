---
title: Reasignar un dispositivo Android
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

El administrador puede transferir la propiedad de un dispositivo Android de un usuario a otro. Durante el proceso de reasignación, el perfil de gestión del dispositivo se reconfigurará o reasignará del usuario actual al nuevo usuario en modo Android Enterprise. La reasignación se puede realizar en todos los dispositivos de Android Enterprise excepto en los dispositivos de Android Management API (AMAPI) y no se puede realizar en los dispositivos de Android Enterprise de Google Domain.

La reasignación de dispositivos solo puede realizarse con los dispositivos en el mismo modo. Por ejemplo, un dispositivo en modo Dispositivo gestionado por el trabajo puede reasignarse a otro usuario en el mismo modo.

El proceso de reasignación de dispositivos tendrá los estados siguientes:

- Iniciado
- Éxito
- Error
- Pendiente

Puede ver el estado de la última reasignación de un dispositivo en la página **Detalles del dispositivo** > pestaña **Información general** > **Estado de la última reasignación**.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Seleccione uno o más dispositivos de la lista.
3. En la lista **Acciones**, haga clic en **Asignar al usuario**.
4. También puede hacer clic en el nombre de cualquier dispositivo. Se abre la **página de información del dispositivo**. Haga clic en el icono **Asignar a usuario** para acceder a la pantalla Asignar a usuario y seleccionar el usuario deseado.
5. Haga clic en **Asignar al usuario**. Las opciones seleccionadas se validarán para comprobar si los dispositivos seleccionados pueden reasignarse a los usuarios seleccionados o no.
   Tras la validación y reasignación correctas, aparece un mensaje de confirmación en la pantalla.
   Si ha seleccionado un número máximo de 10 dispositivos, aparecerá en pantalla el mensaje "Asignación iniciada". Si ha seleccionado 11 o más dispositivos, aparecerá en pantalla la ventana emergente "Validación en curso".

La reasignación de dispositivos Android es una solución innovadora creada exclusivamente para eliminar los datos sobrantes del usuario registrado anterior y solo está disponible en la SKU SUEM-Premium.
