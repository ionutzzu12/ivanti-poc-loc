---
title: Instalación del Certificado MDM
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Debe solicitar e instalar un certificado MDM de Apple para administrar los dispositivos iOS. También tendrá que renovar este certificado una vez al año. (La cuenta de Apple que se usó para crear el certificado recibe una notificación de la web de Apple cuando se acerca la fecha de caducidad). Utilice la página Certificado de MDM para agregar o renovar este certificado.

## Adquirir e instalar el certificado MDM

Procedimiento

1. Utilice la página **Certificado MDM** para descargar una solicitud de firma de certificados (CSR) desde el abonado su Ivanti Neurons for MDM.
2. Cargue el CSR en Apple para crear un certificado nuevo.
3. En el sitio de Apple, añada una nota indicando para qué es el certificado. Esta nota le resultará útil cuando sea el momento de renovarlo.
   Guarde el certificado resultante.
4. Instale el certificado de su abonado de Ivanti Neurons for MDM.

## Renovar el certificado MDM

Procedimiento

1. Haga clic en **Renovar certificado**.
2. Descargue una solicitud de firma de certificado (CSR) de su abonado de Ivanti Neurons for MDM.
3. Cargue el CSR en Apple para renovar el certificado correspondiente.
4. En el sitio de Apple, asegúrese de estar renovando el certificado correcto. Al cargar un certificado diferente en Ivanti Neurons for MDM se retirarán automáticamente todos los dispositivos iOS registrados.
   Instale el certificado de su abonado de Ivanti Neurons for MDM.

Recibirá una advertencia si intenta cargar el certificado incorrecto.

Si no puede ver la página **Instalar certificado de MDM**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Sistema de solo lectura
