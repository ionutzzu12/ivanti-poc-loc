---
title: Inscripción de paquete de aprovisionamiento con PIN
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

El administrador puede inscribir los dispositivos administrados por SCCM o Ivanti Endpoint Manager a Ivanti Neurons for MDM. La herramienta Paquete de despliegue permite a las organizaciones simplificar la transición de los dispositivos de Windows a Ivanti Neurons for MDM Modern Management, sin tiempo de inactividad ni interrupción para el usuario final. La transición sin fisuras se archiva mediante la descarga de un único paquete de despliegue desde la consola de Ivanti Neurons for MDM, a continuación, se despliega a través de la herramienta de administración o del dominio existente. Una vez que se ejecuta el paquete, inscribirá silenciosamente el punto final en Ivanti Neurons for MDM para la administración continua. El enfoque permite a los administradores primero migrar fácilmente los dispositivos y luego tener la flexibilidad de configurar los dispositivos más tarde de forma inalámbrica. Cuando un dispositivo completa la inscripción silenciosa en Ivanti Neurons for MDM, se une a MDM y es coadministrado por las dos autoridades de administración. Una vez que un administrador ha configurado la experiencia de Windows deseada dentro de Ivanti Neurons for MDM, la plataforma de administración heredada se puede retirar, dejando Ivanti Neurons for MDM como la única autoridad de administración del dispositivo.

Hay una excepción a esta regla si un dispositivo va a transicionar de Microsoft Endpoint Manager (MEM) o era anteriormente SCCM. El Cliente MEM existente continuará funcionando en Modo de Coexistencia (opuesto al modo de Co-Administración), hasta que la plataforma MEM sea desmantelada. Cuando está habilitado el Modo de coexistencia, el cliente de MEM deshabilita automáticamente determinadas funciones en favor de que Ivanti Neurons for MDM proporcione esas cargas de trabajo. Para obtener más información, consulte la [**documentación de coexistencia de Microsoft**](https://docs.microsoft.com/en-us/mem/configmgr/comanage/coexistence/).

Para obtener información sobre comportamientos más exactos al usar MEM y otras plataformas de administración de terceros, Ivanti sugiere probar primero la herramienta Paquete de implementación de Ivanti Neurons for MDMen su entorno.

**Requisitos previos**

- Las cuentas de usuario deben importarse en Ivanti Neurons for MDM mediante LDAP, Entra ID (Entra ID), carga local de usuarios u otras integraciones de identidad.
- Todos los dispositivos deben tener instalado [**Windows Configuration Designer**](https://docs.microsoft.com/en-us/windows/configuration/provisioning-packages/provisioning-install-icd).
- Habilitar el registro basado en PIN en Ivanti Neurons for MDM
- Los usuarios no deben tener espacios en su nombre de usuario, esto podría provocar el fallo de la transición del dispositivo del usuario.
- Esta herramienta puede desplegarse en entornos que no aprovechan Entra ID.
- Los elementos principales de Ivanti Neurons for MDM Modern Windows Management Suite no requieren Entra ID. Para evitar el impacto durante la transición, es posible que la coadministración o coexistencia requieran el despliegue de determinadas cargas de trabajo / configuraciones en la inscripción en segundo plano.
- Actualmente, el paquete de despliegue únicamente es compatible con SCCM e Ivanti Endpoint Manager.

**Procedimiento**

1. Vaya a **Administrador>Windows>Paquete de despliegue**.
2. Seleccione el **Usuario** o los **Grupos de usuarios** para generar los PIN y haga clic en **Descargar paquete de implementación** (archivo .zip).
3. El paquete de despliegue se proporciona a los administradores de SCCM / Ivanti Endpoint Manager para que lo extraigan y transfieran los archivos a sus respectivos dispositivos administrados por estos administradores. Para obtener información sobre cómo llevar a cabo este paso, consulte [**Paquetes y programas en Administrador de la configuración**](https://docs.microsoft.com/en-us/mem/configmgr/apps/deploy-use/packages-and-programs).
4. Después de la transferencia, los administradores desencadenan de manera remota la secuencia de comandos de setup.ps1 enlos dispositivos. Para obtener información sobre cómo desencadenar la secuencia de comandos, consulte [**Crear y desplegar secuencias de comandos desde el Administrador de configuración**](https://docs.microsoft.com/en-us/mem/configmgr/apps/deploy-use/create-deploy-scripts).
5. Los dispositivos se inscriben en Ivanti Neurons for MDM.

- El PIN generado para los usuarios es válido solo por 24 horas. Una vez que el PIN caduca, se debe generar un nuevo PIN.
- El archivo que contiene los PIN se elimina del dispositivo después de completar el intento de inscripción.

### Inscribir dispositivos de SCCM a Ivanti Neurons for MDM

**Procedimiento**

1. Descargue todos los archivos relacionados con el despliegue desde Ivanti Neurons for MDM para los usuarios seleccionados.
2. Seleccione las cuentas o grupos que se deberán inscribir.
3. Desplegar archivos del paquete en los dispositivos del cliente mediante SCCM:1) Verifique si los clientes necesarios están presentes en SCCM. Si el diseñador de configuración de Windows no se encuentra en el cliente, el administrador deberá enviar el diseñador y desplegarlo en el cliente.
   2\) En el servidor SCCM, cree una carpeta y copie el archivo zip de despliegue y extraiga el contenido del archivo.
   3\) Cree un archivo .bat que copie el contenido de la carpeta donde se extraen los archivos en el dispositivo del cliente.
   4\) En SCCM, vaya a **Biblioteca de Software > Administración de aplicaciones > Paquetes** y cree un paquete para copiar el contenido de la carpeta en el cliente. Introduzca la carpeta de destino en la que desee copiar el contenido.
   5\) Desplegar el paquete en el dispositivo o la ubicación del dispositivo.
   6\) En la sección Monitorización puede monitorizar el estado de despliegue y confirmar que los archivos se copian en la carpeta de destino del cliente.
4. Ejecute la secuencia de comandos para inscribir un dispositivo:1) Vaya a **Biblioteca de Software > Secuencias de comandos** y cree una secuencia de comandos.
   2\) Introduzca un nombre para la secuencia de comandos y importe la secuencia de comandos de PowerShell **setup.ps1** desde la carpeta descomprimida.
   3\) Aprobar la secuencia de comandos y ejecutarla en el dispositivo de destino.
   4\) Seleccione **Iniciar ahora** y haga clic en **Guardar**. Las tareas programadas empiezan a ejecutar la secuencia de comandos. Si la ejecución es correcta, el estado se volverá Verde.
5. Para verificar la inscripción del dispositivo, **Ajustes** > **Agregue o elimine un paquete de aprovisionamiento** > **Detalles**.

### Inscripción de dispositivos de Ivanti Endpoint Manager en Ivanti Neurons for MDM

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Descargue todos los archivos relacionados con el despliegue desde Ivanti Neurons for MDM para los usuarios seleccionados.
:::

:::WorkflowBlockItem
Seleccione las cuentas o grupos que se deberán inscribir.
:::

:::WorkflowBlockItem
**Caso 1**: se tiene en cuenta un nombre de dispositivo para inscribirlo con el mismo nombre de usuario. En este caso, la dirección de correo electrónico no es una dirección de usuario correcta. Como dirección de correo de inscripción se utiliza un correo electrónico con el nombre del dispositivo concatenado con el dominio de AD. El administrador debe ajustar la Cuenta como LocalSystemAccount y usar setup.ps1 como archivo principal para iniciar la ejecución de PowerShell.

**Caso 2**: se tiene en cuenta una dirección de correo electrónico de usuario para inscribir el dispositivo y no hay restricciones para modificar los archivos en la ubicación del dispositivo. Utilice la dirección de correo electrónico del usuario de la sesión activa para la inscripción. Para habilitar esta inscripción, el administrador debe ajustar la Cuenta como Cuenta de usuario actual y usar setup.ps1 como archivo principal para iniciar la ejecución de PowerShell.

**Caso 3**: se tiene en cuenta una dirección de correo electrónico válida para inscribir el dispositivo con restricciones para modificar los archivos en la ubicación del dispositivo. Utilice la dirección de correo electrónico de la sesión activa para la inscripción. Este caso tiene dos subcasos: 

- Usar dos o más secuencias de comandos para la inscripción: cree un paquete de distribución con **setupEPMCopyContentsToTempFolderStep1.ps1** y ejecútelo como Cuenta de usuario actual. Los archivos se copian en una ubicación temporal: Cree otro paquete de distribución **setupEPMCopyContentsToTempFolderStep2.ps1** y ejecútelo como Cuenta del sistema local.
- Si el usuario del dispositivo tiene restricciones para modificar la carpeta que contiene los archivos del paquete, copie los archivos en una carpeta temporal, compruebe la id del usuario y cree un paquete de PowerShell. El paquete de PowerShell se ejecuta con el script **setupEPMCopyContentsToTempFolderStep2.ps1**. Después de la instalación, se eliminará la carpeta temporal.
  Deshabilitar/Habilitar UAC
  1. Actualizar la entrada de registro para deshabilitar el control de UAC y reiniciar el equipo
  2. Ejecute el paquete de PowerShell como cuenta del Cliente actual y usando setup.ps1
  3. Actualizar la entrada de registro para habilitar el control de UAC y reiniciar el equipo

Crear paquete de PowerShell:1) Verifique si los clientes necesarios están presentes en el Administrador de puntos terminales.
2\) Copie los archivos en C:\Program Files\LANDesk\ManagementSuite\LANDesk\files\\. Cree una subcarpeta en esta carpeta y extraiga los archivos.
3\) Crear un paquete: **Distribución > Paquetes de distribución > Nuevo > Windows > PowerShell**.El administrador puede distribuir los paquetes a distintos dispositivos basándose en el nivel de restricciones que tengan ajustados los dispositivos.
4\) En la sección Archivo principal, introduzca el nombre del paquete y cargue setup.ps1 desde la carpeta donde se han copiado los archivos
5\) En la sección Archivos adicionales, copie los archivos restantes (menos la secuencia de comandos setup.ps1) mediante **Agregar**.
6\) Seleccione la cuenta del usuario actual en la sección Cuentas.
7\) Haga clic en **Guardar**.
:::

:::WorkflowBlockItem
Crear tarea programada:1) Seleccione el paquete creado, haga clic con el botón derecho y seleccione **Crear tareas programadas**. Se crea una tarea programada.
2\) Arrastre el dispositivo y agréguelo a la sección del paquete programado.
3\) En el Paquete programado, haga clic con el botón derecho y seleccione **Propiedades**.
4\) Verifique el paquete.
5\) En Tipo de tarea, seleccione **Enviar**.
6\) Seleccione **Iniciar ahora** y haga clic en **Guardar**. Las tareas programadas empiezan a ejecutar la secuencia de comandos. Si la ejecución es correcta, el estado se volverá Verde.
:::

:::WorkflowBlockItem
Para verificar la inscripción del dispositivo, **Ajustes** > **Agregue o elimine un paquete de aprovisionamiento** > **Detalles**. Como alternativa, el administrador puede verificar la inscripción de un dispositivo en los Registros de diagnóstico del dispositivo.
:::
::::
