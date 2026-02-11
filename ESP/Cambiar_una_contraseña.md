---
title: Cambiar una contraseña
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Cambiar contraseña desde la pestaña Usuarios**](./Cambiar_una_contraseña.md)
- [**Aplicar contraseña que nunca caduque**](./Cambiar_una_contraseña.md)
- [**Eliminar el ajuste para que no caduque nunca la contraseña**](./Cambiar_una_contraseña.md)

Si un usuario tiene un rol de Administración del sistema, solo un Súperusuario o un usuario que tenga la sesión activa podrá ver la opción **Cambiar contraseña**.

Puede cambiar su contraseña de Ivanti Neurons for MDM. También puede cambiar la contraseña para otro usuario si tiene permiso.

**Procedimiento**

1. Haga clic en el icono Cuenta (arriba a la derecha).
2. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/S-yYRfrWZXHOGx4Z-L7mr_usericon.png" alt caption}
   Seleccione **Cambiar contraseña** en el menú desplegable.
3. Introduzca su contraseña actual.
4. Introduzca su nueva contraseña.
5. Introduzca otra vez su nueva contraseña.
6. Para definir una contraseña que no caduque, seleccione **Establecer contraseña para que nunca caduque**.al establecer la contraseña para que nunca caduque, se anula el **Período de caducidad de la contraseña** definido en Usuarios > Ajustes del usuario > Ajuste de complejidad de la contraseña.
7. Haga clic en **Hecho**.para restablecer la contraseña de la cuenta local y que caduque, desactive la opción **Establecer contraseña para que nunca caduque**. Una vez que esta opción deje de estar seleccionada, una ventana emergente mostrará la fecha de caducidad anterior de la contraseña aplicada al usuario.

## Cambiar contraseña desde la pestaña Usuarios

**Procedimiento**

1. Vaya a **Usuarios.**
2. Haga clic en el nombre en pantalla del usuario.
3. Haga clic en **Editar** (arriba a la izquierda). Se abre la ventana **Autenticación obligatoria**. Los administradores (que son usuarios locales o usuarios de LDAP) deben autenticarse introduciendo la contraseña del administrador antes de editar el usuario.
4. Introduzca su contraseña de administrador y haga clic en **Autenticar**.cuando se introducen varias entradas incorrectas de la contraseña y si se supera el «Límite del umbral de inicio de sesión fallido» establecido en los «Ajustes de complejidad de la contraseña», la cuenta se bloqueará y se cerrará la sesión actual.
5. Introduzca la contraseña actual en el campo **Contraseña actual**.este campo no se mostrará cuando cambie la contraseña de otro usuario.
6. Introduzca la nueva contraseña en el campo **Cambiar contraseña**.
7. Confirme la nueva contraseña.
8. Haga clic en **Guardar** (arriba a la izquierda).

## Aplicar contraseña que nunca caduque

1. Vaya a **Usuarios.**
2. Seleccione uno o más usuarios.
3. Haga clic en **Acciones**.
4. Seleccione **Asignar contraseña para que no caduque nunca**. Aparece la ventana **Establecer contraseña de la cuenta local para que nunca caduque**.
5. Haga clic en **Enviar**.

## Eliminar el ajuste para que no caduque nunca la contraseña

1. Vaya a **Usuarios.**
2. Seleccione uno o más usuarios.
3. Haga clic en **Acciones**.
4. Seleccione **Eliminar la opción de que la contraseña no caduque nunca**. Aparece la ventana **Eliminar la contraseña de la cuenta local para que nunca caduque**.
5. Haga clic en **Enviar**. Una vez que se haya eliminado este ajuste, se aplicará a los usuarios la fecha de caducidad anterior de la contraseña.
