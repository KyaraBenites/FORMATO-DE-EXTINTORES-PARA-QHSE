# Inspección Mensual de Extintores SDE — versión móvil 4

## Publicar en GitHub Pages
1. Descomprimir el ZIP.
2. Subir los cinco archivos `index.html`, `app.js`, `styles.css`, `logo-sde.png` y `README.md` **a la raíz** de `KyaraBenites/inspeccion-extintores`, reemplazando versiones anteriores.
3. En GitHub, `Settings > Pages > Deploy from a branch > main > /(root) > Save`.
4. Abrir `https://kyarabenites.github.io/inspeccion-extintores/` y actualizar forzosamente la página si se visualiza la versión anterior.

## Usar desde celular
1. Ingresar datos de inspección en **Editar datos**.
2. Elegir el extintor, marcar verificaciones, escribir observaciones.
3. Pulsar **Tomar foto** para usar cámara o **Elegir de galería o PC** para añadir imágenes ya existentes.
4. Pulsar **Guardar y pasar al siguiente**. Se conserva avance en el almacenamiento local del navegador cuando está disponible.
5. Al terminar, ir a **Guardar y obtener tu reporte**. Se puede guardar borrador o finalizar.
6. Pulsar **Preparar PDF**, **Preparar Word** o **Preparar imagen**. Cuando aparezca el cuadro «Archivo listo», pulsar **Visualizar**, **Descargar** o **Compartir**.
7. En algunos iPhone/iPad, Safari abre la vista previa en lugar de mostrar barra de descargas. Desde esa pantalla usar **Compartir > Guardar en Archivos**; en Android revisar **Descargas**. El botón Compartir adjunta el archivo cuando el navegador permite compartir archivos (Web Share API y contexto HTTPS); si no, descargar y compartir desde Archivos.

## Formatos y limitaciones
- **PDF**: tabla horizontal A3, una o dos hojas según cantidad de filas; contiene una imagen por extintor si se adjuntó.
- **PNG**: un solo archivo largo que contiene las 1-2 hojas A3, evitando bloqueos de descarga múltiple en móviles.
- **Word DOCX**: documento real OOXML, tabla editable en Word; las fotos se señalan en la tabla mediante un contador y se consultan visualmente en PDF/PNG o respaldo. Comprobado con LibreOffice; paginación depende también de la aplicación Word utilizada.
- **JSON**: guarda la inspección íntegra, observaciones sin recortar y todas las fotos.
- **Historial**: IndexedDB por navegador/dispositivo. GitHub Pages **no sincroniza ni almacena** documentos de los inspectores en servidor. No confiar en modo incógnito. Exportar respaldo JSON periódicamente.
- El límite de **dos hojas** de la tabla requiere abreviar observaciones largas, reducir letra si hay muchas filas y mostrar solo la primera fotografía. Si se agregan muchas filas, la legibilidad en impresión puede disminuir. Para conservar los datos completos, usar JSON.
- Los archivos se generan en el navegador sin necesidad de backend o servicios externos. Es recomendable tener conexión HTTPS al abrir desde GitHub Pages, especialmente para Compartir.
