# HISTORIUM — ENTITY LIFECYCLE

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define los estados oficiales por los que pasa una entidad, campaña, nodo o pieza importable dentro de Historium.

Una entidad no es una ficha estática.

Es una pieza viva del Museo.

---

# Estados oficiales

## draft

La pieza existe como borrador.

Puede tener estructura incompleta.

Puede no tener fuentes finales.

Puede cambiar de forma profunda.

Puede avanzar cuando:

- tiene ID asignado,
- tiene frontmatter mínimo,
- tiene tipo oficial,
- tiene propósito claro.

---

## research

La pieza está en investigación histórica.

Aquí se reúnen fuentes, contexto, dudas y posibles relaciones.

Puede avanzar cuando:

- tiene fuentes mínimas,
- no duplica otra entidad,
- tiene relaciones tentativas,
- se entiende su lugar en el Museo.

---

## review

La pieza está lista para revisión editorial, narrativa y arquitectónica.

Puede avanzar cuando:

- el contenido es claro,
- el frontmatter es válido,
- las relaciones usan IDs,
- el naming respeta convención,
- el Museo queda definido,
- las fuentes son aceptables.

---

## official

La pieza forma parte del Canon Oficial en GitHub.

Todavía puede no estar publicada en la app.

Puede avanzar cuando:

- fue aprobada editorialmente,
- pasó validación de importer,
- no rompe relaciones existentes,
- tiene versión oficial.

---

## published

La pieza está disponible en la experiencia activa.

Existe en Supabase como contenido importado.

Puede aparecer en campañas, nodos, Museo, recomendaciones y progreso del usuario.

Puede avanzar a nueva versión cuando:

- se expande,
- se corrige,
- se conecta con nuevas entidades,
- una campaña nueva la reutiliza.

---

## deprecated

La pieza fue reemplazada por otra mejor.

No se borra.

No se reutiliza su ID.

Debe indicar qué pieza la reemplaza.

Puede avanzar cuando:

- se decide archivarla,
- ya no debe aparecer en producción,
- el importer la conserva solo como historial.

---

## archived

La pieza se conserva por historia editorial.

No aparece en la app.

No alimenta nuevas recomendaciones.

Su ID queda reservado para siempre.

---

# Flujo estándar

```text
draft
  ↓
research
  ↓
review
  ↓
official
  ↓
published
```

Ramas posibles:

```text
official → deprecated → archived
published → deprecated → archived
```

---

# Regla de avance

Ninguna pieza avanza de estado por entusiasmo.

Avanza porque cumple criterios verificables.

---

# Regla Suprema

El lifecycle protege al Museo Vivo de contenido incompleto, duplicado o débil.
