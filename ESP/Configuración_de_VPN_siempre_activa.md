---
title: Configuración de VPN siempre activa
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Licencia:**

- Gold para la Android Enterprise
- Silver para iOS

La configuración de VPN siempre activa garantiza que los usuarios se conecten automáticamente a VPN (cuando esté disponible) sin necesidad de llevar a cabo ninguna acción. Esta función requiere Android 7.0 + o iOS 8 +, además de un proveedor de VPN que admita el protocolo IKEv2.

## Ajustes de VPN siempre activa para Android

La configuración de VPN siempre activa se envía a los dispositivos de Android Enterprise con Android 7.0 +. En un dispositivo administrado con un Perfil de trabajo (Android 8.0+), la configuración de VPN se aplica al Perfil de trabajo.

Cuando se despliega un dispositivo en modo **COSU** con **AMA** como tipo de Inscripción de dispositivos, y si se envía al dispositivo una aplicación con la configuración **Siempre activo**, también se enviará la configuración **Siempre activo**.

Para habilitar esta configuración, seleccione una aplicación del Catálogo de aplicaciones o introduzca un nombre de paquete.

## Ajustes de VPN siempre activa para iOS

| Ajuste                                                 | Qué hacer                                                                                                                                                                              |
| ------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre                                                 | Introduzca un nombre que identifique a esta configuración.                                                                                                                             |
| Descripción                                            | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                            |
| Use la misma configuración en túnel para Móvil y Wi-Fi | Seleccione esta opción para definir un par de identificadores del servidor para las conexiones VPN, independientemente de si la conexión se ha establecido por móvil o como red Wi-Fi. |
| Servidor                                               | Introduzca el nombre de host o dirección IP del servidor VPN.                                                                                                                          |
| Identificador local                                    | El identificador del cliente IKEv2 en alguno de los siguientes formatos:\* FQDN                                                                                                        |

- UsuarioFQDN
- Dirección
- ASN1DN                                                                                                                                                                           |
  \| Identificador remoto                                                                      | Identificador remoto en uno de los siguientes formatos:\* FQDN
- UsuarioFQDN
- Dirección
- ASN1DN                                                                                                                                                                                            |
  \| Activar EAP                                                                               | Seleccione esta opción para habilitar la autenticación ampliada.                                                                                                                                                                                                                            |
  \| Autenticación del equipo                                                                  | Solo disponible si «Habilitar EAP» no está seleccionado.Seleccione una de las siguientes opciones:\* Certificado
- Secreto compartido                                                                                                                                                        |
  \| Autenticación EAP                                                                         | Solo disponible si «Habilitar EAP» está seleccionado.Seleccione una de las siguientes opciones:\* Certificado
- Nombre de usuario/contraseña                                                                                                                                                 |
  \| Secreto compartido                                                                        | Solo disponible si se ha seleccionado Secreto compartido para la Autenticación del equipo. Introduzca el secreto compartido para la conexión.                                                                                                                                               |
  \| Credencial                                                                                | Solo disponible si se ha seleccionado Certificado para la Autenticación del equipo. Seleccione el certificado que desea utilizar. Este certificado se enviará para autenticación del cliente IKE. Si se usa la autenticación ampliada, este certificado se puede usar también para EAP-TLS. |
  \| Cuenta                                                                                    | Solo disponible si se ha seleccionado «Nombre de usuario/contraseña» para la Autenticación EAP. Introduzca la Id. de cuenta para el servidor VPN.                                                                                                                                           |
  \| Contraseña                                                                                | Solo disponible si se ha seleccionado «Nombre de usuario/contraseña» para la Autenticación EAP. Introduzca la contraseña para el servidor VPN.                                                                                                                                              |
  \| Intervalo de detección de pares no funcionales                                            | Seleccione una de las siguientes opciones:\* Ninguno (desactivar)
- Bajo (se envía un keepalive 1 vez por hora)
- Medio (se envía un keepalive cada 30 minutos)
- Alto (se envía un keepalive cada 10 minutos)                                                                               |
  \| Algoritmo de cifrado                                                                      | Seleccione una de las siguientes opciones:\* DES
- 3DES
- AES-128
- AES-256
- AES-128-GCM
- AES-256-GCM
- ChaCha20-Poly1305                                                                                                                                                                  |
  \| Algoritmo de integridad                                                                   | Seleccione una de las siguientes opciones:\* SHA1-96
- SHA1-160
- SHA2-256
- SHA2-384
- SHA2-512                                                                                                                                                                                             |
  \| Grupo Diffie Hellman                                                                      | Seleccione el grupo de intercambio de claves D-H.                                                                                                                                                                                                                                           |
  \| Vigencia en minutos                                                                       | Introduzca la vigencia SA (intervalo de reintroducción de clave) en minutos. Los valores válidos van del 10 al 1440.                                                                                                                                                                        |
  \| Correo de voz                                                                             | Seleccione Permitir tráfico a través de túnel para que el correo de voz esté exento de VPN siempre activa. Seleccione «Disminuir tráfico» para que no sea una excepción.                                                                                                                    |
  \| Airprint                                                                                  | Seleccione Permitir tráfico a través de túnel para que el tráfico de Airprint esté exento de VPN siempre activa. Seleccione «Disminuir tráfico» para que no sea una excepción.                                                                                                              |
  \| Servicios móviles                                                                         | Seleccione Permitir tráfico a través de túnel para que el tráfico de los servicios móviles esté exento de VPN siempre activa. Seleccione «Disminuir tráfico» para que no sea una excepción.                                                                                                 |
  \| Permitir el tráfico de la hoja web cautiva fuera del túnel de la VPN                      | Seleccione esta opción para permitir el tráfico de la hoja web cautiva fuera del túnel de la VPN.                                                                                                                                                                                           |
  \| Permitir el tráfico de todas las aplicaciones de la red cautiva fuera del túnel de la VPN | Seleccione esta opción para permitir el trádico de todas las aplicaciones de la red cautiva fuera del túnel de la VPN para realizar la gestión de redes cautivas.                                                                                                                           |
  \| Identificadores del paquete de aplicaciones de red cautiva                                | Enumere los Id. del paquete para aplicaciones de red cautiva cuyo tráfico se permitirá fuera del túnel de VPN para realizar la gestión de redes cautivas. Las aplicaciones de redes cautivas pueden requerir permisos adicionales para operar en un entorno cautivo.                        |
