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

# Formato

Historium usa versionado semántico:

```text
MAJOR.MINOR.PATCH
```

Ejemplo:

```text
1.0.0
```

---

# PATCH

Cambios menores.

Ejemplos:

- corrección ortográfica,
- ajuste de frase,
- mejora de claridad,
- corrección de enlace.

No cambia estructura ni interpretación.

---

# MINOR

Expansión compatible.

Ejemplos:

- nueva relación,
- nuevo asset,
- nueva curiosidad,
- nuevo desbloqueo de Museo,
- ampliación de contexto.

---

# MAJOR

Cambio estructural o interpretativo.

Ejemplos:

- cambio de tipo de entidad,
- reescritura profunda,
- fusión de entidades,
- cambio de modelo de datos,
- cambio de relación central.

---

# IDs y versiones

El ID no cambia con la versión.

```text
CHAR_000001 v1.0.0
CHAR_000001 v1.1.0
CHAR_000001 v2.0.0
```

Sigue siendo la misma entidad.

---

# Changelog editorial

Todo cambio `MINOR` o `MAJOR` debe explicar:

- qué cambió,
- por qué cambió,
- quién lo aprobó,
- impacto en Museo,
- impacto en relaciones,
- impacto en importer.

---

# Supabase

Supabase puede guardar la versión importada.

Esto permite saber qué versión del Canon vio cada jugador.

El progreso del usuario no cambia la versión canon.

---

# Regla Suprema

Versionar no es burocracia.

Es la memoria del universo.
