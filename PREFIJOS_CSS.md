# LEALA F1 — Glosario de prefijos CSS

Referencia rápida para saber a qué sección de la app pertenece cada clase CSS.

---

## Prefijos de sección principal

| Prefijo | Significado completo | Dónde aparece |
|---|---|---|
| `cvr-` | **cover** | Portada — el grid de celdas, el slideshow hero, los logos institucionales |
| `cover-` | **cover (sistema antiguo)** | Portada — versión anterior, código muerto, ya no se usa |
| `cd-` | **circuit detail** | Detalle de un circuito/GP — bandera, foto país, trazado, histórico, nota de prensa |
| `cal-` | **calendar** | Pestaña Calendario — las bandas de cada GP, banderas, fechas |
| `st-` | **standings** | Pestaña Clasificación — filas de pilotos, chips de resultados, banda WARCA |
| `champ-` | **championship** | Título "LEALA F1 WORLD CHAMPIONSHIP 2026" en cabeceras |
| `team-` | **team** | Pestaña Escuderías — tarjetas de equipos, logos, estadísticas |
| `td2-` | **team detail v2** | Detalle de una escudería — foto coche, palmarés, estadísticas combinadas |
| `pr-` | **profile** | Perfil de un piloto — foto, nombre, estadísticas generales |
| `prr-` | **profile race row** | Cada fila del historial de carreras dentro del perfil del piloto |
| `pstat-` | **profile stat** | Bloque de estadística individual dentro del perfil (victorias, poles, etc.) |
| `pen-` | **penalty** | Pestaña Sanciones — tarjetas de sanciones, logo FIA, tipo de sanción |
| `duel-` | **duel** | Pestaña Duelo (VS) — comparativa entre dos pilotos |
| `tt-` | **time trial** | Pestaña Contrarreloj — resultados de clasificación |
| `hem-` | **hemeroteca** | Pestaña Hemeroteca — archivo de noticias antiguas |
| `warca-` | **WARCA** | Elementos relacionados con la marca WARCA (noticias, WTV, WET365) |
| `vid-` | **video** | Sección WTV — reproductor y lista de vídeos |

---

## Prefijos de componentes transversales

Estos aparecen en varias pestañas a la vez.

| Prefijo | Significado completo | Qué es |
|---|---|---|
| `app-` | **app** | Estructura global — nav, footer, vistas principales |
| `nav-` | **navigation** | Barra de navegación superior — botones, logo WARCA, menú WARCA |
| `btn-` | **button** | Botones genéricos reutilizables |
| `auth-` | **authentication** | Botón del candado admin, modal de PIN |
| `badge-` | **badge** | Escudo/logo de un equipo en formato pequeño |
| `logo-` | **logo** | Logos institucionales (F1, FIA, WARCA) |
| `palm-` | **palmarés** | Banda de trofeos — tanto en perfil de piloto como en escudería |
| `chip-` | **chip** | Chips de resultado de carrera (los cuadraditos de colores en clasificación) |
| `race-` | **race** | Elementos relacionados con una carrera — chips, filas de resultado |
| `pos-` | **position** | Número de posición en clasificaciones |
| `pts-` | **points** | Caja de puntos (la caja roja con los puntos totales) |
| `trend-` | **trend** | Flecha de tendencia (↑↓) junto a los puntos |
| `stat-` | **stat** | Bloque de estadística genérico |
| `photo-` | **photo** | Contenedor de foto con hint de subida |
| `up-` | **upload** | Botones y zonas de subida de imágenes |
| `form-` | **form** | Formularios del panel admin |
| `warn-` | **warning** | Mensajes de advertencia |

---

## Prefijos de elementos visuales específicos

| Prefijo | Significado completo | Qué es |
|---|---|---|
| `tri-` | **triangle** | Los triángulos decorativos encima y debajo de los chips de resultado |
| `dot-` | **dot** | Fila de puntos decorativos (separadores visuales) |
| `big-` | **big** | Títulos grandes de sección |
| `re-` | **result** | Fila de resultado dentro del detalle de un GP |
| `qualy-` | **qualifying** | Columna o fila de clasificación (qualy) |
| `after-` | **after GP** | Columna "Después del GP" en el detalle de circuito |
| `sc-` | **safety car** | Indicador de safety car en resultados |
| `evo-` | **evolution** | Banda de evolución del campeonato en el perfil del piloto |
| `gp-` | **grand prix** | Elemento de GP en listados |
| `pin-` | **pin** | Modal y campo de PIN de administrador |
| `tstat-` | **team stat** | Estadística de equipo |
| `tbg-` | **team background** | Fondo de color del equipo |
| `fgb-` | **foreground background** | Degradado de fondo decorativo |
| `pis-` | **pista / circuit** | Elementos del trazado del circuito |
| `fire-` | **fire** | Animación de fuego decorativa |
| `cr-` | **card race** | Tarjeta de resultado de carrera |

---

## Prefijos de modo y estado

| Prefijo | Significado completo | Qué es |
|---|---|---|
| `light-` | **light mode** | Reglas específicas del modo día |
| `theme-` | **theme** | Botón de cambio de tema día/noche |
| `admin-` | **admin** | Elementos visibles solo en modo administrador |
| `next-` | **next GP** | Elementos del próximo GP (sin resultado aún) |
| `has-` | **has (estado)** | Modificador de estado (ej: `.has-photo`) |
| `no-` | **no (negación)** | Modificador de ausencia (ej: `.no-results`) |
| `last-` | **last** | Modificador del último elemento de una lista |

---

## Prefijos de layout genérico

| Prefijo | Significado completo | Qué es |
|---|---|---|
| `fia-` | **FIA** | Logo y elementos de la FIA |
| `bet-` | **bet (WET365)** | Elementos de la sección de apuestas WET365 |
| `font-` | **font** | Panel de selección de tipografías en Admin |

---

## Regla general de nomenclatura

```
[sección]-[elemento]-[modificador]

cd-hero-flag        → circuit detail → zona hero → bandera
pr-stats-band       → profile → banda de estadísticas
td2-palm-slot       → team detail v2 → palmarés → hueco individual
prr-pos             → profile race row → posición
```

Cuantas más letras tiene el prefijo, más específico es el elemento dentro de su sección padre.
