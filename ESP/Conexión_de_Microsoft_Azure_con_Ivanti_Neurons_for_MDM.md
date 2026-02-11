---
title: Conexión de Microsoft Azure con Ivanti Neurons for MDM
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Procedimiento

1. Inicie sesión en Ivanti Neurons for MDM y vaya a **Administración** > **Microsoft Azure**.
2. En el panel de navegación izquierdo, haga clic en **Microsoft Azure** > **Conformidad del dispositivo**.
3. En la sección Conectar cuenta, proporcione los detalles siguientes:\* Id. del inquilino de Azure: búsquelo en su instancia de Microsoft Azure.
   - URL de inscripción (opcional): si el dispositivo no está inscrito en MDM, los usuarios del dispositivo serán dirigidos a esta URL para la inscripción. Al realizar la configuración, utilice el formato HTTPS. Si hospeda una página en su organización para que redirija a los usuarios de dispositivos para obtener información de Inscripción, añada ese enlace aquí.
   - URL de corrección (opcional): si el dispositivo no está conforme, los usuarios del dispositivo serán dirigidos a esta URL para su corrección. Al realizar la configuración, utilice el formato HTTPS. Si hospeda una página en su organización para que redirija a los usuarios de dispositivos para obtener información sobre corrección, añada ese enlace aquí.
4. Haga clic en Conectar cuenta. Se abre el cuadro de diálogo Validación de abonados de Azure.

Los abonados actualmente conectados a Azure y que deseen agregar conformidad de dispositivos para dispositivos macOS deben desconectar la cuenta y luego restablecer la conexión.

1. En el cuadro de diálogo Validación de abonados de Azure, haga clic en el enlace del paso 1.
2. Iniciar sesión.
3. Revise los permisos y haga clic en Aceptar.

Si se conecta y la página le pide que vuelva a conectarse, cierre la pestaña/ventana del navegador.

1. Volver a Ivanti Neurons for MDM. En la casilla de diálogo Conectar cuenta de Azure, marque la casilla de verificación He dado mi consentimiento. Haga clic en Confirmar.

- Para editar la cuenta, haga clic en Editar la cuenta.
- Para desconectar la cuenta, haga clic en Desconectar la cuenta. Para obtener más instrucciones, consulte [**Cancelar el aprovisionamiento del inquilino de Azure**](./Cancelar_el_aprovisionamiento_del_inquilino_de_Azure.md).
- Toda la actividad de adición, edición y desactivación de una cuenta se almacena en los Registros.
