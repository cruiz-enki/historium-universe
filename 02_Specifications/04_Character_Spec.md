# HISTORIUM — CHARACTER SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Entity Specification

---

# Filosofía

Los personajes son el corazón de Historium.

No son únicamente personas.

Son motores del cambio.

Cada personaje representa decisiones, conflictos, ideas y consecuencias que modificaron el rumbo de la Historia.

Historium no colecciona nombres.

Colecciona vidas.

---

# Objetivo

Todo personaje debe responder cuatro preguntas.

¿Quién fue?

¿Qué quería?

¿Qué hizo?

¿Por qué sigue siendo importante?

Si alguna no puede responderse...

el personaje todavía no está listo.

---

# Principios

Cada personaje existe una sola vez dentro del Universo Historium.

Nunca se duplica.

Puede aparecer en cientos de campañas.

Pero solamente existe una entidad oficial.

---

# Identidad

Toda entidad Character debe contener.

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
id: CHAR_000001

slug: pisistratus

type: Character
```

El ID nunca cambia.

El nombre puede actualizarse.

El ID jamás.

---

# Información principal

Nombre completo

Nombre original

Apodos

Títulos

Pronunciación

Nombre en idioma original

Nombre latinizado

Nombre moderno (si aplica)

---

# Resumen

Resumen corto.

150–250 caracteres.

Debe responder.

¿Por qué importa?

Ejemplo.

Pisístrato fue un gobernante ateniense que, pese a llegar al poder como tirano, preparó el terreno para el nacimiento de la democracia.

---

# Biografía

Debe dividirse en.

Infancia

Juventud

Ascenso

Momento decisivo

Máximo poder

Declive

Muerte

Legado

No escribir un texto continuo.

Cada etapa debe poder desbloquearse de forma independiente.

---

# Cronología

Debe existir una línea temporal.

Nacimiento

Eventos importantes

Muerte

Consecuencias

Siempre en orden cronológico.

---

# Fechas

```yaml
birth:

death:

birth_precision:

death_precision:
```

La precisión puede ser.

Exacta

Aproximada

Desconocida

Debatida

---

# Ubicación

Lugar de nacimiento

Lugar de muerte

Lugar donde desarrolló su actividad

Regiones recorridas

Mapa de movimientos

---

# Contexto histórico

Todo personaje debe explicar.

¿Qué estaba ocurriendo en el mundo cuando apareció?

Nunca estudiar personajes aislados.

---

# Motivaciones

¿Qué buscaba?

Poder.

Riqueza.

Fe.

Libertad.

Conquista.

Supervivencia.

Conocimiento.

Debe existir al menos una motivación dominante.

---

# Personalidad

No psicológica.

Histórica.

Debe responder.

¿Cómo lo describen las fuentes?

Ejemplo.

Carismático.

Pragmático.

Impulsivo.

Calculador.

Visionario.

---

# Relaciones

Toda relación utiliza el sistema oficial.

Ejemplo.

Padre de

Hijo de

Esposo de

Aliado de

Enemigo de

Mentor de

Discípulo de

Inspiró a

Fue influenciado por

Gobernó junto a

Nunca texto libre.

---

# Campañas

Debe listar todas las campañas donde participa.

Ejemplo.

Grecia Clásica

Alejandro Magno

Democracia

Historia Política

---

# Capítulos

Debe listar todos los capítulos donde aparece.

---

# Nodos

Debe listar todos los nodos donde participa.

---

# Entidades relacionadas

Ciudades

Conceptos

Batallas

Imperios

Religiones

Monumentos

Documentos

Reliquias

Civilizaciones

---

# Museo

El personaje posee cuatro niveles.

---

## Nivel 1

Descubierto

Desbloquea.

Retrato

Resumen

Fechas

Rareza

---

## Nivel 2

Estudiado

Desbloquea.

Biografía

Cronología

Mapa

Relaciones

---

## Nivel 3

Dominado

Desbloquea.

Curiosidades Premium

Debates

Influencias

Legado

Fuentes

---

## Nivel 4

Maestría

Desbloquea.

Documentos originales

Reconstrucciones

Modelos

Podcast

Bibliografía

Certificado

---

# Curiosidades

Mínimo.

10

Ideal.

15

Máximo.

Sin límite.

Nunca repetir información del nodo.

---

# Debates históricos

Todo personaje debe indicar.

¿Existe consenso?

¿Qué aspectos son debatidos?

¿Qué dicen las principales corrientes?

Nunca ocultar la incertidumbre.

---

# Fuentes

Clasificadas.

Fuentes primarias

Fuentes secundarias

Museos

Artículos

Libros

Documentales

Nunca inventar referencias.

---

# Frases

Debe incluir.

Frases auténticas.

Frases atribuidas.

Frases famosas.

Frases falsas populares.

Siempre indicando el nivel de certeza.

---

# Legado

Debe responder.

¿Qué cambió después de él?

No resumir su vida.

Resumir su impacto.

---

# Interpretaciones

¿Cómo fue visto por distintas épocas?

Ejemplo.

Antigüedad

Edad Media

Renacimiento

Historiografía moderna

Esto ayuda a entender cómo cambia la percepción histórica.

---

# Representación visual

Assets obligatorios.

Portrait

Hero

Card

Full Body

Bust

Silhouette

Museum

Loading

Wallpaper

Thumbnail

---

# Audio

Narración

Pronunciación

Frases célebres

Música asociada (si aplica)

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

No son RPG.

Son históricas.

Ejemplo.

Periodo

Civilización

Área de influencia

Años de actividad

Campañas

Nodos

Relaciones

Documentos

Batallas

Ciudades

---

# Versionado

Toda modificación genera nueva versión.

Nunca se sobrescribe la historia.

Ejemplo.

v1.0

↓

v1.1

↓

v2.0

El historial permanece.

---

# Checklist

Antes de aprobar un personaje.

□ Tiene ID único.

□ Posee cronología.

□ Posee relaciones.

□ Tiene contexto.

□ Tiene legado.

□ Tiene curiosidades.

□ Tiene debates.

□ Tiene assets.

□ Alimenta el Museo.

□ Puede reutilizarse en otras campañas.

Si alguna respuesta es "No"...

el personaje todavía no pertenece al Universo Historium.

---

# Regla Suprema

Un personaje no es importante por la cantidad de batallas que ganó.

Es importante por la huella que dejó en la Historia.

Historium siempre estudia personas.

Nunca únicamente acontecimientos.

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
