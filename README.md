# DJJCM – DJ Carlos Martinez · Website

Sitio web profesional de DJ JCM. Stack: HTML estático + CSS + JS vanilla, desplegado en GitHub Pages con dominio personalizado `www.djjcm.de`.

---

## Cómo actualizar información de contacto

Abre `index.html` y busca los siguientes puntos:

### Teléfono / WhatsApp
Busca `4915252822834` — aparece en varios lugares (botón WhatsApp, footer, etc.).  
Reemplaza el número completo en formato internacional sin `+` ni espacios.

### Nombre / Marca
Busca `DJ Carlos Martinez` o `DJJCM` para actualizar nombre o branding.

### Cobertura geográfica
La línea de cobertura está en el Hero y en el Footer:
```
Nürnberg · Deutschland · Österreich · Schweiz · Italien
```

### Redes sociales / Links externos
Añade enlaces en el footer dentro de `.footer-legal` en `index.html`.

---

## Páginas legales (obligatorio en Alemania)

| Archivo | Descripción |
|---|---|
| `impressum.html` | Impressum — rellenar dirección real y Steuer-ID |
| `datenschutz.html` | Datenschutzerklärung (DSGVO) — ya configurada |

**Campos que DEBES rellenar en `impressum.html`:**
- Dirección real (Straße und Hausnummer, PLZ)
- Steuer-Identifikationsnummer

---

## Cómo desplegar cambios a GitHub Pages

### Requisito previo
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

### Flujo de trabajo
```bash
# 1. Ir al directorio del proyecto
cd "Desktop/⚙️ Proyectos Tech/GitHub/Djjcm09.github.io"

# 2. Ver qué cambió
git status
git diff index.html

# 3. Guardar cambios
git add index.html          # o: git add .   (para todos los archivos)
git commit -m "Descripción del cambio"

# 4. Publicar en GitHub Pages
git push origin main
```

El sitio se actualiza en **~60 segundos** tras el push en `www.djjcm.de`.

---

## Actualizar/añadir fotos

Coloca los archivos en la carpeta `fotos/` y referéncialos en el HTML:
```html
<img src="fotos/mi-nueva-foto.jpg" alt="Descripción en alemán">
```
Formatos recomendados: **WebP** (mejor) o JPG. Tamaño máximo recomendado: 300KB por imagen.

## Actualizar/añadir videos

Coloca los archivos en la carpeta `videos/`. Para comprimir antes de subir:
```bash
ffmpeg -i videos/mi-video.mp4 \
  -vf "scale=720:-2" \
  -c:v libx264 -crf 26 -preset slow \
  -movflags +faststart \
  -c:a aac -b:a 96k \
  -y videos/mi-video_opt.mp4
```

---

## Estructura del proyecto

```
Djjcm09.github.io/
├── index.html          # Página principal
├── impressum.html      # Impressum (legal obligatorio DE)
├── datenschutz.html    # Datenschutz / DSGVO
├── CNAME               # Dominio personalizado (www.djjcm.de)
├── fotos/              # Imágenes del sitio
│   ├── setup-open-air.jpg
│   ├── dj-controller.jpeg
│   ├── dancefloor.jpg
│   └── ...
└── videos/             # Videos del sitio
    ├── bienvenida.mp4  # Video avatar (círculo superior)
    ├── event-highlight.mp4
    └── ...
```

---

## Checklist SEO completado ✅

- [x] `<html lang="de">`
- [x] Title tag optimizado con keywords alemanas
- [x] Meta description con las 4 especialidades
- [x] JSON-LD `ProfessionalService` schema (Google Rich Results)
- [x] Open Graph + Twitter Cards
- [x] Alt tags en alemán en todas las imágenes
- [x] Impressum + Datenschutz (obligatorio DSGVO)
- [x] Canonical URL
- [x] `robots: index, follow`

---

*Contacto técnico: whatsapp.com/4915252822834*
