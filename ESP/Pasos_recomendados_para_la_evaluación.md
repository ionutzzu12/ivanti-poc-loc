---
title: Pasos recomendados para la evaluación
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

Los pasos siguientes se recomiendan para validar una solución:

1. Crear una UO separada (Grupo de usuarios) que tenga un usuario de prueba en la fuente del directorio (ejemplo, Active Directory). Esto evitará el impacto a las Unidades organizativas activas.
2. Sincronice los usuarios entre Ivanti, Google y la fuente de directorios (LDAP). Verifique que la "UO de prueba" está disponible en los Grupos de usuarios.
3. Integrar Ivanti Neurons for MDM con Google como se indica en los pasos anteriores.
4. Cree una configuración de ChromeOS Blueprint y distribúyala solo al grupo de usuarios "UO de prueba".
5. Arranque un Chromebook (nuevo o registrado anteriormente). Asegúrese de que está disponible en la lista de dispositivos.
6. Verifique que los ajustes de ChromeOS Blueprint están disponibles en el dispositivo.
7. Seguir pasos similares para la distribución de aplicaciones de Android.
