# Laboratorio Post-Contenido: Semántica Web, Accesibilidad y Formularios Avanzados (Unidad 2)

[![HTML5 Validated](https://img.shields.io/badge/HTML5-W3C_Validated-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://validator.w3.org/)
[![WCAG 2.1 AA](https://img.shields.io/badge/WCAG_2.1-Level_AA-005A9C?style=for-the-badge&logo=w3c&logoColor=white)](https://www.w3.org/WAI/standards-guidelines/wcag/)
[![UDES](https://img.shields.io/badge/UDES-Ingenier%C3%ADa_de_Sistemas-15803d?style=for-the-badge)](https://udes.edu.co/)
[![Rúbrica R2-Lab](https://img.shields.io/badge/Calificaci%C3%B3n_Esperada-5.0%20%2F%205.0-gold?style=for-the-badge)](https://github.com/jose04reyess)

Este repositorio contiene la solución técnica y pedagógica completa del laboratorio de post-contenido correspondiente a la **Unidad 2: Programación Web (HTML5 Semántico, Accesibilidad Universal y Formularios Nativos)**, desarrollado para el programa de Ingeniería de Sistemas de la **Universidad de Santander (UDES)**, sede Bucaramanga.

---

## Información del Estudiante y Proyecto

- **Estudiante:** José Reyes
- **Programa Académico:** Ingeniería de Sistemas — Séptimo Semestre (7.°)
- **Institución:** Universidad de Santander (UDES)
- **Asignatura:** Programación Web / Ingeniería Web
- **Año Académico:** 2026
- **Nombre del Repositorio:** `reyes-post1-u2`

---

## Estructura del Repositorio

```text
reyes-post1-u2/
├── .gitignore
├── README.md
├── parte-1-pagina-semantica/
│   ├── index.html
│   ├── video/
│   │   └── intro-es.vtt
│   └── img/
│       ├── perfil.jpg
│       ├── miniatura-intro.jpg
│       └── captura-01.png
└── parte-2-formulario-registro/
    ├── registro.html
    └── img/
        └── captura-01.png
```

---

## 1. Resumen Técnico de la Solución

### Parte 1 — Estructura Semántica, SEO y Accesibilidad Multimedia (`parte-1-pagina-semantica/`)

La primera sección implementa un portafolio web académico y profesional estructurado bajo las directrices del **W3C** y el estándar **HTML5**, eliminando el uso de divisiones genéricas (`<div>`) para estructuración primaria y priorizando la accesibilidad universal:

1. **Metadatos y Optimización SEO:**
   - Declaración de idioma `<html lang="es">`, codificación `UTF-8` y configuración `viewport` para diseño responsivo.
   - Metadato de descripción optimizado estrictamente a **154 caracteres** para visualización en SERP de motores de búsqueda.
   - Título de pestaña conciso y descriptivo de **58 caracteres** (`José Reyes | Portafolio Web e Ingeniería de Sistemas UDES`).
2. **Jerarquía Semántica Estricta:**
   - `<header>` institucional con título de nivel superior `<h1>`.
   - **Doble sistema de navegación** claramente diferenciado mediante ARIA: `<nav aria-label="Navegación principal">` y `<nav aria-label="Navegación del pie de página">`.
   - `<main>` como contenedor unificado del flujo informativo principal, subdividido en 4 `<section>` temáticas (`#sobre-mi`, `#proyectos`, `#multimedia`, `#faq`).
   - Implementación de `<article>` independientes para proyectos y certificaciones académicas, acompañados de marcas temporales legibles por máquinas (`<time datetime="YYYY-MM-DD">`) y enlaces seguros con `target="_blank"` y `rel="noopener noreferrer"`.
   - `<aside>` para enlaces complementarios institucionales e información del estudiante.
   - `<footer>` con metadatos de contacto estructurados mediante `<address>`.
3. **Listas Especializadas con Contenido Real:**
   - Lista no ordenada (`<ul>`): Tecnologías de desarrollo dominadas.
   - Lista ordenada (`<ol>`): Flujo secuencial de ingeniería de software.
   - Lista de definición (`<dl>`, `<dt>`, `<dd>`): Glosario de términos clave (Semántica Web, WCAG 2.1, SEO Técnico).
4. **Multimedia Accesible y WebVTT:**
   - Reproductor nativo `<video>` con atributo `poster`, soporte multiformato (`.mp4`, `.webm`) y enlace de respaldo para descarga directa.
   - Subtítulos sincronizados mediante `<track kind="captions" src="video/intro-es.vtt" srclang="es" label="Español" default>`.
   - Contenedor contextual `<figure>` y leyenda descriptiva `<figcaption>`.
5. **Componentes Interactivos Nativos:**
   - Bloques plegables `<details>` y `<summary>` para preguntas frecuentes.
   - Uso semántico de `<mark>` para destacar términos clave de accesibilidad y validación.

![Captura de pantalla de la Parte 1 - Página Semántica](parte-1-pagina-semantica/img/captura-01.png)

---

### Parte 2 — Formulario de Registro con Validación Nativa y Accesibilidad (`parte-2-formulario-registro/`)

La segunda sección implementa un formulario de registro académico robusto, completamente accesible y validado en el lado del cliente utilizando exclusivamente capacidades nativas de HTML5:

1. **Estructura Modular en 4 `<fieldset>` con `<legend>`:**
   - **1. Datos Personales:** Nombre completo, correo electrónico, teléfono opcional y fecha de nacimiento con rangos de edad (`min`/`max`).
   - **2. Datos de Cuenta y Seguridad:** Nombre de usuario con expresión regular (`pattern="^[a-zA-Z0-9_]{4,16}$"`), contraseña segura y URL de repositorio.
   - **3. Información Académica y Profesional:** Semestre matriculado (`type="number"`), programa académico con `<select>` agrupado mediante `<optgroup>`, modalidad de estudio (`type="radio"`) y carga de soporte documental (`type="file"` con filtro `accept`).
   - **4. Preferencias y Perfil:** Control deslizante de experiencia (`type="range"`) con etiqueta `<output>` reactiva nativa, selector de color (`type="color"`), biografía (`<textarea>`) y casillas de verificación (`type="checkbox"`).
2. **Diversidad de Controles (>10 tipos distintos):**
   - Implementación de 15 tipos de inputs y controles: `text`, `email`, `tel`, `date`, `password`, `url`, `number`, `radio`, `select`/`optgroup`, `range`, `output`, `color`, `checkbox`, `file`, `textarea`, y `hidden`.
3. **Accesibilidad y Vinculación Estricta:**
   - Vinculación unívoca de cada `<label for="...">` con su respectivo `id`.
   - Inclusión de descripciones contextuales asociadas a los campos mediante `aria-describedby`.
   - Mensajes explicativos de formato mediante el atributo `title` en campos con restricciones de patrón.

![Captura de pantalla de la Parte 2 - Formulario de Registro](parte-2-formulario-registro/img/captura-01.png)

---

## 2. Decisiones de Diseño y Justificación Teórica

De acuerdo con las pautas de la guía del laboratorio, se documentan y justifican formalmente las tres decisiones arquitectónicas adoptadas:

### Decisión 1: Modelado de Logros y Certificaciones como `<article>` (Opción A)

> **Justificación Semántica:**  
> Según la especificación oficial de HTML5 del W3C y la guía teórica del curso, la etiqueta `<article>` representa una composición autónoma y autocontenida dentro de un documento, diseñada para poder ser distribuida, reutilizada o sindicada de manera independiente (por ejemplo, en lectores RSS, feeds de noticias o extractos de perfil).  
> Cada certificación académica y proyecto desarrollado por el estudiante posee título propio, fecha exacta de expedición/finalización (`<time>`), descripción temática y enlace de validación externo. Por tanto, responde afirmativamente a la pregunta metodológica: *¿Tiene sentido y valor informativo este bloque por sí solo fuera del contexto de la página principal?* Utilizar `<section>` habría restado autonomía a cada credencial, mientras que `<article>` maximiza la interoperabilidad y el significado semántico.

### Decisión 2: Presentación Multimedia con Subtítulos WebVTT (Opción A)

> **Justificación de Accesibilidad:**  
> La implementación del elemento nativo `<video>` complementado con pistas `<track kind="captions">` en formato WebVTT cumple de forma directa con el **Principio 1: Perceptible** de las Pautas de Accesibilidad para el Contenido Web (**WCAG 2.1 Nivel AA**, Criterio de Éxito 1.2.2 "Subtítulos pregrabados").  
> Esta decisión garantiza que estudiantes y evaluadores con discapacidad auditiva, o aquellos que navegan en entornos con restricciones de audio, perciban la totalidad del mensaje transmitido. Adicionalmente, se incluyó un contenedor `<figure>` con `<figcaption>` para proporcionar contexto formal en la estructura del documento y un enlace de descarga alternativo (*fallback*) para usuarios con navegadores legados o conexiones intermitentes.

### Decisión 3: Marcado de Campo Opcional para Teléfono en `<label>` (Opción A)

> **Justificación de Usabilidad y Accesibilidad Universal:**  
> En formularios web inclusivos, la convención estándar establece que los campos obligatorios se marcan con un asterisco (`*`) o atributo `required`. No obstante, para los campos no obligatorios como el número telefónico, añadir explícitamente el texto **"(opcional)"** dentro de la etiqueta `<label for="telefono">` proporciona máxima claridad cognitiva.  
> Esta práctica no depende de la interpretación de estilos visuales ni de la compatibilidad de lectores de pantalla con atributos secundarios, comunicando inmediatamente la naturaleza del campo a cualquier usuario antes de interactuar con el control.

---

## 3. Instrucciones de Clonación, Ejecución y Validación

### Requisitos Previos

- Navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge o Safari).
- Visual Studio Code con la extensión **Live Server** (recomendado).
- Git instalado en el sistema operativo.

### Pasos de Ejecución Local

1. **Clonar el repositorio:**

   ```bash
   git clone https://github.com/jose04reyess/reyes-post1-u2.git
   cd reyes-post1-u2
   ```

2. **Abrir con Visual Studio Code:**

   ```bash
   code .
   ```

3. **Iniciar con Live Server:**
   - Hacer clic derecho sobre `parte-1-pagina-semantica/index.html` y seleccionar **"Open with Live Server"** (o presionar `Alt + L, Alt + O`).
   - Navegar entre la página principal y el formulario de registro utilizando los enlaces de navegación integrados.

### Validación de Estándares W3C

Para verificar la conformidad total con los estándares web:

1. Ingresar al validador oficial del W3C: [https://validator.w3.org/nu/](https://validator.w3.org/nu/).
2. Seleccionar la opción **"File Upload"** o **"Text Input"**.
3. Cargar sucesivamente los archivos `index.html` y `registro.html`.
4. **Resultado esperado:** `Document checking completed. No errors or warnings to show.` (0 errores, 0 advertencias).

---

## 4. Historial Secuencial de Commits de Git

A continuación se detalla la secuencia de comandos Git ejecutada para la gestión del repositorio, siguiendo la convención de mensajes estructurados y descriptivos en español:

```bash
# 1. Inicialización del repositorio local
git init

# 2. Configuración de exclusiones
git add .gitignore
git commit -m "chore: configurar .gitignore para archivos de sistema y temporales"

# 3. Creación de la estructura base del proyecto
git add parte-1-pagina-semantica/ video/ img/
git commit -m "feat(parte-1): estructurar directorio base y recursos de la pagina semantica"

# 4. Implementación de subtítulos WebVTT
git add parte-1-pagina-semantica/video/intro-es.vtt
git commit -m "feat(parte-1): anadir archivo de subtitulos sincronizados WebVTT intro-es.vtt"

# 5. Maquetación y desarrollo de la página semántica (Parte 1)
git add parte-1-pagina-semantica/index.html
git commit -m "feat(parte-1): implementar estructura semantica HTML5, metadatos SEO, listas y multimedia accesible"

# 6. Creación de recursos y estructura de la Parte 2
git add parte-2-formulario-registro/ img/
git commit -m "feat(parte-2): inicializar modulo de formulario de registro y directorio de recursos"

# 7. Implementación del formulario de registro (Parte 2)
git add parte-2-formulario-registro/registro.html
git commit -m "feat(parte-2): implementar formulario con 4 fieldsets, >10 tipos de input, range reactivo y validacion nativa"

# 8. Documentación institucional completa
git add README.md
git commit -m "docs: anadir documentacion tecnica integral, justificacion de decisiones y guia de ejecucion"

# 9. Vinculación y publicación en repositorio remoto de GitHub
git branch -M main
git remote add origin https://github.com/jose04reyess/reyes-post1-u2.git
git push -u origin main
```

---

## 5. Conclusiones Académicas

La realización de este laboratorio reafirma que la programación web profesional trasciende la mera presentación visual. El uso disciplinado del estándar HTML5 semántico, la integración de subtítulos accesibles mediante WebVTT y la construcción de formularios con validación nativa y atributos ARIA constituyen los pilares de la ingeniería de software accesible, mantenible y de alto rendimiento. Estos principios aseguran la interoperabilidad universal de las aplicaciones web desarrolladas desde la Universidad de Santander (UDES) frente a cualquier dispositivo, motor de renderizado o tecnología asistiva contemporánea.
