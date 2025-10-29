# Dev Jobs

Sitio estático de ejemplo para mostrar ofertas y empresas del mundo tech. Incluye una portada con buscador, listados de posiciones destacadas y sección de empresas.

## Propósito
- Proveer una landing simple para oportunidades laborales en tecnología.
- Servir como base para iterar diseño, accesibilidad y funciones de búsqueda/filtrado.
- Publicarse fácilmente como sitio estático (sin backend).

## Estructura de archivos
- `index.html`: Página principal (hero con buscador, listados y footer).
- `code.html`: Página secundaria de ejemplo (puedes reutilizar su estructura o eliminarla si no se usa).
- `style.css`: Hoja de estilos principal (variables CSS, efectos hover/transiciones, grid responsive y soporte claro/oscuro automático con `prefers-color-scheme`).
- `background.jpg`: Imagen del hero.
- `bytedance.png`, `intel.png`, `oracle.png`, `meta.jpg`: Logos/imágenes usadas en secciones.
- Otros assets pueden cargarse desde URLs remotas directas en el HTML.

## Cómo editar
- Contenido: abre `index.html` y `code.html` en tu editor. Actualiza títulos, textos de secciones, tarjetas de empleo y enlaces de navegación.
- Imágenes: reemplaza las imágenes en la carpeta raíz o ajusta los atributos `src` en el HTML. Mantén textos `alt` descriptivos para accesibilidad.
- Estilos: el proyecto usa `style.css` enlazado en `index.html`. Personaliza colores editando las variables en `:root`; ajusta tipografías, grids y efectos hover/transiciones según tus secciones.
- Tema: el CSS respeta `prefers-color-scheme` (claro/oscuro) automáticamente. Si quieres un selector manual y recordar la preferencia, añade un pequeño script que alterne una clase en `<html>` y guarda la elección en `localStorage`.
- Accesibilidad: revisa `alt`, `aria-label` y jerarquía de encabezados (`<h1>` único) antes de publicar.
- Codificación: guarda los archivos en UTF-8 para evitar caracteres extraños.

## Vista previa local
- Opción rápida: haz doble clic en `index.html` para abrirlo en el navegador.
- Opción recomendada: usa una extensión de servidor local (por ejemplo, Live Server en VS Code) para autorecarga al guardar.

## Despliegue
### Netlify (sin build)
1. Conecta tu repositorio: New site from Git → elige el repo.
2. Build command: deja vacío; Publish directory: raíz del repo (`/`).
3. Alternativa rápida: arrastra y suelta la carpeta del proyecto en la UI de Netlify (Deploys → Drag & Drop).

### GitHub Pages
1. Crea un repositorio en GitHub y agrega el remoto desde tu carpeta local:
   - `git remote add origin https://github.com/<usuario>/<repo>.git`
   - `git branch -M main` (opcional)
   - `git push -u origin main` (o `master` si usas esa rama)
2. En GitHub: Settings → Pages → Source: "Deploy from a branch".
3. Selecciona la rama (`main` o `master`) y la carpeta `/ (root)`.
4. Guarda. Tu sitio quedará disponible en `https://<usuario>.github.io/<repo>/`.

## Futuras mejoras
- Selector de tema (claro/oscuro) manual con persistencia en `localStorage`.
- Buscador real con filtrado por palabra clave, ubicación y etiquetas.
- Contenido dinámico desde JSON o API (sincronizar listados reales).
- Mejores prácticas de accesibilidad (contraste, foco visible, navegación por teclado).
- SEO: metadatos, Open Graph, favicon, manifest y sitemap.
- CI/CD: despliegues automáticos (Netlify/GitHub Actions) en cada `push`.
- Extender estilos a `code.html` y unificar componentes.

¿Quieres que agregue un selector de tema y lo deje funcionando?

