# Architecture Overview
# HISTORIUM — ARCHITECTURE OVERVIEW

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Specification

---

# Propósito

Este documento define la arquitectura interna del Universo Historium.

Historium no es solo una app.

Es un sistema compuesto por:

- Canon histórico
- Entidades reutilizables
- Campañas narrativas
- Museo del jugador
- Grafo de conocimiento
- Importador Markdown
- Base de datos en Supabase
- Experiencia RPG educativa

---

# Principio central

GitHub contiene el Canon Oficial.

Supabase contiene el estado del producto y el progreso del usuario.

La app muestra la experiencia.

---

# Separación de responsabilidades

## GitHub

Contiene:

- Biblia editorial
- Game Design
- Specifications
- Entidades históricas
- Campañas
- Prompts
- Templates
- Assets de referencia
- Arquitectura

GitHub es la fuente de verdad del Universo Historium.

---

## Supabase

Contiene:

- Usuarios
- Progreso
- Museo personal
- Entidades importadas
- Campañas publicadas
- Relaciones procesadas
- Quizzes
- Recompensas
- Estado de desbloqueo

Supabase es la fuente de verdad de la experiencia activa.

---

## App

Contiene:

- Interfaz
- Navegación
- Museo visual
- Campañas jugables
- Mapas
- Perfil del jugador
- Sistema de recompensas
- Lectura de nodos

La app no define el canon.

Solo lo presenta.

---

# Modelo general

```text
GitHub Canon
    ↓
Markdown Importer
    ↓
Supabase
    ↓
Historium App
    ↓
Player Museum
Unidades principales

Historium se construye con estas unidades:

Campaign
Chapter
Node
Entity
Relationship
Museum Update
Reward
Asset
Prompt
Quiz
Curiosity
Entidades

Una entidad es una pieza permanente del conocimiento histórico.

Ejemplos:

Character
City
Battle
War
Concept
Document
Artifact
Civilization
Empire
Religion
Technology
Monument
Region
Event

Las entidades viven en:

03_Knowledge/
Campañas

Una campaña no almacena todo el conocimiento.

Una campaña cuenta una historia usando entidades.

Las campañas viven en:

04_Campaigns/
Nodos

Un nodo es la unidad jugable principal.

Un nodo:

narra,
enseña,
actualiza entidades,
desbloquea museo,
entrega XP,
conecta con el siguiente nodo.

Un nodo no debe duplicar información canónica.

Museo

El Museo representa el conocimiento acumulado del jugador.

No vive en GitHub.

Vive en Supabase.

GitHub define qué puede desbloquearse.

Supabase guarda qué desbloqueó cada usuario.

Grafo de conocimiento

Todo está conectado.

Ejemplo:

CHAR_000001
    governed
CITY_000001

CITY_000001
    part_of
CIV_000001

CONCEPT_000001
    originated_in
CITY_000001

El grafo permite:

navegación inteligente,
recomendaciones,
conexiones entre campañas,
museo vivo,
búsquedas avanzadas,
IA histórica futura.
IDs

Toda entidad debe tener un ID permanente.

Ejemplos:

CHAR_000001
CITY_000001
BATTLE_000001
WAR_000001
CONCEPT_000001
DOC_000001
ART_000001

Los IDs nunca cambian.

Frontmatter

Todo archivo Markdown importable debe iniciar con YAML.

Ejemplo:

id: CHAR_000001
type: character
status: official
version: 1.0
canonical: true
museum: true

El frontmatter es lo que permite importar el canon a Supabase.

Versionado

El contenido evoluciona.

Nunca se borra conocimiento sin justificación.

Cada cambio importante debe actualizar la versión.

Ejemplo:

v1.0 — creación inicial
v1.1 — corrección histórica
v2.0 — expansión mayor
Regla Suprema

Historium debe poder crecer durante años sin romper su estructura.

Cada decisión arquitectónica debe responder:

¿Esto funcionará cuando tengamos 100 campañas, 10,000 entidades y millones de jugadores?

Si la respuesta es no...

debe rediseñarse.


Después crea estos archivos vacíos en la misma carpeta:

```text
01_ID_System.md
02_Naming_Convention.md
03_Frontmatter_Spec.md
04_Knowledge_Graph.md
05_Entity_Lifecycle.md
06_Versioning.md
07_Supabase_Model.md
08_Import_Workflow.md
09_Museum_Data_Model.md
10_Architecture_Checklist.md