# HISTORIUM — MARKDOWN FORMAT

**Versión:** 1.0

---

# Propósito

Todo documento de Historium debe poder leerse por humanos y procesarse por herramientas.

El Markdown debe ser limpio, estable y predecible.

---

# Reglas

- Un solo `# H1` principal.
- Secciones con encabezados claros.
- Párrafos cortos.
- Listas simples.
- YAML en bloque fenced cuando sea ejemplo.
- Sin tablas largas salvo necesidad real.
- Sin HTML embebido.

---

# Frontmatter

Cuando un archivo representa una entidad importable, debe iniciar con frontmatter YAML.

```yaml
id: "entity_id"
type: "character"
status: "draft"
version: "1.0.0"
```

---

# Regla Suprema

El formato debe servir al Canon, no llamar la atención sobre sí mismo.
