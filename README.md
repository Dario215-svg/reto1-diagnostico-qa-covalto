# Reto 1: Diagnóstico Básico - Auditoría QA & Corrección de Código

**Candidato:** Carlos Dario Lara Garcia (`@Dario215-svg`)    
**Evaluación:** Challenge Técnico Covalto - Diagnóstico Básico  

---

## Objetivo
Realizar una inspección estática de código (`HTML`, `CSS` y `JS`) y pruebas funcionales/visuales de interfaz de usuario (UI) sobre el proyecto web proporcionado, con el objetivo de:
1. Identificar y documentar todos los defectos (bugs) presentes en la página.
2. Corregir el código fuente (`index1.html`) y presentar la evidencia del sitio funcionando de manera correcta.

---

## Resumen de Hallazgos por Severidad

| Nivel de Severidad | Cantidad de Bugs | IDs Asociados | Estado Actual |
| :--- | :---: | :--- | :---: |
| **Crítica** | 1 | `BUG-01` | 100% Cerrados |
| **Alta** | 10 | `BUG-03` al `BUG-12` | 100% Cerrados |
| **Media** | 2 | `BUG-02`, `BUG-13` |  100% Cerrados |
| **TOTAL** | **13 Defectos** | `BUG-01` al `BUG-13` | **13 / 13 Resueltos** |

---

##  Matriz de Defectos

| ID | Severidad | Título del Defecto | Descripción y Causa Raíz (Resultado Actual) | Corrección Aplicada (Resultado Esperado) | Estado |
| :--- | :---: | :--- | :--- | :--- | :---: |
| **BUG-01** | Crítica | La hoja de estilos no carga por nombre y extensión incorrecta (`estilos2.ssc`) | La etiqueta `<link>` referencia a `href="estilos2.ssc"`, archivo inexistente y con extensión invertida, dejando toda la página sin diseño CSS. | Se corrigió la referencia a `href="estilos.css"`. | Closed |
| **BUG-02** | Media | Clase CSS del contenedor preloader mal escrita (`centradoo`) | El contenedor `#onload` tiene la clase escrita como `class="centradoo"` (doble "o"), impidiendo el centrado del preloader. | Se corrigió el atributo a `class="centrado"`. | Closed |
| **BUG-03** | Alta | Enlaces del menú de navegación inhabilitados por atributo mal escrito (`hred`) | Los 5 enlaces del menú (`Inicio`, `Equipo`, `Servicios`, `Trabajos`, `Contacto`) usan `hred="#"` en lugar de `href="#"`. | Se reemplazó `hred="#"` por `href="#"` en los 5 elementos `<a>`. | Closed |
| **BUG-04** |  Alta | Bloque de título principal duplicado y mal comentado con sintaxis `"//"` | Se intentó comentar un segundo contenedor `<div class="text">` usando `//` en vez de `<!-- -->`, duplicando el título y mostrando `//` en pantalla. | Se eliminó el bloque duplicado y se colocó el nombre del candidato en el `<h1>` principal. | Closed |
| **BUG-05** | Alta | Enlace "Equipo" del menú no hace scroll por discrepancia de ID (`equipos` vs `equipo`) | La sección tiene `id="equipos"` (en plural), mientras que `js/filtro.js` busca el selector `$('#equipo')` (en singular). | Se homologó el identificador a `id="equipo"`. | Closed |
| **BUG-06** | Alta | Error de sintaxis HTML en contenedor `<div class="card")` cerrado con paréntesis | La etiqueta de apertura cierra con un paréntesis `)` en lugar de `>`, rompiendo la estructura del DOM y el contenedor Flexbox de las 3 columnas. | Se corrigió la sintaxis a `<div class="card">`. | Closed |
| **BUG-07** | Alta | Primera tarjeta de "Nuestro equipo" pierde estilos por clase mal escrita (`content-cord`) | La primera tarjeta tiene `class="content-cord"`, perdiendo el ancho, bordes y sombras definidos en `.content-card`. | Se corrigió el nombre de la clase a `class="content-card"`. | Closed |
| **BUG-08** | Alta | Segunda imagen de "Nuestro equipo" no carga por ruta incorrecta (`imd/people2.jpg`) | El atributo `src` apunta a una carpeta inexistente llamada `imd/` en lugar de `img/`. | Se corrigió la ruta a `src="img/people2.jpg"`. | Closed |
| **BUG-09** | Alta | Primer ícono de "Nuestros servicios" no se visualiza por extensión incorrecta (`heart.gif`) | Se invoca `src="img/heart.gif"`, pero el recurso real dentro del directorio `img/` es formato `.png`. | Se actualizó la ruta a `src="img/heart.png"`. | Closed |
| **BUG-10** | Alta | Navegación a "Nuestro trabajo" falla por atributo inválido (`identificador="trabajo"`) | La sección del portafolio utiliza el atributo inexistente `identificador="trabajo"` en lugar de `id="trabajo"`, rompiendo el scroll desde el menú. | Se reemplazó por el atributo estándar `id="trabajo"`. | Closed |
| **BUG-11** | Alta | Etiqueta `<h3>` sin cerrar en sección "Nuestro trabajo" altera estilos de la galería | El título está escrito como `<h3>Nuestro trabajo<h3>` sin la barra diagonal `/`, aplicando estilos de título al resto de elementos. | Se cerró correctamente la etiqueta como `<h3>Nuestro trabajo</h3>`. | Closed |
| **BUG-12** | Alta | Primera tarjeta de "Diseño" (y tarjeta de Marketing) se deforma y no filtra por atributo mal escrito (`clas`) | El contenedor tiene el atributo escrito con una sola "s" (`clas="cont-work diseño"` y `clas="cont-work marketing"`), rompiendo la cuadrícula y el filtro JS. | Se corrigió el atributo a `class="cont-work..."`. | Closed |
| **BUG-13** | Media | Etiqueta `<foooter>` mal escrita e imagen rota (`img/logo.png`) en el pie de página | La etiqueta de apertura tiene tres letras "o" (`<foooter>`) e invoca `img/logo.png`, archivo que no existe en `img/`. | Se corrigió a `<footer id="contacto">` y se retiró la imagen inexistente. | Closed |

---
