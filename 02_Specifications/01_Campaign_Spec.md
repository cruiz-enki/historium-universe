# HISTORIUM — CAMPAIGN SPECIFICATION

**Versión:** 1.0  
**Estado:** Oficial

---

# Filosofía

Una campaña no es una lista de lecciones.

Una campaña es una aventura histórica completa.

Debe tener ritmo de serie premium:

- inicio poderoso,
- capítulos claros,
- tensión creciente,
- personajes memorables,
- decisiones históricas,
- desbloqueos del Museo,
- final satisfactorio,
- conexión con futuras campañas.

---

# Qué es una campaña

Una campaña es una experiencia narrativa compuesta por capítulos y nodos.

Cada campaña debe responder una gran pregunta histórica.

Ejemplos:

## Grecia Clásica

¿Cómo nació la idea de que los ciudadanos podían gobernarse a sí mismos?

## Imperio Romano

¿Cómo una ciudad conquistó el Mediterráneo y luego fue devorada por su propio poder?

## Egipto Faraónico

¿Cómo una civilización construyó una idea de eternidad que sobrevivió milenios?

---

# Estructura oficial

Toda campaña contiene:

1. Ficha de campaña
2. Pregunta central
3. Promesa narrativa
4. Capítulos
5. Nodos
6. Entidades introducidas
7. Entidades actualizadas
8. Recompensas del Museo
9. Línea temporal
10. Mapa de campaña
11. Final de campaña
12. Conexiones futuras

---

# Ficha de campaña

Cada campaña debe tener:

```yaml
id: CAMP_GREECE_CLASSICAL
title: Grecia Clásica
subtitle: El nacimiento del mundo occidental
type: civilization
period: 800–323 a.C.
difficulty: Básico
estimated_nodes: 40
estimated_duration: 12–15 horas
main_question: "¿Cómo una tierra dividida creó ideas que cambiaron el mundo?"
status: in_progress
Capítulos

Una campaña se divide en capítulos.

Cada capítulo representa una transformación histórica.

Ejemplo:

Grecia Clásica
Capítulo 1 — El mundo antes de Grecia

Nacimiento de las polis.

Capítulo 2 — Atenas despierta

Solón, Pisístrato y Clístenes.

Capítulo 3 — Persia amenaza al mundo griego

Guerras Médicas.

Capítulo 4 — La Edad de Oro

Pericles, arte, filosofía y democracia.

Capítulo 5 — Grecia se destruye a sí misma

Guerra del Peloponeso.

Capítulo 6 — El camino hacia Alejandro

Macedonia y el fin de la polis clásica.

Nodos

El nodo es la unidad jugable principal.

Cada nodo debe contener:

Historia principal
Actualizaciones del Museo
Curiosidades
Quiz
Decisión histórica
Recompensas
Prompts visuales
Conexión con el siguiente nodo

Duración ideal:

15–20 minutos
Tipos de nodo
Historia
Biografía
Batalla
Ciudad
Civilización
Concepto
Cultura
Religión
Economía
Política
Exploración
Misterio
What If
Final de capítulo
Final de campaña
Entidades

Cada nodo debe declarar qué entidades toca.

Ejemplo:

entities_introduced:
  - CHAR_PISISTRATUS
  - ARTIFACT_STAFF_OF_TYRANT

entities_updated:
  - CITY_ATHENS
  - CONCEPT_TYRANNY
  - CONCEPT_DEMOCRACY
  - LOCATION_ACROPOLIS
Actualizaciones del Museo

Cada nodo debe indicar qué cambia en el Museo del jugador.

Ejemplo:

museum_updates:
  - entity: CHAR_PISISTRATUS
    level_change: 0 → 2
    progress_added: 35
    unlocked_sections:
      - Retrato
      - Biografía inicial
      - Cronología
      - Relaciones políticas

  - entity: CONCEPT_TYRANNY
    level_change: 0 → 1
    progress_added: 20
    unlocked_sections:
      - Definición histórica
      - Diferencia con uso moderno

  - entity: CITY_ATHENS
    level_change: 1 → 2
    progress_added: 8
    unlocked_sections:
      - Acrópolis
      - Facciones políticas
Regla de introducción de entidades

Un nodo no debe introducir demasiadas entidades nuevas.

Ideal:

1–2 personajes nuevos
1 concepto principal
1–3 lugares
1 reliquia o documento

Si se introducen demasiadas entidades, el jugador se satura.

Ritmo narrativo de campaña

Cada campaña debe alternar tipos de nodo.

Ejemplo:

Nodo 1 — Apertura cinematográfica
Nodo 2 — Contexto histórico
Nodo 3 — Personaje clave
Nodo 4 — Crisis
Nodo 5 — Batalla o decisión
Nodo 6 — Consecuencias
Nodo 7 — Cultura o vida cotidiana
Nodo 8 — Nuevo personaje
Nodo 9 — Giro histórico
Nodo 10 — Final de capítulo
Final de capítulo

Cada capítulo debe terminar con:

una transformación histórica clara,
una recompensa importante,
una decisión histórica fuerte,
una conexión al siguiente capítulo.

Nunca debe sentirse como un corte arbitrario.

Final de campaña

El final de campaña debe cerrar la gran pregunta inicial.

Debe incluir:

resumen emocional,
legado histórico,
entidades dominadas,
museo actualizado,
recompensa especial,
teaser de la siguiente campaña.

Ejemplo:

Has completado Grecia Clásica.

Pero la historia no termina aquí.

Mientras las polis griegas se debilitan...

un reino del norte observa.

Macedonia está lista para cambiar el mundo.
Recompensas de campaña

Al completar una campaña pueden desbloquearse:

Título especial
Insignia legendaria
Reliquia única
Banner de perfil
Galería completa
Mapa final
Certificado de maestría
Campaña conectada

Ejemplo:

campaign_completion_rewards:
  title: Guardián de Grecia
  badge: La Llama de Atenas
  artifact: Corona de Laurel Helénica
  unlocks:
    - Campaña Alejandro Magno
    - Modo Cronología de Grecia
Campañas conectadas

Toda campaña debe conectar con otras.

Ejemplo:

connects_to:
  - Alejandro Magno
  - Imperio Romano
  - Democracia
  - Persia
  - Filosofía Antigua

Historium nunca debe sentirse como campañas separadas.

Debe sentirse como un universo.

Regla de oro

Una campaña no está terminada cuando tiene todos sus nodos.

Está terminada cuando:

cuenta una historia completa,
alimenta el Museo,
actualiza entidades,
genera curiosidad,
desbloquea nuevas rutas,
y deja al jugador con ganas de seguir explorando.

---

# Arquitectura Canónica

Esta especificación forma parte del Canon Oficial de Historium.

Debe mantener compatibilidad con el Museo, el Grafo Histórico, el pipeline de importación y las campañas narrativas.

---

# Identidad YAML

```yaml
id: "example_id"
type: "spec_type"
name: "Nombre oficial"
status: "draft | review | canon | archived"
version: "1.0.0"
museum_gallery: "Museum Gallery"
relationships: []
assets: []
```

---

# Campos obligatorios

- `id`
- `type`
- `name`
- `summary_short`
- `summary_long`
- `museum_gallery`
- `relationships`
- `version`

---

# Campos opcionales

- `alternate_names`
- `period`
- `date_start`
- `date_end`
- `visual_prompt`
- `audio_prompt`
- `map_reference`
- `premium_unlocks`
- `related_campaigns`

---

# Assets

Todo asset debe explicar, ubicar o intensificar el contenido.

No se aceptan assets decorativos sin función narrativa o museística.

---

# Versionado

Todo cambio relevante debe actualizar versión y nota editorial.

El Canon debe poder rastrear por qué cambió una entidad, nodo, campaña o documento.

---

# Objetivo

Establecer una regla de producción clara para que este contenido pueda escribirse, revisarse, importarse y expandirse sin perder coherencia con el Canon Oficial.

---

# Principios

- Debe alimentar el Museo Vivo.
- Debe conectarse con el Grafo Histórico.
- Debe poder vivir fuera de una sola campaña.
- Debe sostener expansión futura.
- Debe mantener tono premium, claro y cinematográfico.

---

# Museo

Toda pieza producida con esta especificación debe declarar qué parte del Museo hace crecer.

Debe indicar si desbloquea descubrimiento, estudio, dominio o maestría.

---

# Relaciones

Toda pieza debe conectarse con entidades, campañas, lugares, conceptos o assets relacionados.

Las relaciones deben tener propósito histórico, no solo navegación.

---

# Checklist

- [ ] Tiene identidad única.
- [ ] Hace crecer el Museo.
- [ ] Incluye relaciones útiles.
- [ ] Respeta voz y tono Historium.
- [ ] Puede importarse sin ambigüedad.
- [ ] Está listo para revisión editorial.

---

# Regla Suprema

Si esta pieza no aumenta comprensión histórica dentro del Museo Vivo, debe rediseñarse antes de entrar al Canon.
