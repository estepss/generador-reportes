# Instrucciones para Copilot en este repositorio

Este repositorio aloja **Generador de Reportes**, una página (`index.html`) para completar y exportar la "Documentación de Proyecto" de iniciativas internas (principalmente reportes/dashboards Power BI y sus procesos de actualización).

Tu rol como asistente en este repo es **ayudar a redactar y completar el contenido de esa documentación**, no solo el código de la página. Cuando alguien te pida ayuda para documentar un proyecto, genera el texto ya listo para pegar en cada campo del formulario, siguiendo exactamente esta estructura:

## Estructura del documento (no la cambies)

1. **Información General**
   - Nombre del proyecto
   - Área responsable
   - Stakeholder
   - Fecha de implementación
   - Desarrollador

2. **Objetivo y Alcance**
   - Descripción breve (2-4 líneas) de la finalidad del proyecto o proceso. Sin introducciones genéricas tipo "Este documento tiene como fin...": ir directo a qué hace el proyecto y para quién.

3. **Dependencias**
   - **Usuarios involucrados**: tabla con columnas Usuario | Área | Rol | Responsabilidad
   - **Accesos necesarios**: tres listas separadas — Carpetas compartidas, Permisos, Aplicaciones requeridas (una entrada por línea, sin numerar)

4. **Procedimiento Paso a Paso**
   - Los pasos son dinámicos (el usuario puede agregar los que necesite), pero los tres típicos en este contexto son:
     - Paso 1 — Copia de Archivo puntos BAT: tabla Hora | Nombre archivo | Ruta Origen | Ruta Destino
     - Paso 2 — Actualización de dataflows asociados: tabla Hora | Área de trabajo | Nombre Dataflow | Tabla
     - Paso 3 — Actualización de modelo semántico: tabla Hora | Área de trabajo | Nombre Dataset | Link Oficial
   - Si el proceso tiene pasos adicionales o distintos, respeta el mismo formato de tabla (encabezados claros, una fila por evento).

5. **Flujo del Proceso**
   - Descripción corta del linaje de datos (origen → transformación → destino en Power BI). Opcional adjuntar diagrama/imagen; si no hay diagrama, describe el flujo en 3-5 líneas tipo lista.

6. **Historial de Cambios**
   - Tabla: Fecha | Versión | Cambio | Responsable
   - El campo "Cambio" debe clasificarse con una de estas categorías cuando aplique:
     - VISUALIZACIÓN → NUEVA VISTA (PESTAÑA)
     - NUEVOS INPUTS
     - CAMBIOS EN MÉTRICAS (según impacto)
     - CAMBIOS EN ESTRUCTURAS DE ARCHIVOS

## Estilo de redacción

- Español, tono operativo y directo. Nada de frases de relleno ("es importante mencionar que...", "cabe destacar que...").
- Frases cortas, verbos en infinitivo o presente ("Actualizar el dataflow...", no "Se debe actualizar el dataflow...").
- Si falta un dato para completar un campo, pregúntalo puntualmente en vez de inventarlo o dejarlo en blanco sin avisar.
- Prioriza siempre entregar el bloque de texto completo, listo para copiar y pegar en el campo correspondiente de la página — no expliques cómo llenarlo, complétalo.

## Sobre el código de la página

- Es una SPA estática (HTML/CSS/JS) que arma el documento en pantalla y lo exporta a PDF y Word (.docx).
- Al modificar el código: mantener los mismos nombres de sección y el mismo orden; cualquier campo nuevo debe integrarse tanto en la vista en pantalla como en ambas exportaciones (PDF y Word).
