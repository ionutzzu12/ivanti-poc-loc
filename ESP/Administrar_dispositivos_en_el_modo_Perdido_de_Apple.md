---
title: Administrar dispositivos en el modo Perdido de Apple
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Activar el modo Perdido**](./Administrar_dispositivos_en_el_modo_Perdido_de_Apple.md)
- [**Realizar acciones del modo Perdido**](./Administrar_dispositivos_en_el_modo_Perdido_de_Apple.md)
- [**Desactivar el modo Perdido**](./Administrar_dispositivos_en_el_modo_Perdido_de_Apple.md)

**Aplicable a:** dispositivos iOS 10.3+ supervisados

Con Ivanti Neurons for MDM, puede poner un dispositivo supervisado en modo Perdido. Esto significa que usted comunica el dispositivo como perdido a los servidores de Apple y esto le permite recuperar la última localización registrada del dispositivo, además de desactivar el modo Perdido si encuentra el dispositivo.

## Activar el modo Perdido

Puede comunicar que ha perdido un dispositivo a los servidores de Apple poniendo el dispositivo en modo Perdido. Una vez que haya puesto el dispositivo en modo Perdido:

- Si se retira el dispositivo, no podrá desactivar el modo Perdido.
- Si se borra el dispositivo, no podrá localizar ni hacer un seguimiento del dispositivo.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Seleccione la casilla del dispositivo.
3. Seleccione **Acciones** > **Común** > **Activar Modo Perdido**.
4. También puede acceder a la página **Detalles del dispositivo** seleccionando el enlace del nombre del dispositivo. Haga clic en el icono de acción del dispositivo y seleccione **Activar modo perdido**.

## Realizar acciones del modo Perdido

Una vez se haya activado el modo Perdido, puede realizar las siguientes acciones desde la sección Modo dispositivo perdido:

- Insertar mensaje/número de teléfono en iPhone
  - Introducir un mensaje que aparecerá en la pantalla bloqueada del dispositivo perdido.
  - Introducir un número de contacto que aparecerá en la pantalla bloqueada del dispositivo perdido. Si alguien encuentra el dispositivo, podrán llamar a ese número para comunicárselo.
    Bloquear dispositivo
- **Actualizar localización del dispositivo**Si el dispositivo se ha borrado, no podrá localizarlo.
- **Reproducir sonido del modo perdido**El sonido se reproducirá hasta que el dispositivo se elimine del modo Perdido o hasta que un usuario desactive el sonido del dispositivo.
- **Actualizar localización**La opción **Actualizar ubicación** se añade a **Modo perdido** para ver la ubicación del dispositivo. Se muestran los siguientes detalles:\* **Latitud**: la latitud de la ubicación del dispositivo.
  - **Marca horaria**: se muestra la marca de fecha y hora de la carga útil.
  - **Longitud**: la longitud de la ubicación del dispositivo.

## Desactivar el modo Perdido

Si se recupera un dispositivo que estaba en modo Perdido o se habilitó el modo Perdido por error, puede desactivar el modo Perdido.

Si el dispositivo perdido se retira de Ivanti Neurons for MDM, la desactivación del modo perdido no funcionará.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Seleccione la casilla del dispositivo.
3. Seleccione **Acciones** > **Común** > **Desactivar Modo Perdido**.
4. Como alternativa, vaya a la página **Detalles del dispositivo** seleccionando el enlace del nombre del dispositivo y seleccione **Modo de dispositivo perdido: Activado** > **Desactivar Modo Perdido**.
