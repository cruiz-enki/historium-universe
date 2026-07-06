# HISTORIUM — MUSEUM DATA MODEL

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define cómo el Museo del jugador representa el progreso personal dentro del Knowledge Graph.

El Museo no es una colección de trofeos.

Es la huella viva de lo que el jugador entiende.

---

# Canon vs Museo personal

El Canon contiene todo el universo.

El Museo personal contiene lo que un jugador ha descubierto, estudiado, dominado o llevado a maestría.

---

# Estados de descubrimiento

```text
locked
discovered
studied
mastered
completed
```

---

# Niveles de conocimiento

## Nivel 1 — Descubierto

El jugador sabe que existe.

---

## Nivel 2 — Estudiado

El jugador entiende su función histórica.

---

## Nivel 3 — Dominado

El jugador comprende conexiones, debates y consecuencias.

---

## Nivel 4 — Maestría

El jugador accede a documentos, reconstrucciones, podcasts, mapas y comparaciones profundas.

---

# Modelo por entidad

```yaml
user_id: "user_123"
entity_id: "CHAR_000001"
state: "studied"
knowledge_level: 2
progress_percent: 46
visible_relationships:
  - "REL_EDGE_000001"
hidden_relationships_remaining: 3
unlocked_assets:
  - "portrait"
  - "timeline"
last_node_completed: "NODE_000008"
```

---

# Modelo por relación

```yaml
user_id: "user_123"
source_id: "CHAR_000001"
relationship_type: "governed"
target_id: "CITY_000001"
visible: true
unlocked_by: "NODE_000008"
```

---

# Progreso global

El Museo puede calcular:

- porcentaje global,
- avance por galería,
- entidades descubiertas,
- entidades en maestría,
- rutas incompletas,
- próximos descubrimientos.

---

# Recompensa

La recompensa principal no es un objeto.

Es nueva comprensión.

Los objetos, badges y XP existen para hacer visible ese crecimiento.

---

# Regla Suprema

El Museo debe hacer sentir que el jugador está construyendo conocimiento, no llenando una lista.
