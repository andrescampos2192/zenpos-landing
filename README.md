# Landing — Zentrix Software / ZenPos

Sitio web estático (marketing) de **Zentrix Software** y su producto **ZenPos**.
Se publica en Netlify → **zentrixsoftware.com**.

- `index.html` — home de la empresa (Zentrix Software).
- `zenpos.html` — landing detallada del producto ZenPos (IA-first).
- `fonts/` — Plus Jakarta Sans self-hosted (sin CDN externo).
- Imágenes (`*.png`), `sitemap.xml`, `robots.txt`, verificación de Google.

## Regla de oro 🔒
Este repo es **solo el sitio estático**. **NUNCA** agregar aquí:
credenciales, `.env`, claves de BD, ni código del sistema (PL/SQL, `f150.sql`, etc.).
Si algo no es HTML/CSS/JS/imagen/fuente de la web pública, no va en este repo.

## Cómo editar y publicar

1. Editá `index.html` o `zenpos.html` (todo el CSS/JS va inline, self-contained).
2. Previsualizá abriendo el archivo en el navegador, o con un server local:
   ```bash
   npx serve .
   # o:  python -m http.server 8080
   ```
3. Guardá los cambios en git y subilos:
   ```bash
   git add -A
   git commit -m "landing: <qué cambiaste>"
   git push
   ```
4. **Netlify despliega solo** en cuanto llega el push a `main` (continuous deploy).
   En ~1 min los cambios están en vivo en zentrixsoftware.com.

## Notas
- Mantener **cero dependencias externas** (el único link externo permitido es `wa.me`).
  Las fuentes están self-hosted en `fonts/` a propósito.
- Al cambiar imágenes de Open Graph o el `sitemap.xml`, actualizar la fecha `lastmod`.
- No romper el `prefers-reduced-motion` ni meter horizontal scroll (probar en móvil ~390px).
