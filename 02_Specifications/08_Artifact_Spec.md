# HISTORIUM — ARTIFACT SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Entity Specification

---

# Filosofía

Un artefacto no es únicamente un objeto.

Es un testigo de la Historia.

Cada arma.

Cada moneda.

Cada corona.

Cada tablilla.

Cada estatua.

Cada herramienta.

Nos cuenta algo sobre quienes la fabricaron.

Historium estudia los objetos como evidencia del pasado.

No únicamente como piezas de museo.

---

# Objetivo

Todo artefacto debe responder seis preguntas.

¿Qué es?

¿Quién lo creó?

¿Para qué servía?

¿Por qué fue importante?

¿Cómo llegó hasta nosotros?

¿Qué nos permite comprender hoy?

---

# Principios

Todo artefacto existe una sola vez dentro del Universo Historium.

Nunca se duplica.

Puede aparecer en múltiples campañas.

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
id: ART_000001

slug: staff-of-pisistratus

type: Artifact
```

---

# Información principal

Nombre

Nombre original

Otros nombres

Idioma original

Pronunciación

Categoría

---

# Categorías

Todo artefacto pertenece a una categoría.

Ejemplos.

Arma

Armadura

Corona

Insignia

Herramienta

Documento físico

Moneda

Joya

Escultura

Objeto ceremonial

Instrumento

Mobiliario

Vehículo

Vestimenta

Tecnología

---

# Resumen

150–250 caracteres.

Debe responder.

¿Por qué este objeto es importante?

Ejemplo.

La Piedra de Rosetta permitió descifrar los jeroglíficos egipcios y revolucionó el estudio del Antiguo Egipto.

---

# Descripción

Debe describir.

Aspecto.

Uso.

Importancia.

Nunca limitarse al aspecto físico.

---

# Materiales

Debe indicar.

Piedra

Bronce

Hierro

Oro

Plata

Madera

Papiro

Arcilla

Cuero

Marfil

Tela

Cerámica

Etc.

---

# Dimensiones

Cuando existan.

Altura

Ancho

Peso

Longitud

Diámetro

---

# Fabricación

¿Quién lo creó?

¿Cómo se fabricó?

¿Qué tecnología requería?

¿Cuánto tiempo tomaba producirlo?

---

# Uso

¿Para qué servía?

Uso cotidiano.

Uso militar.

Uso ceremonial.

Uso religioso.

Uso político.

Uso económico.

---

# Contexto histórico

¿Qué estaba ocurriendo cuando apareció?

¿Por qué fue creado?

¿Qué necesidad resolvía?

---

# Historia del artefacto

Debe dividirse.

Creación

↓

Uso

↓

Pérdida

↓

Descubrimiento

↓

Estado actual

---

# Descubrimiento

Si aplica.

¿Cuándo fue encontrado?

¿Quién lo descubrió?

¿Dónde apareció?

¿Cómo cambió nuestro conocimiento?

---

# Estado actual

Debe indicar.

Museo

Colección

Ubicación

Si desapareció

Si fue destruido

Si existen réplicas

---

# Propietarios históricos

Relacionados mediante IDs.

Ejemplo.

CHAR_000001

EMP_000003

ORG_000007

---

# Ubicaciones

Debe indicar.

Dónde fue creado.

Dónde fue utilizado.

Dónde fue encontrado.

Dónde se conserva.

---

# Entidades relacionadas

Personajes

Ciudades

Imperios

Civilizaciones

Conceptos

Batallas

Documentos

Monumentos

---

# Campañas

Lista completa.

---

# Museo

## Nivel 1

Descubierto

Desbloquea.

Imagen

Nombre

Material

Resumen

---

## Nivel 2

Estudiado

Desbloquea.

Historia

Uso

Fabricación

Contexto

---

## Nivel 3

Dominado

Desbloquea.

Curiosidades

Comparaciones

Debates

Reconstrucciones

---

## Nivel 4

Maestría

Desbloquea.

Modelo 3D

Visor 360°

Podcast

Bibliografía

Galería completa

---

# Curiosidades

Mínimo.

10

Siempre complementan.

Nunca repiten.

---

# Debates

Debe indicar.

Autenticidad.

Origen.

Datación.

Propietarios.

Interpretaciones.

---

# Conservación

Estado físico.

Restauraciones.

Material perdido.

Partes originales.

Réplicas.

---

# Legado

Debe responder.

¿Qué aprendimos gracias a este objeto?

¿Cómo cambió nuestra comprensión histórica?

---

# Assets

Fotografía

Reconstrucción

Modelo 3D

Carta

Hero

Detalle

Animación

Miniatura

Wallpaper

---

# Audio

Pronunciación

Narración

Historia

Descripción

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

Antigüedad

Materiales

Civilizaciones

Imperios

Campañas

Personajes

Conceptos

Museos

---

# Versionado

Toda modificación genera una nueva versión.

Nunca se elimina información.

---

# Checklist

□ Tiene contexto

□ Tiene historia

□ Tiene materiales

□ Tiene uso

□ Tiene ubicación

□ Tiene propietarios

□ Tiene legado

□ Tiene assets

□ Alimenta el Museo

Si alguna respuesta es "No"...

El artefacto todavía no pertenece al Universo Historium.

---

# Regla Suprema

Un artefacto no vale por el material del que está hecho.

Vale por la historia que conserva.

Historium estudia los objetos porque cada uno es una evidencia de cómo vivieron, pensaron y construyeron las civilizaciones.

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

# Relaciones

Toda pieza debe conectarse con entidades, campañas, lugares, conceptos o assets relacionados.

Las relaciones deben tener propósito histórico, no solo navegación.
