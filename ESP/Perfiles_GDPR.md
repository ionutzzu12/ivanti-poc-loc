---
title: Perfiles GDPR
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

El portal administrativo de Ivanti Neurons for MDM ahora contiene una página de perfiles de GDPR que le permite asignar perfiles de GDPR a grupos de usuarios. Solo puede asignar el perfil de GDPR a grupos de usuarios y no a usuarios individuales.

Tenga en cuenta los puntos siguientes:

- En primer lugar debe activar los perfiles de GDPR para asignarlos a un grupo de usuarios específico.
- Si desactiva el perfil GDPR, se desactivarán todas las restricciones del perfil que ya se habían asignado al grupo de usuarios.
- Después de activar el perfil GDPR, se limitará o desactivará la función Editar para algunos campos.

## Los campos que están ocultos tras la asignación del perfil GDPR

Si un usuario tiene un perfil de GDPR, Ivanti Neurons for MDM oculta los campos siguientes por defecto cuando se muestra la información del usuario:

- Id. de Usuario
- Nombre de usuario
- Dirección de correo electrónico
- Número de serie
- ICCID
- IMSI
- MEID
- Dirección IP
- **Número de teléfono**
- **IMEI**
- **Identificador eSIM**
- **Ubicación**Si se añade Ubicación al perfil GDPR, los campos Ubicación del dispositivo Última ubicación en, Latitud y Longitud se enmascaran en los detalles del dispositivo para los usuarios asignados con el perfil GDPR.

## Activación del perfil GDPR

Puede habilitar el perfil de GDPR y seleccionar campos específicos que se deben ocultar en el portal administrativo de Ivanti Neurons for MDM y los dispositivos.

ProcedureProcedimiento

|   | 1. | Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM. |
| - | -- | --------------------------------------------------------------------- |

|   | 2. | Vaya a **Admin** > **Sistema** > **Perfiles GDPR**. |
| - | -- | --------------------------------------------------- |

|   | 3. | Haga clic en **Habilitar**. |
| - | -- | --------------------------- |

|   | 4. | Haga clic en el icono de editar (lápiz). |
| - | -- | ---------------------------------------- |

|   | 5. | Seleccione los campos que se deben ocultar. |
| - | -- | ------------------------------------------- |

|   | 6. | Haga clic en **Guardar**. Los campos seleccionados se enmascararán y no mostrarán los valores de los usuarios específicos. |
| - | -- | -------------------------------------------------------------------------------------------------------------------------- |

## Asigne el perfil GDPR al Grupo de usuarios

Después de activar los perfiles GDPR, podrá asignarlos a un grupo de usuarios específico.

ProcedureProcedimiento

|   | 1. | Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM. |
| - | -- | --------------------------------------------------------------------- |

|   | 2. | Vaya a **Usuarios** > **Grupos de usuarios**. |
| - | -- | --------------------------------------------- |

|   | 3. | Seleccione un grupo de usuario de la lista. |
| - | -- | ------------------------------------------- |

|   | 4. | Haga clic en la lista desplegable **Acciones** y seleccione **Asignar perfil GDPR**. El perfil GDPR se asigna a todos los usuarios de ese grupo específico y todos los valores seleccionados se enmascararán de la vista mediante el portal administrativo y los dispositivos del usuario. Puesto que el administrador también está en el grupo Todos los usuarios, no asigne los perfiles GDPR al grupo Todos los usuarios. |
| - | -- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
