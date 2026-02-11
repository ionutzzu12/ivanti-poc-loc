---
title: Uso de la inscripción en masa para Android
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

La función de inscripción en masa le permite registrar rápidamente múltiples dispositivos Android con Ivanti Neurons for MDM.

Licencia: Silver

Realice las siguientes tareas antes de utilizar la inscripción masiva:

1. Instalar Android SDK, que incluye Android Debug Bridge (adb), en el ordenador que se está usando para registrar los dispositivos.Para obtener más información acerca de Android Debug Bridge, visite: [**http://developer.android.com/tools/help/adb.html.**](http://developer.android.com/tools/help/adb.html)
2. Habilitar la depuración de USB.el procedimiento para habilitar la depuración de USB en dispositivos Android varía dependiendo de la versión de Android. Consulte: [**http://developer.android.com/tools/device.html**](http://developer.android.com/tools/device.html) para obtener más información sobre cómo habilitar la depuración de USB.
3. Instalar el cliente Go en cada dispositivo.
4. Conectar los dispositivos mediante el cable USB al ordenador de aprovisionamiento que se usará para registrarlos.

Se puede iniciar y registrar Go en un servidor utilizando el shell de Android Debug Bridge (adb). Android Debug Bridge es una herramienta que se puede utilizar desde la línea de comandos de Windows o en la utilidad Terminal de iOS. Le permite comunicarse con un dispositivo Android conectado. Desde el shell de adb, el formato de comandos es el siguiente:

\> adb shell

$ am start -a android.intent.action.MAIN -d "mirp\://na1.mobileiron.com?key=value\&key=value" -n com.mobileiron.anyware.android/com.mobileiron.polaris.manager.ui.StartActivity

 El Protocolo de registro (**mirp**) se usa para codificar los datos relevantes para el registro.

Las claves y valores válidos son los siguientes:

| Clave      | Valor                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| usuario    | Dirección de correo electrónico del usuario que se habría escrito en el campo de nombre de usuario si se usara iReg.Obligatorio.                                                                                                                                                                                                                                                                                                     |
| contraseña | Contraseña del usuario                                                                                                                                                                                                                                                                                                                                                                                                               |
| pin        | PIN de registro para el usuario                                                                                                                                                                                                                                                                                                                                                                                                      |
| quickStart | **Cuando se establece en TRUE:** aparece la pantalla de presentación, pero durante menos tiempo. En la pantalla de bienvenida, cuando el control de número cambia al botón Continuar, la pantalla avanzará automáticamente sin tener que pulsar Continuar. Además, este flujo de aprovisionamiento simplificado se produce en todos los dispositivos:\* Las indicaciones de privacidad y acceso directo para el usuario se omitirán. |

- En los dispositivos de Zebra, el cliente debe conceder privilegios de administrador a sí mismo sin un aviso al usuario. Requiere una versión mínima de Zebra MX 4.3.**Cuando se establece en FALSE:** aparece la pantalla de presentación como siempre y el usuario tendrá que pulsar Continuar en la pantalla de bienvenida. Opcionalmente, se puede poner de forma predeterminada en FALSE. |

Para usar la inscripción en masa, es obligatorio utilizar una contraseña, PIN o token.

Este comando de ejemplo especifica un servidor, un usuario, una contraseña, un PIN y un inicio rápido:

am start -a android.intent.action.MAIN -d "mirp\://ppp183.auto.mobileiron.com?user=[**miadmin@auto0001.mobileiron.com**](mailto\:miadmin@auto0001.mobileiron.com)\&password=P@$$W0R3\&pin=12345\&quickStart=true" -n com.mobileiron.anyware.android.qa/com.mobileiron.polaris.manager.ui.StartActivity

**Ejemplo de secuencia de comandos de inscripción en masa**

puede utilizar esta secuencia de comandos como ejemplo a la hora de diseñar su propia secuencia de comandos de inscripción en masa. Esta secuencia de comandos de ejemplo registra todos los dispositivos conectados al equipo de aprovisionamiento con el mismo usuario y contraseña.

for i in \`adb devices | grep -v devices |

do

 eco "Registering $i"

 adb -s $i shell "am start -a android.intent.action.MAIN -d \\"mirp\://\<nombre\_de\_servidor?user=dirección\_de\_correo\_electrónico\_del\_usuariopassword=contraseña

done

**Posibles mensajes de error**

Aquí le mostramos algunos errores potenciales que podría encontrarse al usar la inscripción en masa.:

| Error                                                                                  | Solución                                                                                           |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| mirp scheme not found (no se encontró el esquema mirp)                                 | Comando de ejemplo usando un esquema mirp: am start -a android.intent.action.MAIN -d "xxxmirp\://? |
| La URL no es válida                                                                    | Aparece si no se envía ninguna cadena de datos. Verifique que la URL es correcta.                  |
| No server information found (No se encontró información sobre el servidor)             | Falta información sobre el servidor o se introdujo incorrectamente.                                |
| No user information found (No se encontró información sobre el usuario)                | Verifique que se introdujo la clave del usuario.                                                   |
| No password/pin information found (no se encontró información sobre la contraseña/PIN) | Verifique que se introdujo un PIN O una contraseña.                                                |

Cuando hay varios perfiles creados para la inscripción masiva:

- Un dispositivo Android Enterprise totalmente gestionado e inscrito de forma nativa recibe el atributo personalizado que se creó con el primer perfil.
- Al migrar dispositivos, si el dispositivo está presente en un perfil de inscripción masiva, los atributos personalizados definidos para el dispositivo migrante del perfil de inscripción masiva se aplicarán al dispositivo en la migración. Este comportamiento es el mismo para los dispositivos Android Enterprise migrados totalmente gestionados porque recibe el atributo personalizado del primer perfil.

Además, todos los perfiles creados para ese dispositivo en particular se ven como activos.
