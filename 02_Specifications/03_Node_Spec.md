# HISTORIUM — NODE SPECIFICATION

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Specification

---

# Filosofía

Un nodo es la unidad jugable mínima de Historium.

No es una página.

No es una lección.

No es una tarjeta de contenido.

Es una escena de aprendizaje narrativo que transforma curiosidad en progreso del Museo.

Cada nodo debe entregar una micro-revelación histórica y una actualización visible del conocimiento del jugador.

---

# Objetivo

Definir cómo se crea, valida e importa un nodo para que funcione dentro de una campaña, actualice entidades del Museo y mantenga ritmo cinematográfico.

Un buen nodo debe poder responder tres preguntas:

- ¿Qué vive el jugador?
- ¿Qué entiende mejor?
- ¿Qué parte del Museo crece?

---

# Principios

- Todo nodo pertenece a una campaña y a un capítulo.
- Todo nodo debe actualizar al menos una entidad del Museo.
- Todo nodo debe tener tensión, descubrimiento o consecuencia.
- Todo nodo debe conectarse con entidades existentes o crear entidades nuevas justificadas.
- Todo nodo debe ser breve, claro y memorable.
- Todo nodo debe cerrar con progreso visible.

---

# Identidad YAML

```yaml
id: "greece_classical_ch01_n001"
type: "node"
title: "El problema de Atenas"
campaign: "greece_classical"
chapter: "ch01"
node_number: 1
duration: "3-5 min"
xp: 120
status: "draft | review | canon | archived"
version: "1.0.0"
museum_updates:
  - entity_id: "athens"
    progress: 5
relationships: []
assets: []
```

---

# Campos obligatorios

- `id`
- `type`
- `title`
- `campaign`
- `chapter`
- `node_number`
- `duration`
- `xp`
- `summary_short`
- `narrative_body`
- `museum_updates`
- `relationships`
- `version`

---

# Campos opcionales

- `period`
- `characters`
- `places`
- `concepts`
- `quiz`
- `curiosity`
- `visual_prompt`
- `audio_prompt`
- `map_reference`
- `reward_badge`
- `next_node`

---

# Museo

El nodo debe declarar actualizaciones del Museo.

Puede actualizar varias entidades al mismo tiempo.

Ejemplo:

```yaml
museum_updates:
  - entity_id: "pisistratus"
    gallery: "Characters"
    progress: 18
    unlocks:
      - "Relaciones"
      - "Cronología"
  - entity_id: "athens"
    gallery: "Cities"
    progress: 5
  - entity_id: "tyranny"
    gallery: "Concepts"
    progress: 10
```

El jugador debe sentir que estudió un mundo, no solo un tema.

---

# Relaciones

Todo nodo debe declarar sus conexiones principales.

Relaciones recomendadas:

- personaje protagonista,
- ciudad o región principal,
- concepto histórico central,
- evento asociado,
- documento o artefacto si aplica,
- siguiente nodo narrativo.

---

# Assets

Assets esperados:

- imagen principal o escena,
- miniatura,
- prompt visual,
- audio ambiente o narrativo,
- mapa si el nodo depende de ubicación,
- icono de recompensa si aplica.

Los assets deben reforzar memoria histórica.

No deben distraer del aprendizaje.

---

# Versionado

Todo nodo debe versionarse.

- `1.0.0` primera versión canon.
- `1.1.0` expansión narrativa o museística.
- `1.1.1` corrección menor.
- `2.0.0` cambio estructural del nodo.

---

# Checklist

- [ ] El nodo tiene una pregunta narrativa clara.
- [ ] Actualiza al menos una entidad del Museo.
- [ ] Incluye relaciones útiles.
- [ ] Tiene XP y duración definidos.
- [ ] Tiene assets o prompts esperados.
- [ ] Respeta voz y tono Historium.
- [ ] Conecta con el capítulo y la campaña.
- [ ] Está listo para importación.

---

# Plantilla base

````markdown
# NODO {{numero}} — {{titulo}}

**ID:** {{id}}
**Campaña:** {{campaña}}
**Capítulo:** {{capitulo}}
**Tipo:** {{tipo}}
**Duración:** {{duracion}}
**XP:** {{xp}}

---

# Metadatos

```yaml
id: {{id}}
campaign: {{campaign_id}}
chapter: {{chapter}}
node_number: {{numero}}
title: "{{titulo}}"
type: "{{tipo}}"
duration: "{{duracion}}"
xp: {{xp}}
period: "{{periodo}}"
characters:
  - {{personaje}}
places:
  - {{lugar}}
concepts:
  - {{concepto}}
rewards:
  character: "{{personaje_desbloqueado}}"
  relic: "{{reliquia}}"
  badge: "{{insignia}}"
next_node: "{{siguiente_nodo}}"
```
````

---

# Regla Suprema

Un nodo solo pertenece a Historium si convierte una escena histórica en crecimiento real del Museo Vivo.
