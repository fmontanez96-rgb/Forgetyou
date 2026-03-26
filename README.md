# Colección de Saludos de Doblaje

Aplicación web estática construida desde cero para gestionar una colección de videos de saludos de actores de doblaje.

## Funcionalidades

- Mapa principal de universos con cantidad de videos.
- Vista por universo con tarjetas por personaje.
- Reproducción embebida de videos de YouTube.
- Filtros por personaje, actor de doblaje y rareza.
- Sistema de rarezas: Común, Raro, Épico y Legendario.
- Versiones alternativas por personaje con botón “Ver versiones”.
- Modo Maratón con reproducción encadenada y contador “X de Y”.
- Índice de personajes por universo con cantidad de versiones.
- Pantalla de logros con desbloqueados y pendientes.

## Estructura de datos usada

Cada elemento de la colección usa:

- `id`
- `universo`
- `personaje`
- `actor_de_doblaje`
- `url_video`
- `rareza`
- `version` (opcional)

## Estructura de vistas y convención de estilos

- Las vistas principales se construyen desde funciones `render*View()`:
  - `renderMapView()`: mapa interactivo de universos.
  - `renderUniverseView()`: tablero del universo seleccionado, filtros y reproducción.
  - `renderAchievementsView()`: estado de logros desbloqueados.
- Se estandarizó una capa de componentes reutilizables en `index.html` para mantener consistencia visual y facilitar nuevas pantallas:
  - `.hud-panel`: contenedor base para secciones.
  - `.stat-card`: tarjeta reutilizable para elementos de contenido.
  - `.neon-btn` y `.neon-btn--primary`: botones con glow/hover uniforme.
  - `.terminal-list`: listas secundarias con estilo técnico.
  - `.section-title` y `.section-subtitle`: jerarquía de títulos y subtítulos.
- La animación de entrada (`fade`) y transiciones de hover/glow comparten las mismas variables para una experiencia homogénea en todas las vistas.

## Uso

Abrir `index.html` en cualquier navegador moderno.
