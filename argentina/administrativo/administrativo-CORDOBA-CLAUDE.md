# Perfil de práctica · Derecho administrativo · Provincia de Córdoba

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Córdoba.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.

---

## Configuración inicial - completar antes de usar

**PROVINCIA:** Provincia de Córdoba

**FUERO_HABITUAL:** [COMPLETAR: denominación exacta del tribunal y circunscripción. Ej: "Cámara Contencioso Administrativa de 1ª Nominación, Córdoba Capital" / "Cámara Contencioso Administrativa de 2ª Nominación, Córdoba Capital" / "Cámara Civil y Comercial con competencia contencioso administrativa, Río Cuarto". En la Capital: hay fuero especializado (Cámaras CA). En el interior: las Cámaras Civiles y Comerciales ejercen competencia contencioso administrativa.]

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo Córdoba. Ej: "Responsabilidad del Estado provincial, empleo público, contratación pública, sanciones administrativas, habilitaciones municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos provinciales o municipales ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Salud Córdoba, APROSS, EPEC, Municipalidad de Córdoba".]

---

## Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Córdoba: procedimiento administrativo ante la Administración provincial y municipal (Ley 5350), recursos administrativos en sede provincial, control judicial contencioso administrativo (Ley 7182), responsabilidad del Estado provincial, empleo público provincial y contratación pública provincial.

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Córdoba (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal cordobesa, aplica este perfil. No transpolar plazos ni institutos entre ambos regímenes sin advertencia.

**Tercer nivel - organismos municipales:** la Ley 7182 incluye expresamente los actos de las municipalidades en su ámbito de competencia (art. 1). El agotamiento de la vía ante actos municipales puede requerir la interposición de recursos ante el propio municipio conforme sus ordenanzas de procedimiento; a falta de norma municipal, aplica supletoriamente la Ley 5350 provincial. Verificar si la municipalidad tiene ordenanza de procedimiento propio antes de encuadrar el agotamiento de la vía.

```
[VERIFICAR RÉGIMEN MUNICIPAL CÓRDOBA: actos de municipios - competencia del fuero contencioso administrativo provincial (art. 1 Ley 7182) - verificar si el municipio tiene ordenanza de procedimiento propio que regule el agotamiento de la vía]
```

---

## Normativa de procedimiento administrativo provincial

### Ley de procedimiento administrativo Córdoba

- **Norma principal:** Ley 5350 (Ley de Procedimiento Administrativo de la Provincia de Córdoba), sancionada el 21/03/1972, publicada el 24/04/1972
- **Texto ordenado:** Ley 6658 (T.O. de la Ley 5350, B.O. 24/11/1981) y modificatorias posteriores. La ley fue actualizada con nuevos artículos (13 bis, 13 ter, 13 quáter, 9 bis) que incorporaron principios de celeridad, derechos del administrado, digitalización y simplificación. Última actualización verificada: 04/03/2026 (leyes-ar.com).
- **Sin reglamento separado:** la Ley 5350 contiene la regulación procedimental. No tiene decreto reglamentario separado equivalente al Decreto 1759/72 federal.
- **Texto vigente:** consultar portal de Justicia Córdoba: https://leyes.justiciacordoba.gob.ar o Argentina.gob.ar normativa provincial.
- **Ámbito de aplicación (art. 1 Ley 5350):** se aplica a los Poderes Legislativo, Ejecutivo y Judicial del Estado Provincial, al Tribunal de Cuentas, a las entidades descentralizadas autárquicas y a cualquier órgano o ente dotado de potestad pública. **Excepción:** materia tributaria, para la que es de aplicación supletoria.
- **Articulado clave:** art. 8 (debido proceso adjetivo), art. 7 (celeridad, economía, sencillez), arts. 77-92 (recursos administrativos), arts. 93 y ss. (acto administrativo).

```
[VERIFICAR VIGENCIA: Ley 5350 (T.O. Ley 6658) LPA Córdoba - consultar texto actualizado en https://leyes.justiciacordoba.gob.ar - verificar modificaciones posteriores a mayo 2026]
```

### Régimen de silencio administrativo Córdoba

- **Regla general:** silencio negativo (denegatoria tácita). La Ley 5350 no adoptó el régimen de silencio positivo de la Ley 27.742 nacional (Dec 971/2024). El silencio positivo para autorizaciones regladas aplica solo a procedimientos ante la Administración nacional. No transpolar ese régimen al Estado provincial cordobés sin verificar si Córdoba sancionó norma equivalente.
- **Plazo para resolver recursos:** la autoridad administrativa dispone de 30 días para resolver el recurso de reconsideración (art. 67 inc. h Ley 5350).
- **Denegatoria tácita:** vencido el plazo para resolver, el silencio habilita la interposición del recurso jerárquico o la acción contencioso administrativa según el caso. Verificar el plazo específico del procedimiento de que se trate.

```
[VERIFICAR RÉGIMEN DE SILENCIO CÓRDOBA: Ley 5350 - silencio negativo por regla general - no aplica silencio positivo del Dec 971/2024 nacional - verificar si Córdoba sancionó norma equivalente]
```

### Elementos esenciales del acto administrativo Córdoba

La Ley 5350 regula los elementos esenciales del acto administrativo con estructura paralela al art. 7 LNPA federal (arts. 93 y ss.):

1. Competencia: atribución del órgano provincial o municipal (art. 3 Ley 5350)
2. Causa: antecedentes de hecho y de derecho que fundamentan el acto
3. Objeto: cierto, lícito, físicamente posible
4. Procedimiento: cumplimiento de trámites esenciales previos (incluye vista al Fiscal de Estado cuando corresponde)
5. Motivación: expresión concreta de las razones del dictado del acto
6. Finalidad: adecuada a la causa del acto y al ordenamiento provincial

**Régimen de nulidades Córdoba:** la Ley 5350 distingue nulidades absolutas (vicios en elementos esenciales, insubsanables, declarables de oficio) de nulidades relativas (vicios que admiten saneamiento), con estructura análoga a los arts. 14-17 LNPA federal. Verificar articulado específico.

**Patrocinio letrado:** todos los recursos administrativos (salvo el de reconsideración) requieren patrocinio letrado. Si se presenta sin patrocinio, se intima por 24 horas a suplir la omisión; vencidas sin cumplimiento, se tiene por no presentado (art. 77 Ley 5350). Punto de alta frecuencia de error.

### Recursos administrativos Córdoba

**Recurso de reconsideración (art. 80 Ley 5350):**
- Plazo: 5 días hábiles administrativos desde la notificación fehaciente del acto
- Ante: el mismo órgano que dictó el acto
- Sin patrocinio letrado obligatorio (único recurso que lo exime)
- Efecto: la autoridad dispone de 30 días para resolver (art. 67 inc. h). Si desestima, habilita el recurso jerárquico.
- No procede: cuando se impugna una decisión emitida presuntamente por silencio, o que se limitó a resolver un recurso (art. 82 Ley 5350)

**Recurso jerárquico (art. 83 Ley 5350):**
- Plazo: 10 días hábiles administrativos desde la notificación de la denegatoria de la reconsideración, o desde la fecha de producción presunta del silencio de aquélla. Puede interponerse en forma subsidiaria con la reconsideración.
- Ante: el órgano que dictó el acto impugnado (que lo eleva al superior jerárquico)
- Patrocinio letrado: obligatorio
- Vista al Fiscal de Estado: solo en los recursos jerárquicos que deban ser resueltos por el Poder Ejecutivo (art. 83 in fine Ley 5350)
- Agota la vía: sí, cuando es resuelto por el Poder Ejecutivo o el ministro competente

**Recurso de alzada (art. 84 Ley 5350):**
- Procede contra decisiones definitivas de entes autárquicos, **después** de interponer y que sea desestimado el recurso de reconsideración
- A opción del interesado: alzada (resuelta por el Poder Ejecutivo, previa vista al Fiscal de Estado) **o** vía contencioso administrativa directamente
- Plazo: 10 días hábiles desde la denegatoria de la reconsideración o desde el silencio de aquélla
- El recurso de alzada solo permite control de legitimidad (art. 85 Ley 5350): no cuestiona el mérito de la decisión del ente autárquico

**Recurso de reconsideración ante autoridades con facultad para decidir en última instancia (art. 87 Ley 5350):**
- Cuando el acto emana de autoridades con facultad para decidir en última instancia administrativa, para agotar la vía se debe interponer recurso de reconsideración (salvo los casos del art. 82).
- Este es el recurso que agota la vía en esos supuestos.

**Queja (art. 86 Ley 5350):**
- Plazo: 10 días desde que la autoridad ante la que se interpuso el recurso jerárquico o de alzada notificó su denegatoria, o desde la producción presunta del silencio
- Ante: el Poder Ejecutivo, solicitando se avoque al conocimiento y decisión del recurso
- No interrumpe otros plazos

**Recurso de revisión (art. 89 Ley 5350):**
- Procede en sede administrativa para revisar un acto firme en supuestos taxativos: contradicciones en la parte dispositiva, influencia de documentos falsos, prevaricato o cohecho del funcionario actuante, revelación de hechos desconocidos al momento del acto

**Sin reforma análoga al Decreto 695/2024 nacional:** Córdoba no duplicó los plazos de recursos administrativos como hizo el decreto federal. Los plazos de la Ley 5350 son los originales (5/10 días). No aplicar los plazos federales reformados a recursos ante la Administración cordobesa.

```
[ALERTA PLAZO FATAL: recurso de reconsideración - Ley 5350 art. 80 - 5 días hábiles administrativos desde notificación fehaciente - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico / alzada - Ley 5350 arts. 83/84 - 10 días hábiles administrativos desde notificación de denegatoria o silencio de la reconsideración - patrocinio letrado obligatorio - vencimiento: calcular]
```

### Agotamiento de la vía administrativa Córdoba

- **Regla general:** el agotamiento de la vía administrativa es requisito previo de admisibilidad de la acción ante el fuero contencioso administrativo (art. 1 inc. a Ley 7182). El acto administrativo debe "causar estado" en razón de haberse agotado las instancias administrativas.
- **Vía de agotamiento:** interposición de los recursos previstos en la Ley 5350 (reconsideración + jerárquico, o reconsideración ante autoridad con facultad de decisión definitiva, o alzada contra entes autárquicos). La interposición de todos los recursos "será siempre necesaria a los fines de agotar la vía administrativa" (art. 77 Ley 5350).
- **Excepciones:** el fuero contencioso administrativo cordobés admite excepciones al agotamiento en supuestos análogos a los del régimen federal (acto nulo de nulidad absoluta, inutilidad manifiesta). Verificar jurisprudencia del TSJ Córdoba antes de prescindir del agotamiento.
- **Fiscal de Estado:** interviene con vista preceptiva en los recursos jerárquicos que resuelve el Poder Ejecutivo y en las causas contencioso administrativas. Su omisión cuando es preceptiva puede configurar vicio de procedimiento.

```
[VERIFICAR AGOTAMIENTO DE VÍA CÓRDOBA: Ley 5350 arts. 77-87 - verificar si se interpusieron todos los recursos en plazo, con patrocinio letrado en el jerárquico/alzada, y si la resolución que agota la vía fue notificada - inicio del cómputo del plazo del art. 8 Ley 7182]
```

### Tabla unificada de plazos - sede administrativa

| Recurso / instituto | Plazo | Tipo de días | Patrocinio letrado | Norma |
|---------------------|-------|--------------|-------------------|-------|
| Reconsideración | 5 días | Hábiles administrativos | No obligatorio | Ley 5350 art. 80 |
| Jerárquico | 10 días | Hábiles administrativos | Obligatorio | Ley 5350 art. 83 |
| Alzada (entes autárquicos) | 10 días | Hábiles administrativos | Obligatorio | Ley 5350 art. 84 |
| Queja | 10 días | Hábiles administrativos | - | Ley 5350 art. 86 |
| Silencio de la reconsideración | 30 días sin resolución | - | - | Ley 5350 art. 67 inc. h |
| Acción ante el fuero CA | 30 días | Hábiles judiciales | - | Ley 7182 art. 8 |
| Lesividad | 6 meses desde el acto | - | - | Ley 7182 art. 8 |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial. La presentación del jerárquico y alzada sin patrocinio letrado provoca intimación por 24 horas; vencida sin cumplimiento, el recurso se tiene por no presentado (art. 77 Ley 5350).

---

## Control judicial contencioso administrativo

### Código de proceso contencioso administrativo Córdoba

- **Norma:** Ley 7182 (Código de Procedimiento Contencioso-Administrativo de la Provincia de Córdoba), sancionada el 30/10/1984, publicada el 27/11/1984, y modificatorias
- **Texto vigente:** consultar https://leyes.justiciacordoba.gob.ar y SAIJ. La ley fue modificada en varias oportunidades; verificar texto actualizado antes de aplicar.
- **Subsidiariedad:** el Código Procesal Civil y Comercial de Córdoba se aplica supletoriamente en lo no previsto por la Ley 7182.
- **Ámbito:** comprende impugnaciones de actos administrativos de los Poderes Legislativo, Ejecutivo y Judicial provinciales, del Tribunal de Cuentas, de entes autárquicos, de las municipalidades y de cualquier órgano con potestad pública con facultad para decidir en última instancia administrativa (art. 1 Ley 7182).

### Plazo de caducidad para accionar judicialmente

**Este es el dato más crítico del perfil. Diferencia sustancial con el régimen federal y con PBA.**

- **Plazo general:** 30 días hábiles judiciales desde que el acto fue debidamente notificado (art. 8 Ley 7182)
- **Cómputo:** días hábiles judiciales
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa
- **Inicio del cómputo:** desde la notificación del acto definitivo que agota la vía administrativa
- **Lesividad:** en las causas de lesividad (el Estado impugna sus propios actos), el plazo es de 6 meses desde la emisión del acto presuntamente irregular (art. 8 Ley 7182)
- **¿Declarable de oficio?:** sí, conforme jurisprudencia uniforme del TSJ Córdoba y Cámaras Contencioso Administrativas

```
[ALERTA PLAZO FATAL: art. 8 Ley 7182 CCA Córdoba - 30 días hábiles judiciales - desde notificación del acto que agota la vía - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes:**
- Régimen federal: 180 días hábiles judiciales (actos post-9-jul-2024)
- PBA: 90 días hábiles judiciales
- **Córdoba: 30 días hábiles judiciales**

El plazo cordobés de 30 días hábiles judiciales es significativamente más breve que el federal (180 días) y el de PBA (90 días). Solo Mendoza resulta más corto en términos reales (30 días corridos). Es el principal riesgo de caducidad en la práctica local. No aplicar bajo ningún concepto los plazos federales ni el de PBA a actos de la Administración cordobesa.

**Pago previo en materia tributaria (art. 9 Ley 7182):** cuando el acto impone una obligación tributaria de dar sumas de dinero, el actor debe abonar previamente la suma determinada (excluida multa) para poder promover la acción. Verificar antes de radicar la demanda.

### Órganos jurisdiccionales

**Primera instancia - Capital Córdoba:**
- **Cámaras Contencioso Administrativas:** conocen en primera instancia en la Primera Circunscripción Judicial (Córdoba Capital). Son la primera instancia especializada, no juzgados. Actualmente existen la Cámara Contencioso Administrativa de 1ª Nominación y la Cámara Contencioso Administrativa de 2ª Nominación.
- La Ley 7182 otorga competencia de primera instancia directamente a las Cámaras en la Capital, lo que es una particularidad del sistema cordobés.

**Primera instancia - interior de la provincia:**
- **Cámaras Civiles y Comerciales con competencia contencioso administrativa:** en las demás circunscripciones judiciales del interior (Río Cuarto, San Francisco, Villa María, Bell Ville, La Carlota, Cruz del Eje, Deán Funes, Río Tercero, Marcos Juárez, San Martín, Laboulaye y otras) la competencia contencioso administrativa es ejercida por las Cámaras Civiles y Comerciales correspondientes.
- **Dato práctico:** el juicio tramita ante una sala de la Cámara Civil y Comercial, no ante un juzgado especializado. Las reglas del proceso son las de la Ley 7182, pero el tribunal es el civil y comercial con competencia asignada.

**Alzada:**
- **Tribunal Superior de Justicia de Córdoba (TSJ):** es la alzada de las Cámaras Contencioso Administrativas de la Capital. Para el interior, la alzada varía según el departamento judicial; en algunos casos el TSJ tiene competencia directa.
- **Sala Contencioso Administrativa del TSJ:** conoce en los recursos de casación e inconstitucionalidad en materia contencioso administrativa.

**Tribunal Superior de Justicia (TSJ Córdoba):**
- **Recurso de casación:** procede por inobservancia o errónea aplicación de normas sustantivas o procesales; requiere monto mínimo en algunos supuestos. Verificar acordadas del TSJ.
- **Recurso de inconstitucionalidad:** procede cuando la cuestión versa sobre interpretación constitucional y el tribunal inferior resolvió de modo contrario.
- **Jurisdicción originaria:** el TSJ tiene competencia originaria en causas promovidas por la Provincia (art. 165 Constitución Córdoba). Verificar antes de radicar para determinar si la causa debe ir directamente al TSJ.

**Amparo - competencia especial:**
- Cuando la demandada es el Estado provincial (Poderes Ejecutivo, Legislativo o Judicial, entes autárquicos, empresas del Estado), la competencia en amparo (Ley 4915) corresponde a la **Cámara Contencioso Administrativa de turno en la Capital** y a las **Cámaras Civiles y Comerciales competentes en lo contencioso administrativo** en el interior (art. 4 bis Ley 4915). No al juzgado de primera instancia civil.

### Pretensiones admisibles (Ley 7182)

La Ley 7182 estructura el proceso en dos tipos principales:

**Proceso de plena jurisdicción (Capítulo II Ley 7182):**
- Impugnación de actos administrativos que vulneran un **derecho subjetivo de carácter administrativo** (art. 1 inc. b Ley 7182)
- El tribunal puede anular el acto y disponer el reconocimiento del derecho, incluyendo la reparación de daños

**Proceso de ilegitimidad (Capítulo III Ley 7182):**
- Impugnación de actos administrativos que afectan un **interés legítimo** (art. 1 inc. b Ley 7182)
- La sentencia se limita a resolver sobre la validez del acto impugnado; si declara la nulidad, tiene efecto erga omnes desde su publicación en el Boletín Oficial (art. 39 Ley 7182)
- No procede la pretensión resarcitoria en este proceso; debe plantearse en otro proceso
- El Fiscal de Cámara Contencioso Administrativa (o equivalente en el interior) es parte necesaria en el proceso de ilegitimidad (art. 3 inc. c Ley 7182)

**Distinción crítica derecho subjetivo / interés legítimo:** esta distinción es determinante para elegir el tipo de proceso. El encuadre incorrecto puede llevar a la inadmisibilidad. Verificar jurisprudencia del TSJ Córdoba sobre la calificación del caso concreto antes de elegir la vía.

**Acción contencioso administrativa de lesividad:**
- La Administración puede impugnar sus propios actos irrevocables que son lesivos al interés público (art. 3 inc. b Ley 7182)
- Plazo: 6 meses desde la emisión del acto (art. 8 Ley 7182)

### Medidas cautelares contra el Estado provincial

- **Régimen:** la Ley 7182 no tiene un capítulo específico de cautelares equivalente al de la Ley 12.008 PBA. Las medidas cautelares se rigen por el Código Procesal Civil y Comercial de Córdoba en lo aplicable, con las adaptaciones del fuero. No aplica la Ley 26.854 nacional.
- **Requisitos:** verosimilitud del derecho + peligro en la demora + no afectación grave del interés público. Criterio construido principalmente por jurisprudencia de las Cámaras CA y el TSJ.
- **Suspensión del acto:** la suspensión de la ejecución del acto impugnado es la medida más frecuente. Verificar criterio de la cámara actuante sobre requisitos y contracautela.
- **Contracautela:** exigida como regla; puede ser juratoria según las circunstancias y el criterio del tribunal.

```
[VERIFICAR RÉGIMEN CAUTELAR CÓRDOBA: Ley 7182 + CPCC Córdoba supletorio - no aplica Ley 26.854 nacional - verificar criterio de la cámara actuante y nominación]
```

### Amparo Córdoba

- **Norma:** Ley 4915 (Ley de Amparo de la Provincia de Córdoba) y modificatorias (Ley 5770 y otras)
- **Competencia cuando demandada es el Estado provincial:** Cámara Contencioso Administrativa de turno en la Capital; Cámara Civil y Comercial competente en lo contencioso administrativo en el interior (art. 4 bis Ley 4915). No el juzgado civil de primera instancia.
- **Plazo para interponer:** la Ley 4915 no fija plazo de caducidad propio (a diferencia de la Ley 16.986 federal que es de 15 días). El plazo de caducidad opera por analogía con las reglas generales. Verificar jurisprudencia del TSJ Córdoba sobre el punto.
- **Subsidiariedad:** procede cuando no existe otra vía judicial más idónea y el acto lesiona derechos constitucionales en forma actual o inminente con ilegalidad manifiesta.
- **Amparo por mora (Ley 8508 Córdoba):** acción específica ante la mora o inactividad de la Administración. Tramita ante el fuero contencioso administrativo. Verificar Ley 8508 y modificatorias.

```
[VERIFICAR PLAZO AMPARO CÓRDOBA: Ley 4915 no fija plazo propio de caducidad - verificar jurisprudencia TSJ Córdoba sobre punto de inicio del cómputo y plazo aplicable - competencia: Cámara CA de turno (Capital) o Cámara Civil con competencia CA (interior)]
```

---

## Normativa de referencia Córdoba

### Responsabilidad del Estado provincial

- **Sin ley propia equivalente a Ley 26.944 nacional:** Córdoba no sancionó una ley de responsabilidad del Estado equivalente a la Ley 26.944. Ésta no aplica a demandas contra el Estado provincial cordobés.
- **Régimen aplicable:** el fuero contencioso administrativo cordobés aplica los principios generales del derecho administrativo y la jurisprudencia del TSJ Córdoba. La pretensión resarcitoria puede acumularse a la anulatoria en el proceso de plena jurisdicción (art. 1 inc. b Ley 7182) o plantearse en forma autónoma.
- **No aplicar CCCN:** no invocar arts. 1757, 1741 ni otros del CCCN en demandas contra el Estado provincial sin verificar criterio del fuero.
- **Requisitos según jurisprudencia TSJ Córdoba:** daño cierto y acreditado + imputabilidad al órgano estatal + nexo causal + falta de servicio. Aportar fallo del TSJ o de la cámara actuante.
- **Prescripción de la acción:** verificar criterio del TSJ Córdoba; puede diferir del plazo de 3 años del art. 7 Ley 26.944 federal.

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD CÓRDOBA: sin ley propia equivalente a Ley 26.944 - aplicar principios generales y jurisprudencia TSJ Córdoba - aportar fallo de la cámara actuante]
```

### Empleo público Córdoba

- **Estatuto general:** Ley 7233 (Estatuto del Personal de la Administración Pública Provincial de Córdoba) y modificatorias. Regula las relaciones laborales del personal del Poder Ejecutivo provincial.
- **Ámbito:** personal permanente (con y sin estabilidad), personal no permanente (de gabinete, interino, contratado, transitorio, suplente). Paralelo a la Ley 25.164 federal pero con diferencias sustanciales. No transpolar institutos.
- **Período de prueba (art. 15 Ley 7233):** el nombramiento de personal permanente tiene carácter provisorio durante los primeros 6 meses. Durante ese período, la cesantía no requiere sumario.
- **Estatutos sectoriales principales:**
  - Docentes: Ley 8113 (Estatuto del Docente de Córdoba) y modificatorias
  - Policía: Ley 9235 (Ley Orgánica de la Policía de la Provincia de Córdoba) y modificatorias
  - Personal de salud: verificar norma sectorial vigente (hospitales provinciales)
  - Personal judicial: acordadas del TSJ Córdoba
  - Personal municipal: verificar si el municipio tiene estatuto propio o remite a la Ley 7233 supletoriamente
  - [COMPLETAR: otros estatutos sectoriales según las áreas de práctica habituales]
- **Régimen disciplinario:** Ley 7233 + decreto reglamentario. Sumario administrativo con garantías de debido proceso. Verificar si el organismo tiene reglamento de sumarios propio.
- **Obra Social:** APROSS (Administración Provincial del Seguro de Salud de Córdoba). Sus resoluciones son impugnables ante el fuero contencioso administrativo.

```
[VERIFICAR ESTATUTO APLICABLE CÓRDOBA: Ley 7233 general o estatuto sectorial según el organismo y la categoría del agente - para docentes: Ley 8113 / policial: Ley 9235]
```

### Contratación pública Córdoba

- **Norma general:** Ley 10.155 (Régimen de Contrataciones de Bienes y Servicios de la Administración Pública Provincial de Córdoba) y modificatorias. Aplicación obligatoria a la Administración General Centralizada; supletoria a empresas, agencias y entes estatales.
- **Reglamento:** verificar decreto reglamentario vigente. Los montos y umbrales se actualizan por resolución del organismo rector.
- **Organismo rector:** verificar denominación actual del organismo de compras del Ejecutivo cordobés (históricamente Contaduría General; puede haber sido modificado).
- **Plataforma de compras:** CEPRODAC o sistema electrónico vigente. Verificar URL actual antes de consultar.
- **Obra pública provincial:** Ley 8614 (Ley de Obras Públicas de Córdoba) y modificatorias. La Ley 13.064 (obra pública nacional) no aplica supletoriamente a obra pública provincial salvo remisión contractual expresa.
- **Impugnación de licitaciones:** los plazos para impugnar pliegos y preadjudicación están fijados en la Ley 10.155 y en cada pliego. Verificar antes de analizar la admisibilidad.

```
[VERIFICAR VIGENCIA: Ley 10.155 Córdoba y decreto reglamentario - los montos de licitación pública/privada/contratación directa se actualizan por resolución - verificar antes de encuadrar el procedimiento]
```

### Organismos de control Córdoba

**Tribunal de Cuentas de Córdoba:**
- Control externo del Estado provincial. Tiene función jurisdiccional (juicio de cuentas, cargo de responsabilidad). Sus resoluciones definitivas son impugnables ante el fuero contencioso administrativo bajo las reglas de la Ley 7182.

**Fiscal de Estado de Córdoba:**
- Representante legal del Estado provincial en juicio. Dictamina en los recursos jerárquicos que resuelve el Poder Ejecutivo (art. 83 Ley 5350) y en las causas contencioso administrativas en las que el Estado provincial es parte. Su participación como parte necesaria en el proceso de ilegitimidad es relevante; verificar si fue notificado.
- Las notificaciones al Fiscal de Estado deben realizarse en su despacho oficial.

**Fiscal de Cámara Contencioso Administrativa:**
- Es parte necesaria en el **proceso de ilegitimidad** (art. 3 inc. c Ley 7182). Su omisión puede afectar la regularidad del proceso. En el interior de la provincia, el Fiscal de Cámara Civil y Comercial cumple esta función.

**Defensor del Pueblo de Córdoba:**
- Art. 124 Constitución Córdoba. Tiene legitimación para actuar en defensa de derechos colectivos ante el fuero contencioso administrativo.

---

## Alerta normativa - normas de vigencia variable

*Última verificación de esta sección: mayo 2026. Actualizar cuando cambie alguna de las normas listadas.*

### Plazo de caducidad CCA Córdoba

```
[ALERTA PLAZO FATAL: art. 8 Ley 7182 CCA Córdoba - 30 días hábiles judiciales - desde notificación del acto que agota la vía - vencimiento: calcular]
```

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública (Ley 10.155):** los umbrales para licitación pública, privada y contratación directa se actualizan por resolución del organismo rector. Verificar antes de encuadrar el procedimiento.
- **Escala salarial empleo público Córdoba:** se modifica por paritarias. No asumir montos sin verificar la resolución de homologación vigente.
- **Habilitaciones municipales Córdoba Capital:** el régimen de habilitaciones comerciales se modifica por ordenanzas y resoluciones de la Municipalidad de Córdoba. Ante cualquier habilitación o sanción municipal, verificar norma vigente al momento del acto.
- **Acordadas del TSJ Córdoba:** el TSJ emite acordadas reglamentarias en materia de procedimiento y competencia que pueden modificar aspectos procesales. Verificar acordadas vigentes en la materia específica.

```
[VERIFICAR VIGENCIA: norma Córdoba - [materia] - consultar Boletín Oficial Córdoba (https://boletinoficial.cba.gov.ar) antes de aplicar]
```

## Responsables procesales por instancia

| Instancia | Representante | Rol | Normativa |
|-----------|---------------|-----|-----------|
| Cámaras CA (1ª y 2ª Nominación, Capital) | Fiscal de Estado de Córdoba | Representa al Estado provincial en juicio | Constitución Córdoba + Ley 5350 art. 83 |
| Cámaras Civil y Comercial con competencia CA (interior) | Fiscal de Estado de Córdoba | Ídem | Constitución Córdoba |
| Proceso de ilegitimidad - Capital | Fiscal de Cámara Contencioso Administrativa | Parte necesaria (art. 3 inc. c Ley 7182) | Ley 7182 art. 3 inc. c |
| Proceso de ilegitimidad - interior | Fiscal de Cámara Civil con competencia CA | Parte necesaria | Ley 7182 art. 3 inc. c |
| TSJ Córdoba (alzada, casación, inconstitucionalidad) | Fiscal de Estado de Córdoba | Representa al Estado en instancias superiores | Constitución Córdoba |
| Recursos jerárquicos ante el PE (sede administrativa) | Fiscal de Estado (dictamen preceptivo, art. 83 Ley 5350) | Solo en los que resuelve el PE | Ley 5350 art. 83 in fine |

**Distinción operativa clave:** el Fiscal de Cámara CA es parte necesaria **solo en el proceso de ilegitimidad**; no interviene como parte en el proceso de plena jurisdicción. Su omisión en el proceso de ilegitimidad puede afectar la regularidad del proceso. No confundir el Fiscal de Estado (representante del Estado demandado) con el Fiscal de Cámara CA (parte necesaria en ilegitimidad, rol diferente).

```
[VERIFICAR REPRESENTACIÓN PROCESAL CÓRDOBA: Fiscal de Estado representa al Estado demandado en todas las instancias - Fiscal de Cámara CA es parte necesaria SOLO en el proceso de ilegitimidad (art. 3 inc. c Ley 7182) - en el interior: Fiscal de Cámara Civil con competencia CA - notificaciones en sus respectivos despachos oficiales]
```

---

## Fuentes primarias

- **Boletín Oficial Córdoba:** https://boletinoficial.cba.gov.ar
- **Legislación Córdoba (Justicia):** https://leyes.justiciacordoba.gob.ar
- **TSJ Córdoba (jurisprudencia):** https://www.justiciacordoba.gob.ar
- **Ministerio Público Fiscal Córdoba:** https://www.mpfcordoba.gob.ar
- **Fiscal de Estado Córdoba:** https://fiscaldeestado.cba.gov.ar
- **Tribunal de Cuentas Córdoba:** verificar URL vigente
- **Portal de trámites Córdoba:** https://portaldetramites.cba.gov.ar
- **APROSS:** https://www.apross.gob.ar
- **Argentina.gob.ar / normativa provincial Córdoba:** https://www.argentina.gob.ar/normativa

---

## Reglas de citación - administrativo Córdoba

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para el fuero contencioso administrativo Córdoba:

**Jurisprudencia:** nunca citar sala, expediente o carátula sin material aportado. Las Cámaras CA de 1ª y 2ª Nominación pueden tener criterios diferentes en cuestiones no resueltas por el TSJ. Usar:
```
[INSERTAR FALLO VERIFICADO: TSJ Córdoba / Cámara CA [Nominación] / Cámara Civil y Comercial [departamento] con competencia CA - doctrina requerida]
```

**Actos administrativos Córdoba:** no asumir el contenido de resoluciones, dictámenes del Fiscal de Estado o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos CCA Córdoba:** no transpolar plazos del régimen federal ni de PBA. El plazo cordobés es 30 días hábiles judiciales. Usar:
```
[ALERTA PLAZO FATAL: art. 8 Ley 7182 CCA Córdoba - 30 días hábiles judiciales - desde [inicio del cómputo] - vencimiento: calcular]
```

**Dictámenes del Fiscal de Estado / Fiscal de Cámara:** no asumir su contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: dictamen del Fiscal de Estado / Fiscal de Cámara CA no aportado - verificar intervención en el expediente]
```

---

## Lógica de análisis por institución

### Checklist: acto administrativo provincial/municipal

Aplicar Ley 5350 LPA Córdoba. Elementos: competencia, causa, objeto, procedimiento, motivación, finalidad.

1. ¿Qué acto se impugna? ¿Es del Estado provincial o de un municipio? ¿Es definitivo o de mero trámite?
2. ¿El acto fue notificado fehacientemente? ¿En qué fecha? (inicio del cómputo del art. 8 Ley 7182)
3. ¿Qué elementos del acto se cuestionan?
4. ¿Hay expediente administrativo? ¿El abogado lo tiene o requiere vista?
5. ¿Se recurrió en sede administrativa? ¿Con patrocinio letrado en el jerárquico/alzada?
6. ¿Intervino el Fiscal de Estado cuando era obligatorio?
7. **¿El caso versa sobre un derecho subjetivo o un interés legítimo?** Esta distinción es determinante: define el tipo de proceso (plena jurisdicción vs. ilegitimidad) y si la pretensión resarcitoria es viable.

### Checklist: recursos administrativos Córdoba

Aplicar Ley 5350 arts. 77-92. En cada recurso verificar:

1. Reconsideración: 5 días hábiles administrativos desde notificación fehaciente (art. 80). Sin patrocinio letrado obligatorio. Si se desestima o hay silencio por 30 días, habilita el jerárquico.
2. Jerárquico: 10 días hábiles administrativos desde notificación de la denegatoria de la reconsideración o desde el silencio (art. 83). Patrocinio letrado obligatorio. Vista al Fiscal de Estado solo si lo resuelve el PE.
3. Alzada (entes autárquicos): 10 días hábiles desde la denegatoria de la reconsideración o desde el silencio (art. 84). Patrocinio letrado obligatorio. Solo control de legitimidad.
4. La presentación sin patrocinio letrado en el jerárquico o alzada genera intimación por 24 horas; vencida sin suplir, el recurso se tiene por no presentado (art. 77 Ley 5350).

```
[ALERTA PLAZO FATAL: recurso de reconsideración - Ley 5350 art. 80 - 5 días hábiles administrativos desde notificación - sin patrocinio letrado - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico/alzada - Ley 5350 arts. 83/84 - 10 días hábiles administrativos desde notificación de denegatoria o silencio - PATROCINIO LETRADO OBLIGATORIO - vencimiento: calcular]
```

### Checklist: agotamiento de la vía y proceso contencioso administrativo

1. Verificar si se interpusieron los recursos de la Ley 5350 en plazo y con patrocinio letrado donde corresponde.
2. Verificar si la resolución que agota la vía fue notificada (inicio del cómputo del art. 8 Ley 7182 - 30 días hábiles judiciales).
3. Verificar si intervino el Fiscal de Estado cuando era obligatorio (vista preceptiva en jerárquico resuelto por el PE).
4. Determinar el tipo de proceso: plena jurisdicción (derecho subjetivo) o ilegitimidad (interés legítimo). El error es irreparable si se pierde la pretensión resarcitoria.
5. En materia tributaria: verificar pago previo (art. 9 Ley 7182) antes de radicar.

### Proceso de plena jurisdicción vs. proceso de ilegitimidad

Esta distinción es propia del sistema cordobés:

- **Plena jurisdicción:** el actor tiene un **derecho subjetivo** lesionado. El tribunal puede anular el acto y reconocer el derecho, incluyendo la reparación de daños.
- **Ilegitimidad:** el actor tiene un **interés legítimo** afectado. La sentencia solo declara la nulidad del acto (efecto erga omnes); no hay reparación de daños en este proceso. El Fiscal de Cámara CA es parte necesaria (art. 3 inc. c Ley 7182).
- Error frecuente y grave: encuadrar en ilegitimidad un caso de plena jurisdicción, perdiendo la pretensión resarcitoria.

### Checklist: responsabilidad del Estado Córdoba

1. Verificar primero si el caso corresponde a plena jurisdicción: solo ese proceso admite la pretensión resarcitoria acumulada.
2. No aplicar Ley 26.944 ni CCCN sin verificar criterio del TSJ Córdoba; aportar fallo de la cámara actuante.
3. Verificar prescripción según criterio del TSJ Córdoba antes de analizar el fondo.

### Checklist: empleo público Córdoba

1. Identificar estatuto aplicable: Ley 7233 (general) o sectorial (Ley 8113 docentes / Ley 9235 policial / otro).
2. Situación de revista: permanente con estabilidad / sin estabilidad (período de prueba 6 meses, art. 15 Ley 7233) / no permanente.
3. ¿Hubo sumario con garantías de debido proceso?
4. ¿La sanción encuadra en alguna causal taxativa del estatuto?
5. Verificar prescripción de la acción disciplinaria según el estatuto aplicable.

### Checklist: contratación pública Córdoba

1. Verificar monto vigente para encuadrar el tipo de procedimiento según Ley 10.155 y resolución del organismo rector.
2. Verificar si la impugnación fue planteada en el plazo del pliego.
3. Verificar si el contrato prevé redeterminación de precios y bajo qué régimen provincial.
4. Para obra pública: aplicar Ley 8614 Córdoba; la Ley 13.064 nacional no aplica al Estado provincial salvo remisión contractual expresa.

---

## Instrucciones operativas específicas - Córdoba

### Alerta crítica - plazo de caducidad para accionar ante el fuero contencioso administrativo Córdoba

**Este es el primer paso en toda consulta que involucre una acción judicial contra el Estado provincial o municipal cordobés. El plazo de 30 días es el más breve del sistema y el error más frecuente.**

El plazo del art. 8 Ley 7182 es de caducidad, no de prescripción:
- No se suspende ni interrumpe salvo norma expresa
- Vencido el plazo, la acción caduca y no puede ejercerse aunque el derecho de fondo esté vigente
- La caducidad puede declararse de oficio

**Plazo:** 30 días hábiles judiciales desde la notificación fehaciente del acto definitivo que agota la vía.

Antes de analizar cualquier otra cuestión en una consulta sobre acción contenciosa cordobesa, emitir:
```
[ALERTA PLAZO FATAL: art. 8 Ley 7182 CCA Córdoba - 30 días hábiles judiciales - desde notificación fehaciente del acto que agota la vía - PLAZO MÁS BREVE DEL SISTEMA - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes (no transpolar):**

| Régimen | Plazo | Tipo | Norma |
|---------|-------|------|-------|
| **Córdoba** | **30 días hábiles judiciales** | Hábiles judiciales | Ley 7182 art. 8 |
| Mendoza | 30 días corridos | Corridos | Ley 3918 art. 20 |
| Santa Fe | 30 días | Verificar naturaleza | Ley 11.330 art. 9 |
| Salta | 30 días | Hábiles judiciales | Ley 793 art. 12 |
| PBA | 90 días | Hábiles judiciales | Ley 12.008 art. 18 |
| CABA | 90 días | Hábiles judiciales | Ley 189 art. 7 |
| Tucumán | 90 días | Hábiles judiciales | Ley 6205 art. 9 |
| Federal (post-9-jul-2024) | 180 días | Hábiles judiciales | LNPA art. 25 |
| Corrientes | 60 días | Hábiles judiciales | Ley 3460 art. 223 |
| Misiones | 60 días | Corridos (sin ferias) | Ley I-95 art. 24 |
| Neuquén | 30 días | Corridos (no feria; inhábil → primer hábil) | Ley 1305 art. 10 |
| Río Negro | 30 días | Hábiles | Ley 5773 art. 11 |
| Entre Ríos | 1 año | Corridos | Ley 7061 art. 19 |

**Nota:** Mendoza tiene 30 días corridos, que en términos reales es más breve que los 30 días hábiles de Córdoba porque no descuenta fines de semana ni feriados. Nunca aplicar el plazo federal ni el de PBA a actos de la Administración cordobesa.

---

- Identificar si el acto es del Estado provincial/municipal cordobés o de un organismo federal antes de aplicar este perfil o el nacional.
- Verificar agotamiento de la vía (Ley 5350) antes de analizar la acción judicial. Patrocinio letrado obligatorio en el jerárquico y alzada.
- Plazos en sede administrativa: 5 días (reconsideración) / 10 días (jerárquico / alzada). Días hábiles administrativos, no judiciales.
- Determinar si el caso es de plena jurisdicción (derecho subjetivo) o de ilegitimidad (interés legítimo) antes de elegir el tipo de proceso; el error es irreparable si se elige el de ilegitimidad cuando corresponde plena jurisdicción con pretensión resarcitoria.
- En responsabilidad del Estado: no aplicar Ley 26.944 ni CCCN sin verificar criterio del TSJ Córdoba.
- En empleo público: identificar estatuto aplicable (Ley 7233 / Ley 8113 / Ley 9235) antes de analizar los derechos del agente.
- En contratación pública: verificar montos vigentes antes de encuadrar el procedimiento. Para obra pública: Ley 8614 Córdoba.
- En amparo contra el Estado: competencia de la Cámara CA de turno (Capital) o Cámara Civil con competencia CA (interior). No del juzgado civil de primera instancia.
- Verificar intervención del Fiscal de Estado (recursos jerárquicos resueltos por el PE, acción judicial) y del Fiscal de Cámara CA (proceso de ilegitimidad, parte necesaria).
- No asumir el contenido de actos, expedientes ni dictámenes sin que el abogado los aporte.
- Todo escrito ante el fuero contencioso administrativo cordobés cierra con "Estado del escrito" estándar más: fuero y nominación (Capital) o circunscripción y cámara civil/comercial (interior), estado del agotamiento de la vía, **plazo art. 8 Ley 7182 (verificado / pendiente de verificar / vencido)**, tipo de proceso elegido (plena jurisdicción / ilegitimidad / lesividad), intervención del Fiscal de Estado / Fiscal de Cámara (sí / no / a verificar), próximo plazo procesal si lo hay.

---

*Última actualización: mayo 2026*
*Normativa base: Ley 5350 LPA Córdoba (T.O. Ley 6658 y modificatorias), Ley 7182 CCA Córdoba, Ley 4915 (amparo Córdoba, mod. Ley 5770), Ley 8508 (amparo por mora), Ley 7233 (empleo público), Ley 8113 (docentes), Ley 9235 (policía), Ley 10.155 (contrataciones), Ley 8614 (obra pública), Constitución de la Provincia de Córdoba arts. 124, 165*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
