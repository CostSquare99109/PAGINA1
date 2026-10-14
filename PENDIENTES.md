# Pendientes y decisiones técnicas del sitio

Proyecto técnico 11.B — Institución Educativa Colombia
Equipo: Jhon Fredy Montalvo Cuadrado, José David Mosquera Rodríguez, Esteban Espinoza Gomez

Este archivo no es contenido del sitio web. Es la bitácora interna del proyecto: registra
qué datos no se pudieron verificar, qué decisiones se tomaron al reorganizar los archivos
y qué debe completar el equipo antes de la entrega formal.

---

## 1. Datos que el equipo debe aportar

Durante la auditoría de los archivos **no se encontró ningún documento que identificara el
tema técnico del proyecto**. El HTML original era una plantilla de Bootstrap con textos de
relleno, y las imágenes solo permiten afirmar que el trabajo se desarrolló en un predio rural.

| Dato | Estado | Dónde se refleja en el sitio |
|---|---|---|
| Nombre del proyecto | Pendiente | Ficha de `index.html`, encabezado `<title>` de todas las páginas |
| Programa o técnica | Pendiente | `index.html` (bloque provisional), `conclusiones.html` (apartado 04) |
| Docente asesor | Pendiente | `index.html` (bloque provisional), `conclusiones.html` (apartado 04) |
| Ubicación del predio | Pendiente | `proyecto.html`, sección 02 Contexto |
| Planteamiento del problema | Pendiente | `proyecto.html`, sección 03 |
| Justificación | Pendiente | `proyecto.html`, sección 04 |
| Objetivo general y objetivos específicos | Pendientes | `proyecto.html`, sección 05 |
| Etapas del proyecto técnico | Pendiente | `desarrollo.html`, sección 05 |
| Reparto de responsabilidades del equipo | Pendiente | `integrantes.html`, sección 02 |
| Conclusiones validadas por la tutoría | Pendiente | `conclusiones.html`, sección 01 |
| Fechas de las fotografías | No verificable | `evidencias.html`, sección 02 |

### Cómo se marca el contenido pendiente

Los bloques que faltan están marcados en el sitio con la clase `.provisional`, que aplica un
borde ocre a la izquierda y la etiqueta visible **«Texto provisional»**. Para redactar la
versión definitiva basta con sustituir el texto dentro del bloque:

```html
<div class="provisional">
  <span class="provisional__etiqueta">Texto provisional</span>
  <p>Aquí va el texto definitivo del equipo.</p>
</div>
```

Una vez redactado, se puede eliminar el contenedor completo o quitarle la clase
`provisional`. No hace falta tocar ninguna hoja de estilos.

---

## 2. `img/logo.png` (recurso pendiente por separado)

No existe ningún archivo de escudo institucional en la carpeta del proyecto y **no se creó
uno ficticio**. Todas las páginas referencian la ruta pedida, `img/logo.png`, en el pie de
página, con esta protección para que la página no se rompa mientras el recurso está pendiente:

```html
<img class="pie__escudo" src="img/logo.png" alt="Escudo de la Institución Educativa Colombia"
     width="48" height="48"
     onerror="this.hidden=true;this.nextElementSibling.hidden=false">
<span class="avatar" hidden aria-hidden="true">IE</span>
```

Mientras el archivo no exista, el navegador muestra la marca tipográfica de reserva «IE».
En cuanto se agregue el archivo real a `img/logo.png`, el escudo aparece automáticamente y
no hay que modificar ninguna página. Basta con usar un PNG cuadrado; el CSS ya lo limita a
48 × 48 píxeles con `object-fit: contain`.

---

## 3. Imágenes

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

## 4. Bootstrap

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

## 5. Archivo original conservado

`layout web.html` se dejó tal como estaba, con sus textos de relleno y sus enlaces vacíos,
como registro del punto de partida. **No está enlazado desde la navegación** y el sitio no
lo carga. Puede archivarse o eliminarse sin consecuencias.

---

## 6. Cómo abrir el sitio

Doble clic en `index.html`. No hace falta servidor, instalación ni conexión a internet.

Si se quiere probar desde el celular en la misma red, en Visual Studio Code se puede usar la
extensión **Live Server** (el proyecto ya tiene `.vscode/settings.json` con el puerto 5501).