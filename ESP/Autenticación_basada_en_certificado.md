---
title: Autenticación basada en certificado
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDMes compatible con la autenticación basada en certificados que permite a los administradores iniciar sesión mediante certificados digitales y un nombre de host (vanity) especificado por el abonado. Cuando se habilita y se configura, los administradores pueden iniciar sesión utilizando los certificados digitales en lugar de la autenticación básica (nombre de usuario y contraseña).

Esta opción está desactivada de forma predeterminada. Los administradores deben contactar con la Asistencia técnica para activar esta función en su(s) abonado(s). Esta función solo está disponible en los entornos de clústeres NA3 y solo si está habilitada por la Asistencia técnica. Asegúrese de que su nombre de usuario y contraseña de superadministrador se hayan comprobado y estén preparados, ya que una vez que se habilite la autenticación basada en certificados, estas credenciales serán las únicas que puede utilizar para iniciar sesión hasta que haya configurado correctamente su dominio personalizado.

**Procedimiento**

1. En la pestaña de **Administración**, seleccione **Configuración de host de personalización**.
2. En la página de Configuración del host mnemónico, configure las siguientes opciones:

| Ajuste                                                | Qué hacer                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Crear dominio personalizado                           | Escriba el nombre del dominio mnemónico. Este es el nombre de dominio que puede alinearse más estrechamente con su identidad corporativa y al que puede acceder mediante certificados digitales.                                                                                                                                                                                                                                                                                                                                                                                      |
| Cargar los certificados de EC de emisión de confianza | Haga clic en **Seleccionar archivo** para seleccionar y cargar el certificado de EC que emite los certificados a sus administradores.Para activar la comprobación de la revocación del certificado, seleccione **Habilitar la configuración de validación del estado del certificado para este certificado** (opcional).Esta opción está activada de forma predeterminada. Deseleccione esta opción para desactivar la revocación del certificado.Haga clic en **Añadir más** para añadir más certificados.Asegúrese de que el formato del archivo sea .p7b, .pem, .der, .crt o .cer. |
| Asignación de atributos del certificado               | La asignación de atributos de certificado configura la asignación de los elementos de identidad del certificado a los atributos de la cuenta del administrador.En el campo **A partir del certificado**, seleccione cualquiera de los siguientes elementos del certificado:\* **Nombre principal de NT**                                                                                                                                                                                                                                                                              |

:::Paragraph{listStyleType="disc" indent="2"}
**Nombre RFC 822**En el campo **Para la variable**, seleccione cualquiera de los siguientes atributos de la cuenta del administrador:\* **UPN del usuario**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**$UserEmailAddress**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**$EDIPI**                                                                             |
Haga clic en **Guardar**.Pueden pasar unos minutos hasta que el host mnemónico esté accesible.
:::
