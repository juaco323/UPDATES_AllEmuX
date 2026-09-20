# UPDATES_AllEmuX

Canal de actualizaciones de **allEmu** (Tauri updater + hosting estático en Render).

## Qué va acá

| Archivo | Uso |
|---------|-----|
| `latest.json` | Manifiesto que consulta la app |
| `releases/` | Artefactos firmados (`.nsis.zip` + `.sig`) **o** enlaces en el JSON a GitHub Releases |

No subas núcleos, ROMs ni el código de la app.

## Flujo al publicar una versión

1. En `allEmu_x`, build con `createUpdaterArtifacts` y firma (`TAURI_SIGNING_PRIVATE_KEY`).
2. Copiá el instalador/updater + `.sig` a `releases/` (o a un GitHub Release de este repo).
3. Actualizá `latest.json`: `version`, `notes`, `pub_date`, `url` y `signature`.
4. `git push` → Render redeploy del Static Site.

## Render

- Tipo: **Static Site**
- Repo: `juaco323/UPDATES_AllEmuX`
- Publish directory: `./`
- URL pública (ejemplo): `https://<tu-servicio>.onrender.com/latest.json`

Cuando tengas la URL de Render, configurá en `allEmu_x`:

```json
"plugins": {
  "updater": {
    "endpoints": ["https://<tu-servicio>.onrender.com/latest.json"],
    "pubkey": "<clave pública minisign>"
  }
}
```

## Formato `latest.json` (Tauri v2)

```json
{
  "version": "0.1.1",
  "notes": "Cambios de esta versión",
  "pub_date": "2026-09-20T00:00:00Z",
  "platforms": {
    "windows-x86_64": {
      "signature": "<contenido del .sig>",
      "url": "https://<tu-servicio>.onrender.com/releases/allEmu_0.1.1_x64-setup.nsis.zip"
    }
  }
}
```
