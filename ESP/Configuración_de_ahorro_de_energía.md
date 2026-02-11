---
title: Configuración de ahorro de energía
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM activa la configuración de ahorro de energía para la carga útil que utiliza para configurar los ajustes de ahorro de energía en dispositivos Windows y macOS.

**Disponible para**:

- Windows 10 hasta la versión más reciente compatible con Ivanti Neurons for MDM.
- macOS 10.7 hasta la versión más reciente compatible con Ivanti Neurons for MDM.

**Procedimiento**

1. Vaya a **Configuraciones** > **+Añadir**.
2. Busque y seleccione la configuración de **Ahorro de energía**.
3. En la sección Elegir sistema operativo, seleccione **Windows** o **macOS** y haga clic en **Siguiente**.
4. Haga clic en **+ Añadir descripción** para introducir una breve descripción de la configuración.
5. Para Windows, configure los siguientes ajustes de **Ahorro de energía**:\* [**Dispositivo con batería**](./Configuración_de_ahorro_de_energía.md)
   - [**El dispositivo está enchufado**](./Configuración_de_ahorro_de_energía.md)
6. Configure los ajustes siguientes de **Ahorro de energía**:\* [**Ajustes de ahorro de energía CA del equipo de escritorio**](./Configuración_de_ahorro_de_energía.md)
   - [**Programar los ajustes de arranque o apagado del equipo**](./Configuración_de_ahorro_de_energía.md)
   - [**Ajustes de ahorro de energía CA del portátil**](./Configuración_de_ahorro_de_energía.md)
   - [**Ajustes de ahorro de energía de la batería del portátil**](./Configuración_de_ahorro_de_energía.md)
7. Haga clic en **Siguiente** para configurar los ajustes de distribución.
8. Seleccione una de las opciones de distribución para establecer la configuración de **Ahorro de energía**. Para más información sobre la configuración de las opciones de distribución, consulte [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).
9. Haga clic en **Hecho**.

## Configuración de ahorro de energía de Windows

Cuando se aplica una nueva configuración de ahorro de energía a un dispositivo o cuando se modifican los ajustes de configuración de ahorro de energía existentes, los usuarios deben reiniciar sus dispositivos para que los cambios surtan efecto.

### Dispositivo con batería

Utilice las configuraciones de ahorro de energía siguientes en la tabla cuando el dispositivo esté funcionando con la batería:

| **Ajuste**                                              | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Umbral de batería para activar el ahorro de energía** | Cuando el dispositivo esté usando la batería, introduzca el nivel de carga de la batería para activar el Ahorro de energía; puede introducir valores de 0 a 100. Introduzca un valor porcentual que indique el nivel de carga de la batería. Por ejemplo, cuando se establece en 80, Energy Saver se activa cuando la batería tiene un 80 % de carga o menos carga disponible.Si no introduce un valor, Ivanti Neurons for MDM no cambia ni actualiza esta configuración. De forma predeterminada, Windows lo configurará al 70 %. |
| **Cuando la tapa está cerrada**                         | - **No realizar ninguna acción**: el dispositivo permanece encendido y continúa usando la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                 |

- **Suspender**: el dispositivo entra en modo de suspensión y utiliza una pequeña cantidad de carga de la batería. El equipo todavía está encendido y las aplicaciones y archivos abiertos se almacenan en la memoria de acceso aleatorio (RAM).
- **Estado de suspensión de hibernación**: el dispositivo entra en modo de hibernación. Las aplicaciones y los archivos abiertos se almacenan en el disco duro y el dispositivo se apaga.
- **Apagar**: el dispositivo se apaga. Las aplicaciones y archivos abiertos se cierran sin guardarlos. |
  \| **Cuando se selecciona el botón de encendido**          | \* **No realizar ninguna acción**: el dispositivo permanece encendido y continúa usando la batería.
- **Suspender**: el dispositivo entra en modo de suspensión y utiliza una pequeña cantidad de carga de la batería. El equipo aun está encendido y las aplicaciones y archivos abiertos se almacenan en la RAM.
- **Estado de suspensión de hibernación**: el dispositivo entra en modo de hibernación. Las aplicaciones y los archivos abiertos se almacenan en el disco duro y el dispositivo se apaga.
- **Apagar**: el dispositivo se apaga. Las aplicaciones y archivos abiertos se cierran sin guardarlos.                                   |
  \| **Cuando se selecciona el botón Suspender**             | - **No realizar ninguna acción**: el dispositivo permanece encendido y continúa usando la batería.
- **Suspender**: el dispositivo entra en modo de suspensión y utiliza una pequeña cantidad de carga de la batería. El equipo aun está encendido y las aplicaciones y archivos abiertos se almacenan en la RAM.
- **Estado de suspensión de hibernación**: el dispositivo entra en modo de hibernación. Las aplicaciones y los archivos abiertos se almacenan en el disco duro y el dispositivo se apaga.
- **Apagar**: el dispositivo se apaga. Las aplicaciones y archivos abiertos se cierran sin guardarlos.                                   |
  \| **Activar la suspensión híbrida**                       | \* **Cierto**: los dispositivos pueden entrar en modo de suspensión híbrida. Las aplicaciones y los archivos abiertos se almacenan en la RAM y en el disco duro. Utiliza una pequeña cantidad de carga de batería.
- **Falso**: impide que los dispositivos entren en modo de suspensión híbrida.                                                                                                                                                                                                                                                                                                                                                     |

### El dispositivo está enchufado

Utilice las configuraciones siguientes en la tabla cuando el dispositivo esté usando energía de una fuente de alimentación externa:

| **Ajuste**                                              | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Umbral de batería para activar el ahorro de energía** | Cuando el dispositivo esté enchufado, introduzca el nivel de carga de la batería para activar el Ahorro de energía; puede introducir valores de 0 a 100. Introduzca un valor porcentual que indique el nivel de carga de la batería. Por ejemplo, cuando se establece en 80, Energy Saver se activa cuando la batería tiene un 80 % de carga o menos carga disponible.Si no introduce un valor, Ivanti Neurons for MDM no cambia ni actualiza esta configuración. De forma predeterminada, Windows lo configurará al 70 %. |
| **Cuando la tapa está cerrada**                         | - **No realizar ninguna acción**: el dispositivo permanece encendido y continúa usando una fuente de alimentación externa.                                                                                                                                                                                                                                                                                                                                                                                                 |

- **Suspender**: el dispositivo entra en modo de suspensión y utiliza una pequeña cantidad de fuente de alimentación externa. El equipo aun está encendido y las aplicaciones y archivos abiertos se almacenan en la RAM.
- **Estado de suspensión de hibernación**: el dispositivo entra en modo de hibernación. Las aplicaciones y los archivos abiertos se almacenan en el disco duro y el dispositivo se apaga.
- **Apagar**: el dispositivo se apaga. Las aplicaciones y archivos abiertos se cierran sin guardarlos. |
  \| **Cuando se selecciona el botón de encendido**          | \* **No realizar ninguna acción**: el dispositivo permanece encendido y continúa usando una fuente de alimentación externa.
- **Suspender**: el dispositivo entra en modo de suspensión y utiliza una pequeña cantidad de fuente de alimentación externa. El equipo aun está encendido y las aplicaciones y archivos abiertos se almacenan en la RAM.
- **Estado de suspensión de hibernación**: el dispositivo entra en modo de hibernación. Las aplicaciones y los archivos abiertos se almacenan en el disco duro y el dispositivo se apaga.
- **Apagar**: el dispositivo se apaga. Las aplicaciones y archivos abiertos se cierran sin guardarlos. |
  \| **Cuando se selecciona el botón Suspender**             | - **No realizar ninguna acción**: el dispositivo permanece encendido y continúa usando una fuente de alimentación externa.
- **Suspender**: el dispositivo entra en modo de suspensión y utiliza una pequeña cantidad de fuente de alimentación externa. El equipo aun está encendido y las aplicaciones y archivos abiertos se almacenan en la RAM.
- **Estado de suspensión de hibernación**: el dispositivo entra en modo de hibernación. Las aplicaciones y los archivos abiertos se almacenan en el disco duro y el dispositivo se apaga.
- **Apagar**: el dispositivo se apaga. Las aplicaciones y archivos abiertos se cierran sin guardarlos. |
  \| **Activar la suspensión híbrida**                       | \* **Cierto**: los dispositivos pueden entrar en modo de suspensión híbrida. Las aplicaciones y los archivos abiertos se almacenan en la RAM y en el disco duro. Utiliza una pequeña cantidad de fuente de alimentación externa.
- **Falso**: impide que los dispositivos entren en modo de suspensión híbrida.                                                                                                                                                                                                                                                                                                                                        |

## Configuración de macOS Energy Saver

### Ajustes de ahorro de energía CA del equipo de escritorio

Utilice los ajustes siguientes para configurar los ajustes de ahorro de energía de CA del dispositivo de sobremesa macOS:

| **Ajuste**                                      | **Descripción**                                                                                                                                     |
| ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nombre**,                                     | Introduzca un nombre que identifique a esta configuración.                                                                                          |
| **Descripción**                                 | Introduzca una descripción que explique la finalidad de esta configuración.                                                                         |
| **Arranque automático tras un fallo eléctrico** | Active el arranque automático del dispositivo tras un fallo eléctrico.                                                                              |
| **Poner un disco duro en reposo después de**    | Active la casilla para suspender el disco duro a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca pondrá el disco duro en reposo. |
| **Apagar la pantalla después de**               | Active la casilla para apagar la pantalla a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca apagará la pantalla.                 |
| **Paso de potencia dinámico**                   | Seleccione la casilla para activar el paso de potencia dinámico.                                                                                    |
| **Reducir la velocidad del procesador**         | Seleccione la casilla para reducir la velocidad del procesador.                                                                                     |
| **Poner el equipo en reposo después de**        | Active la casilla para suspender el equipo a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca pondrá el equipo en reposo.         |
| **Activar para acceder a la red**               | Seleccione la casilla para activar el equipo para el acceso a la red.                                                                               |
| **Activar por timbre de módem**                 | Seleccione la casilla para activar el equipo para el timbre del módem.                                                                              |

### Programar los ajustes de arranque o apagado del equipo

Utilice los siguientes ajustes para configurar los dispositivos macOS para el arranque o apagado programado de los dispositivos.

### Desactivar la configuración del dispositivo

Seleccione la casilla **Apagar el dispositivo** para apagar los dispositivos a intervalos fijos.

| **Ajuste**         | **Descripción**                                                                   |
| ------------------ | --------------------------------------------------------------------------------- |
| **Tipo de evento** | Seleccione uno de los tipos de evento opción en la lista desplegable:\* Suspender |

- Reiniciar
- Apagar |
  \| **Cuando**         | Seleccione uno o varios días de la semana para programar un tipo de evento.                           |
  \| **En**             | Seleccione la hora para programar un tipo de evento.                                                  |

### Inicio o activación de la configuración del dispositivo

Seleccione la casilla **Iniciar o activar el dispositivo** para activar los dispositivos a intervalos fijos.

| **Ajuste**         | **Descripción**                                                                 |
| ------------------ | ------------------------------------------------------------------------------- |
| **Tipo de evento** | Seleccione uno de los tipos de evento opción en la lista desplegable:\* Activar |

- Arranque / Activación |
  \| **Cuando**         | Seleccione uno o varios días de la semana para programar un tipo de evento.                            |
  \| **En**             | Seleccione la hora para programar un tipo de evento.                                                   |

### Ajustes de ahorro de energía CA del portátil

Utilice los ajustes siguientes para configurar los ajustes de ahorro de energía de CA del dispositivo portátil macOS:

| **Ajuste**                                      | **Descripción**                                                                                                                                     |
| ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Arranque automático tras un fallo eléctrico** | Active el arranque automático del dispositivo tras un fallo eléctrico.                                                                              |
| **Poner un disco duro en reposo después de**    | Active la casilla para suspender el disco duro a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca pondrá el disco duro en reposo. |
| **Apagar la pantalla después de**               | Active la casilla para apagar la pantalla a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca apagará la pantalla.                 |
| **Paso de potencia dinámico**                   | Seleccione la casilla para activar el paso de potencia dinámico.                                                                                    |
| **Reducir la velocidad del procesador**         | Seleccione la casilla para reducir la velocidad del procesador.                                                                                     |
| **Poner el portátil en reposo después de**      | Active la casilla para suspender el portátil a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca pondrá el portátil en reposo.     |
| **Activar para acceder a la red**               | Seleccione la casilla para activar el portátil para el acceso a la red.                                                                             |
| **Activar por timbre de módem**                 | Seleccione la casilla de verificación para despertar el ordenador portátil para el timbre del módem.                                                |

### Ajustes de ahorro de energía de la batería del portátil

Utilice los ajustes siguientes para configurar los ajustes de ahorro de energía de la batería del dispositivo portátil macOS:

| **Ajuste**                                      | **Descripción**                                                                                                                                                         |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Arranque automático tras un fallo eléctrico** | Active el arranque automático del dispositivo tras un fallo eléctrico.                                                                                                  |
| **Poner un disco duro en reposo después de**    | Active la casilla para suspender el disco duro a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca pondrá el disco duro en reposo.                     |
| **Apagar la pantalla después de**               | Active la casilla para apagar la pantalla a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca apagará la pantalla.                                     |
| **Paso de potencia dinámico**                   | Seleccione la casilla para activar el paso de potencia dinámico.                                                                                                        |
| **Reducir la velocidad del procesador**         | Seleccione la casilla para reducir la velocidad del procesador.                                                                                                         |
| **Poner el equipo en reposo después de**        | Active la casilla para suspender la batería del portátil a intervalos fijos entre 1 y 180 minutos.Un valor de 0 minutos nunca pondrá la batería del portátil en reposo. |
| **Activar para acceder a la red**               | Seleccione la casilla para activar la batería del portátil para el acceso a la red.                                                                                     |
| **Activar por timbre de módem**                 | Seleccione la casilla para activar la batería del portátil para el timbre del módem.                                                                                    |
