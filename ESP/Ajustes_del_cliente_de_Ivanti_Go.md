---
title: Ajustes del cliente de Ivanti Go
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

Configure la recopilación de datos anónimos de los usuarios finales, incluyendo información sobre el dispositivo y su uso, para ayudar a identificar problemas del producto y garantizar una alta calidad del servicio. Esta configuración también habilita las opciones de configuración del contacto de soporte.

**Aplicable a:**

- Mobile\@Work para macOS 1.67 o versiones más recientes compatibles.
- Go para iOS 3.5.0 o las versiones más recientes compatibles.

## Crear una configuración de Ajustes del cliente de Ivanti Go

**Procedimiento**

1. Vaya a **Configuraciones** > **Agregar configuración** > **Ajustes del cliente de Ivanti Go**. Aparece la página **Crear configuración de ajustes del cliente de Ivanti Go**.
2. Introduzca un nombre para la configuración en el cuadro **Nombre**.
3. Introduzca una **Descripción** de la configuración.
4. En **Activaciones basadas en la ubicación**, seleccione la opción **Habilitar SLC**. El servicio de cambio significativo de localización ofrece una alternativa más ahorrativas para instalar actualizaciones de localización en la aplicación Go para iOS solo cuando la posición del usuario cambie considerablemente, después de 15 minutos como mínimo (intervalo predeterminado). Si este servicio está activado, al cambiar la localización la aplicación Go se activa en segundo plano y efectúa un ingreso.
5. En **Recolección de datos mediante análisis para clientes**, seleccione la opción **Habilitar análisis** si esta se encuentra deshabilitada. De forma predeterminada, esta opción está activada.
6. Haga clic en **Siguiente** para configurar los ajustes de distribución.
7. Haga clic en **Listo**.

## Configure la pestaña Ajuste para soporte

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuraciones** > **Agregar configuración** > **Ajustes del cliente de Ivanti Go**. Aparece la página **Crear configuración de ajustes del cliente de Ivanti Go**.
:::

:::WorkflowBlockItem
Introduzca un nombre para la configuración en el cuadro **Nombre**.
:::

:::WorkflowBlockItem
Introduzca una **Descripción** de la configuración.
:::

:::WorkflowBlockItem
En la sección **Configurar la pestaña Ajustes para soporte**, haga clic en **Activar la pestaña Soporte**.
:::

:::WorkflowBlockItem
Asegúrese de que la versión del cliente Ivanti Go sea la 118.0.0 o superior para habilitar la pestaña de Soporte.Los dispositivos con versiones anteriores no se mostrarán ni serán compatibles con esta función.

En la sección **Configuración de Contacto de Soporte**, proporcione los siguientes detalles:\* **Nombre de pestaña**: introduzca el nombre de la pestaña que se muestra en la navegación de aplicaciones de Ivanti. El valor por defecto es "Soporte". (Longitud máxima: 10 caracteres)

- **Instrucciones para el usuario final**: introduzca las instrucciones sobre cómo usar los contactos de soporte. (Longitud máxima: 40 caracteres)
- **Elegir el número de contactos**: selecciona el número de contactos en el menú desplegable. Por defecto es 1 (Números máximos: 5)\* **Introducir el nombre del campo**: introducir el nombre del contacto. (Longitud máxima: 20 caracteres)
  - **Introducir número de teléfono**: introduzca un número de teléfono válido. (Longitud máxima: 10 caracteres)
:::

:::WorkflowBlockItem
- **Dirección de correo electrónico**: introduzca el correo electrónico donde desee enviar los correos de soporte. (Longitud máxima: 40 caracteres)Debe introducir una dirección de correo electrónico válida con formato [**alias@nombrededominio.com**](mailto\:alias@nombrededominio.com)
- **Elegir el número de URL**: selecciona el número de URL en el menú desplegable. Por defecto es 1. (Números máximos: 5)\* **Introducir el nombre del campo**: introducir el nombre de la URL. (Longitud máxima: 20 caracteres)
  - **Introducir URL**: introduzca una URL válida. (Longitud máxima: 20 caracteres)
- **Información adicional**: introduzca cualquier mensaje relacionado con soporte técnico adicional que desee que se muestre aquí. (Longitud máxima: 120 caracteres)
  Haga clic en **Siguiente** para configurar los ajustes de distribución.
:::

:::WorkflowBlockItem
Haga clic en **Listo**.
:::
::::
