# Portal Mesa NT

Página del portal **Mesa NT** — captura de avisos de mercado/logística y promociones
de producto que los clientes ven en la pestaña Mercado de la NT App.

- **Hosting**: GitHub Pages de este repo. La página es estática porque Supabase no
  permite servir HTML en `*.supabase.co`.
- **URL estable para el equipo**: `https://borouviqngtdzfvlmlur.supabase.co/functions/v1/mesa-portal`
  (redirector 302 a esta página; el destino vive en `app_config.mesa_portal_url`).
- **Publicar cambios**: la página se sirve de la rama `gh-pages` (Pages clásico) — al actualizar, empuja a `main` Y a `gh-pages`.
- **Fuente de verdad**: `mesa/index.html` en el repo `nt-portal-app` — se edita ALLÁ y
  se copia aquí. Cero llaves en la página: la clave del equipo vive en el servidor
  (`app_config.mesa_clave`) y la API es la edge function `mesa-nt`.
