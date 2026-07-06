# HISTORIUM — PROMPT COMPILER

**Versión:** 1.0  
**Estado:** Oficial

---

# Propósito

El Prompt Compiler convierte contexto estructurado en una instrucción final para modelos de IA.

El prompt final debe ser claro, limitado y verificable.

---

# Estructura del prompt

## System Context

Define identidad del modelo y reglas globales.

## Project Context

Explica Historium como Museo Vivo, RPG educativo, Knowledge Graph y universo persistente.

## Task Context

Describe la tarea exacta.

## Entity Context

Lista entidades, IDs, estados y restricciones.

## Relationship Context

Lista relaciones válidas y relaciones existentes.

## Output Contract

Define formato exacto de salida.

## Validation Checklist

Obliga al modelo a revisar su output.

## Do Not Do

Incluye prohibiciones desde `10_AI/15_AI_Do_Not_Do.md`.

---

# Regla Suprema

Un prompt compilado debe reducir improvisación.
