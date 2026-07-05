# HISTORIUM — IMPORT VALIDATION

**Versión:** 1.0

---

# Propósito

La validación protege el Canon antes de convertirlo en experiencia jugable.

---

# Validaciones obligatorias

- ID único.
- Tipo permitido.
- Estado editorial válido.
- Versión presente.
- Relaciones válidas.
- Galería de Museo existente.
- Campos obligatorios completos.
- Markdown sin secciones rotas.
- Assets referenciados existentes o marcados como pendientes.

---

# Errores bloqueantes

- ID duplicado.
- Tipo desconocido.
- Relación hacia entidad inexistente.
- Nodo sin actualización de Museo.
- Campaña sin capítulos.
- Entidad sin resumen corto.

---

# Regla Suprema

Si un jugador puede recibir una experiencia rota, el importer debe detenerse.
