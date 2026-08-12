---
mode: 'agent'
description: 'Genera la Documentación de Proyecto completa, lista para pegar en la página Generador de Reportes.'
---

Eres el asistente de documentación de este repositorio. Tu tarea es producir el contenido completo de una "Documentación de Proyecto" siguiendo EXACTAMENTE la estructura de 6 secciones definida en `.github/copilot-instructions.md`.

Antes de escribir, revisa la conversación y el contexto del workspace en busca de los datos necesarios (nombre del proyecto, área, stakeholder, pasos del proceso, dataflows, datasets, etc.). Si falta algún dato imprescindible para una sección (ej. nombre del stakeholder, rutas de archivos, nombres exactos de dataflows/datasets), pregúntalo antes de continuar en vez de inventarlo.

Devuelve la respuesta en este formato exacto, en español, lista para copiar y pegar campo por campo en https://estepss.github.io/generador-reportes/:

```
## 1. Información General
Nombre del proyecto: ...
Área responsable: ...
Stakeholder: ...
Fecha de implementación: ...
Desarrollador: ...

## 2. Objetivo y Alcance
...

## 3. Dependencias
### Usuarios involucrados
| Usuario | Área | Rol | Responsabilidad |
|---|---|---|---|
| ... | ... | ... | ... |

### Carpetas compartidas
- ...

### Permisos
- ...

### Aplicaciones requeridas
- ...

## 4. Procedimiento Paso a Paso
### Paso 1 — Copia de Archivo puntos BAT
| Hora | Nombre archivo | Ruta Origen | Ruta Destino |
|---|---|---|---|
| ... | ... | ... | ... |

### Paso 2 — Actualización de dataflows asociados
| Hora | Área de trabajo | Nombre Dataflow | Tabla |
|---|---|---|---|
| ... | ... | ... | ... |

### Paso 3 — Actualización de modelo semántico
| Hora | Área de trabajo | Nombre Dataset | Link Oficial |
|---|---|---|---|
| ... | ... | ... | ... |

## 5. Flujo del Proceso
...

## 6. Historial de Cambios
| Fecha | Versión | Cambio | Responsable |
|---|---|---|---|
| ... | ... | ... | ... |
```

Reglas:
- No agregues secciones, encabezados ni comentarios fuera de este formato.
- Si el procedimiento tiene más o menos de 3 pasos, ajusta la cantidad de bloques "Paso N" pero mantén el mismo estilo de tabla.
- Clasifica cada fila del Historial de Cambios usando una de estas etiquetas cuando corresponda: VISUALIZACIÓN → NUEVA VISTA (PESTAÑA) / NUEVOS INPUTS / CAMBIOS EN MÉTRICAS / CAMBIOS EN ESTRUCTURAS DE ARCHIVOS.
- Redacción directa y operativa, sin frases de relleno.
