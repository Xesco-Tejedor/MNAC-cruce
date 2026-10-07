# MNAC-cruïlla

Prototipo web que conecta la consulta de obras de la colección del Museu Nacional d'Art de Catalunya con búsquedas de libros y publicaciones basadas en una obra elegida.

Las obras se muestran dentro de la aplicación. Los catálogos bibliográficos se abren en sus propios sitios: no se integran sus resultados ni se verifica automáticamente que una publicación trate sobre la obra seleccionada.

Proyecto independiente, no validado por el museo. El nombre visible es **MNAC-cruïlla**; el repositorio conserva el nombre `MNAC-cruce`.

[Abrir la aplicación](https://xesco-tejedor.github.io/MNAC-cruce/) · [Repositorio](https://github.com/Xesco-Tejedor/MNAC-cruce)

## Qué puedes hacer

- Buscar obras de la colección y recorrer los resultados dentro de la app.
- Seleccionar una obra y ver su imagen, autor y datos disponibles.
- Abrir la ficha original del MNAC.
- Preparar búsquedas bibliográficas por artista, artista + obra o título.
- Abrir el OPAC de la biblioteca del MNAC, el catálogo colectivo CCUC y la Memòria Digital de Catalunya (MDC).
- Exportar la obra seleccionada y sus enlaces de búsqueda a un PDF DIN A4.

## Cómo usarla

1. Abre la aplicación en un navegador con conexión a internet.
2. Introduce un artista, título o término, por ejemplo **Ramon Casas**, y pulsa **Buscar**. La consulta recorre páginas de la web del MNAC; puede tardar.
3. Recorre **Obras de la colección** y elige una obra. El segundo bloque cambia según esa selección.
4. Revisa la imagen y los datos. **Ficha en el MNAC** abre la fuente original.
5. En **Buscar libros por**, elige **Solo artista**, **Artista + obra** o **Solo título**. El modo inicial es Solo artista.
6. Pulsa el botón del catálogo que quieras consultar. Se abre otra pestaña con el término preparado.
7. Si la colección de libros digitalizados del MNAC no devuelve resultados, prueba **Buscar en todo el MDC**. En el modo Artista + obra, las búsquedas del MDC usan solo el título.
8. Pulsa **Exportar resultado a PDF · DIN A4** para descargar la información de esa obra. La exportación no crea un informe de todas las obras de la lista.

## Si un catálogo no muestra resultados

Los enlaces son un punto de partida, no una garantía de coincidencia bibliográfica. Prueba con el apellido, una variante del título o términos en catalán.

La aplicación incluye **¿No carga? Búsqueda manual** para copiar el término y abrir el buscador. En CCUC, revisa el ámbito **Tot** y ejecuta la búsqueda con la lupa. Si estás usando el navegador interno de WhatsApp o una página que incrusta la app, abre la aplicación en Chrome, Firefox o Safari.

## Fuentes y límites

Las obras y sus datos se consultan en la web del MNAC cuando realizas una búsqueda o seleccionas una obra. La consulta tiene un límite de 40 páginas y puede mostrar solo lo cargado si aparece un error.

La interfaz utiliza enlaces de búsqueda para OPAC y CCUC, en lugar de descargar sus resultados. Mantiene así la separación entre la consulta de obras y la consulta bibliográfica. MDC también se abre externamente.

Cambios en las páginas del museo, restricciones de acceso o errores de red pueden afectar a las búsquedas, imágenes y metadatos. Algunos campos pueden faltar o no extraerse correctamente: contrasta los datos con la ficha original. El PDF muestra los campos vacíos como **[ sin dato ]** y no implica que el museo carezca de esa información.

Las imágenes pueden tener derechos de terceros. La consulta o exportación no concede permiso para reutilizarlas; revisa la ficha de la obra antes de difundirlas.

## Ejecutarla en local

La interfaz está en `index.html` y usa JavaScript en el navegador. La exportación PDF depende de jsPDF, cargado desde un servicio externo.

```bash
git clone https://github.com/Xesco-Tejedor/MNAC-cruce.git
cd MNAC-cruce
python3 -m http.server 8000
```

Abre `http://localhost:8000`. Necesita conexión al museo, los catálogos y la biblioteca externa de PDF. Servirla en local no evita las restricciones de acceso entre sitios.
