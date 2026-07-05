# HISTORIUM — SUPABASE MAPPING

**Versión:** 1.0

---

# Separación clave

GitHub contiene el Canon Oficial.

Supabase contiene estado operativo y progreso del usuario.

Nunca deben confundirse.

---

# Mapeo conceptual

- `campaigns` recibe campañas canon.
- `chapters` recibe capítulos canon.
- `nodes` recibe nodos jugables.
- `entities` recibe conocimiento base.
- `relationships` recibe conexiones del Grafo Histórico.
- `user_progress` recibe avance individual.
- `museum_unlocks` recibe desbloqueos por jugador.

---

# Regla de progreso

El progreso del usuario nunca modifica el Canon.

Solo registra qué parte del Canon fue descubierta, estudiada, dominada o completada por ese jugador.

---

# Regla Suprema

Supabase debe hacer jugable el Canon, no reescribirlo.
