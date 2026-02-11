---
title: Inscripción basada en cuentas
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Esta sección es aplicable a las inscripciones de Usuarios controlados por cuentas y Dispositivos controlados por cuentas.

**Dispositivos compatibles**

- Dispositivos con iOS 15+ (para la inscripción de usuarios controlada por cuenta) e iOS17+ (para la inscripción de dispositivos controlada por cuenta)
- Dispositivos con macOS 14+
- Dispositivos con visionOS 1.1+

**Requisitos previos:**

**Para la inscripción de usuarios basada en cuentas**

- Una cuenta de usuario de Ivanti Neurons for MDM con ID de Apple gestionado (usuarios en Apple Business Manager o Apple School Manager).
- En la sección **Inscripción de Apple**, seleccione **Inscripción de usuarios** de la lista desplegable **Seleccionar el tipo de inscripción de Apple**.
- En **Usuarios** -> **Configuración de usuario** -> establezca la **Configuración del propietario del dispositivo** en **ACTIVO** > seleccione la opción **Propiedad del usuario**.

**Inscripción de dispositivo generada por cuentas**

- Una cuenta de usuario en Ivanti Neurons for MDM con ID de Apple gestionado (usuarios en Apple Business Manager o Apple School Manager).
- En la sección **Inscripción de Apple**, seleccione **Inscripción de dispositivos** en la lista desplegable **Seleccionar tipo de inscripción de Apple**.
- En **Usuarios** -> **Configuración de usuario** -> configure **Configuración del propietario del dispositivo** en **ACTIVO** > seleccione la opción **Propiedad de la empresa**.

**Inscripción de usuarios basada en cuentas** para dispositivos iOS 15+, macOS 14+ y visionOS 1.1+ es una opción de inscripción diseñada para empresas que implementan BYOD (Traiga su propio dispositivo). La Inscripción de Usuario generada por cuenta es una versión modificada del protocolo MDM y la Inscripción de Usuarios con Apple Business Manager con un enfoque mucho mayor sobre la privacidad del usuario, implementada con el nivel de seguridad que las empresas necesitan.

**Inscripción de dispositivos basada en cuentas** para dispositivos iOS 17+, macOS 14+ y visionOS 1.1+ es una opción de inscripción diseñada para que las empresas inscriban dispositivos propiedad de la empresa / corporativos. La inscripción de dispositivos basada en cuentas aprovecha el protocolo MDM e Inscripción de dispositivos con Apple Business Manager con un enfoque mucho mayor en la privacidad del usuario, implementado con un nivel de seguridad que las empresas necesitan. Los usuarios finales pueden inscribir sus dispositivos mediante la función Cuenta de trabajo en Configuración.

## Configurar el servicio de localización

Si su empresa tiene un nombre de dominio de empresa, por ejemplo, acme.com, la ID de correo electrónico para su dispositivo es [**nombrededispositivo@acme.com**](mailto\:nombrededispositivo@acme.com).

1. El usuario introduce [**username@acme.com**](mailto\:username@acme.com) para iniciar sesión en su cuenta del trabajo o de la escuela y, a continuación, el dispositivo realiza una llamada de solicitud HTTP GET a la URL:[**https://acme.com/.well-known/com.apple.remotemanagement?user-identifier=user@acme.comPara**](https://acme.com/.well-known/com.apple.remotemanagement?user-identifier=user@acme.comPara) más información, consulte: [**https://developer.apple.com/documentation/devicemanagement/discover\_authentication\_servers**](https://developer.apple.com/documentation/devicemanagement/discover_authentication_servers)
2. En el dominio acme.com, configure la regla de redirección para el URI - /.well-known/com.apple.remotemanagement para redirigirlo a la siguiente URL\:https\://\<n-MDM cluster>/.well-known/com.apple.remotemanagement

## Detección de servicio simplificado para la inscripción de dispositivos impulsados ​​por la cuenta

Aplicable a iOS 18.2+, macOS 15.2+ y dispositivos VisionOS 2.2+.

Para la inscripción impulsada por la cuenta, cuando un usuario introduce al correo electrónico de su empresa para iniciar sesión en su cuenta laboral o escolar, el dispositivo primero busca un recurso HTTP conocido en el dominio de la organización, que contiene un enlace a la URL de inscripción de MDM.

**Procedimiento**

1. Iniciar sesión en la cuenta de trabajo o la cuenta escolar.
2. Verifique los dominios en **Apple Business Manager** y **Apple School Manager**: se aplica solo a los dominios que se han verificado en Apple Business Manager o Apple School Manager. Si se verifica un dominio, el dispositivo puede contactar con Apple Business Manager /Apple School Manager para obtener una URL de inscripción alternativa de MDM.
3. Establezca una asignación predeterminada Ivanti Neurons for MDM para tipos de plataforma **Mac**, **Apple Vision Pro**, **IPhone** y **iPad**.
4. En la consola Ivanti Neurons for MDM, vaya a **Administrador** > **Apple** > **Inscripción del dispositivo**. En la pantalla de **Inscripción del dispositivo**, se agregan las columnas **URL ADDE** y **ESTABLECER HORA DE URL ADDE**.**Primera preferencia**: el dispositivo verifica el conocido recurso HTTP en el dominio de la organización.**Opción de respaldo**: si el primer método falla, el dispositivo contacta con Apple ABM/ASM para obtener el destino alternativo especificado por Ivanti Neurons for MDM.
5. En **Acciones**, seleccione **Configurar la URL ADDE**.
6. Actualizar la página.

### Instrucciones del usuario del dispositivo

En este tema se tratan las acciones que el usuario del dispositivo debe realizar para registrar la inscripción de usuario controlada por cuenta o la inscripción de dispositivo controlada por cuenta.

**Procedimiento**

1. En el dispositivo, vaya a una de las opciones siguientes:\* Para el dispositivo **iOS**: **Ajustes** > **General** > **VPN** y **Gestión de dispositivos**.
   - Para el dispositivo **macOS**: **Configuración del sistema** > **Privacidad y Seguridad** > **Perfiles**.
   - Para el dispositivo **visionOS**: **Ajustes** > **General** > **VPN** y **Gestión de dispositivos**.
2. Ir a **Inicie sesión en la cuenta del trabajo o la escuela**.
3. Escriba la dirección de correo electrónico de la cuenta laboral o educativa. Asegúrese de que la dirección de correo electrónico tenga el siguiente formato:\<enterprise domain name>nombredeusuario@\<nombre del dominio de empresa>, por ejemplo, [**nombredeusuario@acme.com**](mailto\:nombredeusuario@acme.com).
4. La página de inicio de sesión toma automáticamente la ID de Apple administrada y lleva al usuario a través del flujo de iReg. Asegúrese de que introduce las credenciales de Ivanti Neurons for MDM.
5. Escriba las credenciales de la cuenta laboral o educativa y haga clic en **Continuar**.
6. Después de una autenticación de dos factores, queda completa la inscripción del dispositivo.
