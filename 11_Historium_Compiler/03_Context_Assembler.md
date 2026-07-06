# HISTORIUM — CONTEXT ASSEMBLER

**Versión:** 1.0  
**Estado:** Oficial

---

# Propósito

El Context Assembler selecciona qué partes del Canon necesita una tarea.

Nunca manda todo el repositorio a la IA.

Manda contexto relevante.

---

# Ejemplo: crear un nodo

Debe leer:

- `02_Specifications/01_Campaign_Spec.md`
- `02_Specifications/02_Chapter_Spec.md`
- `02_Specifications/03_Node_Spec.md`
- entidades relacionadas en `03_Knowledge/`
- relaciones existentes
- `00_Biblia_Editorial/03_Voice_And_Tone.md`
- `00_Biblia_Editorial/04_Narrative_Patterns.md`
- reglas de `10_AI/`
- `09_Architecture/03_Frontmatter_Spec.md`
- `10_AI/12_Markdown_Output_Format.md`

---

# Paquete de contexto

Debe contener:

- objetivo,
- constraints,
- entidades,
- relaciones,
- tono,
- formato,
- prohibiciones,
- checklist.

---

# Exclusiones

No incluir:

- documentos no relacionados,
- campañas enteras si solo se genera un nodo,
- assets irrelevantes,
- specs que no aplican.

---

# Regla Suprema

El mejor contexto no es el más grande.

Es el más preciso.
