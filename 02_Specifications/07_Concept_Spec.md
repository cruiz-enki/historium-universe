# HISTORIUM — CONCEPT SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Entity Specification

---

# Filosofía

Los conceptos son el conocimiento más valioso de Historium.

Las personas cambian.

Los imperios desaparecen.

Las ciudades evolucionan.

Pero las ideas viajan durante siglos.

Historium no quiere que el jugador memorice la palabra "democracia".

Quiere que comprenda cómo nació, cómo evolucionó y por qué sigue existiendo.

---

# Objetivo

Todo concepto debe responder seis preguntas.

¿Qué es?

¿Por qué surgió?

¿Qué problema resolvía?

¿Cómo evolucionó?

¿Dónde volvió a aparecer?

¿Por qué sigue siendo importante?

---

# Principios

Un concepto existe una sola vez dentro del Universo Historium.

Nunca se duplica.

Puede aparecer en cientos de campañas.

Siempre será la misma entidad.

---

# Identidad

```yaml
id:
slug:
type:
status:
version:
created_at:
updated_at:
```

---

# Identificación

Ejemplo.

```yaml
id: CONCEPT_000001

slug: democracy

type: Concept
```

---

# Información principal

Nombre

Nombre original

Idioma original

Pronunciación

Categoría

---

# Categorías

Todo concepto pertenece a una categoría.

Ejemplos.

Política

Economía

Filosofía

Religión

Sociedad

Militar

Ciencia

Arte

Arquitectura

Derecho

Tecnología

Cultura

---

# Resumen

150–250 caracteres.

Debe responder inmediatamente.

¿Por qué este concepto cambió la Historia?

Ejemplo.

La democracia fue una forma de organización política nacida en Atenas que permitió a los ciudadanos participar directamente en el gobierno de su ciudad.

---

# Definición

Debe existir una definición clara.

Nunca excesivamente académica.

Debe entenderla cualquier persona.

---

# El problema

Todo concepto nace para resolver algo.

Debe responder.

¿Qué problema existía antes?

Ejemplo.

Democracia.

↓

Concentración del poder.

---

# Origen

¿Dónde apareció?

¿Cuándo apareció?

¿Quiénes participaron?

¿Qué circunstancias lo hicieron posible?

---

# Evolución

Debe dividirse en etapas.

Ejemplo.

Nacimiento

↓

Primer desarrollo

↓

Expansión

↓

Transformación

↓

Estado actual

Nunca un solo bloque.

---

# Línea del tiempo

Toda idea posee historia.

Ejemplo.

508 a.C.

↓

Roma

↓

Ilustración

↓

Revolución Francesa

↓

Constituciones modernas

---

# Relaciones

Los conceptos siempre están conectados.

Ejemplo.

Democracia

↓

Ciudadanía

↓

República

↓

Constitución

↓

Estado

↓

Derechos Humanos

---

# Conceptos relacionados

Relacionados únicamente mediante IDs.

Nunca texto libre.

---

# Personajes relacionados

Quienes crearon.

Defendieron.

Criticaron.

Transformaron.

Popularizaron.

---

# Ciudades relacionadas

Donde surgió.

Donde evolucionó.

Donde desapareció.

---

# Documentos relacionados

Constituciones.

Leyes.

Tratados.

Manifiestos.

---

# Eventos relacionados

Revoluciones.

Guerras.

Reformas.

Descubrimientos.

---

# Campañas

Todas las campañas donde aparece.

---

# Museo

## Nivel 1

Descubierto

Desbloquea.

Nombre

Definición corta

Origen

Resumen

---

## Nivel 2

Estudiado

Desbloquea.

Historia

Línea temporal

Relaciones

Ejemplos

---

## Nivel 3

Dominado

Desbloquea.

Debates

Malentendidos comunes

Comparaciones

Influencias

---

## Nivel 4

Maestría

Desbloquea.

Documentos originales

Bibliografía

Podcast

Comparaciones modernas

Mapa conceptual completo

---

# Evolución histórica

Todo concepto debe responder.

¿Cómo cambió con el paso del tiempo?

Ejemplo.

La democracia ateniense.

↓

República romana.

↓

Democracias modernas.

El jugador debe entender que las ideas evolucionan.

---

# Aplicaciones

¿Dónde se utilizó?

¿Dónde fracasó?

¿Dónde sigue existiendo?

---

# Malentendidos comunes

Todo concepto debe desmontar ideas erróneas.

Ejemplo.

Democracia.

↓

No todos podían votar en Atenas.

---

# Curiosidades

Mínimo.

10

Nunca repetir el nodo.

Siempre ampliar.

---

# Debates

Toda idea importante tiene debates.

Ejemplo.

¿Nació realmente en Atenas?

¿Existieron formas anteriores?

¿Qué diferencias tenía con la democracia moderna?

---

# Legado

Debe responder.

¿Qué cambió gracias a esta idea?

---

# Comparación moderna

Todo concepto debe conectarse con la actualidad.

Ejemplo.

La ciudadanía ateniense.

↓

Ciudadanía contemporánea.

Siempre aclarando diferencias.

Nunca simplificando.

---

# Assets

Mapa conceptual

Infografía

Timeline

Carta

Hero

Diagrama

Miniatura

Wallpaper

Animación

---

# Audio

Narración

Pronunciación

Explicación resumida

Podcast

---

# Datos del Universo

```yaml
rarity:

difficulty:

museum_max_level:

estimated_learning_time:

unlock_node:

first_campaign:
```

---

# Estadísticas

Campañas

Personajes relacionados

Ciudades

Documentos

Eventos

Civilizaciones

Imperios

Conceptos conectados

---

# Versionado

Toda modificación genera una nueva versión.

Nunca se elimina conocimiento.

---

# Checklist

□ Tiene definición clara

□ Tiene origen

□ Tiene evolución

□ Tiene relaciones

□ Tiene contexto

□ Tiene debates

□ Tiene comparación moderna

□ Tiene assets

□ Alimenta el Museo

Si alguna respuesta es "No"...

El concepto todavía no pertenece al Universo Historium.

---

# Regla Suprema

Los personajes hacen la Historia.

Las ideas la sobreviven.

Historium debe enseñar ambas.

Pero el verdadero objetivo es que el jugador comprenda cómo las ideas nacen, cambian y siguen influyendo miles de años después.

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
