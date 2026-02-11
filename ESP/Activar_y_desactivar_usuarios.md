---
title: Activar y desactivar usuarios
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Activar y desactivar usuarios locales**](./Activar_y_desactivar_usuarios.md)
- [**Activar y desactivar usuarios LDAP**](./Activar_y_desactivar_usuarios.md)

Los usuarios locales y de LDAP pueden estar en estado activado o desactivado. En función de su estado, puede crear [**políticas personalizadas**](./Política_personalizada.md) utilizando la condición «Usuario activado» y configurando una acción para esa condición en el creador de normas. Por ejemplo, puede existir la regla de política personalizada para retirar los dispositivos que pertenecen a los usuarios locales/LDAP desactivados.

## Activar y desactivar usuarios locales

De forma predeterminada, cuando se crea un usuario local, el usuario está en estado activado.

**Procedimiento**

1. Vaya a **Usuarios.**
2. Haga clic en el nombre en pantalla del usuario local.
3. Haga clic en **Editar**. Aparecerá la ventana **Autenticación obligatoria**.
4. Introduzca su contraseña de administrador y haga clic en **Autenticar**.cuando se introducen varias entradas incorrectas de la contraseña y si se supera el «Límite del umbral de inicio de sesión fallido» establecido en los «Ajustes de complejidad de la contraseña», la cuenta se bloqueará y se cerrará la sesión actual.
5. Seleccione o deseleccione la opción **Activado** para activar o desactivar, respectivamente, al usuario local.
6. Haga clic en **Guardar**.

## Activar y desactivar usuarios LDAP

Puede activar o desactivar usuarios LDAP solo para Microsoft Active Directory. En Microsoft Active Directory, al abrir las propiedades de la cuenta de un usuario, haga clic en la pestaña **Cuenta** y, a continuación, seleccione o deseleccione las casillas del cuadro de diálogo con las opciones de **Cuenta**. Entonces se asignarán valores numéricos al atributo **UserAccountControl**. El valor que se asigne al atributo indicará a Windows qué opciones se han activado. Luego de asignar un valor al atributo UserAccountControl, el estado del usuario lo reflejará después de la sincronización de LDAP con Ivanti Neurons for MDM.

A continuación se indican los posibles valores que se pueden asignar:

- 512 - Habilitado.
- 514 - Desactivado.
- 66048 - Activado, la contraseña no caduca nunca.
- 66050 - Desactivado, la contraseña no caduca nunca.

### Ver las cuentas del usuario

**Procedimiento**

|   | 1. | Haga clic en **Iniciar**. |
| - | -- | ------------------------- |

|   | 2. | Vaya a **Programas**. |
| - | -- | --------------------- |

|   | 3. | Vaya a **Herramientas administrativas**. |
| - | -- | ---------------------------------------- |

|   | 4. | Haga clic en **Usuarios y equipos de Active Directory**. |
| - | -- | -------------------------------------------------------- |

Para obtener más información, consulte [**https://support.microsoft.com/en-in/help/305144/how-to-use-the-useraccountcontrol-flags-to-manipulate-user-account-pro**](https://support.microsoft.com/en-in/help/305144/how-to-use-the-useraccountcontrol-flags-to-manipulate-user-account-pro).

Puede ver y editar los atributos usando la herramienta Ldp.exe o el complemento Adsiedit.msc. Solo los administradores con experiencia debe usar estas herramientas para editar Active Directory. Ambas herramientas están disponibles después de haber instalado las herramientas de la Asistencia técnica desde sus soportes de instalación originales de Windows.
