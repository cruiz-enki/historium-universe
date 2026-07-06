# HISTORIUM — RELATIONSHIP EXTRACTION RULES

**Versión:** 1.0  
**Estado:** Oficial

---

# Propósito

La IA debe extraer relaciones válidas para el Knowledge Graph.

No puede crear relaciones libres.

---

# Reglas

- Usar `03_Knowledge/RELATIONSHIP_TYPES.md`.
- Usar IDs.
- Validar `source_type`.
- Validar `target_type`.
- Evitar duplicados.
- Evitar relaciones débiles.
- Declarar evidencia.

---

# Formato

```yaml
relationships:
  - type: governed
    source: CHAR_000001
    target: CITY_000001
    confidence: high
    visibility: public
    evidence_note: ""
```

---

# Rechazar si

- usa nombres en lugar de IDs,
- el tipo no existe,
- el origen/destino no cumple tipos,
- la conexión no aporta comprensión.

---

# Regla Suprema

Una relación debe revelar sentido histórico.
