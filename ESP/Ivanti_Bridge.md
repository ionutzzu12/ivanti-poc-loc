---
title: Ivanti Bridge
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Tipos de archivo compatibles con Bridge**](./Ivanti_Bridge.md)
- [**Configuración de Bridge**](./Ivanti_Bridge.md)
- [**Registros de Bridge**](./Ivanti_Bridge.md)
- [**Último ingreso de Bridge**](./Ivanti_Bridge.md)
- [**Recuperación de un fallo en el servicio de Bridge**](./Ivanti_Bridge.md)

Ivanti Bridge unifica las operaciones móviles y de escritorio para Windows 10 mediante una única consola y un único canal de comunicaciones. Amplía las funciones de UEM para administrar PC permite a las organizaciones sacar partido de [**costes considerablemente reducidos**](https://www.mobileiron.com/en/solutions/windows/pc-management-tco) y una mayor eficiencia a la vez que se garantiza una seguridad uniforme en todos los PC y dispositivos móviles. Usando Ivanti Bridge, las empresas pueden usar un único protocolo para los dispositivos de Windows 10 Desktop, del mismo modo que hacen con dispositivos móviles compatibles con Windows, para enviar información a las aplicaciones legadas del SO.

Ivanti Bridge permite que el departamento informático modernice las operaciones de Windows en UEM sin sacrificar las funciones críticas. El departamento informático puede aplicar políticas y secuencias de comandos que ya estén implementados sin que sea necesaria una imagen del sistema, unirse al dominio o múltiples canales de comunicación con el dispositivo.

Con Ivanti Bridge, ahora las empresas pueden:

- Tener un control total sobre los PC con UEM
- Administrar los PC de forma remota e inalámbrica
- Reducir la necesidad de digitalización de equipos de sobremesa
- Hacer uso de comandos basados en GPO con secuencias de comandos Powershell implementados por UEM
- Editar y administrar fácilmente el registro
- Despliegue fácilmente aplicaciones Win32 no envueltas en MSI y aplicaciones Win32 Store
- Obtener visibilidad del sistema de archivos

Ivanti Bridge es compatible con dispositivos Windows 11+ y procesadores ARM. Ivanti Bridge no es compatible con dispositivos de escritorio de Windows 10 Home.

## Tipos de archivo compatibles con Bridge

Ivanti Bridge incluye la compatibilidad para los siguientes tipos de archivos:

- PowerShellLas secuencias de comando de PowerShell que se insertan en los dispositivos con Bridge admiten estos argumentos.Las secuencias de comandos de PowerShell de 64 bits son compatibles con los dispositivos de sobremesa Windows 10 de 64 bits.
- El tiempo de espera de Bridge en el lado del servidor para el resultado esperado tras enviar una secuencia de comandos de PowerShell es de aproximadamente 20 minutos. El tiempo de espera se registra como un Fallo. No obstante, la secuencia de comandos del dispositivo sigue funcionando.
  El tiempo de espera de Bridge en el lado del dispositivo para el proceso esperado de la ejecución de una secuencia de comandos de PowerShell es de aproximadamente 60 minutos. Tras 60 minutos, el proceso se cerrará, no se guardan los resultados de la secuencia de comandos y se envía un nuevo Fallo al servidor.
  Los tiempos de espera del lado del servidor y del lado del dispositivo están registrados como Errores. Si transcurre el segundo tiempo de espera y la secuencia de comandos genera algún resultado, no se registrará ningún resultado en el servidor.
  Registro
- Secuencias de comandos VB
- .EXE para implementación de aplicaciones Win32
- Las aplicaciones de Win32 Store utilizan la herramienta WinGet para instalar y desinstalar las aplicaciones.

Si el administrador necesita insertar archivos Win32 (.EXE) en un dispositivo (por ejemplo, como aplicación interna Windows, se utilizará la funcionalidad de Bridge automáticamente si estuviera disponible. Es obligatorio introducir un argumento para ejecutar de forma silenciosa al archivo (por ejemplo, /SILENT o /VERYSILENT).Las aplicaciones .EXE se instalan a través de Bridge usando el modo de administrador de PowerShell. En los dispositivos Windows, para instalar usando las credenciales del usuario, seleccione la opción «Ejecutado como usuario».

Los administradores deben seleccionar la casilla de verificación **Instalador ejecutado como usuario** en **Instalador de aplicaciones: ajustes** para instalar las aplicaciones para un usuario. No marque la casilla si desea que las aplicaciones se instalen a nivel de sistema.

Mediante Ivanti Bridge, el dispositivo se puede aumentar en las siguientes áreas clave.

- **Registro:** leer, escribir y actualizar valores del registro.
- **Archivos:** verificar, leer y actualizar contenidos de un archivo.
- **Implementación de aplicaciones:** añadir la posibilidad de instalar aplicaciones basadas en .EXE al dispositivo de sobremesa. Estas aplicaciones se pueden encontrar en los servidores de Ivanti Neurons for MDM o en una red de entrega de contenido (CDN, por sus siglas en inglés) en la nube.

## Configuración de Bridge

La configuración de Ivanti Bridge requiere que los administradores completen los pasos siguientes en el orden indicado:

1. [**Activación de las licencias de Bridge**](./Ivanti_Bridge.md)
2. [**Instalación de la aplicación Bridge**](./Ivanti_Bridge.md)
3. [**Cargar secuencias de comandos en los dispositivos**](./Ivanti_Bridge.md) para uso permanente o único en los dispositivos

### Activación de las licencias de Bridge

Ivanti Bridge forma parte del paquete Gold legado y del paquete actual de Secure UEM.

### Instalación de la aplicación Bridge

Después de desactivar las licencias de Ivanti Bridge, la aplicación móvil de Bridge se puede instalar de la siguiente manera:

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Haga clic en **+Añadir**.
3. Haga clic en **Ivanti Bridge** en la sección de Aplicaciones empresariales.
4. Añada los detalles, personalice y distribuya la aplicación móvil Bridge a los dispositivos necesarios según las licencias que haya obtenido.Si activó la opción **Instalación silenciosa en los dispositivos Windows**, la aplicación móvil Bridge se instalará en silencio y el servicio Bridge comenzará a ejecutarse en los dispositivos.

La aplicación Bridge se añade al Catálogo de aplicaciones por defecto, y también se distribuye por defecto a todos los dispositivos.

Tras importar la última versión de Ivanti Bridge (2.1.419.0) al catálogo del abonado, el administrador puede ver la versión recién alineada de la aplicación.

### Cargar secuencias de comandos en los dispositivos

Los administradores pueden cargar secuencias de comandos en los dispositivos para usarlos de forma permanente creando una nueva configuración de Bridge:

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuración > +Agregar**.
:::

:::WorkflowBlockItem
Seleccione la configuración de **Ivanti Bridge**.
:::

:::WorkflowBlockItem
Introduzca un nombre para la configuración.
:::

:::WorkflowBlockItem
Introduzca una descripción.
:::

:::WorkflowBlockItem
En la sección Establecimiento de la configuración, especifique los demás ajustes según se describe en la tabla del paso 7:
:::

:::WorkflowBlockItem
1. Ingrese los ajustes de la categoría **Archivo de la secuencia de comandos** para especificar una secuencia de comandos de instalación para ser insertado o ejecutado en los dispositivos.
2. (Opcional) Ingrese los ajustes de la categoría **Deshacer**&#xNAN;**&#x20;archivo de la secuencia de comandos** para especificar la secuencia de comandos de desinstalación que se insertará o ejecutará en los dispositivos. Esto es útil cuando, por ejemplo, se retira un dispositivo o se borra una configuración.
3. (Opcional) Seleccione la opción **Configurar Outlook** para configurar Microsoft Outlook en un dispositivo mediante Bridge.Solo es compatible con Outlook 2000 y 2013.
   Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione una distribución para esta configuración.Para estas acciones de los dispositivos se forzará el ingreso automáticamente.
:::
::::

| Categoría                        | Ajuste                                                 | Qué hacer                                                                                                                                                                                             |
| -------------------------------- | ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                  | Nombre                                                 | Introduzca un nombre que identifique a esta configuración.                                                                                                                                            |
|                                  | Descripción                                            | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                           |
| Archivo de secuencia de comandos | Todas las versiones (equipos de sobremesa Windows 10+) |                                                                                                                                                                                                       |
|                                  | Archivo de secuencia de comandos                       | Seleccione una secuencia de comandos válida o archivo ejecutable (.ps1, .reg, .exe).\* El archivo de secuencia de comandos o ejecutable especificado (.ps1, .reg, .exe) se ejecutará automáticamente. |

- Otros tipos de archivo solamente se copiarán el la carpeta de destino. |
  \|                                           | Argumentos de secuencia de comandos                    | Especifique la lista de argumentos para el archivo de la secuencia de comandos.\* En archivos Win32 (.exe), introduzca un argumento para ejecutar de forma silenciosa al archivo (por ejemplo, /SILENT o /VERYSILENT). Esto es obligatorio.                                    |
  \|                                           | Carpeta de destino                                     | Especifique la carpeta de destino para el archivo de la secuencia de comandos.\* Si no se especifica la carpeta de destino, se utilizará el valor de la variable del entorno del sistema %TEMP% como carpeta de destino.                                                       |
  \| Deshacer archivo de secuencia de comandos | Todas las versiones (equipos de sobremesa Windows 10+) |                                                                                                                                                                                                                                                                               |
  \|                                           | Archivo de secuencia de comandos                       | Seleccione una secuencia de comandos válida o archivo ejecutable (.ps1, .reg, .exe).\* El archivo de secuencia de comandos o ejecutable especificado (.ps1, .reg, .exe) se ejecutará automáticamente.
- Otros tipos de archivo solamente se copiarán el la carpeta de destino. |
  \|                                           | Argumentos de secuencia de comandos                    | Especifique la lista de argumentos para el archivo de la secuencia de comandos.\* En archivos Win32 (.exe), introduzca un argumento para ejecutar de forma silenciosa al archivo (por ejemplo, /SILENT o /VERYSILENT). Esto es obligatorio.                                    |
  \|                                           | Carpeta de destino                                     | Especifique la carpeta de destino para el archivo de la secuencia de comandos.\* Si no se especifica la carpeta de destino, se utilizará el valor de la variable del entorno del sistema %TEMP% de forma predeterminada.                                                       |

### Cargar secuencias de comandos a los dispositivos para un uso puntual

Los administradores pueden cargar una secuencia de comandos en los dispositivos para utilizarlos una sola vez (ad hoc).

1. Vaya a **Dispositivos > Dispositivos**.
2. Haga clic en el enlace con el nombre del dispositivo para ir a la página de detalles del Dispositivo. Este es el dispositivo de sobremesa Windows 10 donde se insertará/ejecutará la secuencia de comandos de uso puntual.
3. Haga clic en el icono

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
y en **Script y Acciones a través de Ivanti Bridge**.
:::

4. Introduzca nombre.
5. En la sección Archivo de la secuencia de comandos, especifique una secuencia de comandos para insertar/ejecutar en el dispositivo tal y como se describe en la tabla anterior.
6. Haga clic en **Aplicar**.La ejecución de la secuencia de comandos se pondrá en la cola y puede que tarde en completarse. Vaya a la pestaña Registros para comprobar y ver el estado (mensajes de salida y error). Para estas acciones de los dispositivos se forzará el ingreso automáticamente.

## Registros de Bridge

Esta función le permite extraer informes de Ivanti Bridge para dispositivos individuales, para aplicaciones de resolución de problemas y de diagnóstico. Los registros se envían la próxima vez que el dispositivo ingrese. Puede esperar a la próxima sincronización programada o realizar un registro forzado del dispositivo para obtener los registros rápidamente.

Para extraer los registros desde un dispositivo:

1. Vaya a **Dispositivos > Dispositivos**.
2. Haga clic en el enlace con el nombre del dispositivo para ir a la página de detalles del Dispositivo. Este es el dispositivo de sobremesa Windows 10 donde se insertará/ejecutará la secuencia de comandos de uso puntual.
3. Haga clic en el icono

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
y en **Extraer el registro de Ivanti Bridge**. Se muestra la ventana **Extraer registro de Ivanti Bridge**.
:::

4. Seleccione una de las siguientes opciones:**Un solo registro**: solicita a Ivanti Neurons for MDM que extraiga el registro de Bridge más reciente del dispositivo.**Todos los registros:** solicita a Ivanti Neurons for MDM extraer todos los registros (hasta 30 días) en el dispositivo.
5. Haga clic en **Extraer registro**. Una vez que el dispositivo lo haya enviado a Ivanti Neurons for MDM, puede ver el registro de Bridge en la pestaña Registros en la página Detalles del dispositivo.Solo los registros enviados mediante la opción **Todos los registros** pueden descargarse como un archivo ZIP únicamente.

## Último ingreso de Bridge

La columna última conexión de Bridge lista la fecha y hora de la última conexión del dispositivo Bridge en la página de Dispositivos. Se puede agregar la columna a la página Dispositivos mediante la opción Personalizar columnas y no es visible por defecto.

Para que esta columna sea visible, seleccione **Dispositivos** > **Personalizar columnas** > seleccione **Contacto de Bridge**.

Los datos exportados también tendrán los detalles de la última conexión de Bridge siempre que sea de aplicación.

## Recuperación de un fallo en el servicio de Bridge

Bridge Service Failure Recovery se ha introducido en Bridge 2.1.14. Por defecto, esta versión se importa al Catálogo de aplicaciones de todos los usuarios. En raras ocasiones, el Servicio de Bridge puede fallar sin un motivo conocido. En esos casos, la compatibilidad está disponible para Bridge 2.1.14 y versiones posteriores.
