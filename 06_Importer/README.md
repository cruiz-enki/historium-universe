# HISTORIUM — IMPORTER

**Estado:** Oficial

---

# Propósito

Esta carpeta define cómo el Canon Oficial en Markdown se convierte en datos listos para producción.

GitHub contiene el Canon.

Supabase contiene el progreso del usuario.

El importer conecta ambos mundos sin mezclarlos.

Debe respetar los formatos de salida definidos en `../10_AI/`, especialmente:

- `12_Markdown_Output_Format.md`
- `13_Validation_Rules.md`
- `10_Entity_Extraction_Rules.md`
- `11_Relationship_Extraction_Rules.md`

---

# Principios

- Markdown es la fuente editorial.
- Frontmatter define identidad estructurada.
- Supabase no decide canon.
- El importer valida antes de publicar.
- Ningún contenido roto debe llegar al jugador.

---

# Documentos

- `Markdown_Format.md`
- `../02_Specifications/Frontmatter_Spec.md`
- `Import_Validation.md`
- `Supabase_Mapping.md`

---

# Regla Suprema

Importar no es copiar archivos.

Importar es proteger el Canon mientras se vuelve jugable.
