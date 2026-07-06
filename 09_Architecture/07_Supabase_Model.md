# HISTORIUM — SUPABASE MODEL

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define el modelo conceptual de Supabase para Historium.

No es SQL todavía.

Es el mapa de responsabilidades de datos para convertir el Canon en experiencia activa.

---

# Separación crítica

GitHub contiene el Canon Oficial.

Supabase contiene:

- contenido importado,
- estado activo,
- progreso de usuario,
- desbloqueos del Museo,
- recompensas,
- perfiles.

Supabase no decide qué es canon.

Supabase ejecuta el canon.

---

# Modelo conceptual

## entities

Contiene entidades importadas desde `03_Knowledge`.

Ejemplos:

- Character
- City
- Battle
- Concept
- Document
- Artifact
- Civilization

Campos conceptuales:

- `id`
- `type`
- `slug`
- `title`
- `status`
- `version`
- `canonical`
- `museum_gallery`
- `source_path`

---

## relationships

Contiene conexiones tipificadas del Knowledge Graph.

Campos conceptuales:

- `relationship_type`
- `source_id`
- `target_id`
- `visibility`
- `intensity`
- `confidence`
- `evidence_note`
- `version`

---

## campaigns

Experiencias narrativas oficiales.

Una campaña recorre una parte del grafo.

---

## chapters

Bloques narrativos dentro de campañas.

Organizan el ritmo de aprendizaje.

---

## nodes

Escenas jugables.

Actualizan Museo, XP, relaciones visibles y progreso.

---

## quizzes

Preguntas asociadas a nodos, entidades o campañas.

Nunca deben existir como trivia aislada.

---

## curiosities

Piezas breves de descubrimiento.

Pueden desbloquearse por nivel de Museo o por nodo.

---

## assets

Imágenes, audio, video, mapas, modelos 3D y referencias visuales.

Deben apuntar a entidades, nodos o campañas.

---

## museum_unlocks

Reglas que indican qué se desbloquea, cuándo y por qué.

Ejemplos:

- nueva entidad,
- nueva sección,
- nueva relación,
- nuevo asset,
- nuevo badge.

---

## user_museum_progress

Estado personal del Museo de cada usuario.

Guarda progreso por entidad.

---

## user_node_progress

Registra nodos completados, XP, respuestas y timestamps.

---

## user_campaign_progress

Registra avance por campaña, capítulo y arco.

---

## rewards

Define recompensas visibles:

- XP,
- badges,
- títulos,
- reliquias,
- desbloqueos,
- certificados.

---

## profiles

Información del jugador.

No pertenece al Canon.

Sirve para experiencia personalizada.

---

# Regla Suprema

Supabase debe hacer jugable el Canon sin reemplazarlo.
