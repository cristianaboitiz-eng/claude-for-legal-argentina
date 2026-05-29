# Perfil de práctica · Derecho administrativo · Provincia de Tucumán

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Tucumán.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.

---

## Configuración inicial - completar antes de usar

**PROVINCIA:** Provincia de Tucumán

**FUERO_HABITUAL:** [COMPLETAR: denominación exacta del juzgado/sala y nominación. Ej: "Juzgado en lo Contencioso Administrativo de la Xª Nominación, Centro Judicial Capital" / "Sala I (o II o III) de la Cámara en lo Contencioso Administrativo, Tucumán". Los Juzgados de Primera Instancia en lo Contencioso Administrativo actúan en primera instancia; la Cámara en lo Contencioso Administrativo (tres Salas) es la alzada; la Corte Suprema de Justicia de Tucumán es el tribunal superior.]

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen. Ej: "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, contratación pública, habilitaciones municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: ej. "Ministerio de Salud Tucumán, SIPROSA, APUNT, DGR, Municipalidad de San Miguel de Tucumán".]

---

## Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Tucumán: procedimiento administrativo ante la Administración provincial y municipal (Ley 4537), recursos administrativos en sede provincial, proceso contencioso administrativo ante los Juzgados en lo Contencioso Administrativo y la Cámara en lo Contencioso Administrativo (Ley 6205), responsabilidad del Estado, empleo público y contratación pública provincial.

**Estructura judicial:** Tucumán tiene un fuero contencioso administrativo propio con primera instancia diferenciada (Juzgados CA) y alzada especializada (Cámara CA con tres Salas). Esto lo distingue de Mendoza y Entre Ríos (que tienen tribunal superior como única instancia) y lo asemeja a PBA y Córdoba.

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Tucumán (ARCA/ex AFIP, ANSES), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal tucumana, aplica este perfil.

**Tercer nivel - organismos municipales:** los actos de los municipios tucumanos son impugnables ante el fuero contencioso administrativo provincial (art. 32 Ley 6238 y Ley 6205). La notificación de la demanda cuando el demandado es un municipio se hace al Intendente (art. 33 inc. c Ley 6205). Verificar si el municipio tiene ordenanza de procedimiento propio que regule el agotamiento de la vía antes de ocurrir al fuero judicial.

---

## Normativa de procedimiento administrativo provincial

### Ley de procedimiento administrativo Tucumán

- **Norma principal:** Ley 4537 (Ley de Procedimiento Administrativo de la Provincia de Tucumán), promulgada el 31/08/1976, modificada por Ley 6311 (1991) y otras
- **Texto vigente:** consultar el Registro Oficial de Leyes y Decretos de Tucumán: https://leyes.tucuman.gob.ar y el portal del Poder Judicial: https://www.justucuman.gov.ar. Texto consolidado disponible.
- **Articulado clave:** art. 3 (principios), art. 38 (plazos - días hábiles administrativos), art. 39 (pérdida del derecho por vencimiento de plazos recursivos), art. 43 (requisitos del acto administrativo), arts. 44-65 (recursos administrativos), art. 47 (suspensión de ejecutoriedad en sede administrativa).

```
[VERIFICAR VIGENCIA: Ley 4537 LPA Tucumán (mod. Ley 6311 y otras) - consultar https://leyes.tucuman.gob.ar - verificar modificaciones posteriores a mayo 2026]
```

### Régimen de silencio administrativo Tucumán

- **Regla general:** silencio negativo (denegatoria tácita). Vencidos los plazos para resolver sin pronunciamiento expreso, el silencio habilita los recursos correspondientes o la acción judicial, según la instancia.
- **Constitución provincial art. 19:** el art. 9 inc. d Ley 6205 menciona expresamente el silencio con sentido desestimatorio "por haber transcurrido el plazo previsto por el artículo 19 de la Constitución de la Provincia, respecto de peticiones fundadas en derecho, recursos o reclamos". Verificar el plazo constitucional vigente.
- **Sin reforma análoga al Dec 971/2024 nacional:** Tucumán no adoptó el régimen de silencio positivo de la Ley 27.742 nacional. El silencio positivo aplica solo ante la Administración nacional.

```
[VERIFICAR SILENCIO TUCUMÁN: Ley 4537 + art. 19 Constitución Tucumán - silencio negativo por regla general - verificar plazo constitucional que habilita la vía judicial por denegación tácita]
```

### Elementos esenciales del acto administrativo Tucumán

El art. 43 Ley 4537 enumera los requisitos esenciales del acto administrativo:
1. Que emane de autoridad competente
2. Que tenga sustento en los hechos y antecedentes que le sirvan de causa
3. Que su objeto sea cierto y física y jurídicamente posible
4. Procedimiento: cumplimiento de trámites esenciales previos
5. Motivación: expresar las razones del dictado (exigida expresamente; puede omitirse excepcionalmente para actos que no incidan en relaciones jurídicas con administrados)
6. Finalidad: adecuada a la causa del acto y al ordenamiento
7. Que se exteriorice por instrumento idóneo, expresamente y por escrito, indicando lugar y fecha

**Proporcionalidad:** las medidas del acto deben ser "proporcionalmente adecuadas" a la finalidad. El art. 43 Ley 4537 exige proporcionalidad como elemento del acto.

**Vicios del acto:** la Ley 4537 regula nulidades absolutas y relativas con estructura análoga al régimen federal. Verificar articulado específico.

**Dictamen de Fiscalía de Estado:** es preceptivo para ciertos actos (ej. nombramientos en el empleo público, art. 6 Ley 5473). Su omisión cuando es obligatorio puede configurar vicio de procedimiento.

### Recursos administrativos Tucumán (Ley 4537)

**Recurso de reconsideración (arts. 44 y ss. Ley 4537):**
- Plazo: 15 días hábiles administrativos desde la notificación del acto
- Ante: el mismo órgano que dictó el acto
- Efecto: interrumpe el plazo para interponer el recurso jerárquico (art. 40 Ley 4537)

**Recurso jerárquico (arts. 55 y ss. Ley 4537):**
- Plazo: 15 días hábiles desde la notificación de la denegatoria de la reconsideración, o desde el silencio de aquélla. Puede interponerse subsidiariamente con la reconsideración.
- Ante: el superior jerárquico del órgano emisor, recorriendo la línea hasta el Gobernador o ministro competente
- Agota la vía: sí, cuando es resuelto por el Poder Ejecutivo. Con esta decisión queda agotada la vía administrativa (art. 55 in fine Ley 4537).

**Recurso de alzada (art. 68 Ley 4537):**
- Procede contra actos administrativos definitivos emanados del órgano superior del ente autárquico
- Plazo: 15 días hábiles desde la notificación
- Solo puede fundarse en ilegitimidad del acto (no en oportunidad, mérito o conveniencia)
- Ante: el Poder Ejecutivo
- Si procede: el PE se limita a revocar el acto impugnado, pudiendo modificarlo o sustituirlo excepcionalmente por razones de interés público

**Pérdida del derecho recursivo (art. 39 Ley 4537):**
Una vez vencidos los plazos para interponer recursos administrativos, se pierde el derecho a articularlos. La presentación extemporánea **no** será considerada como denuncia de ilegitimidad (a diferencia del régimen federal anterior). Excepción: actos contrarios al orden público o a las buenas costumbres.

**Sin reforma análoga al Decreto 695/2024 nacional:** Tucumán no duplicó los plazos de recursos administrativos. El plazo de la Ley 4537 para la reconsideración y el jerárquico es de 15 días hábiles administrativos. No aplicar los plazos federales reformados.

```
[ALERTA PLAZO FATAL: recurso de reconsideración - Ley 4537 - 15 días hábiles administrativos desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico - Ley 4537 - 15 días hábiles desde denegatoria de la reconsideración o desde el silencio - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de alzada - Ley 4537 art. 68 - 15 días hábiles desde notificación - solo por ilegitimidad - ante PE - vencimiento: calcular]
```

### Agotamiento de la vía administrativa Tucumán

- **Regla general:** es requisito previo de admisibilidad de la acción contencioso administrativa (art. 12 Ley 6205), salvo excepciones expresas.
- **Excepciones al agotamiento (art. 13 Ley 6205):**
  - Repetición de lo pagado a requerimiento de la Administración luego de agotada la vía de determinación
  - Únicamente daños y perjuicios causados por actos o hechos administrativos, si el monto no está determinado en norma legal (no requiere impugnación recursiva previa del acto generador)
  - Anulación de un acto si la pretensión se funda exclusivamente en la inconstitucionalidad de la norma que aplica ese acto
  - Juicio promovido como consecuencia de otro anterior en que el actor fue demandado
  - Hacer cesar un hecho administrativo ilegítimo
  - Cuando medie una clara e indubitable conducta de la Administración que haga presumir la ineficacia cierta del procedimiento, o cuando la reclamación previa resulte inidónea para preservar el derecho
- **Límite de pretensiones (art. 12 Ley 6205):** no pueden articularse en sede judicial pretensiones no planteadas en sede administrativa. Excepción: pueden deducirse las pretensiones no planteadas pero resueltas, o las planteadas y no resueltas.
- **Fiscalía de Estado:** interviene en los recursos que resuelve el PE y en el proceso judicial como representante del Estado provincial.

```
[VERIFICAR AGOTAMIENTO DE VÍA TUCUMÁN: Ley 4537 - reconsideración + jerárquico ante PE (agota la vía) - para entes autárquicos: alzada ante PE (solo por ilegitimidad) - art. 12 Ley 6205: no plantear en sede judicial lo no planteado en sede administrativa]
```

### Tabla unificada de plazos - sede administrativa

| Recurso / instituto | Plazo | Tipo de días | Norma | Observación |
|---------------------|-------|--------------|-------|-------------|
| Reconsideración | 15 días | Hábiles administrativos | Ley 4537 | Interrumpe el plazo para el jerárquico |
| Jerárquico | 15 días | Hábiles administrativos | Ley 4537 arts. 55 y ss. | Desde denegatoria de reconsideración o silencio; puede interponerse subsidiariamente |
| Alzada (entes autárquicos) | 15 días | Hábiles administrativos | Ley 4537 art. 68 | Solo por ilegitimidad; ante PE |
| Silencio / denegatoria tácita | - | - | Ley 6205 art. 9 inc. d + art. 19 Const. Tucumán | Verificar plazo constitucional vigente |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial, no días hábiles judiciales.

---

## Control judicial contencioso administrativo

### Código Procesal Administrativo Tucumán

- **Norma:** Ley 6205 (Código Procesal Administrativo de la Provincia de Tucumán), promulgada el 23/08/1991, texto actualizado con las modificaciones introducidas por Leyes 6242, 6282 y 6944. Texto consolidado por Ley 9924 (Digesto Jurídico).
- **Texto vigente:** https://www.justucuman.gov.ar/leyes-decretos (texto consolidado disponible). Verificar modificaciones posteriores a mayo 2026.
- **Subsidiariedad:** el Código Procesal Civil y Comercial de Tucumán se aplica supletoriamente en lo no previsto (art. 89 y concordantes Ley 6205).

### Plazo de caducidad para accionar judicialmente

**Este es el dato más crítico del perfil.**

- **Proceso ordinario:** 90 días hábiles judiciales desde la notificación del acto expreso que agote la instancia administrativa (art. 9 Ley 6205)
- **Proceso sumario:** 10 días hábiles judiciales desde la notificación del acto que agota la instancia administrativa (art. 9 párr. 3 Ley 6205). El proceso sumario tiene reglas específicas (art. 86 y ss. Ley 6205).
- **Recurso previsto por norma especial:** cuando por norma expresa el caso deba incoarse por vía de recurso, el plazo es de 30 días hábiles judiciales (art. 9 párr. 4 Ley 6205)
- **Naturaleza:** caducidad - los plazos son perentorios (art. 7 Ley 6205) - no se suspenden ni interrumpen salvo norma expresa
- **¿Declarable de oficio?:** sí (art. 35 inc. b: la caducidad puede oponerse como excepción previa)

**Supuestos sin plazo de caducidad (arts. 10 y 11 Ley 6205):**
- Acto que lesiona un derecho subjetivo fundado principalmente en normas de derecho privado
- Pretensión exclusivamente resarcitoria dejando subsistente el acto ilegítimo
- Daños por actividad lícita de la Administración
- Silencio desestimatorio por transcurso del plazo constitucional (art. 19 Constitución Tucumán)
- Acto contrario al orden público o a las buenas costumbres
- La Administración pública como actora (sin perjuicio de la prescripción)

```
[ALERTA PLAZO FATAL: art. 9 Ley 6205 CPA Tucumán - proceso ordinario: 90 días hábiles judiciales - proceso sumario: 10 días hábiles judiciales - desde notificación del acto que agota la vía - vencimiento: calcular]
```

**Diferencia con otros regímenes (solo a título informativo; no transpolar):**

| Régimen | Plazo ordinario | Norma |
|---------|-----------------|-------|
| **Tucumán ordinario** | **90 días hábiles judiciales** | Ley 6205 art. 9 |
| **Tucumán sumario** | **10 días hábiles judiciales** | Ley 6205 art. 9 |
| PBA | 90 días hábiles judiciales | Ley 12.008 art. 18 |
| CABA | 90 días hábiles judiciales | Ley 189 art. 7 |
| Federal (post-9-jul-2024) | 180 días hábiles judiciales | LNPA art. 25 |
| Corrientes | 60 días | Hábiles judiciales | Ley 3460 art. 223 |
| Misiones | 60 días | Corridos (sin ferias) | Ley I-95 art. 24 |
| Neuquén | 30 días | Corridos (no feria; inhábil → primer hábil) | Ley 1305 art. 10 |
| Río Negro | 30 días | Hábiles | Ley 5773 art. 11 |
| Córdoba | 30 días hábiles judiciales | Ley 7182 art. 8 |
| Santa Fe | 30 días (verificar naturaleza) | Ley 11.330 art. 9 |
| Mendoza | 30 días corridos | Ley 3918 art. 20 |
| Entre Ríos | 1 año corrido | Ley 7061 art. 19 |
| Salta | 30 días hábiles judiciales | Ley 793 art. 12 |

### Órganos jurisdiccionales

**Primera instancia:**
- **Juzgados en lo Contencioso Administrativo:** creados por Ley 8970 (con vigencia especial: "a partir de la puesta en funcionamiento de los Juzgados de Primera Instancia en el Fuero Contencioso Administrativo"). La Ley 6238 (Ley Orgánica del Poder Judicial, mod. por Ley 9712, B.O. 12/10/2023) los regula en su Cap. VIII, arts. 69 y ss. Asiento: Centro Judicial Capital (San Miguel de Tucumán) principalmente.
- **Competencia material (art. 69 Ley 6238):** causas en que el acto o hecho jurídico constitutivo de la acción sea de naturaleza administrativa o tributaria. **Excepciones:** cobro de tributos y sanciones pecuniarias (vía apremio); acciones contra decisiones de la Inspección General de Personas Jurídicas; y otras previstas en la ley.

**[CONFIRMADO] Estado operativo del fuero (mayo 2026):**

- **Centro Judicial Capital (San Miguel de Tucumán):** 3 Juzgados de Primera Instancia CA operativos (Iª, IIª y IIIª Nominación). Alzada: Cámara en lo Contencioso Administrativo con 3 Salas, plenamente operativa.
- **Centro Judicial Concepción:** 1 Juzgado de Primera Instancia CA operativo. Alzada transitoria: Cámara de Apelaciones en lo Civil, Comercial, Común y del Trabajo de Concepción (conexidad material transitoria hasta la total autonomía del fuero en esa jurisdicción).
- La implementación fue progresiva y sujeta a partidas presupuestarias y concursos del Consejo de la Magistratura. La estructura descripta absorbe la totalidad de la matrícula litigiosa activa.

```
[VERIFICAR NOMINACIÓN: identificar la nominación del Juzgado CA (Iª, IIª o IIIª) competente según el turno y circunscripción antes de radicar]
```

**Alzada:**
- **Cámara en lo Contencioso Administrativo:** 3 Salas, 2 vocales por Sala (art. 28 Ley 6238). Asiento: San Miguel de Tucumán. Actúa como tribunal de alzada de los Juzgados CA.
- **Competencia (art. 32 Ley 6238):** causas de naturaleza administrativa o tributaria; recursos contra decisiones de organismos provinciales, municipales o entes no estatales que ejerzan prerrogativas de derecho público.
- Verificar la Sala actuante antes de citar jurisprudencia: las tres Salas pueden tener criterios diferentes en cuestiones no unificadas.

**Tribunal Superior:**
- **Corte Suprema de Justicia de Tucumán (CSJ Tucumán):** tribunal de casación e inconstitucionalidad en materia contencioso administrativa. Recurso de casación: art. 89 Ley 6205 y Código Procesal Civil y Comercial de Tucumán.

### Actos impugnables y pretensiones (Ley 6205)

**Proceso ordinario - pretensiones (art. 9 Ley 6205):**
- Restitución en una situación jurídica-subjetiva (derecho subjetivo lesionado): demanda dentro de los 90 días hábiles judiciales, con acumulación de pretensión anulatoria.
- Anulación de un acto por quien invoca un interés legítimo: mismo plazo de 90 días.
- Resarcimiento de daños (acumulado o autónomo): ver arts. 10 y 13 para los supuestos sin plazo de caducidad.

**Proceso sumario (arts. 86 y ss. Ley 6205):** plazo de 10 días hábiles judiciales. Verificar en qué supuestos la Ley 6205 prevé este trámite abreviado.

**Habilitación de la instancia (art. 12 Ley 6205):** el ejercicio de las acciones requiere el agotamiento de la instancia administrativa por las vías previstas en la Ley 4537 y leyes especiales. No pueden articularse pretensiones no planteadas en sede administrativa, pero pueden deducirse las no planteadas y resueltas o las planteadas y no resueltas.

**Sin plazos de caducidad (arts. 10 y 11 Ley 6205):** los supuestos del art. 10 (daños por actividad lícita, pretensión exclusivamente resarcitoria sin anulación, silencio desestimatorio constitucional, actos contra el orden público) y el art. 11 (Administración como actora) no tienen plazo de caducidad, sin perjuicio de la prescripción.

### Medidas cautelares (arts. 18-27 Ley 6205)

- **Suspensión de ejecutoriedad (arts. 20-26 Ley 6205):** puede solicitarse antes, simultánea o posteriormente a la acción. Procede cuando: (a) la ejecución pudiere causar grave daño al particular sin grave perjuicio para el interés público; (b) el acto apareje una ilegalidad manifiesta; (c) la Administración la solicita por lesividad.
- **Requisito previo para suspensión durante el trámite administrativo (art. 22 Ley 6205):** si se pide como cautelar pendiente el agotamiento de la vía, el particular debe acreditar haber solicitado la suspensión ante la Administración y haber sido denegado expresamente, o que no se expidió en 10 días. Excepción: cuando la Administración asuma comportamientos que hagan presumir inequívocamente que pondrá el acto en ejecución.
- **No procede la suspensión (art. 23 Ley 6205):** clausura/demolición por razones de seguridad/salubridad/higiene con dictamen técnico; cesantía o exoneración de agentes con defensa asegurada; preservación del orden público; autotutela de bienes del dominio público; decomiso o destrucción por peligro para la salud.
- **Caducidad de la suspensión (art. 26 Ley 6205):** si la suspensión fue ordenada antes de la demanda, caduca si la acción no se deduce dentro de los **15 días** contados desde que la suspensión se cumplió.
- **Otras cautelares:** las del Código Procesal Civil y Comercial de Tucumán, conforme sus requisitos genéricos (art. 27 Ley 6205).
- **No aplica Ley 26.854 nacional.**

```
[ALERTA CAUTELAR TUCUMÁN: suspensión ordenada antes de la acción caduca si la demanda no se interpone en 15 días desde que se cumplió la suspensión (art. 26 Ley 6205)]
[ATENCIÓN: no procede suspensión en cesantías/exoneraciones con defensa asegurada - art. 23 inc. b Ley 6205]
```

### Amparo Tucumán

- **Norma:** art. 20 Constitución Tucumán (2006) + Ley 6944 (Código Procesal Constitucional de Tucumán) - texto consolidado por Ley 9924. El amparo está integrado en el Código Procesal Constitucional.
- **Competencia:** los juzgados de primera instancia con competencia en la materia (civil o contencioso administrativa según el acto impugnado). En materia administrativa, los Juzgados CA.
- **Plazo:** verificar plazo de caducidad en la Ley 6944. El art. 20 inc. 2 Constitución Tucumán establece que la acción de amparo no procede contra leyes, a menos que la inconstitucionalidad sea manifiesta.
- **Subsidiariedad:** procede cuando no existe otro remedio judicial más idóneo y la lesión es manifiestamente ilegítima.

```
[VERIFICAR AMPARO TUCUMÁN: Ley 6944 (Código Procesal Constitucional, texto consolidado Ley 9924) - plazo de caducidad - competencia en materia administrativa (Juzgados CA)]
```

---

## Normativa de referencia Tucumán

### Responsabilidad del Estado provincial

- **Sin ley propia equivalente a Ley 26.944 nacional:** Tucumán no sancionó una ley de responsabilidad del Estado equivalente a la Ley 26.944. Ésta no aplica a demandas contra el Estado provincial tucumano.
- **Régimen procesal (Ley 6205):** los arts. 10 y 13 establecen supuestos de pretensiones resarcitorias sin plazo de caducidad específico:
  - Pretensión exclusivamente resarcitoria dejando subsistente el acto (art. 10 inc. b): no requiere impugnación recursiva previa del acto generador como requisito de admisibilidad
  - Daños por actividad lícita de la Administración (art. 10 inc. c): sin plazo de caducidad
  - Daños por actos o hechos cuando el monto no está determinado en norma (art. 13 inc. b): no requiere agotar la vía administrativa
- **Régimen sustantivo:** principios generales del derecho administrativo y jurisprudencia de la CSJ Tucumán y Cámara CA. No aplicar Ley 26.944 ni CCCN sin verificar criterio del fuero.
- **Prescripción de la acción:** verificar criterio de la CSJ Tucumán y la Cámara CA.

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD TUCUMÁN: sin ley propia - principios generales + jurisprudencia CSJ Tucumán y Cámara CA - verificar arts. 10 y 13 Ley 6205 para determinar si hay plazo de caducidad o no - no aplicar Ley 26.944 ni CCCN sin verificar]
```

### Empleo público Tucumán

- **Estatuto general:** Ley 5473 (Estatuto para el Personal de la Administración Pública Provincial de Tucumán) y modificatorias (inc. Ley 9140 de 2018). Regula el personal permanente y no permanente del Poder Ejecutivo provincial y organismos autárquicos que así lo dispongan.
- **Dictamen de Fiscalía de Estado en nombramientos:** el art. 6 Ley 5473 exige dictamen de la Fiscalía de Estado antes de todo nombramiento. La designación en violación de este requisito es nula.
- **Proceso sumario de impugnación:** verificar si el Código Procesal Administrativo (Ley 6205) prevé un proceso sumario específico de 10 días para impugnar sanciones a empleados públicos (art. 9 Ley 6205).
- **Estatutos sectoriales principales:**
  - Docentes: Ley 7673 (Estatuto del Docente Provincial de Tucumán) y modificatorias
  - **Policía (personal):** Ley N° 3823 (Ley del Personal Policial de Tucumán) y modificatorias. [A VERIFICAR: verificar si Ley 5598 es la Ley Orgánica complementaria o si la Ley 3823 es la vigente para el personal — confirmar en Boletín Oficial de Tucumán]
  - **Policía (orgánica):** Ley N° 3656 (Ley Orgánica de la Policía de Tucumán) y modificatorias
  - **Personal de salud:** Ley N° 5908 (Estatuto de la Carrera Sanitaria Provincial — SIPROSA). Regula ingreso por concurso, agrupaciones por complejidad asistencial, licencias por insalubridad y escalafón salarial diferenciado
  - Personal municipal: verificar si el municipio tiene estatuto propio o remite a la Ley 5473 supletoriamente
- **APUNT (Administración Provincial de Urbanismo de Tucumán):** ente autárquico; sus resoluciones son impugnables ante el fuero CA.

```
[VERIFICAR VIGENCIA ESTATUTOS SECTORIALES TUCUMÁN: Ley 3823 (personal policial) / Ley 3656 (orgánica Policía) / Ley 5908 (carrera sanitaria SIPROSA) - confirmar en Boletín Oficial Tucumán. Dictamen Fiscalía de Estado obligatorio en nombramientos (art. 6 Ley 5473)]
```

### Contratación pública Tucumán

- **Norma general:** Ley 7394 (Régimen de Contrataciones del Estado de Tucumán) y modificatorias. Regula el subsistema de contrataciones del Poder Ejecutivo provincial.
- **Reglamento:** verificar decretos reglamentarios vigentes. Los umbrales se actualizan por resolución del organismo rector.
- **Organismo rector:** Dirección de Contrataciones del Estado o equivalente. Verificar denominación actual.
- **Plataforma de compras:** TUCUMÁN COMPRAS (sistema electrónico de contrataciones de la Provincia). Verificar URL vigente.
- **Obra pública provincial:** verificar ley de obras públicas provincial vigente. La Ley 13.064 (obra pública nacional) no aplica supletoriamente salvo remisión contractual expresa.
- **Impugnación de licitaciones:** los plazos para impugnar pliegos y preadjudicación están fijados en la Ley 7394 y en cada pliego. Verificar antes de analizar la admisibilidad.

```
[VERIFICAR VIGENCIA: Ley 7394 Tucumán (contrataciones) y decretos reglamentarios - los montos de licitación pública/privada/contratación directa se actualizan - verificar en el portal de compras de Tucumán]
```

### Organismos de control Tucumán

**Tribunal de Cuentas de Tucumán:**
- Control externo del Estado provincial. Tiene función jurisdiccional. Sus resoluciones definitivas son impugnables ante el fuero contencioso administrativo (Ley 6205).

**Fiscalía de Estado de Tucumán:**
- Representante legal del Estado provincial en juicio. Interviene en los recursos jerárquicos resueltos por el PE (con dictamen preceptivo en muchos casos) y en el proceso judicial como parte representante de la Provincia.
- Publica dictámenes destacados en https://www.fiscaliatucuman.gob.ar
- Las notificaciones a la Fiscalía de Estado se hacen en su despacho oficial.
- Todo nombramiento en la Administración Pública requiere dictamen de la Fiscalía de Estado (art. 6 Ley 5473).

**APUNT (Administración Provincial de Urbanismo de Tucumán):**
- Ente autárquico relevante en materia de habilitaciones y urbanismo. Sus resoluciones se impugnan ante el fuero CA.

**DGR (Dirección General de Rentas de Tucumán):**
- En materia tributaria: el fuero CA tiene competencia para las impugnaciones de actos de la DGR. Verificar si existe Tribunal Fiscal de Apelación tucumano para instancia administrativa previa.

**Defensor del Pueblo de Tucumán:**
- Art. 40 Constitución Tucumán (2006). Legitimación para actuar en defensa de derechos colectivos.

---

## Alerta normativa - normas de vigencia variable

*Última verificación de esta sección: mayo 2026. Actualizar cuando cambie alguna de las normas listadas.*

### Plazos de caducidad CPA Tucumán

```
[ALERTA PLAZO FATAL: art. 9 Ley 6205 CPA Tucumán - proceso ordinario: 90 días hábiles judiciales - proceso sumario: 10 días hábiles judiciales - desde notificación del acto que agota la vía - vencimiento: calcular]
```

### Normas de vigencia variable a verificar en cada consulta

- **Estado del fuero (Juzgados CA):** [CONFIRMADO] operativos — 3 Juzgados CA en Capital (Iª, IIª, IIIª Nom.) + 1 en Concepción. Identificar nominación antes de radicar.
- **Montos de contratación pública (Ley 7394):** se actualizan por resolución. Verificar antes de encuadrar el procedimiento.
- **Escala salarial empleo público:** se modifica por paritarias. Verificar resolución de homologación vigente.
- **Acordadas de la CSJ Tucumán:** pueden modificar aspectos procesales y de competencia. Verificar acordadas vigentes en la materia específica.
- **Habilitaciones municipales:** el régimen varía por municipio. Verificar norma vigente al momento del acto.

```
[VERIFICAR VIGENCIA: norma Tucumán - [materia] - consultar Registro Oficial de Leyes y Decretos (https://leyes.tucuman.gob.ar) y Boletín Oficial Tucumán antes de aplicar]
```

## Responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| Juzgados en lo Contencioso Administrativo (1ª instancia) | Fiscalía de Estado de Tucumán | Ley 5473 art. 6 y Ley Orgánica Fiscalía de Estado |
| Cámara en lo Contencioso Administrativo (alzada - Salas I, II y III) | Fiscalía de Estado de Tucumán | Ley Orgánica Fiscalía de Estado |
| Corte Suprema de Justicia de Tucumán (casación / inconstitucionalidad) | Fiscalía de Estado de Tucumán | Ley Orgánica Fiscalía de Estado |
| Recursos jerárquicos resueltos por el PE (sede administrativa) | Fiscalía de Estado (dictamen preceptivo en los supuestos de la Ley 5473 art. 6 y otros) | Ley 4537 + Ley 5473 art. 6 |
| Notificaciones a la Fiscalía de Estado | En su despacho oficial (https://www.fiscaliatucuman.gob.ar) | Praxis del fuero |

**Estado actual del fuero:** los Juzgados CA de primera instancia están operativos en Capital (3 juzgados) y en Concepción (1 juzgado). Identificar la nominación y circunscripción correspondiente antes de radicar.

```
[VERIFICAR REPRESENTACIÓN PROCESAL TUCUMÁN: Fiscalía de Estado como representante del Estado en todas las instancias - notificaciones en despacho oficial - verificar si los Juzgados CA de primera instancia están operativos antes de determinar la instancia de radicación]
```

---

## Fuentes primarias

- **Registro Oficial de Leyes y Decretos Tucumán:** https://leyes.tucuman.gob.ar
- **Poder Judicial Tucumán (jurisprudencia y normativa):** https://www.justucuman.gov.ar
- **Fiscalía de Estado Tucumán:** https://www.fiscaliatucuman.gob.ar
- **Tribunal de Cuentas Tucumán:** https://www.tribunaldecuentas.gob.ar
- **Portal del Empleado Público Tucumán:** https://www.empleadopublico.tucuman.gov.ar
- **Portal de trámites Tucumán:** https://www.tucuman.gob.ar
- **Digesto Jurídico Tucumán:** consultar en el portal del Poder Judicial (Ley 9924)

---

## Reglas de citación - administrativo Tucumán

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para el fuero contencioso administrativo Tucumán:

**Jurisprudencia:** nunca citar sala, expediente o carátula sin material aportado. Las tres Salas de la Cámara CA pueden tener criterios diferentes; verificar la Sala actuante. Usar:
```
[INSERTAR FALLO VERIFICADO: CSJ Tucumán / Cámara CA Tucumán - Sala [I/II/III] / Juzgado CA [Nominación] - doctrina requerida]
```

**Actos administrativos Tucumán:** no asumir el contenido de resoluciones, dictámenes de la Fiscalía de Estado o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos CPA Tucumán:** no transpolar plazos del régimen federal ni de otras provincias. Usar:
```
[ALERTA PLAZO FATAL: art. 9 Ley 6205 CPA Tucumán - proceso ordinario: 90 días hábiles judiciales / proceso sumario: 10 días hábiles judiciales - desde [inicio del cómputo] - vencimiento: calcular]
```

---

## Lógica de análisis por institución

### Checklist: acto administrativo provincial/municipal

Aplicar Ley 4537. Elementos: competencia, causa, objeto, procedimiento (incluyendo dictamen de Fiscalía de Estado cuando es obligatorio), motivación, finalidad, proporcionalidad, forma escrita.

1. ¿Qué acto se impugna? ¿Es del Estado provincial o de un municipio? ¿Es definitivo?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo del art. 9 Ley 6205)
3. ¿Qué elementos del acto se cuestionan?
4. ¿Hay expediente administrativo? ¿El abogado tiene los antecedentes o requiere vista?
5. ¿Se interpusieron los recursos de la Ley 4537 en plazo? ¿Con patrocinio letrado?
6. ¿Intervino la Fiscalía de Estado cuando era obligatorio (ej. nombramientos, art. 6 Ley 5473)?
7. ¿La pretensión a plantear en sede judicial coincide con lo planteado en sede administrativa? (art. 12 Ley 6205)
8. ¿Es un caso del art. 10 o art. 13 Ley 6205 (sin plazo de caducidad)?

### Checklist: recursos administrativos Tucumán

Aplicar Ley 4537 arts. 44-68. En cada recurso verificar:

1. Plazo en días hábiles administrativos: reconsideración 15 días / jerárquico 15 días / alzada 15 días.
2. El vencimiento de los plazos hace perder el derecho sin posibilidad de denuncia de ilegitimidad (art. 39 Ley 4537). No confundir con el régimen federal.
3. Para entes autárquicos: alzada ante el PE, solo por ilegitimidad (art. 68 Ley 4537).
4. El jerárquico puede interponerse subsidiariamente con la reconsideración; en ese caso el plazo de 15 días para el jerárquico corre desde la notificación de la denegatoria de la reconsideración o desde el silencio de aquélla.
5. Si el recurso agota la vía (el PE lo resuelve): notificar ese hito para computar el art. 9 Ley 6205.
6. Articular en sede administrativa todas las pretensiones que se quieran sostener en el proceso judicial.

```
[ALERTA PLAZO FATAL: recursos Ley 4537 Tucumán - 15 días hábiles administrativos (reconsideración / jerárquico / alzada) - su vencimiento hace perder el derecho sin posibilidad de denuncia de ilegitimidad (art. 39) - vencimiento: calcular]
```

### Checklist: agotamiento de la vía y proceso contencioso administrativo

1. Verificar si se interpusieron los recursos de la Ley 4537 en plazo.
2. Verificar si la resolución del PE agota la vía y fue notificada (inicio del cómputo art. 9 Ley 6205).
3. Determinar el tipo de proceso: ordinario (90 días) / sumario (10 días) / recurso especial (30 días).
4. Verificar si el caso corresponde a los arts. 10/11/13 Ley 6205 (sin plazo de caducidad).
5. Verificar que el objeto de la acción no supere lo planteado en sede administrativa (art. 12 Ley 6205).
6. Identificar la nominación del Juzgado CA competente (Capital: Iª, IIª o IIIª Nom.; Concepción: 1 juzgado).
7. En materia tributaria: verificar pago previo si aplica.

### Checklist: responsabilidad del Estado Tucumán

1. Determinar si la pretensión tiene o no plazo de caducidad (arts. 10, 13 Ley 6205).
2. Si la pretensión es exclusivamente resarcitoria: no requiere agotar la vía ni impugnar el acto (art. 13 inc. b Ley 6205).
3. No aplicar Ley 26.944 ni CCCN sin verificar criterio del fuero; aportar fallo de la Cámara CA o CSJ Tucumán.
4. Verificar prescripción según criterio de la CSJ Tucumán.

```
[INSERTAR FALLO VERIFICADO: CSJ Tucumán / Cámara CA - requisitos de la responsabilidad extracontractual del Estado provincial]
```

### Checklist: empleo público Tucumán

1. Identificar estatuto aplicable: Ley 5473 (general) o sectorial: Ley 7673 (docentes) / Ley 3823 + Ley 3656 (Policía: personal + orgánica) / Ley 5908 (personal de salud - SIPROSA) / estatuto municipal del organismo concreto.
2. Situación de revista del agente.
3. ¿El nombramiento contó con dictamen de la Fiscalía de Estado? (art. 6 Ley 5473 - su omisión nulifica la designación).
4. ¿Hubo sumario con garantías de debido proceso?
5. Determinar si aplica proceso ordinario (90 días) o sumario (10 días) para la impugnación (art. 9 Ley 6205).

### Checklist: contratación pública Tucumán

1. Verificar monto vigente según Ley 7394 y resoluciones del organismo rector para encuadrar el tipo de procedimiento.
2. Verificar plazos de impugnación de pliegos y preadjudicación en la Ley 7394 y en el pliego específico.
3. Para obra pública: verificar ley provincial; la Ley 13.064 nacional no aplica al Estado provincial salvo remisión contractual expresa.
4. Verificar sistema TUCUMÁN COMPRAS para publicaciones vigentes.

---

## Instrucciones operativas específicas - Tucumán

### Alerta crítica - plazo de caducidad

El plazo del art. 9 Ley 6205 es de caducidad, no de prescripción:
- Es perentorio (art. 7 Ley 6205): su vencimiento opera de pleno derecho
- 90 días hábiles judiciales para el proceso ordinario
- 10 días hábiles judiciales para el proceso sumario

Antes de analizar cualquier otra cuestión, emitir:
```
[ALERTA PLAZO FATAL: art. 9 Ley 6205 CPA Tucumán - proceso ordinario: 90 días hábiles judiciales / proceso sumario: 10 días hábiles judiciales - desde notificación del acto que agota la vía - vencimiento: calcular]
```

### Alerta crítica - estado del fuero

Antes de radicar cualquier acción ante el fuero contencioso administrativo de Tucumán:
```
[CONFIRMAR NOMINACIÓN: Juzgados CA Tucumán operativos - Capital: Iª, IIª, IIIª Nom. / Concepción: 1 juzgado - identificar nominación competente antes de radicar]
```

---

- Identificar si el acto es del Estado provincial tucumano, de un municipio o de un organismo federal antes de aplicar este perfil o el nacional.
- Verificar agotamiento de la vía (Ley 4537: reconsideración + jerárquico ante PE) antes de analizar la acción. Para entes autárquicos: alzada ante PE (solo por ilegitimidad).
- Plazos en sede administrativa: 15 días hábiles administrativos (reconsideración / jerárquico / alzada). Vencidos, se pierde el derecho sin posibilidad de denuncia de ilegitimidad.
- Determinar si el caso tiene plazo de caducidad o no (arts. 10, 11 y 13 Ley 6205).
- Determinar el tipo de proceso (ordinario: 90 días / sumario: 10 días).
- Verificar el estado de funcionamiento del fuero antes de radicar.
- En cesantías/exoneraciones con defensa asegurada: no procede la suspensión cautelar (art. 23 inc. b Ley 6205).
- La suspensión antes de la acción caduca si la demanda no se interpone en 15 días desde que la suspensión se cumplió (art. 26 Ley 6205).
- Verificar intervención preceptiva de la Fiscalía de Estado (recursos ante PE, proceso judicial).
- No aplicar Ley 26.944 ni CCCN sin verificar criterio del fuero.
- No asumir contenido de actos, expedientes ni dictámenes sin que el abogado los aporte.
- Todo escrito ante el fuero contencioso administrativo tucumano cierra con "Estado del escrito" estándar más: tipo de proceso (ordinario/sumario/recurso especial), fuero y nominación (verificado / pendiente), estado del agotamiento de la vía, **plazo art. 9 Ley 6205 (verificado / pendiente de verificar / vencido)**, verificación de si el caso tiene o no plazo de caducidad (arts. 10/13), intervención de Fiscalía de Estado (sí / no / a verificar), Sala de la Cámara CA si ya está radicada la causa, próximo plazo procesal.

---

*Última actualización: mayo 2026*
*Normativa base: Ley 4537 LPA Tucumán (mod. Ley 6311), Ley 6205 CPA Tucumán (mod. Leyes 6242, 6282 y 6944, texto consolidado Ley 9924), Ley 6238 LOPJ Tucumán (mod. Leyes 8970 y 9712), Ley 6944 (Código Procesal Constitucional / amparo), Ley 5473 (empleo público, mod. Ley 9140), Ley 7673 (estatuto docente), Ley 5598 (policía), Ley 7394 (contrataciones), Constitución de Tucumán (2006) arts. 19, 20, 40*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
