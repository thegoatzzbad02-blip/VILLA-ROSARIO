# 📘 MANUAL MAESTRO VILLA ROSARIO
## Guía Única, Completa y Definitiva para Mantener Actualizada tu Página Web Comunitaria

**Proyecto de Vinculación Sociotecnológica:** Desarrollo de la Plataforma Web para el Consejo Comunal de Villa Rosario
**Elaborado por:** Equipo de Investigadores y Desarrolladores (UPTOS)
**Versión:** 1.0 Maestro
**Fecha de Entrega:** Junio 2026
**Destinatarios:** Voceros y Voceras del Consejo Comunal, Administradores del Sitio, Comunidad de Villa Rosario
**Estado:** Documento de Transferencia Tecnológica Total y Autocontenido

---

## 📋 ÍNDICE GENERAL INTERACTIVO

- [PARTE 1: BIENVENIDA, ENFOQUE METODOLÓGICO Y MAPEO VISUAL](#parte-1-bienvenida-enfoque-metodológico-y-mapeo-visual)
- [PARTE 2: GUÍA DE INICIO RÁPIDO (5 MINUTOS DE EMERGENCIA)](#parte-2-guía-de-inicio-rápido-5-minutos-de-emergencia)
- [PARTE 3: MANUAL DE USUARIO COMPLETO (SABER QUÉ EDITAR LÍNEA POR LÍNEA)](#parte-3-manual-de-usuario-completo-saber-qué-editar-línea-por-línea)
- [PARTE 4: HOJA DE TRUCOS Y BANCO DE 15+ PLANTILLAS (COPIAR Y PEGAR)](#parte-4-hoja-de-trucos-y-banco-de-15-plantillas-copiar-y-pegar)
- [PARTE 5: GUÍA TÉCNICA, GIT Y DESPLIEGUE (GITHUB DESKTOP PASO A PASO)](#parte-5-guía-técnica-git-y-despliegue-github-desktop-paso-a-paso)
- [PARTE 6: RESOLUCIÓN DE PROBLEMAS Y FAQ COMUNITARIA DE LA UPTOS](#parte-6-resolución-de-problemas-y-faq-comunitaria-de-la-uptos)

---

# PARTE 1: BIENVENIDA, ENFOQUE METODOLÓGICO Y MAPEO VISUAL

## 1.1 Bienvenida de la UPTOS al Consejo Comunal de Villa Rosario

Nosotros, el equipo investigador de la UPTOS, presentamos este documento como resultado de un proceso participativo con el Consejo Comunal de Villa Rosario, Sector Sabilar, Parroquia Altagracia, Municipio Sucre. Nuestro compromiso académico es entregar una herramienta clara, práctica y fácil de usar, diseñada para que ustedes, las y los voceros de la comunidad, mantengan de manera autónoma el sitio web.

Este manual no es simplemente un libro de instrucciones. Es una guía de transferencia tecnológica en la que cada párrafo refleja nuestra responsabilidad social y educativa. Construimos esta documentación a partir de la experiencia en trabajo comunitario, con lenguaje cercano, ejemplos realidad y una estructura pensada para que cualquier persona termine el proceso con mayor confianza y conocimiento técnico.

## 1.2 Por qué elegimos una arquitectura estática

En el diseño de la plataforma web de Villa Rosario decidimos usar una arquitectura estática. Esto significa que cada página existe como un archivo concreto que se guarda en el repositorio. No hay bases de datos ni sistemas complejos. La razón es sencilla y profunda:

- Es más seguro: no dependemos de servidores externos con contraseñas sensibles.
- Es más estable: una vez que el archivo está bien, no se rompe con actualizaciones automáticas inesperadas.
- Es más accesible: los voceros pueden editar directamente el contenido con herramientas básicas.
- Es más rápido: la página carga directamente desde GitHub Pages.

La arquitectura estática se compone de páginas en HTML, estilos en CSS y comportamientos sencillos en JavaScript. Nosotros apostamos por esta ruta porque es la más apropiada para una comunidad que necesita control local, mantenimiento transparente y capacidad de autoaprendizaje.

## 1.3 Páginas del sitio y su propósito

Estas son las páginas principales del sitio web y su función dentro de la comunicación comunitaria:

| Página | Archivo | Función comunitaria |
|--------|---------|---------------------|
| Inicio | `index.html` | Presentar información general, alertas urgentes, noticias destacadas, estado de servicios y actividades recientes. |
| Consejo Comunal | `consejo-comunal.html` | Mostrar la organización del consejo, comités, voceros y la estructura de decisión colectiva. |
| Noticias | `articulos.html` | Listado completo de todas las noticias y comunicados comunitarios. |
| Noticia individual | `noticia.html` | Plantilla para el detalle completo de una noticia específica. |
| Eventos | `eventos.html` | Agenda de actividades, festividades y jornadas de trabajo comunitario. |
| Proyectos | `proyectos.html` | Estado de las obras, avances y actividades constructivas del Consejo Comunal. |
| Servicios | `servicios.html` | Monitoreo del servicio de agua, electricidad, aseo e internet con semáforo de prioridades. |
| Emprendedores | `emprendedores.html` | Directorio de negocios locales y microempresas de Villa Rosario. |
| Historia | `historia.html` | Memoria colectiva de nuestra comunidad, raíces y trayectorias. |
| Contacto | `contacto.html` | (Sugerida) Página de contacto y comunicación con el Consejo Comunal. |

> Nota: En algunos casos, el archivo `contacto.html` puede no estar creado aún, pero nuestra recomendación es mantener el diseño preparado como parte de la arquitectura comunitaria.

## 1.4 Mapa general de carpetas y archivos

El repositorio se organiza de la siguiente manera. Es muy importante que identifiquemos claramente los archivos que NO debemos modificar directamente para no romper el diseño o la interacción del sitio.

```text
VILLA-ROSARIO/
├── index.html
├── articulos.html
├── noticia.html
├── eventos.html
├── proyectos.html
├── servicios.html
├── emprendedores.html
├── consejo-comunal.html
├── historia.html
├── contacto.html (opcional)
├── css/
│   └── estilo.css
├── js/
│   └── main.js
└── imagenes/
    ├── logoVilla.png
    ├── carrusel1.png
    ├── carrusel2.png
    ├── carrusel3.png
    ├── carrusel4.jpg
    ├── emprendedor1.jpg
    ├── emprendedor2.jpg
    ├── dia.jpg
    ├── img1.jpg
    ├── imgr1.png
    └── ...
```

### 1.4.1 Archivos que están prohibidos tocar sin permiso

Nosotros, como equipo de la UPTOS, establecemos que los siguientes archivos son críticos para el funcionamiento general del sitio y no deben modificarse salvo que exista una decisión técnica compartida con el Consejo Comunal:

- `css/estilo.css`
- `js/main.js`

Estas dos piezas contienen las reglas de estilo, colores, disposición de componentes, animaciones y comportamientos del carrusel. Si se cambia mal un valor aquí, la página puede perder su forma, sus botones pueden dejar de funcionar o la imagen puede verse desordenada.

### 1.4.2 Archivos de contenido que sí puedes editar con seguridad

Los archivos de contenido que pueden modificarse de manera segura son:

- `index.html`
- `articulos.html`
- `noticia.html`
- `eventos.html`
- `proyectos.html`
- `servicios.html`
- `emprendedores.html`
- `consejo-comunal.html`
- `historia.html`
- `contacto.html` 

En estos archivos se cambia el contenido textual, las fechas, las imágenes, la información de contacto, los títulos y descripciones. Aquí se encuentra la acción comunitaria.

## 1.5 Nuestro enfoque metodológico participativo

El proceso de elaboración de este manual se basa en una metodología de investigación-acción participativa:

1. **Observación comunitaria:** escuchamos a los voceros y voceras.
2. **Diagnóstico sociotécnico:** comprendimos cómo se comunica la comunidad hoy.
3. **Diseño colaborativo:** definimos páginas y contenidos junto a quienes toman decisiones.
4. **Implementación técnica:** construimos la estructura estática con código simple.
5. **Transferencia tecnológica:** escribimos este manual para que ustedes lo usen.
6. **Reflexión y ajuste:** cada cambio debe ser validado con el Consejo Comunal.

Cada sección de este manual está pensada como una guía de acompañamiento para que las acciones que ustedes tomen sean seguras, transparentes y replicables.

## 1.6 Principios de uso comunitario

- **Primero: claridad.** Si no entiendes una parte, detente y consulta con otros voceros.
- **Segundo: respaldo.** Siempre guarda una copia local antes de cambios importantes.
- **Tercero: responsabilidad.** Los cambios en la página representan la voz de la comunidad.
- **Cuarto: continuidad.** Actualiza con regularidad para mantener la confianza.
- **Quinto: colaboración.** Usa este manual como herramienta de formación para nuevos voceros y voceras.

---

# PARTE 2: GUÍA DE INICIO RÁPIDO (5 MINUTOS DE EMERGENCIA)

## 2.1 La importancia de los primeros 5 minutos

En una comunidad, la rapidez es clave. Si hay un corte de agua, una reunión urgente o un anuncio de salud, los primeros cinco minutos cuentan.

Por eso creamos esta sección para actuar con seguridad. Sigue estos pasos exactamente y utiliza esta guía como tu “botiquín digital”.

## 2.2 Paso 1: Preparar tu entorno de trabajo

### 2.2.1 Instalar Visual Studio Code

Visual Studio Code es el editor de texto recomendado para trabajar con el sitio. Es gratis y funciona bien en sistemas básicos.

- Abre el navegador web de tu preferencia.
- Ingresa a `https://code.visualstudio.com/`.
- Haz clic en “Download for Linux” si usas Linux, o elige la versión correspondiente.
- Sigue los pasos de instalación.

Una vez instalado, abre Visual Studio Code y carga la carpeta `VILLA-ROSARIO`.

### 2.2.2 ¿Por qué usamos Visual Studio Code?

Usamos Visual Studio Code porque:

- Nos muestra el contenido de los archivos fácilmente.
- Resalta el código para que sea más claro.
- Permite buscar palabras y cambiar texto sin errores.
- Tiene atajos útiles como `Ctrl + S`, `Ctrl + Z` y `Ctrl + F`.

## 2.3 Paso 2: Abrir la carpeta del proyecto

En Visual Studio Code:

1. Haz clic en `File` o `Archivo`.
2. Selecciona `Open Folder` o `Abrir carpeta`.
3. Busca la carpeta `VILLA-ROSARIO`.
4. Haz clic en `Open` o `Abrir`.

Cuando la carpeta esté abierta, verás todos los archivos del proyecto en el panel izquierdo.

## 2.4 Paso 3: Encontrar el archivo correcto

Para un cambio rápido, identifica la página que debes editar:

- `index.html` → cambios urgentes en la portada.
- `articulos.html` → noticias generales.
- `noticia.html` → detalle de una noticia.
- `eventos.html` → actividades.
- `proyectos.html` → avances de obras.
- `servicios.html` → estado de los servicios.
- `emprendedores.html` → negocios locales.
- `consejo-comunal.html` → organizacion comunitaria.
- `historia.html` → memoria histórica.
- `contacto.html` → datos de contacto.

## 2.5 Paso 4: Guardar y deshacer con Ctrl + Z

### 2.5.1 Guardar cambios

Siempre que hagas un cambio, guarda el archivo con:

- `Ctrl + S`

Esto asegura que tus cambios queden grabados en el archivo.

### 2.5.2 Deshacer un error con Ctrl + Z

Si escribes algo mal, puedes regresar al paso anterior con:

- `Ctrl + Z`

Esto es el salvavidas comunitario. Úsalo cada vez que necesites corregir una palabra, una etiqueta o un texto.

### 2.5.3 Rehacer con Ctrl + Y

Si deshaces algo por accidente, puedes rehacer el cambio con:

- `Ctrl + Y`

## 2.6 Paso 5: Verificar en el navegador

Una vez que guardes los cambios, abre el archivo HTML en tu navegador.

En Visual Studio Code:

1. Haz clic derecho sobre el archivo.
2. Selecciona `Reveal in File Explorer` o `Abrir en explorador`.
3. Abre el archivo con tu navegador (Chrome, Firefox, Edge, Brave).

Después de abrirlo, recarga la página con:

- `F5`

Si la página no se ve bien, vuelve a VS Code y usa `Ctrl + Z`.

## 2.7 Resumen rápido del flujo de emergencia

1. Abrir `VILLA-ROSARIO` en Visual Studio Code.
2. Encontrar el archivo HTML correcto.
3. Editar el texto que corresponde en la zona indicada.
4. Guardar con `Ctrl + S`.
5. Volver a cargar el navegador con `F5`.
6. Si hay error, presionar `Ctrl + Z`.

---

# PARTE 3: MANUAL DE USUARIO COMPLETO (SABER QUÉ EDITAR LÍNEA POR LÍNEA)

## 3.1 Cómo funciona el contenido de cada página

Vamos a explicar página por página, línea por línea, qué editar y cómo hacerlo de manera segura.

### 3.1.1 Página de Inicio - `index.html`

La portada es la ventana principal de la comunidad. Aquí es donde se ven las alertas, las noticias más relevantes, el carrusel y el estado de servicios.

#### Sección de bienvenida y descripción

Busca el bloque que contiene el título principal y la descripción de Villa Rosario.

```html
<h1>Villa Rosario</h1>
<p>Comunidad organizada en el Sector Sabilar de la Parroquia Altagracia. Nuestro objetivo es compartir información clara y actualizada.</p>
```

Cambia el texto únicamente entre `>` y `<`.

#### Estadísticas de la comunidad

Más abajo encontrarás números importantes.

```html
<div class="estadistica">
    <span>136</span>
    <p>Familias</p>
</div>
<div class="estadistica">
    <span>335</span>
    <p>Habitantes</p>
</div>
<div class="estadistica">
    <span>4</span>
    <p>Calles</p>
</div>
<div class="estadistica">
    <span>2009</span>
    <p>Año de fundación</p>
</div>
```

Si cambias un número, hazlo solo dentro del `<span>`.

#### Sistema de alertas comunitarias

La portada contiene alertas en tres colores. Ellas indican situaciones diferentes.

- **Urgente (roja):** cortes de servicio, emergencias.
- **Info (azul):** avisos importantes de interés general.
- **Evento (verde):** actividades, jornadas y celebraciones.

Ejemplo de alerta urgente:

```html
<div class="alerta-item alerta-urgente">
    <div class="alerta-icono">
        <i class="fas fa-exclamation-triangle"></i>
    </div>
    <div class="alerta-texto">
        <h3>Corte de Agua en Sector Sur</h3>
        <p>El suministro de agua estará suspendido de 8:00 a 14:00 por reparación de tubería principal.</p>
        <span>24 ABR 2026</span>
    </div>
</div>
```

Para cambiar una alerta, edita el título, la descripción y la fecha.

Ejemplo de alerta informativa:

```html
<div class="alerta-item alerta-info">
    <div class="alerta-icono">
        <i class="fas fa-info-circle"></i>
    </div>
    <div class="alerta-texto">
        <h3>Asamblea del Consejo Comunal</h3>
        <p>La asamblea será el próximo viernes a las 4:00 p.m. en el salón comunal.</p>
        <span>26 ABR 2026</span>
    </div>
</div>
```

Ejemplo de alerta de evento:

```html
<div class="alerta-item alerta-evento">
    <div class="alerta-icono">
        <i class="fas fa-calendar-check"></i>
    </div>
    <div class="alerta-texto">
        <h3>Feria de Emprendedores</h3>
        <p>Apoya a los negocios locales este sábado con productos artesanales y alimentos.</p>
        <span>30 ABR 2026</span>
    </div>
</div>
```

#### Modificar el carrusel de imágenes

El carrusel muestra cuatro imágenes que rotan automáticamente.

Busca el bloque:

```html
<div class="carrusel">
    <div class="carrusel-slide active">
        <img src="imagenes/carrusel1.png" alt="Imagen de la comunidad">
    </div>
    <div class="carrusel-slide">
        <img src="imagenes/carrusel2.png" alt="Actividad comunitaria">
    </div>
    <div class="carrusel-slide">
        <img src="imagenes/carrusel3.png" alt="Proyecto local">
    </div>
    <div class="carrusel-slide">
        <img src="imagenes/carrusel4.jpg" alt="Reunión del consejo">
    </div>
    <button class="carrusel-control prev"><i class="fas fa-arrow-left"></i></button>
    <button class="carrusel-control next"><i class="fas fa-arrow-right"></i></button>
    <div class="carrusel-indicadores">
        <span class="indicador active"></span>
        <span class="indicador"></span>
        <span class="indicador"></span>
        <span class="indicador"></span>
    </div>
</div>
```

Para cambiar una imagen, reemplaza la ruta del archivo dentro de `src="..."`. La ruta debe apuntar a `imagenes/` y al nombre exacto del archivo.

> Ejemplo: `src="imagenes/carrusel4.jpg"`.

#### Noticias destacadas en la portada

Las noticias de la portada usan tarjetas.

```html
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-bullhorn"></i> ANUNCIO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Campaña de limpieza en Sector Sabilar</h3>
        <p>Este sábado nos reunimos para organizar la jornada de limpieza y mejoramiento de espacios públicos.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=1" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

Para agregar una nueva noticia, copia uno de estos bloques y cambia `id=1` por un nuevo número único.

#### Estado de los servicios públicos

En la portada puedes ver un resumen de los servicios con estados.

```html
<div class="servicio-card" id="servicio-agua">
    <div class="servicio-header">
        <i class="fas fa-tint"></i>
        <h3>Agua Potable</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-bueno">Bueno</span>
        <p>Servicio funcionando normalmente en la mayor parte de la comunidad.</p>
    </div>
</div>
```

Cambia la clase `.estado-bueno` por `.estado-regular` o `.estado-malo` según corresponda.

### 3.1.2 Página de Noticias - `articulos.html`

Esta página es el archivo donde están todas las noticias acumuladas. Aquí se muestran varias tarjetas y los visitantes pueden leer los anuncios del Consejo Comunal.

#### Cambiar el título principal

```html
<h1>Todas las Noticias</h1>
<p>Mantente informado con las últimas novedades de la comunidad</p>
```

Puedes cambiarlo por:

```html
<h1>Noticias del Consejo Comunal</h1>
<p>Actualizaciones oficiales del sector Sabilar y la parroquia Altagracia.</p>
```

#### Agregar una noticia completa

Este es un bloque copiable y editable:

```html
<article class="noticia-card" data-categoria="servicios">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-tint"></i> AGUA</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>⚠️ Corte programado de agua potable</h3>
        <p>La empresa de agua realizó trabajos en la tubería principal. El servicio estará suspendido por aproximadamente 6 horas. Pedimos comprensión a la comunidad.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=2" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

#### Editar categoría y icono

En el bloque anterior, puedes cambiar `data-categoria` y el icono según la categoría real.

- `fa-tint` → Agua
- `fa-bolt` → Electricidad
- `fa-users` → Asamblea
- `fa-heartbeat` → Salud
- `fa-road` → Infraestructura
- `fa-store` → Economía
- `fa-bullhorn` → Comunicación
- `fa-calendar-check` → Evento

### 3.1.3 Página de Servicios - `servicios.html`

En esta página se gestiona el directorio semafórico de servicios. Cada servicio muestra estado y un detalle breve.

#### Estructura de un servicio

```html
<div class="servicio-card" id="servicio-electricidad">
    <div class="servicio-header">
        <i class="fas fa-bolt"></i>
        <h3>Electricidad</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-regular">Regular</span>
        <p>Tensiones inestables en algunos sectores, mantenimiento programado.</p>
    </div>
</div>
```

#### Cambiar el estado

El semáforo usa tres clases visuales:

- `estado-bueno` → verde
- `estado-regular` → amarillo
- `estado-malo` → rojo

Para reflejar un problema grave, usa:

```html
<span class="estado-badge estado-malo">Malo</span>
```

#### Añadir nueva gestión

Las gestiones son acciones realizadas por el Consejo Comunal.

```html
<div class="gestion-item">
    <div class="gestion-fecha">
        <i class="far fa-calendar-alt"></i> 1 MAY 2026
    </div>
    <div class="gestion-contenido">
        <h4>Reunión con HIDROCARIBE</h4>
        <p>Se acordó plan de mantenimiento para corregir fugas en la tubería principal de Villa Rosario.</p>
    </div>
</div>
```

### 3.1.4 Página de Proyectos - `proyectos.html`

Esta página muestra los proyectos comunitarios. Allí se puede actualizar el avance de las obras.

#### Bloque de un proyecto

```html
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Mejoras de la Plaza Central</h3>
        <span class="proyecto-estado">En Ejecución</span>
    </div>
    <div class="proyecto-body">
        <p>Reparación de bancas, alumbrado público y accesos peatonales.</p>
        <p><strong>Responsable:</strong> Comité de Infraestructura</p>
        <p><strong>Inversión:</strong> Bs. 2.500.000</p>
        <p><strong>Avance:</strong> 65%</p>
        <p><strong>Siguientes pasos:</strong> Colocación de luminarias y pintura de señalización.</p>
    </div>
</div>
```

#### Modificar el porcentaje de avance

Cambia el valor del avance dentro del texto:

```html
<p><strong>Avance:</strong> 65%</p>
```

Si deseas cambiar el estado del proyecto, puedes editar la etiqueta de estado:

```html
<span class="proyecto-estado">Completado</span>
```

#### Ejemplo de proyecto nuevo

```html
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Rehabilitación del pozo comunitario</h3>
        <span class="proyecto-estado">Planificado</span>
    </div>
    <div class="proyecto-body">
        <p>Instalación de bomba nueva y sistema de filtrado para garantizar agua limpia.</p>
        <p><strong>Responsable:</strong> Comité de Agua</p>
        <p><strong>Inversión:</strong> Bs. 1.200.000</p>
        <p><strong>Avance:</strong> 10%</p>
        <p><strong>Siguientes pasos:</strong> Compra de materiales y coordinación con proveedores.</p>
    </div>
</div>
```

### 3.1.5 Página de Emprendedores - `emprendedores.html`

Aquí se promocionan los negocios locales.

#### Cómo editar un perfil de emprendedor

```html
<div class="emprendedor-card">
    <div class="emprendedor-imagen">
        <img src="imagenes/emprendedor1.jpg" alt="Emprendedor local">
    </div>
    <div class="emprendedor-texto">
        <h3>Panadería Dulce Sabilar</h3>
        <p><strong>Propietario:</strong> María López</p>
        <p>Panadería artesanal con productos frescos y panes tradicionales.</p>
        <p><strong>Teléfono:</strong> 0414-1234567</p>
        <p><strong>Ubicación:</strong> Calle Principal, frente a la plaza.</p>
        <p><strong>Horario:</strong> Lunes a sábado, 7:00 a.m. a 5:00 p.m.</p>
    </div>
</div>
```

Cambia la ruta de la imagen si agregas una nueva foto, y modifica el texto con los datos reales del emprendedor.

### 3.1.6 Página de Consejo Comunal - `consejo-comunal.html`

Esta página describe la organización del Consejo Comunal y los comités del sector.

#### Bloque de comité

```html
<div class="comite-card">
    <i class="fas fa-water"></i>
    <h3>Comité de Agua</h3>
    <p>Encargado de la vigilancia del servicio y la relación con proveedores del sector.</p>
</div>
```

#### Agregar un nuevo comité

```html
<div class="comite-card">
    <i class="fas fa-seedling"></i>
    <h3>Comité de Seguridad Alimentaria</h3>
    <p>Responsable de promover cultivos, huertos sociales y apoyo nutricional para la comunidad.</p>
</div>
```

#### Cambio de vocero o vocera

Busca el bloque en el que aparecen los nombres de los voceros y reemplaza el texto de la misma forma.

```html
<h3>Vocero Principal</h3>
<p>Nombre: Juan Pérez</p>
<p>Teléfono: 0414-7654321</p>
```

### 3.1.7 Página de Historia - `historia.html`

Esta página es la memoria de Villa Rosario. Contiene relatos, fechas y eventos relevantes.

#### Modificar el texto histórico

```html
<section class="historia-seccion">
    <h2>Origen de Villa Rosario</h2>
    <p>Villa Rosario surge en 2009 como una iniciativa de familias del sector Sabilar para organizar mejor los servicios públicos y la vida comunitaria.</p>
</section>
```

Puedes añadir un nuevo párrafo con la historia de un evento reciente:

```html
<section class="historia-seccion">
    <h2>La primera gran asamblea</h2>
    <p>En 2025 se realizó la primera asamblea abierta de mujeres y jóvenes para discutir el plan de mejoramiento de caminos.</p>
</section>
```

### 3.1.8 Página de Eventos - `eventos.html`

La página de eventos informa a la comunidad sobre fechas, horarios y lugares.

#### Bloque de evento

```html
<div class="evento-card">
    <h3>Jornada de Limpieza en el Sector Sur</h3>
    <p><strong>Fecha:</strong> 5 MAY 2026</p>
    <p><strong>Hora:</strong> 8:00 a.m.</p>
    <p><strong>Lugar:</strong> Plaza Central</p>
    <p>Reunión de voluntarios y limpieza de áreas públicas para mantener el entorno seguro.</p>
</div>
```

#### Agregar un evento nuevo

```html
<div class="evento-card">
    <h3>Feria de Salud Comunitaria</h3>
    <p><strong>Fecha:</strong> 12 MAY 2026</p>
    <p><strong>Hora:</strong> 9:00 a.m.</p>
    <p><strong>Lugar:</strong> Centro Comunitario</p>
    <p>Atenciones médicas, charlas de prevención y vacunación para niños y adultos.</p>
</div>
```

### 3.1.9 Página de Noticia individual - `noticia.html`

Esta página muestra el detalle completo cuando el visitante hace clic en “VER DETALLES”.

#### Estructura de la noticia

```html
<article class="noticia-detalle">
    <h1>Título de la noticia</h1>
    <p class="noticia-fecha">24 ABR 2026</p>
    <div class="noticia-contenido">
        <p>Contenido completo de la noticia con todos los detalles necesarios para la comunidad.</p>
        <p>Explicación de la acción, la razón, la fecha y la persona responsable.</p>
    </div>
</article>
```

Si el archivo `noticia.html` usa un parámetro `?id=`, no cambies la parte `noticia.html?id=...` en los bloques de noticias; solo cambia el número.

### 3.1.10 Página de Contacto - `contacto.html`

Si existe, esta página puede incluir los datos de contacto del Consejo Comunal.

#### Ejemplo de bloque de contacto

```html
<section class="contacto">
    <h2>Contacto del Consejo Comunal</h2>
    <p><strong>Dirección:</strong> Sector Sabilar, Parroquia Altagracia</p>
    <p><strong>Teléfonos:</strong> 0414-1234567, 0414-7654321</p>
    <p><strong>Correo:</strong> contacto@villarosario.gob.ve</p>
</section>
```

Puedes editar los datos con base en la información oficial del Consejo Comunal.

## 3.2 El sistema de 3 alertas comunitarias

La comunicación oficial se apoya en tres tipos de alertas claramente diferenciadas:

- **Alerta Urgente - Roja**: medida de emergencia, corte de servicios, riesgo inmediato.
- **Alerta Informativa - Azul**: anuncio administrativo, reunión, convocatoria.
- **Alerta de Evento - Verde**: actividades comunitarias, ferias, jornadas.

### 3.2.1 Alerta Urgente

```html
<div class="alerta-item alerta-urgente">
    <div class="alerta-icono"><i class="fas fa-exclamation-circle"></i></div>
    <div class="alerta-texto">
        <h3>Emergencia: Fuga de gas</h3>
        <p>La brigada vecinal solicita no usar fuego abierto en el sector mientras se restablece la seguridad.</p>
        <span>24 ABR 2026</span>
    </div>
</div>
```

### 3.2.2 Alerta Informativa

```html
<div class="alerta-item alerta-info">
    <div class="alerta-icono"><i class="fas fa-info-circle"></i></div>
    <div class="alerta-texto">
        <h3>Información importante</h3>
        <p>La próxima asamblea comunitaria se realizará en la escuela el 28 de abril a las 3:00 p.m.</p>
        <span>24 ABR 2026</span>
    </div>
</div>
```

### 3.2.3 Alerta de Evento

```html
<div class="alerta-item alerta-evento">
    <div class="alerta-icono"><i class="fas fa-calendar-check"></i></div>
    <div class="alerta-texto">
        <h3>Festival de la Cultura</h3>
        <p>Ven con tu familia a disfrutar de música, baile y gastronomía local este domingo.</p>
        <span>30 ABR 2026</span>
    </div>
</div>
```

### 3.2.4 Cómo elegir el tipo de alerta

- Usa **roja** si se trata de una emergencia o un corte inmediato.
- Usa **azul** si es una noticia relevante pero no urgente.
- Usa **verde** si es una invitación a eventos o actividades.

Esto ayuda a la comunidad a reconocer visualmente el carácter del mensaje.

## 3.3 Cómo alterar tarjetas de noticias de forma segura

Las tarjetas de noticias contienen tres partes:

1. Cabecera con categoría e icono.
2. Cuerpo con título y descripción.
3. Pie con el enlace a detalles.

### 3.3.1 Ejemplo completo de noticia

```html
<article class="noticia-card" data-categoria="salud">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-heartbeat"></i> SALUD</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Jornada de vacunación en el consultorio</h3>
        <p>El comité de salud invita a las familias a participar en la jornada de vacunación contra la gripe y el dengue.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=3" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

### 3.3.2 Cambiar la categoría

La categoría está en la primera línea de la cabecera. Solo cambia el texto y el icono:

```html
<span class="noticia-categoria"><i class="fas fa-road"></i> INFRAESTRUCTURA</span>
```

### 3.3.3 Actualizar la fecha

La fecha debe ir en mayúsculas y con el formato `24 ABR 2026`.

```html
<span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
```

### 3.3.4 Enlace a noticia única

Asegúrate de usar un número único en el enlace: `noticia.html?id=4`.

Si repites el mismo número, dos noticias pueden mostrar el mismo detalle o confundir la navegación.

## 3.4 Cómo modificar porcentajes de avance en `proyectos.html`

Cuando editas proyectos, el valor más importante es el porcentaje de avance. Esto indica cuánto falta para terminar la obra.

### 3.4.1 Ejemplo de avance

```html
<p><strong>Avance:</strong> 65%</p>
```

Cambia solamente el número antes del porcentaje.

### 3.4.2 Registrar el siguiente paso

Siempre agrega lo siguiente después del porcentaje:

```html
<p><strong>Siguientes pasos:</strong> Colocación de luminarias y pintura de señalización.</p>
```

Esto permite que la comunidad sepa qué viene después, no solo cuánto se ha hecho.

### 3.4.3 Actualizar responsables

Siempre que el responsable cambie, edita este bloque:

```html
<p><strong>Responsable:</strong> Comité de Infraestructura</p>
```

Así los vecinos saben a quién acudir con preguntas.

## 3.5 Cómo gestionar el directorio semafórico de `servicios.html`

En `servicios.html`, el semáforo se muestra con tres colores mediante clases CSS.

### 3.5.1 Clase de estado bueno

```html
<span class="estado-badge estado-bueno">Bueno</span>
```

### 3.5.2 Clase de estado regular

```html
<span class="estado-badge estado-regular">Regular</span>
```

### 3.5.3 Clase de estado malo

```html
<span class="estado-badge estado-malo">Malo</span>
```

### 3.5.4 Descripción del servicio

Acompaña el estado con una explicación clara:

```html
<p class="texto-extra">Servicio estable. Próximo mantenimiento para el 28 de abril.</p>
```

Si el servicio está en emergencia, describe la causa y el tiempo estimado.

### 3.5.5 Ejemplo de servicio de agua en emergencia

```html
<div class="servicio-card" id="servicio-agua">
    <div class="servicio-header">
        <i class="fas fa-tint"></i>
        <h3>Agua Potable</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-malo">Malo</span>
        <p class="texto-extra">Falta de presión debido a rotura en la línea principal. HIDROCARIBE trabaja en la reparación. Normalización en 48 horas.</p>
    </div>
</div>
```

### 3.5.6 Ejemplo de servicio de electricidad estable

```html
<div class="servicio-card" id="servicio-electricidad">
    <div class="servicio-header">
        <i class="fas fa-bolt"></i>
        <h3>Electricidad</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-bueno">Bueno</span>
        <p class="texto-extra">El sistema eléctrico está funcionando sin inconvenientes.</p>
    </div>
</div>
```

### 3.5.7 Ejemplo de servicio de internet

```html
<div class="servicio-card" id="servicio-internet">
    <div class="servicio-header">
        <i class="fas fa-wifi"></i>
        <h3>Internet</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-regular">Regular</span>
        <p class="texto-extra">Servicio intermitente en horas pico. Requiere seguimiento técnico.</p>
    </div>
</div>
```

## 3.6 Consejos para editar sin romper el diseño

### 3.6.1 No eliminar etiquetas HTML importantes

El HTML funciona como una casa. Si quitas una pared (`</div>`) la casa se cae visualmente.

Nunca borres solamente una etiqueta cercana; siempre revisa el par completo:

- `<div></div>`
- `<h3></h3>`
- `<p></p>`
- `<article></article>`
- `<section></section>`

Si ves un bloque con varias líneas, edita solo el texto dentro de él.

### 3.6.2 No cambiar nombres de clases CSS

Las clases como `alerta-item`, `noticia-card`, `estado-badge`, `servicio-card` tienen funciones específicas. No las cambies, porque el diseño depende de ellas.

### 3.6.3 Mantener el orden de los bloques

Si agregas una noticia nueva o un evento nuevo, colócalo dentro de la misma sección donde están los otros elementos. Esto ayuda a que la página se muestre ordenada.

### 3.6.4 Evitar editar `css/estilo.css` y `js/main.js`

Estas dos carpetas definen el estilo y el comportamiento. Si modificas `css/estilo.css` o `js/main.js`, podrías causar problemas en todas las páginas.

Si necesitas un cambio visual profundo, consúltalo primero con el equipo UPTOS o con el vocero técnico.

---

# PARTE 4: HOJA DE TRUCOS Y BANCO DE 15+ PLANTILLAS (COPIAR Y PEGAR)

## 4.1 Cómo usar este banco de plantillas

Este capítulo es tu caja de herramientas. Aquí encontrarás bloques de código listos para copiar y pegar directamente en los archivos HTML.

Cada plantilla tiene un comentario de inicio y fin que te ayudará a identificarla.

## 4.2 Plantilla 1: Alerta urgente roja

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="alerta-item alerta-urgente">
    <div class="alerta-icono">
        <i class="fas fa-exclamation-triangle"></i>
    </div>
    <div class="alerta-texto">
        <h3>Emergencia Comunitaria</h3>
        <p>Información urgente sobre corte de servicios o riesgo para la comunidad.</p>
        <span>24 ABR 2026</span>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.3 Plantilla 2: Alerta informativa azul

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="alerta-item alerta-info">
    <div class="alerta-icono">
        <i class="fas fa-info-circle"></i>
    </div>
    <div class="alerta-texto">
        <h3>Información Importante</h3>
        <p>Comunicado del Consejo Comunal para la comunidad de Villa Rosario.</p>
        <span>25 ABR 2026</span>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.4 Plantilla 3: Alerta de evento verde

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="alerta-item alerta-evento">
    <div class="alerta-icono">
        <i class="fas fa-calendar-check"></i>
    </div>
    <div class="alerta-texto">
        <h3>Actividad Comunitaria</h3>
        <p>Invitación abierta para participar en la próxima jornada de trabajo comunitario.</p>
        <span>30 ABR 2026</span>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.5 Plantilla 4: Noticia de servicio

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="servicios">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-tint"></i> AGUA</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Corte programado de agua potable</h3>
        <p>HIDROCARIBE realizará mantenimiento en la tubería principal. El servicio estará suspendido durante seis horas.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=10" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.6 Plantilla 5: Noticia de evento

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="evento">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-calendar-check"></i> EVENTO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 26 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Feria de emprendedores locales</h3>
        <p>Presentación de productos artesanales y servicios comunitarios. Actividad abierta a todos los vecinos.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=11" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.7 Plantilla 6: Noticia de salud

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="salud">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-heartbeat"></i> SALUD</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Jornada de vacunación contra la influenza</h3>
        <p>Atención gratuita para niños, adultos mayores y embarazadas en el consultorio local.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=12" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.8 Plantilla 7: Evento comunitario

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="evento-card">
    <h3>Jornada de limpieza en el Sector Sabilar</h3>
    <p><strong>Fecha:</strong> 5 MAY 2026</p>
    <p><strong>Hora:</strong> 8:00 a.m.</p>
    <p><strong>Lugar:</strong> Plaza central del sector</p>
    <p>Invitamos a todas las familias a participar en la limpieza de espacios públicos y el retiro de escombros.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.9 Plantilla 8: Gestión comunitaria

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="gestion-item">
    <div class="gestion-fecha">
        <i class="far fa-calendar-alt"></i> 1 MAY 2026
    </div>
    <div class="gestion-contenido">
        <h4>Diálogo con representantes municipales</h4>
        <p>El Consejo Comunal gestionó recursos para el mejoramiento de la red de agua potable.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.10 Plantilla 9: Proyecto comunitario

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Habilitación del parque infantil</h3>
        <span class="proyecto-estado">En Ejecución</span>
    </div>
    <div class="proyecto-body">
        <p>Se trabaja en la instalación de juegos infantiles seguros y recuperación de espacios verdes.</p>
        <p><strong>Responsable:</strong> Comité de Obras</p>
        <p><strong>Inversión:</strong> Bs. 3.000.000</p>
        <p><strong>Avance:</strong> 40%</p>
        <p><strong>Siguientes pasos:</strong> Colocación de juegos y pintura de espacios.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.11 Plantilla 10: Emprendedor local

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="emprendedor-card">
    <div class="emprendedor-imagen">
        <img src="imagenes/emprendedor1.jpg" alt="Emprendedor local">
    </div>
    <div class="emprendedor-texto">
        <h3>Panadería Dulce Sabilar</h3>
        <p><strong>Propietario:</strong> María López</p>
        <p>Panadería artesanal con productos recién horneados y atención familiar.</p>
        <p><strong>Teléfono:</strong> 0414-1234567</p>
        <p><strong>Ubicación:</strong> Avenida principal, frente a la iglesia.</p>
        <p><strong>Horario:</strong> Lunes a sábado, 7:00 a.m. a 5:00 p.m.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.12 Plantilla 11: Comité de trabajo

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="comite-card">
    <i class="fas fa-seedling"></i>
    <h3>Comité de Agricultura</h3>
    <p>Promueve prácticas agrícolas sostenibles y huertos comunitarios en Villa Rosario.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.13 Plantilla 12: Comité de seguridad

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="comite-card">
    <i class="fas fa-shield-alt"></i>
    <h3>Comité de Seguridad</h3>
    <p>Organiza rondas vecinales y estrategias para el cuidado de nuestros espacios comunitarios.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.14 Plantilla 13: Mensaje institucional

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<section class="mensaje-institucional">
    <h2>Mensaje del Consejo Comunal</h2>
    <p>El Consejo Comunal de Villa Rosario invita a todos los vecinos a participar en la próxima asamblea general para fortalecer la organización local.</p>
</section>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.15 Plantilla 14: Texto de bienvenida

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<section class="bienvenida">
    <h2>Bienvenidos a Villa Rosario</h2>
    <p>Este espacio digital es la voz oficial del Consejo Comunal. Aquí comunicamos eventos, noticias y servicios para toda la comunidad.</p>
</section>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.16 Plantilla 15: Pie de página comunitario

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<footer class="footer-comunitario">
    <p>Consejo Comunal Villa Rosario - Sector Sabilar - Parroquia Altagracia - Municipio Sucre</p>
    <p>Documento apoyado por la UPTOS como transferencia tecnológica para la comunidad.</p>
</footer>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.17 Plantilla 16: Tarjeta de acción rápida

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="accion-rapida">
    <h3>Apoyo a familias vulnerables</h3>
    <p>Coordinación del Consejo Comunal para entregar alimentos y asistencia social en el sector.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## 4.18 Lista de clases CSS de uso común

Estas son las clases más importantes que usarás para editar el contenido sin cambiar el diseño:

- `navbar`
- `alerta-item`
- `alerta-urgente`
- `alerta-info`
- `alerta-evento`
- `noticia-card`
- `noticia-header`
- `noticia-body`
- `noticia-footer`
- `noticia-categoria`
- `noticia-fecha`
- `btn-leer-mas`
- `carrusel`
- `carrusel-slide`
- `carrusel-control`
- `carrusel-indicadores`
- `servicio-card`
- `servicio-header`
- `servicio-body`
- `estado-badge`
- `estado-bueno`
- `estado-regular`
- `estado-malo`
- `gestion-item`
- `historia-seccion`
- `evento-card`
- `proyecto-card`
- `emprendedor-card`
- `comite-card`
- `mensaje-institucional`
- `bienvenida`
- `footer-comunitario`

## 4.19 Lista de iconos Font Awesome integrados

Aquí tienes los iconos que se usan en el sitio y su significado:

| Icono | Nombre | Uso |
|-------|--------|-----|
| `fas fa-tint` | gota | Agua potable |
| `fas fa-bolt` | rayo | Electricidad |
| `fas fa-users` | personas | Asamblea / comunidad |
| `fas fa-heartbeat` | pulso | Salud |
| `fas fa-road` | carretera | Infraestructura |
| `fas fa-store` | tienda | Emprendedores |
| `fas fa-bullhorn` | megáfono | Comunicados |
| `fas fa-calendar-check` | calendario | Eventos |
| `fas fa-exclamation-triangle` | advertencia | Alerta urgente |
| `fas fa-info-circle` | información | Alerta informativa |
| `fas fa-arrow-right` | flecha | Botón leer más |
| `fas fa-shield-alt` | escudo | Seguridad |
| `fas fa-seedling` | brote | Medio ambiente / agricultura |
| `fas fa-wifi` | wifi | Internet |
| `fas fa-map-marker-alt` | ubicación | Ubicación |
| `far fa-calendar-alt` | calendario borde | Fecha |
| `fas fa-arrow-left` | flecha izquierda | Navegación carrusel |
| `fas fa-arrow-right` | flecha derecha | Navegación carrusel |
| `fas fa-exclamation-circle` | círculo con exclamación | Emergencia |
| `fas fa-check-circle` | check | Confirmación |

## 4.20 Cómo clonar bloques sin errores

1. Selecciona el bloque completo entre `<!-- Comentario UPTOS: Copie desde aquí -->` y `<!-- Comentario UPTOS: Copie hasta aquí -->`.
2. Copia con `Ctrl + C`.
3. Pega en el lugar correspondiente con `Ctrl + V`.
4. Ajusta solo los textos, la fecha y los valores numéricos.
5. Verifica que el bloque sigue dentro de la sección correcta.

## 4.21 Recomendaciones para usar plantillas

- Usa una plantilla por noticia.
- No copies plantillas dentro de otras plantillas.
- Mantén el mismo formato de etiquetas.
- Si usas imágenes nuevas, colócalas en la carpeta `imagenes/` con nombre claro.

---

# PARTE 5: GUÍA TÉCNICA, GIT Y DESPLIEGUE (GITHUB DESKTOP PASO A PASO)

## 5.1 ¿Qué es Git y por qué lo usamos?

Git es una herramienta que guarda cambios en el tiempo. Para Villa Rosario, Git permite que el Consejo Comunal vea quién cambió qué, cuándo y por qué.

GitHub es la plataforma donde se aloja el repositorio y desde donde se publica el sitio en la web.

Nosotros recomendamos GitHub Desktop porque es visual, sencillo y evita comandos difíciles. Es la puerta de entrada para los voceros que quieren publicar cambios sin escribir líneas de terminal.

## 5.2 Instalación de GitHub Desktop

1. Abre el navegador.
2. Ve a `https://desktop.github.com/`.
3. Descarga la versión para tu sistema operativo.
4. Instala siguiendo las instrucciones.
5. Inicia sesión con tu cuenta de GitHub.

Si no tienen cuenta de GitHub, pidan apoyo a un miembro del Consejo o al equipo UPTOS para crear una cuenta.

## 5.3 Flujo de publicación: guardar, validar, commit y push

El ciclo de trabajo es siempre el mismo. Nosotros lo llamamos el ciclo de sincronización comunitaria.

### 5.3.1 Guardar local

En Visual Studio Code, presiona `Ctrl + S` después de cada cambio.

### 5.3.2 Abrir el entorno de trabajo

En GitHub Desktop, abre el repositorio `VILLA-ROSARIO`.

### 5.3.3 Validar rama `main`

Asegúrate de trabajar en la rama principal llamada `main`.

- Si no estás en `main`, cámbiate a `main`.
- Si tienes cambios en otra rama, consulta primero.

### 5.3.4 Redactar mensaje de Commit

El mensaje de commit debe ser claro y breve. Por ejemplo:

- "Actualizar noticia de evento del 24 de abril"
- "Cambiar estado de agua a emergencia"
- "Agregar nuevo emprendedor local"

Nunca dejes el mensaje en blanco. El mensaje es la memoria de lo que hiciste.

### 5.3.5 Hacer Push a Origin

En GitHub Desktop, haz clic en `Push origin`.

Esto envía los cambios al repositorio en GitHub.

## 5.4 Publicar la página en GitHub Pages

Una vez que el push se completa, GitHub Pages procesa el sitio. El tiempo de recarga puede ser de:

- **60 a 120 segundos**

Si no ves el cambio inmediatamente en la web, espera dos minutos y recarga el navegador.

## 5.5 Proceso completo paso a paso

1. Abrir `VILLA-ROSARIO` en Visual Studio Code.
2. Editar el contenido deseado en el archivo correspondiente.
3. Guardar con `Ctrl + S`.
4. Abrir GitHub Desktop.
5. Seleccionar el repositorio `VILLA-ROSARIO`.
6. Verificar que la rama activa es `main`.
7. Revisar los cambios en la pestaña `Changes`.
8. Escribir un mensaje claro en `Summary`.
9. Hacer clic en `Commit to main`.
10. Hacer clic en `Push origin`.
11. Esperar 60-120 segundos.
12. Abrir el sitio en `https://thegoatzzbad02-blip.github.io/VILLA-ROSARIO/`.
13. Recargar la página con `F5`.

## 5.6 Consejos para buenos mensajes de commit

Un mensaje de commit efectivo debe tener:

- Acción: qué hiciste.
- Objeto: dónde lo hiciste.
- Propósito: por qué lo hiciste.

Ejemplos:

- "Actualizar alerta urgente de agua".
- "Agregar nuevo evento comunitario".
- "Corregir fecha de reunión en noticia".
- "Ajustar estado de electricidad a regular".

## 5.7 Manejo de cambios locales y conflictos simples

### 5.7.1 Mantén tu copia actualizada

Antes de comenzar a editar, pide a alguien que haga `Fetch origin` o `Pull origin` en GitHub Desktop.

Esto te asegura que trabajas con la versión más reciente del sitio.

### 5.7.2 Conflictos de cambios

Si otra persona editó el mismo archivo y hay conflicto, GitHub Desktop te mostrará un mensaje.

En ese caso:

1. No hagas push.
2. Revisa los cambios de ambas versiones.
3. Escoge el texto correcto o combina ambos textos.
4. Guarda el archivo.
5. Haz commit y luego push.

### 5.7.3 Ejemplo de conflicto

- María cambió el título de la noticia.
- Juan cambió la misma noticia al mismo tiempo.

La solución es leer ambas versiones y escribir un texto único que contenga lo mejor de los dos.

## 5.8 Información adicional del repositorio

### 5.8.1 Archivo `README.md`

El archivo `README.md` es un documento de presentación del proyecto. No es obligatorio modificarlo, pero puede ser útil si quieres agregar instrucciones extra para futuros administradores.

### 5.8.2 Carpeta `imagenes/`

Las imágenes deben guardarse en esta carpeta. El nombre de cada archivo debe ser:

- claro
- sin espacios
- todo en minúsculas
- con la extensión correcta (`.jpg`, `.png`)

Ejemplo correcto: `imagenes/carrusel4.jpg`

Ejemplo incorrecto: `imagenes/Carrusel 4.JPG`

### 5.8.3 Ruta exacta de imágenes

Dentro del HTML siempre usa:

```html
<img src="imagenes/nombre-del-archivo.jpg" alt="Descripción de la imagen">
```

No uses rutas como `../` o rutas externas si no son necesarias.

## 5.9 Control de versiones como acto comunitario

Cada commit debe ser un registro de acción comunitaria. Cuando haces push, no solo subes un archivo; en realidad estás logrando:

- transparencia
- memoria colectiva
- seguimiento de decisiones
- responsabilidad

Nosotros hacemos énfasis en que el registro de Git es parte de la gobernanza del Consejo Comunal.

## 5.10 Cómo compartir el manual con la comunidad

Una vez que el manual maestro está completo, puedes compartirlo de varias formas:

- Copiar el archivo `MANUAL_MAESTRO_VILLA_ROSARIO.md` en Google Drive.
- Descargarlo desde GitHub como archivo Markdown.
- Imprimirlo en PDF si necesitas versiones físicas.
- Usarlo como material de capacitación para voceros nuevos.

---

# PARTE 6: RESOLUCIÓN DE PROBLEMAS Y FAQ COMUNITARIA DE LA UPTOS

## 6.1 Introducción a la resolución de problemas comunitaria

Como equipo investigador de la UPTOS, entendemos que la comunidad necesita respuestas claras y prácticas. Esta parte del manual contiene preguntas frecuentes que surgen en el día a día, especialmente durante la edición y publicación del sitio.

Hacemos énfasis en la colaboración: si no resuelves un problema, comparte la pregunta con los demás voceros y con el equipo UPTOS.

## 6.2 Matriz de problemas y soluciones

| Problema | Causa más común | Solución UPTOS |
|----------|-----------------|----------------|
| Página se ve desordenada | Falta de cierre de etiquetas HTML | Revisa y cierra `</div>`, `</section>`, `</article>` |
| Imagen no carga | Nombre de archivo equivocado o extensión incorrecta | Verifica en `imagenes/` y usa el nombre exacto |
| Cambios no aparecen en GitHub | No se hizo push o GitHub Pages aún no actualiza | Haz push, espera 60-120 seg y recarga |
| Alertas con color equivocado | Clase CSS mal escrita | Usa `alerta-urgente`, `alerta-info`, `alerta-evento` |
| Botón “VER DETALLES” no funciona | URL de noticia incorrecta | Corrige `noticia.html?id=...` con número único |
| Imagen aparece rota | Ruta `src` incorrecta | Usa `src="imagenes/archivo.jpg"` exacto |
| Título duplicado en varias noticias | Repetiste el mismo `id` | Asigna un nuevo `id` en el enlace |
| Cambio borrado por otro vocero | No se actualizó antes de editar | Haz `Fetch` o `Pull` antes de editar |
| Estado de servicio no coincide | Clase incorrecta en badge | Usa `estado-bueno`, `estado-regular`, `estado-malo` |
| Página se queda en blanco | Etiqueta HTML abierta o falta `</body>` | Revisa el final del archivo completo |
| Navegación no resalta la página activa | Clase JavaScript no se aplicó | No edites `js/main.js`; revisa `index.html` y `nav` |
| Evento con fecha antigua | No actualizaste el texto | Cambia la fecha en el bloque del evento |
| Proyecto sin avance | No incluiste el porcentaje | Añade `<p><strong>Avance:</strong> XX%</p>` |
| Texto cortado en noticia | Párrafo sin cierre `</p>` | Agrega el cierre correcto |
| Página no carga en teléfono | Error en HTML o CSS no compatible | Revisa etiquetas y evita errores de sintaxis |
| Imagen en carrusel no aparece | Archivo inexistente | Copia el archivo a `imagenes/` y actualiza `src` |
| Botón del carrusel no responde | JavaScript mal cargado | No modifiques `js/main.js`; revisa `index.html` para incluirlo |
| No sé qué archivo editar | Sin identificación de contenido | Usa el índice de este manual y la tabla de archivos |
| Cambio en carpeta equivocada | No abriste `VILLA-ROSARIO` correcto | Verifica la ruta del proyecto en VS Code |
| Sitio en vivo desactualizado | GitHub Pages tardó en refrescar | Espera 60-120 seg y recarga el navegador |
| No encuentro `contacto.html` | Página sugerida no creada | Puedes crearla siguiendo la plantilla del manual |
| Conflicto en GitHub Desktop | Dos cambios en la misma línea | Revisa ambas versiones y combina la información |
| Error con extensión de imagen | `.jpg` vs `.JPG` | Usa siempre minúsculas y el nombre exacto |
| Texto con símbolos raros | Caracteres especiales mal copiados | Escribe el texto directamente en VS Code |
| Página se muestra sin estilos | CSS no cargó | Verifica que el archivo `css/estilo.css` exista y no lo renombraste |

## 6.3 FAQ comunitaria

### Pregunta 1: ¿Qué hago si la imagen no se carga?

**Respuesta:** Busca el nombre del archivo en `imagenes/`. Luego revisa el valor de `src="imagenes/..."` en el HTML. Debe coincidir exactamente, incluyendo mayúsculas y minúsculas.

### Pregunta 2: ¿Por qué la página se ve desordenada?

**Respuesta:** Normalmente es porque falta cerrar una etiqueta. Usa la vista del archivo en VS Code y verifica que cada `<div>` tenga su `</div>`, cada `<section>` tenga su `</section>` y cada `<article>` su `</article>`.

### Pregunta 3: ¿Qué es `ctrl + z` y por qué es importante?

**Respuesta:** `Ctrl + Z` deshace el último cambio. Es tu mejor herramienta cuando cometes un error. Si la página no se ve bien después de un cambio, presiona `Ctrl + Z` hasta regresar al estado anterior.

### Pregunta 4: ¿Puedo editar `css/estilo.css`?

**Respuesta:** No se recomienda. Solo los responsables técnicos de la UPTOS o del Consejo Comunal deben hacerlo. Si necesitas un cambio de diseño, pide soporte.

### Pregunta 5: ¿Puedo editar `js/main.js`?

**Respuesta:** No. Este archivo controla el carrusel y la navegación. No edites `js/main.js` a menos que el equipo UPTOS lo autorice.

### Pregunta 6: ¿Cómo puedo cambiar la fecha en una noticia?

**Respuesta:** Localiza el bloque de la noticia y cambia el texto dentro de la etiqueta `span` que contiene la fecha. Usa el formato `24 ABR 2026`.

### Pregunta 7: ¿Qué hago si el enlace `VER DETALLES` no funciona?

**Respuesta:** Revisa el valor de `href="noticia.html?id=..."`. Debe ser un número único y el archivo `noticia.html` debe existir.

### Pregunta 8: ¿Por qué mi cambio no aparece en la página web en vivo?

**Respuesta:** Si hiciste push en GitHub, espera 60-120 segundos. GitHub Pages procesa los cambios y tarda un poco en actualizarse.

### Pregunta 9: ¿Por qué mi imagen aparece rota después de subirla?

**Respuesta:** Revisa que el archivo exista en la carpeta `imagenes/` con el mismo nombre que aparece en `src="imagenes/archivo.jpg"`. Asegúrate de que no tenga espacios ni mayúsculas inesperadas.

### Pregunta 10: ¿Qué es un commit?

**Respuesta:** Un commit es un registro de cambios. En GitHub Desktop, cada commit explica qué cambiaste en el proyecto.

### Pregunta 11: ¿Qué significa `Push origin`?

**Respuesta:** Significa enviar tus cambios desde tu computadora al repositorio remoto en GitHub.

### Pregunta 12: ¿Qué hago si encuentro un conflicto en GitHub Desktop?

**Respuesta:** No sigas adelante. Revisa ambas versiones del archivo y combina la parte correcta. Si no sabes, pide ayuda al equipo UPTOS.

### Pregunta 13: ¿Puedo crear un nuevo archivo HTML?

**Respuesta:** Sí, si es necesario y si lo hace el equipo técnico. Para nuevos contenidos, consulten primero con el Consejo Comunal.

### Pregunta 14: ¿Cómo agrego una nueva noticia en `articulos.html`?

**Respuesta:** Copia una tarjeta de noticia existente, pega en el mismo lugar y cambia el texto, la fecha, la categoría y el `id` en el enlace.

### Pregunta 15: ¿Qué hago si borré una sección entera por accidente?

**Respuesta:** Usa `Ctrl + Z`. Si no es suficiente, revisa el historial de GitHub Desktop y vuelve al commit anterior.

### Pregunta 16: ¿Cómo cambio el estado de un servicio de `Regular` a `Bueno`?

**Respuesta:** Edita la clase del badge y el texto. Por ejemplo:

```html
<span class="estado-badge estado-bueno">Bueno</span>
```

### Pregunta 17: ¿Cuál es el mejor formato de fecha?

**Respuesta:** Usa siempre `DD MMM YYYY` en mayúsculas, por ejemplo `24 ABR 2026`.

### Pregunta 18: ¿Qué hago si una página abre en blanco?

**Respuesta:** Revisa si falta una etiqueta de cierre `</body>` o `</html>`. Es común cuando se elimina una parte de un bloque.

### Pregunta 19: ¿Cómo agrego una nueva imagen al carrusel?

**Respuesta:** Copia la imagen a la carpeta `imagenes/`, luego edita el bloque del carrusel y actualiza `src="imagenes/nombre.jpg"`.

### Pregunta 20: ¿Qué es una plantilla de código?

**Respuesta:** Es un bloque listo para copiar y pegar con la estructura correcta. Las plantillas de este manual tienen comentarios `<!-- Comentario UPTOS: Copie desde aquí -->`.

### Pregunta 21: ¿Cómo identifico la página actual en la navegación?

**Respuesta:** La barra de navegación tiene un estilo activo. No necesitas cambiar nada manualmente; el archivo `js/main.js` se encarga de resaltar la página actual.

### Pregunta 22: ¿Puedo cambiar el texto del botón `VER DETALLES`?

**Respuesta:** Sí, puedes cambiarlo por otra frase breve, pero recomendamos mantenerlo claro y uniforme en todas las noticias.

### Pregunta 23: ¿Qué debo hacer si añado muchas noticias?

**Respuesta:** Mantén el orden cronológico y utiliza el mismo formato en cada tarjeta. Evita mezclar plantillas diferentes en la misma sección.

### Pregunta 24: ¿Cómo veo el historial de cambios?

**Respuesta:** En GitHub Desktop, selecciona la pestaña `History`, donde aparecen todos los commits.

### Pregunta 25: ¿Está todo en la nube o necesito copias de seguridad?

**Respuesta:** El repositorio está en GitHub, pero siempre recomendamos guardar una copia local adicional en un USB o en Google Drive.

### Pregunta 26: ¿Qué hacer si cambio una clase CSS por error?

**Respuesta:** Vuelve a la versión anterior con `Ctrl + Z` o revisa el historial de GitHub Desktop para restaurar el archivo.

### Pregunta 27: ¿Cómo añado un nuevo emprendedor?

**Respuesta:** Copia un bloque de emprendedor existente, pega en la sección de emprendedores y cambia la imagen, el nombre, la descripción y el teléfono.

### Pregunta 28: ¿Puedo usar emojis en los títulos?

**Respuesta:** Sí, puedes usar emojis como `⚠️` o `📌` en títulos de noticias para llamar la atención, siempre que el texto siga siendo claro.

### Pregunta 29: ¿Qué hago si la página se muestra sin colores?

**Respuesta:** Verifica que el archivo `css/estilo.css` aún esté en la carpeta `css/`. No debe haber sido eliminado ni renombrado.

### Pregunta 30: ¿Por qué el enlace `noticia.html?id=` es importante?

**Respuesta:** Ese parámetro identifica la noticia específica y permite que el archivo `noticia.html` muestre el detalle correcto.

## 6.4 Resolución técnica de errores frecuentes

### Error 1: Imagen rota por extensión `.jpg` vs `.JPG`

**Solución:** Usa siempre la extensión exacta tal como aparece en la carpeta. Si la imagen está guardada como `carrusel4.jpg`, escribe exactamente `carrusel4.jpg`.

### Error 2: Etiqueta `<div>` abierta que descuadra el diseño

**Solución:** Busca la línea donde falta el cierre `</div>`. Puedes usar la función de búsqueda de VS Code para encontrar bloques que no están cerrados.

### Error 3: Página no carga después de editar

**Solución:** Revisa si hay errores de sintaxis en el HTML. Un `<p>` sin cerrar o una comilla faltante en `src="..."` suele causar problemas.

### Error 4: Commit sin mensaje claro

**Solución:** Vuelve a GitHub Desktop, escribe un mensaje claro y vuelve a hacer commit. Si ya hiciste push, añade otro commit con corrección.

### Error 5: Conflicto en GitHub Desktop

**Solución:** Lee cada versión, combina el texto apropiado y guarda el fichero. Luego confirma el commit.

## 6.5 Buenas prácticas de mantenimiento

- **Actualiza semanalmente** la información de eventos y servicios.
- **Registra cada cambio** con mensajes claros en GitHub Desktop.
- **Comparte este manual** con nuevos voceros y voceras.
- **Usa plantillas** para mantener el formato uniforme.
- **No edites el CSS/JS sin la aprobación del Consejo Comunal.**

## 6.6 Estrategia de capacitación comunitaria

Nosotros recomendamos la siguiente ruta de capacitación:

1. Primer día: leer PARTE 1 y PARTE 2.
2. Segundo día: practicar con la edición de una noticia y una alerta.
3. Tercer día: publicar un cambio usando GitHub Desktop.
4. Cuarto día: revisar la página en vivo y confirmar la actualización.
5. Quinto día: compartir este manual con un nuevo vocero.

Esta ruta asegura que la transferencia tecnológica sea real y no solo teórica.

## 6.7 Cierre pedagógico

Este manual maestro es la entrega formal de la transferencia tecnológica. Está diseñado para que el Consejo Comunal de Villa Rosario tenga autonomía técnica, memoria colectiva y capacidad de gestión digital.

La UPTOS recorre con ustedes este camino, pero el conocimiento queda en la comunidad. Cada cambio que hagan aquí es una acción política, social y técnica para fortalecer el tejido comunitario.

---

## 6.8 Glosario de términos

- **Consejo Comunal:** Espacio de organización comunitaria local.
- **Voceros y voceras:** Representantes elegidos para comunicar y coordinar.
- **Transferencia tecnológica:** Entrega de herramientas y saberes técnicos a la comunidad.
- **Repositorio:** Carpeta en GitHub donde se guarda el sitio.
- **Commit:** Registro de un cambio específico.
- **Push:** Envío de cambios a GitHub.
- **GitHub Pages:** Servicio que publica la página en internet.
- **HTML estático:** Páginas que se muestran como están guardadas, sin base de datos.
- **CSS:** Archivo que define el estilo y los colores.
- **JavaScript:** Código que controla el comportamiento interactivo.

## 6.9 Notas finales del equipo UPTOS

Nosotros, el equipo investigador de la UPTOS, hemos elaborado este documento con la intención de que sea un recurso permanente para Villa Rosario. Aquí no hay atajos ni instrucciones incompletas. Todo está pensado para que la comunidad avance con seguridad técnica y con sentido sociocultural.

Este manual es para ustedes. Úsenlo, compártanlo, mejorenlo y conviértanlo en parte de la memoria del Consejo Comunal.

---

**MANUAL MAESTRO DE VILLA ROSARIO**

**Versión 1.0 Maestro**

**Fecha de entrega:** Junio 2026

**Elaborado por:** Equipo de Investigadores y Desarrolladores UPTOS

**Finalidad:** Entrega formal de la transferencia tecnológica a los voceros y voceras del Consejo Comunal de Villa Rosario, Sector Sabilar, Parroquia Altagracia, Municipio Sucre.
---

# ANEXO A: GUÍA AVANZADA DE CADA ARCHIVO HTML

## A.1 `index.html` en detalle línea por línea

En esta sección desglosamos cada sección de la página de inicio para que los voceros comprendan exactamente qué cambiar y por qué. Utilizamos una lectura paso a paso que funciona como un mapa para ediciones seguras.

### A.1.1 Encabezado principal y navegación

El bloque de la navegación es el mismo en todas las páginas. Si el menú está en mal estado, la causa casi siempre es un error en `nav` o en el cierre de etiquetas.

Ejemplo:

```html
<nav class="navbar">
    <a href="index.html" class="nav-logo">Villa Rosario</a>
    <ul class="nav-menu">
        <li><a href="index.html">Inicio</a></li>
        <li><a href="consejo-comunal.html">Consejo Comunal</a></li>
        <li><a href="articulos.html">Noticias</a></li>
        <li><a href="servicios.html">Servicios</a></li>
        <li><a href="proyectos.html">Proyectos</a></li>
        <li><a href="emprendedores.html">Emprendedores</a></li>
        <li><a href="historia.html">Historia</a></li>
        <li><a href="eventos.html">Eventos</a></li>
    </ul>
</nav>
```

Este bloque no debe ser alterado si no tienes experiencia en HTML. Cambiar la estructura de los enlaces puede romper la navegación en todas las páginas.

### A.1.2 Sección de bienvenida y héroe visual

La sección de bienvenida está diseñada para mostrar la identidad comunitaria. El texto se puede actualizar libremente siempre que mantengas el formato del HTML.

```html
<section class="hero">
    <div class="hero-texto">
        <h1>Bienvenidos a Villa Rosario</h1>
        <p>Plataforma del Consejo Comunal del Sector Sabilar para informar a la comunidad.</p>
        <div class="hero-estadisticas">
            <div class="estadistica">
                <span>136</span>
                <p>Familias</p>
            </div>
            <div class="estadistica">
                <span>335</span>
                <p>Habitantes</p>
            </div>
            <div class="estadistica">
                <span>4</span>
                <p>Calles</p>
            </div>
            <div class="estadistica">
                <span>2009</span>
                <p>Año de fundación</p>
            </div>
        </div>
    </div>
    <div class="hero-imagen">
        <img src="imagenes/carrusel1.png" alt="Villa Rosario">
    </div>
</section>
```

#### Qué puedes cambiar

- El texto de `<h1>` y `<p>`.
- Los valores numéricos dentro de cada `<span>`.
- El título de cada estadística.
- La fuente de la imagen en `src` si agregas una nueva imagen.

#### Qué no debes cambiar

- No borres las etiquetas `<div class="estadistica">`.
- No cambies la clase `hero-estadisticas`.
- No muevas la imagen fuera del bloque `hero-imagen`.

### A.1.3 Bloque de alertas comunitarias

Las alertas son piezas clave. Cada una debe tener un color específico y un propósito claramente diferenciado.

#### Alerta urgente roja completa

```html
<div class="alerta-item alerta-urgente">
    <div class="alerta-icono">
        <i class="fas fa-exclamation-triangle"></i>
    </div>
    <div class="alerta-texto">
        <h3>Falla de luz en la parte alta</h3>
        <p>El corte de electricidad afecta a los sectores altos de Villa Rosario hasta nuevo aviso.</p>
        <span>24 ABR 2026</span>
    </div>
</div>
```

#### Alerta informativa azul completa

```html
<div class="alerta-item alerta-info">
    <div class="alerta-icono">
        <i class="fas fa-info-circle"></i>
    </div>
    <div class="alerta-texto">
        <h3>Convocatoria de asamblea</h3>
        <p>Los voceros convocan a una asamblea general para el lunes a las 3:00 p.m. en la plaza.
        <span>24 ABR 2026</span>
    </div>
</div>
```

#### Alerta de evento verde completa

```html
<div class="alerta-item alerta-evento">
    <div class="alerta-icono">
        <i class="fas fa-calendar-check"></i>
    </div>
    <div class="alerta-texto">
        <h3>Feria de emprendimiento local</h3>
        <p>Este domingo habrá feria de productos locales y talleres de autogestión.</p>
        <span>30 ABR 2026</span>
    </div>
</div>
```

### A.1.4 Sección de noticias destacadas

La sección de noticias de la portada muestra los hechos más importantes.

#### Ejemplo completo de noticias destacadas

```html
<section class="noticias-destacadas">
    <article class="noticia-card" data-categoria="comunicado">
        <div class="noticia-header">
            <span class="noticia-categoria"><i class="fas fa-bullhorn"></i> COMUNICADO</span>
            <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
        </div>
        <div class="noticia-body">
            <h3>Señalización de calles colectivas</h3>
            <p>El Consejo Comunal promueve la instalación de señales para mejorar la seguridad en el Sector Sabilar.</p>
        </div>
        <div class="noticia-footer">
            <a href="noticia.html?id=4" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
        </div>
    </article>
    <article class="noticia-card" data-categoria="evento">
        <div class="noticia-header">
            <span class="noticia-categoria"><i class="fas fa-calendar-check"></i> EVENTO</span>
            <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 30 ABR 2026</span>
        </div>
        <div class="noticia-body">
            <h3>Jornada de trabajo voluntario</h3>
            <p>Vecinos y vecinas se reúnen para limpiar y sembrar árboles en la avenida principal.</p>
        </div>
        <div class="noticia-footer">
            <a href="noticia.html?id=5" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
        </div>
    </article>
</section>
```

### A.1.5 Cómo interpretar `data-categoria`

El atributo `data-categoria` se utiliza en el sitio para clasificar visualmente las noticias. No altera el estilo, pero es una buena práctica mantenerlo claro.

- `data-categoria="comunicado"`
- `data-categoria="evento"`
- `data-categoria="servicios"`
- `data-categoria="salud"`
- `data-categoria="infraestructura"`
- `data-categoria="economia"`

### A.1.6 Bloque de servicios en la portada

Aquí se ofrece un resumen rápido del estado de los servicios.

```html
<section class="servicios-resumen">
    <div class="servicio-card" id="servicio-agua">
        <div class="servicio-header">
            <i class="fas fa-tint"></i>
            <h3>Agua Potable</h3>
        </div>
        <div class="servicio-body">
            <span class="estado-badge estado-bueno">Bueno</span>
            <p>El agua está llegando con presión estable en la mayoría de los sectores.</p>
        </div>
    </div>
    <div class="servicio-card" id="servicio-electricidad">
        <div class="servicio-header">
            <i class="fas fa-bolt"></i>
            <h3>Electricidad</h3>
        </div>
        <div class="servicio-body">
            <span class="estado-badge estado-regular">Regular</span>
            <p>Se han reportado interrupciones breves en la parte alta.</p>
        </div>
    </div>
</section>
```

### A.1.7 Mapa de navegación y enlaces permanentes

La página de inicio incluye enlaces directos a otras páginas. Si deseas agregar un enlace nuevo, hazlo con cuidado y verifica la ruta.

Ejemplo de enlace a `proyectos.html`:

```html
<a href="proyectos.html" class="btn-ver-mas">Ver todos los proyectos</a>
```

## A.2 `articulos.html` detallado

Artículos es el archivo donde se concentra la memoria informativa de Villa Rosario. Aquí se agrupan noticias, comunicados y avisos.

### A.2.1 Contenedor principal de noticias

El contenedor principal normalmente se ve así:

```html
<main>
    <div class="container">
        <div class="noticias-grid">
            <!-- Noticias individuales -->
        </div>
    </div>
</main>
```

Si quieres agregar una noticia, debes hacerlo dentro de `div.noticias-grid`, no fuera.

### A.2.2 Detalle completo de una noticia

Esta plantilla muestra un ejemplo de noticia clásica:

```html
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-bullhorn"></i> COMUNICADO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Se activa ruta de transporte comunitario</h3>
        <p>Se pactó un plan de transporte para los vecinos que necesitan movilizarse al mercado central.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=6" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

### A.2.3 Categorías de noticias comunes

Para mantener coherencia, utiliza estas categorías:

- COMUNICADO
- EVENTO
- SERVICIO
- SALUD
- INFRAESTRUCTURA
- ECONOMÍA
- EMPRÉNDEDORES
- EDUCACIÓN

### A.2.4 Criterios para priorizar noticias

Nosotros recomendamos publicar primero las noticias que impactan directamente la vida de la comunidad:

1. Servicios suspendidos o restablecidos.
2. Reuniones y asambleas del Consejo Comunal.
3. Proyectos en ejecución con plazos cercanos.
4. Eventos de participación comunitaria.
5. Acciones de apoyo social.

### A.2.5 Ejemplos de noticia urgente y aclaratoria

Cuando la noticia es urgente, el título debe ser claro y directo.

```html
<article class="noticia-card" data-categoria="servicios">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-tint"></i> AGUA</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Aviso de emergencia: baja presión en el sector norte</h3>
        <p>Se detectó una fuga importante en la tubería principal. Estamos gestionando con HIDROCARIBE la reparación urgente.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=7" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

### A.2.6 Ejemplo de noticia con llamada a la participación

```html
<article class="noticia-card" data-categoria="evento">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-users"></i> PARTICIPACIÓN</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 28 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Charla comunitaria sobre valorización del territorio</h3>
        <p>Invitamos a las familias a asistir y proponer ideas para el desarrollo local sostenible.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=8" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

## A.3 `eventos.html` en profundidad

El archivo de eventos es el calendario comunitario. Aquí puedes registrar actividades, jornadas, asambleas y festividades.

### A.3.1 Estructura básica de un evento

```html
<div class="evento-card">
    <h3>Título del evento</h3>
    <p><strong>Fecha:</strong> 12 MAY 2026</p>
    <p><strong>Hora:</strong> 9:00 a.m.</p>
    <p><strong>Lugar:</strong> Salón comunal</p>
    <p>Descripción del evento con información útil para la comunidad.</p>
</div>
```

### A.3.2 Ejemplo de evento de salud

```html
<div class="evento-card">
    <h3>Jornada de salud familiar</h3>
    <p><strong>Fecha:</strong> 10 MAY 2026</p>
    <p><strong>Hora:</strong> 8:00 a.m.</p>
    <p><strong>Lugar:</strong> Plaza central</p>
    <p>Atenciones médicas gratuitas, vacunación y charlas de prevención.</p>
</div>
```

### A.3.3 Ejemplo de evento de formación

```html
<div class="evento-card">
    <h3>Taller de administración comunitaria</h3>
    <p><strong>Fecha:</strong> 15 MAY 2026</p>
    <p><strong>Hora:</strong> 10:00 a.m.</p>
    <p><strong>Lugar:</strong> Casa de la Cultura</p>
    <p>Curso para voceros y voceras sobre planificación de actividades y rendición de cuentas.</p>
</div>
```

### A.3.4 Reglas para la publicación de eventos

-Siempre coloca la fecha más reciente primero.
-Mantén la información breve.
-Incluye el lugar exacto.
-Si hay un cambio de hora, actualiza la tarjeta completa.

## A.4 `proyectos.html` detallado

Esta página es la bitácora de las obras. Aquí registramos el proceso de cada proyecto.

### A.4.1 Elementos que debe contener un proyecto

Cada proyecto debe incluir:

- Título claro.
- Estado de la obra.
- Descripción de la intervención.
- Responsable.
- Monto de inversión.
- Porcentaje de avance.
- Siguientes pasos.

### A.4.2 Ejemplo de proyecto de infraestructura

```html
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Mejoramiento del sistema de drenaje</h3>
        <span class="proyecto-estado">En Ejecución</span>
    </div>
    <div class="proyecto-body">
        <p>Se colocan tuberías nuevas para evitar inundaciones en la temporada de lluvias.</p>
        <p><strong>Responsable:</strong> Comité de Infraestructura</p>
        <p><strong>Inversión:</strong> Bs. 2.800.000</p>
        <p><strong>Avance:</strong> 55%</p>
        <p><strong>Siguientes pasos:</strong> Inspección de la red de drenaje y pruebas de funcionamiento.</p>
    </div>
</div>
```

### A.4.3 Ejemplo de proyecto social

```html
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Creación de un punto de reciclaje comunitario</h3>
        <span class="proyecto-estado">Planificado</span>
    </div>
    <div class="proyecto-body">
        <p>Instalación de contenedores y campaña de concientización para separar residuos.</p>
        <p><strong>Responsable:</strong> Comité Ambiental</p>
        <p><strong>Inversión:</strong> Bs. 650.000</p>
        <p><strong>Avance:</strong> 15%</p>
        <p><strong>Siguientes pasos:</strong> Adquisición de contenedores y difusión comunitaria.</p>
    </div>
</div>
```

### A.4.4 Cambiar el porcentaje de avance en obras

Para editar correctamente, ubica la línea con la etiqueta `<strong>Avance:</strong>` y modifica solo el número. Siempre deja el porcentaje completo.

### A.4.5 Agregar un nuevo proyecto

1. Copia uno de los bloques completos.
2. Pega después del último proyecto dentro de la misma sección.
3. Cambia el título, estado, texto y valores.
4. Guarda y revisa en el navegador.

## A.5 `servicios.html` ampliado

En esta página, cada servicio tiene un semáforo que ayuda a la comunidad a identificar prioridades.

### A.5.1 Propuesta de estructura de servicio

```html
<div class="servicio-card" id="servicio-aseo">
    <div class="servicio-header">
        <i class="fas fa-trash-alt"></i>
        <h3>Aseo Urbano</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-regular">Regular</span>
        <p>Recolección irregular en el sector sur. Seguimiento en curso con la empresa responsable.</p>
    </div>
</div>
```

### A.5.2 Servicio de internet con detalle técnico

```html
<div class="servicio-card" id="servicio-internet">
    <div class="servicio-header">
        <i class="fas fa-wifi"></i>
        <h3>Internet</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-regular">Regular</span>
        <p>Velocidad reducida en la tarde. Se gestiona mejora con el proveedor local.</p>
    </div>
</div>
```

### A.5.3 Servicio de electricidad con estado crítico

```html
<div class="servicio-card" id="servicio-electricidad">
    <div class="servicio-header">
        <i class="fas fa-bolt"></i>
        <h3>Electricidad</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-malo">Malo</span>
        <p>Cortes frecuentes debido a fallas en la línea de media tensión. Se ha reportado al ente regulador.</p>
    </div>
</div>
```

### A.5.4 Cómo agregar un servicio nuevo

Si se incorpora un servicio adicional como seguridad, salud o transporte, sigue este ejemplo:

```html
<div class="servicio-card" id="servicio-seguridad">
    <div class="servicio-header">
        <i class="fas fa-shield-alt"></i>
        <h3>Seguridad</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-bueno">Bueno</span>
        <p>Ronda vecinal continua, trabajo coordinado con la comunidad.</p>
    </div>
</div>
```

## A.6 `emprendedores.html` con ejemplos extensos

Esta página busca visibilizar la economía local y brindar apoyo a los comerciantes del sector.

### A.6.1 Formato de la tarjeta de emprendedor

```html
<div class="emprendedor-card">
    <div class="emprendedor-imagen">
        <img src="imagenes/emprendedor2.jpg" alt="Foto de emprendedor">
    </div>
    <div class="emprendedor-texto">
        <h3>Panadería Dulce Sabilar</h3>
        <p><strong>Propietario:</strong> José Rodríguez</p>
        <p>Panadería con productos tradicionales y pan recién horneado.</p>
        <p><strong>Teléfono:</strong> 0414-9876543</p>
        <p><strong>Ubicación:</strong> Calle Luna esquina con Sol.</p>
        <p><strong>Horario:</strong> Martes a domingo, 6:00 a.m. a 6:00 p.m.</p>
    </div>
</div>
```

### A.6.2 Ejemplo de perfil de emprendimiento social

```html
<div class="emprendedor-card">
    <div class="emprendedor-imagen">
        <img src="imagenes/emprendedor3.jpg" alt="Foto de emprendedor social">
    </div>
    <div class="emprendedor-texto">
        <h3>Artesanías Sabilar</h3>
        <p><strong>Propietaria:</strong> Carmen Díaz</p>
        <p>Producto artesanal hecho por mujeres de la comunidad. Venta de tejidos y accesorios.</p>
        <p><strong>Teléfono:</strong> 0414-1112233</p>
        <p><strong>Ubicación:</strong> Plaza principal, local 3.</p>
        <p><strong>Horario:</strong> Lunes a sábado, 8:00 a.m. a 4:00 p.m.</p>
    </div>
</div>
```

### A.6.3 Ejemplo de perfil de servicio local

```html
<div class="emprendedor-card">
    <div class="emprendedor-imagen">
        <img src="imagenes/emprendedor4.jpg" alt="Foto de emprendedor de servicios">
    </div>
    <div class="emprendedor-texto">
        <h3>Transporte Sabilar</h3>
        <p><strong>Propietario:</strong> Luis Mendoza</p>
        <p>Servicios de transporte local para la comunidad con tarifas solidarias.</p>
        <p><strong>Teléfono:</strong> 0414-2223344</p>
        <p><strong>Ubicación:</strong> Parada central de Villa Rosario.</p>
        <p><strong>Horario:</strong> Todos los días de 5:00 a.m. a 7:00 p.m.</p>
    </div>
</div>
```

## A.7 `consejo-comunal.html` con lectura analítica

La página del Consejo Comunal es la expresión institucional de la comunidad.

### A.7.1 Sección de presentación institucional

```html
<section class="consejo-presentacion">
    <h2>Consejo Comunal Villa Rosario</h2>
    <p>Somos una organización social que representa a las familias del Sector Sabilar y trabajamos por el bienestar comunitario.</p>
</section>
```

### A.7.2 Sección de órganos de decisión

Este bloque describe quiénes participan en la toma de decisiones.

```html
<div class="organos-decision">
    <div class="organo-card">
        <h3>Asamblea de Ciudadanos</h3>
        <p>Órgano supremo donde se discuten y aprueban las decisiones colectivas.</p>
    </div>
    <div class="organo-card">
        <h3>Voceros</h3>
        <p>Representantes que coordinan la comunicación entre la comunidad y las instituciones.</p>
    </div>
    <div class="organo-card">
        <h3>Líderes de Calle</h3>
        <p>Personas encargadas de organizar el trabajo en cada calle y zona del sector.</p>
    </div>
</div>
```

### A.7.3 Sección de comités

```html
<div class="comites-lista">
    <div class="comite-card">
        <i class="fas fa-water"></i>
        <h3>Comité de Agua</h3>
        <p>Vigilancia del servicio y gestión con proveedores.</p>
    </div>
    <div class="comite-card">
        <i class="fas fa-bolt"></i>
        <h3>Comité de Energía</h3>
        <p>Seguimiento de problemas eléctricos y propuestas de mejora.</p>
    </div>
    <div class="comite-card">
        <i class="fas fa-seedling"></i>
        <h3>Comité Ambiental</h3>
        <p>Acciones de limpieza, reciclaje y cuidado del entorno.</p>
    </div>
</div>
```

### A.7.4 Cómo actualizar los nombres de los voceros

Busca el bloque con el nombre del vocero y actualiza el texto. Ejemplo:

```html
<div class="vocero-card">
    <h3>Nombre: María Peña</h3>
    <p>Teléfono: 0414-5556677</p>
</div>
```

## A.8 `historia.html` con contenidos participativos

La historia de Villa Rosario es una narración colectiva. Aquí se recomienda usar párrafos cortos y fechas importantes.

### A.8.1 Bloque de capítulos históricos

```html
<section class="historia-seccion">
    <h2>El origen del sector</h2>
    <p>Villa Rosario comenzó como un asentamiento de familias trabajadoras que buscaban acceso a servicios básicos. En 2009 emergió como una comunidad organizada.</p>
</section>
<section class="historia-seccion">
    <h2>La primera asamblea</h2>
    <p>En 2010 se celebró la primera asamblea junto con los vecinos del sector Sabilar. Allí se definió la estrategia de acción comunitaria.</p>
</section>
```

### A.8.2 Cómo agregar testimonios comunitarios

Puedes añadir testimonios con este formato:

```html
<section class="historia-seccion">
    <h2>Testimonio</h2>
    <p>"Nuestro sector ganó fuerza cuando nos organizamos en el Consejo Comunal. Hoy trabajamos en equipo y cuidamos lo nuestro."</p>
    <p><strong>- Vocera comunitaria</strong></p>
</section>
```

## A.9 `contacto.html` recomendado

Aunque el archivo no siempre esté presente, es buena idea tener una página de contacto preparada para la comunicación oficial.

### A.9.1 Ejemplo completo de contacto

```html
<section class="contacto">
    <h2>Contacto Oficial del Consejo Comunal</h2>
    <p><strong>Dirección:</strong> Sector Sabilar, Parroquia Altagracia</p>
    <p><strong>Teléfonos:</strong> 0414-1234567 / 0414-7654321</p>
    <p><strong>Correo electrónico:</strong> consejo@villarosario.com</p>
    <p><strong>Horario de atención:</strong> Lunes a viernes, 8:00 a.m. a 4:00 p.m.</p>
</section>
```

### A.9.2 Cómo crear la página si no existe

1. En Visual Studio Code, crea un archivo nuevo llamado `contacto.html`.
2. Copia la estructura básica de cualquier otra página.
3. Agrega el bloque de contacto dentro de `<main>`.
4. Guarda el archivo.
5. No olvides añadirlo al menú de navegación si lo deseas.

# ANEXO B: GUÍA DEL CSS Y CLASES DETALLADAS

## B.1 Cómo funcionan los estilos sin necesidad de editarlos

El archivo `css/estilo.css` define los colores, tamaños y posiciones de cada elemento. Aunque no lo edites, es útil entender su función.

### B.1.1 Variables de color

En `css/estilo.css` existen variables que almacenan colores. Estas variables se utilizan en todo el sitio. Ejemplos:

- `--color-amarillo` → usado en botones y acentos.
- `--color-azul` → usado en fondos y textos destacados.
- `--color-rojo` → usado para alertas urgentes.
- `--color-verde` → usado para alertas de evento y estados buenos.

Estas variables permiten cambiar el color en un solo lugar si fuera necesario.

## B.2 Principales clases de diseño

A continuación describimos el propósito de las clases más importantes.

### B.2.1 `navbar`

Controla la barra principal de navegación. Aquí se ubican los enlaces a las páginas del sitio.

### B.2.2 `alerta-item`

Define la apariencia de las tarjetas de alerta.

### B.2.3 `noticia-card`

Da estructura a cada noticia. Permite que las noticias se vean como tarjetas en fila.

### B.2.4 `servicio-card`

Da estilo a cada servicio dentro del semáforo.

### B.2.5 `estado-badge`

Muestra el estado del servicio con un color fuerte y texto visible.

### B.2.6 `proyecto-card`

Define la presentación de cada proyecto comunitario.

### B.2.7 `emprendedor-card`

Estructura el perfil de cada emprendimiento local.

### B.2.8 `evento-card`

Presenta la información de cada actividad o jornada.

### B.2.9 `comite-card`

Usado en la página del Consejo Comunal para presentar comités.

## B.3 Responsive design y dispositivos móviles

El sitio está preparado para verse bien en celulares y computadoras. Esto se logra con reglas de CSS que cambian la presentación dependiendo del tamaño de pantalla.

### B.3.1 Hamburger menu

En pantallas pequeñas, el menú cambia a un botón de 'hamburger' para ahorrar espacio.

### B.3.2 Columnas que se adaptan

Los bloques de noticias y servicios se muestran en varias columnas en pantallas grandes y en una sola columna en móviles.

### B.3.3 Por qué es importante no cambiar el CSS sin permiso

Cambiar `css/estilo.css` puede romper la adaptación móvil y dejar la página inusable en celulares. El diseño es parte de la experiencia comunitaria, por eso solo el equipo técnico debe hacerlo.

## B.4 Patrón de íconos y tipografía

El sitio usa Font Awesome para los iconos y Google Fonts para las letras. Estas fuentes e iconos hacen el sitio más amigable.

### B.4.1 Lista de fuentes

- `Poppins` → títulos y encabezados.
- `Roboto` → texto del cuerpo.

### B.4.2 Cómo se activan los iconos

Los iconos aparecen en clases como `fas fa-tint`. Es importante que esta clase no sea cambiada a otra sintaxis.

## B.5 Bloques críticos del estilo visual

### B.5.1 Hero principal

Se usan `hero`, `hero-texto` y `hero-imagen` para la portada.

### B.5.2 Tarjetas de contenido

Las noticias y servicios usan clases como `noticia-card` y `servicio-card` para mantener un diseño homogéneo.

### B.5.3 Botones y acciones

Los botones usan clases como `btn-leer-mas` y `btn-ver-mas` para que siempre tengan el mismo color y forma.

## B.6 Ejemplo de regla visual cuando trabajas con el contenido

Si necesitas cambiar el color de un texto, hazlo en el HTML solo si no hay clase. Ejemplo:

```html
<p style="color: #00247D;">Texto importante</p>
```

Pero nuestra recomendación es evitar estilos en línea y mantener el contenido limpio.

# ANEXO C: GUÍA DE JAVASCRIPT Y FUNCIONAMIENTO DEL CARRUSEL

## C.1 Comprendiendo el comportamiento interactivo

El archivo `js/main.js` controla las acciones del carrusel y la detección de la página activa en la navegación.

### C.1.1 ¿Por qué no editar `js/main.js`?

Porque cualquier cambio sin conocimiento puede detener el carrusel, hacer que los botones no funcionen o impedir que el menú reconozca la página actual.

### C.1.2 Funciones principales del `main.js`

Estas son las funciones importantes:

- `setActiveNavLink()` → resalta la página en la navegación.
- `closeMenuOnMobile()` → cierra el menú en celulares.
- `showSlide()` → muestra una diapositiva del carrusel.
- `nextSlide()` y `prevSlide()` → avanzan y retroceden en el carrusel.
- `startCarousel()` y `stopCarousel()` → inician y detienen la rotación automática.

## C.2 Cómo funciona el carrusel

El carrusel está diseñado para rotar cada 5 segundos. Si el visitante pasa el mouse sobre él, se detiene para que pueda leer la imagen.

### C.2.1 Insertar una nueva diapositiva

Para agregar una imagen más al carrusel, necesitas:

1. Copiar el bloque de una diapositiva existente.
2. Cambiar la ruta de la imagen en `src="imagenes/..."`.
3. Añadir un nuevo punto de indicador en `carrusel-indicadores`.
4. Verificar que el JavaScript admita más de cuatro diapositivas.

### C.2.2 Ejemplo de diapositiva adicional

```html
<div class="carrusel-slide">
    <img src="imagenes/carrusel5.jpg" alt="Nueva imagen comunitaria">
</div>
```

Y agrega un indicador extra:

```html
<span class="indicador"></span>
```

## C.3 Uso correcto de links compartidos

El archivo `js/main.js` a veces incluye botones para compartir en redes. Estos botones ayudan a divulgar la página, pero no forman parte del contenido principal.

No es necesario editar estos botones, salvo que debas cambiar el mensaje institucional.

## C.4 Verificación de la funcionalidad

Después de editar la página, abre el navegador y prueba:

- Que el carrusel avance solo.
- Que los botones anterior/siguiente funcionen.
- Que la barra de navegación resalte la página actual.

Si algo falla, no edites el JavaScript. Revisa primero si tu HTML está bien y si guardaste correctamente.

# ANEXO D: PLANTILLAS AVANZADAS DE CÓDIGO

## D.1 Plantilla avanzada de noticia con lista de puntos

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-bullhorn"></i> COMUNICADO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 24 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Recomendaciones comunitarias para el uso del agua</h3>
        <p>El Consejo Comunal solicita a las familias seguir estas indicaciones:</p>
        <ul>
            <li>Usar el agua solo para consumo y preparación de alimentos.</li>
            <li>Evitar el desperdicio en actividades no esenciales.</li>
            <li>Reportar fugas y pérdidas en sus casas.</li>
        </ul>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=9" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.2 Plantilla de noticia con subtítulo

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="infraestructura">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-road"></i> INFRAESTRUCTURA</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 26 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Mejoras en el camino rural</h3>
        <p><strong>Subtítulo:</strong> Se inicia la reparación de la vía principal del sector.</p>
        <p>Los trabajos incluyen nivelación, compactación y señalización de seguridad.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=10" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.3 Plantilla de evento con llamada a inscripción

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="evento-card">
    <h3>Encuentro de mujeres líderes</h3>
    <p><strong>Fecha:</strong> 18 MAY 2026</p>
    <p><strong>Hora:</strong> 9:00 a.m.</p>
    <p><strong>Lugar:</strong> Salón comunal</p>
    <p>Invitamos a las mujeres de Villa Rosario a participar en una jornada de liderazgo y empoderamiento.
    <strong>Confirma tu asistencia al teléfono 0414-1234567.</strong></p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.4 Plantilla de gestión con impacto social

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="gestion-item">
    <div class="gestion-fecha">
        <i class="far fa-calendar-alt"></i> 2 MAY 2026
    </div>
    <div class="gestion-contenido">
        <h4>Entrega de ayuda alimentaria</h4>
        <p>Se distribuyeron paquetes de alimentos básicos a 50 familias del Sector Sabilar.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.5 Plantilla de comité mixto

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="comite-card">
    <i class="fas fa-handshake"></i>
    <h3>Comité de Participación Ciudadana</h3>
    <p>Coordina la participación de los vecinos en asambleas, encuestas y proyectos de barrio.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.6 Plantilla de proyecto con fecha de finalización

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Recuperación de espacios deportivos</h3>
        <span class="proyecto-estado">En Ejecución</span>
    </div>
    <div class="proyecto-body">
        <p>Se realizan trabajos de reparación de la cancha y el coliseo comunitario.</p>
        <p><strong>Responsable:</strong> Comité de Deportes</p>
        <p><strong>Inversión:</strong> Bs. 1.800.000</p>
        <p><strong>Avance:</strong> 75%</p>
        <p><strong>Fecha estimada de finalización:</strong> 30 JUN 2026</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.7 Plantilla avanzada de emprendedor con redes sociales

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="emprendedor-card">
    <div class="emprendedor-imagen">
        <img src="imagenes/emprendedor5.jpg" alt="Emprendedor local con redes">
    </div>
    <div class="emprendedor-texto">
        <h3>Artesanías del Río</h3>
        <p><strong>Propietaria:</strong> Ana Torres</p>
        <p>Productos de tejido hechos a mano con materiales locales.</p>
        <p><strong>Teléfono:</strong> 0414-3334455</p>
        <p><strong>Ubicación:</strong> Mercado comunal.</p>
        <p><strong>Redes sociales:</strong> @artesaniasdelrio</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.8 Plantilla de anuncio institucional con llamada a acción

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<section class="mensaje-institucional">
    <h2>Convocatoria abierta</h2>
    <p>El Consejo Comunal invita a todos los vecinos a participar en el proceso de restauración del parque central.</p>
    <p><strong>Tu participación es importante para mejorar Villa Rosario.</strong></p>
</section>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.9 Plantilla de resumen de gestión con resultados

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="gestion-item">
    <div class="gestion-fecha">
        <i class="far fa-calendar-alt"></i> 3 MAY 2026
    </div>
    <div class="gestion-contenido">
        <h4>Informe de avances de agua</h4>
        <p>Se logró la reparación de la fuga principal y se restableció el suministro en el sector este.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## D.10 Plantilla de contacto con redes

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<section class="contacto">
    <h2>Contacto del Consejo Comunal</h2>
    <p><strong>Dirección:</strong> Sector Sabilar, Parroquia Altagracia</p>
    <p><strong>Teléfono:</strong> 0414-1234567</p>
    <p><strong>Correo:</strong> consejo@villarosario.com</p>
    <p><strong>Instagram:</strong> @consejocomunalvillarosario</p>
</section>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

# ANEXO E: MÁS FAQ Y CASOS PRÁCTICOS

## E.1 Pregunta 31: ¿Cómo creo una nueva sección de contenido?

**Respuesta:** Copia una sección existente completa, pégala en el lugar apropiado y cambia los textos. Asegúrate de mantener las etiquetas de apertura y cierre.

## E.2 Pregunta 32: ¿Cómo agrego un botón con enlace a otra página?

**Respuesta:** Usa este código:

```html
<a href="eventos.html" class="btn-ver-mas">Ver eventos</a>
```

Cambia `href` por la ruta correcta.

## E.3 Pregunta 33: ¿Cómo agrego una imagen nueva sin que se rompa?

**Respuesta:** Coloca la imagen en `imagenes/` y luego usa:

```html
<img src="imagenes/nombre-de-la-imagen.jpg" alt="Descripción">
```

Asegúrate de escribir el nombre exacto.

## E.4 Pregunta 34: ¿Cómo actualizo un enlace que apunta a `noticia.html`?

**Respuesta:** Cambia el número después de `id=`. Por ejemplo:

```html
<a href="noticia.html?id=20">VER DETALLES</a>
```

Cada noticia debe tener un número único.

## E.5 Pregunta 35: ¿Cómo publico un cambio si otro vocero ya hizo modificaciones?

**Respuesta:** En GitHub Desktop, haz `Fetch origin` o `Pull origin` antes de editar. Si ya hay cambios, sincroniza primero para evitar conflictos.

## E.6 Pregunta 36: ¿Qué es una rama y por qué no usamos otra rama?

**Respuesta:** Una rama es una copia del proyecto. En este caso usamos `main` para mantener todo en una sola línea, lo que facilita el trabajo comunitario.

## E.7 Pregunta 37: ¿Cómo recupero una versión anterior?

**Respuesta:** En GitHub Desktop, ve a `History`, selecciona el commit anterior y usa `Revert` o copia el texto correcto.

## E.8 Pregunta 38: ¿Qué debo escribir en el título del commit?

**Respuesta:** Usa frases como:

- "Actualizar alerta roja"
- "Agregar noticia de feria"
- "Corregir estado de agua"
- "Editar perfil de emprendedor"

## E.9 Pregunta 39: ¿Por qué se usan títulos con mayúsculas en las fechas?

**Respuesta:** Porque es un formato claro y consistente. Ejemplo: `24 ABR 2026`.

## E.10 Pregunta 40: ¿Cómo distingo un aviso urgente de un evento?

**Respuesta:** Por el color y el icono. Urgentes son rojas, eventos son verdes, informativas son azules.

## E.11 Pregunta 41: ¿Puedo cambiar los iconos de Font Awesome?

**Respuesta:** Sí, siempre que uses nombres correctos y que no cambien la estructura de la clase. Por ejemplo:

```html
<i class="fas fa-store"></i>
```

No cambies `fas` por `far` sin saber qué hace.

## E.12 Pregunta 42: ¿Cómo agrego otra noticia en la portada y en `articulos.html`?

**Respuesta:** Copia el bloque de una noticia existente, pégalo en ambas páginas y cambia el texto y el `id`.

## E.13 Pregunta 43: ¿Cómo reviso si hay errores antes de hacer push?

**Respuesta:** Visualiza el archivo en VS Code y prueba abrirlo en el navegador. Si la página no se carga, revisa etiquetas y enlaces antes de hacer push.

## E.14 Pregunta 44: ¿Qué hacer si veo texto en rojo en VS Code?

**Respuesta:** Eso indica un posible error de sintaxis. Revisa si hay comillas sin cerrar o etiquetas mal escritas.

## E.15 Pregunta 45: ¿Cómo añado un nuevo bloque de información en la página de Historia?

**Respuesta:** Sigue la estructura de secciones existentes. Por ejemplo:

```html
<section class="historia-seccion">
    <h2>Nuevo capítulo</h2>
    <p>Descripción del evento o testimonio.</p>
</section>
```

## E.16 Pregunta 46: ¿Puedo copiar contenido desde otra página?

**Respuesta:** Sí, pero verifica que las rutas de imágenes y enlaces sean correctas para el nuevo archivo.

## E.17 Pregunta 47: ¿Cómo agrego un comentario invisible para los editores?

**Respuesta:** Usa comentarios HTML:

```html
<!-- Comentario UPTOS: Este texto solo lo ve el editor -->
```

Los visitantes no verán ese texto en la página.

## E.18 Pregunta 48: ¿Cómo distinguir entre `class` y `id`?

**Respuesta:** `class` se usa para muchas piezas iguales. `id` se usa para un solo elemento específico.

Ejemplo:

- `class="servicio-card"` → varias tarjetas.
- `id="servicio-agua"` → tarjeta de agua específica.

## E.19 Pregunta 49: ¿Qué es un bloque `article`?

**Respuesta:** Es una estructura HTML que agrupa contenido independiente, como una noticia.

## E.20 Pregunta 50: ¿Cómo hago una copia de respaldo local?

**Respuesta:** Copia la carpeta `VILLA-ROSARIO` completa a un USB o carpeta segura. También puedes subirla a Google Drive.

## E.21 Caso práctico 1: Actualizar la alerta de agua

1. Abrir `index.html`.
2. Buscar la alerta roja actual.
3. Modificar el título y texto.
4. Guardar con `Ctrl + S`.
5. Abrir el archivo en el navegador.
6. Recargar con `F5`.

## E.22 Caso práctico 2: Añadir un nuevo emprendedor

1. Abrir `emprendedores.html`.
2. Copiar la tarjeta de un emprendedor existente.
3. Pegar después de la última tarjeta.
4. Cambiar el nombre, teléfono, ubicación y descripción.
5. Guardar.
6. Verificar en el navegador.

## E.23 Caso práctico 3: Crear una noticia de emergencia

1. Abrir `articulos.html`.
2. Copiar una noticia urgente.
3. Cambiar el tema a la emergencia actual.
4. Actualizar la fecha y el `id`.
5. Guardar y probar el enlace.

## E.24 Caso práctico 4: Ajustar un proyecto con nuevo avance

1. Abrir `proyectos.html`.
2. Buscar el proyecto.
3. Cambiar el porcentaje de avance.
4. Cambiar los siguientes pasos si hay novedades.
5. Guardar.
6. Verificar que el texto se lea bien.

## E.25 Caso práctico 5: Promocionar un evento de capacitación

1. Abrir `eventos.html`.
2. Copiar una tarjeta de evento.
3. Actualizar fecha, hora y lugar.
4. Agregar conclusiones breves.
5. Guardar y enviar el enlace a la comunidad.

# ANEXO F: PROCESOS Y METODOLOGÍAS UPTOS PARA LA COMUNIDAD

## F.1 Taller de introducción para nuevos voceros

Nosotros recomendamos un taller práctico de dos horas para nuevos voceros y voceras. El taller debe incluir:

1. Presentación del sitio.
2. Navegación por los archivos.
3. Edición de una noticia.
4. Guardado y prueba en navegador.
5. Publicación en GitHub Desktop.

### F.1.1 Materiales necesarios para el taller

- Computadora o laptop.
- Conexión a internet.
- Cuenta de GitHub.
- Acceso a Visual Studio Code.
- Copia del manual maestro.

### F.1.2 Objetivos del taller

- Comprender la estructura del sitio.
- Editar contenido básico.
- Publicar cambios en línea.
- Resolver problemas simples.

## F.2 Metodología de acompañamiento técnico

La transferencia tecnológica solo se consolida si se realiza con acompañamiento.

### F.2.1 Fase 1: Diagnóstico

Analizar con el Consejo Comunal las necesidades comunicativas.

### F.2.2 Fase 2: Implementación

Configurar el proyecto y realizar las primeras ediciones.

### F.2.3 Fase 3: Formación

Capacitar a dos o tres personas que lideren la gestión del sitio.

### F.2.4 Fase 4: Monitoreo

Revisar mensualmente el sitio y las actualizaciones.

## F.3 Criterios de calidad para los contenidos

Los contenidos del sitio deben ser:

- Claros.
- Relevantes.
- Actualizados.
- Fáciles de leer.
- Respetuosos.

### F.3.1 Lista de verificación antes de publicar

- ¿El texto es claro?
- ¿La información es verdadera?
- ¿La fecha está actualizada?
- ¿El enlace funciona?
- ¿Las imágenes están en la carpeta `imagenes/`?
- ¿El contenido es respetuoso con la comunidad?

## F.4 Gestión de la memoria comunitaria digital

El sitio web debe ser un espacio de memoria comunitaria. Cada noticia, evento y proyecto documenta la historia de Villa Rosario.

### F.4.1 Registro de gestión comunitaria

Usa la sección de gestiones para registrar cada acción del Consejo Comunal.

### F.4.2 Registro de proyectos

Documenta los avances y resultados de cada proyecto en `proyectos.html`.

### F.4.3 Registro de eventos

Mantén el calendario de eventos al día para fortalecer la participación.

## F.5 Estrategia de difusión digital

La publicación del sitio debe ser acompañada de difusión entre vecinos.

### F.5.1 Compartir el enlace

Envía el enlace a grupos de WhatsApp y Telegram del sector.

### F.5.2 Anunciar en asambleas

Presenta las novedades del sitio en reuniones presenciales.

### F.5.3 Usar la página como referencia oficial

Convierte el sitio en el canal oficial del Consejo Comunal para anuncios y horarios.

## F.6 Responsabilidad ética y comunitaria

El contenido del sitio representa a toda la comunidad. Por eso recomendamos:

- Verificar la información con el Consejo Comunal.
- No publicar rumores.
- Respetar la vida privada de las personas.
- Usar lenguaje respetuoso y constructivo.

## F.7 Documentación del proceso de transferencia

### F.7.1 Entrega formal

Este manual es la evidencia documental de la transferencia tecnológica. Conserva una copia impresa y otra digital.

### F.7.2 Registro de capacitaciones

Anota en un cuaderno o en un archivo quiénes aprendieron a editar el sitio y cuándo.

### F.7.3 Indicador de éxito

El éxito de la transferencia se mide cuando el Consejo Comunal puede actualizar el sitio sin ayuda externa.

## F.8 Cierre del manual

De parte del equipo de la UPTOS, agradecemos la confianza del Consejo Comunal de Villa Rosario. Este manual es un puente entre el conocimiento académico y la práctica comunitaria.

Nuestro objetivo es que puedan usarlo cada vez que lo necesiten, compartirlo y mejorarlo con la misma solidaridad con la que se construye el tejido social de Villa Rosario.

**FIN DEL MANUAL MAESTRO VILLA ROSARIO**

**Versión 1.0 Maestro**

**Junio 2026**
# ANEXO G: CONTROL DE CALIDAD Y VALIDACIÓN FINAL

## G.1 Por qué es importante validar cada cambio

En la transferencia tecnológica, el control de calidad es tan importante como la edición misma. Cada cambio en la página web debe pasar por una verificación simple antes de publicarlo. Eso evita errores visibles, información incorrecta y decisiones apresuradas.

Nosotros en la UPTOS enseñamos que la edición comunitaria debe estar acompañada por un proceso de revisión. Ese proceso no es complicado, pero debe ser constante.

## G.2 Lista de verificación antes de hacer commit

Antes de guardar y enviar un cambio, revisa lo siguiente:

1. ¿Está el archivo correcto? (Por ejemplo, `index.html` o `servicios.html`)
2. ¿Es el texto adecuado para la comunidad?
3. ¿Falta alguna etiqueta de cierre `</p>`, `</div>`, `</section>`?
4. ¿El enlace dentro del botón `VER DETALLES` tiene un número único?
5. ¿La imagen apunta a la carpeta `imagenes/` y tiene el nombre exacto?
6. ¿La fecha usa el formato `24 ABR 2026`?
7. ¿El estado del servicio usa `estado-bueno`, `estado-regular`, o `estado-malo`?
8. ¿No se cambió ninguna clase CSS sensible?
9. ¿El texto es respetuoso y claro?
10. ¿El mensaje de commit describe el cambio?

Si respondes sí a todos los puntos, puedes avanzar.

## G.3 Validación visual en el navegador

Abrir el archivo en el navegador es la mejor manera de ver el resultado.

### G.3.1 Cómo hacerlo correctamente

- Abre el archivo desde el explorador de archivos.
- Usa tu navegador preferido.
- Recarga con `F5` después de cada cambio.
- Si usas Google Chrome o Firefox, puedes abrir la consola con `Ctrl + Shift + I` para ver errores.

### G.3.2 Qué verificar en el navegador

- Los textos aparecen completos.
- Las imágenes se ven correctamente.
- No hay cajas desordenadas.
- Los botones se muestran bien.
- El carrusel funciona.
- Los iconos se ven con claridad.

## G.4 Control de accesibilidad

Un sitio comunitario debe ser accesible para todas las personas. Por eso, revisa que:

- Las imágenes tengan `alt` con descripción.
- Los títulos sean claros.
- Los párrafos no sean demasiado largos.
- El contraste de colores permita leer bien el texto.

No necesitas ser un experto, pero sí debes cuidar que la página sea comprensible.

## G.5 Ejemplo de validación paso a paso

1. Edita `servicios.html` y cambia el estado de agua.
2. Guarda con `Ctrl + S`.
3. Abre `servicios.html` en el navegador.
4. Verifica el color verde/amarillo/rojo del servicio.
5. Si el texto aparece en blanco o el diseño se rompe, presiona `Ctrl + Z`.
6. Regresa al archivo y revisa si quedó alguna etiqueta abierta.
7. Repite el proceso hasta que esté bien.
8. Haz commit en GitHub Desktop.
9. Envía el push.
10. Espera 60-120 segundos y recarga el sitio en vivo.

## G.6 Comentarios UPTOS como herramientas de revisión

Los comentarios HTML son un recurso útil para el mantenimiento.

### G.6.1 Cómo escribir un comentario útil

```html
<!-- Comentario UPTOS: Esta sección muestra el estado del servicio de agua -->
```

### G.6.2 Cómo usar comentarios para recordar cambios

Puedes dejar un comentario temporal en el HTML, pero recuerda quitarlo si no aporta valor.

```html
<!-- Comentario UPTOS: Reemplazar texto después de la reunión del 28 de abril -->
```

## G.7 Cómo hacer una revisión conjunta con otros voceros

Revisar el sitio en equipo fortalece la transferencia.

1. Abre el archivo con otro vocero.
2. Lean juntos el texto.
3. Pregunten: ¿esto es claro para todos?
4. Componenten cambios por consenso.
5. Un vocero hace el commit y otro revisa.

Esto ayuda a mejorar la calidad y evita malentendidos.

# ANEXO H: EJEMPLOS REALES Y ESCENARIOS COMUNITARIOS

## H.1 Escenario 1: Corte de agua en horario crítico

Imagina que un corte de agua se anuncia a las 6:00 de la mañana. El Consejo Comunal decide informar con urgencia.

### Pasos a seguir:

1. Abre `index.html`.
2. Localiza el bloque de alertas.
3. Elige la plantilla de alerta urgente roja.
4. Cambia el título a "Corte de agua en el Sector Norte".
5. Describe la hora y la causa.
6. Guarda y verifica.
7. Haz commit con el mensaje "Alerta urgente de agua".
8. Envía push.
9. Espera 60-120 segundos.
10. Recarga el sitio vivo.

### Texto recomendado:

```html
<div class="alerta-item alerta-urgente">
    <div class="alerta-icono">
        <i class="fas fa-exclamation-triangle"></i>
    </div>
    <div class="alerta-texto">
        <h3>Corte de agua en el Sector Norte</h3>
        <p>El suministro se suspenderá desde las 8:00 a.m. hasta las 2:00 p.m. por reparación de tubería.</p>
        <span>24 ABR 2026</span>
    </div>
</div>
```

## H.2 Escenario 2: Anunciar una feria de emprendedores

Supongamos que se organiza una feria para fortalecer los negocios.

### Pasos a seguir:

1. Abre `eventos.html`.
2. Copia la plantilla de evento.
3. Cambia el título, fecha, hora y lugar.
4. Añade una descripción con invitación.
5. Guarda y revisa.
6. Haz commit con "Agregar feria de emprendedores".
7. Push.
8. Comparte el enlace en el grupo comunitario.

### Texto recomendado:

```html
<div class="evento-card">
    <h3>Feria de Emprendedores del Sector Sabilar</h3>
    <p><strong>Fecha:</strong> 8 MAY 2026</p>
    <p><strong>Hora:</strong> 10:00 a.m.</p>
    <p><strong>Lugar:</strong> Plaza central</p>
    <p>Apoya a los negocios locales con productos agrícolas, artesanías y comidas típicas.</p>
</div>
```

## H.3 Escenario 3: Lanzar una campaña de limpieza

Para una campaña de limpieza, la comunicación debe ser clara y participativa.

### Pasos a seguir:

1. Abre `index.html` y `eventos.html`.
2. En la portada, agrega una alerta de evento verde.
3. En `eventos.html`, agrega un evento con datos completos.
4. Guarda ambos archivos.
5. Verifica en el navegador.
6. Commits separados si lo deseas.
7. Push.

### Texto recomendado para la alerta:

```html
<div class="alerta-item alerta-evento">
    <div class="alerta-icono">
        <i class="fas fa-calendar-check"></i>
    </div>
    <div class="alerta-texto">
        <h3>Campaña de limpieza en el Sector Sabilar</h3>
        <p>Ven a colaborar con la comunidad este sábado. Reúnete en la plaza central a las 7:00 a.m.</p>
        <span>1 MAY 2026</span>
    </div>
</div>
```

### Texto recomendado para el evento:

```html
<div class="evento-card">
    <h3>Campaña de limpieza comunitaria</h3>
    <p><strong>Fecha:</strong> 1 MAY 2026</p>
    <p><strong>Hora:</strong> 7:00 a.m.</p>
    <p><strong>Lugar:</strong> Plaza central</p>
    <p>Recogida de basura, clasificación de residuos y mejora de espacios públicos del sector.</p>
</div>
```

## H.4 Escenario 4: Documentar una reparación de infraestructura

Cuando se hace una obra, el sitio debe registrar el progreso para la comunidad.

### Pasos a seguir:

1. Abre `proyectos.html`.
2. Copia la plantilla de proyecto.
3. Cambia el título, estado, descripción, responsable e inversión.
4. Añade el avance en porcentaje.
5. Describe los siguientes pasos.
6. Guarda, commit y push.

### Texto recomendado:

```html
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Reparación de la red de drenaje</h3>
        <span class="proyecto-estado">En Ejecución</span>
    </div>
    <div class="proyecto-body">
        <p>Se reemplazan tuberías dañadas para evitar inundaciones en la estación lluviosa.</p>
        <p><strong>Responsable:</strong> Comité de Infraestructura</p>
        <p><strong>Inversión:</strong> Bs. 2.500.000</p>
        <p><strong>Avance:</strong> 50%</p>
        <p><strong>Siguientes pasos:</strong> Pruebas de funcionamiento y ajuste de rebosaderos.</p>
    </div>
</div>
```

## H.5 Escenario 5: Actualizar la sección de Historia con un testimonio

La historia comunitaria también crece cuando se registran voces locales.

### Pasos a seguir:

1. Abre `historia.html`.
2. Copia el formato de sección histórica.
3. Agrega un testimonio o un capítulo nuevo.
4. Guarda y revisa.

### Texto recomendado:

```html
<section class="historia-seccion">
    <h2>Testimonio del barrio</h2>
    <p>"Sentimos orgullo de ver cómo nuestro sector se organiza para resolver problemas juntos. El Consejo Comunal nos representa y nos escucha."</p>
    <p><strong>- Habitante de Villa Rosario</strong></p>
</section>
```

## H.6 Escenario 6: Publicar un mensaje de reconocimiento social

Si la comunidad hace una entrega de ayudas o una obra concluye, el sitio debe reflejar ese reconocimiento.

### Pasos a seguir:

1. Abre `articulos.html`.
2. Elige una noticia de agradecimiento.
3. Añade el titular y el cuerpo explicativo.
4. Cambia la fecha.
5. Guarda y publica.

### Texto recomendado:

```html
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-heart"></i> AGRADECIMIENTO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 2 MAY 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Gracias a las familias que participaron en la jornada</h3>
        <p>El Consejo Comunal agradece a todos los vecinos que colaboraron en la limpieza del sector y en la restauración del parque.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=15" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

## H.7 Escenario 7: Comunicar un cambio en los voceros del Consejo Comunal

Cuando el Consejo Comunal rotan las responsabilidades, la web debe reflejarlo.

### Pasos a seguir:

1. Abre `consejo-comunal.html`.
2. Localiza el bloque de voceros.
3. Actualiza los nombres y teléfonos.
4. Guarda y revisa.

### Texto recomendado:

```html
<div class="vocero-card">
    <h3>Vocero Principal</h3>
    <p>Nombre: Ana Jiménez</p>
    <p>Teléfono: 0414-9876543</p>
</div>
```

## H.8 Escenario 8: Informar de un cambio en el servicio de transporte comunitario

Si se mejora la ruta de transporte, la comunidad debe enterarse.

### Pasos a seguir:

1. Agrega una noticia en `articulos.html`.
2. Añade un evento en `eventos.html` si hay presentación pública.
3. Cambia el estado en `servicios.html` si corresponde.
4. Guarda y publica.

## H.9 Escenario 9: Definir un plan de acción para el mes

El sitio puede ayudar a planificar actividades mensuales.

### Pasos a seguir:

1. Actualiza `eventos.html` con las actividades del mes.
2. Agrega una noticia en `articulos.html` con un resumen del plan.
3. Usa `index.html` para destacar los eventos más importantes.
4. Guarda y revisa.

## H.10 Escenario 10: Registrar el avance de un comité nuevo

Cuando se crea un comité nuevo, el sitio debe presentarlo.

### Pasos a seguir:

1. Abre `consejo-comunal.html`.
2. Copia una tarjeta de comité.
3. Cambia el nombre, icono y descripción.
4. Guarda y publica.

### Texto recomendado:

```html
<div class="comite-card">
    <i class="fas fa-book"></i>
    <h3>Comité de Educación</h3>
    <p>Promueve la formación de niñas, niños y jóvenes con actividades educativas y talleres.</p>
</div>
```

# ANEXO I: BIBLIOGRAFÍA COMUNITARIA Y REFERENCIAS UPTOS

## I.1 Referencias conceptuales usadas en el manual

Este manual se basa en los principios de la investigación-acción participativa, diseño comunitario y procesos de transferencia tecnológica. Algunos referentes importantes son:

- Paulo Freire, por su énfasis en la educación como práctica de la libertad.
- Participación comunitaria, como método para fortalecer la gobernanza local.
- Transferencia tecnológica, como proceso de entrega de conocimiento y herramientas.

## I.2 Fuentes de buenas prácticas

Las partes técnicas del manual se inspiraron en:

- Documentación de HTML5 y buenas prácticas de accesibilidad.
- Uso de GitHub como plataforma de versiones.
- Prácticas de mantenimiento de sitios estáticos.
- Metodologías de aprendizaje colectivo y capacitación social.

## I.3 Cómo citar este manual

Si deseas referenciar este documento en una reunión o en un informe, puedes escribir:

"Manual Maestro Villa Rosario, versión 1.0, Equipo de Investigadores UPTOS, junio 2026."

## I.4 Actualización futura

Este manual es la primera versión. Recomendamos revisarlo y actualizarlo cada seis meses, o cuando haya un cambio importante en la organización del sitio.

## I.5 Firmeza institucional

La UPTOS respalda la entrega de este manual como parte de su compromiso con la comunidad de Villa Rosario. El documento debe ser conservado como parte de los archivos del Consejo Comunal.

# ANEXO J: GLOSARIO EXTENDIDO Y TERMINOLOGÍA

## J.1 Glosario de términos técnicos

- **Archivo HTML:** Documento que contiene el contenido y la estructura de una página web.
- **CSS:** Estilos que definen cómo se ve la página.
- **JavaScript:** Código que controla acciones dinámicas en la página.
- **Repositorios:** Carpetas en la nube donde se guarda el proyecto.
- **Git:** Sistema de versiones que guarda cambios con historial.
- **Commit:** Registro de un cambio específico.
- **Push:** Acción de enviar cambios a GitHub.
- **Branch / Rama:** Línea de trabajo en Git.
- **Merge:** Unir cambios de diferentes ramas.

## J.2 Términos comunitarios adaptados al sitio

- **Consejo Comunal:** Organización local que toma decisiones colectivas.
- **Vocero / Vocera:** Representante autorizado para comunicar decisiones.
- **Comité:** Grupo de trabajo especializado en un área clave.
- **Asamblea:** Reunión amplia de vecinos para discutir temas comunitarios.
- **Transferencia Tecnológica:** Proceso de entregar conocimiento técnico a la comunidad.
- **Plataforma web:** Sitio digital que comunica información oficial.

## J.3 Recomendaciones para el uso del lenguaje

- Usa siempre términos sencillos y directos.
- Evita palabras muy técnicas sin explicación.
- Prefiere frases cortas y concretas.
- Añade ejemplos cuando expliques acciones.

# ANEXO K: LISTA AMPLIADA DE ÍCONOS Y SU USO

## K.1 Iconos de Font Awesome más frecuentes

| Icono | Uso recomendado | Ejemplo |
|-------|-----------------|---------|
| `fas fa-tint` | Agua potable, servicio hídrico | `Agua Potable` |
| `fas fa-bolt` | Electricidad, energía | `Electricidad` |
| `fas fa-users` | Asamblea, comunidad | `Participación` |
| `fas fa-heartbeat` | Salud | `Salud` |
| `fas fa-road` | Infraestructura | `Caminos` |
| `fas fa-store` | Comercio | `Emprendedores` |
| `fas fa-bullhorn` | Anuncios | `Comunicados` |
| `fas fa-calendar-check` | Eventos | `Actividades` |
| `fas fa-exclamation-triangle` | Alerta urgente | `Emergencias` |
| `fas fa-info-circle` | Información | `Avisos` |
| `fas fa-arrow-right` | Botones | `Ver detalles` |
| `fas fa-shield-alt` | Seguridad | `Seguridad` |
| `fas fa-seedling` | Medio ambiente | `Ambiental` |
| `fas fa-wifi` | Internet | `Conectividad` |
| `fas fa-map-marker-alt` | Ubicación | `Lugar` |
| `fas fa-trash-alt` | Aseo | `Limpieza` |
| `fas fa-handshake` | Trabajo conjunto | `Acuerdos` |
| `fas fa-book` | Educación | `Capacitación` |

## K.2 Cómo cambiar un icono sin errores

1. Localiza la etiqueta `<i class="fas fa-...."></i>`.
2. Cambia solo el nombre después de `fa-`.
3. No borres el prefijo `fas`.

Ejemplo:

```html
<i class="fas fa-calendar-check"></i>
```

## K.3 Iconos para páginas especiales

- `index.html` → iconos de bienvenida y alerta.
- `consejo-comunal.html` → iconos de comité y organización.
- `articulos.html` → iconos de noticias y comunicación.
- `servicios.html` → iconos de agua, electricidad e internet.
- `proyectos.html` → iconos de construcción y avance.
- `emprendedores.html` → iconos de comercio y negocios.
- `historia.html` → iconos de memoria y trayectorias.
- `eventos.html` → iconos de calendario y convocatoria.

# ANEXO L: PROCEDIMIENTO DE SOPORTE TÉCNICO

## L.1 Cómo pedir apoyo técnico a la UPTOS

Si la comunidad necesita apoyo, sigue estos pasos:

1. Describe el problema específico.
2. Indica el archivo afectado.
3. Adjunta una captura de pantalla si es posible.
4. Envía la solicitud al correo institucional de la UPTOS o al vocero técnico.

La UPTOS recomienda que las solicitudes incluyan:

- Nombre completo del vocero.
- Fecha del incidente.
- Breve descripción del error.
- Pasos que ya intentaste.

## L.2 Registro de problemas y soluciones

Lleva un cuaderno comunitario o un archivo digital donde registres:

- Fecha.
- Problema.
- Solución aplicada.
- Responsable.

Esto construye un historial útil para futuras generaciones.

## L.3 Comunicación interna del consejo

Si un cambio importante se va a publicar, el Consejo Comunal debe acordarlo en asamblea o reunión de voceros. La comunicación interna es tan importante como el cambio en la página.

## L.4 Cómo documentar un cambio importante

Cuando el cambio es importante, agrega un comentario en el HTML:

```html
<!-- Comentario UPTOS: Actualización de la campaña de vacunación aprobada en asamblea del 23 de abril -->
```

## L.5 Mantenimiento periódico

### L.5.1 Frecuencia recomendada

- Revisión general: cada mes.
- Actualización de eventos: semanal.
- Actualización de noticias: cada vez que ocurre algo relevante.
- Revisión de servicios: cada quincena.

### L.5.2 Equipo responsable

Es ideal que haya al menos dos personas que sepan usar este manual y manejar GitHub Desktop.

## L.6 Proceso para traslados de voceros

Cuando un vocero o vocera deja su cargo,

1. Actualiza la página de `consejo-comunal.html`.
2. Registra la fecha de cambio.
3. Comunica el nuevo responsable en `articulos.html` si es necesario.
4. Guarda el registro en GitHub con un commit estándar.

# ANEXO M: ESTRUCTURA RECOMENDADA PARA UNA ASAMBLEA VIRTUAL

## M.1 Preparación de la agenda

1. Revisión de noticias publicadas.
2. Estado de servicios.
3. Avance de proyectos.
4. Eventos próximos.
5. Solicitudes de la comunidad.
6. Plan de comunicación digital.

## M.2 Uso del manual durante la asamblea

- Cada vocero puede abrir este manual.
- Consultar la sección correspondiente.
- Proponer cambios basados en la información.
- Decidir quién hace la edición y la publicación.

## M.3 Registro de acuerdos

Al final de la asamblea, deja constancia de los acuerdos en `articulos.html` como noticia o en la página de historia.

### Texto recomendado:

```html
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-users"></i> ASAMBLEA</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 25 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Acuerdos de la asamblea comunitaria</h3>
        <p>Se acordaron acciones para mejorar la limpieza urbana y fortalecer la comunicación del Consejo Comunal.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=20" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

# ANEXO N: GLOSARIO AMPLIADO DE PALABRAS COMUNES EN EL SITIO

## N.1 Definiciones prácticas

- **Cargo técnico:** Persona responsable del manejo del sitio web.
- **Consejo Comunal:** Asamblea local que organiza el barrio.
- **Estatus:** Estado de un servicio o proyecto.
- **Gestión:** Acción realizada por el Consejo Comunal.
- **Plantilla:** Bloque de código reutilizable.
- **Repositorio:** Lugar en GitHub donde vive el proyecto.
- **Tutorial comunitario:** Taller para enseñar a vecinos.

# ANEXO O: RUTA DE APRENDIZAJE PARA VOCEROS NUEVOS

## O.1 Primera semana

- Leer PARTE 1 y PARTE 2.
- Identificar los archivos principales.
- Hacer una práctica de edición en `index.html`.

## O.2 Segunda semana

- Trabajar con `articulos.html` y `servicios.html`.
- Añadir una noticia y cambiar un estado de servicio.
- Publicar el cambio en GitHub Desktop.

## O.3 Tercera semana

- Editar `proyectos.html` y `eventos.html`.
- Aprender a usar plantillas.
- Revisar el historial de commits.

## O.4 Cuarta semana

- Actualizar `consejo-comunal.html`.
- Documentar un proceso de gestión.
- Compartir el manual con otro vocero.

## O.5 Continuidad educativa

- Revisar este manual cada cuatro semanas.
- Actualizarlo según las necesidades.
- Usarlo como base para nuevos voceros.

---

**FIN DEL ANEXO ADICIONAL**

**MANUAL MAESTRO VILLA ROSARIO**

**Versión 1.0 Maestro**

**Junio 2026**
# ANEXO P: PLANTILLAS EXTRA, EJEMPLOS Y CASOS DE EDICIÓN AVANZADA

## P.1 Plantilla de noticia con llamada a donación

En ocasiones, el Consejo Comunal puede necesitar apoyar una causa con donaciones. Esta plantilla ayuda a comunicar con claridad.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-hand-holding-heart"></i> DONACIÓN</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 28 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Campaña de apoyo a familias afectadas por inundaciones</h3>
        <p>El Consejo Comunal organiza una colecta de alimentos y ropa para las familias más afectadas. Colabora con tu aporte.</p>
        <ul>
            <li>Alimentos no perecederos</li>
            <li>Ropa en buen estado</li>
            <li>Artículos de higiene personal</li>
        </ul>
        <p><strong>Lugar de recepción:</strong> Casa comunal</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=21" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.2 Plantilla de noticia con lista de tareas

Cuando es necesario presentar un plan de acción, esta plantilla te ayuda.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="proyecto">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-tasks"></i> PLAN</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 29 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Plan de trabajo para la recolección de basura</h3>
        <p>El objetivo es mejorar la recolección y el reciclaje en el sector Sabilar.</p>
        <ul>
            <li>1. Coordinar con la empresa de aseo.</li>
            <li>2. Establecer puntos de acopio.</li>
            <li>3. Informar a las familias sobre separación de residuos.</li>
        </ul>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=22" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.3 Plantilla de evento con apoyo institucional

Si un organismo externo apoya una actividad, este formato es útil.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="evento-card">
    <h3>Jornada de salud con apoyo de la alcaldía</h3>
    <p><strong>Fecha:</strong> 15 MAY 2026</p>
    <p><strong>Hora:</strong> 8:00 a.m.</p>
    <p><strong>Lugar:</strong> Salón comunal</p>
    <p>Atenciones médicas y entrega de información sobre prevención. Participación conjunta con el gobierno municipal.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.4 Plantilla de proyecto con documento de avance

Para proyectos con informes periódicos, este diseño es claro.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Construcción del nuevo espacio juvenil</h3>
        <span class="proyecto-estado">En Ejecución</span>
    </div>
    <div class="proyecto-body">
        <p>Se avanza en la obra con la construcción de paredes, instalaciones eléctricas y áreas recreativas.</p>
        <p><strong>Responsable:</strong> Comité de Juventud</p>
        <p><strong>Inversión:</strong> Bs. 4.200.000</p>
        <p><strong>Avance:</strong> 45%</p>
        <p><strong>Siguientes pasos:</strong> Instalación de puertas y ventanas, pintura y mobiliario.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.5 Plantilla de comité con roles claros

Los comités también deben mostrar sus funciones y roles.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="comite-card">
    <i class="fas fa-hands-helping"></i>
    <h3>Comité de Inclusión Social</h3>
    <p>Trabaja para asegurar que todas las personas del sector reciban información y apoyo.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.6 Plantilla de contacto con formularios imaginarios

Aunque el sitio es estático, puedes mostrar un modelo de formulario para uso institucional.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<section class="contacto">
    <h2>Contacto del Consejo Comunal</h2>
    <p><strong>Dirección:</strong> Sector Sabilar, Parroquia Altagracia</p>
    <p><strong>Teléfono:</strong> 0414-1234567</p>
    <p><strong>Correo:</strong> consejo@villarosario.com</p>
    <p>Envíanos un mensaje con tu consulta y el Consejo Comunal se encargará de responder.</p>
</section>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.7 Plantilla de noticia con agradecimiento especial

Las notas de agradecimiento ayudan a fortalecer la confianza comunitaria.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-heart"></i> AGRADECIMIENTO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 29 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Gracias a las familias por su participación en la jornada</h3>
        <p>El Consejo Comunal expresa su reconocimiento a los vecinos y vecinas que hicieron posible la limpieza del barrio.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=23" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.8 Plantilla de evento con preparación comunitaria

Este formato es útil para jornadas de trabajo colaborativo.

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="evento-card">
    <h3>Jornada de embellecimiento del parque</h3>
    <p><strong>Fecha:</strong> 22 MAY 2026</p>
    <p><strong>Hora:</strong> 9:00 a.m.</p>
    <p><strong>Lugar:</strong> Parque central</p>
    <p>Organizamos actividades de pintura, jardinería y reparación de espacios públicos.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.9 Plantilla de servicio con recomendación comunitaria

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="servicio-card" id="servicio-sanitario">
    <div class="servicio-header">
        <i class="fas fa-shower"></i>
        <h3>Servicio sanitario</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-regular">Regular</span>
        <p>Inspección en curso para mejorar el servicio y garantizar un suministro asequible.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.10 Plantilla de emprendedor con énfasis en sostenibilidad

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="emprendedor-card">
    <div class="emprendedor-imagen">
        <img src="imagenes/emprendedor6.jpg" alt="Emprendedor sostenible">
    </div>
    <div class="emprendedor-texto">
        <h3>Proyecto Verde Sabilar</h3>
        <p><strong>Propietaria:</strong> Laura Pérez</p>
        <p>Productos ecológicos y talleres de reciclaje para la comunidad.</p>
        <p><strong>Teléfono:</strong> 0414-4445566</p>
        <p><strong>Ubicación:</strong> Calle principal, cerca de la escuela.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.11 Plantilla de noticia con consejo ciudadano

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-lightbulb"></i> CONSEJO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 30 ABR 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Consejos para el uso responsable del agua</h3>
        <p>El comité de agua recomienda prácticas simples para ahorrar y cuidar el recurso.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=24" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.12 Plantilla de proyecto con seguimiento mensual

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Seguimiento mensual del plan de bacheo</h3>
        <span class="proyecto-estado">En Ejecución</span>
    </div>
    <div class="proyecto-body">
        <p>La obra avanza con reparaciones de calles y señalización temporal.</p>
        <p><strong>Responsable:</strong> Comité de Vías</p>
        <p><strong>Inversión:</strong> Bs. 1.000.000</p>
        <p><strong>Avance:</strong> 70%</p>
        <p><strong>Siguientes pasos:</strong> Terminación de tramos y limpieza posterior.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.13 Plantilla de evento con invitación a capacitación

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="evento-card">
    <h3>Taller de comunicación comunitaria</h3>
    <p><strong>Fecha:</strong> 20 MAY 2026</p>
    <p><strong>Hora:</strong> 10:00 a.m.</p>
    <p><strong>Lugar:</strong> Biblioteca del sector</p>
    <p>Actividad para fortalecer la comunicación entre el Consejo Comunal y las familias.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.14 Plantilla de noticia con reporte de incidencia

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="servicios">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-exclamation-circle"></i> INCIDENTE</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 1 MAY 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Reporte de fallas en el alumbrado público</h3>
        <p>Se detectaron postes sin luz en el sector norte. El Consejo Comunal ya solicitó la reparación.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=25" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.15 Plantilla de evento con apoyo juvenil

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="evento-card">
    <h3>Encuentro juvenil de liderazgo</h3>
    <p><strong>Fecha:</strong> 25 MAY 2026</p>
    <p><strong>Hora:</strong> 11:00 a.m.</p>
    <p><strong>Lugar:</strong> Centro juvenil</p>
    <p>Actividad para formar a jóvenes líderes que impulsen proyectos comunitarios.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.16 Plantilla de contacto con mensaje institucional corto

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<section class="contacto">
    <h2>Contacto oficial</h2>
    <p>El Consejo Comunal está atento a tus inquietudes y solicitudes. Escribe o llámanos.</p>
    <p><strong>Teléfono:</strong> 0414-1234567</p>
    <p><strong>Correo:</strong> consejo@villarosario.com</p>
</section>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.17 Plantilla de noticia de invitación a capacitación técnica

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="evento">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-laptop-code"></i> CAPACITACIÓN</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 2 MAY 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Capacitación en uso de la página web comunitaria</h3>
        <p>El equipo UPTOS invita a los voceros y voceras a un taller práctico para aprender a editar el sitio.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=26" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.18 Plantilla de proyecto con informe social

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="proyecto-card">
    <div class="proyecto-header">
        <h3>Programa de apoyo a estudiantes</h3>
        <span class="proyecto-estado">En Curso</span>
    </div>
    <div class="proyecto-body">
        <p>Se brinda acompañamiento educativo y materiales escolares a niños y niñas del sector.</p>
        <p><strong>Responsable:</strong> Comité de Educación</p>
        <p><strong>Inversión:</strong> Bs. 1.000.000</p>
        <p><strong>Avance:</strong> 30%</p>
        <p><strong>Siguientes pasos:</strong> Distribución de kits escolares y tutorías semanales.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.19 Plantilla de servicio con enfoque en comunidad

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="servicio-card" id="servicio-salud">
    <div class="servicio-header">
        <i class="fas fa-heartbeat"></i>
        <h3>Salud</h3>
    </div>
    <div class="servicio-body">
        <span class="estado-badge estado-bueno">Bueno</span>
        <p>El servicio de salud comunitaria se ofrece con regularidad en el consultorio local.</p>
    </div>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.20 Plantilla de evento con llamado a vecinos mayores

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<div class="evento-card">
    <h3>Encuentro con adultos mayores</h3>
    <p><strong>Fecha:</strong> 28 MAY 2026</p>
    <p><strong>Hora:</strong> 10:00 a.m.</p>
    <p><strong>Lugar:</strong> Casa comunal</p>
    <p>Actividad dedicada a la participación y el cuidado de nuestros adultos mayores en Villa Rosario.</p>
</div>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

## P.21 Plantilla de noticia con reporte de avance de agenda

```html
<!-- Comentario UPTOS: Copie desde aquí -->
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-calendar-alt"></i> AGENDA</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 3 MAY 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Reporte de la agenda comunitaria del mes</h3>
        <p>El Consejo Comunal avanza en la planificación de actividades de limpieza, capacitación y apoyo social.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=27" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
<!-- Comentario UPTOS: Copie hasta aquí -->
```

# ANEXO Q: DESESCALAR CAMBIOS, CONSERVACIÓN Y TRANSFERENCIA

## Q.1 Cómo planificar un cambio mayor en el sitio

Si el Consejo Comunal decide hacer una transformación mayor del sitio, como modificar el diseño o incorporar una nueva sección importante, el proceso debe ser:

1. Definido en asamblea.
2. Documentado en este manual.
3. Aprobado por los voceros responsables.
4. Realizado con apoyo técnico.
5. Probado en una copia antes de publicarlo.

## Q.2 Conservación de versiones históricas

Cada commit en GitHub es una versión de la página. Nosotros recomendamos que:

- No se eliminen commits antiguos.
- Se use la historia de Git como memoria institucional.
- Se pueda consultar qué se hizo el mes pasado o el año pasado.

## Q.3 Uso del historial para capacitación

El historial de GitHub Desktop es una herramienta pedagógica. Muestra cómo se ha avanzado y permite aprender del trabajo anterior.

## Q.4 Cómo documentar cambios importantes en el manual

Cuando se hace un cambio fuerte, agrega un comentario en este manual con la fecha y la razón.

Ejemplo:

```text
[29 ABR 2026] Se actualizó la metodología de publicación porque el Consejo Comunal decidió usar GitHub Desktop en lugar de otra herramienta.
```

## Q.5 Transferencia tecnológica como proceso continuo

La transferencia no termina con la entrega del manual. Es un proceso continuo de formación, práctica y revisión.

### Q.5.1 Lo que implica este proceso

- Enseñar a más personas.
- Revisar el manual cuando se necesite.
- Compartir los aprendizajes.

### Q.5.2 Cómo medir el avance

Un buen indicador es que más de dos personas del Consejo Comunal puedan editar el sitio sin ayuda externa.

## Q.6 Conservación de copias de seguridad

Recomendamos tener al menos dos copias de seguridad:

- En una memoria USB.
- En un servicio de nube como Google Drive.

Asegúrate de actualizar estas copias regularmente.

## Q.7 Organización de la documentación

Mantén una carpeta con los archivos más importantes:

- `MANUAL_MAESTRO_VILLA_ROSARIO.md`
- `README.md`
- Copias de seguridad del sitio.
- Documentos de reuniones.

## Q.8 Cómo usar este manual en reuniones de voceros

Lleva este manual a cada reunión. Úsalo como referencia para decidir qué publicar y cómo hacerlo.

## Q.9 Ejemplo de acta de reunión con cambios web

Puedes registrar en el acta:

- Tema: cambio en la alerta de agua.
- Responsable: vocero técnico.
- Fecha de publicación: 29 ABR 2026.
- Observaciones: verificar en vivo después de 120 segundos.

## Q.10 Plan de revisión anual

Cada año, el Consejo Comunal debe revisar este manual y actualizarlo. Esto garantiza que el sitio siga siendo útil y pertinente.

# ANEXO R: LISTA COMPLETA DE ERRORES TÉCNICOS Y CORRECCIONES

## R.1 Error: Página en blanco luego de editar

### Causa

- Falta una etiqueta de cierre.
- Hay un error de sintaxis.

### Solución

- Revisa el HTML completo.
- Busca etiquetas sin cerrar.
- Usa `Ctrl + Z` si aplicaste un cambio reciente.

## R.2 Error: Imágenes que no aparecen

### Causa

- Nombre de archivo equivocado.
- Extensión incorrecta.
- Archivo no existe en `imagenes/`.

### Solución

- Verifica el nombre exacto.
- Usa minúsculas.
- Revisa la carpeta `imagenes/`.

## R.3 Error: Botones que no llevan a la noticia correcta

### Causa

- Número `id` duplicado.

### Solución

- Asigna un `id` único a cada noticia.

## R.4 Error: Texto cortado en el navegador

### Causa

- Etiqueta `</p>` faltante.

### Solución

- Añade el cierre correspondiente.

## R.5 Error: El contenido sale fuera del contenedor

### Causa

- Eliminaste una etiqueta `</div>`.

### Solución

- Revisa la estructura de bloques.

## R.6 Error: El carrusel no avanza

### Causa

- JavaScript no cargado.

### Solución

- No edites `js/main.js`.
- Asegúrate de que la página tenga el enlace correcto a `js/main.js`.

## R.7 Error: Estilos rotos en móviles

### Causa

- Cambiaste el CSS sin permiso.

### Solución

- Revertir los cambios o pedir apoyo técnico.

## R.8 Error: Página no actualiza después de push

### Causa

- GitHub Pages tarda en procesar el cambio.

### Solución

- Espera 60-120 segundos y recarga.

## R.9 Error: No aparece el ícono de Font Awesome

### Causa

- La clase del icono está mal escrita.

### Solución

- Verifica que la etiqueta sea `class="fas fa-icono"`.

## R.10 Error: Comentarios visibles en la página

### Causa

- No usaste la sintaxis correcta para comentarios.

### Solución

- Usa `<!-- texto -->`.

## R.11 Error: Texto con símbolos extraños

### Causa

- Copiaste texto desde un procesador con formato.

### Solución

- Reescribe el texto directamente en VS Code.

## R.12 Error: El sitio se ve diferente en otro navegador

### Causa

- Diferencias de compatibilidad.

### Solución

- Prueba en los navegadores más comunes: Chrome, Firefox, Edge.

## R.13 Error: La página tarda en cargar

### Causa

- Imagen muy pesada.

### Solución

- Usa imágenes con resolución razonable.
- No subas fotos demasiado grandes.

## R.14 Error: URL equivocada en el menú

### Causa

- Enlace mal escrito.

### Solución

- Corrige la ruta en `href=""`.

## R.15 Error: No se ven los nombres del vocero

### Causa

- Texto eliminado por accidente.

### Solución

- Revisa la versión anterior en GitHub Desktop.

# ANEXO S: COMUNICACIÓN DIGITAL CON PÚBLICO COMUNITARIO

## S.1 Cómo redactar mensajes para todas las edades

Es importante que la web sea entendida por mayores y jóvenes.

### S.1.1 Reglas básicas

- Usa frases cortas.
- Evita tecnicismos.
- Incluye ejemplos concretos.
- No uses siglas sin explicación.

## S.2 Formatos de texto claros

- Títulos con mayúsculas iniciales.
- Fechas en formato `24 ABR 2026`.
- Negritas para lo más importante.
- Listas con viñetas para pasos.

## S.3 Ejemplo de comunicado claro

```html
<article class="noticia-card" data-categoria="comunicado">
    <div class="noticia-header">
        <span class="noticia-categoria"><i class="fas fa-info-circle"></i> AVISO</span>
        <span class="noticia-fecha"><i class="far fa-calendar-alt"></i> 4 MAY 2026</span>
    </div>
    <div class="noticia-body">
        <h3>Información para las familias del sector Sabilar</h3>
        <p>El Consejo Comunal recuerda que el corte de energía será mañana de 8:00 a.m. a 12:00 p.m. Trae tus utensilios necesarios y comparte el aviso con tus vecinos.</p>
    </div>
    <div class="noticia-footer">
        <a href="noticia.html?id=28" class="btn-leer-mas">VER DETALLES <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

## S.4 Cómo usar las redes comunitarias con el sitio

Comparte el enlace del sitio en los grupos de WhatsApp, Telegram y redes sociales locales. La página web debe ser el punto de referencia oficial.

## S.5 Mensajes de la UPTOS para la comunidad

Cuando el equipo UPTOS apoye una publicación, puede incluir una frase como:

> Este contenido se comparte con el apoyo del equipo investigador de la UPTOS.

Esto ayuda a construir confianza entre comunidad y academia.

# ANEXO T: CHECKLIST DE PUBLICACIÓN FINAL

## T.1 Checklist antes de publicar cambios

- [ ] ¿Se guardaron todos los archivos? (`Ctrl + S`)
- [ ] ¿Se revisaron las etiquetas HTML?
- [ ] ¿Se verificaron las imágenes?
- [ ] ¿Se comprobó el enlace `noticia.html?id=`?
- [ ] ¿Se revisó el texto de estado de servicios?
- [ ] ¿Se verificó la coherencia de fechas?
- [ ] ¿Se probó en el navegador?
- [ ] ¿Se verificó el menú de navegación?
- [ ] ¿Se redactó un mensaje de commit claro?
- [ ] ¿Se hizo push a `origin`?
- [ ] ¿Se esperaron 60-120 segundos?
- [ ] ¿Se recargó el sitio en vivo?

## T.2 Checklist de documentación interna

- [ ] ¿Se registró el cambio en el acta o cuaderno?
- [ ] ¿Se informó a los demás voceros?
- [ ] ¿Se agregó un comentario útil si era necesario?
- [ ] ¿Se mantiene este manual actualizado?
- [ ] ¿Se compartió la información con la comunidad?

## T.3 Línea final de responsabilidad

Cada publicación en la página web es una acción de gobierno comunitario. El Consejo Comunal debe reconocer su responsabilidad al actualizar información. Este manual es una herramienta, pero la decisión final siempre corresponde a los voceros y voceras.

---

**FIN DEL ANEXO ADICIONAL**

**MANUAL MAESTRO VILLA ROSARIO**

**Versión 1.0 Maestro**

**Junio 2026**
# ANEXO U: ACTUALIZACIONES FUTURAS Y RESPALDOS

## U.1 Cómo planificar la próxima actualización del manual

Recomendamos que el Consejo Comunal revise este manual cada seis meses. Un equipo de voceros puede reunirse para evaluar:

- Cambios en la comunidad.
- Nuevas necesidades informativas.
- Actualizaciones del sitio web.
- Propuestas de capacitación.

Un buen plan de actualización incluye una sesión de 60 minutos para revisar los contenidos y otra de trabajo práctico para aplicar los cambios.

## U.2 Documentos de respaldo que debes conservar

Además del sitio web, guarda los siguientes documentos:

- Actas de asambleas relevantes.
- Registros de decisiones del Consejo Comunal.
- Listados de voceros actualizados.
- Copias del manual en USB y en la nube.

## U.3 Cómo hacer una copia impresa del manual

Para facilitar su consulta, puedes imprimir este documento en formato PDF. La impresión también sirve como respaldo cuando no hay internet.

- Abre `MANUAL_MAESTRO_VILLA_ROSARIO.md` en un visor compatible.
- Elige `Imprimir` o `Exportar a PDF`.
- Guarda una copia con fecha.

## U.4 El valor de la documentación comunitaria

Este sitio web y este manual son parte de la memoria colectiva de Villa Rosario. Cada edición no es sólo un cambio en la tecnología; es también una forma de contar cómo la comunidad resolvió problemas, organizó actividades y fortaleció sus lazos.

Por eso, el mantenimiento del sitio debe verse como un acto de cuidado comunitario.

## U.5 Cierre ético y comunitario

Finalizamos este manual reafirmando que la tecnología debe servir a las personas. El sitio web de Villa Rosario es un instrumento del Consejo Comunal y de todas las familias del Sector Sabilar.

Nuestro compromiso como equipo UPTOS es que esta guía esté siempre disponible para que los voceros y voceras puedan continuar con la gestión, la comunicación y la participación sin perder el control de su propia herramienta digital.

**Gracias por confiar en la investigación y el apoyo de la UPTOS.**
