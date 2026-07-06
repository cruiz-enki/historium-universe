# HISTORIUM — ENTITY EXTRACTION RULES

**Versión:** 1.0  
**Estado:** Oficial

---

# Propósito

La IA debe detectar entidades nuevas sin duplicar el Canon.

---

# Tipos clave

- Character
- City
- Battle
- Concept
- Document
- Artifact
- War
- Monument
- Religion
- Technology

---

# Proceso

1. Detectar candidatos.
2. Buscar si ya existen.
3. Comparar nombres alternativos.
4. Revisar carpeta correcta.
5. Consultar `03_Knowledge/REGISTRY.yaml`.
6. Proponer ID solo si la entidad es nueva.
7. Incrementar `next_id` después de crear.

---

# No crear entidad si

- ya existe con otro nombre,
- solo es una mención pasajera,
- no alimenta el Museo,
- no tendrá relaciones útiles.

---

# Output recomendado

```yaml
new_entities:
  - type: Character
    proposed_id: CHAR_000001
    title: ""
    reason: ""
```

---

# Regla Suprema

Crear una entidad es ampliar el universo, no llenar una lista.
