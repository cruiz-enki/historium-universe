# HISTORIUM — VERSIONING

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

El versionado permite que Historium crezca sin perder memoria editorial.

La Historia se refina.

El Canon también.

---

# Formato oficial

Historium usa versiones con prefijo `v`.

```text
v1.0
v1.1
v1.2
v2.0
```

En frontmatter puede guardarse sin `v` si el importer lo requiere.

El documento visible debe mostrar la versión editorial con `v`.

---

# v1.0 — creación oficial

Primera versión aprobada de una pieza.

Significa:

- tiene ID,
- tiene frontmatter válido,
- tiene contenido suficiente,
- tiene relación con el Museo,
- puede considerarse Canon Oficial.

---

# v1.1 — correcciones menores

Correcciones que no cambian estructura ni interpretación.

Ejemplos:

- ortografía,
- claridad,
- enlaces,
- formato,
- precisión menor.

---

# v1.2 — expansión menor

Agrega contenido compatible.

Ejemplos:

- nueva relación,
- nueva fuente,
- nueva curiosidad,
- nuevo asset,
- nueva sección del Museo,
- conexión con campaña nueva.

---

# v2.0 — reestructuración mayor

Cambio estructural o interpretativo.

Ejemplos:

- cambio de tipo,
- fusión de entidades,
- reescritura profunda,
- cambio de modelo de Museo,
- reemplazo de relaciones centrales,
- cambio que requiere migración en Supabase.

---

# IDs y versiones

El ID no cambia con la versión.

```text
CHAR_000001 v1.0
CHAR_000001 v1.1
CHAR_000001 v1.2
CHAR_000001 v2.0
```

Sigue siendo la misma entidad.

---

# Changelog obligatorio

Todo cambio `v1.2` o `v2.0` debe explicar:

- qué cambió,
- por qué cambió,
- impacto en Museo,
- impacto en relaciones,
- impacto en importer,
- impacto en Supabase.

---

# Regla Suprema

Versionar no es burocracia.

Es la memoria del universo.
