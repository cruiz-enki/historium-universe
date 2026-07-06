# HISTORIUM — IMPORT WORKFLOW

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define cómo el Canon en Markdown se convierte en datos activos.

Importar no es copiar.

Importar es validar, transformar y proteger el universo.

---

# Flujo general

```text
Markdown Canon
  ↓
Frontmatter validation
  ↓
ID validation
  ↓
Relationship validation
  ↓
Museum mapping
  ↓
Supabase upsert
  ↓
Import report
```

---

# Paso 1 — Lectura

El importer lee archivos Markdown canónicos.

Debe ignorar:

- borradores sin frontmatter,
- documentos editoriales no importables,
- archivos archivados,
- carpetas de referencia sin entidad.

---

# Paso 2 — Validación de ID

Cada ID debe:

- usar prefijo oficial,
- tener seis dígitos,
- existir como valor asignado,
- no duplicarse,
- no contradecir `REGISTRY.yaml`.

---

# Paso 3 — Validación de frontmatter

El frontmatter debe incluir campos mínimos según tipo.

Si falta un campo obligatorio, el importer se detiene.

---

# Paso 4 — Validación de relaciones

Cada relación debe:

- usar tipo oficial,
- apuntar a IDs existentes,
- respetar source_types y target_types,
- no duplicar relaciones equivalentes,
- tener visibilidad válida.

---

# Paso 5 — Mapeo de Museo

Toda entidad importable debe mapearse a una galería del Museo.

Todo nodo debe declarar actualizaciones del Museo.

Sin Museo, no hay importación.

---

# Paso 6 — Upsert

Supabase debe actualizar por ID.

Nunca por nombre.

Si el ID existe, se actualiza versión y contenido.

Si no existe, se crea.

---

# Paso 7 — Reporte

Cada importación debe generar reporte con:

- archivos procesados,
- entidades creadas,
- entidades actualizadas,
- relaciones creadas,
- errores,
- advertencias,
- versión de importación.

---

# Errores bloqueantes

- ID duplicado.
- Relación hacia entidad inexistente.
- Tipo desconocido.
- Nodo sin actualización de Museo.
- Campaña sin estructura.
- Frontmatter inválido.

---

# Regla Suprema

El importer debe fallar antes de contaminar el universo activo.
