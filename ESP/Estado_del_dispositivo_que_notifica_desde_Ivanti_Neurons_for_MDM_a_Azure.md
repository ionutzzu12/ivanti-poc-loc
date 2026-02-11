---
title: Estado del dispositivo que notifica desde Ivanti Neurons for MDM a Azure
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

En los siguientes casos, Ivanti Neurons for MDM informa del inventario de dispositivos y del estado de cumplimiento.

- Cambio de estado del cumplimiento en el dispositivo
- Cambio de inventario en el dispositivo
- Una vez a la semana, Ivanti Neurons for MDM informa del estado de cumplimiento y del inventario

En función de la acción seleccionada en la directiva de cumplimiento, se enviará el siguiente estado del dispositivo:

| Acción(se aplica la más restrictiva)                                | Lo que envía Ivanti Neurons for MDM                        |
| ------------------------------------------------------------------- | ---------------------------------------------------------- |
| Bloquear correo electrónico, Aplicaciones de AppConnect, Cuarentena | Dispositivo no compatible                                  |
| Enviar alerta                                                       | Compatible con Azure                                       |
| Retirar un dispositivo                                              | Datos del dispositivo eliminados de la plataforma de Azure |

## Página de detalles del dispositivo

Para ver la información de Azure sobre el dispositivo, visite la página de detalles del dispositivo. La descripción de los campos y sus posibles valores:

| Campo                                        | Descripción                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Identificador del dispositivo Azure          | El Id. de dispositivo informado por Microsoft al dispositivo iOS o Android. Por ejemplo: 007c8232-9489-4074-9b35-345b16f0a72d. Ivanti Neurons for MDM recibe este Id. de dispositivo porque los usuarios de dispositivos tienen que registrarse en la aplicación Autenticador de Microsoft.Si no puede obtener el Id. de dispositivo, este campo se deja en blanco. |
| Estado de cumplimiento del dispositivo Azure | Detalla el estado de cumplimiento del dispositivo en Azure. Valores posibles:\* En curso                                                                                                                                                                                                                                                                            |

- Correcto
- Error                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| Código de estado del cliente de Azure                  | Indica si el dispositivo está o no conectado a Azure. Valores posibles:\* Correcto: se pudo obtener el Id. de dispositivo.
- Internal\_Error: se produjo un error irrecuperable por parte del cliente o del servidor.
- Workplace\_Join\_Required: es necesario registrar el dispositivo. El usuario del dispositivo puede mitigar este estado.
- Interaction\_Required: es necesario un inicio de sesión interactivo. El usuario del dispositivo puede mitigar este estado.
- Server\_Declined\_Scopes: no se concedió acceso a algunos ámbitos.
- Server\_Protection\_Policies\_Required: el recurso solicitado está protegido por una directiva de Acceso condicional de Intune.
- User\_Canceled: el usuario del dispositivo canceló la sesión de autenticación web al tocar el botón «Hecho» o «Cancelar» del navegador web.
- Account\_logged\_out: se cerró la sesión de la cuenta. |
  \| Hora del informe de cumplimiento del dispositivo Azure | La hora en que Ivanti Neurons for MDM informó sobre el estado de cumplimiento de los dispositivos a Microsoft Intune. Un campo en blanco indica una de las siguientes situaciones:\* esa característica está deshabilitada
- Ivanti Neurons for MDM recibió los datos y todavía tiene que llamar a la API de Microsoft
- hay un error como user\_Cancelled o Error interno                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
