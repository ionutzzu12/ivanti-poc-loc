---
title: Configurar la aplicación Provisioner
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Requisitos de aprovisionamiento**](./Configurar_la_aplicación_Provisioner.md)
- [**Habilitar la transferencia Android para que use el intercambio de datos NFC**](./Configurar_la_aplicación_Provisioner.md)
- [**Aprovisionar un dispositivo propiedad de la empresa**](./Configurar_la_aplicación_Provisioner.md)
- [**Registrar el dispositivo**](./Configurar_la_aplicación_Provisioner.md)
- [**Verificar el estado del registro del dispositivo**](./Configurar_la_aplicación_Provisioner.md)

Proveedor es una aplicación de Ivanti Neurons for MDM que se usa para aprovisionar los dispositivos de empresa para que se puedan registrar como dispositivos administrados del trabajo y ubicados en el modo Propietario del dispositivos.  

Los dispositivos propiedad de la empresa solo tienen perfil corporativo y no tienen perfil profesional. El administrador puede establecer más de 20 bloqueos en el dispositivo, que pueden restringir funciones del dispositivo como la cámara, llamadas de teléfono, SMS, redes, etc.

La aplicación Proveedor es necesaria en el dispositivo que iniciará la configuración del dispositivo de destino de Android Enterprise con separador NFC. Para aprovisionar dispositivos propiedad de la empresa, instale la aplicación Provisioner en un dispositivo maestro y utilice la opción de intercambio de datos NFC (transmisión de datos en proximidad) para aprovisionar los dispositivos nuevos. La función de intercambio de datos está conectando los dos dispositivos. Los dispositivos se pueden aprovisionar para usarse en una de estas aplicaciones del cliente:

- Go para usar con Ivanti Neurons for MDM
- At Work UEM, una aplicación de cliente sin marca, para usar con Ivanti Neurons for MDM.

## Requisitos de aprovisionamiento

Para aprovisionar un dispositivo con la versión corporativa de Android y que sea un dispositivo administrado en el trabajo:

- Los dispositivos compatibles con Android Enterprise nativo propiedad de la empresa se deben restablecer a sus valores de fábrica antes del aprovisionamiento.
- La configuración de Android Enterprise se debe definir y aplicar en el grupo de dispositivos de Android.
- Un dispositivo Android compatible con NFC designado para servir como dispositivo maestro o como plantilla, con la aplicación Provisioner instalada.
- Dispositivos compatibles con Android Enterprise que se van a aprovisionar.
- Aplicación ProvisionerDescargue la aplicación Provisioner para Android de Google Play.

## Habilitar la transferencia Android para que use el intercambio de datos NFC

**Procedimiento**

1. Vaya a los **Ajustes** del dispositivo.
2. Vaya a **Redes inalámbricas y redes** y haga clic en **Más**.
3. Seleccione la casilla **NFC**.
4. Haga clic en **Transferencia Android** y deslice el interruptor a **On (Activado)**.

Estos pasos pueden variar ligeramente para su dispositivo.

## Aprovisionar un dispositivo propiedad de la empresa

**Procedimiento**

1. Instale la aplicación Provisioner en el dispositivo para usarla como dispositivo Android maestro.
2. Inicie Provisioner en el dispositivo maestro.
3. Seleccione una aplicación del menú desplegable.
4. Introduzca la información solicitada por la aplicación Provisioner. Algunos campos podrían autorrellenarse si existe un tipo de Wi-Fi compatible. Siga estas pautas:| **Campo**                                      | **Valor**                                                                                                                                                               |
   \| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Seleccione la aplicación que va a aprovisionar | Vaya a (seleccionar para usar con Ivanti Neurons for MDM)At Work UEM (aplicación de cliente sin marca; seleccionar para utilizar con Ivanti Neurons for MDM con marca). |
   \| SSID de la red Wi-Fi                           | Introduzca la SSID de la Wi-Fi que va a usar el dispositivo maestro.                                                                                                    |
   \| Tipo de seguridad Wi-Fi                        | Introduzca el tipo de seguridad Wi-Fi                                                                                                                                   |
   \| Contraseña Wi-Fi                               | Introduzca la contraseña para la Wi-Fi                                                                                                                                  |
   \| Zona horaria                                   | Introduzca la zona horaria local actual                                                                                                                                 |
   \| Configuración regional                         | Introduzca la configuración regional                                                                                                                                    |
5. Haga clic en **Continuar**.Se mostrará la pantalla **Conectar los dispositivos&#x20;**&#x65;n el dispositivo maestro.
6. Con el dispositivo de destino encendido y mostrando la pantalla de Bienvenida de Android, presione la parte posterior del dispositivo maestro contra la parte posterior del dispositivo de destino para iniciar la transferencia NFC.Si la transferencia NFC se produce correctamente, el dispositivo de destino hará un sonido y, a continuación, comenzará a descargar la aplicación de cliente elegida. Si el dispositivo no está cifrado, comenzará el proceso de cifrado antes de continuar.
7. Siga aprovisionando dispositivos adicionales intercambiando datos en los dispositivos. El dispositivo de destino debe mostrar la pantalla de Bienvenida y el dispositivo maestro debe mostrar la pantalla **Intercambio de datos en dispositivos**.

## Registrar el dispositivo

Una vez que el dispositivo propiedad de la empresa se ha aprovisionado mediante el intercambio de datos NFC, tendrá instalada la aplicación de cliente seleccionada. Inicie la aplicación de cliente y registre el dispositivo.

## Verificar el estado del registro del dispositivo

**Procedimiento**

1. Vaya a **Dispositivos > Dispositivos**.
2. Haga clic en el vínculo del dispositivo para ver los detalles.
3. El estado del dispositivo aparece en el panel izquierdo.
