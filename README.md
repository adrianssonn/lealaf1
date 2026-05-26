# LEALA F1 — proyecto fragmentado con auto-carga de datos

## Estructura

```
proyecto/
├── index.html
├── css/styles.css
├── js/app.js
├── data/
│   ├── data.json          · datos del Mundial (KB) — se carga AUTO
│   └── data_media.json    · imágenes base64 (MB) — respaldo
├── docs/                  · tipografías
├── exports/               · exportaciones
└── assets/                · imágenes (archivos físicos)
    ├── cards/ cars/ drivers/ flags/ head/ layouts/
    ├── logos/ news/ photos/ sponsors/ teams/ trophies/ ui/
```

## Cómo abrir (IMPORTANTE)

La auto-carga de `data/data.json` requiere servidor HTTP. **Con file://
NO funciona** por seguridad del navegador. Desde esta carpeta:

```
python3 -m http.server 8000
```

Y abre http://localhost:8000

## Comportamiento

1. Al abrir la primera vez (localStorage vacío) → carga AUTO `data/data.json`.
2. Los cambios que hagas (nuevos resultados, etc.) se guardan en localStorage.
3. Si quieres volver al estado original del JSON sin tocar imágenes:
   - Consola del navegador (F12): `recargarDatosMundial()`

## Imágenes

Las imágenes se cargan desde `assets/...` (archivos físicos). Si por
algún motivo necesitas tener todas las base64 originales otra vez,
puedes importar `data/data_media.json` con la función de importación
de la app.

## Funciones de consola

- `limpiarImagenesLocales()` → borra imágenes base64 de localStorage.
- `recargarDatosMundial()` → vuelve a cargar data/data.json.

## Convenciones de nombres en assets/

- Banderas: `flags/{pais}_flag.webp` o `{pais}Sq_flag.webp`.
- Trazados: `layouts/{circuito}_layout.webp`.
- Coches: `cars/{escuderia}_cars.webp`.
- Escudos: `teams/esc_{escuderia}_small.webp`.
- Pilotos: `drivers/driver_{slug}.webp` y `cards/card_{slug}.webp`.
- Logos institucionales: `logos/f1_logo.webp`, `logos/fia_logo.webp`, `logos/warca_logo.webp`.

Slug = nombre en minúsculas, sin acentos, con `_` en lugar de espacios.
