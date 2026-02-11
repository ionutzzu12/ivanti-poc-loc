---
title: Configuración de comprobación de revocación de certificados
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta configuración permite a los administradores comprobar una serie de certificados revocados de un dispositivo. Los administradores pueden especificar una autoridad de certificación (CA) que permite que la configuración habilite la comprobación de revocación para todos los certificados que están vinculados a esa CA.

Aplicable a: iOS 14.2+ y visionOS 1.1+

**Procedimiento**

1. Vaya a Configuraciones > +Añadir.
2. Escriba certificado en el campo de búsqueda y, a continuación, haga clic en la configuración de Configuración de comprobación de revocación de certificado.
3. Introduzca un Nombre y Descripción de la configuración.
4. Seleccione un algoritmo como SHA 256 e introduzca la Hash del certificado raíz.En Hash, tiene que introducir un hash SHA-256 codificado en Base64 (binario) de la clave pública del certificado. Consulte [**Documentación de Apple**](https://support.apple.com/en-us/HT209143) para los certificados de raíz confiable de los sistemas operativos Apple. Puede añadir varios certificados raíz en esta configuración.
5. Haga clic en Siguiente.
6. Seleccione la opción Habilitar esta configuración.
7. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
   - Ningún dispositivo (predeterminada)
   - Personalizado.
8. Haga clic en Hecho.
