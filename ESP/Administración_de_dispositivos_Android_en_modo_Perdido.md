---
title: Administración de dispositivos Android en modo Perdido
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Activar el modo Perdido**](./Administración_de_dispositivos_Android_en_modo_Perdido.md)
- [**Desactivar el modo Perdido**](./Administración_de_dispositivos_Android_en_modo_Perdido.md)

## Activar el modo Perdido

**Aplicable a:** dispositivos Android 8+

Puede colocar múltiples dispositivos Android simultáneamente en modo Perdido a través de Ivanti Neurons for MDM. Esto significa que puede informar de un dispositivo perdido a Ivanti Neurons for MDM colocando los dispositivos en modo Perdido, lo que le permite mostrar un mensaje personalizado, número de teléfono y nota al pie de página en la pantalla, junto con una opción para reproducir un sonido.

Esta función solo es compatible con los dispositivos totalmente gestionados, incluidos los dispositivos no GMS.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Seleccione la casilla de los dispositivos.
3. Seleccione **Acciones > Activar modo perdido**.
4. Alternativamente, también puede hacer clic en el enlace del nombre del dispositivo para ir a la página de detalles del Dispositivo y hacer clic en el icono

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt="width: 40px;height: 27px;" isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
. Seleccione **Activar modo perdido**.
:::

5. Introduzca un mensaje en la pantalla de bloqueo o un número de teléfono, o ambos, para que aparezca en la pantalla de bloqueo del dispositivo o dispositivos perdidos. Los administradores también pueden seleccionar la nota al pie y las opciones **Reproducir sonido en modo perdido**. Si alguien encuentra los dispositivos, podrán llamar a ese número para comunicárselo.Se debe introducir un mensaje o un número de teléfono en los campos respectivos para activar la opción **Activar modo perdido**.El sonido del Modo Perdido se reproducirá durante 5 minutos a menos que el teléfono se desbloquee, se pulse el botón de llamada o el Administrador desactive el Modo Perdido dentro de ese tiempo. Para reproducir un sonido, vuelva a activar el Modo Perdido en los dispositivos.
6. Seleccione **Activar el modo Perdido** para colocar los dispositivos Android en modo Perdido.

La activación del modo perdido deshabilitará las acciones siguientes:

- Desbloquear
- Entrar/Salir de kiosco
- Fuerza inicio de sesión para el kiosco compartido
- Asignar al usuario
- Enviar mensaje
- Establecer propiedad

Una vez que se activa el modo Perdido en un dispositivo, se desactivará la opción del modo Perdido en el servidor.

## Desactivar el modo Perdido

Si se recupera un dispositivo en modo Perdido o el modo Perdido se activó por error, puede desactivarlo.

Si los dispositivos perdidos se borran de Ivanti Neurons for MDM, no funcionará la desactivación del Modo perdido.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Seleccione la casilla de los dispositivos.
3. Seleccione **Acciones > Desactivar modo perdido**.
4. También puede hacer clic en el enlace del nombre del dispositivo para ir a la página de detalles del dispositivo y seleccionar **Modo dispositivo perdido: Activado > Desactivar Modo Perdido**.

En la sección **Detalles**, **Desactivar modo perdido** se vuelve visible solo después de activar **Activar modo perdido**. Una vez activado **Desactivar modo perdido**, desaparece el campo **Modo dispositivo perdido: Activado**, que incluye la opción **Desactivar Modo Perdido**.

Los dispositivos que estaban previamente en Modo Kiosko tendrán que volver a entrar en Kiosko después de desactivar el modo Perdido.
