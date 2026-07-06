# HISTORIUM — REPOSITORY STATUS

**Fecha:** 2026-07-05  
**Estado:** Fundación reorganizada y sincronizada en GitHub

---

# Qué se creó

- Estructura final del Canon Oficial.
- Carpeta `02_Specifications/` con especificaciones hasta `26_Location_Spec.md`.
- Nuevas galerías de conocimiento: Events, Wars, Regions, Routes, Laws, Organizations, Dynasties, Languages, Currencies, Myths y Locations.
- `03_Knowledge/RELATIONSHIP_TYPES.md`.
- Campañas base: Greece Classical, Egypt Pharaonic, Rome Empire y Alexander The Great.
- Subcarpetas de prompts: Images, Audio, Video, Maps, Characters y Artifacts.
- Documentación del importer.
- `07_Assets/README.md`.
- Carpeta `08_Templates/` con plantillas oficiales.
- README principal mejorado.
- README internos para carpetas principales.

---

# Qué se reorganizó

- `02_Campaigns/` fue reemplazada por `04_Campaigns/`.
- `04_Templates/` fue reemplazada por `08_Templates/`.
- `02_Specifications/` quedó como carpeta oficial para todos los archivos `*_Spec.md`.
- `07_Assets/` quedó creada con `README.md`.
- `README.md` principal refleja la arquitectura final:
  `00_Biblia_Editorial`, `01_Game_Design`, `02_Specifications`, `03_Knowledge`, `04_Campaigns`, `05_Prompts`, `06_Importer`, `07_Assets`, `08_Templates`.

---

# Fase de arquitectura del Knowledge Graph

- `09_Architecture/` quedó completada como capa de arquitectura del universo.
- `01_ID_System.md` documenta `03_Knowledge/REGISTRY.yaml` como fuente de verdad para IDs.
- `02_Naming_Convention.md` define carpetas PascalCase plural para entidades y archivos `ID_EnglishName.md`.
- `03_Frontmatter_Spec.md` define frontmatter universal y específico para Character, City, Battle, Concept, Document, Artifact, Campaign, Chapter y Node.
- `04_Knowledge_Graph.md` define entidad, relación, campaña, nodo, Museo, taxonomía y reglas del grafo.
- `05_Entity_Lifecycle.md` define estados `draft`, `research`, `review`, `official`, `published`, `deprecated` y `archived`.
- `06_Versioning.md` define reglas `v1.0`, `v1.1`, `v1.2` y `v2.0`.
- `07_Supabase_Model.md` define el modelo conceptual de entidades, relaciones, campañas, nodos, Museo y progreso de usuario.
- `08_Import_Workflow.md` define el flujo Markdown → Validation → Parse frontmatter → Resolve IDs → Supabase → Relationships → Museum unlocks → App.
- `09_Museum_Data_Model.md` define niveles 0 a 4 y campos de progreso.
- `10_Architecture_Checklist.md` valida IDs, frontmatter, relaciones, Museo, naming, versionado, importación, fuentes, assets y consistencia narrativa.
- `03_Knowledge/RELATIONSHIP_TYPES.md` quedó tipificado con relaciones oficiales en `snake_case`.
- `03_Knowledge/REGISTRY.yaml` incluye prefijos oficiales para entidades, lugares, eventos, ideas, objetos y estructura de campaña.
- Se documentó la separación GitHub Canon Oficial / Supabase estado activo y progreso de usuario.

---

# Qué falta

- Poblar campañas reales con capítulos y nodos.
- Crear primeras entidades canon dentro de `03_Knowledge/`.
- Definir IDs oficiales globales.
- Conectar specs con esquemas técnicos definitivos del importer.
- Crear prompts visuales finales por estilo histórico.
- Añadir fuentes y referencias por entidad.

---

# Estructura final

```text
Historium-Universe/
  00_Biblia_Editorial/
  01_Game_Design/
  02_Specifications/
  03_Knowledge/
  04_Campaigns/
  05_Prompts/
  06_Importer/
  07_Assets/
  08_Templates/
  09_Architecture/
```

---

# Próximos pasos recomendados

1. Definir convención global de IDs.
2. Crear la primera campaña canon: Greece Classical.
3. Crear las primeras entidades: Pisístrato, Atenas, Solón, Clístenes, Tiranía y Democracia.
4. Validar el flujo Node → Museo → Supabase.
5. Crear prompts visuales base para Grecia Clásica.

---

# Riesgos o decisiones pendientes

- Decidir si los specs tendrán frontmatter real además de ejemplos YAML.
- Definir qué entidades serán premium y cuáles gratuitas.
- Determinar nivel de profundidad de fuentes históricas por rareza.
- Alinear nombres finales entre Markdown, importer y Supabase.
- Decidir política de idiomas para nombres históricos.

---

# Nota editorial

La fundación ya permite que Historium funcione como universo persistente.

El siguiente reto no es crear más carpetas.

Es empezar a poblar el Museo Vivo con entidades canónicas de alto nivel.
