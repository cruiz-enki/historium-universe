# HISTORIUM — NAMING CONVENTION

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define cómo se nombran carpetas, archivos, slugs, IDs y campos dentro del Canon Oficial de Historium.

Los nombres visibles pueden cambiar.

Los nombres técnicos deben permanecer estables.

---

# Principio Supremo

El nombre visible sirve al jugador.

El nombre técnico sirve al sistema.

El ID sirve al Canon.

Nunca deben confundirse.

---

# Carpetas principales

Las carpetas numeradas se usan solo para secciones principales del repositorio.

Ejemplos:

```text
00_Biblia_Editorial/
01_Game_Design/
02_Specifications/
03_Knowledge/
09_Architecture/
```

No crear carpetas numeradas dentro de galerías de entidades.

---

# Carpetas de entidades

Las carpetas de entidades usan PascalCase plural.

Correcto:

```text
Characters/
Cities/
Battles/
Concepts/
Artifacts/
Documents/
```

Incorrecto:

```text
characters/
03_Characters/
historical-characters/
Personajes/
```

---

# Archivos de entidades

Los archivos de entidades usan:

```text
ID_EnglishName.md
```

Ejemplo:

```text
CHAR_000001_Pisistratus.md
CITY_000001_Athens.md
BAT_000001_Marathon.md
```

Reglas:

- Sin acentos.
- Sin espacios.
- Sin caracteres especiales.
- Sin signos de puntuación.
- Nombre en inglés para estabilidad técnica.
- PascalCase después del ID.

---

# Archivos de campaña

Las campañas usan:

```text
CAMP_000001_GreeceClassical.md
```

Los nodos usan:

```text
NODE_000001_BirthOfThePolis.md
```

Los capítulos usan:

```text
CH_000001_AthensBeforeDemocracy.md
```

---

# Slugs

Los slugs usan `snake_case`.

Ejemplos:

```yaml
slug: "pisistratus"
slug: "greece_classical"
slug: "birth_of_the_polis"
```

El slug no reemplaza al ID.

El slug ayuda a rutas, búsquedas y lectura humana.

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

# Nombres visibles

El título visible puede usar idioma histórico o local.

Ejemplos:

```text
Pisístrato
Atenas
Imperio aqueménida
```

El archivo técnico no debe usar esos caracteres si generan ambigüedad.

---

# Regla Suprema

Un nombre técnico debe permitir encontrar, importar y mantener una pieza del universo sin adivinar.
