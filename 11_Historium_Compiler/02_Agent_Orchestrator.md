# HISTORIUM — AGENT ORCHESTRATOR

**Versión:** 1.0  
**Estado:** Oficial

---

# Propósito

El Orchestrator decide qué agente actúa, en qué orden y con qué contexto.

Ningún agente debe trabajar solo con intuición.

---

# Research Agent

Función: reunir contexto histórico, claims y dudas.

Input: brief, periodo, entidades iniciales.

Output: notas clasificadas en hecho, interpretación, debate y mito.

Reglas: citar incertidumbre.

No debe: inventar fuentes.

---

# Entity Agent

Función: detectar y resolver entidades.

Input: texto, brief, Knowledge folders, Registry.

Output: entidades existentes y propuestas nuevas.

Reglas: reutilizar IDs.

No debe: duplicar entidades.

---

# Relationship Agent

Función: mapear relaciones.

Input: entidades, Relationship Types.

Output: YAML de relaciones válidas.

Reglas: validar source y target.

No debe: crear relaciones libres.

---

# Narrative Agent

Función: producir experiencia narrativa Historium.

Input: outline, voz, specs, entidades.

Output: borrador narrativo.

Reglas: tono premium y Museo.

No debe: sonar enciclopédico.

---

# Curiosity Agent

Función: crear curiosidades que expanden contexto.

Input: nodo, entidades, debates.

Output: curiosidades públicas y premium.

No debe: repetir el nodo.

---

# Quiz Agent

Función: crear evaluación de comprensión.

Input: nodo, insight, relaciones.

Output: preguntas con explicación.

No debe: crear trivia vacía.

---

# Museum Agent

Función: definir actualizaciones del Museo.

Input: nodo, entidades, progresión.

Output: `museum_updates`.

No debe: entregar recompensas sin conocimiento.

---

# Visual Prompt Agent

Función: crear prompts de imagen.

Input: guía visual, entidad, escena.

Output: prompts sin texto ni anacronismos.

No debe: mezclar épocas.

---

# Audio Prompt Agent

Función: crear prompts de narración/TTS.

Input: texto, tono, pronunciación.

Output: guía de voz.

No debe: ignorar nombres históricos.

---

# Validator Agent

Función: revisar salida.

Input: Markdown generado.

Output: errores, advertencias y aprobación.

No debe: aprobar por estilo si falla estructura.

---

# Publisher Agent

Función: preparar publicación.

Input: Markdown validado.

Output: commit, PR o importación.

No debe: publicar sin revisión humana.
