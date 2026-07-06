# HISTORIUM — RELATIONSHIP TYPES

**Versión:** 1.0  
**Estado:** Oficial  
**Tipo:** Knowledge Graph Specification

---

# Propósito

Este documento define las relaciones oficiales del Knowledge Graph de Historium.

Las relaciones deben estar tipificadas.

Deben ser legibles para humanos.

Deben ser validables por el importer.

Deben alimentar el Museo Vivo.

---

# Reglas

- Usar nombres técnicos en inglés `snake_case`.
- Usar IDs como origen y destino.
- Evitar relaciones duplicadas.
- Evitar relaciones ambiguas.
- Usar `connected_to` solo cuando no exista una relación más precisa.
- Toda relación debe poder explicarse al jugador.

---

# Relationship Registry

```yaml
governed:
  label: "Gobernó"
  description: "Indica que una persona gobernó una ciudad, imperio, reino, república u organización política."
  source_types:
    - Character
  target_types:
    - City
    - Empire
    - Kingdom
    - Republic
    - City-State
    - Organization
  inverse: was_governed_by
  example:
    source: CHAR_000001
    target: CITY_000001

founded:
  label: "Fundó"
  description: "Indica que una persona, grupo o entidad política fundó una ciudad, organización, dinastía o institución."
  source_types:
    - Character
    - Civilization
    - Empire
    - Organization
  target_types:
    - City
    - Organization
    - Dynasty
    - Kingdom
    - Republic
  inverse: was_founded_by
  example:
    source: CHAR_000002
    target: CITY_000002

conquered:
  label: "Conquistó"
  description: "Indica control adquirido mediante campaña militar o expansión política."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Civilization
    - Organization
  target_types:
    - City
    - Region
    - Empire
    - Kingdom
    - Civilization
  inverse: was_conquered_by
  example:
    source: EMP_000001
    target: REG_000001

destroyed:
  label: "Destruyó"
  description: "Indica destrucción material, política o institucional significativa."
  source_types:
    - Character
    - Empire
    - Kingdom
    - War
    - Battle
    - Event
  target_types:
    - City
    - Monument
    - Organization
    - Empire
    - Historical Object
  inverse: was_destroyed_by
  example:
    source: WAR_000001
    target: CITY_000003

rebuilt:
  label: "Reconstruyó"
  description: "Indica reconstrucción física, política o simbólica después de destrucción o crisis."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Organization
    - Civilization
  target_types:
    - City
    - Monument
    - Organization
    - Historical Object
  inverse: was_rebuilt_by
  example:
    source: EMP_000002
    target: MON_000001

born_in:
  label: "Nació en"
  description: "Conecta una persona con su lugar de nacimiento."
  source_types:
    - Character
  target_types:
    - City
    - Location
    - Region
  inverse: birthplace_of
  example:
    source: CHAR_000003
    target: CITY_000004

died_in:
  label: "Murió en"
  description: "Conecta una persona con su lugar de muerte."
  source_types:
    - Character
  target_types:
    - City
    - Location
    - Region
  inverse: deathplace_of
  example:
    source: CHAR_000004
    target: LOC_000001

participated_in:
  label: "Participó en"
  description: "Indica participación directa en una batalla, guerra, evento, tratado, expedición o revolución."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Civilization
  target_types:
    - Battle
    - War
    - Event
    - Treaty
    - Expedition
    - Revolution
  inverse: had_participant
  example:
    source: CHAR_000005
    target: BAT_000001

commanded:
  label: "Comandó"
  description: "Indica mando militar o estratégico."
  source_types:
    - Character
  target_types:
    - Battle
    - War
    - Siege
    - Expedition
    - Organization
  inverse: was_commanded_by
  example:
    source: CHAR_000006
    target: BAT_000002

won:
  label: "Ganó"
  description: "Indica victoria reconocida en batalla, guerra, disputa política o competición histórica."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Civilization
  target_types:
    - Battle
    - War
    - Siege
    - Event
  inverse: was_won_by
  example:
    source: EMP_000003
    target: WAR_000002

lost:
  label: "Perdió"
  description: "Indica derrota reconocida en batalla, guerra, disputa política o evento histórico."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Civilization
  target_types:
    - Battle
    - War
    - Siege
    - Event
  inverse: was_lost_by
  example:
    source: EMP_000004
    target: BAT_000003

allied_with:
  label: "Aliado con"
  description: "Indica alianza política, militar, económica o diplomática."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - City-State
    - Organization
    - Civilization
  target_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - City-State
    - Organization
    - Civilization
  inverse: allied_with
  example:
    source: EMP_000005
    target: KING_000001

enemy_of:
  label: "Enemigo de"
  description: "Indica rivalidad o enemistad política, militar, personal o cultural."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - City-State
    - Organization
    - Civilization
  target_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - City-State
    - Organization
    - Civilization
  inverse: enemy_of
  example:
    source: CHAR_000007
    target: CHAR_000008

teacher_of:
  label: "Maestro de"
  description: "Indica relación de enseñanza directa o tradición intelectual reconocida."
  source_types:
    - Character
  target_types:
    - Character
  inverse: student_of
  example:
    source: CHAR_000009
    target: CHAR_000010

student_of:
  label: "Alumno de"
  description: "Indica que una persona fue estudiante, discípulo o aprendiz de otra."
  source_types:
    - Character
  target_types:
    - Character
  inverse: teacher_of
  example:
    source: CHAR_000010
    target: CHAR_000009

parent_of:
  label: "Padre o madre de"
  description: "Indica relación parental directa."
  source_types:
    - Character
  target_types:
    - Character
  inverse: child_of
  example:
    source: CHAR_000011
    target: CHAR_000012

child_of:
  label: "Hijo de"
  description: "Indica filiación directa."
  source_types:
    - Character
  target_types:
    - Character
  inverse: parent_of
  example:
    source: CHAR_000012
    target: CHAR_000011

predecessor_of:
  label: "Predecesor de"
  description: "Indica que una persona, dinastía, estado, idea o institución antecede a otra."
  source_types:
    - Character
    - Dynasty
    - Empire
    - Kingdom
    - Republic
    - Concept
    - Organization
  target_types:
    - Character
    - Dynasty
    - Empire
    - Kingdom
    - Republic
    - Concept
    - Organization
  inverse: successor_of
  example:
    source: CHAR_000013
    target: CHAR_000014

successor_of:
  label: "Sucesor de"
  description: "Indica continuidad posterior en cargo, dinastía, institución, estado o idea."
  source_types:
    - Character
    - Dynasty
    - Empire
    - Kingdom
    - Republic
    - Concept
    - Organization
  target_types:
    - Character
    - Dynasty
    - Empire
    - Kingdom
    - Republic
    - Concept
    - Organization
  inverse: predecessor_of
  example:
    source: CHAR_000014
    target: CHAR_000013

inspired:
  label: "Inspiró"
  description: "Indica inspiración cultural, política, religiosa, tecnológica o artística."
  source_types:
    - Character
    - Concept
    - Religion
    - Philosophy
    - Document
    - Event
    - Civilization
  target_types:
    - Character
    - Concept
    - Religion
    - Philosophy
    - Document
    - Event
    - Civilization
  inverse: was_inspired_by
  example:
    source: CON_000001
    target: DOC_000001

influenced:
  label: "Influyó en"
  description: "Indica influencia histórica significativa sin implicar causalidad única."
  source_types:
    - Character
    - Concept
    - Religion
    - Philosophy
    - Law
    - Technology
    - Document
    - Event
    - Civilization
  target_types:
    - Character
    - Concept
    - Religion
    - Philosophy
    - Law
    - Technology
    - Document
    - Event
    - Civilization
  inverse: was_influenced_by
  example:
    source: LAW_000001
    target: REP_000001

created:
  label: "Creó"
  description: "Indica creación de un objeto, documento, institución, obra, tecnología o concepto formal."
  source_types:
    - Character
    - Organization
    - Civilization
  target_types:
    - Artifact
    - Document
    - Technology
    - Law
    - Organization
    - Concept
    - Historical Object
  inverse: was_created_by
  example:
    source: CHAR_000015
    target: DOC_000002

codified:
  label: "Codificó"
  description: "Indica formalización de leyes, normas, escritura, doctrina o sistema."
  source_types:
    - Character
    - Organization
    - Empire
    - Kingdom
    - Republic
  target_types:
    - Law
    - Religion
    - Language
    - Concept
    - Document
  inverse: was_codified_by
  example:
    source: CHAR_000016
    target: LAW_000001

wrote:
  label: "Escribió"
  description: "Indica autoría de documento, obra, ley, crónica o texto histórico."
  source_types:
    - Character
    - Organization
  target_types:
    - Document
    - Law
    - Myth
    - Philosophy
  inverse: was_written_by
  example:
    source: CHAR_000017
    target: DOC_000003

signed:
  label: "Firmó"
  description: "Indica firma, ratificación o participación formal en un documento o tratado."
  source_types:
    - Character
    - Empire
    - Kingdom
    - Republic
    - Organization
  target_types:
    - Document
    - Treaty
    - Law
  inverse: was_signed_by
  example:
    source: CHAR_000018
    target: TREAT_000001

occurred_in:
  label: "Ocurrió en"
  description: "Conecta un evento con el lugar donde ocurrió."
  source_types:
    - Event
    - War
    - Battle
    - Siege
    - Treaty
    - Revolution
    - Discovery
    - Expedition
  target_types:
    - City
    - Location
    - Region
    - River
    - Mountain
    - Sea
  inverse: hosted_event
  example:
    source: BAT_000004
    target: LOC_000002

located_in:
  label: "Ubicado en"
  description: "Indica ubicación geográfica o espacial."
  source_types:
    - City
    - Location
    - Monument
    - River
    - Mountain
    - Sea
    - Artifact
    - Historical Object
  target_types:
    - City
    - Location
    - Region
    - Empire
    - Kingdom
    - Republic
  inverse: contains_location
  example:
    source: MON_000001
    target: CITY_000001

part_of:
  label: "Parte de"
  description: "Indica relación jerárquica o de pertenencia estructural."
  source_types:
    - City
    - Location
    - Region
    - Monument
    - Organization
    - Dynasty
    - Chapter
    - Node
  target_types:
    - Region
    - City
    - Civilization
    - Empire
    - Kingdom
    - Republic
    - Campaign
    - Arc
    - Chapter
  inverse: contains
  example:
    source: LOC_000003
    target: CITY_000001

capital_of:
  label: "Capital de"
  description: "Indica que una ciudad funciona como capital política o administrativa."
  source_types:
    - City
  target_types:
    - Empire
    - Kingdom
    - Republic
    - Civilization
    - Region
  inverse: has_capital
  example:
    source: CITY_000005
    target: EMP_000006

belonged_to:
  label: "Perteneció a"
  description: "Indica pertenencia histórica de objeto, territorio, documento o institución."
  source_types:
    - Artifact
    - Historical Object
    - Document
    - City
    - Region
    - Organization
  target_types:
    - Character
    - City
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Civilization
  inverse: owned_or_contained
  example:
    source: ART_000001
    target: CHAR_000019

used_by:
  label: "Usado por"
  description: "Indica uso histórico de tecnología, objeto, moneda, lengua, ruta o documento."
  source_types:
    - Artifact
    - Historical Object
    - Technology
    - Currency
    - Language
    - Route
    - Document
  target_types:
    - Character
    - City
    - Civilization
    - Empire
    - Kingdom
    - Republic
    - Organization
  inverse: used
  example:
    source: CUR_000001
    target: CITY_000001

discovered_by:
  label: "Descubierto por"
  description: "Indica descubrimiento, hallazgo o identificación histórica."
  source_types:
    - Artifact
    - Document
    - Historical Object
    - Location
    - Discovery
  target_types:
    - Character
    - Organization
    - Expedition
  inverse: discovered
  example:
    source: ART_000002
    target: CHAR_000020

preserved_in:
  label: "Preservado en"
  description: "Indica lugar o institución donde se conserva un objeto, documento o monumento."
  source_types:
    - Artifact
    - Document
    - Historical Object
    - Monument
  target_types:
    - City
    - Location
    - Organization
  inverse: preserves
  example:
    source: DOC_000004
    target: ORG_000001

evolved_into:
  label: "Evolucionó hacia"
  description: "Indica transformación histórica de una entidad, idea, lengua, institución o estado en otra."
  source_types:
    - Concept
    - Language
    - Religion
    - Philosophy
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Technology
  target_types:
    - Concept
    - Language
    - Religion
    - Philosophy
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Technology
  inverse: evolved_from
  example:
    source: CON_000002
    target: CON_000003

opposed:
  label: "Se opuso a"
  description: "Indica oposición política, militar, religiosa, filosófica o conceptual."
  source_types:
    - Character
    - Concept
    - Religion
    - Philosophy
    - Empire
    - Kingdom
    - Republic
    - Organization
  target_types:
    - Character
    - Concept
    - Religion
    - Philosophy
    - Empire
    - Kingdom
    - Republic
    - Organization
  inverse: opposed
  example:
    source: CON_000004
    target: CON_000005

replaced:
  label: "Reemplazó"
  description: "Indica sustitución histórica de institución, sistema, tecnología, moneda o autoridad."
  source_types:
    - Concept
    - Technology
    - Currency
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Law
  target_types:
    - Concept
    - Technology
    - Currency
    - Empire
    - Kingdom
    - Republic
    - Organization
    - Law
  inverse: was_replaced_by
  example:
    source: LAW_000002
    target: LAW_000001

caused:
  label: "Causó"
  description: "Indica causalidad histórica significativa."
  source_types:
    - Event
    - War
    - Battle
    - Treaty
    - Revolution
    - Concept
    - Law
    - Technology
  target_types:
    - Event
    - War
    - Battle
    - Treaty
    - Revolution
    - Concept
    - Law
    - Technology
  inverse: consequence_of
  example:
    source: EVT_000001
    target: REV_000001

consequence_of:
  label: "Consecuencia de"
  description: "Indica que una entidad o evento deriva de una causa histórica anterior."
  source_types:
    - Event
    - War
    - Battle
    - Treaty
    - Revolution
    - Concept
    - Law
    - Technology
  target_types:
    - Event
    - War
    - Battle
    - Treaty
    - Revolution
    - Concept
    - Law
    - Technology
  inverse: caused
  example:
    source: REV_000001
    target: EVT_000001

connected_to:
  label: "Conectado con"
  description: "Indica conexión editorial útil cuando todavía no existe una relación más específica."
  source_types:
    - Any
  target_types:
    - Any
  inverse: connected_to
  example:
    source: CHAR_000021
    target: CON_000006
```

---

# Intensidad

Toda relación puede declarar intensidad:

```text
low
medium
high
decisive
```

La intensidad define prioridad de visualización.

---

# Visibilidad

Toda relación puede tener visibilidad:

```text
public
hidden
premium
secret
```

Las relaciones `hidden` y `secret` permiten descubrimientos del Museo.

---

# Regla Suprema

Una relación solo entra al grafo si ayuda a entender mejor la Historia.
