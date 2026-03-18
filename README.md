# Forgetyou

Mini experiencia web estática para convertir historias en cartas fantásticas medievales.

## Nuevo: generación de imagen con IA

La página ahora ofrece dos modos de ilustración:

- **Ilustración local (SVG):** todo sucede en el navegador y no requiere servicios externos.
- **IA real con OpenAI:** usa el endpoint oficial de generación de imágenes para producir una ilustración más cercana a lo que describe la historia.

### Importante para GitHub Pages

Como este proyecto es estático, **no debes incrustar una API key dentro del código**. La implementación actual pide la key al usuario en pantalla y la guarda solo en `sessionStorage` mientras esa pestaña siga abierta.

Si quieres una integración realmente segura para producción, lo ideal es mover la llamada a OpenAI a un backend o serverless function.
