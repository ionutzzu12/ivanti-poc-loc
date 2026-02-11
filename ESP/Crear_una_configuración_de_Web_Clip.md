---
title: Crear una configuración de Web Clip
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

Un clip web es un acceso directo a un sitio web o página web desde un dispositivo iOS. Utilice la configuración del clip web para crear clips web estándar en los dispositivos. Puede agregar un icono de clip web a su dispositivo iOS que iniciará un sitio web específico. Web Clips le ayuda a encontrar rápidamente y utilizar marcadores en las pantallas de inicio de sus dispositivos. También puede controlar algunos parámetros de la experiencia visual de Mobile Safari en el sitio.

La opción de delegación con distribución personalizada está disponible para esta configuración. Para obtener más información, consulte el tema *Distribuir la configuración* en [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Haga clic en **Configuraciones**.
3. Haga clic en +**Añadir**.
4. Busque y seleccione la configuración de Web Clip.
5. Configure los ajustes en esta página. Consulte la tabla del tema **Ajustes de la configuración de Web Clip** para obtener ayuda acerca de los valores.
6. Haga clic en **Siguiente** para configurar los ajustes de distribución.
7. Seleccione **Personalizado** y a continuación **Dispositivos/ Grupos de dispositivos**.
8. Haga clic en **Hecho**.

## Ajustes de configuración del clip web

La siguiente lista de tablas enumera los ajustes de configuración de Web clip:

| **Ajuste**                                             | Qué hacer                                                                                                                                                                             |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nombre**,                                            | Introduzca un nombre que identifique a esta configuración.                                                                                                                            |
| **Descripción**                                        | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                           |
| **Etiqueta**                                           | Introduzca el texto que desee mostrar bajo el acceso directo en la pantalla del dispositivo.\*                                                                                        |
| **URL**                                                | Introduzca la URL a la que accederá el webclip.\*                                                                                                                                     |
| **Extraíble**                                          | Marque la casilla para permitir que el usuario del dispositivo elimine el clip web.                                                                                                   |
| **Icono**                                              | Arrastre el archivo del logotipo hasta el cuadro punteado o haga clic en **Elegir archivo** para seleccionarlo desde su sistema de archivos.                                          |
| **Icono precompuesto**                                 | Seleccione esta opción para eliminar los efectos especiales añadidos por versiones más recientes de Safari.                                                                           |
| **Pantalla completa**                                  | Seleccione esta opción para mostrar el clip web en modo pantalla completa en lugar de hacerlo como contenido en un explorador.                                                        |
| **Ignorar el ámbito del manifiesto**                   | Seleccione permitir la navegación hasta un sitio web externo sin mostrar el navegador de Safari. Esta opción no tiene efecto cuando no está seleccionada la opción Pantalla completa. |
| **Identificador del grupo de aplicaciones de destino** | El identificador del grupo de aplicaciones que especifica la aplicación que abre la URL. **Ejemplo**: com.google.chrome.ios                                                           |

Escriba $ para ver una lista de [**variables&#x20;**](./Variables.md)compatibles, si las hubiera, para este campo.

**Temas relacionados:**

- [**Inicio de sesión seguro multiusuario para iOS**](./Inicio_de_sesión_seguro_multiusuario_para_iOS.md)
