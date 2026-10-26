# Boceto del sitio público de NUVYRA

Boceto de diseño en HTML estático (fase 2). **No forma parte de la aplicación y no cambia nada de ella.**

## Cómo verlo
Abre `index.html` con doble clic (no necesita servidor ni internet). Las páginas se enlazan entre sí.

| Página | Archivo |
|---|---|
| Inicio | `index.html` |
| Producto (disponible hoy, en desarrollo y cadena prevención–operación) | `producto.html` |
| Seguridad | `seguridad.html` |
| Quiénes somos | `nosotros.html` |
| Contacto (canales y formulario) | `contacto.html` |
| Ingresar | `login.html` |

## Qué es de ejemplo
- Las pantallas del producto son capturas de la aplicación real con **datos ficticios** del servidor de pruebas (nombres, empresa «Minera Andes» y puntajes inventados). Cada una lleva su leyenda.
- El formulario de contacto y el de ingreso **no envían nada**.
- Contacto: «Próximamente» hasta que existan canales oficiales. No se publica ningún teléfono ni correo.
- No hay logos de clientes, testimonios, cifras ni certificaciones: no existen.

## Cómo está hecho
- Un solo CSS (`estilos.css`) con los mismos colores y tipografía de la aplicación (Source Sans 3, alojada aquí en `fonts/`; licencia SIL OFL 1.1).
- Sin JavaScript ni recursos externos: coincide con la política de contenido del sitio (`frontend/public/_headers`).
- Menú móvil con `<details>`; adaptable a escritorio, tableta y celular, sin desplazamiento horizontal.
- Las capturas se regeneran con `frontend/e2e-capture/sitio.spec.ts` (`playwright.capture.config.ts`).

## Pendiente antes de llevarlo a la aplicación
Canal de contacto real, política de privacidad y términos, dominio, y revisar el análisis de las páginas de referencia (aún sin acceso de red).

## Qué se publica sobre seguridad (criterio)
- Se dice **qué protege al cliente** (datos separados por empresa, registro de actividad, permisos por rol, acceso protegido), no **cómo está hecho**.
- No se publican: tecnologías y proveedores, umbrales (intentos, plazos), qué roles tienen o no verificación en dos pasos, estado de la documentación de la API, detalles de respaldos ni de cómo se calcula o verifica cada dato.
- Los informes internos (`docs/AUDITORIA-*`, `docs/ANALISIS-*`) describen debilidades conocidas: **el repositorio debe seguir privado** y esos archivos no se publican en el sitio.
