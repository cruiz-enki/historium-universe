# HISTORIUM — DOCUMENT SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Entity Specification

---

# Filosofía

Las ideas sobreviven gracias a los documentos.

Un documento puede cambiar una nación.

Una religión.

Un imperio.

Una civilización.

Historium estudia los documentos como motores del cambio histórico.

No únicamente como textos antiguos.

---

# Objetivo

Todo documento debe responder seis preguntas.

¿Qué es?

¿Quién lo creó?

¿Por qué fue escrito?

¿Qué decía?

¿Qué cambió?

¿Por qué sigue siendo importante?

---

# Principios

Todo documento existe una sola vez dentro del Universo Historium.

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
id: DOC_000001

slug: code-of-hammurabi

type: Document
```

---

# Información principal

Título

Título original

Otros nombres

Idioma original

Pronunciación

Categoría

---

# Categorías

Todo documento pertenece a una categoría.

Ejemplos.

Ley

Código

Constitución

Tratado

Edicto

Carta

Crónica

Manifiesto

Declaración

Inscripción

Texto religioso

Contrato

Decreto

Biografía

Obra literaria

Obra filosófica

Documento diplomático

---

# Resumen

150–250 caracteres.

Debe responder.

¿Por qué este documento cambió la Historia?

Ejemplo.

El Código de Hammurabi fue uno de los primeros conjuntos de leyes escritos de la humanidad y sentó precedentes para el desarrollo del derecho.

---

# Contexto histórico

Debe responder.

¿Qué estaba ocurriendo cuando fue creado?

¿Por qué era necesario?

¿Qué problema intentaba resolver?

---

# Autor

Relacionar mediante IDs.

Puede ser.

Persona

Institución

Gobierno

Imperio

Civilización

---

# Fecha

```yaml
creation_date:

precision:
```

Precisión.

Exacta

Aproximada

Debatida

Desconocida

---

# Lugar de creación

Relacionado mediante IDs.

Ciudad

Región

Imperio

---

# Propósito

¿Por qué fue escrito?

Legislar.

Registrar.

Narrar.

Convencer.

Organizar.

Justificar.

Inspirar.

Comunicar.

---

# Contenido

Debe dividirse.

Introducción

↓

Ideas principales

↓

Puntos clave

↓

Conclusión

Nunca copiar el documento completo.

Historium explica.

No reemplaza la fuente.

---

# Ideas principales

Mínimo.

5

Ideal.

10

Cada idea debe explicarse de forma sencilla.

---

# Consecuencias

Debe dividirse.

Inmediatas

↓

Mediano plazo

↓

Largo plazo

---

# Influencia

¿Qué documentos inspiró?

¿Qué leyes cambió?

¿Qué gobiernos influyó?

¿Qué movimientos surgieron gracias a él?

---

# Relaciones

Relacionado mediante IDs.

Personajes

Conceptos

Ciudades

Imperios

Religiones

Organizaciones

Eventos

Objetos históricos

---

# Campañas

Lista completa.

---

# Museo

## Nivel 1

Descubierto

Desbloquea.

Título

Resumen

Autor

Fecha

---

## Nivel 2

Estudiado

Desbloquea.

Contexto

Ideas principales

Propósito

Relaciones

---

## Nivel 3

Dominado

Desbloquea.

Debates

Interpretaciones

Influencias

Comparaciones

---

## Nivel 4

Maestría

Desbloquea.

Texto original (cuando sea de dominio público)

Traducciones

Facsímiles

Podcast

Bibliografía

Comentario histórico

---

# Curiosidades

Mínimo.

10

Nunca repetir el nodo.

Siempre ampliar.

---

# Debates

Debe indicar.

Autoría.

Fecha.

Interpretación.

Autenticidad.

Traducciones.

Versiones.

---

# Estado actual

¿Existe el original?

¿Dónde se conserva?

¿Se perdió?

¿Existen copias?

¿Está digitalizado?

---

# Legado

Debe responder.

¿Por qué seguimos hablando de este documento?

---

# Comparación moderna

Siempre que sea posible.

Ejemplo.

Código de Hammurabi

↓

Código Civil moderno

Declaración de Independencia

↓

Constituciones contemporáneas

Siempre aclarando diferencias.

Nunca simplificando.

---

# Assets

Portada

Facsímil

Hero

Carta

Infografía

Timeline

Miniatura

Wallpaper

Animación

---

# Audio

Narración

Pronunciación

Lectura de fragmentos

Comentario

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

Antigüedad

Autores

Idiomas

Traducciones

Campañas

Personajes

Conceptos

Ciudades

Imperios

Eventos

---

# Versionado

Toda modificación genera una nueva versión.

Nunca se elimina información.

---

# Checklist

□ Tiene contexto

□ Tiene autor

□ Tiene propósito

□ Tiene ideas principales

□ Tiene consecuencias

□ Tiene influencia

□ Tiene debates

□ Tiene assets

□ Alimenta el Museo

Si alguna respuesta es "No"...

El documento todavía no pertenece al Universo Historium.

---

# Regla Suprema

Los documentos conservan las ideas que transformaron la Historia.

Comprender un documento no consiste únicamente en leerlo.

Consiste en entender por qué alguien sintió la necesidad de escribirlo y cómo esas palabras cambiaron el mundo.

Historium estudia documentos porque las civilizaciones también se construyen con tinta.

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
