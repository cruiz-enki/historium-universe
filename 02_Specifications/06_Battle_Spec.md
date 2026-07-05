# HISTORIUM — BATTLE SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Entity Specification

---

# Filosofía

Las batallas no son listas de movimientos militares.

Son momentos donde miles de decisiones humanas convergen en unas pocas horas.

Cada batalla cambia algo.

Un imperio.

Una civilización.

Una frontera.

Una idea.

Historium estudia las causas, el desarrollo y las consecuencias.

Nunca únicamente el combate.

---

# Objetivo

Toda batalla debe responder seis preguntas.

¿Por qué ocurrió?

¿Quiénes participaron?

¿Cómo se desarrolló?

¿Por qué ganó un bando?

¿Qué cambió después?

¿Qué podemos aprender de ella?

---

# Principios

Una batalla existe una sola vez dentro del Universo Historium.

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
id: BATTLE_000001

slug: marathon

type: Battle
```

---

# Información principal

Nombre

Nombre original

Otros nombres

Pronunciación

Periodo histórico

---

# Resumen

150–250 caracteres.

Debe responder inmediatamente.

¿Por qué esta batalla cambió la Historia?

Ejemplo.

La Batalla de Maratón demostró que el Imperio Persa podía ser derrotado y transformó la confianza del mundo griego, preparando el camino para el desarrollo de Atenas.

---

# Contexto

Toda batalla debe explicar.

¿Qué estaba ocurriendo antes?

Nunca comenzar directamente con el combate.

Debe responder.

¿Por qué ambos ejércitos llegaron aquí?

---

# Localización

```yaml
latitude:

longitude:

region:

country_modern:

terrain:
```

---

# Terreno

Tipo.

Llanura

Montaña

Bosque

Desierto

Costa

Río

Pantano

El terreno debe explicarse.

No únicamente mencionarse.

---

# Fecha

```yaml
date:

precision:
```

La precisión puede ser.

Exacta

Aproximada

Debatida

---

# Bandos

Debe existir una ficha para cada bando.

Nombre

Civilización

Imperio

Comandante

Objetivo

Motivación

Fortalezas

Debilidades

---

# Comandantes

Relacionados mediante IDs.

Nunca texto libre.

Ejemplo.

CHAR_000032

CHAR_000078

---

# Fuerzas

Siempre indicar cuando sea posible.

Infantería

Caballería

Arqueros

Flota

Elefantes

Artillería

Apoyo

Las cifras aproximadas deben marcarse como estimaciones.

---

# Tecnología

Toda batalla debe indicar.

Armas principales

Armaduras

Formaciones

Innovaciones

Ventajas tecnológicas

---

# Desarrollo

Debe dividirse en fases.

Nunca un bloque único.

Ejemplo.

Preparativos

↓

Despliegue

↓

Primer contacto

↓

Punto de ruptura

↓

Desenlace

↓

Persecución

Cada fase debe sentirse como un episodio.

---

# Estrategia

Debe responder.

¿Qué plan tenía cada bando?

¿Por qué funcionó?

¿Por qué fracasó?

---

# Decisiones críticas

Toda batalla debe contener.

Mínimo.

3

Ideal.

5

Ejemplo.

Milcíades decide atacar.

↓

Los persas reaccionan tarde.

↓

La falange rompe el centro enemigo.

---

# Resultado

Ganador

Perdedor

Estado

Victoria decisiva

Victoria táctica

Empate

Derrota estratégica

Etc.

---

# Consecuencias

Inmediatas

Mediano plazo

Largo plazo

Nunca limitarse al resultado militar.

---

# Impacto histórico

Debe responder.

¿Por qué seguimos hablando de esta batalla?

---

# Personajes relacionados

Todos mediante IDs.

Comandantes

Gobernantes

Héroes

Traidores

Cronistas

---

# Ciudades relacionadas

IDs únicamente.

---

# Campañas

Todas donde aparece.

---

# Conceptos

Ejemplo.

Falange

Imperio

Logística

Democracia

Honor

Táctica

---

# Museo

## Nivel 1

Descubierta

Desbloquea.

Mapa

Resumen

Fecha

Bandos

---

## Nivel 2

Estudiada

Desbloquea.

Cronología

Desarrollo

Ejércitos

Terreno

---

## Nivel 3

Dominada

Desbloquea.

Análisis táctico

Errores

Curiosidades

Fuentes

Comparaciones

---

## Nivel 4

Maestría

Desbloquea.

Mapa interactivo

Animación

Reconstrucción

Modelos

Podcast

Documentos

---

# Curiosidades

Mínimo.

10

Nunca repetir información del nodo.

---

# Debates históricos

Toda batalla debe indicar.

Número de soldados debatido.

Ubicación debatida.

Cronología debatida.

Interpretaciones modernas.

---

# Reconstrucción

Debe existir una reconstrucción oficial.

Mapa

Movimientos

Formaciones

Cronología minuto a minuto (cuando sea posible)

---

# Estado actual

¿Qué existe hoy?

Campo de batalla

Museo

Monumento

Ruinas

Centro de interpretación

---

# Visita moderna

País

Acceso

Museos

Restos arqueológicos

Sitios recomendados

---

# Assets

Hero

Mapa táctico

Vista aérea

Carta

Infografía

Reconstrucción

Animación

Wallpaper

Miniatura

---

# Audio

Narración

Ambiente

Reconstrucción sonora

Pronunciación

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

Duración

Soldados estimados

Bajas

Comandantes

Bandos

Tecnologías

Formaciones

Conceptos

Campañas

---

# Versionado

Toda actualización genera una nueva versión.

Nunca se elimina conocimiento.

---

# Checklist

□ Tiene contexto

□ Tiene terreno

□ Tiene estrategia

□ Tiene desarrollo por fases

□ Tiene consecuencias

□ Tiene impacto histórico

□ Tiene debates

□ Tiene assets

□ Alimenta el Museo

Si alguna respuesta es "No"...

La batalla todavía no pertenece al Universo Historium.

---

# Regla Suprema

Una batalla no se gana únicamente por tener más soldados.

Se gana por decisiones.

Comprender una batalla es comprender cómo el liderazgo, la logística, la tecnología, el terreno y el factor humano pueden cambiar el curso de la Historia.

Ese es el objetivo de Historium.

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
