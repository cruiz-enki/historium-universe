# HISTORIUM — REPOSITORY STATUS

**Fecha:** 2026-07-05  
**Estado:** Fundación completada localmente

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
