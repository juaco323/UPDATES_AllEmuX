# Política de Privacidad de allEmu

Última actualización: 10 de octubre de 2026

allEmu es un emulador de escritorio gratuito y de código abierto. **No tiene
cuentas de usuario, no recopila telemetría ni estadísticas de uso y no tiene
servidores propios que almacenen tus datos.** Todo lo que configuras (ROMs,
partidas guardadas, carátulas, ajustes) permanece en tu computadora.

## Qué se conecta a internet y por qué

| Función | A dónde se conecta | Qué se envía |
|---|---|---|
| Buscar actualizaciones | `updates-allemux.onrender.com` y GitHub (`github.com/juaco323/UPDATES_AllEmuX`) | Solo la solicitud para consultar la versión más reciente y descargar el instalador. |
| Descargar carátulas | GitHub (`github.com`, `api.github.com`, `raw.githubusercontent.com`) | El nombre del archivo o el identificador (CRC/ID) del juego, para solicitar su imagen. Solo cuando usas la sincronización de carátulas. |
| Instalar Xenia (Xbox 360) | GitHub (`api.github.com`, repositorio `xenia-canary`) | Solo la solicitud de descarga. Solo cuando tú la inicias. |

Estas conexiones las reciben GitHub o Render, que pueden registrar datos
técnicos habituales de cualquier conexión web (como tu dirección IP), según sus
propias políticas de privacidad. allEmu no recibe ni almacena esos datos.

## Estado en Discord (Rich Presence)

Si tienes Discord abierto, allEmu envía **a la aplicación de Discord instalada
en tu propia computadora** el título del juego, la consola y la hora de inicio
de la partida, para mostrarlos en tu perfil. allEmu no envía nada a internet
para esto: es Discord quien lo muestra a tus contactos, según la
[política de privacidad de Discord](https://discord.com/privacy).

Puedes desactivarlo en **Ajustes → Interfaz → Estado en Discord**. Al cerrar el
juego o la aplicación, el estado se elimina.

## Datos almacenados en tu computadora

Los ajustes, controles, partidas guardadas y carátulas se guardan en la carpeta
de instalación de allEmu. Al desinstalar la aplicación o eliminar esa carpeta,
se borran.

## Menores de edad

allEmu no recopila datos personales de nadie, incluidos los menores de edad.

## Cambios

Si esta política cambia, se actualizarán este archivo y su fecha. El historial
completo está disponible en este repositorio.

## Contacto

Para dudas o solicitudes, abre un *issue* en
[github.com/juaco323/UPDATES_AllEmuX/issues](https://github.com/juaco323/UPDATES_AllEmuX/issues).
