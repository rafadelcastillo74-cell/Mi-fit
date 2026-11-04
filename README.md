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


## Calendario integrado (versión 2)
La pestaña Calendario muestra el mes, permite avanzar y retroceder por meses y días, y reúne suplementos previstos y tomas registradas, ejercicios/entrenamientos y registros de sueño. Desde el detalle de un día puedes marcar una toma o deshacer la última. Los entrenamientos y el sueño aparecen automáticamente al guardarlos en sus secciones.


## Versión 3
- **Inicio = tu día de hoy**: marca cada suplemento como tomado (o todos a la vez), y ve de un vistazo qué has cumplido hoy de suplementos, ejercicio y sueño, con accesos rápidos para registrar entrenamiento o sueño.
- **Calendario**: cada día muestra su resumen (suplementos, ejercicio, sueño). El punto de suplementos es verde si completaste las tomas y rojo si quedaron pendientes en un día pasado. Puedes marcar/deshacer tomas de cualquier día, añadir tomas fuera de plan, y saltar a registrar entrenamiento o sueño con esa fecha ya puesta. Resumen mensual bajo el calendario.
- **Datos**: se guardan en IndexedDB (se pide al navegador almacenamiento persistente). La pestaña Copias muestra la fecha de tu última copia y la pantalla de Inicio avisa si llevas 14 días o más sin exportar.
- Correcciones: la fecha "hoy" usa tu hora local (antes podía adelantarse de noche), la navegación por meses ya no salta de mes en los días 29-31, y borrar un entrenamiento o un registro de sueño actualiza el calendario. Ahora también puedes eliminar registros de sueño.
- El service worker usa "red primero", así que las actualizaciones se ven al recargar. Al subir esta versión a GitHub Pages, abre la app una vez con conexión y recarga.
