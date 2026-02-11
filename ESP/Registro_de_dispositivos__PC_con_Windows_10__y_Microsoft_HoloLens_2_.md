---
title: Registro de dispositivos (PC con Windows 10+ y Microsoft HoloLens 2)
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Registro manual**](./Registro_de_dispositivos__PC_con_Windows_10__y_Microsoft_HoloLens_2_.md)\* [**Enviar una invitación**](./Registro_de_dispositivos__PC_con_Windows_10__y_Microsoft_HoloLens_2_.md)
  - [**Completar el proceso de registro del usuario final**](./Registro_de_dispositivos__PC_con_Windows_10__y_Microsoft_HoloLens_2_.md)
- [**Windows Autopilot**](./Registro_de_dispositivos__PC_con_Windows_10__y_Microsoft_HoloLens_2_.md)
- [**Registro estándar de Entra ID**](./Registro_de_dispositivos__PC_con_Windows_10__y_Microsoft_HoloLens_2_.md)

Hay dos tipos de proceso de registro de dispositivos:

- Registro manual\* Invitación
  - Registro de usuario final
- Windows Autopilot
- Con SCCM e Ivanti EPM, a través de la inscripción de paquetes de aprovisionamiento con PIN. Consulte [**Inscripción de paquete de aprovisionamiento con PIN**](./Inscripción_de_paquete_de_aprovisionamiento_con_PIN.md).
- [**Inscripción en masa**](./Uso_de_la_Inscripción_en_masa_para_dispositivos_Windows.md)

## Registro manual

La mayoría de los usuarios comienzan por registrar un dispositivo. Para iniciar el proceso de registro, puede hacerlo de cualquiera de las siguientes formas:

- Invitación por correo electrónico
- Dirigir a los usuarios la URL para su implementación
- El [**usuario final debe tener una cuenta**](./Usuarios.md) en Ivanti Neurons for MDM antes de poder iniciar el proceso de registro del dispositivo. Para los usuarios de LDAP, esto significa que deben tener configurados un [**Conector**](./Conector.md) y un [**servidor LDAP**](./Configuración_del_servidor_LDAP.md) y que el usuario debe importarse del servidor LDAP. Para los usuarios locales, esto implica [**añadir un usuario**](./Usuarios.md).
- La URL de inscripción de dispositivos generada en las versiones anteriores de Ivanti Neurons for MDM dejará de funcionar en la versión actual. El administrador deberá regenerar la URL de inscripción de dispositivos para el registro el dispositivo.

## Enviar una invitación

En la mayoría de los casos, comenzará el proceso de registro enviando una invitación. Ivanti Neurons for MDM ofrece las siguientes formas de enviar una invitación a los usuarios finales para que registren un dispositivo:

- en el [**Asistente de inicio**](./Introducción.md)
- al [**añadir uno o más usuarios**](./Usuarios.md)
- en la página Usuarios ([**Acciones > Enviar invitación**](./Invitar_a_usuarios.md))

Si los usuarios finales pierden la invitación, la reciben en un ordenador de escritorio o un portátil o si, por cualquier motivo, no la reciben, puede enviarles la URL que se incluía en la invitación. Solo tiene que añadir **\go** al final de la URL del servicio.

Los usuarios finales que tienen una cuenta de Ivanti Neurons for MDM con una contraseña establecida no necesitan una invitación para iniciar el proceso de registro. Puede enviarles la URL que aparecería en la invitación.

## Completar el proceso de registro del usuario final

Dígale a los usuarios de sus dispositivos cómo completar el proceso de registro. Puede usar las siguientes instrucciones como plantilla y realizar cualquier cambio necesario:

**Procedimiento**

1. Abra un navegador en su PC con Windows 10+.
2. Navegue hasta mobileiron.com/go.Será redirigido a una página nueva que contiene una URL de inscripción.
3. Copie esa URL de inscripción en el portapapeles.
4. Pulse **añadir cuenta** en la parte inferior de la página **Ajustes**.
5. Introduzca la dirección de correo electrónico asociada con la invitación recibida.
6. Si el nombre de usuario de Ivanti Neurons for MDM no coincide con la dirección de correo electrónico que este ingresó en Ivanti Neurons for MDM, dígale al usuario que ingrese su nombre de usuario cuando se le solicite la dirección de correo electrónico.
   Copie la URL del servidor del lugar de trabajo que copió en el siguiente campo de texto.
7. Pulse **iniciar sesión**.
8. Introduzca su contraseña en el siguiente campo.
9. Deje en blanco los demás campos.
10. Pulse **iniciar sesión**.
11. Haga clic en **hecho** en la pantalla **CUENTA AÑADIDA**.La pantalla de inicio del lugar de trabajo muestra que se ha añadido una cuenta.

## Windows Autopilot

Windows Autopilot es una característica de Microsoft que ayuda a los administradores a configurar y pre-configurar nuevos dispositivos para que estén listos para la empresa. La función de Autopilot ayuda a un aprovisionamiento rápido, fiable y sin problemas de los dispositivos Windows Desktop o HoloLens 2. Además, la función Autopilot ayuda a realizar las siguientes tareas: 

- Unir automáticamente dispositivos a Entra ID (Entra ID)
- Inscribir automáticamente los dispositivos en los servicios MDM
- Crear y auto-asignar dispositivos a grupos de configuración basados en el perfil del dispositivo
- Personalizar la experiencia de inscripción
- Aplicar configuraciones y políticas
- Instalar aplicaciones esenciales

Ivanti es compatible con todos los modos de perfiles Autopilot: 

- Impulsado por el usuario
- Proveído previamente impulsado por el usuario (anteriormente White Glove)
- Modo de auto-despliegue

Para obtener más información, consulte [**Configuración de los perfiles de Windows Autopilot**](./Configuración_de_los_perfiles_de_Windows_Autopilot.md).

Por motivos de seguridad y uso no autorizado del dispositivo, todos los dispositivos Windows de Autopilot se pueden bloquear para un arrendatario mediante la función TenantLockdown CSP. Para utilizar esta función, los dispositivos deben estar inscritos mediante la opción Autopilot. Esta configuración se aplica a nivel de dispositivo. Ver [**TenantLockdown CSP**](./TenantLockdown_CSP.md).

## Registro estándar de Entra ID

Cuando los usuarios se añaden al abonado de Entra ID, pueden inscribir directamente sus dispositivos a través de la Cuenta de Trabajo.

**Procedimiento**

1. En un dispositivo Windows, vaya a **Ajustes > Cuentas > Acceder al trabajo o escuela**.
2. Seleccione Agregar cuenta de trabajo o escuela y haga clic en **Conectar**.
3. Proporcione una dirección de correo electrónico desde su cuenta de trabajo.

El dispositivo se inscribe automáticamente a Ivanti Neurons for MDM.
