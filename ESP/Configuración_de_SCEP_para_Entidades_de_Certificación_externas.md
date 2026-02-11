---
title: Configuración de SCEP para Entidades de Certificación externas
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Esta función permite la configuración de Simple Certificate Enrollment Protocol (SCEP) para autoridades de certificación externas para dispositivos Windows 10.

La opción de delegación con distribución personalizada está disponible para esta configuración. Para obtener más información, consulte el tema *Distribuir la configuración* en [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).

### Configurar una Entidad de Certificación externa

Primero debe configurar una EC externa. Puede pasar a la siguiente sección si ya tiene una EC externa.

1. Vaya a **Administración > Infraestructura > Administración de certificados**.
2. Haga clic en **+Añadir**.
3. Introduzca un nombre para la Entidad de Certificación.
4. Use el menú desplegable para seleccionar Microsoft como el **Tipo de entidad de certificación**.
5. Introduzca la **URL de SCEP**.
6. Introduzca el **Nombre de usuario** y la **Contraseña**.
7. Introduzca la **URL de comprobación**.
8. Haga clic en **Guardar**.

### Configuración SCEP

Ahora puede proceder con la configuración SCEP.

1. Vaya a **Configuración > +Añadir**.
2. Seleccione el icono de Windows.
3. Seleccion&#x65;**&#x20;Certificado de identidad&#x20;**&#x70;ara ir a la págin&#x61;**&#x20;Crear configuración del certificado de identidad**.
4. Introduzca un nombre para la configuración.
5. Seleccione **Configuración de Windows** de la lista de configuraciones SCEP del menú desplegable **Distribución de certificados**.
6. Seleccione la EC externa.
7. Introduzca los detalles de distribución de certificados.\* Introduzca el asunto. Por ejemplo: CN=$\{userEmailAddress}
   - Seleccione el número de intentos en el menú desplegable **Reintento**.
   - Seleccione el número de segundos a esperar antes de cada entrada en el menú desplegable **Retraso en el reintento**.
   - Seleccione un tamaño de clave del menú desplegable **Longitud de clave**.
   - Seleccione al menos una opción de uso del certificado.
   - Introduzca el tiempo en el campo **Validez** y el menú desplegable.
   - Introduzca la Huella digital de la EC.
   - Vaya a la URL de SCEP challenge, copie la huella CA y péguela aquí o haga clic en **Crear desde un certificado**... para cargar el certificado desde el que se puede crear la huella de CA.
     Seleccione al menos un algoritmo hash de las opciones **Familia de algoritmos hash**.
8. Haga clic en **Siguiente**.
