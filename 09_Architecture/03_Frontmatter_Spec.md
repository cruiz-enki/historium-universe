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

# Frontmatter universal

Todo archivo importable debe usar esta estructura base.

Los campos pueden estar vacíos durante `draft`, pero deben existir.

```yaml
---
id: "CHAR_000001"
type: "Character"
slug: "pisistratus"
title: "Pisístrato"
status: "draft"
version: "1.0.0"
canonical: false

museum:
  gallery: "Characters"
  default_level: 1
  max_level: 4
  unlockable: true

rarity: "common"
difficulty: "introductory"

created_at: "2026-07-05"
updated_at: "2026-07-05"

first_campaign: "CAMP_000001"
unlock_node: "NODE_000001"

tags:
  - "athens"
  - "tyranny"

relationships:
  - type: "governed"
    target: "CITY_000001"
    confidence: "high"
    visibility: "public"

sources:
  - type: "book"
    citation: ""
    url: ""

assets:
  image: ""
  audio: ""
  video: ""
  map: ""
  model_3d: ""
---
```

---

# Campos obligatorios

Todo archivo importable debe incluir:

- `id`
- `type`
- `slug`
- `title`
- `status`
- `version`
- `canonical`
- `museum`
- `rarity`
- `difficulty`
- `created_at`
- `updated_at`
- `first_campaign`
- `unlock_node`
- `tags`
- `relationships`
- `sources`
- `assets`

---

# Frontmatter específico por tipo

Estos ejemplos extienden el frontmatter universal.

No reemplazan los campos universales.

---

## Character

```yaml
type: "Character"
birth_date: ""
death_date: ""
birth_place: "CITY_000001"
primary_civilization: "CIV_000001"
roles:
  - "tyrant"
related_periods:
  - "archaic_greece"
```

---

## City

```yaml
type: "City"
region: "REG_000001"
modern_country: ""
founded_date: ""
coordinates:
  lat: null
  lng: null
primary_civilization: "CIV_000001"
```

---

## Battle

```yaml
type: "Battle"
war: "WAR_000001"
location: "LOC_000001"
date_start: ""
date_end: ""
belligerents:
  - "EMP_000001"
commanders:
  - "CHAR_000001"
result: ""
```

---

## Concept

```yaml
type: "Concept"
category: "political"
origin_period: ""
related_ideas:
  - "CON_000001"
modern_relevance: ""
```

---

## Document

```yaml
type: "Document"
author: "CHAR_000001"
created_in: "CITY_000001"
date_created: ""
language: "LANG_000001"
document_kind: "law | treaty | chronicle | inscription | letter | myth"
```

---

## Artifact

```yaml
type: "Artifact"
origin_place: "CITY_000001"
material: ""
current_location: "LOC_000001"
artifact_kind: "weapon | tool | ritual_object | coin | sculpture | vessel"
```

---

## Campaign

```yaml
type: "Campaign"
campaign_id: "CAMP_000001"
period: ""
primary_region: "REG_000001"
main_question: ""
chapters:
  - "CH_000001"
```

---

## Chapter

```yaml
type: "Chapter"
campaign_id: "CAMP_000001"
chapter_id: "CH_000001"
chapter_number: 1
nodes:
  - "NODE_000001"
chapter_question: ""
```

---

## Node

```yaml
type: "Node"
campaign_id: "CAMP_000001"
chapter_id: "CH_000001"
node_id: "NODE_000001"
node_number: 1
duration: "3-5 min"
xp: 120
museum_updates:
  - entity_id: "CHAR_000001"
    progress: 10
next_node: "NODE_000002"
```

---

# Definición de campos

## id

ID canónico asignado desde `03_Knowledge/REGISTRY.yaml`.

Formato:

```text
PREFIX_000001
```

---

## type

Tipo oficial de entidad, campaña, nodo, asset o estructura.

Debe coincidir con la taxonomía del Knowledge Graph.

---

## slug

Nombre técnico estable.

Usar `snake_case`, minúsculas y ASCII.

---

## title

Nombre visible para edición y producto.

Puede incluir acentos, espacios y nombre histórico correcto.

---

## status

Estado editorial.

```text
draft
review
canon
archived
deprecated
```

---

## version

Versión editorial del archivo.

Usar formato semántico:

```text
1.0.0
```

---

## canonical

Booleano.

Indica si el archivo ya pertenece al Canon Oficial.

```yaml
canonical: true
```

---

## museum

Define cómo se ubica la pieza en el Museo Vivo.

Debe incluir galería, niveles y desbloqueo.

---

## rarity

Rareza museística o de recompensa.

Valores sugeridos:

```text
common
uncommon
rare
epic
legendary
mythic
```

---

## difficulty

Dificultad cognitiva del contenido.

Valores sugeridos:

```text
introductory
intermediate
advanced
expert
```

---

## created_at / updated_at

Fechas editoriales en formato:

```text
YYYY-MM-DD
```

---

## first_campaign

Primera campaña donde la pieza aparece o se desbloquea.

Puede quedar vacío en entidades todavía no asignadas.

---

## unlock_node

Primer nodo que desbloquea la pieza para el jugador.

Puede quedar vacío si el desbloqueo aún no está definido.

---

## tags

Etiquetas editoriales para búsqueda interna, recomendaciones y agrupación.

No reemplazan relaciones del grafo.

---

## relationships

Relaciones tipificadas del Knowledge Graph.

Siempre deben apuntar a IDs.

Nunca a nombres visibles.

---

## sources

Fuentes históricas, curatoriales o editoriales.

Pueden estar incompletas en `draft`, pero deben completarse antes de `canon`.

---

## assets

Referencias a imagen, audio, video, mapa, modelo 3D u otros recursos.

Los assets deben aumentar comprensión.

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
