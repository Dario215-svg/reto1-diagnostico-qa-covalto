# reto1-diagnostico-qa-covalto
Reto 1: Diagnóstico Básico - Auditoría QA & Corrección de Código

**Candidato:** Carlos Dario Lara Garcia    
**Evaluación:** Challenge Técnico Covalto - Diagnóstico Básico  

---

## Objetivo
Realizar una inspección estática de código (HTML, CSS y JS) y pruebas de interfaz de usuario (UI) sobre el proyecto `DiagnosticoBásico`, con el fin de:
1. Identificar y documentar todos los defectos (bugs) presentes en la página.
2. Corregir el código fuente para restaurar el diseño, la carga de recursos multimedia y la funcionalidad de filtrado y navegación.
3. Presentar la evidencia visual del resultado final esperado.

---

## Reporte de Bugs

Durante la revision sobre `index1.html` y su integración con `estilos.css` y `js/filtro.js`, se detectaron y corrigieron **15 defectos**:

| ID | Severidad | Línea (`index1.html`) | Descripción del Defecto (Resultado Actual) | Corrección Aplicada (Resultado Esperado) | Estado |
| :--- | :---: | :---: | :--- | :--- | :---: |
| **BUG-01** | 🔴 Crítica | 9 | Hoja de estilos no carga por nombre y extensión incorrecta: `href="estilos2.ssc"`. | Se corrigió la referencia a `href="estilos.css"`. | ✅ Resuelto |
| **BUG-02** | 🟡 Media | 15 | Clase del preloader mal escrita con doble "o": `class="centradoo"`. | Se corrigió a `class="centrado"`. | ✅ Resuelto |
| **BUG-03** | 🟢 Baja | 22 | Etiqueta `<img src="#">` sin ruta válida en `.logo` muestra ícono de imagen rota. | Se limpió el contenedor `.logo` para coincidir con el diseño oficial. | ✅ Resuelto |
| **BUG-04** | 🟠 Alta | 25-29 | Los 5 enlaces del menú principal usan el atributo inexistente `hred="#"`. | Se corrigió a `href="#"` en los 5 enlaces de navegación. | ✅ Resuelto |
| **BUG-05** | 🟢 Baja | 26 | En la vista preliminar del reto el menú muestra el error ortográfico `"Eupipo"`. | Se verificó y aseguró el texto correcto `"Equipo"`. | ✅ Resuelto |
| **BUG-06** | 🟠 Alta | 40-43 | Título principal duplicado y mal comentado con `//` (sintaxis JS) en lugar de `<!-- -->`. | Se eliminó el bloque duplicado y se colocó el nombre del autor en el `<h1>`. | ✅ Resuelto |
| **BUG-07** | 🟠 Alta | 46 | Sección de equipo tiene `id="equipos"` (plural), rompiendo el scroll de `filtro.js`. | Se corrigió a `id="equipo"` (singular). | ✅ Resuelto |
| **BUG-08** | 🟠 Alta | 49 | Error de sintaxis HTML: contenedor `<div class="card")` cerrado con paréntesis `)`. | Se corrigió la etiqueta a `<div class="card">`. | ✅ Resuelto |
| **BUG-09** | 🟠 Alta | 50 | Primera tarjeta de equipo tiene la clase mal escrita como `content-cord`. | Se corrigió a `class="content-card"` para alinear las 3 columnas. | ✅ Resuelto |
| **BUG-10** | 🟠 Alta | 60 | Segunda foto de equipo apunta a carpeta inexistente: `src="imd/people2.jpg"`. | Se corrigió la ruta a `src="img/people2.jpg"`. | ✅ Resuelto |
| **BUG-11** | 🟠 Alta | 81 | Primer ícono de servicios busca `src="img/heart.gif"`, formato inexistente en `img/`. | Se corrigió la extensión a `src="img/heart.png"`. | ✅ Resuelto |
| **BUG-12** | 🟠 Alta | 97 | Sección de portafolio usa atributo inválido `identificador="trabajo"`. | Se reemplazó por el estándar `id="trabajo"`. | ✅ Resuelto |
| **BUG-13** | 🟠 Alta | 98 | Encabezado `<h3>Nuestro trabajo<h3>` sin barra diagonal de cierre `</h3>`. | Se cerró correctamente como `<h3>Nuestro trabajo</h3>`. | ✅ Resuelto |
| **BUG-14** | 🟠 Alta | 133, 165 | Dos tarjetas de la galería tienen el atributo mal escrito como `clas="cont-work..."`. | Se corrigió a `class="cont-work..."` en Diseño y Marketing. | ✅ Resuelto |
| **BUG-15** | 🟡 Media | 182, 185 | Etiqueta `<foooter>` con tres "o" e invocación a `img/logo.png` inexistente. | Se corrigió a `<footer id="contacto">` y se retiró la imagen rota. | ✅ Resuelto |
