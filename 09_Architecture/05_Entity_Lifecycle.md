# HISTORIUM — ENTITY LIFECYCLE

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define cómo nace, madura, se valida y evoluciona una entidad dentro de Historium.

Una entidad no es una ficha.

Es una pieza viva del Museo.

---

# Estados oficiales

## idea

Existe como intención editorial.

Todavía no tiene ID.

---

## drafted

Ya tiene ID asignado desde `REGISTRY.yaml`.

Tiene estructura mínima.

Puede cambiar mucho.

---

## reviewed

Fue revisada por narrativa, conocimiento y arquitectura.

Sus relaciones principales son válidas.

---

## canon

Forma parte del Canon Oficial.

Puede importarse a Supabase.

Puede aparecer en campañas y Museo.

---

## expanded

Recibió nuevas capas de conocimiento.

Mantiene el mismo ID.

---

## deprecated

Fue reemplazada por una entidad mejor.

No se elimina.

No se reutiliza su ID.

---

## archived

Se conserva por historial editorial.

No se muestra al jugador salvo uso interno.

---

# Flujo

```text
idea
  ↓
drafted
  ↓
reviewed
  ↓
canon
  ↓
expanded
```

Ramas posibles:

```text
canon → deprecated
canon → archived
```

---

# Asignación de ID

El ID se asigna al pasar de `idea` a `drafted`.

Debe venir de `03_Knowledge/REGISTRY.yaml`.

Después de asignarlo, se incrementa `next_id`.

---

# Validación antes de canon

Una entidad no puede ser `canon` si:

- no tiene ID válido,
- no tiene tipo oficial,
- no tiene resumen corto,
- no tiene galería de Museo,
- no tiene relaciones mínimas,
- duplica una entidad existente,
- contradice una entidad canon sin nota editorial,
- no puede importarse.

---

# Expansión

Expandir una entidad no crea una entidad nueva.

Ejemplo:

Pisístrato puede aparecer en una campaña de Atenas, otra de tiranía y otra de democracia temprana.

Sigue siendo el mismo `CHAR_000001`.

---

# Fusión

Si dos entidades representan lo mismo:

- una se mantiene como principal,
- la otra pasa a `deprecated`,
- se registra la razón,
- ambos IDs quedan reservados.

---

# Regla Suprema

Una entidad puede evolucionar durante años.

Su ID nunca.
