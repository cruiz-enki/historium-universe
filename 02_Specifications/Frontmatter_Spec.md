# HISTORIUM — FRONTMATTER SPEC

**Versión:** 1.0

---

# Propósito

El frontmatter identifica cada pieza importable del Canon.

Debe ser breve, estructurado y suficiente para validar el documento antes de enviarlo a Supabase.

---

# Campos base

```yaml
id: "unique_id"
type: "node | campaign | character | city | battle | concept | artifact | document"
title: "Título visible"
status: "draft | review | canon | archived"
version: "1.0.0"
updated_at: "YYYY-MM-DD"
```

---

# Campos de Museo

```yaml
museum_gallery: "Characters"
knowledge_level: 1
rewards: []
relationships: []
```

---

# Regla Suprema

Si el frontmatter no permite importar con confianza, el documento no está listo.
