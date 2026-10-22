# Enigma Studio · Landing y catálogo

Sitio estático publicado con GitHub Pages mediante GitHub Actions.

## Estructura
- `site/index.html` — la página (no hace falta tocarla para cambiar productos).
- `site/catalogo.json` — productos, precios, medidas, personalización, fotos y ajustes (WhatsApp, Instagram, texto de bienvenida).
- `.github/workflows/pages.yml` — despliega `site/` en cada push a `main` que cambie algo en `site/`.

## Primera vez
1. Sube estos archivos a un repo (rama `main`).
2. En el repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Haz un push (o corre el workflow a mano desde la pestaña Actions). La URL aparece en el resumen del job.

## Editar el catálogo
1. Abre `https://<tu-usuario>.github.io/<repo>/#editar`.
2. Agrega o edita productos y ajustes. El borrador se guarda en tu navegador.
3. Pulsa **Descargar catalogo.json**.
4. Reemplaza `site/catalogo.json` en el repo (Add file → Upload files, o commit desde tu máquina).
5. El workflow vuelve a publicar en uno o dos minutos.

El modo `#editar` solo cambia la copia de tu navegador: nadie puede modificar el sitio sin hacer commit en el repo.

Las fotos van dentro de `catalogo.json` comprimidas (máx. 900 px, JPEG). Con muchos productos el archivo crece; si pasa de unos 20–30 MB conviene mover las fotos a `site/fotos/`.
