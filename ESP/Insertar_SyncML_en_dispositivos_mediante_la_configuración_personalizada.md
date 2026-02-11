---
title: Insertar SyncML en dispositivos mediante la configuración personalizada
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Puede crear sus propios archivos de configuración de idioma de marcado de sincronización (SyncML, Synchronization Markup Language) u obtenerlos de un tercero para implementar características personalizadas añadiéndolas a una configuración personalizada.

Plataformas compatibles:

- Windows

**Dispositivos compatibles:**

- Windows 10+
- Microsoft HoloLens 2

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Haga clic en **Configuración personalizada&#x20;**&#x70;ara visualizar la página **Crear configuración personalizada**.
4. Introduzca un nombre para la configuración.
5. Haga clic en el icono del SO Windows.
6. Arrastre y suelte el archivo SyncML en la interfaz o haga clic en **Elegir archivo** para navegar hasta el archivo que va a seleccionar para cargar el dispositivo.Ivanti Neurons for MDM no realiza verificaciones de validación en el código del archivo.
7. Haga clic en **Siguiente**.

**Registro personalizado de SyncML**

Los comandos de SyncML que se envían al dispositivo de Windows y las respuestas de SyncML de estos comandos desde el dispositivo se pueden ver en la pestaña Registros de dispositivos. Esta información de registro estará disponible después de enviar la configuración de **SyncML personalizada de Windows**. Cuando el sistema envía una configuración personalizada de SyncML, tiene el estado "Instalado" siempre en la pestaña "Configuración" del dispositivo para su configuración, independientemente de las respuestas de SyncML.
