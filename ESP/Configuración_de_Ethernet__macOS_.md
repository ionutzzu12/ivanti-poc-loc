---
title: Configuración de Ethernet (macOS)
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

**Licencia:** Gold

**Aplicable a:** macOS 10.13+ o versiones más recientes compatibles.

El administrador puede configurar la interfaz Ethernet en variaciones. Las siguientes cargas útiles están disponibles para la configuración de Ethernet:

- Ethernet general
- Primera Ethernet activa
- Primera Ethernet
- Segunda Ethernet activa
- Segunda Ethernet
- Tercera Ethernet activa
- Tercera Ethernet

Las diferentes cargas útiles para configurar Ethernet son: Global por defecto, Primera, Primera activa, Segunda, Segunda activa, Tercera y Tercera interfaz de Ethernet activa. Apple tiene un problema conocido con la instalación de la Primera, Primera activa, Segunda, Segunda activa, Tercera y Tercera interfaz de Ethernet activa.

## Configuración de Ethernet

Procedimiento

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **Ethernet** en el campo de búsqueda y, a continuación, seleccione configuración de **Ethernet**.
4. Introduzca un nombre y describa la configuración.
5. Elija la configuración en la lista desplegable:
6. Escriba los [**ajustes de configuración de Ethernet**](./Configuración_de_Ethernet__macOS_.md).
7. Haga clic en **Siguiente**.
8. Seleccione la opción **Habilitar esta configuración**.
9. Seleccione una de las siguientes opciones de canal para aplicar la configuración:\* Canal de dispositivos (el más común)
   - Canal del usuario (usuario actualmente registrado)
10. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
    - Ningún dispositivo (predeterminada)
    - personalizada
11. Haga clic en **Hecho**.

## Ajustes de la configuración de Ethernet

Utilice los ajustes de la siguiente tabla para configurar la Ethernet. Para obtener más información sobre estos ajustes, consulte [**Documentación de Apple**](https://developer.apple.com/documentation/devicemanagement/profile-specific_payload_keys?language=objc).

| **Ajuste**                 | **Descripción**                                                                                                                                                                                                                                                                                          |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Protocolos**             |                                                                                                                                                                                                                                                                                                          |
| **Tipos de EAP aceptados** | Seleccione los tipos de EAP que pueden utilizarse para acceder a esta red:\* Seguridad de la capa de transporte (TLS): la TLS es un protocolo que establece una sesión cifrada entre dos ordenadores en Internet. Verifica la identidad del servidor y evita que los hackers intercepten cualquier dato. |

- TTLS: en el campo **Identidad interior**, seleccione uno de los protocolos de autenticación como SO predeterminado, PAP, CHAP, MSCHAP, MSCHAPv2 y EAP.
- PEAP
- LEAP
- EAP-SIM: en el campo **EAP SIM Number of RANDs** (Número SIM de RAND de EAP), seleccione el número de «rands» en la lista desplegable.
- EAP-AKA
- EAP- FAST: seleccione la opción EAP-FAST que define los métodos de autenticación:\* **Usar PAC:** seleccione esta opción para usar la autoconfiguración del proxy (PAC).
  - **PAC de aprovisionamiento:** seleccione esta opción para permitir que se aprovisione la PAC. De lo contrario, solamente podrán utilizarse las PAC ya aprovisionadas en el dispositivo. Esta opción solamente está disponible si ha seleccionado Usar PAC.
  - **PAC de aprovisionamiento anónimo:** seleccione esta opción para permitir que se aprovisione una PAC sin autenticar el servidor. Esta opción solamente está disponible si ha seleccionado PAC de aprovisionamiento.                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| **Autenticación**          | **Nombre de usuario**: especifique el nombre de usuario requerido para acceder a la red. Si deja esta opción en blanco, se le solicitará al usuario del dispositivo.\* Usar contraseña por conexión: seleccione esta opción para solicitar al usuario el dispositivo una contraseña cada vez que se conecte. Cuando el dispositivo vuelva a unirse a la misma red, se solicitará al usuario del dispositivo que vuelva a autenticarse para unirse a la red. Cada vez que se inicia la conexión, se solicita la contraseña.
- Solicitar la contraseña una vez cuando se conecte a la red: la contraseña se solicita una sola vez cuando se envía la configuración al dispositivo. Cada conexión y desconexión a la red no solicitará ninguna contraseña.**Contraseña**: (opcional) introduzca la contraseña para acceder a esta red. De lo contrario, se le pedirá al usuario del dispositivo la contraseña necesaria para acceder a la red.**Identidad exterior**:(opcional) para TTLS, PEAP y EAP-FAST, seleccione esta opción para permitir a los usuarios de los dispositivos que oculten su identidad. El nombre real del usuario solo aparecerá dentro del túnel cifrado. Esta opción puede mejorar la seguridad porque un atacante no puede ver claramente el nombre del usuario de autenticación.Identidad de origen de las credenciales del modo de sistema: el modo de sistema se utiliza para la autenticación del ordenador. La autenticación mediante el modo de sistema se produce antes de que un usuario inicie sesión en el ordenador. El modo de sistema suele estar configurado para proporcionar autenticación con el certificado X.509 del ordenador (EAP-TLS) emitido por una autoridad certificadora local. |
  \| **Confiar**                | **Certificados de confianza:&#x20;**&#x73;eleccione las casillas de verificación para seleccionar varios certificados de la lista.**Nombres de certificado del servidor de confianza**: agregue el nombre del certificado.\* **Permitir excepciones de confianza**: permitir que el usuario tome decisiones de confianza en una ventana de diálogo.
- **Requerir certificado TLS****Versión máxima de TLS permitida con la autenticación EAP****Versión mínima de TLS permitida con la autenticación EAP\*\*\*\*Certificados de confianza TLS: certificado EC del agente de MobileIron**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
