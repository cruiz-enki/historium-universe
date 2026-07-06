# HISTORIUM — IMPORT WORKFLOW

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define cómo el Canon en Markdown se convierte en datos activos en Supabase.

Importar no es copiar archivos.

Importar es validar el universo antes de hacerlo jugable.

---

# Flujo oficial

```text
Markdown
↓
Validation
↓
Parse frontmatter
↓
Resolve IDs
↓
Create/update Supabase records
↓
Create relationships
↓
Create museum unlock rules
↓
Publish to app
```

---

# 1. Markdown

El importer lee archivos Markdown del Canon Oficial.

Solo procesa archivos importables.

Documentos editoriales puros pueden quedar fuera.

---

# 2. Validation

Valida:

- nombre de archivo,
- ubicación,
- extensión,
- frontmatter,
- estado,
- versión,
- tipo oficial.

---

# 3. Parse frontmatter

Extrae datos estructurados.

Si el frontmatter no existe o está roto, el flujo se detiene.

---

# 4. Resolve IDs

Verifica que:

- el ID usa prefijo oficial,
- el formato es `PREFIX_000001`,
- no hay duplicados,
- las relaciones apuntan a IDs existentes,
- `REGISTRY.yaml` no fue contradicho.

---

# 5. Create/update Supabase records

Crea o actualiza registros por ID.

Nunca por nombre.

Nunca por slug.

---

# 6. Create relationships

Crea relaciones tipificadas.

Valida `source_types`, `target_types` e inversas sugeridas.

---

# 7. Create museum unlock rules

Genera reglas de desbloqueo:

- entidad descubierta,
- sección estudiada,
- relación visible,
- asset desbloqueado,
- recompensa entregada.

---

# 8. Publish to app

Solo se publica contenido:

- válido,
- oficial,
- importado,
- sin errores bloqueantes.

---

# Errores bloqueantes

- ID duplicado.
- Tipo desconocido.
- Relación inválida.
- Frontmatter incompleto.
- Nodo sin `museum_updates`.
- Campaña sin capítulos.
- Asset roto.

---

# Regla Suprema

El importer debe detenerse antes de contaminar el universo activo.
