# Homes JN — web de casas prefabricadas expandibles

Demo de cliente hecha por NEO Labs a partir de las fotos, los vídeos y los datos
aportados por el negocio (Homes JN, teléfono 615 69 11 17).

- `index.html` — una sola página: hero, sistema expandible, distribución (plano SVG),
  equipamiento, vídeo tour, galería, comparativa, usos, proceso, FAQ y contacto.
- `assets/fotos/` — fotos reales de la unidad (exterior e interior) en webp + jpg.
- `assets/video/` — dos vídeos verticales reales (tour interior 71 s, exterior 40 s) + póster.
- `assets/brand/` — logotipo vectorial y favicon.
- `og.jpg` — imagen de compartición en WhatsApp y redes.
- `aviso-legal.html`, `politica-privacidad.html`, `politica-cookies.html` — páginas legales.

## Cómo se regenera

```bash
cd ~/clients/homes-jn
python3 build_assets.py      # fotos y vídeos -> webp/jpg y mp4 comprimidos
python3 build_interiores.py  # reencuadre de fotogramas de interior
python3 build_og.py          # og.jpg
cat p1.html p2.html p3.html p4.html p5.html > index.html
```

Los parciales `p1..p5.html` se ignoran en git: el fichero publicado es `index.html`.

## Datos pendientes del titular

- Razón social, NIF y domicilio fiscal (para el aviso legal).
- Precio de salida de la unidad y condiciones de garantía.
- Confirmación de la superficie y de la distribución final de la unidad.
