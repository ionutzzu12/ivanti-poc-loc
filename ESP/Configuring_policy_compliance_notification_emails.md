---
title: Configuring policy compliance notification emails
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

## Configuración y uso de los correos electrónicos de notificación de cumplimiento de políticas

Los administradores pueden ajustar en una plantilla de correo electrónico de notificación de cumplimiento de políticas los correos electrónicos enviados por las acciones de envío de correos «políticas de aplicaciones personalizadas y permitidas» para los usuarios cuyos dispositivos hayan infringido el cumplimiento. Los siguientes procesos describen la configuración:

- **Configuración de la función:**\* **Configure la plantilla de correo electrónico**.La plantilla de correo electrónico en inglés tiene este aspecto por defecto, pero se puede revisar para que se adapte mejor a sus necesidades siguiendo las instrucciones que hay en [**Personalización de una plantilla de correo electrónico**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md) en [**Cómo personalizar las plantillas de correo electrónico**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md)

::Image[]{src="Resources/Images/68PolicyEmailTemplate.png" signedSrc="Resources/Images/68PolicyEmailTemplate.png" size="41" caption alt isUploading="false" sha initialPath="Resources/Images/68PolicyEmailTemplate.png" githubPath="Resources/Images/68PolicyEmailTemplate.png" position="flex-start" indent="2"}

:::Paragraph{listStyleType="disc" indent="2"}
**Active la plantilla de notificación de cumplimiento de políticas**. Esta plantilla funciona junto con el mensaje que se elabora mediante las acciones de envío de correo electrónico de «políticas de aplicaciones personalizadas y permitidas» . Ivanti Neurons for MDM inserta la información que usted especifica en esas acciones de correo electrónico en la plantilla de notificación de cumplimiento de políticas. Se puede activar la plantilla de correo electrónico de cumplimiento de políticas al crear o editar una política de aplicaciones personalizadas o permitidas. Para obtener más información sobre las instrucciones para habilitar la plantilla de notificación de cumplimiento de políticas para una política Personalizada o una política de Aplicaciones permitidas, consulte [**Añadir una política personalizada**](./Política_personalizada.md) y [**Crear una Política de aplicaciones permitidas**](./Supervisar_y_controlar_las_aplicaciones_permitidas.md) respectivamente.
:::

- **Cómo usar esta función:**\* Cuando un dispositivo no cumple con una política de aplicaciones personalizadas o permitidas con la plantilla de notificación de políticas activada, Ivanti Neurons for MDM envía un correo electrónico al propietario del dispositivo, y ajusta primero el correo electrónico en la plantilla de notificación de políticas. Su interacción con esta función consiste en configurarla como se ha resumido anteriormente, mientras que Ivanti Neurons for MDM es quien hace uso de esta función.
