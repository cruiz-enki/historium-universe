# HISTORIUM — ARCHITECTURE CHECKLIST

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Checklist

---

# Propósito

Este checklist valida que una pieza nueva respete la arquitectura del universo Historium.

Debe usarse antes de declarar contenido como canon.

---

# ID

- [ ] El ID viene de `03_Knowledge/REGISTRY.yaml`.
- [ ] Usa formato `PREFIX_000001`.
- [ ] El prefijo existe.
- [ ] El ID no fue usado antes.
- [ ] `next_id` fue incrementado después de asignar.

---

# Naming

- [ ] El título visible es claro.
- [ ] El slug técnico usa `snake_case`.
- [ ] El nombre no depende del idioma.
- [ ] El archivo está en la carpeta correcta.

---

# Frontmatter

- [ ] Tiene campos obligatorios.
- [ ] El tipo es oficial.
- [ ] El estado editorial es válido.
- [ ] La versión está definida.
- [ ] La galería del Museo está definida si aplica.

---

# Knowledge Graph

- [ ] Tiene relaciones útiles.
- [ ] Las relaciones usan IDs.
- [ ] No duplica relaciones existentes.
- [ ] No usa relaciones ambiguas sin justificación.
- [ ] Respeta source_types y target_types.

---

# Museo

- [ ] Hace crecer una parte del Museo.
- [ ] Define nivel o progreso.
- [ ] Tiene desbloqueos claros si aplica.
- [ ] Puede mostrarse al jugador con sentido.

---

# Supabase

- [ ] Puede importarse sin transformación manual.
- [ ] No mezcla Canon con progreso de usuario.
- [ ] Tiene versión rastreable.
- [ ] Puede actualizarse por ID.

---

# Tono

- [ ] Mantiene voz Historium.
- [ ] No suena a Wikipedia.
- [ ] No suena a curso genérico.
- [ ] Tiene claridad premium.

---

# Regla Suprema

Si una pieza no puede conectarse al Museo Vivo y al Knowledge Graph, no está lista.
