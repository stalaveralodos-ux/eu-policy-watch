# Guía: subir la sección "EU Policy Watch" a tu portfolio

Vas a subir 4 archivos nuevos y editar 1 archivo existente. Todo desde la interfaz web de GitHub, como ya haces, sin git local.

## Archivos que vas a subir

1. `_briefs/2026-08-digital-omnibus.md`
2. `_briefs/2026-08-digital-networks-act.md`
3. `_briefs/2026-08-energy-omnibus.md`
4. `_layouts/brief.html`
5. `briefs/index.md`

## Pasos

**1. Entra a tu repositorio**
Ve a `github.com/stalaveralodos-ux/s.talaveralodos`.

**2. Crea la carpeta `_briefs` y sube los tres briefs**
- Haz clic en "Add file" → "Create new file".
- En el campo de nombre, escribe `_briefs/2026-08-digital-omnibus.md` (al escribir la barra `/`, GitHub crea la carpeta sola).
- Pega el contenido del archivo `2026-08-digital-omnibus.md`.
- Baja hasta el final de la página y haz clic en "Commit changes".
- Repite el mismo proceso para `_briefs/2026-08-digital-networks-act.md` y `_briefs/2026-08-energy-omnibus.md`.

**3. Crea el layout**
- "Add file" → "Create new file".
- Nombre: `_layouts/brief.html`.
- Pega el contenido de `brief.html`.
- "Commit changes".

**4. Crea la página índice**
- "Add file" → "Create new file".
- Nombre: `briefs/index.md`.
- Pega el contenido de `index.md`.
- "Commit changes".

**5. Edita `_config.yml`**
- Busca el archivo `_config.yml` en la raíz del repositorio y ábrelo.
- Haz clic en el icono del lápiz (editar).
- Añade estas líneas al final:

```yaml
collections:
  briefs:
    output: true
    permalink: /briefs/:name/
```

- "Commit changes".

**6. Añade el enlace desde tu página principal**
- Abre el archivo de tu página de inicio (probablemente `index.md` en la raíz, o dentro de `_layouts/default.html` si tienes un menú de navegación fijo).
- Añade un enlace de texto: `[Policy Briefs](/briefs/)`.
- "Commit changes".

**7. Espera y revisa**
- GitHub Pages tarda entre 1 y 3 minutos en reconstruir el sitio tras cada commit.
- Entra en `stalaveralodos-ux.github.io/s.talaveralodos/briefs/` y comprueba que aparece la página índice con los tres briefs listados.
- Entra en uno de los briefs individuales y comprueba que el layout se ve bien (título, fecha, contenido, enlace de vuelta).

## Si algo no se ve bien

- Si la página índice aparece en blanco o sin lista: revisa que el `_config.yml` tenga exactamente el bloque `collections` de arriba, sin errores de indentación (YAML es sensible a los espacios).
- Si un brief individual no coge el layout (se ve sin estilo, como texto plano): revisa que la primera línea del archivo del brief sea `---` y que `layout: brief` esté escrito exactamente así en el front matter.
- Si nada cambia tras el commit: comprueba en la pestaña "Actions" del repositorio si la build de GitHub Pages falló, y qué error da.
