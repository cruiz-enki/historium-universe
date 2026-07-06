# HISTORIUM — SUPABASE MODEL

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define el modelo conceptual de Supabase para Historium.

GitHub contiene el Canon Oficial.

Supabase contiene el estado activo del producto y el progreso del usuario.

---

# Separación crítica

Supabase no decide qué es canon.

Supabase ejecuta el canon.

---

# Tablas conceptuales

## canon_entities

Entidades importadas desde Markdown.

Campos sugeridos:

- `id`
- `type`
- `title`
- `slug`
- `status`
- `version`
- `museum_gallery`
- `source_path`

---

## canon_relationships

Relaciones importadas del Knowledge Graph.

Campos sugeridos:

- `id`
- `relationship_type`
- `source_id`
- `target_id`
- `visibility`
- `intensity`
- `evidence_note`
- `status`

---

## campaigns

Campañas publicadas.

Campos sugeridos:

- `id`
- `title`
- `slug`
- `period`
- `status`
- `version`

---

## chapters

Capítulos dentro de campañas.

---

## nodes

Escenas jugables que actualizan Museo.

Campos clave:

- `id`
- `campaign_id`
- `chapter_id`
- `node_number`
- `xp`
- `duration`
- `museum_updates`

---

## user_museum_entities

Estado del Museo por usuario y entidad.

Campos clave:

- `user_id`
- `entity_id`
- `discovery_state`
- `knowledge_level`
- `progress_percent`
- `last_updated_at`

---

## user_relationship_unlocks

Relaciones visibles para cada usuario.

Permite relaciones ocultas desbloqueables.

---

## user_node_progress

Registra avance de nodos.

---

# Importación

El importer debe guardar:

- ruta fuente,
- hash del archivo,
- versión canon,
- fecha de importación,
- estado de validación.

---

# Regla Suprema

Supabase debe hacer jugable el Canon sin reemplazarlo.
