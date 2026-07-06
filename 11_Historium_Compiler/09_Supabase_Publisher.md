# HISTORIUM — SUPABASE PUBLISHER

**Versión:** 1.0  
**Estado:** Oficial

---

# Flujo conceptual

```text
Markdown
↓
Parser
↓
Frontmatter
↓
Entity records
↓
Relationship records
↓
Campaign records
↓
Museum unlock rules
↓
Assets
↓
Published state
```

---

# Parser

Lee Markdown y YAML.

No interpreta nombres como IDs.

---

# Entity records

Crea o actualiza entidades por ID.

---

# Relationship records

Crea conexiones tipificadas.

---

# Campaign records

Crea campañas, capítulos y nodos.

---

# Museum unlock rules

Define qué desbloquea cada nodo.

---

# Assets

Conecta prompts, imágenes, audio, video y mapas.

---

# Published state

Solo contenido validado llega a published.

---

# Regla Suprema

Supabase publica estado activo.

No decide Canon.
