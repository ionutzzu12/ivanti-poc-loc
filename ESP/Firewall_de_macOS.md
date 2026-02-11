---
title: Firewall de macOS
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Licencia:&#x20;**&#x47;old

El Firewall de macOS administra los ajustes de cortafuegos de la aplicación a los que se puede acceder en el panel Preferencias de seguridad en dispositivos macOS.

**Aplicable a**: macOS 12.3+

- **Permitir que el software integrado reciba conexiones entrantes**: si es cierto, permite al software integrado reciba conexiones entrantes.
- **Permitir que el software firmado descargado reciba conexiones entrantes**: si es cierto, permite que el software firmado descargado reciba conexiones entrantes.

**Aplicable a**: macOS 12.0+

- **Habilitar registro**: si es cierto, se habilita el registro
- **Especifique el tipo de registro**\* **Acelerador**
  - **Resumen**
  - **Detalle**

**Aplicable a:** macOS 10.12+

Cuando hace clic en **Activar firewall**, puede seleccionar una o más de las siguientes opciones:

- **Bloquear todas las conexiones entrantes**: seleccione esta opción para evitar que todos los servicios de uso compartido reciban conexiones entrantes en dispositivos macOS, como compartir pantalla o compartir archivos. Los siguientes servicios del sistema aún pueden recibir conexiones entrantes:\* configd, que implementa DHCP y otros servicios de configuración de red
  - mDNSResponder, que implementa Bonjour
  - racoon, que implementa IPSec
- **Habilitar modo sigiloso**: Seleccione esta opción para evitar que los dispositivos macOS respondan a solicitudes de sondeo. Los dispositivos macOS administrados aún responden a las solicitudes entrantes de aplicaciones autorizadas, mientras ignoran las solicitudes inesperadas, como ICMP (ping).
- **Aplicaciones**: La lista de aplicaciones con conexiones controladas por el firewall. Seleccione las aplicaciones específicas para las que desea recibir conexiones entrantes en dispositivos macOS.

Seleccione **Agregar** para agregar una fila a la lista de aplicaciones. Seleccione la celda debajo de **ID de paquete** para seleccionar la aplicación cuyas conexiones entrantes desea permitir explícitamente. Seleccione la casilla de verificación en la celda **Permitir conexiones** para permitir conexiones entrantes desde la aplicación seleccionada.

- la configuración debe existir en un perfil con ámbito del sistema. Si más de un perfil contiene esta configuración, se utilizará la unión de configuraciones más restrictiva.
  No se admiten las opciones **"Permitir automáticamente el software descargado firmado"** y **"Permitir automáticamente el software integrado"**. Sin embargo, ambas se pondrán activadas (ON) obligatoriamente cuando esta configuración esté disponible.
  El administrador puede habilitar el modo sigiloso especificando un dispositivo que no se pueda descubrir por el comando ping.
