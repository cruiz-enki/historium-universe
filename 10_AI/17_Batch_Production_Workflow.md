# HISTORIUM — BATCH PRODUCTION WORKFLOW

**Versión:** 1.0  
**Estado:** Oficial

---

# Propósito

Este documento define cómo producir campañas en lote sin romper el Canon.

La velocidad no debe destruir el Museo.

---

# Flujo

```text
Generar blueprint
↓
Crear entidades
↓
Mapear relaciones
↓
Generar nodos por bloques
↓
Validar
↓
Importar
↓
Revisión humana
↓
Publicación
```

---

# Generar blueprint

Definir campaña, pregunta histórica, capítulos, ritmo y entidades clave.

---

# Crear entidades

Buscar primero.

Crear solo lo que falta.

Asignar IDs desde `REGISTRY.yaml`.

---

# Mapear relaciones

Usar `RELATIONSHIP_TYPES.md`.

No aceptar relaciones libres.

---

# Generar nodos por bloques

Trabajar en grupos pequeños.

Validar antes de avanzar.

---

# Validar

Aplicar `13_Validation_Rules.md`.

---

# Importar

Solo Markdown válido pasa al importer.

---

# Revisión humana

Un editor aprueba Canon.

---

# Publicación

La app recibe contenido importado y validado.

---

# Regla Suprema

Producción en lote no significa producción automática sin criterio.
