# PROYECTO FINAL 1ª EVALUACIÓN: LÚMEN STUDIOS
## Memoria Técnica y Documento del Proceso
**Módulo:** Lenguajes de Marcas y Sistemas de Gestión de Información (DAM / DAW / ASIR)  
**Tema elegido:** Una productora de cine independiente (*Lúmen Studios Cinematográficos S.L.*)  
**Integrantes del Grupo:**
- **Persona A:** [Nombre del Alumno 1] — *Coordinación técnica, estructura base, página de inicio y CSS global*
- **Persona B:** [Nombre del Alumno 2] — *Páginas temáticas (Proyectos, Servicios, Equipo), tablas y listas*
- **Persona C:** [Nombre del Alumno 3] — *Página de contacto, investigación y maquetación del formulario HTML5*

---

## 1. Portada y Justificación del Proyecto
* **Nombre de la entidad:** Lúmen Studios Cinematográficos S.L.
* **Actividad:** Productora y distribuidora de cine independiente, servicios de alquiler de platós insonorizados, rodaje en alta definición (4K/8K) y salas de postproducción de color y mezcla Dolby Atmos.
* **Motivación del tema:** El cine es una disciplina que conjuga el arte narrativo con una exigencia técnica muy alta. Modelar una productora de cine ficticia permite desarrollar una estructura semántica rica en contenidos (sinopsis, palmarés, fichas técnicas, desgloses de tarifas por jornadas de rodaje y formularios de contratación o recepción de guiones).

---

## 2. Mapa del Sitio Web (Estructura de Páginas)
El sitio web está compuesto por **5 páginas HTML** interconectadas entre sí mediante un menú de navegación persistente en la cabecera y un mapa de enlaces en el pie de página:

1. **`index.html` (Inicio):**
   - Presentación institucional y manifiesto artístico de la productora.
   - Cabecera con selector `#hero` que incluye llamada a la acción (CTA) y gráfico principal.
   - Tres tarjetas en columnas destacando los pilares de la compañía (Producción Propia, Platós y Postproducción).
   - Bloque `<aside id="cifras-cine">` con métricas de la empresa (años de trayectoria, premios, largometrajes, platós).
   - Lista ordenada con las 5 fases del proceso de rodaje.

2. **`proyectos.html` (Filmografía y Catálogo):**
   - Catálogo de producciones cinematográficas en distribución:
     - *Ecos del Silencio* (Ciencia ficción).
     - *La Sombra del Farero* (Thriller psicológico en 35mm).
     - *Raíces de Cristal* (Documental de naturaleza y etnografía).
   - Fichas técnicas detalladas con listas de datos (dirección, guion, formato, sonido) y palmarés de premios en festivales (`<ul class="lista-premios">`).
   - Próximos estrenos y proyectos en preproducción estructurados mediante lista ordenada (`<ol>`).

3. **`servicios.html` (Instalaciones, Servicios y Tarifas):**
   - Descripción técnica de los dos platós de rodaje (ciclorama verde y espacio negro) y suites de postproducción.
   - Uso de `<figure>` y `<figcaption>` para diagramas técnicos.
   - **Tabla completa con `rowspan` y `colspan` (`#tabla-tarifas`):**
     - `colspan="4"` en la cabecera superior y en el pie de condiciones legales (`<tfoot>`).
     - `rowspan="2"` y `rowspan="3"` para agrupar servicios por departamentos (Platós, Cámaras y Ópticas, Postproducción y Audio).
     - `colspan="2"` en paquetes integrales ("Todo en Uno").
   - Lista de definiciones `<dl>` con los protocolos de seguridad y normativas en set (*Green Shooting*).

4. **`equipo.html` (Equipo Humano y Valores):**
   - Presentación de los directores y jefes de departamento (Dirección Creativa, Producción Ejecutiva, Dirección de Fotografía).
   - Tarjetas de perfil con imagen, biografía profesional y especialidad técnica.
   - Código ético y compromisos laborales (jornadas de 8 horas, paridad e inclusión, formación de aprendices).

5. **`contacto.html` (Contacto y Solicitud de Producción):**
   - Información física y de localización con etiqueta semántica `<address>`.
   - Vías de comunicación directa (teléfono con enlace `tel:`, correos electrónicos por departamento con enlace `mailto:`).
   - **Formulario técnico avanzado** con múltiples tipos de campos, validaciones nativas y agrupación mediante `<fieldset>` y `<legend>`.

---

## 3. Reparto de Tareas del Equipo
Para cumplir los hitos de la propuesta de forma equitativa, el trabajo se dividió según lo estipulado en las pautas:

| Integrante | Rol Asignado | Responsabilidades Principales | Archivos Desarrollados |
| :--- | :--- | :--- | :--- |
| **Persona A** | Arquitectura y Maquetación Base | Diseño de la guía de estilo, paleta de colores, tipografía, menú de navegación, pie de página, maquetación de `index.html` y creación de la hoja de estilos global `css/estilos.css`. | `index.html`, `css/estilos.css` |
| **Persona B** | Contenido Temático y Tablas | Redacción de sinopsis, fichas técnicas y tarifas; estructuración de `proyectos.html`, `servicios.html` y `equipo.html`; diseño de la tabla con `rowspan` y `colspan`; integración de listas. | `proyectos.html`, `servicios.html`, `equipo.html` |
| **Persona C** | Formularios e Investigación | Aprendizaje autónomo de formularios HTML5 a partir de MDN; diseño y maquetación de `contacto.html`; configuración de validaciones, campos (`select`, `radio`, `checkbox`, `date`, `textarea`) y docencia interna al grupo. | `contacto.html`, sección de formularios |

---

## 4. Decisiones de Diseño y Guía de Estilo

### 4.1. Paleta Cromática (Atmósfera Cinematográfica)
Se optó por una paleta de colores sobria, elegante y profesional inspirada en las salas de cine y festivales internacionales:
- **Negro Grafito Profundo (`#0f1015`, `#12131a`):** Utilizado en cabecera, pie de página, tarjetas oscuras y botones de contraste. Aporta empaque cinematográfico.
- **Dorado Ámbar / Film Gold (`#e5a93b`, `#ffd700`, `#b45309`):** Empleado en bordes decorativos, elementos activos del menú, enlaces y precios destacados. Simboliza los premios cinematográficos y el haz de luz de los proyectores.
- **Blanco Humo de Fondo (`#f7f7f9`):** Fondo principal del cuerpo para garantizar máxima legibilidad en los textos largos.
- **Blanco Puro (`#ffffff`):** Fondo de tarjetas de contenido (`.card`) y artículos para generar jerarquía visual limpia.

### 4.2. Tipografías
- **Títulos y Encabezados (`h1`, `h2`, `h3`, `legend`):** Familia Serif clásica (`Georgia`, `Times New Roman`, serif), evocando los créditos iniciales y cartelería del cine de autor.
- **Cuerpo de Texto y Formularios:** Familia Sans-Serif moderna (`Segoe UI`, `Tahoma`, `Verdana`, sans-serif), seleccionada por su legibilidad en pantalla e interfaces de usuario.

### 4.3. Maquetación con Modelo de Caja y Display (Sin Flexbox ni Grid)
Siguiendo las restricciones pedagógicas de la 1ª evaluación:
- **`box-sizing: border-box`** en todos los elementos para facilitar el cálculo exacto de anchos, rellenos (`padding`) y márgenes (`margin`).
- **`display: inline-block`** combinado con `vertical-align: top` y porcentajes controlados (`width: 31%`, `width: 48%`, `width: 63%`) para maquetar rejillas de tarjetas, columnas de formulario e información lateral sin desbordamientos.
- Separación vertical armónica mediante `margin-bottom` de 1.5rem a 3rem.

---

## 5. El Formulario HTML: Investigación y Desarrollo (Persona C)

### 5.1. ¿Qué campos tiene y por qué?
El formulario de `contacto.html` está concebido para atender solicitudes reales de una productora de cine:
1. **Identificación (`type="text"`, `type="email"`, `type="tel"`):**
   - Recoge el nombre, empresa y datos de contacto directo. Incluye atributos `required` para impedir envíos incompletos y `pattern` para el teléfono.
2. **Selección de Servicio (`<select>` con `<optgroup>`):**
   - Agrupa los motivos de contacto por departamentos: *Infraestructura y Rodaje* (Plató 1, Plató 2, Cámaras 8K), *Postproducción* (Color, Dolby Atmos, Montaje) y *Desarrollo* (Coproducción, Guiones, Casting). Facilita al usuario ubicar su necesidad exacta.
3. **Fecha de Rodaje (`type="date"`):**
   - Permite al cliente indicar en qué fecha tiene previsto iniciar la producción en los estudios.
4. **Presupuesto Estimado (`type="radio"`):**
   - Tres botones de opción mutuamente excluyentes (menor de 5.000 €, entre 5.000 € y 25.000 €, más de 25.000 €) para clasificar el tipo de producción (cortometraje, spot publicitario o largometraje).
5. **Servicios Técnicos Adicionales (`type="checkbox"`):**
   - Casillas de selección múltiple para añadir personal especializado (electricista gaffer, sonidista directo, salas de maquillaje).
6. **Área de Texto (`<textarea rows="6">`):**
   - Campo amplio para la sinopsis del proyecto o memoria de necesidades.
7. **Consentimiento Legal (`type="checkbox"` obligatorio):**
   - Aceptación de la política de confidencialidad y tratamiento de datos antes del envío.
8. **Botones de Control (`button type="submit"` y `button type="reset"`):**
   - Permiten despachar la información o limpiar los campos para reiniciar la carga.

### 5.2. ¿Qué ha aprendido la persona encargada?
- **Asociación semántica `<label for="id">`:** Comprender la importancia de vincular cada etiqueta con el identificador del campo para que las personas con lectores de pantalla o movilidad reducida puedan hacer clic en la etiqueta para enfocar o activar el control.
- **Validación nativa en el navegador:** Comprobar cómo `required`, `type="email"`, `minlength` y expresiones regulares validan datos sin necesidad de recurrir a código JavaScript.
- **Estructuración con `<fieldset>` y `<legend>`:** Organizar formularios extensos en bloques temáticos lógicos que mejoran notablemente la experiencia de usuario (UX).

---

## 6. Diario del Proceso (Hitos del Proyecto)

* **Hito 1: Propuesta y Reparto:**
  - *Actividades:* Elección del tema "Una productora de cine", definición de la identidad ("Lúmen Studios"), elaboración del mapa del sitio web y reparto formal de tareas entre los tres integrantes.
  - *Problemas detectados:* Dudas sobre si podíamos usar Flexbox. Se revisó la guía docente y se acordó ceñirse estrictamente al modelo de caja (`display: inline-block` y `margin/padding`).
  - *Resolución:* Aprobación de la propuesta por parte del docente.

* **Hito 2: Esqueleto HTML:**
  - *Actividades:* Creación de las 5 páginas (`index.html`, `proyectos.html`, `servicios.html`, `equipo.html`, `contacto.html`). Redacción de todas las etiquetas semánticas (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`), listas y enlaces relativos entre todas las páginas.
  - *Problemas detectados:* Enlaces rotos si se cambiaba de carpeta.
  - *Resolución:* Unificación de todos los archivos HTML en la raíz del proyecto y carpetas ordenadas `css/` e `img/`.

* **Hito 3: Contenido y Hoja de Estilos Común:**
  - *Actividades:* Redacción del contenido real y original de cada película, servicios técnicos y perfiles del equipo. Maquetación de la tabla de tarifas con `rowspan` y `colspan`. Creación de los gráficos vectoriales SVG en `img/`. Construcción de la hoja de estilos unificada `css/estilos.css` con selectores de etiqueta, clase e identificadores (`#hero`, `#tabla-tarifas`, `#formulario-contacto`, `#cifras-cine`).
  - *Problemas detectados:* Los elementos con `display: inline-block` dejaban un pequeño espacio en blanco entre sí debido al salto de línea del HTML.
  - *Resolución:* Ajuste de los porcentajes de ancho al 31% y márgenes horizontales de 1% para que las tres columnas encajaran perfectamente sin saltar de línea.

* **Hito 4: Revisión, Validación W3C y Entrega:**
  - *Actividades:* Comprobación de todas las etiquetas de cierre, verificación de textos alternativos (`alt`) en todas las imágenes, validación de la sintaxis según los estándares del consorcio W3C y redacción de la memoria del proceso.
  - *Resultado:* Cero errores de sintaxis y código 100% válido y ordenado.

---

## 7. Fuentes Consultadas y Declaración de Uso de IA

### 7.1. Documentación Oficial y Tutoriales
- **MDN Web Docs (Mozilla Developer Network):**
  - *Mi primer formulario HTML* y *Cómo estructurar un formulario HTML*.
  - *HTML table basics* (guía de uso de atributos `rowspan` y `colspan`).
  - *The CSS Box Model* (margen, relleno, bordes y dimensión de caja).
- **W3C Nu HTML Checker:** Herramienta de validación de sintaxis de código HTML5.

### 7.2. Origen de las Imágenes
- Todas las imágenes e iconos alojados en el directorio `img/` (`logo.svg`, `hero-cine.svg`, `pelicula1.svg`, `pelicula2.svg`, `pelicula3.svg`, `plato.svg`, `postproduccion.svg`, `equipo.svg`, `director.svg`) son ilustraciones vectoriales originales creadas en formato SVG libre de derechos de autor para este proyecto académico, garantizando que el proyecto se ejecute de forma autónoma e íntegramente offline.

### 7.3. Declaración de Uso de Inteligencia Artificial (Apéndice)
En cumplimiento de las instrucciones de la asignatura:
- **Plataforma de IA utilizada:** Asistente de IA (Antigravity / DeepMind).
- **Consultas realizadas:**
  1. *Estructuración y diseño semántico de plantillas HTML5 conformes a los requisitos de 1ª evaluación de Lenguajes de Marcas.*
  2. *Generación de ilustraciones vectoriales en formato SVG para cartelería cinematográfica y diagramas de plató libres de derechos.*
  3. *Revisión y optimización de selectores CSS para evitar dependencias de Flexbox/Grid respetando el modelo de caja tradicional.*
- **Cómo se ha aprovechado:** La IA actuó como herramienta de apoyo metodológico y revisión de código. Todos los textos, estructuras de páginas, campos de formulario y estilos fueron revisados, adaptados y verificados activamente por el equipo de alumnos para asegurar el dominio pleno de cada línea de código ante la defensa oral.

---

## 8. Autoevaluación del Equipo
- **Qué ha salido especialmente bien:**
  - El aspecto visual y la coherencia estética del sitio web: la paleta de colores y el estilo cinematográfico dotan a la web de un acabado profesional.
  - La tabla de tarifas técnicas, donde `rowspan` y `colspan` tienen una función clara y real de agrupación que facilita su comprensión.
  - El formulario de contacto, que cuenta con una amplia variedad de controles funcionales e intuitivos.
- **Qué mejoraríamos en el futuro:**
  - Cuando se impartan en clase los temas de la 2ª evaluación, nos gustaría incorporar animaciones CSS, un diseño responsive completo mediante *Media Queries* más complejas y adaptación fluida con CSS Grid.
  - Integrar JavaScript para dotar al formulario de validación dinámica en tiempo real y mostrar un mensaje modal de confirmación al usuario tras enviar la solicitud.
