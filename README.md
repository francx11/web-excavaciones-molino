# Web Excavaciones Molino E Hijos S.L.

Web estática lista para GitHub Pages. Un único archivo `index.html` — sin servidor, sin dependencias.

## Ver en local

```bash
python -m http.server 8080
# Abrir: http://localhost:8080
```

O simplemente abre `index.html` en el navegador (el formulario de contacto no funcionará en `file://`, el resto sí).

## Despliegue en GitHub Pages

1. Ve a **Settings → Pages**
2. Source: `Deploy from a branch`
3. Branch: `main` / `/ (root)`
4. Guarda. En ~2 minutos estará en: `https://francx11.github.io/web-excavaciones-molino/`

## Dominio propio (opcional)

Si el cliente tiene dominio (ej. `excavacionesmolino.es`):
1. Edita el archivo `CNAME` y escribe el dominio sin `https://`
2. En el DNS del dominio añade un registro `A` apuntando a:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. En GitHub Pages activa "Enforce HTTPS"

## Placeholders que el cliente debe rellenar

Busca `[PLACEHOLDER]` en `index.html` y reemplaza:

| Placeholder | Qué poner |
|---|---|
| `[CIF]` | CIF/NIF de la empresa |
| `[AÑOS_EXPERIENCIA]` | Años en activo (ej: 20) |
| `[NUM_VEHICULOS]` | Nº de vehículos propios |
| `[NUM_PROYECTOS]` | Proyectos realizados (aprox.) |
| `[FORMSPREE_ID]` | ID del formulario en formspree.io |

## Formulario de contacto (Formspree — gratis)

1. Crea cuenta en [formspree.io](https://formspree.io) con el email `transportesmolinoehijos@gmail.com`
2. Crea un nuevo formulario
3. Copia el ID (parte final de la URL, ej: `xpzgkdba`)
4. En `index.html` busca `[FORMSPREE_ID]` y reemplaza por ese ID

## Imagen OG (redes sociales)

Reemplaza `assets/og-image.jpg` con una foto real de 1200×630 px.
Buenas opciones: maquinaria en obra, equipo, o fachada del negocio.

## SEO — pasos post-lanzamiento

1. Añade la web a [Google Search Console](https://search.google.com/search-console)
2. Valida los datos estructurados en [Rich Results Test](https://search.google.com/test/rich-results)
3. Comprueba el rendimiento en [PageSpeed Insights](https://pagespeed.web.dev)
