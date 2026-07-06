# HISTORIUM — CONTENT GENERATION PIPELINE

**Versión:** 1.0  
**Estado:** Oficial

---

# Flujo oficial

```text
Brief
↓
Research
↓
Entity lookup
↓
Relationship lookup
↓
Outline
↓
Draft
↓
Fact check
↓
Museum update
↓
Markdown validation
↓
Human review
↓
Import
```

---

# Brief

Define campaña, objetivo, audiencia, periodo, tono, output esperado y restricciones.

---

# Research

Reúne contexto histórico.

Separa hechos, debate, mito e interpretación.

---

# Entity lookup

Busca entidades existentes antes de crear nuevas.

Consulta `03_Knowledge/REGISTRY.yaml` solo si una entidad nueva es necesaria.

---

# Relationship lookup

Consulta `03_Knowledge/RELATIONSHIP_TYPES.md`.

No se permiten relaciones libres.

---

# Outline

Define estructura narrativa, Museo, entidades y assets antes de redactar.

---

# Draft

Produce contenido con tono Historium.

Párrafos cortos.

Ritmo cinematográfico.

---

# Fact check

Valida claims y marca incertidumbre.

---

# Museum update

Declara qué entidades, niveles, relaciones o assets desbloquea.

---

# Markdown validation

Comprueba frontmatter, headings, YAML, relaciones y checklist.

---

# Human review

Un humano aprueba Canon.

La IA no publica sola.

---

# Import

Solo contenido validado pasa al importer.
