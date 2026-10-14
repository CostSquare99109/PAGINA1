# Pendientes y decisiones técnicas del sitio

Medidor de temperatura en Aulas de Clases — Prototipo en desarrollo
Curso 11.B Media Técnica de Sistemas — Institución Educativa Colombia
Equipo: Jhon Fredy Montalvo Cuadrado, José David Mosquera Rodríguez, Esteban Espinoza Gomez,
Brandol Stevan Durango Moreno

Este archivo no es contenido del sitio web. Es la bitácora interna del proyecto: registra
qué datos no se pudieron verificar, qué decisiones se tomaron al reorganizar los archivos
y qué debe completar el equipo antes de la entrega formal.

---

## 1. Estado del proyecto

El proyecto es un **prototipo en desarrollo**, no una instalación terminada. Todo el sitio
debe hablar en ese tono: lo que existe es un montaje de trabajo y sus pruebas de
validación, y el medidor todavía no está colocado de forma permanente en las aulas.

---

## 2. Datos que el equipo debe aportar

Durante la auditoría de los archivos **no se encontró ningún documento que identificara el
tema técnico del proyecto**, por lo que el equipo suministró los datos
básicos (nombre del proyecto, programa, equipo y contacto). El HTML original era una plantilla
de Bootstrap con textos de relleno.

| Dato | Estado | Dónde se refleja en el sitio |
|---|---|---|
| Nombre del proyecto | **Confirmado:** Medidor de temperatura en Aulas de Clases | Ficha de `index.html`, encabezado `<title>` de todas las páginas |
| Programa o técnica | **Confirmado:** 11.B Media Técnica de Sistemas | Ficha de `index.html`, encabezado y pie de página de las 6 páginas |
| Contacto del equipo | **Confirmado:** 3104618120 | Ficha de `index.html`, `integrantes.html`, `proyecto.html` y pie de página de las 6 páginas |
| Docente asesor | Pendiente | `index.html` (bloque provisional), `conclusiones.html` (apartado 04) |
| Aulas donde se colocará el medidor | Pendiente | `proyecto.html`, sección 02 Prototipo en desarrollo |
| Planteamiento del problema | Pendiente | `proyecto.html`, sección 03 |
| Justificación | Pendiente | `proyecto.html`, sección 04 |
| Objetivo general y objetivos específicos | Pendientes | `proyecto.html`, sección 05 |
| Componentes exactos del medidor | Pendiente | `proyecto.html`, sección 01 |
| Resultados de las pruebas del prototipo | Pendiente | `desarrollo.html`, secciones 01 y 05 |
| Fechas de cada etapa del desarrollo | Pendiente | `desarrollo.html`, secciones 01 y 05 |
| Reparto de responsabilidades del equipo | Pendiente | `integrantes.html`, sección 02 |
| Conclusiones validadas por la tutoría | Pendiente | `conclusiones.html`, sección 01 |
| Fechas de las fotografías | No verificable | `evidencias.html`, sección 02 |

Nota sobre las fotografías: las cuatro imágenes disponibles en `img/` corresponden a un
predio rural (potrero, maquinaria agrícola, animales en pastoreo y campo de juego) y no
documentan el prototipo. Se conservaron porque son las únicas disponibles; el equipo debe
reemplazarlas por fotos del montaje, las conexiones y las pruebas de lectura en
`evidencias.html` y en las imágenes de portada.

### Cómo se marca el contenido pendiente

Los bloques que faltan siguen apareciendo marcados con la clase `.provisional`, que aplica un
borde ocre a la izquierda y la etiqueta visible **«Texto provisional»**. Quedan ocho en total:
uno en `index.html` (docente asesor), cinco en `proyecto.html` (componentes, pruebas,
planteamiento, justificación y objetivos), uno en `desarrollo.html` (fechas de las etapas),
uno en `evidencias.html` (fotos del montaje) y uno en `conclusiones.html` (aprendizajes).
`integrantes.html` no tiene ninguno.

Para redactar la versión definitiva basta con sustituir el texto dentro del bloque:

```html
<div class="provisional">
  <span class="provisional__etiqueta">Texto provisional</span>
  <p>Aquí va el texto definitivo del equipo.</p>
</div>
```

Una vez redactado, se puede eliminar el contenedor completo o quitarle la clase
`provisional`. No hace falta tocar ninguna hoja de estilos.

---

## 3. `img/logo.png` y la marca del proyecto

El equipo aportó una imagen de 580 × 412 px que se preparó y se colocó como `img/logo.png`:
se le hizo transparente el fondo blanco, se recortó el margen y se redujo a 348 × 199 px
(43 KB). Ya aparece en la barra y en el pie de las seis páginas, y funciona como favicon.

**Decisión importante:** el texto alternativo no dice «escudo de la Institución Educativa
Colombia», sino **«Logotipo del proyecto técnico del curso 11.B»**, y bajo la imagen hay una
nota visible que dice «Logotipo del proyecto técnico». El archivo no es un escudo
institucional, así que el sitio no lo presenta como tal: el nombre de la institución sigue
escrito en texto aparte.

Si el equipo consigue después el escudo real de la institución, no hace falta tocar el
código: bastaría con sustituir el archivo `img/logo.png` y actualizar los textos
alternativos y la nota a «Escudo de la Institución Educativa Colombia».

---

## 4. Imágenes

### Fotografía del equipo

El equipo aportó una foto grupal (`img/integrantes.jpg`, 1600 × 1200 px), que se redujo a
1200 × 900 px (110 KB). Muestra a los cuatro integrantes con el uniforme del colegio dentro
de un aula, junto a computadores portátiles y un televisor en la pared. Se usa en la portada
de `integrantes.html`, con texto alternativo descriptivo y pie de foto. No se identifica
quién está en cada posición porque la imagen no permite verificarlo.

### Material usado (fotografías del predio)

Las cuatro fotografías del predio se abrieron una por una antes de decidir su uso. Los archivos
originales **no se movieron ni se renombraron**; el sitio usa copias ligeras con nombres
limpios, para evitar rutas con espacios y reducir el peso en móvil.

| Archivo original (intacto) | Copia usada en el sitio | Peso original → copia |
|---|---|---|
| `img/What.jpeg` | `img/doc-01-potrero.jpg` | 466 KB → 236 KB |
| `img/WhatsApp Image 2.jpeg` | `img/doc-02-maquinaria.jpg` | 700 KB → 367 KB |
| `img/WhatsApp Image 2026-02-18 at 2.03.37 PM.jpeg` | `img/doc-03-pastoreo.jpg` | 420 KB → 258 KB |
| `img/WhatsApp Image 2026-02-21 at 7.34.05 PM.jpeg` | `img/doc-04-cancha.jpg` | 635 KB → 326 KB |

Las copias son de 1200 × 900 px, calidad 72 y carga progresiva. Los originales son de
1600 × 1200 px y **no conservan metadatos EXIF**, por lo que no se pudo establecer la fecha
ni el dispositivo de captura. Dos nombres de archivo incluyen una fecha (18 y 21 de febrero
de 2026), pero se trata del nombre con el que se guardaron, no de un dato verificado.

### Material no usado (se conserva, no se muestra)

| Archivo | Motivo de no uso |
|---|---|
| `img/descarga.jpg` | Fotografía de un jugador de fútbol, descargada de Internet. No documenta el proyecto. |
| `img/iiiii.jpg` | Miniatura de un paisaje de montaña con marca de agua. No documenta el proyecto. |
| `img/florian-schindler-3CRgpaPLCsM-unsplash.jpg` | Paisaje de montaña de Unsplash, usado como fondo decorativo en la plantilla original. No documenta el proyecto y pesa 4,9 MB. |

Los tres archivos siguen intactos en la carpeta. Se conservan por si el equipo decide
reutilizarlos como material de apoyo, pero no se presentan como evidencia.

---

## 5. Bootstrap

La carpeta traía la distribución completa de **Bootstrap 5.3.2** (CSS completo, variantes de
derecha a izquierda, de rejilla, de reinicio y de utilidades, más los mapas `.map` y los
paquetes JavaScript sin comprimir, ESM y con Polyfill).

- El sitio carga **una sola hoja**: `css/bootstrap.min.css`.
- El sitio carga **un solo paquete**: `js/bootstrap.bundle.min.js` (necesario para el menú
  colapsable y los modales de la galería).
- Los demás archivos **no se modificaron ni se borraron**. Quedan en la carpeta como respaldo
  y no están enlazados desde ninguna página. Se pueden eliminar si el equipo quiere aligerar
  el repositorio; no afectan el funcionamiento del sitio.

---

## 6. Archivo original conservado

`layout web.html` se dejó tal como estaba, con sus textos de relleno y sus enlaces vacíos,
como registro del punto de partida. **No está enlazado desde la navegación** y el sitio no
lo carga. Puede archivarse o eliminarse sin consecuencias.

---

## 7. Cómo abrir el sitio

Doble clic en `index.html`. No hace falta servidor, instalación ni conexión a internet.

Si se quiere probar desde el celular en la misma red, en Visual Studio Code se puede usar la
extensión **Live Server** (el proyecto ya tiene `.vscode/settings.json` con el puerto 5501).

---

## 8. Cambios en el encabezado, el menú y la portada (revisión de presentación)

Se revisó el encabezado y la navegación de las seis páginas para que el sitio se presente
como una página académica completa. Los cambios fueron acotados al `<header>`, al `navbar`
y a la portada de `index.html`; no se tocó la lógica de contenido de las demás secciones.

**Marca del encabezado.** La barra mostraba el nombre de la institución como título
principal. Ahora muestra el nombre completo del proyecto, «Medidor de temperatura en Aulas de
Clases», en dos líneas junto al logo, con el curso («11.B · Media Técnica de Sistemas») como
segunda línea. El nombre de la institución sigue presente en la ficha de `index.html`,
`proyecto.html`, `integrantes.html` y en el pie de las seis páginas. El logo pasó de 42 px a
48 px de ancho para que no compita en tamaño con el texto.

**Estados del menú.** En pantallas anchas los enlaces habían perdido el subrayado de estado:
solo el enlace activo se distinguía. Ahora todos los enlaces reservan el mismo espacio de
subrayado, el activo se marca con la línea ocre y el hover con un fondo verde tenue. En
móvil y tableta el menú desplegable separa cada enlace con un borde ocre a la izquierda en el
elemento activo y enlaces de altura cómoda para el dedo (47 px medidos).

**Portada de inicio.** El rótulo superior pasó a ser «Bienvenida» y la descripción se ajustó
al alcance real del sistema (lectura con sensor y visualización en un programa, en etapa de
prototipo). La fotografía de portada dejó de ser una imagen del predio y ahora es la foto del
equipo (`img/integrantes.jpg`), que antes solo aparecía en `integrantes.html`; el pie enlaza
a la página de integrantes. Las fotos del predio siguen siendo el material de `evidencias.html`.

**Contacto.** No se agregó «Contacto» al menú principal porque el proyecto no tiene una página
de contacto: los datos disponibles (teléfono 3104618120) aparecen en la ficha de `index.html`,
en `integrantes.html` y en el pie de las seis páginas. Si el equipo crea la sección, se agrega
el enlace al menú.

**Verificado:** las seis páginas mantienen elHTML balanceado, sin ids duplicados y con todas
las rutas de imágenes y hojas de estaldo existentes; el menú responsive se abrió y cerró
correctamente en una prueba de navegador a 390 px, 768 px y 1280 px, sin desplazamiento
horizontal en ningún ancho. **Pendiente del equipo:** reemplazar en `evidencias.html` las fotos
del predio por imágenes reales del montaje y las pruebas del prototipo.
