# HISTORIUM — NAMING CONVENTION

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define cómo se nombran archivos, carpetas, entidades y campos dentro del Canon Oficial de Historium.

Los nombres humanos pueden ser elegantes.

Los nombres técnicos deben ser estables.

Historium necesita ambos.

---

# Principio Supremo

El nombre visible sirve al jugador.

El nombre técnico sirve al sistema.

Nunca deben confundirse.

---

# Carpetas

Las carpetas principales usan numeración de dos dígitos y Pascal/Snake mixto legible:

```text
00_Biblia_Editorial/
01_Game_Design/
02_Specifications/
03_Knowledge/
09_Architecture/
```

Las carpetas de taxonomía usan singular conceptual en inglés pluralizado:

```text
Characters/
Cities/
Civilizations/
Artifacts/
```

---

# Archivos

Los documentos de arquitectura usan prefijo numérico:

```text
04_Knowledge_Graph.md
```

Los specs usan sufijo `_Spec.md`:

```text
03_Node_Spec.md
14_Technology_Spec.md
```

Las plantillas usan sufijo `_Template.md`:

```text
Node_Template.md
Character_Template.md
```

---

# Entidades

El nombre visible de una entidad puede usar acentos, espacios y nombre histórico correcto.

Ejemplo:

```text
Pisístrato
Alejandría
Imperio aqueménida
```

El slug técnico debe usar minúsculas, ASCII y guiones bajos:

```text
pisistratus
alexandria
achaemenid_empire
```

El ID canónico siempre viene del Registry:

```text
CHAR_000001
CITY_000001
EMP_000001
```

---

# Campos

Los campos estructurados usan `snake_case`.

Correcto:

```yaml
summary_short: ""
museum_gallery: ""
knowledge_level: 1
related_campaigns: []
```

Incorrecto:

```yaml
summaryShort: ""
Museum Gallery: ""
knowledge-level: 1
```

---

# Idiomas

El Canon puede tener nombres en español e inglés.

El ID no depende del idioma.

El slug técnico debe mantenerse estable aunque cambie la traducción visible.

---

# Títulos

Los títulos editoriales deben ser claros, no genéricos.

Mejor:

```text
El día que Atenas eligió recordar
```

Peor:

```text
Nodo 4
```

---

# Regla Suprema

Un buen nombre debe ayudar a encontrar, mantener o recordar una pieza del universo.

Si no ayuda a ninguna de esas tres cosas, debe cambiarse.
