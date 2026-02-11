---
title: FileVault 2
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

**Licencia:** Gold

FileVault 2 ofrece la posibilidad de realizar un cifrado completo del disco XTS-AES 128 en el contenido de un volumen.

Al habilitar FileVault 2, estarán disponibles los siguientes ajustes para la configuración:

| Categoría                        | Ajustes                                                     |
| -------------------------------- | ----------------------------------------------------------- |
| Ajustes del usuario de FileVault | - Activar FileVault en SetupAssist**Predeterminado**: falso |

- Si es cierto, y la carga útil se instala después de inscribirse con Ivanti Neurons for MDM en el Asistente de instalación, solicita al Asistente de instalación que habilite FileVault en el momento de la instalación. Además, el sistema ignora las demás claves de esta carga útil, excepto ShowRecoveryKey.**Prerrequisito**: antes de activar file vault en el asistente de configuración, asegúrese de que la opción **Esperar a la configuración del dispositivo durante la configuración de inscripción del dispositivo** está activada en el perfil de inscripción de dispositivos.
- Aplazar la habilitación de FileVault hasta que el usuario designado cierre sesión
  - Pedir siempre al usuario que active FileVault
  - Número máximo de veces que un usuario puede omitir la activación de FileVault
    No solicitar la activación de FileVault en el momento en que el usuario cierra sesión |
    \| Ruta de salida                     | Introduzca la ruta hasta la ubicación donde se almacenarán la clave de recuperación y el plist de la información del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
    \| Clave de recuperación personal     | \* Crear una clave de recuperación personal
- Mostrar la clave de recuperación personal al usuario una vez que se haya habilitado FileVaultEsta opción solo está visible cuando la opción **Crear una clave de personal de recuperación** está habilitada. De forma predeterminada, la opción está desactivada.
- Habilitar Clave de recuperación institucional: uso de la llave - si no se proporciona ninguna información sobre el certificado en esta carga útil, se usará la llave ya creada en /Library/Keychains/FileVaultMaster.keychainSeleccione una de las siguientes opciones:
  - Cargar certificado
  - Certificado
  - Usar llave en el sistema del usuario                                                                                                                                                                                                                                                                                                   |
    \| Rotar FileVault Key tras \_\_ días | Los administradores pueden configurar la rotación periódica de las claves de FileVault de los dispositivos macOS para mitigar el riesgo de seguridad de los dispositivos implementados. Los administradores pueden establecer el intervalo de rotación en términos de días.Solo se rotan las Claves de Recuperación personal.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
