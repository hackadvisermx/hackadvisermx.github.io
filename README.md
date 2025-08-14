# hackadviser // blog (Hugo + PaperMod)

Blog minimalista de hacking y ciberseguridad.

## 🚀 Puesta en marcha (local)
1. Instala Hugo **extended** (comprueba con `hugo version`).
2. Clona este repo y añade el tema PaperMod como submódulo:
   ```bash
   git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod
   ```
3. Levanta el sitio:
   ```bash
   hugo server -D
   ```

## 📦 Despliegue con GitHub Pages
- GitHub Actions ya está configurado en `.github/workflows/pages.yml`.
- Haz push a `main` y en **Settings → Pages** selecciona **GitHub Actions**.

## ✍️ Crear posts
```bash
hugo new posts/mi-primer-post.md
# edita el archivo y pon draft: false
```

## 🧩 Extras
- Comentarios: integra Giscus (PaperMod lo soporta).
- Analíticas sin cookies: Plausible o GoatCounter.
- Búsqueda local: Lunr/Fuse.

## 🔒 Legal
- Usa este repo solo con fines educativos y éticos.
