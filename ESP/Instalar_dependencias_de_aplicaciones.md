---
title: Instalar dependencias de aplicaciones
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Cuando carga un paquete de aplicaciones internas, Ivanti Neurons for MDM escanea la aplicación para identificar las dependencias. Si se encuentra alguna dependencia, las enumera en el tercer paso del asistente Añadir aplicación. Para cualquier dependencia de la aplicación, los administradores pueden optar por cargar un archivo de dependencia. No obstante, es posible que algunas aplicaciones no se instalen sin cargar el archivo de dependencias.

El administrador tiene la opción de ajustar la dependencia de la aplicación cuando instala una aplicación concreta. En tal caso, puede haber una o más aplicaciones etiquetadas con la aplicación principal. Cuando un usuario intenta instalar la aplicación principal, el usuario se notificará sobre las aplicaciones dependientes que se instalarán con la aplicación principal.

Esta función es compatible con los dispositivos iOS, Android, Windows, y macOS.

Tenga en cuenta los siguientes puntos sobre las dependencias de la aplicación y los requisitos previos:

- El administrador puede configurar las aplicaciones dependientes que son requisitos previos para que se pueda instalar una aplicación en un dispositivo. Una aplicación de requisito previo puede ser una aplicación interna, pública, privada (Android) o una VPP.
- El recuento de aplicaciones de requisitos previos ahora se muestra en la columna Aplicaciones de requisitos previos en la página Catálogo de aplicaciones. Puede pasar el ratón sobre el número para ver la lista de aplicaciones de requisitos previos.
- Una aplicación que es requisito previo se descarga directamente una vez que la aplicación principal se activa para la instalación.
- Si se delega una aplicación principal, las aplicaciones asociadas que son requisitos previos se delegan automáticamente.
- No puede eliminar una aplicación que es requisito previo del catálogo de aplicaciones hasta que se elimine la relación de requisito previo.
- Varias versiones de una aplicación pueden tener diferentes aplicaciones que son requisitos previos.
- La página Seguimiento de auditoría registra si se añaden, eliminan o se delegan automáticamente los requisitos previos de las aplicaciones de iOS, Android y macOS.
- Si el administrador o el usuario fina instala una aplicación que tiene aplicaciones de requisito previo, éstas se instalan antes que la aplicación principal. Si se realiza un registro de dispositivo antes de que se instalen todas las aplicaciones de requisitos previos, todas las aplicaciones de requisitos previos se desinstalarán.

Si bien una aplicación necesita un archivo de dependencia, Ivanti Neurons for MDM no requiere que usted cargue ningún archivo para implementar una aplicación.

Para dispositivos Samsung, el administrador debe agregar aplicaciones de requisito previo a la lista de aplicaciones permitidas del modo kiosko. Las aplicaciones que son prerrequisito que estén agregadas a la lista de Aplicaciones permitidas no se agregan a la lista de aplicaciones de la Lista negra.

Para dispositivos distintos a Samsung, si la aplicación principal se agrega a la lista de aplicaciones permitidas del modo kiosko, la aplicación de requisito previo se deberá ejecutar en segundo plano. Puede ver una aplicación de requisitos previos en modo Kiosko solo si el administrador ajusta esta aplicación en modo quiosco.

**Dispositivos de Windows**: si la aplicación Bridge es un requisito previo que no se distribuye, y la aplicación principal es un ejecutable que se distribuye en segundo plano. Cuando se elimina la dependencia, se desinstalará la aplicación Bridge, pero después de este paso, el archivo .exe falla. El administrador debe asegurarse de que la aplicación de Bridge no esté sin distribuir por defecto.

**Dispositivos de Windows**: cuando la aplicación principal no se distribuye en segundo plano y la aplicación principal tiene una aplicación de requisito previo sin distribución, se instala correctamente la aplicación de requisito previo. No obstante, si la aplicación principal no se instala correctamente, inmediatamente se desinstalará la aplicación de requisito previo. El reintento de la aplicación principal fallida se produce solo cuando el usuario desencadena una solicitud de instalación.

## Añadir una aplicación interna

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Haga clic en **Añadir**.
3. Arrastre el archivo de la aplicación hasta el cuadro punteado o haga clic en **Elegir archivo** para seleccionarlo del sistema de archivos y haga clic en **Confirmar**.
4. Haga clic en **Siguiente** (abajo a la derecha). Ivanti Neurons for MDM examina la aplicación para encontrar archivos de dependencias y los enumera en la tabla **Dependencias de la aplicación**.
5. Revise la información de la aplicación y verifique que ha seleccionado la aplicación correcta.
6. Haga clic en el icono de Cargar, en la columna Acciones.**** Aparecerá la ventana **Cargar dependencia**.
7. Haga clic en **Elegir archivo** para examinar y encontrar una copia local del archivo y, a continuación, haga clic en **Cargar**.
8. Ivanti Neurons for MDM escanea los paquetes opcionales de la aplicación, si los hay, y los enumera en la tabla de paquetes opcionales. Si aparece en la lista, haga clic en el icono de Cargar, en la columna Acciones. Aparece la ventana de carga de paquetes opcionales.
9. Revise la información de la aplicación y verifique que ha seleccionado la aplicación correcta.
10. Haga clic en **Elegir archivo** para examinar y encontrar una copia local del archivo y, a continuación, haga clic en Cargar.
11. Haga clic en **Siguiente**.
12. (Opcional) Añada capturas de pantalla de la aplicación y haga clic en **Siguiente**.
13. Si la aplicación requiere otras aplicaciones de requisitos previos.1) Seleccione la opción **Sobre** desde el **Aplicaciones de requisitos previos** sección.
    2\) Busque la solicitud de requisitos previos bajo la pestaña **Añadir aplicaciones**.
    3\) Seleccione las aplicaciones.
    4\) Haga clic en **Guardar**.
14. Defina la distribución de aplicaciones y haga clic en **Siguiente**.
15. Defina la sección de Configuración de la aplicación y haga clic en **Listo**. La próxima vez que los dispositivos se sincronicen con Ivanti Neurons for MDM, la aplicación se implementa en el dispositivo junto con los archivos de dependencia.Puede añadir dependencias adicionales haciendo clic en el botón Añadir dependencias. Una vez cargadas, estas dependencias adicionales también aparecerán enumeradas en la tabla Dependencias de la aplicación. El administrador también puede agregar manualmente un paquete opcional solo con el tipo de contenido. Este tipo de paquete no depende de la versión.

## Añadir una aplicación de requisito previo

Puede agregar una aplicación de requisito previo a una aplicación principal. Puede añadir diferentes requisitos previos para diferentes versiones de una aplicación principal. La página del catálogo de aplicaciones le brinda la opción de mantener la descripción, las secuencias de comandos, las capturas de pantalla, la distribución, los requisitos previos de la aplicación y las configuraciones de la aplicación igual que la versión de la aplicación existente o cambiar las aplicaciones requeridas asociadas. No puede eliminar una aplicación de requisito previo sin eliminar la asociación con la aplicación principal.

- La página Seguimiento de Auditoría ahora muestra las aplicaciones de requisitos previos admitidas en campos específicos de la siguiente manera\:La sección Prerrequisitos de aplicaciones de las aplicaciones de iOS,Android, y macOS de la página Seguimiento de auditoría muestra los campos siguientes:\* appVersionId
  - nombre
  - platformAppIdSe muestran las aplicaciones de requisitos previos que se delegan automáticamente o no se delegan y que contienen los siguientes campos:\* dmPartitionDistributionType
  - dmPartitionDistributionReason

**Procedimiento**

1. Seleccione una aplicación del **Catálogo de aplicaciones**.
2. Haga clic en **Editar**.
3. Desplácese hacia abajo hasta **Delegación de aplicaciones** y seleccione la opción **Delegar esta aplicación a todos los espacios**.
4. Haga clic en **Guardar**.Si delega varias aplicaciones y elige eliminar la delegación de la aplicación principal, la aplicación de requisito previo no se eliminará de la delegación automáticamente.
