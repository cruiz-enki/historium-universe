# HISTORIUM — ENTITY SPECIFICATION

**Versión:** 1.0

**Estado:** Oficial

---

# Introducción

Todo el contenido de Historium se construye a partir de entidades.

Una entidad representa un elemento único del conocimiento histórico.

Una entidad nunca pertenece exclusivamente a una campaña.

Puede aparecer en decenas de campañas diferentes.

Ejemplo.

Alejandro Magno aparece en:

- Grecia
- Macedonia
- Persia
- Egipto
- India
- Helenismo
- Roma (influencia)
- Grandes Conquistadores

Solo existe una entidad.

Las campañas únicamente la utilizan.

---

# Principios

Una entidad debe cumplir siempre estas reglas.

• Tiene un ID único.

• Existe una sola vez en todo Historium.

• Puede relacionarse con cualquier otra entidad.

• Puede crecer durante años.

• Nunca contiene información duplicada.

• Es independiente de cualquier campaña.

---

# Tipos oficiales de entidades

Historium reconoce las siguientes entidades.

👤 Character

🏛 Civilization

👑 Empire

🏙 City

⚔ Battle

📜 Event

💡 Concept

📄 Document

🏺 Artifact

🏛 Monument

🧭 Location

🛣 Route

🎭 Culture

⚖ Law

🔬 Technology

📚 Book

🌎 Region

🌊 Sea

🏔 Mountain

🏞 River

🪙 Currency

🏺 Religion

---

# Estructura común

Toda entidad posee los siguientes campos.

id

type

name

slug

summary

description

era

start_date

end_date

status

rarity

difficulty

museum_level

tags

sources

relations

assets

campaigns

created_at

updated_at

---

# ID

Cada entidad posee un identificador permanente.

Ejemplos.

CHAR_000001

CITY_000031

BATTLE_000142

CONCEPT_000017

Nunca cambia.

Nunca se reutiliza.

---

# Type

Tipo de entidad.

Valores permitidos.

Character

City

Battle

Concept

Empire

Civilization

Religion

Document

Artifact

Monument

Technology

Law

Event

Location

Route

Book

---

# Name

Nombre oficial.

Ejemplo.

Alejandro Magno

---

# Slug

Nombre para URLs.

Ejemplo.

alejandro-magno

---

# Summary

Descripción corta.

Máximo.

250 caracteres.

Se utiliza en tarjetas.

Resultados de búsqueda.

Notificaciones.

---

# Description

Descripción completa.

No tiene límite fijo.

Es la ficha principal del Museo.

---

# Era

Periodo histórico.

Ejemplos.

Edad del Bronce

Grecia Arcaica

Grecia Clásica

Helenismo

República Romana

Imperio Romano

Edad Media

Renacimiento

---

# Fechas

start_date

end_date

Siempre que existan.

Si se desconocen.

Se marca.

unknown

---

# Status

Estado histórico.

Activo

Desaparecido

En construcción

En investigación

Hipotético

Legendario

---

# Rareza

Las entidades poseen rareza.

Común

Poco Común

Raro

Épico

Legendario

Mítico

---

# Difficulty

Nivel recomendado.

Básico

Intermedio

Avanzado

Experto

---

# Museum Level

Representa el nivel de investigación del jugador.

0

No descubierto

1

Descubierto

2

Estudiado

3

Dominado

4

Maestría

---

# Tags

Palabras clave.

Ejemplo.

Grecia

Política

Democracia

Tiranía

Atenas

---

# Sources

Referencias históricas.

Pueden ser.

Libros.

Artículos.

Museos.

Documentos.

Fuentes clásicas.

Nunca visibles por defecto.

---

# Assets

Toda entidad puede tener recursos multimedia.

Imagen principal

Galería

Modelo 3D

Audio

Video

Mapa

Animación

Reconstrucción

Documento PDF

---

# Campaigns

Lista todas las campañas donde aparece.

Ejemplo.

Grecia

Alejandro

Roma

Democracia

---

# Relaciones

Las relaciones nunca se escriben como texto libre.

Siempre siguen el sistema oficial.

Ejemplo.

Fue maestro de

Gobernó

Inspiró

Participó en

Fundó

Conquistó

Derrotó

---

# Campos específicos por entidad

## Character

Además de la estructura común.

birth_place

death_place

occupation

titles

family

successor

predecessor

portrait

quotes

timeline

legacy

---

## City

country

region

latitude

longitude

population_estimate

founded

destroyed

government

economy

religion

important_buildings

---

## Battle

date

location

commanders

armies

winner

loser

casualties

importance

map

formations

---

## Civilization

capital

language

religion

government

currency

writing_system

territory

greatest_extent

legacy

---

## Empire

founder

capital

maximum_extent

government

economy

dynasties

fall_reason

legacy

---

## Concept

definition

modern_equivalent

origin

importance

examples

misconceptions

connections

---

## Monument

architect

construction_date

location

style

materials

height

current_state

unesco

---

## Artifact

material

owner

current_location

period

dimensions

discovery

museum

---

## Document

author

date

language

location

original

translations

importance

---

# Versionado

Las entidades evolucionan.

Nunca se reemplazan.

Ejemplo.

Pisístrato

v1.0

↓

v1.1

↓

v2.0

El historial permanece.

---

# Regla de Oro

Las campañas cuentan historias.

Las entidades almacenan conocimiento.

Nunca mezclar ambas responsabilidades.

Una campaña termina.

Una entidad permanece para siempre.

Todo nuevo contenido debe enriquecer una entidad existente o crear una nueva.

Así el Universo Historium crece sin duplicar información.
