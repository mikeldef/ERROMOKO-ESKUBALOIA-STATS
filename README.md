# Erromoko Eskubaloia — Handball Stats 2.0

Web responsive para registrar estadísticas de partidos de balonmano desde móvil u ordenador. Diseño en tonos burdeos inspirado en las publicaciones de Erromoko Eskubaloia. HTML, CSS y JavaScript sin librerías externas ni cuotas de IA.

## Novedades de esta versión
- Interfaz adaptada a móvil, con botones grandes y navegación sencilla.
- Paleta burdeos/rosa claro.
- Estadísticas separadas para:
  - Penalti provocado a favor en ataque.
  - Penalti cometido en defensa (penalti en contra).
  - Exclusión a favor provocada en ataque.
  - Exclusión provocada en defensa (se mantiene como estadística independiente).
- Las nuevas acciones aparecen en la tabla de estadísticas por jugador, en el editor de acciones y en el CSV exportado.

## Funciones
- Plantilla editable con dorsal, nombre y posición.
- Cronómetro, pausa y cambio de parte.
- Registro de acciones asociadas a jugador y minuto.
- Entradas/salidas de pista y cálculo de minutos.
- Marcador derivado de goles y goles recibidos.
- Corrección y eliminación de acciones.
- Estadísticas por jugador, historial y exportación CSV.
- Copia de seguridad y restauración JSON.
- Caché para abrir la web sin conexión tras la primera visita.

## Publicar online gratis con Cloudflare Pages
No necesitas comprar dominio ni pagar por tokens. La URL gratuita será del tipo `https://nombre.pages.dev`.

1. Descarga y descomprime el ZIP.
2. En GitHub crea un repositorio llamado `erromoko-handball-stats`.
3. Sube **los tres archivos** `index.html`, `manifest.json` y `sw.js` directamente a la raíz del repositorio (no subas la carpeta contenedora como una carpeta extra).
4. Entra en https://dash.cloudflare.com/ y crea/inicia sesión en una cuenta gratuita.
5. Abre **Workers & Pages** → **Create** → **Pages** → conecta GitHub y selecciona el repositorio.
6. Si pide configuración, elige sin comando de compilación (None) y usa la raíz del proyecto como directorio de salida.
7. Pulsa **Deploy**. Cloudflare generará una URL pública.
8. Abre esa URL en el móvil. En Android/Chrome, abre el menú del navegador y pulsa **Añadir a pantalla de inicio**. En iPhone/Safari, pulsa **Compartir** → **Añadir a pantalla de inicio**.

## Importante sobre los datos
Esta versión guarda la plantilla y los partidos en el almacenamiento local de cada navegador. **La web es online, pero los datos todavía no se sincronizan entre dispositivos.** Por ejemplo, un partido guardado en tu móvil no aparecerá automáticamente en el ordenador. Para compartir datos entre varios dispositivos habría que conectar una base de datos y autenticación, por ejemplo Supabase con políticas de acceso seguras.

Haz una copia JSON periódica desde la pestaña Historial. Tras publicar, abre la web una vez con conexión para que se almacenen los archivos necesarios para el modo sin conexión.

## Uso
1. Entra en Plantilla y añade los jugadores.
2. En Partido, selecciona al jugador antes de registrar una acción.
3. Usa los botones de entrada/salida para calcular minutos.
4. En Estadísticas consulta las columnas nuevas y exporta CSV para Excel.
5. Al terminar, pulsa Nuevo partido para guardar el encuentro en el historial.
