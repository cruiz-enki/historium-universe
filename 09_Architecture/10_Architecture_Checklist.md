# HISTORIUM — ARCHITECTURE CHECKLIST

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Architecture Checklist

---

# Propósito

Este checklist valida si una pieza nueva puede entrar al Canon Oficial y al flujo de importación.

Debe usarse antes de declarar contenido como `official` o `published`.

---

# IDs

- [ ] El ID viene de `03_Knowledge/REGISTRY.yaml`.
- [ ] Usa formato `PREFIX_000001`.
- [ ] El prefijo existe.
- [ ] El ID no fue usado antes.
- [ ] `next_id` fue incrementado después de asignar.
- [ ] El ID no depende de idioma, nombre o campaña.

---

# Frontmatter

- [ ] Incluye todos los campos universales.
- [ ] Incluye campos específicos del tipo.
- [ ] `type` coincide con la taxonomía oficial.
- [ ] `status` es válido.
- [ ] `canonical` está definido.
- [ ] `version` está definido.

---

# Relaciones

- [ ] Las relaciones usan tipos oficiales.
- [ ] Las relaciones apuntan a IDs.
- [ ] No hay duplicados.
- [ ] No hay relaciones ambiguas.
- [ ] Cada relación ayuda a entender algo.
- [ ] Source y target respetan tipos permitidos.

---

# Museo

- [ ] La pieza alimenta una galería del Museo.
- [ ] Define nivel, estado o progreso.
- [ ] Los nodos incluyen `museum_updates`.
- [ ] Los desbloqueos son claros.
- [ ] El jugador puede entender qué ganó.

---

# Naming

- [ ] La carpeta respeta convención.
- [ ] El archivo usa `ID_EnglishName.md` si es entidad.
- [ ] El archivo no tiene acentos.
- [ ] El archivo no tiene espacios.
- [ ] El slug usa `snake_case`.

---

# Versionado

- [ ] La pieza tiene versión.
- [ ] La versión sigue reglas `v1.0`, `v1.1`, `v1.2`, `v2.0`.
- [ ] Cambios importantes tienen changelog.
- [ ] El ID se mantiene estable entre versiones.

---

# Importación

- [ ] Puede importarse sin intervención manual.
- [ ] No mezcla Canon con progreso de usuario.
- [ ] No depende de nombres visibles.
- [ ] Puede crear o actualizar registros por ID.
- [ ] No genera errores bloqueantes.

---

# Fuentes

- [ ] Tiene fuentes suficientes para su estado.
- [ ] Las fuentes están en `sources`.
- [ ] Las afirmaciones fuertes tienen respaldo.
- [ ] Las dudas están marcadas como debate o pendiente.

---

# Assets

- [ ] Los assets están referenciados.
- [ ] Los assets aumentan comprensión.
- [ ] No son decorativos sin propósito.
- [ ] Tienen relación con entidad, campaña o nodo.

---

# Consistencia narrativa

- [ ] Respeta voz Historium.
- [ ] No suena a Wikipedia.
- [ ] No suena a curso genérico.
- [ ] Tiene propósito narrativo.
- [ ] Conecta con el Museo Vivo.

---

# Regla Suprema

Si una pieza no puede conectarse a IDs, frontmatter, relaciones, Museo e importación, no está lista.
