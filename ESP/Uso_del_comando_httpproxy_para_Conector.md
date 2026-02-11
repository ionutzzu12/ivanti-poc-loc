---
title: Uso del comando httpproxy para Conector
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Un nuevo comando shell klish se creó para ayudar a editar la configuración de Conector para su instalación de Ivanti Neurons for MDM. Use este comando para cambiar la información de contacto y otros parámetros para configurar el conector.

Ahora, el comando httpproxy está disponible en esta versión con estos requisitos.

- klish shell

Para configurar su conector:

1. Inicie sesión en klish shell.
2. Introduzca un ? para obtener una lista de comandos shell klish disponibles.
3. Introduzca **httpproxy** para mostrar el valor actual de estos parámetros:1) habilitado
   2\) esquema
   3\) servidor
   4\) tipo de autenticación
   5\) nombre de usuario
   6\) contraseña
4. Introduzca **httpproxy ?** para ver un listado de los comandos disponibles para usar con httpproxy.1) authtype - Establecer el tipo de autenticación del proxy http en NONE, BASIC o NTLM
   2\) disable - Desactivar el proxy http
   3\) enable - Activar el proxy http
   4\) host - Establecer el host del proxy http; debe ser un FQDN o una IP, ya sea http o https
   5\) password - Establecer la contraseña de autenticación del proxy http
   6\) port - Establecer el puerto del proxy http
   7\) scheme - Establecer el esquema del proxy http, debe ser http o https
   8\) show - Mostrar los ajustes actuales del proxy http
   9\) username - Establecer el nombre de usuario de autenticación del proxy http
5. Use los comandos indicados más arriba para configurar su conector.
