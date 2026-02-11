---
title: Uso de la Inscripción en masa para dispositivos Windows
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

La función de registro en bloque le permite registrar rápidamente múltiples dispositivos Windows con Ivanti Neurons for MDM.

**Requisitos previos:**

- Las cuentas de usuario deben importarse en Ivanti Neurons for MDM utilizando Entra ID (Entra ID) Cuenta Premium.
- Todos los dispositivos deben tener instalado [**Windows Configuration Designer**](https://docs.microsoft.com/en-us/windows/configuration/provisioning-packages/provisioning-install-icd).

**Procedimiento:**

::::WorkflowBlock
:::WorkflowBlockItem
Enlace el Ivanti Neurons for MDM y los abonados de Entra ID. Consulte [**Conexión de Entra ID a UEM para dispositivos Windows 10.**](./Uso_de_Microsoft_Azure.md)
:::

:::WorkflowBlockItem
Abra la aplicación de **Windows Configuration Designer** y seleccione **Aprovisionar dispositivos de escritorio**. Aparece una nueva ventana de proyecto en la pantalla.
:::

:::WorkflowBlockItem
Ingrese los siguientes detalles:
:::

:::WorkflowBlockItem
- Nombre: un nombre único para su proyecto
- Carpeta de proyecto: ubicación del dispositivo donde desee guardar el proyecto
- Descripción: descripción opcional del proyecto
  Haga clic en **Finalizar** para cerrar la ventana del nuevo proyecto y lleve a cabo una secuencia de pasos.
:::

:::WorkflowBlockItem
**Ajuste del dispositivo**

Introduzca un nombre único para sus dispositivos. El nombre puede incluir un número de serie (%SERIAL%) o un conjunto aleatorio de caracteres.
:::

:::WorkflowBlockItem
También puede introducir una clave de producto si va a actualizar Windows, si va a configurar el dispositivo para un uso compartido o si va a eliminar un software preinstalado.
:::

:::WorkflowBlockItem
**Ajuste de la red**

Además, puede configurar la red Wi-Fi a la que se conectarán los dispositivos la primera vez que se inicien. Si los dispositivos de red no están configurados, será necesaria una conexión de red con cable la primera vez que se inicie el dispositivo.
:::

:::WorkflowBlockItem
**Gestión de la cuenta**

Seleccione **Inscribir en Entra ID**, introduzca una fecha de caducidad **Caducidad masiva de Token** y, a continuación, haga clic en **Obtener token en masa**.
:::

:::WorkflowBlockItem
Introduzca sus credenciales de Entra ID para obtener un token masivo.
:::

:::WorkflowBlockItem
En la página **Mantener la sesión en todas las aplicaciones**, haga clic en **No, iniciar sesión solo en esta aplicación**.
:::

:::WorkflowBlockItem
- Haga clic en Siguiente cuando se obtenga correctamente el Token en masa y cree el paquete.
- Se crea un usuario con un paquete de aprovisionamiento en el portal de Azure: nombre principal del usuario (like [**package\_0ea893a5-1e93-4d21-a6b1-dc788946fd1d@miwinqe.onmicrosoft.com**](mailto\:package_0ea893a5-1e93-4d21-a6b1-dc788946fd1d@miwinqe.onmicrosoft.com)). Copie el archivo (herramienta ppkg de tiempo de ejecución) en un dispositivo de almacenamiento.
  El usuario Entra ID para crear el token masivo, y el usuario del paquete no deben tener MFA activado. Para verificarlo, debe realizar la unión OOBE + Entra ID en ese usuario.

Recree o sincronice el usuario del paquete (creado en Azure) para Ivanti Neurons for MDM.
:::
::::

Inscriba en masa un dispositivo con una unidad flash dentro del paquete de aprovisionamiento. También puede hacer doble clic en el dispositivo existente para llevar a cabo la experiencia posterior a OOBE. Si el paquete no se instaló correctamente en el primer intento, el segundo intento también fallará. Compruebe si el nuevo dispositivo se ha creado en Ivanti Neurons for MDM y Entra ID pertenece al usuario del paquete.
