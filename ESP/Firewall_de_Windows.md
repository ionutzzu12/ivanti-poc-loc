---
title: Firewall de Windows
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

La configuración del Firewall de Windows permite configurar los ajustes del perfil del cortafuegos de Windows, así como el conjunto deseado de reglas personalizadas que se aplicarán en el dispositivo. Esta configuración se puede utilizar para administrar dispositivos que no sean del dominio y para reducir el riesgo de amenazas a la seguridad en la red en todos los sistemas que se están conectando a la red corporativa.

## Configuración del Firewall de Windows

**Procedimiento**

1. Vaya a **Configuración > +Agregar**.
2. Seleccione la configuración de **Cortafuegos**.
3. Haga clic en el icono de **Windows**.
4. Introduzca un nombre para la configuración.
5. Introduzca una descripción para la configuración del cortafuegos.
6. En la sección Establecimiento de la configuración, especifique los demás ajustes según se describe en la siguiente tabla.| Ajuste                           | Qué hacer                                                                                                                                                                             |
   \| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Perfiles**                     |                                                                                                                                                                                       |
   \| Activar                          | Deslice el control deslizante hacia Activado (ON) para activar el perfil.                                                                                                             |
   \| Tipo                             | Muestra el tipo de perfil.Ejemplo: Dominio.                                                                                                                                           |
   \| Acción de entrada predeterminada | Seleccione una opción para la acción predeterminada que debe realizarse cuando haya tráfico de entrada.**Permitir**: para permitir el tráfico.**Bloquear**: para bloquear el tráfico. |
   \| Acción de salida predeterminada  | Seleccione la acción predeterminada que debe realizarse cuando haya tráfico de salida.**Permitir**: para permitir el tráfico.**Bloquear**: para bloquear el tráfico.                  |
7. Para agregar Reglas, haga clic en **+Agregar** y configure los ajustes siguientes:| Ajuste                        | Qué hacer                                                                                                                                                                                                                                                    |
   \| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   \| **Reglas**                    |                                                                                                                                                                                                                                                              |
   \| ENCENDIDO                     | Deslice el control deslizante para activar el perfil.                                                                                                                                                                                                        |
   \| Nombre de la regla            | Introduzca un nombre que identifique esta regla.                                                                                                                                                                                                             |
   \| Descripción                   | Introduzca una descripción que explique el objetivo de esta regla.                                                                                                                                                                                           |
   \| Dirección                     | Seleccione la dirección del tráfico hacia la cual debe aplicarse la regla:\* **Entrada**: para el tráfico de entrada
   - **Salida**: para el tráfico de salida
   - **Ambas**: en ambas direcciones                                                                |
     \| Acción                        | Seleccione la acción que se realizará:\* **Permitir**: para permitir el tráfico.
   - **Bloquear**: para bloquear el tráfico.                                                                                                                                    |
     \| Perfil                        | Seleccione el(los) perfil(es) a los que debe aplicarse la regla:\* **Todos**
   - **Dominio**
   - **Privado**
   - **Pública**                                                                                                                                        |
     \| Aplicación                    | Escriba el nombre de familia del paquete (PFN, en inglés) o la ruta completa hacia el ejecutable de la aplicación.                                                                                                                                           |
     \| Protocolo                     | Seleccione cualquiera de los siguientes protocolos a los que debe aplicarse la regla:\* **TCP**
   - **UDP**
   - **ICMP**                                                                                                                                          |
     \| Rangos de direcciones locales | Escriba los rangos de direcciones IPv4/IPv6 locales o máscaras de subred.                                                                                                                                                                                    |
     \| Rangos de puertos locales     | Escriba una lista separada por comas de los puertos locales o los rangos de puertos.Ejemplos: 20,50,100-120.                                                                                                                                                 |
     \| Rangos de direcciones remotas | Escriba los rangos de direcciones IPv4/IPv6 remotas o máscaras de subred.                                                                                                                                                                                    |
     \| Rangos de puertos remotos     | Escriba una lista separada por comas de los puertos locales o los rangos de puertos.Ejemplos: 20,50,100-120.                                                                                                                                                 |
     \| Tipos de interfaz             | Seleccione cualquiera de las siguientes opciones de tipo de interfaz:\* **Todos**
   - **Acceso remoto**
   - **Inalámbrico**
   - **LAN**
   - **Banda ancha móvil**La opción predeterminada **Todos** se aplica si no se selecciona ninguna opción de tipo de interfaz. |
8. Haga clic en **Siguiente**.
9. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
   - Ningún dispositivo (predeterminada)
   - personalizada
10. Haga clic en **Hecho**.
