---
title: Ejemplos de espacios
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Este tema da ejemplos relacionados con cómo los administradores pueden utilizar los espacios.

## Administrador por localización

ACME, Inc. tiene oficinas en Norteamérica y Europa. Por cuestiones de idioma y zona horaria, ACME quiere tener un administrador en EE. UU. que administre los dispositivos de Norteamérica y otro administrador en Alemania que administre los dispositivos de Europa.

Para configurar estos espacios, ACME llevó a cabo los siguientes cambios:

1. Se ha creado un grupo de usuarios en Ivanti Neurons for MDM para usuarios de Europa.
2. Creó un grupo de usuarios en Ivanti Neurons for MDM para usuarios en Norteamérica.
3. Creó un espacio de Europa con la siguiente regla:
4. Grupo de usuarios = Europa
   Creó un espacio de Norteamérica con la siguiente regla:
5. Grupo de usuarios = Norteamérica
   Asignó la función de Administración de dispositivos de cada espacio al administrador adecuado.

Ahora, ACME cuenta con los siguientes espacios:

- Europa
- Norteamérica
- Predeterminada

## Administrador por SO por localización

ACME ha decidido que solo los expertos en Android deben administrar los dispositivos Android. Se ha añadido un experto en Android a la organización de Norteamérica y otro a la de Europa. En consecuencia, se necesitan dos nuevos espacios.

Para añadir los espacios, ACME llevó a cabo los siguientes cambios:

1. Creó un espacio de Europa-Android con las siguientes reglas:
2. Grupo de usuarios = Europa
   OS = Android
   Creó un espacio de Norteamérica-Android con las siguientes reglas:
3. Grupo de usuarios = Norteamérica
   OS = Android
   Asignó la función de Administración de dispositivos de cada espacio al administrador adecuado.

Ahora, ACME cuenta con los siguientes espacios:

- Europa-Android
- Norteamérica-Android
- Europa
- Norteamérica
- Predeterminada

## Administrador para ejecutivos

Los ejecutivos de ACME han decidido que quieren recibir un servicio especial de un administrador especial. Solo los ejecutivos más importantes están en esta lista.

Para añadir este espacio, ACME llevó a cabo los siguientes cambios:

1. Creó un espacio de ejecutivos con las siguientes reglas:
2. Nombre de usuario = [**pruiz@acme.com**](mailto\:pruiz@acme.com)
   Nombre de usuario = [**gmontero@acme.com**](mailto\:gmontero@acme.com)
   Nombre de usuario = [**aperez@acme.com**](mailto\:aperez@acme.com)
   Nombre de usuario = [**fayuso@acme.com**](mailto\:fayuso@acme.com)
   Movió el espacio a la parte superior de la lista de la página **Espacio**.
3. De lo contrario, los ejecutivos con dispositivos Android tendrían el administrador equivocado.
   Asignó la función de Administración de dispositivos del espacio al administrador especial.

Ahora, ACME cuenta con los siguientes espacios:

- Equipo directivo
- Europa-Android
- Norteamérica-Android
- Europa
- Norteamérica
- Predeterminada

## Administrador para todos los demás dispositivos

Cuando ACME abra una nueva oficina en Japón, los dispositivos que se añadan se asignarán al administrador del espacio predeterminado hasta que alguien cree un espacio de Japón.
