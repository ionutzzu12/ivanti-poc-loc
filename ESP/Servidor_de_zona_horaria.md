---
title: Servidor de zona horaria
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** macOS 10.12.4 y la versión más reciente compatible.

Crear la configuración del servidor de zona horaria para permitir que los dispositivos se conecten a los servidores con horas personalizadas.

## Crear una configuración de servidor de zona horaria

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **hora** en el campo de búsqueda y, a continuación, haga clic en la configuración de **Servidor de zona horaria**.
4. Introduzca un nombre y describa la configuración.
5. Especifique el **Servidor NTP**.
6. Especifique la cadena de **Zona horaria** en formato de ID de zona horaria de Olson (por ejemplo, Pacific/Midway). Para obtener el formato de zona horaria de Olson, ejecute el comando `"/usr/sbin/systemsetup -listtimezones`" en el dispositivo macOS del administrador.
7. Haga clic en **Siguiente** para configurar los ajustes de distribución.
8. Haga clic en **Hecho**.
