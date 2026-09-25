# Protocolo: Proyecto 9

App para organizar el protocolo de tesis de Valen (Proyecto 9, CUAAD 2026B): apartados, bibliografía, documentos, pendientes "atorados" y un reporte de "Avance para la maestra". Publicada en https://vmmterminus-star.github.io/protocolo-p9/

## Cómo está hecha
- Todo vive en un solo `index.html` (HTML + CSS + JS juntos). No hay que instalar ni compilar nada.
- Fuente: Alexandria. Color de tema: `#2E5266`.
- Íconos y manifest van embebidos en el `<head>`.
- Busca datos de fuentes por DOI en la API de Crossref (`api.crossref.org`).

## Datos (¡cuidado!)
- Se guardan en `localStorage` con la clave `protocolo_v1`. Hace respaldos automáticos con el prefijo `protocolo_v1_respaldo_`.
- Sincronización opcional con Supabase: ella captura la URL y la llave en Ajustes, y se guardan en `protocolo_supa`. Otras claves: `protocolo_synccode`, `protocolo_local_ts`, `protocolo_remote_ts`.
- Tiene descarga de respaldo `.json`.
- Nunca cambies nombres de claves ni la forma de los datos sin migrar lo que ya existe.

## Cómo trabajar con Valen
- Valen no programa. Explícale todo en español sencillo, sin tecnicismos.
- Antes de subir cualquier cambio: abre la app en el navegador integrado, prueba el cambio (también en tamaño celular) y revisa la consola.
- Enséñale el resultado. Haz commit y push a `main` solo cuando ella diga que sí. En ~1 minuto queda en línea.
- El repo es público: nada de contraseñas ni datos personales aquí.
