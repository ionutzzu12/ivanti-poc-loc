---
title: Cómo personalizar las plantillas de correo electrónico
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

Puede personalizar la invitación por correo electrónico del usuario final para que la apariencia le resulte más familiar a sus usuarios finales. Haga clic en **Revertir a los ajustes predeterminados** para borrar las personalizaciones.

Puede personalizar las siguientes plantillas de correo electrónico en todos los idiomas compatibles:

- **Invitación del usuario final**- invite a un usuario a conectar sus dispositivos para obtener acceso a aplicaciones y configuraciones.
- **Notificación de restablecimiento de contraseña**- el sistema envía correos electrónicos recordatorios 7 días y 24 horas antes de la caducidad de la contraseña de las cuentas locales. Esta opción no es aplicable a las cuentas LDAP.
- **Confirmación de registro**- el correo electrónico se envía una vez que el usuario completa el registro. Puede usar esta opción para agradecer a los usuarios que se hayan registrado y para indicarles más recursos de aprendizaje.
- **Notificación de cumplimiento de políticas**- el correo electrónico se envía cuando los dispositivos no cumplen con la política.

Esta sección contiene los siguientes temas:

- [**Previsualizar y probar una plantilla de correo electrónico**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md)
- [**Personalizar los encabezados de los mensajes**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md)
- [**Personalización de una plantilla de correo electrónico**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md)
- [**Variables de correo electrónico compatibles**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md)

## Previsualizar y probar una plantilla de correo electrónico

Puede previsualizar y probar las plantillas de correo electrónico. Esta prueba le permite enviar un correo electrónico basado en la plantilla a una dirección de correo electrónico que usted especifique.

Para previsualizar y probar una plantilla de correo electrónico:

1. Haga clic en **Administrador**.
2. En Plantillas de correo electrónico, haga clic e&#x6E;**&#x20;Invitación de usuario final**,**&#x20;Notificación de restablecimiento de contraseña&#x20;**, **Confirmación de registro**, o**Notificación de cumplimiento de políticas**.
3. Haga clic en el enlace **Previsualizar y probar** asociado con la plantilla de correo electrónico que desea previsualizar y probar.
4. Vea la plantilla procesada en el panel de plantillas procesadas.
5. Especifique una dirección de correo electrónico de prueba a la que enviar el correo electrónico de prueba.Si la dirección de correo electrónico que usted especifica pertenece a un usuario actual, el correo electrónico de prueba sustituirá los valores de la mayoría de las variables de la plantilla de correo electrónico, proporcionándole una idea bastante precisa de cómo será la experiencia del usuario con el correo electrónico. No obstante, el correo electrónico de prueba no sustituirá los valores de las variables que Ivanti Neurons for MDM genera en el momento en que genera una invitación real por correo electrónico.
6. Haga clic en **Enviar correo electrónico de prueba**.

## Personalizar los encabezados de los mensajes

1. Haga clic en **Administrador**.
2. Haga clic en **Plantillas de correo electrónio**.
3. Haga clic en el vínculo del icono **Editar** (situado en la columna Acciones) asociado con la plantilla de correo electrónico que desea editar.
4. Proporcione los nuevos ajustes que desee para **Nombre para mostrar del correo electrónico**, **Dirección de correo electrónico del remitente**, **Dirección de correo electrónico de respuesta** y **Configurar correo electrónico SMTP**.
5. Si personaliza las direcciones de correo electrónico del remitente y a la que responder, recomendamos que ponga en la lista de permitidos el servicio de retransmisión de correo electrónico para asegurarse de que sus mensajes de correo electrónico no los bloqueen los servicios de filtrado de SPAM. Consulte [**este documento**](https://forums.ivanti.com/s/article/MobileIron-Cloud-Ports-Hosts-and-IP-Addresses) para ver más información.
   Haga clic en **Guardar**.
6. Revise la previsualización de la plantilla de correo electrónico y haga clic en **Guardar**.

## Uso de la configuración de SMTP

Se ha añadido **Ajustar la configuración de correo electrónico de SMTP** para que el administrador pueda configurar su propia integración del servidor de correo electrónico para las notificaciones salientes.

1. Vaya a **Administración > Marca > Ajustes de correo electrónico**, active la opción **Establecer la configuración de correo electrónico SMTP**.
2. Actualice los siguientes campos:\* Servidor SMTP
   - Puerto del servidor SMTP
   - Protocolo
   - Nombre de usuario
   - Contraseña
3. Haga clic en **Probar** para enviar un correo de prueba, aparecerá una pantalla emergente **Correo electrónico de prueba**.
4. Introduzca el nombre **Destinatario** y **Cuerpo** del mensaje, haga clic en **Guardar**.Si las credenciales no son correctas, aparecerá un mensaje de error.
5. Haga clic en **Guardar**.

La tabla siguiente resume los campos y descripciones de la ventana Configuración de SMTP:

| Campos                   | Descripción                                                                                                                                                                  |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor SMTP            | Especifique la dirección IP o el nombre de host completo del servidor SMTP que utilizará el servidor Ivanti Neurons for MDM.                                                 |
| Puerto del servidor SMTP | Especifique el puerto configurado para el servidor SMTP.                                                                                                                     |
| Protocolo                | Si el servidor SMTP que está configurando es un servidor seguro, es decir, utiliza el protocolo SMTPS, seleccione el botón SMTPS. En caso contrario, deje seleccionado SMTP. |
| Nombre de usuario        | Introduzca el nombre de usuario necesario para la autenticación SMTP.                                                                                                        |
| Contraseña               | Introduzca la contraseña necesaria para la autenticación SMTP.                                                                                                               |

## Personalización de una plantilla de correo electrónico

1. Seleccione **Administrador > Personalización > Plantillas de correo electrónico**.
2. Seleccione la plantilla que se va a editar, **Invitación de usuario final**, **Notificación de restablecimiento de contraseña**, **Confirmación de registro** o **Notificación de cumplimiento de políticas**.
3. Haga clic en el icono del lápiz para editar que aparece junto a la plantilla de correo electrónico que desee personalizar.

::Image[]{src="r45emailtemplates003.png" signedSrc="r45emailtemplates003.png" size="35" caption alt isUploading="false" sha initialPath="r45emailtemplates003.png" githubPath="r45emailtemplates003.png" position="flex-start" indent="2"}

4. Edite la línea de asunto, si así lo desea.
5. Edite la plantilla de correo electrónico que contiene los elementos HTML del panel del cuerpo para personalizar el contenido del mensaje.|                    |                                                                                                                                                                  |
   \| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/SQzgYEkUp0Aua6_gXx8uA_infoicon.png" alt caption} | Puede utilizar las variables que aparecen en la parte derecha del cuerpo del correo electrónico. Consulte [**Variables compatibles del correo electrónico**](./Cómo_personalizar_las_plantillas_de_correo_electrónico.md). |
6. Haga clic en **Vista previa** para previsualizar la plantilla de correo electrónico a medida va creando iteraciones según lo desee.
7. Cuando esté listo para guardar la plantilla, haga clic en **Vista previa**. Esto generará la vista previa y le ofrecerá la función de guardado.

::Image[]{src="r45emailtemplates004.png" signedSrc="r45emailtemplates004.png" size="19" caption alt isUploading="false" sha initialPath="r45emailtemplates004.png" githubPath="r45emailtemplates004.png" position="flex-start" indent="2"}

8. Haga clic en **Guardar** si está satisfecho con la vista previa.

### Contenido en la lista de permitidos y la lista de bloqueados en la invitación personalizada para el usuario

Mientras personaliza la plantilla de correo electrónico de la invitación del usuario en **Invitación del usuario final**, hay un conjunto de etiquetas de HTML en la lista de permitidos y atributos que están permitidos. También existe una lista de cadenas en la lista de bloqueados que no están permitidas en la invitación del usuario para evitar la vulnerabilidad de Cross Site Scripting (XSS).

Solo tiene permiso para usar las etiquetas y atributos de la lista de permitidos que hay en el correo electrónico de la invitación. En la siguiente tabla se enumeran las etiquetas de la lista de permitidos y sus atributos correspondientes permitidos.

Algunas etiquetas de la lista permitida (ejemplo: \<big>) no deben tener ningún atributo de la lista permitida y, por tanto, se muestran en blanco.

| Etiquetas incluidas en la lista de permitidos | Atributos incluidos en la lista de permitidos                                                                                                                      |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| \<big>                                        | \[]                                                                                                                                                                |
| \<img>                                        | \["id","label","editable","height","border","src","style","width", "align", "class","cellpadding","alt","title","data-max-width","data-default"]                   |
| \<strong>                                     | \[]                                                                                                                                                                |
| \<singleline>                                 | \["label"]                                                                                                                                                         |
| \<tbody>                                      | \[]                                                                                                                                                                |
| \<!DOCTYPE>                                   | \[]                                                                                                                                                                |
| \<h1>                                         | \["style"]                                                                                                                                                         |
| \<h2>                                         | \["style"]                                                                                                                                                         |
| \<hr>                                         | \["noshade","style"]                                                                                                                                               |
| \<h3>                                         | \[]                                                                                                                                                                |
| \<body>                                       | \["style", "class", "bgcolor", "paddingwidth", "paddingheight", "offset", "toppadding", "leftpadding", "lang","link","vlink","border","cellspacing","cellpadding"] |
| \<title>                                      | \["id"]                                                                                                                                                            |
| \<head>                                       | \[]                                                                                                                                                                |
| \<div>                                        | \["style","class","width","align","id"]                                                                                                                            |
| \<br>                                         | \[]                                                                                                                                                                |
| \<path>                                       | \["d"]                                                                                                                                                             |
| \<ul>                                         | \["style"]                                                                                                                                                         |
| \<html>                                       | \["xmlns","xmlns\:mso","xmlns\:msdt"]                                                                                                                              |
| \<ol>                                         | \["start"]                                                                                                                                                         |
| \<table>                                      | \["class","width","border","cellspacing","cellpadding","style","height","bgcolor","align","background"]                                                            |
| \<a>                                          | \["href","style","target","rel","class","title"]                                                                                                                   |
| \<b>                                          | \[]                                                                                                                                                                |
| \<o\:p>                                       | \[]                                                                                                                                                                |
| \<svg>                                        | \["xmlns","class","viewbox","width","height","role","aria-labelledby"]                                                                                             |
| \<center>                                     | \[]                                                                                                                                                                |
| \<em>                                         | \[]                                                                                                                                                                |
| \<i>                                          | \[]                                                                                                                                                                |
| \<label>                                      | \["style"]                                                                                                                                                         |
| \<td>                                         | \["valign","width","height","class", "cellpadding", "cellspacing","border","bgcolor","align", "style","colspan","id"]                                              |
| \<p>                                          | \["style","class","align"]                                                                                                                                         |
| \<u>                                          | \[]                                                                                                                                                                |
| \<meta>                                       | \["name","content","http-equiv","charset"]                                                                                                                         |
| \<multiline>                                  | \["label"]                                                                                                                                                         |
| \<style>                                      | \["type","id"]                                                                                                                                                     |
| \<li>                                         | \["style"]                                                                                                                                                         |
| \<tr>                                         | \["style"]                                                                                                                                                         |
| \<span>                                       | \["style","class","lang"]                                                                                                                                          |
| \<font>                                       | \["color"]                                                                                                                                                         |

A continuación se muestra la lista de cadenas en la lista de bloqueados que no están permitidas en la invitación de usuario personalizada.

- Script, @import, ¼script¾, script>, \<script, \<script>, \</script>, javascript, alert(, moz-binding, expression(, +ADw-SCRIPT+AD4- ,+ADw-/SCRIPT+AD4-, xml\:base
- Caracteres especiales y búsqueda de javascript o secuencia de comandos
- El atributo de metacontenido que contiene "url=" no distingue entre mayúsculas y minúsculas
- El img src que no contiene .svg.
- Valor de atributo que contiene "\00"

Si se usa alguna de las cadenas de texto de la lista de bloqueados anterior en el contenido HTML de la invitación del usuario final, aparecerá un mensaje de error al hacer clic en **Vista previa**. Este mensaje de error muestra el contenido HTML que no está permitido en la invitación del usuario final. Edite y elimine el contenido HTML no permitido y, a continuación, haga clic en **Vista previa** para continuar.

No se le permitirá guardar las plantillas editadas que contengan contenido HTML en una lista de bloqueados.

## Variables de correo electrónico compatibles

Ivanti Neurons for MDM ofrece diversas variables que puede utilizar para personalizar sus plantillas de correo electrónico.

### Variables de la invitación del usuario final

| Variable                                                 | Descripción                                                                                                                                                                      |
| -------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\{userActivationUrl}                                    | La URL de activación del usuario: este es el hipervínculo que aparece en torno al texto $\{email.idp.invitation.get.started}.                                                    |
| $\{clusterRegistrationUrl}                               | La URL de registro del clúster: NO aparece en la plantilla predeterminada, pero se hace referencia a ella indirectamente (a través de la variable $\{email.idp.invitation.pg4}). |
| $\{productBrandName}                                     | El nombre de marca del producto: éste se define como etiqueta \<title> en el encabezado de la plantilla predeterminada.                                                          |
| $\{companyLogoUrl}                                       | La URL del logotipo de la empresa\:esta es la imagen que aparece en la plantilla predeterminada;redirecciona a una imagen en la CDN de MobileIron.                               |
| $\{message:$\{email.idp.invitation.register.your.device} | El registro del título del dispositivo del usuario.                                                                                                                              |
| $\{message:$\{email.idp.invitation.title}}               | Título de la invitación por correo electrónico.                                                                                                                                  |
| $\{message:$\{email.idp.invitation.pg1}}                 | Verificación de que el usuario está en el dispositivo.                                                                                                                           |
| $\{message:$\{email.idp.invitation.get.started}}         | El texto de introducción de la invitación por correo electrónico.                                                                                                                |
| $\{message:$\{email.idp.invitation.pg2}}                 | Instrucciones de inicio de sesión y registro.                                                                                                                                    |
| $\{message:$\{email.idp.invitation.pg3}}                 | Correo electrónico y aplicaciones insertadas en la información del dispositivo.                                                                                                  |
| $\{message:$\{email.idp.invitation.pg4}}                 | Información del registro si el usuario no está en su dispositivo, que incluye la URL de registro del clúster.                                                                    |
| $\{message:$\{email.footer}}                             | El pie de página de la invitación por correo electrónico, que incluye la etiqueta del sitio web de la empresa.                                                                   |
| $\{companyWebsiteLabel}                                  | La etiqueta del sitio web de la empresa: NOaparece en la plantilla predeterminada pero sehace referencia a ella indirectamente (a través dela variable $\{email.footer}).        |

### Variables de notificación de caducidad de la contraseña

| Variable                                               | Descripción                                                                                                                                                               |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\{passwordResetUrl}                                   | La URL para restablecer la contraseña.                                                                                                                                    |
| $\{productBrandName}                                   | El nombre de marca del producto: éste se define como etiqueta \<title> en el encabezado de la plantilla predeterminada.                                                   |
| $\{companyLogoUrl}                                     | La URL del logotipo de la empresa\:esta es la imagen que aparece en la plantilla predeterminada;redirecciona a una imagen en la CDN de MobileIron.                        |
| $\{message:$\{password.expiration.notification.title}} | El título de la notificación sobre la caducidad de la contraseña                                                                                                          |
| $\{message:$\{password.expiration.notification.pg1}}   | El párrafo introductorio de la notificación sobre la caducidad de la contraseña                                                                                           |
| $\{message:$\{email.password.reset.url.name}}          | El nombre de la URL para restablecer la contraseña                                                                                                                        |
| $\{message:$\{email.footer}}                           | El pie de página de la invitación por correo electrónico, que incluye la etiqueta del sitio web de la empresa.                                                            |
| $\{companyWebsiteLabel}                                | La etiqueta del sitio web de la empresa: NOaparece en la plantilla predeterminada pero sehace referencia a ella indirectamente (a través dela variable $\{email.footer}). |

### Variables de confirmación de registro

| **Variable**                             | **Descripción**                                                                                                                                    |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\{productBrandName}                     | El nombre de marca del producto: éste se define como etiqueta \<title> en el encabezado de la plantilla predeterminada.                            |
| $\{companyLogoUrl}                       | La URL del logotipo de la empresa\:esta es la imagen que aparece en la plantilla predeterminada;redirecciona a una imagen en la CDN de MobileIron. |
| $\{message:$\{email.confirmation.title}} | El título de la confirmación de registro.                                                                                                          |
| $\{message:$\{email.confirmation.pg1}}   | El párrafo introductorio de la confirmación de registro.                                                                                           |

### Variables de cumplimiento de políticas

| Variable                     | Descripción                                                                                                                                                                |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\{policyMessageTitle}       | Esta variable será reemplazada por el contenido que se introduce en la línea de asunto de la medida de cumplimiento del correo electrónico de envío dentro de la política. |
| $\{policyMessageContent}     | Esta variable será reemplazada por el contenido que se introduce en la parte del mensaje de la medida de cumplimiento de la política de envío de correo electrónico.       |
| $\{productBrandName}         | El nombre de marca del producto: éste se define como etiqueta \<title> en el encabezado de la plantilla predeterminada.                                                    |
| $\{companyLogoUrl}           | La URL del logotipo de la empresa\:esta es la imagen que aparece en la plantilla predeterminada;redirecciona a una imagen en la CDN de MobileIron.                         |
| $\{message:$\{email.footer}} | El pie de página de la invitación por correo electrónico, que incluye la etiqueta del sitio web de la empresa.                                                             |
| $\{companyWebsiteLabel}      | La etiqueta del sitio web de la empresa: NOaparece en la plantilla predeterminada pero sehace referencia a ella indirectamente (a través dela variable $\{email.footer}).  |

### Variables de atributos personalizados del usuario

El administrador puede usar [**atributos personalizados del usuario**](./Atributos.md) como variables de correo electrónico en la plantilla personalizada del correo electrónico en las siguientes condiciones:

- Los atributos personalizados del usuario existen en la página **Administrador > Atributos**.
