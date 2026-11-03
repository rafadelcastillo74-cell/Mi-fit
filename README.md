# MY LIFE TRACKER

Aplicación web progresiva (PWA) en español para registrar suplementos, entrenamientos y sueño.

## Publicar en GitHub Pages
1. Crea un repositorio en GitHub.
2. Sube `index.html`, `manifest.webmanifest` y `sw.js` a la raíz.
3. En Settings → Pages, selecciona Deploy from a branch, `main` y `/ (root)`.
4. Abre la URL HTTPS generada desde Safari o Chrome.
5. En iPhone: Compartir → Añadir a pantalla de inicio. En Android: menú de Chrome → Instalar aplicación.

## Almacenamiento
Los datos se guardan en IndexedDB del navegador. Exporta periódicamente una copia JSON desde la pestaña Copias. Restaurar sustituye los datos actuales. Borrar datos del sitio/navegador puede eliminar la base local.

## Alcance
La puntuación de sueño se introduce manualmente desde Samsung Health u otra fuente; no hay integración automática con sensores ni con Samsung Health. El catálogo de ejercicios es una selección amplia y ampliable, no una lista literalmente exhaustiva.
