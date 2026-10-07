# Rastreo de migración

Corte: ejecución local de esta revisión. Robots público permite sitio y restringe wp-admin; declara sitemap.xml y sitemap.rss. sitemap.xml/sitemap_index.xml apuntan a cuatro sitemaps hijos: post, page, elementor-hf, category. Los cuatro fueron descargados y parseados: 26 URLs de páginas únicas (6 artículos, 12 páginas, 2 plantillas Elementor y 6 categorías).

Rastreo por enlaces/medios descubrió 227 URLs literales internas y realizó 53 solicitudes. No son 227 páginas: incluye CSS, JS, imágenes y variantes. 26 respuestas 200, una 404 de /cdn-cgi/l/email-protection y 26 respuestas 429 (límite del servidor); después de una pausa el 429 persistió y se detuvieron reintentos. No considerar 429 como ausencia ni errores SEO confirmados. Algunas páginas pendientes podrían contener más enlaces. No se afirma inventario exhaustivo de URLs huérfanas ni de Google; Search Console aún procesa datos.

## Redirecciones añadidas en data/redirects.yml

- nuestra-historia → nosotros.
- estudios → nosotros, sección trayectoria-formacion.
- servicios → inicio, sección areas: es el resumen de las dos áreas vigentes, no fingir equivalencia con Civil.
- Seis archivos category (uncategorized, licencia, militar, estudios, horarios, futuro) → biblioteca completa: agrupa artículos existentes, no a home. No inventar categorías nuevas para archivos heredados mínimos.
- PDF de informe jornada antiguo en wp-content → copia original local renombrada.

Diez reglas adicionales, destinos finales sin cadenas. Comprobar fragmentos y reglas generadas tras build y en Pages antes de conectar dominio. Mantener rutas conservadas de militar, administrativo, contacto y legales.

## Retiradas sin destino equivalente

- /derecho-civil/: servicio expresamente excluido. No redirigirlo a Militar ni home como falso equivalente. Recomendación: 410 explícito al lanzar si el hosting lo permite; si no, 404 real, no soft-404. No implementado como cambio de infraestructura.
- /elementor-hf/footer/ y /elementor-hf/cabecera/: plantillas técnicas que el sitemap anterior publicaba; no contenido útil nuevo. 404/410, no redirección a home.
- MP4 antiguo FALTAS-LEVES: restaurado por petición posterior de Loren; redirección directa a `/u/videos/procedimiento-falta-leve.mp4`, ahora optimizado. Artículo canónico `/articulo/procedimiento-falta-leve/`; el alias `/articulos/procedimiento-falta-leve/` redirige a él. Documentos trasladados a `/u/recursos/`, conservando redirects directos de sus rutas anteriores.
- CSS/JS/plugin assets WordPress y endpoint Cloudflare email-protection no se migran como páginas. Imágenes históricas: inventario pendiente si deben preservarse enlaces externos directos; no redirigir todas a un logo.

## Infraestructura pendiente, no modificada

Canonicalizar http/https y www conservando path y query mediante regla de host/HTTPS en Cloudflare; comprobar no cadenas con redirects de ruta. No emitir wildcard a home. Sitemap y robots nuevos generados deben anunciar dominio canónico y excluir plantillas, páginas noindex y borradores según decisión editorial. Una URL Pages no es privada por carecer de dominio conectado.

Inventario de 26 URLs en [rastreo-sitemap.csv](rastreo-sitemap.csv), con estado observado (429 no conclusivo). Fuentes públicas: https://jumalegal.com/robots.txt y sitemaps hijos arriba. Evidencia de respuestas y 227 URLs guardada fuera del repo; el clon no depende de ella para conocer las decisiones.
