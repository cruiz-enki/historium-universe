# HISTORIUM — CHAPTER SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Specification

---

# Filosofía

Un capítulo representa una transformación histórica.

No existe porque el contenido sea demasiado largo.

Existe porque la Historia ha cambiado.

Cuando termina un capítulo, el mundo ya no es el mismo que al comenzar.

---

# Objetivo

Cada capítulo debe responder una gran pregunta.

Ejemplo.

¿Cómo pasó Atenas de ser una ciudad dividida a convertirse en el laboratorio político del mundo?

Los nodos responderán preguntas más pequeñas.

El capítulo responde la gran transformación.

---

# Duración

Duración ideal.

45 a 120 minutos.

Dependiendo del tema.

Nunca dividir únicamente por cantidad de nodos.

---

# Número de nodos

Ideal.

4 a 8 nodos.

Máximo recomendado.

10 nodos.

Si necesita más...

Probablemente deban existir dos capítulos.

---

# Estructura oficial

Todo capítulo contiene.

• Introducción

• Objetivo

• Estado inicial

• Transformación

• Nodos

• Entidades introducidas

• Entidades evolucionadas

• Museo

• Recompensa

• Cliffhanger

---

# Introducción

Debe responder.

¿Qué está ocurriendo al comenzar este capítulo?

Debe recordar brevemente el capítulo anterior.

Nunca resumir demasiado.

---

# Objetivo

Una sola frase.

Ejemplo.

Comprender cómo las reformas políticas prepararon el nacimiento de la democracia.

---

# Estado inicial

Describe el mundo al iniciar.

Ejemplo.

Atenas vive una profunda crisis política.

Las familias aristocráticas compiten por el poder.

Los campesinos exigen cambios.

---

# Transformación

Describe cómo cambiará el mundo.

Ejemplo.

Al terminar este capítulo...

Atenas tendrá un nuevo equilibrio político.

---

# Tipos de nodo recomendados

Todo capítulo debe combinar diferentes experiencias.

Ejemplo.

Nodo 1

Historia

Nodo 2

Biografía

Nodo 3

Ciudad

Nodo 4

Concepto

Nodo 5

Evento

Nodo 6

Consecuencias

Nunca repetir demasiados nodos del mismo tipo.

---

# Ritmo emocional

Todo capítulo debe seguir una curva.

Inicio

↓

Descubrimiento

↓

Conflicto

↓

Escalada

↓

Clímax

↓

Consecuencias

↓

Reflexión

↓

Cliffhanger

---

# Introducción de entidades

Un capítulo puede introducir.

2–6 personajes.

2–5 conceptos.

1–3 ciudades.

1–2 reliquias.

1 documento.

Varias relaciones.

No saturar.

---

# Evolución del Museo

Todo capítulo debe producir crecimiento visible.

Ejemplo.

Personajes.

+4

Conceptos.

+3

Ciudades.

+2

Reliquias.

+1

Colecciones.

+1

El jugador debe sentir progreso importante.

---

# Pregunta del capítulo

Toda introducción debe plantear una pregunta.

Todo final debe responderla.

Pero generar otra.

Ejemplo.

Pregunta inicial.

¿Quién conseguirá controlar Atenas?

Pregunta final.

Ahora que Atenas cambió...

¿Podrá sobrevivir a Persia?

---

# Recompensa de capítulo

Todo capítulo debe entregar una recompensa importante.

Ejemplos.

Nueva colección.

Nueva galería.

Título.

Insignia.

Mapa.

Personaje épico.

Nunca solamente XP.

---

# Resumen del capítulo

Al finalizar.

Historium recuerda.

Qué ocurrió.

Qué cambió.

Qué aprendimos.

Qué conexiones aparecieron.

No debe durar más de un minuto.

---

# Conexión con el siguiente capítulo

Todo capítulo termina generando expectativa.

Ejemplo.

Los griegos resolvieron sus conflictos internos.

Ahora deberán enfrentarse al mayor imperio del planeta.

---

# Actualización del Museo

Cada capítulo debe mostrar.

══════════════════════

Museo actualizado

+4 Personajes

+3 Conceptos

+2 Ciudades

+1 Reliquia

+18 Relaciones

══════════════════════

El crecimiento debe sentirse importante.

---

# Checklist de validación

Antes de aprobar un capítulo responder.

□ ¿Existe una transformación clara?

□ ¿Hay una pregunta central?

□ ¿Los nodos cuentan una misma historia?

□ ¿El Museo crece de forma significativa?

□ ¿Se introducen nuevas entidades?

□ ¿Se profundiza en entidades anteriores?

□ ¿Existe un clímax?

□ ¿El final conecta naturalmente con el siguiente capítulo?

Si alguna respuesta es "No"...

El capítulo aún no está listo.

---

# Ejemplo

## Campaña

Grecia Clásica

---

## Capítulo 2

Atenas despierta

---

Pregunta.

¿Cómo encontró Atenas una nueva forma de gobernarse?

---

Estado inicial.

Crisis política.

---

Estado final.

Democracia en construcción.

---

Nodos.

GRC-006

GRC-007

GRC-008

GRC-009

GRC-010

---

Personajes.

Solón

Pisístrato

Clístenes

---

Conceptos.

Tiranía

Ciudadanía

Democracia

---

Recompensa.

Título.

"Arquitecto de Atenas"

---

Próximo capítulo.

Las Guerras Médicas.

---

# Regla Suprema

Un nodo cambia una historia.

Un capítulo cambia una etapa.

Una campaña cambia una civilización.

Nunca confundir esos niveles.

Cada uno debe sentirse claramente diferente para el jugador.

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
