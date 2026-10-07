# Pendientes antes del lanzamiento

## Integraciones y legales

- Formulario aún sin envío probado: no afirmar recepción/autorrespuesta. Backend, antispam, privacidad, confirmación y entregabilidad necesitan pruebas. Email como vía explícita, no simulación de formulario.
- GA4 `G-5GJ2SPD9V8` conservado del repo; validar titularidad, consentimiento/eventos y ausencia de datos personales en analítica. No cambiar IDs por intuición ni certificar cumplimiento por tener banner.
- Overrides legales adaptados para revisión. Confirmar titular jurídico, condición autónomo/sociedad y NIF, tratamientos/proveedores efectivos y validación final de quien asesore al cliente. Ya recibidos ICAMUR 8075 y domicilio fiscal: no repetir petición genérica.
- Experto Militar: falta denominación completa, institución y fecha. No bloquea integración. No exportarlo como credencial concreta ni inventar la entidad.
- Por decisión de Loren, retirados los avisos públicos de pendientes de legales/cookies/privacidad. Es una limpieza editorial, no una validación legal ni habilitación para publicar. Siguen sin confirmar identidad jurídica/NIF del prestador y responsable, bases de cada tratamiento, intereses legítimos si los hay, criterios/plazos efectivos de consultas sin encargo, clientes y registros, proveedores de correo/alojamiento/analítica, contratos, transferencias, inventario de cookies/almacenamiento (identificador, titular, finalidad, duración y datos), y pruebas de aceptar/rechazar/retirar consentimiento. No trasladar tablas antiguas de SESS/Analytics/YouTube ni afirmar cumplimiento. Los controles y derechos sustantivos permanecen en público.

## IRPF visible en entorno de revisión

Loren pidió retirar draft para que Manuel pueda verlo. No significa validación jurídica independiente del caso. Artículo accesible bajo `/articulo/exencion-irpf-misiones-otan/`, con redacción atribuida a Juma y sin detalles identificantes de unidad, ejercicio, duración o misión concreta.

CGPJ acredita criterio Supremo, no caso particular TEAR. Falta confirmar año/referencia/resolución anonimizada y alcance (anulación, rectificación, devolución e intereses), permiso de publicación conforme al secreto profesional y vías/plazos. La fecha de preparación del archivo no debe confundirse con fecha del pleno ni resolución. Entorno sin dominio vinculado según Loren, pero una URL técnica Pages puede ser pública: no prometer privacidad.

## Sociales

Observación 05/10/2026, cuadrícula Instagram: icono de view count; IPEC `DYScJIytAxx` 60.7K aproximadas, destino `DdZandEKNNv` 1331. Orden priorizado entre candidatas comparables, no catálogo ni ranking exhaustivo. Muestra de 15 reels con views; historia `DW4V876Dfq4` sin views verificadas, separada biográfica. TikTok sin reproducciones visibles verificadas, 637 eran likes. No mostrar cifras efímeras ni extrapolar popularidad a leads. Mantener enlaces fuente en secciones.

## Publicación y controles

Loren autorizó commit y push de los cambios actuales del submódulo y Juma para continuar en local. Main es la rama de trabajo; no crear rama adicional por iniciativa. Esto no autoriza conectar el dominio ni nuevos cambios de infraestructura.

Comprobar redirects antiguos de artículos y enlaces /u/, siete artículos visibles para revisión (seis históricos y nuevo IRPF), overrides legales, JSON-LD real, CMS generado y responsive. Public/ y recursos son outputs, no fuente. No afirmar CMS editado/guardado remotamente: no login ni guardado GitHub autorizado.

## Límites detectados en verificación final

- El theme procesa Hero desde uploads y lo sirve en `/fonts/hero-700.woff2`, no `/u/fonts/`; el archivo generado debe compararse con la fuente.
- JSON-LD exporta LegalService, área, perfiles y catálogo. La revisión fijada no exporta `org.mail` como email. Su objeto `logo` reutiliza referencia/dimensiones de imagen principal en el grafo, aunque el SVG se carga correctamente en página: corregir en una tarea explícita de theme si se quiere validar ese detalle. No modificar output como workaround.
- La salida de GA4 contiene arranque con `isCk=true`: consentimiento aún no auditado, no declarar control correcto de analítica solo por existir banner.
- Apertura/guardado interactivos de CMS no completados; esquema generado y construcción sí comprobados.
- Revisión de autor y MP4: build de producción completo en copia aislada, JSON-LD real de los siete artículos con autor `https://jumalegal.com/autor/manuel-acosta/#schema-person`, `ProfilePage`/`Person`, cinco credenciales verificadas y LinkedIn exacto. En la recuperación inicial, vídeo original y fotograma real generados por el build con hash idéntico. Posteriormente Loren autorizó optimización web: versión y controles actualizados en [assets.md](assets.md); no confundir su hash con el original. No se intervino el servidor Hugo del usuario.
- Limitaciones nativas adicionales del tema: el `ImageObject` principal que referencia `Person.image` carece de `url`/`contentUrl` y hereda dimensiones del poster (1280 × 960), aunque el retrato informal real y sus derivados se sirven correctamente (1600 × 1479). `VideoObject` del hero exporta `contentUrl`/`embedUrl` relativos y omite duración; portada y fecha editorial sí son correctas. No añadir schemas paralelos ni editar el tema sin autorización específica. Verificación visual/reproducción interactiva y guardado CMS no realizados en esta revisión.
