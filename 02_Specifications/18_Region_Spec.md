# HISTORIUM — REGION SPECIFICATION

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Specification

---

# Filosofía

Una región es un espacio histórico con geografía, rutas, culturas y disputas propias.

En Historium, una región no existe como dato aislado.

Existe como una pieza del Museo Vivo.

Debe poder aparecer en campañas, conectarse con otras entidades y crecer con nuevas capas de conocimiento.

---

# Objetivo

Definir cómo se crea, valida, relaciona, versiona y publica una entidad de tipo región dentro del Canon Oficial.

La especificación debe permitir que cualquier equipo produzca contenido consistente sin perder tono, profundidad ni ritmo narrativo.

---

# Principios

- Debe tener identidad única.
- Debe aportar conocimiento histórico real.
- Debe poder relacionarse con otras entidades.
- Debe alimentar el Museo del jugador.
- Debe evitar duplicidad con entidades existentes.
- Debe sostener contenido futuro durante años.
- Debe ser clara para producción, narrativa, arte e importación.

---

# Identidad YAML

```yaml
id: "region_example"
type: "region"
name: "Nombre oficial"
subtitle: "Frase breve de contexto"
period: "Periodo histórico"
date_start: ""
date_end: ""
primary_place: ""
rarity: "common | uncommon | rare | epic | legendary | mythic"
museum_gallery: "Regions"
knowledge_level: 1
status: "draft | review | canon | archived"
version: "1.0.0"
```

---

# Campos obligatorios

- `id`
- `type`
- `name`
- `summary_short`
- `summary_long`
- `period`
- `museum_gallery`
- `rarity`
- `knowledge_levels`
- `relationships`
- `sources`
- `version`

---

# Campos opcionales

- `alternate_names`
- `date_start`
- `date_end`
- `location`
- `visual_prompt`
- `audio_prompt`
- `map_reference`
- `modern_comparison`
- `debates`
- `premium_unlocks`
- `related_campaigns`

---

# Museo

Toda entidad de tipo región debe definir cómo progresa dentro del Museo.

## Nivel 1 — Descubierto

El jugador reconoce que existe y entiende su contexto mínimo.

## Nivel 2 — Estudiado

El jugador comprende su función histórica y sus conexiones principales.

## Nivel 3 — Dominado

El jugador entiende su impacto, debates y consecuencias.

## Nivel 4 — Maestría

El jugador accede a materiales profundos: documentos, mapas, reconstrucciones, comparaciones o análisis premium.

---

# Relaciones

Toda región debe conectarse al Grafo Histórico.

Relaciones recomendadas:

- `pertenece_a`
- `ocurre_en`
- `influye_en`
- `deriva_en`
- `representa`
- `se_opone_a`
- `conecta_con`

Cada relación debe incluir dirección, intensidad y nota de evidencia.

---

# Assets

Assets esperados:

- imagen principal,
- miniatura de Museo,
- prompt visual,
- prompt de audio si aplica,
- mapa o ubicación si aplica,
- referencias de estilo,
- etiquetas para búsqueda interna.

Los assets no decoran.

Deben aumentar comprensión.

---

# Versionado

Toda entidad debe versionarse.

Usar formato semántico:

- `1.0.0` primera versión canon,
- `1.1.0` expansión de contenido,
- `1.1.1` corrección menor,
- `2.0.0` cambio estructural.

Nunca sobrescribir conocimiento sin dejar rastro editorial.

---

# Checklist

Antes de publicar, validar:

- [ ] Tiene ID único.
- [ ] No duplica una entidad existente.
- [ ] Tiene resumen corto y largo.
- [ ] Define niveles de Museo.
- [ ] Tiene relaciones útiles.
- [ ] Incluye assets esperados.
- [ ] Puede aparecer en campañas futuras.
- [ ] Respeta voz y tono Historium.
- [ ] Está listo para importación.

---

# Regla Suprema

Una región solo entra al Canon si hace crecer el Museo Vivo del jugador.
