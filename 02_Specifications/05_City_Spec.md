# HISTORIUM — CITY SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Entity Specification

---

# Filosofía

Las ciudades son organismos vivos.

Respiran.

Crecen.

Cambian.

Son conquistadas.

Se reconstruyen.

Desaparecen.

Vuelven a surgir.

Una ciudad puede sobrevivir miles de años mientras cambian imperios, religiones y gobernantes.

Historium estudia esa evolución.

No solamente una ubicación geográfica.

---

# Objetivo

Toda ciudad debe responder cinco preguntas.

¿Dónde está?

¿Cómo nació?

¿Por qué fue importante?

¿Cómo cambió con el tiempo?

¿Qué queda de ella hoy?

---

# Principios

Una ciudad existe una sola vez dentro del Universo Historium.

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

Ejemplo

```yaml
id: CITY_000001

slug: athens

type: City
```

---

# Información principal

Nombre actual

Nombre histórico

Nombre original

Otros nombres

Pronunciación

Idioma original

Gentilicio

---

# Resumen

150–250 caracteres.

Debe responder inmediatamente:

¿Por qué esta ciudad cambió la Historia?

Ejemplo.

Atenas fue el principal centro político, filosófico y cultural del mundo griego, cuna de la democracia y hogar de algunos de los pensadores más influyentes de la humanidad.

---

# Localización

```yaml
continent:

country_modern:

region:

latitude:

longitude:

elevation:
```

---

# Geografía

Tipo de terreno

Clima

Ríos

Montañas

Costa

Recursos naturales

Ventajas estratégicas

Limitaciones

---

# Fundación

Fecha aproximada

Fundadores

Origen

Mitos fundacionales

Primeros asentamientos

---

# Evolución histórica

La historia debe dividirse por etapas.

Ejemplo.

Nacimiento

Crecimiento

Edad de Oro

Crisis

Reconstrucción

Declive

Estado actual

Nunca escribir un único bloque enorme.

---

# Línea del tiempo

Debe existir una cronología.

Ejemplo.

c. 3000 a.C.

↓

800 a.C.

↓

508 a.C.

↓

490 a.C.

↓

404 a.C.

↓

146 a.C.

↓

Hoy

---

# Gobierno

Tipos de gobierno que tuvo.

Ejemplo.

Monarquía

Aristocracia

Tiranía

Democracia

Imperio

República

---

# Economía

Actividades económicas principales.

Agricultura

Comercio

Minería

Industria

Puertos

Mercados

Moneda

---

# Sociedad

Población estimada

Clases sociales

Diversidad cultural

Idiomas

Costumbres

Educación

---

# Religión

Religión predominante

Templos principales

Festividades

Cultos importantes

Cambios religiosos

---

# Arquitectura

Edificios principales

Murallas

Puertos

Palacios

Templos

Mercados

Calles

Distritos

Acueductos

---

# Monumentos

Relacionar únicamente IDs.

Ejemplo.

MON_000021

MON_000045

MON_000111

---

# Personajes relacionados

Fundadores

Gobernantes

Filósofos

Militares

Artistas

Todos mediante IDs.

---

# Batallas

Todas las batallas ocurridas en la ciudad.

Nunca texto libre.

Solo relaciones.

---

# Conceptos relacionados

Democracia

Imperio

Comercio

Ciudad Estado

Filosofía

Etc.

---

# Civilizaciones

Debe indicar todas las civilizaciones a las que perteneció.

Ejemplo.

Micénica

Griega

Romana

Bizantina

Otomana

Griega moderna

---

# Imperios

Todos los imperios que la controlaron.

---

# Campañas

Lista completa.

Ejemplo.

Grecia Clásica

Alejandro

Roma

Bizancio

Edad Media

---

# Museo

## Nivel 1

Descubierta

Desbloquea.

Mapa

Resumen

Ubicación

Bandera histórica (si aplica)

---

## Nivel 2

Explorada

Desbloquea.

Historia

Distritos

Cronología

Gobierno

Economía

---

## Nivel 3

Dominada

Desbloquea.

Curiosidades

Arquitectura

Comparaciones

Fuentes

Reconstrucciones

---

## Nivel 4

Maestría

Desbloquea.

Modelo 3D

Tour interactivo

Documentos

Podcast

Galería completa

---

# Curiosidades

Mínimo.

10

Nunca repetir el nodo.

Siempre ampliar.

---

# Debates históricos

Toda ciudad debe indicar.

Origen debatido.

Ubicación debatida.

Cronología debatida.

Interpretaciones arqueológicas.

---

# Estado actual

¿Qué existe hoy?

Ruinas

Ciudad moderna

Museo

Sitio UNESCO

Excavaciones

Acceso turístico

---

# Visita moderna

Información para viajeros.

País

Ciudad moderna

Museo cercano

Principales restos

---

# Assets

Hero

Mapa

Reconstrucción

Vista aérea

Carta

Panorámica

Distrito

Modelo 3D

Wallpaper

Miniatura

---

# Audio

Pronunciación

Narración

Ambiente

Reconstrucción sonora

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

Años habitada

Población máxima estimada

Imperios

Civilizaciones

Monumentos

Personajes

Batallas

Documentos

Conceptos

Campañas

---

# Versionado

Cada actualización genera una nueva versión.

Nunca se pierde información.

---

# Checklist

□ Tiene ubicación exacta

□ Tiene cronología

□ Tiene evolución

□ Tiene monumentos

□ Tiene personajes

□ Tiene conceptos

□ Tiene campañas

□ Tiene assets

□ Tiene estado actual

□ Alimenta el Museo

Si alguna respuesta es "No"...

La ciudad todavía no pertenece al Universo Historium.

---

# Regla Suprema

Una ciudad no es un punto en el mapa.

Es un escenario donde miles de personas vivieron, soñaron, lucharon y cambiaron la Historia.

Historium siempre contará esa historia.

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
