# MapLab

MapLab es una pagina estatica para convertir Markdown en mapas visuales editables. Funciona directo en GitHub Pages: no requiere backend, compilacion ni instalacion.

## Caracteristicas

- Editor Markdown con numeros de linea, plantillas, importar y descargar `.md`.
- Parser para titulos, listas y relaciones como `A --> B`, `A --relacion--> B` y `A <--> B`.
- Lienzo SVG con zoom, pan, seleccion multiple, arrastre de nodos y conexiones editables.
- Layouts: radial, horizontal, arbol vertical, arbol horizontal, organigrama, conceptual, flujo, Ishikawa, timeline, circular, graph y tarjetas.
- Inspector para texto, color, borde, forma, fuente, conexiones y paletas por profundidad.
- Persistencia local con `localStorage`, historial undo/redo y gestion basica de proyectos.
- Guardado manual como archivo `.maplab.json` descargado al PC, ideal para GitHub Pages sin base de datos.
- Exportacion del mapa completo a PNG, PNG 2x, PNG 4x, SVG vectorial, Markdown, JSON y PDF vectorial descargable, sin usar impresora ni dialogo de impresion.

## Publicar en GitHub Pages

1. Sube `index.html` y `README.md` a un repositorio de GitHub.
2. En GitHub, abre `Settings` > `Pages`.
3. En `Build and deployment`, selecciona `Deploy from a branch`.
4. Elige la rama `main` y la carpeta `/root`.
5. Guarda los cambios y abre la URL que GitHub Pages genere.

## Uso local

Abre `index.html` en tu navegador. Tambien puedes servir la carpeta con cualquier servidor estatico:

```bash
python -m http.server 8080
```

Luego entra a `http://localhost:8080`.

## Formato Markdown compatible

```markdown
# Tema principal

## Rama

### Concepto

- Detalle
- Otro detalle

Concepto -- explica --> Detalle
Rama <--> Tema principal
```

Los titulos y listas forman la jerarquia. Las relaciones con flechas agregan conexiones conceptuales sin romper el mapa jerarquico.
