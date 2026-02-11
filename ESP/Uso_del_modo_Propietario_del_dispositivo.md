---
title: Uso del modo Propietario del dispositivo
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Aprovisionamiento de dispositivos Android Enterprise mediante un código QR o NFC Bump**](./Uso_del_modo_Propietario_del_dispositivo.md)
- [**Aprovisionamiento de dispositivos Android Enterprise mediante token de cliente**](./Uso_del_modo_Propietario_del_dispositivo.md)

**Licencia**: Gold

Una vez que los dispositivos se hayan registrado, los puede designar como Propiedad de la empresa o Propiedad del empleado. Esta designación ayuda a administrar las políticas basadas en si el usuario tiene un dispositivo personal o un dispositivo propiedad de la empresa. Con la licencia correcta, podrá usar la propiedad en reglas para crear grupos de dispositivos.

Empezando con un dispositivo nuevo o con el restablecimiento de los valores de fábrica, utilice la aplicación [**Provisioner**](./Configurar_la_aplicación_Provisioner.md) para aprovisionar el modo del propietario del dispositivo mediante una de las siguientes opciones:

- Intercambio de datos NFC (Near Field Communication)
- Escaneo de código QR

Para realizar el intercambio de datos NFC, es necesario que el dispositivo maestro o la plantilla entre en contacto físico con un dispositivo nuevo o con la configuración de fábrica para aprovisionarlo.

Para realizar un escaneo del código QR, es necesario pulsar la pantalla de un dispositivo nuevo o con la configuración de fábrica, configurar una red Wi-Fi y escanear el código cuando dispositivo esté listo para ser aprovisionado.

Durante el aprovisionamiento del modo propietario del dispositivo utilizando el código NFC o QR code, la aplicación Provisioner acepta un token de inscripción. En el registro, el token de inscripción se envía al servidor. Si está presente en el servidor y el dispositivo se asigna a un usuario, el dispositivo está correctamente registrado.

El cliente Go controlará el dispositivo una vez que esté en el modo Propietario del dispositivo y bloqueará la pantalla hasta que el dispositivo esté registrado con Ivanti Neurons for MDM para evitar que los usuarios salgan del proceso de aprovisionamiento. El modo Propietario del dispositivo también es compatible con el modo Kiosco. Para ver información sobre la configuración, vaya a: [**Bloqueo y configuración de kiosco**](./Bloqueo_y_kiosco__modo_de_administrador_de_dispositivos_de_Android.md).

**Importante**

- Si retira un dispositivo en el modo Propietario del dispositivo, se restablecerá la configuración de fábrica del dispositivo.
- Todos los dispositivos del modo Propietario del dispositivo pueden tener opcionalmente todas las aplicaciones del sistema habilitadas.
- Un dispositivo solo puede tener un propietario del dispositivo activo a la vez.
- Solo los dispositivos compatibles con Android Enterprise se pueden aprovisionar en modo propietario.
- Para los dispositivos Samsung KNOX Standard que estén en modo Propietario del dispositivo, se pedirá a los usuarios que activen la licencia Samsung ELM. Este aviso aparecerá también en los dispositivos Samsung que estén en modo Propietario del dispositivo cuando la aplicación de cliente Go se actualice desde una versión anterior a la versión lanzada más recientemente compatible con Ivanti Neurons for MDM. Después de la activación, se muestra el número de serie en la página de detalles del Dispositivo, que debe coincidir con el campo Dispositivo > Ajustes > Número de serie.

## Aprovisionamiento de dispositivos Android Enterprise mediante un código QR o NFC Bump

Para aprovisionar dispositivos Android Enterprise mediante código QR o NFC bump, deberá descargar e instalar la aplicación Provisioner de Google Play en el dispositivo maestro.

Componentes compatibles

Versión de Provisioner: 1.3.0.

Provisioner es compatible o funciona con lo siguiente:

| Elemento                                               | Versión                                                                                 |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| SO de Android(el dispositivo que se va a aprovisionar) | - Es necesaria la versión 5.0 o versiones más recientes compatibles, si se utiliza NFC. |

- Es necesaria la versión 7.0 o versiones más recientes compatibles si se utiliza un código QR.El dispositivo debe ser compatible con Android Enterprise. |
  \| SO de Android (en el dispositivo maestro)                    | 5.1 hasta la versión lanzada más recientemente.Para usar el intercambio de datos NFC, el dispositivo debe contar con NFC. No es necesario para el código QR.                                                                                      |
  \| Producto de servidor UEM, habilitado para Android Enterprise | Uno de los siguientes\:Ivanti Neurons for MDM, o permitir Ivanti Neurons for MDM etiquetado.                                                                                                                                                      |
  \| Aplicación del cliente Android                               | Provisioner instalará automáticamente la última versión de la aplicación del cliente en el dispositivo aprovisionado.                                                                                                                             |

**Requisitos previos**

Para aprovisionar un dispositivo de Android Enterprise para que sea un dispositivo administrado en el trabajo, debe:

- Asegúrese de que la configuración necesaria relacionada con Android Enterprise está definida y se aplicará al dispositivo registrado.
- La configuración por defecto de Android Enterprise: Work Managed Device debe estar habilitada para el dispositivo.
  Habilitar Android Enterprise en el servidor.
- Tenga un dispositivo Android compatible con NFC (solo si se va usar NFC) para que sirva como dispositivo maestro, con la aplicación Provisioner instalada.
- Disponga de dispositivos compatibles con Android Enterprise para aprovisionar.

Para habilitar la transferencia Android con el fin de usarla con el intercambio de datos NFC:

**Procedimiento**

1. Vaya a los **Ajustes** del dispositivo.
2. Vaya a **Redes > Redes inalámbricas**.
3. En la sección **Conectividad**, seleccione **Compartir y conectar**.
4. Ponga el interruptor **NFC** en **Activado (On)**.
5. Ponga el interruptor de **Transferencia Android** en **Activado (On)**.

Los pasos para activar la transferencia Android y NFC pueden variar según cada dispositivo.

## Aprovisionamiento de dispositivos de Android Enterprise para que sea un dispositivo administrado en el trabajo

**Procedimiento**

1. Utilizando el dispositivo maestro Android, descargue de Google Play la aplicación Provisioner e instálela.
2. Inicie Provisioner en el dispositivo maestro.
3. Seleccione el método de aprovisionamiento: NFC o código QR.
4. Pulse **Aplicación a aprovisionar** y elija la aplicación del cliente que va a instalar en el dispositivo aprovisionado:| Seleccione esta aplicación de cliente: | Para registrarse con este servidor UEM:       |
   \| -------------------------------------- | --------------------------------------------- |
   \| Ir                                     | Ivanti Neurons for MDM                        |
   \| En el UEM de trabajo                   | (Permitir etiquetados) Ivanti Neurons for MDM |
5. Rellene los campos restantes en la aplicación Provisioner. Algunos campos podrían autorrellenarse si existe un tipo de Wi-Fi compatible. Los campos de Wi-Fi no aparecen si se selecciona el código QR. Siga estas pautas:| Campo                                          | Valor                                                                                                                                                                                                                                                                                                            |
   \| ---------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Seleccione la aplicación que va a aprovisionar | Go o At Work                                                                                                                                                                                                                                                                                                     |
   \| Zona horaria                                   | Introduzca la zona horaria que se va configurar en el dispositivo                                                                                                                                                                                                                                                |
   \| Configuración regional                         | Introduzca la configuración regional que se va configurar en el dispositivo                                                                                                                                                                                                                                      |
   \| Activar todas las aplicaciones del sistema     | Haga clic en la casilla para activar todas las aplicaciones del sistema                                                                                                                                                                                                                                          |
   \| SSID de la red Wi-Fi                           | Introduzca la SSID de la Wi-Fi que va a usar el dispositivo de destino                                                                                                                                                                                                                                           |
   \| Tipo de seguridad Wi-Fi                        | Introduzca el tipo de seguridad Wi-Fi                                                                                                                                                                                                                                                                            |
   \| Contraseña Wi-Fi                               | Introduzca la contraseña para la Wi-Fi                                                                                                                                                                                                                                                                           |
   \| Inscripción en masa                            | La función de inscripción en masa es opcional. Para usar la inscripción en masa, es necesario un nombre de host. Opcionalmente, también se puede introducir un nombre de usuario y seleccionar la opción de inicio rápido. Para omitir la función de inscripción en masa, estos campos se deben dejar en blanco. |
6. Pulse **Continuar**.
7. Si se seleccionó **NFC**, pulse **Continuar**. La pantalla **Subir los dispositivos** aparece en el dispositivo maestro. Continúe con la sección **Intercambio de datos NFC** que aparece a continuación.
8. Si seleccionó **Código QR**, aparece la pantalla **Escanear este código QR** en el dispositivo maestro. Continúe con la sección **Código QR** que aparece a continuación.
   **Siga los siguientes pasos al para el intercambio de datos NFC**
   Confirme que el dispositivo de destino esté mostrando la pantalla de bienvenida de Android.
9. Haga «chocar» la parte posterior del dispositivo maestro con la del dispositivo destino para iniciar la transferencia NFC. Si la transferencia NFC se produce correctamente, el dispositivo de destino hará un sonido y, a continuación, comenzará a descargar la aplicación de cliente. Si no se puede establecer una conexión Wi-Fi o si el dispositivo no puede descargar la aplicación el cliente, este realizará automáticamente un restablecimiento a la configuración de fábrica.
10. Si oye un sonido o ve una pantalla que no sea la de bienvenida, puede desacoplar los dispositivos. Esto suele tardar algunos segundos. Si el dispositivo no está cifrado, comenzará el proceso de cifrado antes de continuar.
11. Puede seguir aprovisionando dispositivos adicionales «haciéndolos chocar» con el dispositivo maestro. El dispositivo de destino debe mostrar la pantalla de Bienvenida y el dispositivo maestro debe mostrar la pantalla "Subir los dispositivos".
    **Siga los siguientes pasos al para el aprovisionamiento con código QR.**
    Confirme que el dispositivo de destino esté mostrando la pantalla de bienvenida de Android.
12. Pulse la pantalla de Bienvenida de Androud en el dispositivo de destino 6 veces en el mismo punto de la pantalla.
13. Se le pedirá que configure una red Wi-Fi para que el asistente de configuración pueda descargar un lector de códigos QR en el dispositivo de destino.
14. Una vez que se haya descargado el lector de códigos QR, se habrá iniciado la cámara.
15. Sujete el dispositivo de destino algunos centímetros por encima del dispositivo maestro hasta que se haya escaneando correctamente el código QR. A continuación, el asistente de configuración procederá a descargar la aplicación del cliente. Si no puede descargar la aplicación de cliente, realizará automáticamente un restablecimiento a la configuración de fábrica.
16. Puede seguir aprovisionando dispositivos adicionales escaneando el código QR en el dispositivo maestro. El dispositivo de destino debe tener una cámara lista para escanear y el dispositivo maestro debe mostrar la pantalla "Escanee este código QR".
17. El código QR también se puede exportar pulsando el botón Compartir. Las opciones de exportación que se ofrecen variarán según el dispositivo.

## Aprovisionamiento de dispositivos Android Enterprise mediante token de cliente

Puede aprovisionar un dispositivo Android Enterprise en modo Propietario del dispositivo mediante un token de cliente de marca en lugar de utilizar los métodos de NFC bump o código QR. Este método le permite iniciar sesión en un dispositivo con un token, lo cual facilita la instalación automática del cliente Go o At Work y el aprovisionamiento en el modo Propietario del dispositivo:

Los tokens de cliente de marca son compatibles con los dispositivos aprovisionados con cuentas gestionadas de Google Play, que utilizan Android 6 o versiones más recientes compatibles. Para obtener más detalles, consulte la guía para desarrolladores de UEM de Android. [**https://developers.google.com/android/work/prov-devices#Key\_provisioning\_differences\_across\_android\_releases.**](https://developers.google.com/android/work/prov-devices#Key_provisioning_differences_across_android_releases)

Requisitos para usar este método:

- Debes estar registrado con una cuenta Android Enterprise.
- El dispositivo debe ser compatible con Android Enterprise.
- El dispositivo debe usar desde Android 6 hasta la versión lanzada más recientemente.
- Debe tener dispositivo nuevo o con la configuración de fábrica.

## Para configurarlo (para dispositivos con Android 5.0+):

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
En elIvanti Neurons for MDMportal de , vaya a **Configuraciones**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir**.
:::

:::WorkflowBlockItem
Seleccione **Bloqueo y kiosco: Android Enterprise**.
:::

:::WorkflowBlockItem
Se muestra la página **Crear configuración de bloqueo y kiosco: para Android Enterprise**.

Introduzca un nombre y descripción para la configuración.
:::

:::WorkflowBlockItem
Elija un tipo de bloqueo.

Haga clic en **Dispositivos administrados en el trabajo (Propietario del dispositivo)**.
:::

:::WorkflowBlockItem
Aparecerán las opciones de ajustes de bloqueo de Propietario del dispositivo.

Opcionalmente, también puede

- Desactivar la Wi-Fi o los ajustes de Wi-Fi
- Desactivar cámara
- Desactivar Bluetooth
- No permitir ajustes de Bluetooth
- Desactivar captura de pantalla
- Silenciar volumen principal
- No permitir el Control de aplicaciones
- No permitir credenciales
- No permitir emisiones de emergencia
- No permitir redes móviles
- No permitir tethering
- No permitir VPN
- No permitir configuración predeterminada de fábrica
- Activar protección de restablecimiento de valores de fábrica.
- Opcionalmente, puede especificar una lista de Id. de cuentas Google autorizadas (un valor entero) que pueda aprovisionar el dispositivo después del restablecimiento de fábrica o dejar el cursor sobre el icono de ayuda para ver ayuda sobre cómo recuperar Id. de cuentas autorizadas).
  No permitir Modificar cuentas
- Desactivar NFC (transferencia de salida)
- No permitir llamadas salientes
- No permitir arranque seguro
- No permitir Compartir localización
- No permitir características de depuración
- Asegurar Verify Apps
- No permitir SMS
- No permitir Silenciar micrófono
- No permitir hora automática
- No permitir zona de hora automática
- Desactivar itinerancia de datos
- No permitir suspensión de Wi-Fi
- Restringir métodos de entrada
- Restringir servicios de accesibilidad
- Desactivar transferencia de archivos USB
- Desactivar elementos multimedia externos
- Desactivar el protector de teclado (no tendrá efecto si está configurado el PIN/código de acceso)
- Mantener la pantalla encendida mientras esté conectada a la corriente
- No permitir la creación de ventanas
- Saltar consejos para el primer uso
  En la sección **Activar/desactivar aplicaciones del sistema**, puede optar opcionalmente por desactivar las siguientes aplicaciones del sistema:
:::

:::WorkflowBlockItem
| Elemento                                            | Versión                                                                                                                                                                                                                                                                                   |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Aplicaciones del sistema predefinidas**           |                                                                                                                                                                                                                                                                                           |
| **Cámara integrada**                                | Haga clic en el botón de alternar para **ENCENDER** o **APAGAR** la aplicación de Cámara integrada.                                                                                                                                                                                       |
| **Teléfono integrado**                              | Haga clic en el botón de alternar para **ENCENDER** o **APAGAR** la aplicación de Teléfono integrada.                                                                                                                                                                                     |
| **Nombre del paquete de la aplicación del sistema** | Para activar o desactivar cualquier otra aplicación del sistema que no sean las aplicaciones del sistema predefinidas, haga clic en el icono + (más) y añada el nombre del paquete de aplicaciones del sistema. Para eliminar la aplicación del sistema, haga clic en el icono - (menos). |
| También puede elegir habilitar el **Modo kiosco**.  |                                                                                                                                                                                                                                                                                           |

Aparecerán los siguientes ajustes:

- Activar el modo de Bloqueo de tarea
- Entrar en el modo kiosko automáticamente (solo en la configuración inicial)
- Desactivar los ajustes rápidos
- Permitir al usuario acceder a los ajustes Wi-Fi
- Permitir al usuario acceder a los ajustes Bluetooth
- Permitir al usuario acceder a los ajustes de localización
- Permitir al usuario retrasar las actualizaciones de la aplicación
- Permitir al usuario acceder a los ajustes de fecha y hora
- Permitir al usuario acceder a los ajustes de red móvil
- Permitir al usuario seleccionar el idioma
- Activar dispositivo compartido (seleccione cualquiera de las siguientes opciones)
  - Activar inicio de sesión
  - Activar cierre de sesión (proporcione el ajuste de tiempo de espera por inactividad en horas)
    Opcionalmente, seleccione las opciones de imagen de marca personalizada o predeterminada de la lista desplegable.
:::

:::WorkflowBlockItem
También puede crear un PIN de salida del kiosco para salir del modo kiosco.
:::

:::WorkflowBlockItem
También puede crear una lista de permitidos de aplicaciones que estarán disponibles para los usuarios en el modo kiosco.
:::
::::

## Aprovisionar el dispositivo

**Procedimiento**

1. Encienda el dispositivo e introduzca su contraseña Wi-Fi. Es posible que su dispositivo le solicite una contraseña diferente.
2. En la pantalla **Verificar cuenta** introduzca el token de Android Enterprise. Haga clic en **Siguiente**.
3. En la pantalla **Servicios de Google**, haga clic en **Instalar**.
4. Acepte de los Términos y condiciones.
5. En la pantalla Configurar dispositivo de trabajo, haga clic en **Siguiente**. Se descargará el cliente Go o At Work y se instalará en el dispositivo. Ahora, el dispositivo entrará en modo Propietario del dispositivo.

**Temas relacionados**

- [**Uso de la inscripción en masa para Android**](./Uso_de_la_inscripción_en_masa_para_Android.md)
