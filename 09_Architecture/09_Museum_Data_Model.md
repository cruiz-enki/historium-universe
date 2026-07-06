# HISTORIUM — MUSEUM DATA MODEL

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define cómo el Museo Vivo representa progreso, conocimiento y desbloqueos.

El Museo no es una lista de coleccionables.

Es la memoria personal del jugador dentro del Knowledge Graph.

---

# Niveles oficiales

## 0 — not_discovered

La entidad existe en el Canon.

El jugador aún no sabe que existe.

---

## 1 — discovered

El jugador sabe que existe.

Puede ver nombre, rareza, imagen básica y resumen corto.

---

## 2 — studied

El jugador entiende su función histórica.

Puede ver biografía, cronología, relaciones iniciales y campañas conectadas.

---

## 3 — mastered

El jugador comprende importancia, debates, consecuencias e influencia.

Puede ver relaciones avanzadas y contenido premium.

---

## 4 — mastery

El jugador domina el tema.

Puede desbloquear documentos, reconstrucciones, podcasts, mapas, comparaciones y certificado.

---

# Campos centrales

## progress_percent

Porcentaje de avance dentro de una entidad o colección.

Debe ir de `0` a `100`.

---

## unlocked_sections

Lista de secciones visibles para el jugador.

Ejemplos:

- summary
- timeline
- relationships
- debates
- sources
- reconstructions

---

## entity_level

Nivel numérico del 0 al 4.

---

## entity_state

Estado legible:

```text
not_discovered
discovered
studied
mastered
mastery
```

---

## museum_updates

Cambios generados por nodos, campañas o recompensas.

Ejemplo:

```yaml
museum_updates:
  - entity_id: "CHAR_000001"
    progress_delta: 12
    unlocked_sections:
      - "timeline"
      - "relationships"
```

---

## collection_progress

Progreso agregado por galería o colección.

Ejemplos:

- Characters
- Cities
- Battles
- Greece Classical
- Athenian Democracy

---

# Modelo por usuario y entidad

```yaml
user_id: "user_123"
entity_id: "CHAR_000001"
entity_level: 2
entity_state: "studied"
progress_percent: 46
unlocked_sections:
  - "summary"
  - "timeline"
  - "relationships"
collection_progress:
  Characters: 8
  Greece_Classical: 21
```

---

# Regla Suprema

El Museo debe hacer visible el crecimiento del conocimiento, no solo el consumo de contenido.
