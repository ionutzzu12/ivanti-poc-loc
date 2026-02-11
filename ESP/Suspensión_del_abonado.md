---
title: Suspensión del abonado
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

El acceso a un abonado que se utiliza junto con una licencia de evaluación o de producción puede ser suspendido por Ivanti Neurons for MDM. Se puede suspender una licencia de evaluación cuando caduque el período de evaluación o se exceda el límite de uso. Igualmente, se puede suspender una licencia de producción cuando caduque el período de suscripción o se exceda el límite de uso. Ivanti Neurons for MDM restablecerá los derechos del abonado suspendido cuando se haya renovado la licencia o se hayan comprado licencias adicionales, en los casos que excedan el límite de uso.

### Cuando se suspende la licencia de un abonado:

- Los dispositivos existentes registrados continuarán funcionando con normalidad.
- Los administradores no podrán iniciar sesión en el Portal de administración.
- No se podrán registrar nuevos dispositivos.
- El acceso a la API por parte del abonado estará bloqueado.
- Los usuarios finales podrán seguir accediendo al Portal de autoservicio.

### Acciones y mensajes de error de la suspensión de abonados

| Acción de suspensión                                                             | Error                                                           | Mensaje de error mostrado                                                                                                                                                                                                                                                                                                                                                                                        | Ubicación                              |
| -------------------------------------------------------------------------------- | --------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| El acceso a la API de integración del cliente final está bloqueado.              | La llamada a la API no funciona.                                | Acceso denegado. Su licencia de evaluación ha caducado. Renueve su licencia para volver a habilitar el acceso a la API. Contacte con su administrador de sistemas para obtener más detalles.                                                                                                                                                                                                                     | Error de API 401.                      |
| Se bloquea el registro de nuevos dispositivos.                                   | Aparece un mensaje de error en la pantalla de inscripción.      | No se ha podido registrar su dispositivo. La licencia de su sistema ha caducado. Contacte con su administrador de sistemas para obtener más detalles. Los dispositivos previamente inscritos seguirán funcionando con normalidad.                                                                                                                                                                                | Tras la verificación de la contraseña. |
| Se bloquea el inicio de sesión del administrador en el Portal de administración. | Aparece un mensaje de error en la pantalla de inicio de sesión. | No se ha podido iniciar sesión. Su licencia ha caducado. Renueve su licencia para recuperar el acceso al Portal de administración y para inscribir nuevos dispositivos. Los dispositivos previamente inscritos seguirán funcionando con normalidad. Contacte con su representante de ventas para renovar sus licencias. Tenga en cuenta que la contraseña del administrador caduca después de un año (365 días). | Tras la verificación de la contraseña. |
