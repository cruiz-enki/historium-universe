# ID System
# HISTORIUM — ID SYSTEM

**Versión:** 1.0

**Estado:** Oficial

**Tipo:** Architecture Specification

---

# Filosofía

Todo elemento del Universo Historium posee una identidad permanente.

Un nombre puede cambiar.

Una traducción puede cambiar.

Una clasificación puede cambiar.

El ID nunca.

Los IDs son la columna vertebral del Universo Historium.

---

# Principio Supremo

Un ID jamás debe reutilizarse.

Nunca.

Aunque una entidad sea eliminada.

Aunque se descubra un error.

Aunque cambie de nombre.

Ese ID queda reservado para siempre.

---

# Estructura

Todos los IDs siguen exactamente el mismo formato.

```
PREFIX_000001
```

Ejemplo.

```
CHAR_000001
```

---

# Formato

```
[PREFIX]_[Número de seis dígitos]
```

Ejemplos.

```
CHAR_000001

CITY_000001

WAR_000001

CONCEPT_000001
```

---

# Longitud

Todos los IDs tienen exactamente:

```
PREFIX + "_" + 6 dígitos
```

Ejemplo.

```
CHAR_000001
```

Nunca.

```
CHAR1

CHAR_12

CHARACTER_001
```

---

# Prefijos Oficiales

## Personas

```
CHAR
```

Character

Ejemplo.

```
CHAR_000145
```

---

## Ciudades

```
CITY
```

---

## Lugares

```
LOC
```

Incluye:

- Acrópolis
- Foro Romano
- Ágora
- Monte Olimpo

No ciudades completas.

---

## Regiones

```
REG
```

---

## Monumentos

```
MON
```

---

## Civilizaciones

```
CIV
```

---

## Imperios

```
EMP
```

---

## Batallas

```
BAT
```

---

## Guerras

```
WAR
```

---

## Eventos

```
EVT
```

---

## Conceptos

```
CON
```

---

## Religiones

```
REL
```

---

## Tecnologías

```
TECH
```

---

## Documentos

```
DOC
```

---

## Artefactos

```
ART
```

---

## Biografías

```
BIO
```

---

## Organizaciones

```
ORG
```

---

## Dinastías

```
DYN
```

---

## Idiomas

```
LANG
```

---

## Monedas

```
CUR
```

---

## Leyes

```
LAW
```

---

## Rutas

```
ROUTE
```

---

## Mitos

```
MYTH
```

---

## Campañas

```
CAMP
```

---

## Arcos

```
ARC
```

---

## Capítulos

```
CH
```

---

## Nodos

```
NODE
```

---

# Numeración

La numeración siempre es incremental.

Nunca depende del contenido.

Ejemplo.

```
CHAR_000001

CHAR_000002

CHAR_000003
```

Aunque el personaje sea mucho más importante.

No existe prioridad.

---

# IDs Humanos

Los IDs están diseñados para ser fáciles de leer.

Nunca usar UUID.

Nunca usar hashes.

Nunca usar GUID.

Incorrecto.

```
ab92f8c3-44...
```

Correcto.

```
CHAR_000084
```

---

# IDs Permanentes

Cambiar el nombre de una entidad no modifica su ID.

Ejemplo.

```
CITY_000031

Constantinopla
```

↓

Pasa a llamarse.

```
Estambul
```

El ID sigue siendo.

```
CITY_000031
```

---

# IDs y Traducciones

El ID nunca depende del idioma.

Ejemplo.

```
CITY_000001
```

Puede mostrarse como.

Athens

Atenas

Athènes

Athen

Pero el ID siempre será el mismo.

---

# IDs y Versiones

El ID no cambia cuando cambia el contenido.

Ejemplo.

```
CHAR_000001
v1.0

↓

CHAR_000001
v2.0
```

---

# IDs Reservados

Nunca reutilizar.

Nunca reciclar.

Nunca renumerar.

Aunque una entidad desaparezca.

El ID permanece reservado.

---

# ID Registry

El archivo `03_Knowledge/REGISTRY.yaml` es la fuente de verdad para asignar nuevos IDs canónicos.

Ningún documento, campaña, entidad o importador debe inventar IDs fuera del Registry.

El Registry controla el siguiente número disponible para cada prefijo oficial mediante `next_id`.

Reglas obligatorias:

- Nunca reutilizar IDs.
- Nunca reducir `next_id`.
- Cada entidad nueva debe tomar el ID indicado por `next_id`.
- Después de crear una entidad, incrementar `next_id`.
- Usar siempre el formato `PREFIX_000001`.

Ejemplo:

```yaml
characters:
  prefix: CHAR
  next_id: 42
```

La siguiente entidad de personaje debe usar:

```text
CHAR_000042
```

Después de crearla, el Registry debe quedar así:

```yaml
characters:
  prefix: CHAR
  next_id: 43
```

Si una entidad se elimina, fusiona o archiva, su ID no vuelve al Registry.

Queda reservado para siempre.

---

# Relaciones

Las relaciones siempre utilizan IDs.

Nunca nombres.

Incorrecto.

```
Pisístrato

↓

Gobernó

↓

Atenas
```

Correcto.

```
CHAR_000001

↓

governed

↓

CITY_000001
```

---

# Importador

El Importador utiliza únicamente IDs.

Nunca interpreta nombres.

Esto evita errores por traducciones.

---

# Ejemplo Completo

```
CHAR_000021

Nombre:

Pericles

↓

Gobernó

↓

CITY_000001

↓

Participó en

↓

WAR_000003

↓

Introdujo

↓

CON_000004
```

---

# Futuro

El sistema está preparado para millones de entidades.

Los seis dígitos permiten:

999,999 entidades por categoría.

Si algún día fuera necesario.

Se ampliará a siete dígitos.

Nunca modificando los existentes.

---

# Checklist

□ El ID tiene prefijo válido.

□ Tiene seis dígitos.

□ Nunca fue utilizado.

□ No depende del idioma.

□ No depende del nombre.

□ Es permanente.

---

# Regla Suprema

El ID es la identidad oficial de una entidad.

Todo lo demás puede evolucionar.

El ID permanece para siempre.
