# Nor Consulting — Sitio web informativo

Sitio estático (HTML/CSS/JS puro, sin build) basado en el branding de Nor Consulting:
navy `#002D62`, dorado `#E8A13B`, blanco y gris claro `#F4F6F8`, tipografías Montserrat + Open Sans.

## Estructura
```
nor-consulting/
├── index.html        → Home
├── nosotros.html      → Sobre Nor Consulting
├── servicios.html      → Servicios
├── contacto.html      → Contacto (formulario visual, sin backend aún)
├── css/styles.css      → Sistema de diseño (colores, tipografía, componentes)
├── js/main.js          → Menú móvil, animaciones al hacer scroll, formulario
├── assets/logo.svg      → Isologo
├── assets/favicon.svg    → Favicon
└── vercel.json         → Config de deploy (URLs limpias)
```

## 1. Subir el código a GitHub

Desde la carpeta `nor-consulting`:

```bash
git init
git add .
git commit -m "Sitio Nor Consulting v1"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/nor-consulting.git
git push -u origin main
```

Si aún no tienes el repo creado en GitHub: entra a github.com → **New repository** →
nómbralo `nor-consulting` → **Create repository** (sin README, sin .gitignore, para no chocar
con estos archivos) → copia la URL que te da y úsala en el `git remote add origin`.

## 2. Publicar gratis en Vercel

**Opción A — desde la web (recomendado, sin instalar nada):**
1. Entra a [vercel.com](https://vercel.com) e inicia sesión con tu cuenta de GitHub.
2. **Add New → Project**.
3. Elige el repo `nor-consulting`.
4. Framework Preset: **Other** (no necesita build, es estático).
5. Deploy. Te va a dar una URL gratis tipo `nor-consulting.vercel.app`.

**Opción B — desde la terminal:**
```bash
npm install -g vercel
vercel login
vercel        # deploy de prueba
vercel --prod # deploy definitivo
```

Cada vez que hagas `git push` a `main`, Vercel vuelve a publicar automáticamente
(deploy continuo) — así vas subiendo correcciones sin repetir estos pasos.

## Pendientes / notas para las próximas correcciones
- El formulario de contacto es solo visual: falta conectar un endpoint (ej. Formspree,
  Resend, o una función serverless de Vercel) para que los mensajes lleguen a un correo real.
- Reemplazar el teléfono, email y enlaces de WhatsApp/LinkedIn de ejemplo por los reales.
- El logo en `assets/logo.svg` es una reconstrucción simplificada del isologo — cuando tengas
  el archivo original (AI/SVG/PNG en alta resolución) se puede reemplazar directamente.
