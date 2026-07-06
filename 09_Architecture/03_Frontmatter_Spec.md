# HISTORIUM — FRONTMATTER SPEC

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

El frontmatter es la puerta entre el Canon Markdown y los sistemas activos de Historium.

Permite que un documento sea leído por humanos y procesado por el importer.

Debe ser breve.

Debe ser estable.

Debe ser suficiente para validar una pieza antes de importarla.

---

# Regla base

Todo archivo importable debe iniciar con frontmatter YAML.

Los documentos puramente editoriales pueden no tenerlo.

Las entidades, campañas, capítulos, nodos y assets canónicos sí deben tenerlo.

---

# Campos universales

```yaml
---
id: "CHAR_000001"
type: "Character"
title: "Pisístrato"
slug: "pisistratus"
status: "draft"
version: "1.0.0"
language: "es"
created_at: "2026-07-05"
updated_at: "2026-07-05"
---
```

---

# Campos de Museo

```yaml
museum:
  gallery: "Characters"
  default_level: 1
  max_level: 4
  unlockable: true
```

---

# Campos del Knowledge Graph

```yaml
relationships:
  - type: "governed"
    target: "CITY_000001"
    confidence: "high"
    visibility: "public"
```

Las relaciones siempre apuntan a IDs.

Nunca a nombres visibles.

---

# Campos de campaña

```yaml
campaign:
  id: "CAMP_000001"
  arc: "ARC_000001"
  chapter: "CH_000001"
  node: "NODE_000001"
```

---

# Estados permitidos

```text
draft
review
canon
archived
deprecated
```

`canon` significa que el contenido forma parte del universo oficial.

`archived` significa que se conserva por historia editorial.

`deprecated` significa que fue reemplazado pero no eliminado.

---

# Visibilidad

```yaml
visibility: "public | hidden | premium | secret"
```

`hidden` permite relaciones desbloqueables.

`secret` permite conexiones futuras que aún no deben mostrarse al jugador.

---

# Regla Suprema

Si el frontmatter no permite importar, validar y conectar la pieza sin ambigüedad, el documento no está listo.
