# HISTORIUM — KNOWLEDGE GRAPH

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Core Architecture Specification

---

# Propósito

Este documento define el Knowledge Graph de Historium.

Es el mapa vivo que conecta personas, lugares, ideas, objetos, campañas y descubrimientos.

Historium no almacena contenido como una biblioteca plana.

Historium organiza el conocimiento como un universo persistente.

---

# Qué es el Knowledge Graph

El Knowledge Graph es la estructura que conecta todas las entidades históricas del Canon Oficial.

Cada entidad es un nodo del grafo.

Cada relación es una conexión con significado.

Cada campaña recorre una parte del grafo.

Cada nodo jugable actualiza una parte del grafo en el Museo del jugador.

---

# Qué no es

No es una lista de links.

No es una categoría de Wikipedia.

No es un mapa mental improvisado.

No es una tabla de tags.

El grafo solo existe si las relaciones tienen valor histórico, narrativo o museístico.

---

# Entidad, Relación, Campaña, Nodo y Museo

## Entidad

Una entidad es una pieza canónica del mundo histórico.

Ejemplos:

- Pisístrato
- Atenas
- Democracia
- Batalla de Maratón
- Partenón
- Dracma

La entidad almacena conocimiento.

---

## Relación

Una relación conecta dos entidades.

Ejemplo:

```text
CHAR_000001 -- governed --> CITY_000001
```

La relación explica cómo se conectan las piezas del Museo.

---

## Campaña

Una campaña es una experiencia narrativa que guía al jugador por una región del grafo.

La campaña no es dueña de las entidades.

Solo las utiliza.

---

## Nodo

Un nodo es una escena jugable.

Actualiza entidades.

Desbloquea relaciones.

Hace crecer el Museo.

---

## Museo

El Museo es la vista personal del jugador sobre el grafo.

El Canon contiene todo.

El jugador descubre una parte.

---

# Taxonomía principal

## People

- Character
- Biography

## Places

- City
- Location
- Region
- River
- Mountain
- Sea
- Monument

## Polities

- Civilization
- Empire
- Kingdom
- Republic
- City-State
- Dynasty
- Organization

## Events

- Event
- War
- Battle
- Siege
- Treaty
- Revolution
- Discovery
- Expedition

## Ideas

- Concept
- Religion
- Philosophy
- Law
- Technology
- Language
- Myth

## Objects

- Artifact
- Document
- Currency
- Historical Object

## Campaign Structure

- Campaign
- Arc
- Chapter
- Node

---

# Cómo se conectan las entidades

Las entidades se conectan con relaciones tipificadas.

Toda relación debe incluir:

- tipo técnico,
- entidad origen,
- entidad destino,
- dirección,
- visibilidad,
- evidencia,
- intensidad,
- estado editorial.

Ejemplo:

```yaml
type: governed
source: CHAR_000001
target: CITY_000001
visibility: public
intensity: high
status: canon
evidence_note: "Pisístrato ejerció poder político sobre Atenas durante sus tiranías."
```

---

# Relaciones jerárquicas

Sirven para organizar estructuras de pertenencia.

Ejemplos:

```text
Athens part_of Greece
Alexandria part_of Egypt
Parthenon located_in Acropolis
Acropolis located_in Athens
```

Usos:

- construir mapas,
- agrupar galerías del Museo,
- navegar de lo general a lo específico,
- evitar entidades duplicadas.

---

# Relaciones temporales

Sirven para entender sucesión, causa y evolución.

Ejemplos:

```text
Solon predecessor_of Cleisthenes
Athenian tyranny evolved_into democratic reforms
Persian Wars caused political transformation in Athens
```

Usos:

- timelines,
- recomendaciones cronológicas,
- progresión de campañas,
- desbloqueos históricos.

---

# Relaciones geográficas

Sirven para ubicar el conocimiento.

Ejemplos:

```text
Battle of Marathon occurred_in Marathon
Nile located_in Egypt
Delphi connected_to Athens
```

Usos:

- mapas narrativos,
- campañas regionales,
- rutas comerciales,
- exploración del Museo.

---

# Relaciones narrativas

Sirven para construir ritmo y continuidad.

Ejemplos:

```text
Pisistratus opposed Solon
Cleisthenes inspired democratic reform
Alexander connected_to Aristotle
```

Estas relaciones ayudan a que Historium se sienta como una serie premium.

No reemplazan la verdad histórica.

La hacen navegable.

---

# Relaciones conceptuales

Sirven para conectar hechos con ideas.

Ejemplos:

```text
Athenian democracy connected_to citizenship
Tyranny opposed democracy
Roman law influenced republic
```

Usos:

- comprensión profunda,
- preguntas de quiz,
- comparaciones modernas,
- recomendaciones de aprendizaje.

---

# Relaciones ocultas desbloqueables

No todas las relaciones aparecen desde el inicio.

Algunas se desbloquean cuando el jugador alcanza un nivel de conocimiento.

Ejemplo:

```yaml
type: influenced
source: CON_000001
target: EVT_000034
visibility: hidden
unlock_condition:
  entity: CON_000001
  museum_level: 3
```

Estas relaciones generan sensación de descubrimiento.

El jugador no solo gana información.

Descubre conexiones.

---

# Cómo las campañas alimentan el grafo

Una campaña debe:

- usar entidades existentes,
- crear nuevas entidades solo cuando sea necesario,
- actualizar relaciones,
- desbloquear rutas del Museo,
- dejar puertas abiertas hacia campañas futuras.

Cada nodo de campaña debe declarar sus actualizaciones del grafo.

Ejemplo:

```yaml
graph_updates:
  entities:
    - CHAR_000001
    - CITY_000001
  relationships:
    - governed
    - located_in
  hidden_unlocks:
    - inspired
```

---

# Cómo el Museo usa el grafo

El Museo personal del jugador no copia todo el Canon.

Registra qué parte del grafo ha sido descubierta.

Por cada entidad puede guardar:

- estado de descubrimiento,
- nivel de conocimiento,
- porcentaje de progreso,
- relaciones visibles,
- relaciones ocultas pendientes,
- assets desbloqueados,
- campañas donde apareció.

---

# Recomendaciones futuras

El grafo permite recomendar contenido por conexión real.

Ejemplos:

- Si el jugador estudia Atenas, recomendar Solón, Clístenes y Democracia.
- Si domina Roma Republicana, recomendar Ley, Senado, Ciudadanía y Guerras Púnicas.
- Si desbloquea una ruta comercial, recomendar ciudades, monedas, tecnologías y religiones conectadas.

La recomendación no debe basarse solo en popularidad.

Debe basarse en sentido histórico.

---

# IA histórica futura

El grafo puede alimentar una IA histórica interna.

La IA no debe inventar Canon.

Debe consultar entidades, relaciones y estados editoriales.

Usos futuros:

- responder preguntas del jugador,
- explicar conexiones,
- sugerir rutas de aprendizaje,
- generar resúmenes personalizados,
- preparar quizzes,
- detectar contradicciones.

La IA debe hablar desde el Canon.

No por encima del Canon.

---

# Reglas contra relaciones inútiles

Una relación no debe crearse si:

- solo repite una categoría,
- no explica nada,
- no puede mostrarse al jugador,
- no puede validarse editorialmente,
- conecta entidades por asociación débil,
- duplica una relación existente,
- usa nombres en lugar de IDs,
- no tiene dirección clara cuando la necesita.

---

# Relaciones duplicadas

Antes de crear una relación nueva, revisar:

- mismo origen,
- mismo destino,
- mismo tipo,
- misma dirección,
- misma visibilidad.

Si todo coincide, actualizar la relación existente.

No crear otra.

---

# Relaciones ambiguas

Si una relación puede significar varias cosas, debe separarse.

Malo:

```text
connected_to
```

Bueno:

```text
teacher_of
student_of
influenced
opposed
```

`connected_to` solo debe usarse cuando una relación específica aún no existe y la conexión es editorialmente útil.

---

# Regla Suprema

El Knowledge Graph existe para revelar conexiones históricas significativas.

Si una relación no mejora comprensión, navegación o descubrimiento, no pertenece al grafo.
