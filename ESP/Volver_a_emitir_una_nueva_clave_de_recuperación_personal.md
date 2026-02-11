---
title: Volver a emitir una nueva clave de recuperación personal
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** dispositivos macOS con Mobile\@Work para macOS 1.66 o versiones más recientes compatibles.

Al migrar desde otras soluciones MDM a Ivanti Neurons for MDM, los administradores pueden solicitar al sistema operativo que vuelva a emitir una nueva clave de recuperación personal (PRK, en inglés) en el momento de la inscripción, si ya se emitió una PRK previamente antes de la inscripción. Esto permite almacenar la clave en Ivanti Neurons for MDM.

Puede ver las entradas del registro de Trazas de auditoría para las actividades PRK de la siguiente manera:

1. Vaya a **Panel de control > Audit Trails**.
2. El filtro Tipo, seleccione **Clave personal de recuperación.** Las entradas de PRK aparecerán en la categoría de Administración de dispositivo y actividades como “Clave personal de recuperación vista”.

**Requisito previo**

Distribuya las siguientes configuraciones a los dispositivos antes de realizar este procedimiento:

- Configuración de Mobile\@Work para macOS.
- Configuración de la Clave de recuperación de FileVault.

**Procedimiento**

1. Póngase en contacto con la [**asistencia técnica**](./Abrir_un_tique_de_asistencia.md) para solicitar la secuencia de comandos para generar una nueva PRK en el dispositivo.
2. Cree un atributo personalizado del dispositivo con el nombre «deviceprk» que se utilizará en la secuencia de comandos.
3. Suba el script al repositorio en **Admin > Todos los scripts**. Mientras lo hace, seleccione el atributo personalizado «deviceprk».
4. Cree un grupo de dispositivos dinámico para los dispositivos en los que no se ha recuperado la PRK de la antigua solución de MDM. Seleccione las reglas del grupo de dispositivos de la siguiente manera: «**Platform=macOS&#x20;**&#x61;n&#x64;**&#x20;Encryption Enabled is equal to Yes** and **macOS Personal Recovery Key escrowed is equal to No** and **macOS Recovery Key Type is equal to Personal**» («Plataforma=macOS y Cifrado habilitado es igual a Sí y Clave de recuperación personal de macOS en custodia es igual a No y Tipo de clave de recuperación de macOS es igual a Personal»).
5. Cree una configuración de secuencia de comandos de Mobile\@Work para macOS en la que se pueda seleccionar la secuencia de comandos de la PRK del repositorio. Distribuya la configuración al nuevo grupo de dispositivos.
6. Programe la secuencia de comandos para que se ejecute una vez al día o según desee. Esta secuencia de comandos pedirá la contraseña de usuario cada vez que se ejecute. De forma predeterminada, el período de tiempo de espera para la ejecución de la secuencia de comandos es de 60 segundos. Se recomienda ampliar el periodo de tiempo de espera en la configuración correspondiente de Mobile\@Work para macOS estableciendo el campo **Max Run Time** en 300 segundos.

- La clave descifrada está disponible en la página de detalles del dispositivo de un dispositivo de la sección Estado de cifrado del dispositivo. Haga clic en **Ver** junto al campo Cifrado de FileVault habilitado.
- Al obtener la PRK, el dispositivo se sale del grupo de dispositivos. Por lo tanto, la configuración de la secuencia de comandos ya no será aplicable y se eliminará del dispositivo.
- Una vez que MDM recupere la clave de recuperación de un dispositivo utilizando la secuencia de comandos, este se desinstalará del dispositivo.

Temas relacionados:

- [**Atributos**](./Atributos.md)
- [**Todas las secuencia de comandos**](./Todas_las_secuencia_de_comandos.md)
- [**Grupos de dispositivos**](./Grupos_de_dispositivos.md)
- [**Mobile@Work para macOS**](./Mobile@Work_para_macOS.md)
