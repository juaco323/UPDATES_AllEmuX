# Política de Privacidad de allEmu

Última actualización: 14 de octubre de 2026

allEmu es un emulador de escritorio gratuito y de código abierto. **No tiene
cuentas de usuario propias, no recopila telemetría ni estadísticas de uso y no
tiene servidores propios que almacenen tus datos.** Todo lo que configuras (ROMs,
partidas guardadas, carátulas, ajustes, tiempo de juego) permanece en tu
computadora. La única cuenta que puedes usar es, si quieres, la tuya de
RetroAchievements (ver más abajo).

## Qué se conecta a internet y por qué

| Función | A dónde se conecta | Qué se envía |
|---|---|---|
| Buscar actualizaciones | `updates-allemux.onrender.com` y GitHub (`github.com/juaco323/UPDATES_AllEmuX`) | Solo la solicitud para consultar la versión más reciente y descargar el instalador. |
| Descargar carátulas | GitHub (`github.com`, `api.github.com`, `raw.githubusercontent.com`) | El nombre del archivo o el identificador (CRC/ID) del juego, para solicitar su imagen. Solo cuando usas la sincronización de carátulas. |
| Imagen del canal (vista Canales Wii) | GitHub (`raw.githubusercontent.com`, repositorios `libretro-thumbnails`) | El nombre del juego, para descargar su pantalla de título o una captura. Solo al abrir un canal, y una sola vez por juego. |
| RetroAchievements (opcional) | `retroachievements.org` y `media.retroachievements.org` | Ver la sección siguiente. Solo si inicias sesión con tu cuenta. |
| Instalar Xenia (Xbox 360) | GitHub (`api.github.com`, repositorio `xenia-canary`) | Solo la solicitud de descarga. Solo cuando tú la inicias. |

Estas conexiones las reciben GitHub o Render, que pueden registrar datos
técnicos habituales de cualquier conexión web (como tu dirección IP), según sus
propias políticas de privacidad. allEmu no recibe ni almacena esos datos.

## RetroAchievements (opcional)

Si inicias sesión en **Ajustes → RetroAchievements** con tu cuenta de
[retroachievements.org](https://retroachievements.org), allEmu se comunica con
ese servicio para que ganes logros mientras juegas:

- **Al iniciar sesión** se envían tu usuario y tu contraseña a
  `retroachievements.org`, que responde con un token de sesión. allEmu guarda
  solo el usuario y ese token (en `config/retroachievements.cfg`), **nunca la
  contraseña**.
- **Al jugar** se envía un identificador del juego (un hash calculado a partir
  de la ROM, no la ROM en sí), los logros y puntajes de tablas que consigues, el
  modo (casual o hardcore), el texto de presencia del juego («Rich Presence») y
  la versión de allEmu y del núcleo usado. Las insignias se descargan de
  `media.retroachievements.org`.

RetroAchievements trata esos datos según sus
[condiciones legales](https://retroachievements.org/terms) y los muestra en
tu perfil público de ese sitio. Para dejar de enviar datos, usa **Cerrar
sesión**: el token se borra de tu computadora. Si no inicias sesión, allEmu no
se conecta con RetroAchievements.

## Estado en Discord (Rich Presence)

Si tienes Discord abierto, allEmu envía **a la aplicación de Discord instalada
en tu propia computadora** el título del juego, la consola (o, si usas
RetroAchievements, el texto de presencia del juego) y la hora de inicio de la
partida, para mostrarlos en tu perfil. allEmu no envía nada a internet
para esto: es Discord quien lo muestra a tus contactos, según la
[política de privacidad de Discord](https://discord.com/privacy).

Puedes desactivarlo en **Ajustes → Interfaz → Estado en Discord**. Al cerrar el
juego o la aplicación, el estado se elimina.

## Datos almacenados en tu computadora

Los ajustes (incluidos los propios de cada juego), controles, partidas
guardadas, carátulas, tiempo de juego (`config/playtime.json`) y, si usas
RetroAchievements, tu usuario y token de sesión se guardan en la carpeta de
instalación de allEmu. Al desinstalar la aplicación o eliminar esa carpeta,
se borran.

## Menores de edad

allEmu no recopila datos personales de nadie, incluidos los menores de edad.

## Cambios

Si esta política cambia, se actualizarán este archivo y su fecha. El historial
completo está disponible en este repositorio.

## Contacto

Para dudas o solicitudes, abre un *issue* en
[github.com/juaco323/UPDATES_AllEmuX/issues](https://github.com/juaco323/UPDATES_AllEmuX/issues).
