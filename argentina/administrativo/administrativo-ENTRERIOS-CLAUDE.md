# Perfil de práctica · Derecho administrativo · Provincia de Entre Ríos

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Entre Ríos.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.

---

## Configuración inicial - completar antes de usar

**PROVINCIA:** Provincia de Entre Ríos

**FUERO_HABITUAL:** Superior Tribunal de Justicia de Entre Ríos (STJER) en pleno - única instancia en materia contencioso administrativa (art. 1 Ley 7061). Al igual que Mendoza, no existe un fuero contencioso administrativo de primera instancia separado: el STJER actúa como tribunal originario y en única instancia para las acciones contencioso administrativas.

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo Entre Ríos. Ej: "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, habilitaciones municipales, contratación pública, IOSPER".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos provinciales o municipales ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Salud ER, IOSPER, DGE, Municipalidad de Paraná, Municipalidad de Concordia".]

---

## Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Entre Ríos: procedimiento administrativo ante la Administración provincial (Ley 7060) y municipal, recursos administrativos en sede provincial, acción contencioso administrativa ante el Superior Tribunal de Justicia en pleno (Ley 7061), responsabilidad del Estado provincial, empleo público provincial y contratación pública provincial.

**Particularidad estructural central - única instancia en el STJER:** al igual que Mendoza, en Entre Ríos no existe un fuero contencioso administrativo de primera instancia. El **Superior Tribunal de Justicia de Entre Ríos (STJER)** actúa en pleno como tribunal originario y en instancia única para las acciones contencioso administrativas (art. 1 Ley 7061). No hay apelación ordinaria de la sentencia definitiva ante otra instancia local.

**Diferencia clave con Mendoza:** el plazo de caducidad de la acción en Entre Ríos es de **1 año** (art. 19 Ley 7061), significativamente más largo que el de Mendoza (30 días corridos), PBA (90 días hábiles), Córdoba (30 días hábiles) o Santa Fe (30 días).

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Entre Ríos (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal entrerriана, aplica este perfil. No transpolar plazos ni institutos.

**Tercer nivel - organismos municipales:** los actos de los municipios entrerrianos son impugnables ante el STJER por la Ley 7061, previo agotamiento de la vía administrativa municipal. El art. 7 Ley 7061 exige que se hayan agotado los procedimientos de control de legitimidad del PE cuando se trata de entes desconcentrados, descentralizados o no estatales. Para actos directamente emanados del Intendente o del Concejo Deliberante: verificar si hay recursos administrativos obligatorios ante el municipio y si el PE provincial tiene instancia de control antes de ocurrir al STJER. Verificar jurisprudencia del STJER.

---

## Normativa de procedimiento administrativo provincial

### Ley de procedimiento administrativo Entre Ríos

- **Norma principal:** Ley 7060 (Ley de Procedimientos Administrativos de la Provincia de Entre Ríos), sancionada el 25/01/1983
- **Sin decreto reglamentario separado:** la Ley 7060 es la norma de procedimiento para toda la Administración centralizada y descentralizada provincial. Los municipios pueden tener ordenanzas propias.
- **Texto vigente:** consultar el portal del Poder Judicial de Entre Ríos (https://www.jusentrerios.gov.ar) y el portal oficial de la provincia (https://www.entrerios.gov.ar)
- **Articulado clave:** art. 18 (términos - días hábiles), arts. 55-56 (recurso de revocatoria), arts. 60-65 (recurso de apelación jerárquica), arts. 69-70 (recurso de queja), arts. 72-76 (recurso de revisión)

**Nota:** hay un proyecto de ley de procedimiento administrativo en estudio en la legislatura entrerriana (Expediente E22027-03052017) que reformaría la Ley 7060. Al momento de este perfil (mayo 2026), la Ley 7060 sigue vigente. Verificar si fue sancionado el nuevo texto.

```
[VERIFICAR VIGENCIA: Ley 7060 LPA Entre Ríos - consultar https://www.jusentrerios.gov.ar - verificar si fue sancionada nueva ley de procedimiento administrativo]
```

### Régimen de silencio administrativo Entre Ríos

- **Regla general:** silencio negativo (denegatoria tácita). La Ley 7061 (art. 5) establece que hay denegación tácita cuando formulada una petición no se resuelve definitivamente dentro de los 60 días corridos de estar el expediente en estado de ser resuelto, o cuando el órgano no dicta providencias de trámite en los plazos fijados y transcurren 60 días corridos desde el vencimiento del término.
- **Sin reforma análoga al Dec 971/2024 nacional:** Entre Ríos no adoptó el régimen de silencio positivo de la Ley 27.742 nacional. El silencio positivo aplica solo ante la Administración nacional. No transpolar ese régimen al Estado provincial entrerriano.

```
[VERIFICAR SILENCIO ENTRE RÍOS: Ley 7061 art. 5 - denegación tácita a los 60 días corridos sin resolver - inicio del cómputo del plazo del art. 19 en caso de denegación tácita]
```

### Elementos esenciales del acto administrativo Entre Ríos

La Ley 7060 regula los elementos esenciales del acto administrativo con estructura análoga al régimen federal:
1. Competencia del órgano provincial o municipal
2. Causa: antecedentes de hecho y de derecho
3. Objeto: cierto, lícito, posible
4. Procedimiento: trámites esenciales previos (incluye intervención del Fiscal de Estado cuando corresponde)
5. Motivación: expresión concreta de las razones del acto
6. Finalidad: adecuada al ordenamiento provincial

Verificar articulado específico de la Ley 7060 sobre requisitos del acto y nulidades.

### Recursos administrativos Entre Ríos (Ley 7060)

**Recurso de revocatoria (arts. 55-57 Ley 7060):**
- Plazo: 5 días hábiles administrativos desde la notificación de la resolución (art. 56)
- Ante: la misma autoridad que dictó el acto
- Es optativo (art. 55); no es obligatorio para agotar la vía
- La autoridad debe resolver en 10 días, excepto cuando se trate de un acto del PE

**Recurso de apelación jerárquica (arts. 60-65 Ley 7060):**
- Procede contra actos o decisiones de una autoridad administrativa sometida a vínculo jerárquico, cuando lesionen un derecho o interés legítimo
- **Plazo: 10 días hábiles administrativos** desde la notificación del acto o desde el silencio de la revocatoria (art. 61 Ley 7060)
- Ante: el superior jerárquico del órgano emisor, recorriendo la línea jerárquica hasta el Gobernador
- La decisión del Gobernador o de la máxima autoridad agota la vía

**Recurso de queja (arts. 69-70 Ley 7060):**
- Por mora o defecto en el trámite
- No interrumpe el plazo para interponer otros recursos

**Recurso de revisión (arts. 72-76 Ley 7060):**
- Procede en sede administrativa para revisar un acto firme en supuestos taxativos: contradicciones en la parte dispositiva, documentos falsos, prevaricato o cohecho
- Puede interponerse "en cualquier tiempo" (art. 79); se resuelve en 30 días

**Recurso de gracia (arts. 78-79 Ley 7060):**
- Ante la misma autoridad que dictó el acto, para obtener su modificación por razones de equidad
- Se interpone "en cualquier tiempo"; se resuelve en 30 días

**Sin reforma análoga al Decreto 695/2024 nacional:** Entre Ríos no duplicó los plazos de recursos administrativos. Los plazos de la Ley 7060 son los originales (5 días para la revocatoria). No aplicar los plazos federales reformados.

**Días hábiles administrativos (art. 18 Ley 7060):** los términos se cuentan desde el día siguiente de la notificación y solo se computan días hábiles.

```
[ALERTA PLAZO FATAL: recurso de revocatoria - Ley 7060 art. 56 - 5 días hábiles administrativos desde notificación - OPTATIVO pero su interposición puede ser conveniente - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de apelación jerárquica - Ley 7060 arts. 60-65 - verificar plazo específico en el articulado - ante el superior jerárquico - vencimiento: calcular]
```

### Agotamiento de la vía administrativa Entre Ríos

- **Regla general:** es requisito previo a la acción contencioso administrativa ante el STJER. El acto debe ser "definitivo y causar estado" (art. 4 Ley 7061).
- **Reclamación previa obligatoria:** los hechos administrativos no generan directamente la acción; siempre es necesaria la reclamación administrativa para obtener la decisión impugnable (art. 6 Ley 7061).
- **Entes desconcentrados, descentralizados y no estatales (art. 7 Ley 7061):** la acción no procede cuando no se han agotado los procedimientos para hacer efectivo el control de legitimidad del PE. Para colegios profesionales: la vía se agota conforme a sus respectivas normas de creación.
- **Límite de pretensiones (art. 10 Ley 7061):** las acciones deben limitarse a las cuestiones debatidas previamente en las reclamaciones o recursos administrativos. Lo no planteado en sede administrativa no puede introducirse en la acción ante el STJER.

```
[VERIFICAR AGOTAMIENTO DE VÍA ENTRE RÍOS: Ley 7060 + Ley 7061 arts. 4, 6 y 7 - verificar cadena recursiva completa - para entes descentralizados: control de legitimidad del PE previo - límite de pretensiones art. 10 Ley 7061]
```

### Tabla unificada de plazos - sede administrativa y judicial

| Recurso / instituto | Plazo | Tipo de días | Norma |
|---------------------|-------|--------------|-------|
| Revocatoria (optativa) | 5 días | Hábiles administrativos | Ley 7060 art. 56 |
| Apelación jerárquica | 10 días | Hábiles administrativos | Ley 7060 art. 61 |
| Denegación tácita | 60 días corridos sin resolver | Corridos | Ley 7061 art. 5 |
| Acción ante el STJER | 1 año | Corridos | Ley 7061 art. 19 |
| Revisión y gracia (sede administrativa) | En cualquier tiempo | - | Ley 7060 arts. 72-79 |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial. El plazo de la acción ante el STJER es en días corridos (art. 20 Ley 7061, remite al art. 6 CCCN).

---

## Control judicial contencioso administrativo

### Código Procesal Administrativo Entre Ríos

- **Norma:** Ley 7061 (Código Contencioso Administrativo de la Provincia de Entre Ríos), sancionada el 25/01/1983 y publicada el 02/02/1983, y modificatorias
- **Texto vigente:** https://www.jusentrerios.gov.ar y SAIJ. Verificar modificaciones posteriores a mayo 2026.
- **Base constitucional:** art. 204 y ss. Constitución Entre Ríos (el STJER tiene competencia originaria en determinadas materias, incluyendo la contencioso administrativa por la vía de la Ley 7061).
- **Subsidiariedad:** el Código Procesal Civil y Comercial de Entre Ríos se aplica en materia de plazos y notificaciones (art. 18 Ley 7061) y supletoriamente en todo lo no previsto.

### Plazo de caducidad para accionar judicialmente

**Este es el dato más crítico del perfil. El plazo entrerriано es el MÁS LARGO de los cinco sistemas analizados: 1 año.**

- **Plazo:** 1 año desde el día siguiente al de la notificación de la decisión administrativa; o, en caso de denegación tácita, desde el día siguiente al del vencimiento del plazo del art. 5 inc. b (art. 19 Ley 7061)
- **Cómputo:** conforme al art. 25 del Código Civil (hoy art. 6 CCCN) - días corridos (art. 20 Ley 7061)
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa
- **¿Declarable de oficio?:** sí, por el STJER
- **Acción de lesividad (art. 17 inc. e Ley 7061):** el STJER también conoce en las acciones de lesividad (anulación de actos irrevocables previamente declarados lesivos por el PE)

```
[ALERTA PLAZO FATAL: art. 19 Ley 7061 CCA Entre Ríos - 1 AÑO corrido - desde notificación de la decisión que agota la vía - PLAZO MÁS LARGO DEL SISTEMA - vencimiento: calcular]
```

**Diferencia con otros regímenes:**
- Federal: 180 días hábiles judiciales (actos post-9-jul-2024)
- PBA: 90 días hábiles judiciales
- Córdoba: 30 días hábiles judiciales
| Régimen | Plazo | Tipo | Norma |
|---------|-------|------|-------|
| Córdoba | 30 días | Hábiles judiciales | Ley 7182 art. 8 |
| Salta | 30 días | Hábiles judiciales | Ley 793 art. 12 |
| Santa Fe | 30 días | A verificar | Ley 11.330 art. 9 |
| Neuquén | 30 días | Corridos (no feria; inhábil → primer hábil) | Ley 1305 art. 10 |
| Río Negro | 30 días | Hábiles | Ley 5773 art. 11 |
| Mendoza | 30 días | Corridos | Ley 3918 art. 20 |
| Corrientes | 60 días | Hábiles judiciales | Ley 3460 art. 223 |
| Misiones | 60 días | Corridos (sin ferias) | Ley I-95 art. 24 |
| PBA | 90 días | Hábiles judiciales | Ley 12.008 art. 18 |
| CABA | 90 días | Hábiles judiciales | Ley 189 art. 7 |
| Tucumán | 90 días | Hábiles judiciales | Ley 6205 art. 9 |
| **Entre Ríos** | **1 año** | **Corridos** | **Ley 7061 art. 19** |
| Federal (post-9-jul-2024) | 180 días | Hábiles judiciales | LNPA art. 25 |

Aunque el plazo es más largo, igual es de caducidad: su vencimiento extingue la acción. No descuidar el seguimiento del plazo por considerarlo extenso.

### Tribunal competente

**Superior Tribunal de Justicia de Entre Ríos (STJER) en pleno:**
- Competencia: originaria, exclusiva y en única instancia para todas las acciones contencioso administrativas (art. 1 Ley 7061)
- Actúa en pleno (todos los miembros del STJER)
- Radicación: Paraná (capital provincial)
- **No hay primera instancia separada:** a diferencia de PBA y Córdoba, no existen juzgados ni cámaras de primera instancia en lo contencioso administrativo. El STJER es el tribunal en instancia única ordinaria.

**Recursos contra la sentencia definitiva del STJER:**
- Recurso extraordinario federal ante la CSJN (art. 14 Ley 48): única vía de revisión ordinaria
- El STJER también actúa como tribunal de casación e inconstitucionalidad en otras materias, pero en materia contencioso administrativa su sentencia es definitiva sin instancia ordinaria de revisión local

**Fiscal del Superior Tribunal:**
- Interviene en los conflictos de competencia (art. 11 Ley 7061) y en el proceso contencioso administrativo
- Cuando la parte demandada es la Provincia, la representación corresponde a la Fiscalía de Estado

**Ministerio Público Fiscal:**
- Ley 9544 (Ley Orgánica del Ministerio Público de Entre Ríos). El Fiscal del STJER y los Fiscales de Cámara tienen intervención en el proceso.

### Actos impugnables (Ley 7061)

Procede la acción contra toda violación de un derecho subjetivo o interés legítimo regido por norma administrativa (art. 1). También son impugnables (art. 2):
- Actos discrecionales cuando la impugnación se funde en ilegitimidad
- Actos separables de contratos en la actividad administrativa
- Actos sobre reclamos por retribuciones, jubilaciones o pensiones de agentes estatales (excepto los regidos por derecho del trabajo)

**No corresponden a esta vía (art. 3 Ley 7061):**
- Juicios ejecutivos, de apremio, desalojo, interdictos, acciones posesorias
- Juicios de expropiación
- Los que deban resolverse aplicando exclusivamente normas de derecho privado o del trabajo
- Conflictos provenientes de convenios laborales
- **Importante excepción:** los reclamos de daños y perjuicios ocasionados por agentes, cosas o hechos de la Administración **cuando no se produzcan por incumplimiento o en relación a la vinculación especial de derecho público** (art. 3 inc. e). Esto implica que los daños extracontractuales puros (sin vínculo especial administrativo) pueden no corresponder al STJER. Verificar jurisprudencia del STJER sobre la determinación de competencia en responsabilidad del Estado.

### Pretensiones admisibles (art. 17 Ley 7061)

- Anulación total o parcial de la disposición administrativa impugnada
- Restablecimiento o reconocimiento del derecho vulnerado, desconocido o incumplido
- Resarcimiento de los daños y perjuicios sufridos
- Interpretación que corresponde a la norma en cuestión
- Anulación de actos irrevocables administrativamente, previamente declarados lesivos por el PE (lesividad)

**Límite de pretensiones (art. 10 Ley 7061):** las acciones deben limitarse a lo debatido en las reclamaciones o recursos administrativos previos. Lo no planteado allí no puede introducirse ante el STJER.

### Suspensión de la ejecución del acto (medida cautelar) (arts. 21-29 Ley 7061)

- **Oportunidad:** previa, simultánea o posterior a la interposición de la acción
- **Trámite:** previa vista de 5 días a la demandada; el STJER resuelve en 5 días
- **Requisito:** que "prima facie" la disposición sea nula o pueda producir un daño irreparable si apareciere como anulable
- **Contracautela:** a criterio del tribunal
- **Suspensión antes de la acción:** si se solicita antes de interponer la acción, caduca automáticamente si la acción no se deduce en el plazo legal (art. 27 Ley 7061). Dado que el plazo es de 1 año, el riesgo es menor que en Mendoza, pero aplica igual.
- **Levantamiento por interés público:** la demandada puede pedir el levantamiento alegando grave daño al interés público; el tribunal resuelve declarando a cargo del peticionante la responsabilidad por perjuicios si prospera la demanda.

```
[VERIFICAR RÉGIMEN CAUTELAR ENTRE RÍOS: Ley 7061 arts. 21 y ss. - vista previa 5 días a la demandada - verificar si hay restricciones específicas según el tipo de acto]
```

### Amparo Entre Ríos

- **Norma:** art. 66 y ss. Constitución Entre Ríos (2008) + Ley 8369 (Procedimientos Constitucionales, 1990) modificada por Ley 10704 y otras.
- **Competencia:** el amparo individual en materia administrativa tramita ante los Juzgados de Primera Instancia (no el STJER). La Sala de Procedimientos Constitucionales y Penal del STJER conoce en el recurso de apelación contra las sentencias de los juzgados en amparo.
- **[CONFIRMADO] Plazo general (art. 3 inc. c Ley 8369):** **30 días corridos** desde el momento en que el acto fue ejecutado, debió producirse, o desde que el titular del derecho conoció o pudo conocer sus efectos de manera efectiva. Al ser corridos no se suspende por feriados ni días inhábiles; opera como caducidad formal que los jueces analizan de oficio.
- **[CONFIRMADO] Omisiones lesivas continuadas:** cuando la afectación es de tracto sucesivo (ej. falta de pago reiterada de haberes o prestaciones de salud), el cómputo de los 30 días se renueva mes a mes con cada iteración del daño. Criterio consolidado en la jurisprudencia del STJER.
- **[CONFIRMADO] Amparos especiales (Ley 10704 — Capítulo V):**
  - **Amparo por mora (art. 63 y ss.):** sin el plazo de caducidad de 30 días del amparo común. Requiere: (1) vencimiento del plazo legal de la autoridad para resolver (o plazo prudencial de 30 días hábiles en su defecto); (2) presentación de pronto despacho; (3) transcurso de otros 10 días hábiles adicionales sin respuesta. Recién entonces queda expedita la vía del amparo por mora.
  - **Amparo ambiental (art. 65 y ss.):** se rige por el trámite rápido del amparo genérico. El STJER flexibiliza el plazo de 30 días cuando la afectación o el riesgo de daño es de ilegalidad continuada o de tracto sucesivo (principio precautorio + naturaleza de los derechos difusos). Ley 9032 como normativa complementaria.
- **Subsidiariedad:** procede cuando no existe otra vía judicial más idónea y urgente.
- **Amparo colectivo:** art. 66 Const. Entre Ríos 2008 amplió la legitimación activa.
- **Acción popular de inconstitucionalidad:** art. 61 Const. Entre Ríos — cualquier habitante puede ejercerla ante el STJER; es distinta de la acción contencioso administrativa.

```
[ALERTA PLAZO FATAL: amparo Entre Ríos - art. 3 inc. c Ley 8369 - 30 días corridos desde que el acto fue ejecutado o conocido - caducidad - NO se suspende por feriados ni inhábiles - EXCEPCIÓN omisiones continuadas: cómputo se renueva mes a mes]
[AMPARO POR MORA: Ley 10704 art. 63 y ss. - sin plazo de caducidad - requiere vencimiento del plazo + pronto despacho + 10 días hábiles adicionales sin respuesta]
```

---

## Normativa de referencia Entre Ríos

### Responsabilidad del Estado provincial

- **Sin ley propia equivalente a Ley 26.944 nacional:** Entre Ríos no sancionó una ley de responsabilidad del Estado equivalente a la Ley 26.944. Ésta no aplica a demandas contra el Estado provincial entrerriano.
- **Competencia del STJER en responsabilidad:** el art. 3 inc. e Ley 7061 excluye de la competencia contencioso administrativa los daños "cuando no se produzcan por incumplimiento o en relación a la vinculación especial de derecho público contractual o reglamentaria". Los daños derivados de responsabilidad extracontractual pura del Estado pueden tramitar ante el fuero civil y no ante el STJER. Verificar jurisprudencia del STJER sobre el punto antes de radicar.
- **Régimen aplicable:** principios generales del derecho administrativo y jurisprudencia del STJER. La pretensión resarcitoria puede acumularse a la anulatoria cuando el daño deriva del incumplimiento o de la vinculación especial de derecho público (art. 17 inc. c Ley 7061).
- **No aplicar CCCN:** no invocar arts. 1757, 1741 ni otros del CCCN en demandas contra el Estado provincial sin verificar criterio del STJER.
- **Prescripción de la acción:** verificar criterio del STJER; puede diferir del plazo federal.

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD ENTRE RÍOS: sin ley propia - verificar si el daño corresponde al STJER (vinculación especial de derecho público) o al fuero civil (daños extracontractuales puros) - jurisprudencia STJER sobre art. 3 inc. e Ley 7061]
```

### Empleo público Entre Ríos

- **Estatuto general:** Ley 8115 (Estatuto del Personal de la Administración Pública Provincial de Entre Ríos) y modificatorias. Regula las relaciones laborales del personal dependiente del Poder Ejecutivo provincial.
- **Escalafón:** verificar decreto de escalafón general vigente.
- **Régimen disciplinario:** Ley 8115 + reglamentación. Sumario administrativo con garantías de debido proceso.
- **Los actos sobre retribuciones, jubilaciones y pensiones (art. 2 inc. c Ley 7061):** son expresamente impugnables ante el STJER, excepto los regidos por el derecho del trabajo.
- **Estatutos sectoriales principales:**
  - Docentes: DGE (Dirección General de Educación); verificar estatuto docente provincial
  - Policía: verificar Ley Orgánica de la Policía de Entre Ríos (Ley 8100 y modificatorias)
  - Personal de salud: verificar norma sectorial vigente
  - IOSPER (Instituto de Obra Social de la Provincia de Entre Ríos): ente autárquico con régimen especial; sus resoluciones son impugnables ante el STJER
  - Personal municipal: verificar si el municipio tiene estatuto propio o remite a la Ley 8115 supletoriamente
  - [COMPLETAR: otros estatutos sectoriales según las áreas de práctica habituales]

```
[VERIFICAR ESTATUTO APLICABLE ENTRE RÍOS: Ley 8115 general o estatuto sectorial según el organismo - para docentes: verificar estatuto docente / policial: Ley 8100]
```

### Contratación pública Entre Ríos

- **Norma general:** Ley 10.027 (Régimen de Contrataciones del Estado Provincial de Entre Ríos), sancionada en 2011. Derogó el régimen anterior (Ley 5140). Verificar decretos reglamentarios vigentes y actualizaciones de montos.
- **Reglamento:** verificar decretos reglamentarios vigentes. Los montos y procedimientos se actualizan por decreto o resolución del Poder Ejecutivo.
- **Plataforma de compras:** verificar sistema electrónico de contrataciones vigente en Entre Ríos (portal https://compras.entrerios.gov.ar o equivalente).
- **Obra pública provincial:** verificar ley de obras públicas provincial vigente. La Ley 13.064 (obra pública nacional) no aplica supletoriamente salvo remisión contractual expresa.
- **Impugnación de licitaciones:** verificar plazos en la norma de contrataciones provincial y en cada pliego.

```
[VERIFICAR VIGENCIA: normativa de contrataciones Entre Ríos - los montos de licitación pública/privada/contratación directa se actualizan - verificar antes de encuadrar el procedimiento - consultar https://www.entrerios.gov.ar]
```

### Organismos de control Entre Ríos

**Tribunal de Cuentas de Entre Ríos:**
- Control externo de la hacienda pública provincial. Tiene función jurisdiccional. Sus resoluciones definitivas son impugnables ante el STJER por la vía de la Ley 7061.

**Fiscalía de Estado de Entre Ríos:**
- Representante legal del Estado provincial en juicio. Es parte necesaria en las acciones contencioso administrativas ante el STJER cuando la demandada es la Provincia.
- Las notificaciones a la Fiscalía de Estado se hacen en su despacho oficial.
- Interviene con vista cuando es preceptivo en los recursos administrativos resueltos por el PE.

**Ministerio Público Fiscal:**
- El Fiscal del STJER interviene en los conflictos de competencia (art. 11 Ley 7061) y en el proceso contencioso administrativo.

**IOSPER (Instituto de Obra Social de la Provincia de Entre Ríos):**
- Ente autárquico. Sus resoluciones son frecuentemente impugnadas ante el STJER. Verificar el régimen de recursos previos ante el propio IOSPER antes de ocurrir al STJER (art. 7 Ley 7061 - control de legitimidad del PE previo para entes descentralizados).

**Defensor del Pueblo de Entre Ríos:**
- Art. 196 Constitución Entre Ríos (2008). Legitimación para actuar en defensa de derechos colectivos.

---

## Alerta normativa - normas de vigencia variable

*Última verificación de esta sección: mayo 2026. Actualizar cuando cambie alguna de las normas listadas.*

### Plazo de caducidad CCA Entre Ríos

```
[ALERTA PLAZO CADUCIDAD: art. 19 Ley 7061 CCA Entre Ríos - 1 AÑO corrido - desde notificación de la decisión que agota la vía - cómputo conforme art. 6 CCCN (días corridos) - vencimiento: calcular]
```

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública:** actualizados por decreto o resolución. Verificar antes de encuadrar el procedimiento.
- **Escala salarial empleo público:** se modifica por paritarias. Verificar resolución de homologación vigente.
- **Nueva ley de procedimiento administrativo:** proyecto en curso (Expediente E22027-03052017). Verificar si fue sancionado.
- **Modificaciones a la Ley 8369 (amparo):** la Ley 10704 incorporó el Capítulo V de Amparos Especiales (mora y ambiental). Plazo general del amparo: 30 días corridos (art. 3 inc. c); el plazo del amparo por mora no aplica al cómputo general. [CONFIRMADO]
- **Habilitaciones municipales:** el régimen varía por municipio (Paraná, Concordia, Gualeguaychú tienen ordenanzas propias). Verificar norma vigente al momento del acto.

```
[VERIFICAR VIGENCIA: norma Entre Ríos - [materia] - consultar Boletín Oficial Entre Ríos (https://www.entrerios.gov.ar) antes de aplicar]
```

## Responsables procesales por instancia

| Instancia | Representante | Rol | Normativa |
|-----------|---------------|-----|-----------|
| STJER en pleno (única instancia) - Provincia como demandada | Fiscalía de Estado de Entre Ríos | Representante legal del Estado provincial en juicio; parte necesaria | Ley 7061 + Constitución ER |
| STJER en pleno - conflictos de competencia | Fiscal del STJER (Ministerio Público) | Dictamina en conflictos de competencia | Ley 7061 art. 11 |
| Proceso contencioso administrativo - intervención del Ministerio Público | Fiscal del STJER | Interviene según praxis del tribunal | Ley 9544 (Ley Orgánica del Ministerio Público ER) |
| Recursos administrativos ante el PE | Fiscalía de Estado (vista cuando es preceptiva) | Dictamina antes del acto del PE | Ley 7060 |
| CSJN (REF) | Fiscalía de Estado de Entre Ríos | - | - |
| Amparo (1ª instancia, juzgados) | Fiscalía de Estado | Parte necesaria cuando el Estado es demandado | Ley 8369 |

**Distinción operativa clave:** la Fiscalía de Estado representa al Estado provincial como demandado. El Fiscal del STJER (Ministerio Público) tiene un rol diferente: dictamina en conflictos de competencia y actúa como parte en el proceso. No son el mismo órgano. Las notificaciones a la Fiscalía de Estado se hacen en su despacho oficial.

```
[VERIFICAR REPRESENTACIÓN PROCESAL ENTRE RÍOS: Fiscalía de Estado como parte necesaria cuando el Estado es demandado - Fiscal del STJER (Ministerio Público) tiene rol diferente (conflictos de competencia, art. 11 Ley 7061) - notificaciones a la Fiscalía en despacho oficial]
```

---

## Fuentes primarias

- **Portal oficial Entre Ríos:** https://www.entrerios.gov.ar
- **Boletín Oficial Entre Ríos:** https://boletin.entrerios.gov.ar
- **Poder Judicial Entre Ríos (jurisprudencia y normativa):** https://www.jusentrerios.gov.ar
- **Fiscalía de Estado Entre Ríos:** verificar URL vigente en el portal provincial
- **Tribunal de Cuentas Entre Ríos:** verificar URL vigente
- **IOSPER:** https://www.iosper.gov.ar
- **Portal de compras Entre Ríos:** https://compras.entrerios.gov.ar (verificar URL vigente)

---

## Reglas de citación - administrativo Entre Ríos

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para el STJER en materia contencioso administrativa:

**Jurisprudencia:** nunca citar expediente o carátula sin material aportado. El STJER actúa en pleno; verificar la composición del pleno al momento del fallo. Usar:
```
[INSERTAR FALLO VERIFICADO: STJER En Pleno / Sala Procedimientos Constitucionales - doctrina requerida]
```

**Actos administrativos Entre Ríos:** no asumir el contenido de resoluciones, dictámenes de la Fiscalía de Estado o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos CCA Entre Ríos:** no transpolar plazos de otros regímenes. Usar:
```
[ALERTA PLAZO CADUCIDAD: art. 19 Ley 7061 CCA Entre Ríos - 1 año corrido desde notificación de la decisión que agota la vía - vencimiento: calcular]
```

---

## Lógica de análisis por institución

### Checklist: acto administrativo provincial/municipal

Aplicar Ley 7060 LPA Entre Ríos. Elementos: competencia, causa, objeto, procedimiento, motivación, finalidad.

1. ¿Qué acto se impugna? ¿Es del Estado provincial o de un municipio? ¿Es definitivo y causa estado?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo del art. 19 Ley 7061 - 1 año)
3. ¿Qué elementos del acto se cuestionan? ¿Hay vicio de ilegitimidad?
4. ¿Hay expediente administrativo? ¿El abogado lo tiene o requiere vista?
5. ¿Se interpusieron los recursos de la Ley 7060? La revocatoria es optativa (5 días); la apelación jerárquica es el recurso que articula el agotamiento (10 días).
6. ¿El ente requería control de legitimidad del PE previo? (art. 7 Ley 7061)
7. ¿Las pretensiones que se quieren plantear ante el STJER coinciden con lo planteado en sede administrativa? (art. 10 Ley 7061)
8. ¿La pretensión resarcitoria deriva de la vinculación especial de derecho público o es un daño extracontractual puro? (determina competencia del STJER o del fuero civil)

### Checklist: recursos administrativos Entre Ríos

Aplicar Ley 7060 arts. 55-79. En cada recurso verificar:

1. Revocatoria: optativa, 5 días hábiles administrativos (art. 56). Si no se interpone, puede ir directamente a la apelación jerárquica.
2. Apelación jerárquica: 10 días hábiles administrativos desde notificación del acto o desde el silencio de la revocatoria (art. 61).
3. Articular en sede administrativa todas las pretensiones que se quieran sostener ante el STJER.
4. Revisión (arts. 72-76) y gracia (arts. 78-79): en cualquier tiempo, para supuestos taxativos. No interrumpen el plazo del art. 19 Ley 7061.

```
[ALERTA PLAZO FATAL: recurso de revocatoria (optativo) - Ley 7060 art. 56 - 5 días hábiles administrativos desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de apelación jerárquica - Ley 7060 art. 61 - 10 días hábiles administrativos desde notificación del acto o desde el silencio de la revocatoria - vencimiento: calcular]
```

### Checklist: agotamiento de la vía y acción contencioso administrativa

1. Verificar si la decisión es definitiva y causa estado (art. 4 Ley 7061).
2. Para entes descentralizados y no estatales: verificar control de legitimidad del PE (art. 7 Ley 7061).
3. Verificar que el objeto de la acción no supere lo planteado en sede administrativa (art. 10 Ley 7061).
4. Calcular el plazo de **1 año corrido** desde la notificación de la decisión que agota la vía (art. 19 Ley 7061, cómputo conforme art. 6 CCCN).
5. Verificar si la pretensión resarcitoria corresponde al STJER (art. 3 inc. e y art. 17 inc. c Ley 7061) o al fuero civil.

### Checklist: responsabilidad del Estado Entre Ríos

1. **Verificar competencia antes de radicar:** si el daño no deriva de la vinculación especial de derecho público, puede corresponder al fuero civil (art. 3 inc. e Ley 7061). El error de radicación puede ser irrecuperable.
2. No aplicar Ley 26.944 ni CCCN sin verificar criterio del STJER.
3. La pretensión resarcitoria puede acumularse a la anulatoria cuando el daño corresponde al STJER (art. 17 inc. c Ley 7061).
4. Verificar prescripción según criterio del STJER.

```
[INSERTAR FALLO VERIFICADO: STJER En Pleno - criterio para determinar si el daño corresponde al fuero CA o al fuero civil (art. 3 inc. e Ley 7061)]
```

### Checklist: empleo público Entre Ríos

1. Identificar estatuto aplicable: Ley 8115 (general) o sectorial (docentes / Ley 8100 policial / IOSPER / municipal).
2. Situación de revista del agente.
3. ¿Hubo sumario con garantías de debido proceso?
4. Si la pretensión involucra retribuciones, jubilaciones o pensiones: impugnable ante el STJER (art. 2 inc. c Ley 7061) salvo relaciones de derecho del trabajo.
5. Plazo de 1 año corrido desde el acto que agota la vía.

### Checklist: contratación pública Entre Ríos

1. Verificar normativa vigente (Ley 10.027) y montos actualizados por resolución del PE.
2. Verificar plazos de impugnación de pliegos y preadjudicación en la norma y en el pliego específico.
3. Para obra pública: verificar ley provincial; la Ley 13.064 nacional no aplica al Estado provincial salvo remisión contractual expresa.

---

## Instrucciones operativas específicas - Entre Ríos

### Alerta sobre el plazo de caducidad

El plazo de 1 año de la Ley 7061 es el más largo de los sistemas analizados, pero eso no implica que pueda descuidarse:
- Es de caducidad, no de prescripción: su vencimiento extingue la acción sin posibilidad de suspensión o interrupción salvo norma expresa
- El STJER lo verifica de oficio
- El cómputo es en días corridos (art. 20 Ley 7061 remite al art. 25 CC, hoy art. 6 CCCN)
- En caso de denegación tácita: el plazo corre desde el día siguiente al del vencimiento de los 60 días del art. 5 Ley 7061; verificar ese punto de inicio con precisión

Antes de analizar cualquier otra cuestión, emitir:
```
[ALERTA PLAZO CADUCIDAD: art. 19 Ley 7061 CCA Entre Ríos - 1 AÑO corrido desde notificación de la decisión que agota la vía - cómputo conforme art. 6 CCCN - vencimiento: calcular]
```

**Alerta adicional - competencia en responsabilidad:** verificar si el daño reclamado corresponde al STJER (vinculación especial de derecho público) o al fuero civil (daño extracontractual puro). El error de radicación puede ser irrecuperable.

---

- Identificar si el acto es del Estado provincial entrerriano, de un municipio entrerriano o de un organismo federal antes de aplicar este perfil o el nacional.
- El STJER actúa en pleno y en única instancia; no hay primera instancia contencioso administrativa separada.
- Verificar agotamiento de la vía (Ley 7060) antes de analizar la acción. Para entes descentralizados: control de legitimidad del PE previo (art. 7 Ley 7061).
- Articular en sede administrativa todas las pretensiones; las no planteadas allí no pueden introducirse ante el STJER (art. 10 Ley 7061).
- El plazo es de 1 año corrido. Calcularlo con días corridos incluyendo fines de semana y feriados.
- Verificar si la pretensión resarcitoria corresponde al STJER o al fuero civil antes de radicar.
- Amparo: competencia de los juzgados de primera instancia (no el STJER). La Sala Procedimientos Constitucionales del STJER conoce en alzada.
- Acción popular de inconstitucionalidad: cualquier habitante puede interponerla ante el STJER (art. 61 Constitución Entre Ríos) - distinta de la acción contencioso administrativa.
- Verificar intervención preceptiva de la Fiscalía de Estado.
- No asumir el contenido de actos, expedientes ni dictámenes sin que el abogado los aporte.
- Todo escrito ante el STJER en materia contencioso administrativa cierra con "Estado del escrito" estándar más: estado del agotamiento de la vía (incluyendo control de legitimidad del PE si corresponde), **plazo art. 19 Ley 7061 (verificado / pendiente de verificar / vencido)**, verificación de competencia del STJER en la pretensión resarcitoria, verificación de coincidencia entre pretensiones judiciales y planteadas en sede administrativa (art. 10), intervención de Fiscalía de Estado (sí / no / a verificar).

---

*Última actualización: mayo 2026*
*Normativa base: Ley 7060 LPA Entre Ríos, Ley 7061 (Código Contencioso Administrativo Entre Ríos), Ley 8369 (Procedimientos Constitucionales, mod. Ley 10704), Ley 8115 (empleo público), Ley 8100 (policía), Ley 9032 (amparo ambiental), Constitución de Entre Ríos (2008) arts. 61, 66, 196, 204 y ss.*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
