# Perfil de práctica · Derecho administrativo · Provincia de Mendoza

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Mendoza.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.

---

## Configuración inicial - completar antes de usar

**PROVINCIA:** Provincia de Mendoza

**FUERO_HABITUAL:** Suprema Corte de Justicia de la Provincia de Mendoza - Sala con Competencia Originaria (única instancia en materia procesal administrativa). No hay cámaras ni juzgados de primera instancia en lo contencioso administrativo: la SCJ Mendoza es el único tribunal con competencia originaria y exclusiva en materia procesal administrativa (art. 1 Ley 3918, art. 144 inc. 5 Constitución Mendoza).

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo Mendoza. Ej: "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, habilitaciones municipales, contratación pública provincial".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos provinciales o municipales ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Salud Mendoza, DGE, EMOP, Municipalidad de Godoy Cruz".]

---

## Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Mendoza: procedimiento administrativo ante la Administración provincial y municipal (Ley 9003, que derogó la Ley 3909), recursos administrativos en sede provincial, acción procesal administrativa ante la Suprema Corte de Justicia (Ley 3918), responsabilidad del Estado provincial, empleo público provincial y contratación pública provincial.

**Particularidad estructural central - única instancia en la SCJ Mendoza:** a diferencia de PBA, Córdoba y Santa Fe, en Mendoza no existe un fuero contencioso administrativo de primera instancia separado. La **Suprema Corte de Justicia de Mendoza (SCJ)** es el único tribunal con competencia originaria y exclusiva para conocer en las acciones procesales administrativas (art. 1 Ley 3918, art. 144 inc. 5 Constitución Mendoza). La SCJ actúa por salas: en materia procesal administrativa lo hace la Sala con Competencia Originaria (integrada por los miembros de la SCJ con turnos rotativos). No hay apelación ordinaria de la sentencia definitiva.

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Mendoza (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal mendocina, aplica este perfil. No transpolar plazos ni institutos.

**Tercer nivel - organismos municipales:** los actos de los municipios mendocinos son impugnables ante la SCJ por la vía de la Ley 3918, previo agotamiento de la vía administrativa municipal. El art. 8 Ley 3918 exige agotar el control administrativo de legitimidad que corresponde al PE cuando se trata de entidades desconcentradas, descentralizadas, no estatales o privadas. Para actos directamente emanados del Intendente o del Concejo Deliberante: verificar si hay recurso obligatorio ante el propio municipio y si cabe recurso de alzada ante el PE provincial antes de ocurrir a la SCJ. Verificar jurisprudencia de la SCJ sobre el punto.

---

## Normativa de procedimiento administrativo provincial

### Ley de procedimiento administrativo Mendoza

- **Norma principal vigente:** Ley 9003 (Ley de Procedimiento Administrativo de la Provincia de Mendoza), sancionada el 19/09/2017, vigente a partir de los 30 días hábiles de su publicación (art. 188). **Derogó expresamente la Ley 3909** (art. 191). Mantiene la numeración de artículos de la Ley 3909 para facilitar la continuidad jurisprudencial (los artículos de procedimiento y recursos tienen la misma numeración en ambas leyes).
- **Ámbito:** rige la actividad administrativa de todos los órganos y entes del Estado provincial, y también la actividad administrativa que por atribución legal desarrollen sujetos no estatales (art. 1 Ley 9003). Municipios: pueden adaptar las disposiciones procedimentales de la Ley 9003 (art. 190).
- **Texto vigente:** consultar portal oficial de Mendoza: https://www.mendoza.gov.ar o el portal del Poder Judicial de Mendoza: https://wwwjuri.jus.mendoza.gov.ar
- **Articulado clave:** art. 177 (recurso de revocatoria), arts. 181-182 (recurso jerárquico), arts. 183-184 (recurso de alzada), art. 185 (silencio), art. 162 (denegatoria tácita).

```
[VERIFICAR VIGENCIA: Ley 9003 LPA Mendoza (derogó la Ley 3909) - consultar texto actualizado en https://www.mendoza.gov.ar - verificar modificaciones posteriores a mayo 2026]
```

### Régimen de silencio administrativo Mendoza

- **Regla general:** silencio negativo (denegatoria tácita). La Ley 9003 (art. 162) y la Ley 3918 (art. 6) regulan la denegatoria tácita: hay denegación tácita cuando formulada una petición no se resuelve dentro de los 60 días corridos de estar el expediente en estado de ser resuelto, o cuando no se dictan providencias de trámite en los plazos correspondientes y transcurren 60 días corridos (art. 6 Ley 3918).
- **Sin reforma análoga al Dec 971/2024 nacional:** Mendoza no adoptó el régimen de silencio positivo de la Ley 27.742 nacional. El silencio positivo aplica solo ante la Administración nacional. No transpolar ese régimen al Estado provincial mendocino.
- **Pronto despacho:** ante el silencio del organismo, el interesado debe pedir pronto despacho antes de articular el recurso siguiente (Ley 9003 art. 185 y praxis de la SCJ).

```
[VERIFICAR SILENCIO MENDOZA: Ley 9003 art. 162 / Ley 3918 art. 6 - denegación tácita a los 60 días corridos de estar el expediente en estado de resolver - pronto despacho previo antes del siguiente recurso]
```

### Elementos esenciales del acto administrativo Mendoza

La Ley 9003 regula los elementos esenciales del acto administrativo con estructura paralela al art. 7 LNPA federal. El art. 45 Ley 9003 enumera los actos que deben motivarse:
- los que decidan sobre intereses jurídicamente protegidos o procedimientos de contratación
- los que resuelvan denuncias, reclamos o recursos
- los que modifiquen o extingan actos que favorezcan a particulares

Elementos generales: competencia, causa, objeto, procedimiento, motivación, finalidad.

**Vicios del acto:** la Ley 9003 regula nulidades absolutas y relativas con estructura análoga al régimen federal. Verificar articulado específico.

### Recursos administrativos Mendoza (Ley 9003)

**Recurso de revocatoria (art. 177 Ley 9003):**
- Plazo: 10 días hábiles administrativos desde la notificación del acto
- Ante: el mismo órgano que dictó el acto
- Se resuelve sin sustanciación (salvo medidas para mejor proveer) dentro de los 10 días de interpuesto

**Recurso jerárquico (arts. 181-182 Ley 9003):**
- Procede cuando el recurrente no considera satisfecho su derecho luego de la revocatoria
- Se reproduce por vía de apelación ante el superior jerárquico del órgano que resolvió el primero, recorriendo sucesivamente todos los grados de la línea jerárquica hasta llegar al Gobernador o a la autoridad superior del organismo
- La decisión del Gobernador o autoridad superior causa estado (agota la vía)
- **Plazo: 15 días hábiles administrativos** desde la notificación de la resolución que resuelve la revocatoria, o desde el vencimiento del plazo para resolver si operó el silencio (art. 181 Ley 9003, misma numeración que la Ley 3909 derogada)

**Recurso de alzada (arts. 183-184 Ley 9003):**
- Procede contra las decisiones definitivas de las entidades descentralizadas que causen estado dentro de las mismas
- Ante: el Poder Ejecutivo (Gobernador), cuya decisión cierra la instancia administrativa
- El recurso de alzada es **obligatorio** (art. 184 Ley 9003) y se presenta directamente ante el PE
- El art. 8 Ley 3918 exige que se haya agotado el control de legitimidad que corresponde al PE antes de ocurrir a la SCJ cuando se trata de entidades descentralizadas o no estatales

**Cadena recursiva:**
La cadena típica en Mendoza es: **revocatoria → jerárquico** (recorriendo los grados de la línea jerárquica hasta el Gobernador). Para entes descentralizados: revocatoria ante el ente → alzada obligatoria ante el PE. La decisión del Gobernador o del PE en la alzada cierra la instancia administrativa y habilita la acción ante la SCJ.

**Sin reforma análoga al Decreto 695/2024 nacional:** Mendoza no duplicó los plazos de recursos administrativos. El plazo de la Ley 9003 para la revocatoria es de 10 días hábiles administrativos. No aplicar los plazos federales reformados.

```
[ALERTA PLAZO FATAL: recurso de revocatoria - Ley 9003 art. 177 - 10 días hábiles administrativos desde notificación del acto - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico - Ley 9003 art. 181 - 15 días hábiles administrativos desde notificación de la resolución de la revocatoria o desde el silencio - ante el superior jerárquico / Gobernador según el grado - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de alzada - Ley 9003 arts. 183-184 - ante el PE - plazo: verificar articulado - obligatorio para entes descentralizados antes de la acción ante la SCJ - vencimiento: calcular]
```

### Agotamiento de la vía administrativa Mendoza

- **Regla general:** es requisito previo a la acción procesal administrativa ante la SCJ. El acto debe ser "definitivo y causar estado": decisión definitiva (resuelve el fondo o impide la continuación del reclamo) dictada por la más alta autoridad competente una vez agotados todos los medios de impugnación (art. 5 Ley 3918).
- **Reclamación administrativa previa:** los hechos administrativos no generan directamente la acción; siempre es necesaria la reclamación administrativa para obtener la decisión impugnable (art. 7 Ley 3918).
- **Entes descentralizados y no estatales:** el art. 8 Ley 3918 exige que se hayan agotado los procedimientos tendientes a hacer efectivo el control de legitimidad del PE (recurso de alzada obligatorio) antes de ocurrir a la SCJ. Este es un punto de alta frecuencia de inadmisibilidad.
- **Límite de pretensiones (art. 11 Ley 3918):** las acciones procesales deben limitarse a las cuestiones que fueron debatidas previamente en las reclamaciones o recursos administrativos. Al igual que en Santa Fe, este límite es crítico.
- **Procurador General:** interviene cuando hay conflictos de competencia entre la SCJ y tribunales ordinarios (art. 12 Ley 3918) y en otras instancias previstas por la normativa.

```
[VERIFICAR AGOTAMIENTO DE VÍA MENDOZA: Ley 9003 arts. 177-184 + Ley 3918 arts. 5, 7 y 8 - verificar cadena recursiva completa - para entes descentralizados: alzada obligatoria ante el PE - límite de pretensiones art. 11 Ley 3918]
```

### Tabla unificada de plazos - sede administrativa

| Recurso / instituto | Plazo | Tipo de días | Norma |
|---------------------|-------|--------------|-------|
| Revocatoria | 10 días | Hábiles administrativos | Ley 9003 art. 177 |
| Jerárquico | 15 días | Hábiles administrativos | Ley 9003 art. 181 |
| Alzada (entes descentralizados) | A verificar en arts. 183-184 | Hábiles administrativos | Ley 9003 arts. 183-184 |
| Denegación tácita | 60 días corridos sin resolver | Corridos | Ley 9003 art. 162 / Ley 3918 art. 6 |
| Acción ante la SCJ | 30 días corridos | Corridos | Ley 3918 art. 20 |
| Prescripción - acto anulable | 2 años | - | Ley 3918 art. 19 |
| Prescripción - acto nulo | 5 años | - | Ley 3918 art. 19 |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial. El plazo de la acción ante la SCJ es en días **corridos**: no descuenta fines de semana ni feriados.

---

## Control judicial contencioso administrativo

### Código Procesal Administrativo Mendoza

- **Norma:** Ley 3918 (Código Procesal Administrativo de la Provincia de Mendoza), sancionada el 07/08/1973, y modificatorias
- **Texto vigente:** https://wwwjuri.jus.mendoza.gov.ar/legislacion/ley003918.php y SAIJ. Verificar modificaciones posteriores a mayo 2026.
- **Base constitucional:** art. 144 inc. 5 Constitución Mendoza (la SCJ decide las causas contencioso-administrativas en única instancia, previa denegación expresa o tácita de la autoridad administrativa competente) + art. 128 inc. 20 (es atribución del PE conocer y resolver los asuntos contencioso-administrativos antes de que lleguen a la SCJ).
- **Subsidiariedad:** el Código Procesal Civil de Mendoza se aplica supletoriamente (art. 17 Ley 3918).

### Plazo para interponer la acción procesal administrativa

**Este es el dato más crítico del perfil. El plazo mendocino es el más breve de los cinco sistemas y además se cuenta en días corridos.**

- **Plazo:** 30 días **corridos** desde el día siguiente al de la notificación de la decisión administrativa, o desde el día siguiente al del vencimiento de los 60 días de denegación tácita (art. 20 Ley 3918)
- **Cómputo:** **días corridos** (no hábiles judiciales). Esta es la diferencia más relevante: en PBA son días hábiles judiciales, en Córdoba son días hábiles judiciales, y en Mendoza son días **corridos**.
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa
- **¿Declarable de oficio?:** sí; la SCJ examina la admisión formal del recurso antes de dar traslado (art. 38 Ley 3918 y modificatorias en trámite legislativo al momento de este perfil)
- **Acción de lesividad (art. 21 Ley 3918):** se interpone dentro del plazo de prescripción

```
[ALERTA PLAZO FATAL: art. 20 Ley 3918 APA Mendoza - 30 días CORRIDOS - desde notificación de la decisión que agota la vía - PLAZO EN DÍAS CORRIDOS, NO HÁBILES - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes:**
- Federal: 180 días hábiles judiciales (actos post-9-jul-2024)
- PBA: 90 días hábiles judiciales
- Córdoba: 30 días hábiles judiciales
- Santa Fe: 30 días (verificar naturaleza)
- **Mendoza: 30 días corridos** - el más breve en términos reales porque no descuenta fines de semana ni feriados

Nunca aplicar plazos de otros regímenes a la acción procesal administrativa mendocina.

### Tribunal competente

**Suprema Corte de Justicia de Mendoza - Sala con Competencia Originaria:**
- Competencia: originaria, exclusiva y en única instancia para todas las acciones procesales administrativas (art. 1 Ley 3918, art. 144 inc. 5 Constitución Mendoza)
- Estructura: la SCJ actúa por salas; en materia procesal administrativa lo hace la Sala con Competencia Originaria, integrada por miembros de la SCJ con rotación
- Radicación: ciudad de Mendoza (capital provincial)
- **No hay primera instancia separada:** a diferencia de PBA, Córdoba y Santa Fe, no existen juzgados ni cámaras de primera instancia en lo contencioso administrativo. La SCJ es el único tribunal, en única instancia ordinaria.

**Recursos contra la sentencia definitiva de la SCJ:**
- Recurso extraordinario federal ante la CSJN (art. 14 Ley 48): única vía de revisión ordinaria de las sentencias definitivas de la SCJ en materia procesal administrativa
- No existe recurso de casación ni inconstitucionalidad local adicional, dado que la SCJ ya es el tribunal superior de la provincia

**Fiscalía de Estado de Mendoza:**
- Representa al Estado provincial en juicio (art. 155 Constitución Mendoza y Ley Orgánica de la Fiscalía de Estado)
- Es parte necesaria en las acciones procesales administrativas
- Las notificaciones a la Fiscalía de Estado se hacen en su despacho oficial. En la práctica de la SCJ, la Fiscalía de Estado tiene rol activo en el control de legalidad del proceso.

### Actos impugnables (Ley 3918)

Procede la acción contra cualquier violación de un derecho subjetivo o interés legítimo regido por norma administrativa (art. 1 Ley 3918). También son impugnables (art. 2):
- Actos dictados en ejercicio de facultades discrecionales, cuando la impugnación se funde en razones de ilegitimidad (concepto amplio: vicios en competencia, objeto, voluntad, forma, desviación, abuso o exceso de poder, arbitrariedad, violación de principios generales del derecho)
- Actos separables de los contratos en la actividad administrativa
- Actos que resuelven reclamos por retribuciones, jubilaciones o pensiones de agentes estatales (excepto los regidos por el derecho del trabajo)

**No corresponden a esta vía (art. 4 Ley 3918):**
- Juicios ejecutivos, de apremio, interdictos y acciones posesorias
- Juicios de expropiación
- Los que deban resolverse aplicando exclusivamente normas de derecho privado o del trabajo

### Pretensiones admisibles (art. 18 Ley 3918)

- Anulación total o parcial de la disposición administrativa impugnada
- Restablecimiento o reconocimiento del derecho vulnerado, desconocido o incumplido
- Resarcimiento de los perjuicios sufridos

Las tres pretensiones pueden acumularse en una misma acción. El resarcimiento es una pretensión admisible que puede plantearse junto con la anulatoria.

**Límite de pretensiones (art. 11 Ley 3918):** las acciones procesales deben limitarse a las cuestiones debatidas previamente en la reclamación administrativa. Lo no planteado en sede administrativa no puede introducirse en la acción ante la SCJ.

### Prescripción de la acción (art. 19 Ley 3918)

- Acto anulable: prescripción de 2 años
- Acto nulo: prescripción de 5 años

Estos plazos son distintos del plazo de caducidad del art. 20 (30 días corridos). Si vence el plazo de caducidad del art. 20 antes de que prescriba la acción, la acción caduca de todos modos.

### Suspensión de la ejecución del acto (medida cautelar) (arts. 22-27 Ley 3918)

- **Requisitos:** que "prima facie" la disposición sea nula o pueda producir un daño irreparable si apareciere como anulable (art. 23)
- **Trámite:** previa vista de 2 días a la demandada; la SCJ resuelve en 3 días (art. 22)
- **Contracautela:** a criterio de la SCJ (art. 25)
- **Suspensión antes de interponer la acción:** si la suspensión se solicita antes de interponer la acción, **caduca automáticamente si la acción no se deduce en el plazo legal** (art. 27). Riesgo crítico: obtener la suspensión y luego perder la cautelar por no interponer la acción en el plazo del art. 20.
- **Levantamiento por interés público:** la demandada puede pedir el levantamiento alegando grave daño al interés público; el tribunal puede dejarlo sin efecto, declarando a cargo del peticionante la responsabilidad por los perjuicios si prospera la demanda (art. 26)
- **No procede la suspensión (art. 24):** clausura o demolición por razones de seguridad/moralidad/higiene (con dictamen de órgano competente); cesantías o exoneraciones de agentes estatales. Este último punto es especialmente relevante en empleo público.

```
[ALERTA CAUTELAR MENDOZA: suspensión solicitada antes de la acción caduca automáticamente si la acción no se interpone en 30 días corridos - art. 27 Ley 3918 - verificar plazo antes de pedir la suspensión]
[ATENCIÓN: no procede la suspensión en cesantías/exoneraciones - art. 24 inc. b Ley 3918]
```

### Amparo Mendoza

- **Norma:** art. 43 CN + Ley 2589 (Ley de Amparo de Mendoza) y modificatorias [VERIFICAR VIGENCIA: Ley 2589 y sus modificatorias]
- **Plazo:** 15 días desde que el afectado conoció o pudo conocer el acto lesivo (art. 2 Ley 2589) [A VERIFICAR: confirmar en el texto actualizado de la Ley 2589 antes de computar]
- **Subsidiariedad del amparo frente a la acción procesal administrativa:** la SCJ Mendoza tiene jurisprudencia consolidada que considera la acción procesal administrativa (con posibilidad de solicitar la suspensión del acto, art. 22 Ley 3918) como vía ordinaria idónea que desplaza el amparo en materia administrativa. El amparo procede solo cuando la vía del art. 3918 no ofrece la misma efectividad por la urgencia o la evidencia de la ilegalidad manifiesta.
- **Competencia:** los juzgados civiles de primera instancia de Mendoza tienen competencia en amparo; cuando la materia es contencioso administrativa, la jurisprudencia tiende a remitir a la SCJ. Verificar jurisprudencia vigente antes de radicar.
- **Amparo de pronto despacho:** ante la mora de la Administración. Verificar regulación en la Ley 2589.

```
[VERIFICAR AMPARO MENDOZA: Ley 2589 - subsidiariedad frente a la APA de la Ley 3918 - competencia - plazo de caducidad - consultar jurisprudencia SCJ Mendoza vigente]
```

---

## Normativa de referencia Mendoza

### Responsabilidad del Estado provincial

- **Sin ley propia equivalente a Ley 26.944 nacional:** Mendoza no sancionó una ley de responsabilidad del Estado equivalente a la Ley 26.944. Ésta no aplica a demandas contra el Estado provincial mendocino.
- **Régimen aplicable:** principios generales del derecho administrativo y jurisprudencia de la SCJ Mendoza. La pretensión resarcitoria puede acumularse a la anulatoria en la misma acción procesal administrativa (art. 18 Ley 3918).
- **No aplicar CCCN:** no invocar arts. 1757, 1741 ni otros del CCCN en demandas contra el Estado provincial sin verificar criterio de la SCJ Mendoza.
- **Prescripción de la acción resarcitoria:** la SCJ Mendoza ha elaborado criterios propios; verificar jurisprudencia de la Sala con Competencia Originaria antes de plantear la pretensión.
- **Lesividad (art. 3 Ley 3918):** el Estado puede impugnar sus propios actos irrevocables que sean lesivos al interés público, previo acto administrativo que los declare lesivos. El plazo es el de prescripción (art. 21 Ley 3918).

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD MENDOZA: sin ley propia - principios generales + jurisprudencia SCJ Mendoza Sala Competencia Originaria - acumular pretensión resarcitoria a la anulatoria (art. 18 Ley 3918)]
```

### Empleo público Mendoza

- **Estatuto general:** Ley 5892 (Estatuto del Empleado Público de la Provincia de Mendoza) y modificatorias. Regula las relaciones laborales del personal dependiente del Poder Ejecutivo provincial.
- **Escalafón:** verificar decreto de escalafón general vigente. Los distintos agrupamientos pueden tener escalafones diferenciados.
- **Régimen disciplinario:** Ley 5892 + reglamentación. Sumario administrativo con garantías de debido proceso. Verificar si el organismo tiene reglamento de sumarios propio.
- **Suspensión cautelar no procede en cesantías/exoneraciones (art. 24 inc. b Ley 3918):** punto crítico en litigios de empleo público. El actor no puede obtener la suspensión del acto de cesantía o exoneración mientras tramita la acción procesal administrativa.
- **Actos sobre retribuciones, jubilaciones y pensiones (art. 2 inc. c Ley 3918):** son expresamente impugnables ante la SCJ por la vía de la Ley 3918, salvo los regidos por el derecho del trabajo.
- **Estatutos sectoriales principales:**
  - Docentes: DGE (Dirección General de Escuelas); verificar estatuto docente provincial (Ley 4934 y modificatorias)
  - Policía: verificar Ley Orgánica de la Policía de Mendoza (Ley 6721 y modificatorias)
  - Personal de salud: verificar norma sectorial vigente
  - Personal municipal: verificar si el municipio tiene estatuto propio o remite a la Ley 5892 supletoriamente
  - [COMPLETAR: otros estatutos sectoriales según las áreas de práctica habituales]

```
[VERIFICAR ESTATUTO APLICABLE MENDOZA: Ley 5892 general o estatuto sectorial según el organismo - para docentes: Ley 4934 / policial: Ley 6721 - ATENCIÓN: suspensión cautelar no procede en cesantías/exoneraciones (art. 24 inc. b Ley 3918)]
```

### Contratación pública Mendoza

- **Norma general:** Ley 8706 (Ley de Administración Financiera y Control de la Administración General del Estado de Mendoza) y modificatorias. Regula el sistema de contrataciones del Estado provincial.
- **Reglamento:** verificar decretos reglamentarios vigentes. Los montos y procedimientos se actualizan por resolución del organismo rector.
- **Organismo rector:** verificar denominación actual del organismo de compras/contrataciones (históricamente bajo la órbita de la Contaduría General de la Provincia).
- **Plataforma de compras:** verificar sistema electrónico de contrataciones vigente en Mendoza.
- **Obra pública provincial:** verificar ley de obras públicas provincial vigente. La Ley 13.064 (obra pública nacional) no aplica supletoriamente salvo remisión contractual expresa.
- **Impugnación de licitaciones:** verificar plazos y procedimientos en la Ley 8706 y el pliego correspondiente.

```
[VERIFICAR VIGENCIA: Ley 8706 Mendoza (contrataciones) y decretos reglamentarios - los montos de licitación pública/privada/contratación directa se actualizan - verificar antes de encuadrar el procedimiento]
```

### Organismos de control Mendoza

**Tribunal de Cuentas de Mendoza:**
- Control externo del Estado provincial. Tiene función jurisdiccional. Sus resoluciones definitivas son impugnables ante la SCJ por la vía de la Ley 3918.

**Fiscalía de Estado de Mendoza:**
- Representante legal del Estado provincial en juicio (art. 155 Constitución Mendoza). Es parte necesaria en las acciones procesales administrativas ante la SCJ.
- Las notificaciones a la Fiscalía de Estado se hacen en su despacho oficial.
- Interviene con vista en las instancias previstas por la Ley 9003 (recursos jerárquicos resueltos por el PE) y en el proceso judicial.

**Procurador General de Mendoza:**
- Resuelve conflictos de competencia entre la SCJ y los tribunales ordinarios en materia procesal administrativa (art. 12 Ley 3918).

**Defensor del Pueblo de Mendoza:**
- Art. 124 Constitución Mendoza. Legitimación para actuar en defensa de derechos colectivos.

---

## Alerta normativa - normas de vigencia variable

*Última verificación de esta sección: mayo 2026. Actualizar cuando cambie alguna de las normas listadas.*

### Plazo de la acción procesal administrativa Mendoza

```
[ALERTA PLAZO FATAL: art. 20 Ley 3918 APA Mendoza - 30 días CORRIDOS - desde notificación de la decisión que agota la vía - DÍAS CORRIDOS (no hábiles judiciales, no descuenta fines de semana ni feriados) - vencimiento: calcular]
```

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública (Ley 8706):** los umbrales para licitación pública, privada y contratación directa se actualizan por decreto o resolución. Verificar antes de encuadrar el procedimiento.
- **Escala salarial empleo público Mendoza:** se modifica por paritarias. No asumir montos sin verificar la resolución de homologación vigente.
- **Modificaciones a la Ley 3918:** al momento de este perfil, había proyectos legislativos en trámite para modificar el art. 38 de la Ley 3918 (admisión formal de la acción). Verificar si fueron sancionados antes de aplicar ese artículo.
- **Habilitaciones municipales:** el régimen varía por municipio (Mendoza capital, Godoy Cruz, Las Heras, Maipú, Luján de Cuyo, Guaymallén tienen ordenanzas propias). Verificar norma vigente al momento del acto.

```
[VERIFICAR VIGENCIA: norma Mendoza - [materia] - consultar Boletín Oficial Mendoza (https://www.mendoza.gov.ar/boletin-oficial) antes de aplicar]
```

## Responsables procesales por instancia

| Instancia | Representante del Estado | Observación |
|-----------|--------------------------|-------------|
| SCJ Mendoza - Sala Competencia Originaria (única instancia) | Fiscalía de Estado de Mendoza | Es parte necesaria; las notificaciones se hacen en su despacho oficial |
| Recursos jerárquicos ante el PE (sede administrativa) | Fiscalía de Estado (vista preceptiva en los supuestos de la Ley 9003) | La omisión de la vista puede configurar vicio de procedimiento |
| Conflictos de competencia | Procurador General de Mendoza | Art. 12 Ley 3918 |
| Recursos ante la CSJN (REF) | Fiscalía de Estado de Mendoza | Única instancia de revisión ordinaria post-SCJ |

**Nota:** la SCJ Mendoza actúa en materia procesal administrativa por la Sala con Competencia Originaria (integración rotativa de miembros del tribunal). No existen salas fijas; verificar la composición al momento de la presentación.

```
[VERIFICAR REPRESENTACIÓN PROCESAL MENDOZA: Fiscalía de Estado como parte necesaria en la acción procesal administrativa - notificaciones en despacho oficial - Procurador General en conflictos de competencia (art. 12 Ley 3918)]
```

---

## Fuentes primarias

- **Boletín Oficial Mendoza:** https://www.mendoza.gov.ar/boletin-oficial
- **Portal jurídico Mendoza (leyes):** https://wwwjuri.jus.mendoza.gov.ar
- **SCJ Mendoza (jurisprudencia):** https://www2.jus.mendoza.gov.ar
- **Fiscalía de Estado Mendoza:** https://www.mendoza.gov.ar (sección Fiscalía de Estado)
- **Tribunal de Cuentas Mendoza:** verificar URL vigente
- **Portal de contrataciones Mendoza:** verificar URL vigente

---

## Reglas de citación - administrativo Mendoza

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para la SCJ Mendoza en materia procesal administrativa:

**Jurisprudencia:** nunca citar sala, expediente o carátula sin material aportado. La SCJ Mendoza actúa por salas rotativas en materia procesal administrativa; verificar la sala actuante. Usar:
```
[INSERTAR FALLO VERIFICADO: SCJ Mendoza - Sala Competencia Originaria / Sala I / Sala II - doctrina requerida]
```

**Actos administrativos Mendoza:** no asumir el contenido de resoluciones, dictámenes de la Fiscalía de Estado o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos APA Mendoza:** no transpolar plazos del régimen federal ni de otras provincias. Usar:
```
[ALERTA PLAZO FATAL: art. 20 Ley 3918 APA Mendoza - 30 días CORRIDOS desde notificación - vencimiento: calcular]
```

---

## Lógica de análisis por institución

### Checklist: acto administrativo provincial/municipal

Aplicar Ley 9003 LPA Mendoza. Elementos: competencia, causa, objeto, procedimiento, motivación, finalidad.

1. ¿Qué acto se impugna? ¿Es del Estado provincial (órgano centralizado, ente descentralizado) o de un municipio? ¿Es definitivo y causa estado?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo de 30 días corridos del art. 20 Ley 3918)
3. ¿Qué elementos del acto se cuestionan? ¿Hay vicio de ilegitimidad?
4. ¿Hay expediente administrativo? ¿El abogado lo tiene o requiere vista?
5. ¿Se interpuso recurso de revocatoria en plazo (10 días hábiles)? ¿Se agotó la cadena recursiva completa? Para entes descentralizados: ¿se interpuso la alzada obligatoria ante el PE (art. 8 Ley 3918)?
6. ¿Las pretensiones que se quieren plantear en la acción judicial coinciden con las articuladas en sede administrativa? (art. 11 Ley 3918 - límite crítico)
7. ¿Intervino la Fiscalía de Estado cuando era preceptivo?

### Checklist: recursos administrativos Mendoza

Aplicar Ley 9003 arts. 177-184. En cada recurso verificar:

1. Revocatoria: 10 días hábiles administrativos desde notificación (art. 177).
2. Jerárquico: 15 días hábiles administrativos desde la notificación de la resolución de la revocatoria o desde el silencio (art. 181).
3. Para entes descentralizados: alzada obligatoria ante el PE (art. 184) antes de la acción ante la SCJ. Si no se interpone, la acción es inadmisible (art. 8 Ley 3918).
4. Si la decisión emana directamente del Gobernador o máxima autoridad: verificar si hay recurso previo o si esa decisión agota directamente la vía.
5. Articular en sede administrativa todas las pretensiones que se quieran plantear después.

```
[ALERTA PLAZO FATAL: revocatoria - Ley 9003 art. 177 - 10 días hábiles administrativos desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: jerárquico - Ley 9003 art. 181 - 15 días hábiles administrativos desde resolución de la revocatoria o silencio - vencimiento: calcular]
```

### Checklist: agotamiento de la vía y acción procesal administrativa

1. Verificar si la decisión es definitiva y causa estado (art. 5 Ley 3918).
2. Para entes descentralizados: verificar alzada obligatoria ante el PE (art. 8 Ley 3918). Punto de alta frecuencia de inadmisibilidad.
3. Verificar que el objeto de la acción no supere lo planteado en sede administrativa (art. 11 Ley 3918).
4. Calcular el plazo de **30 días corridos** desde la notificación de la decisión que agota la vía. Incluir fines de semana y feriados en el cómputo.
5. Si se planea pedir la suspensión antes de interponer la acción: tener presente que la suspensión caducará automáticamente si no se deduce la acción en plazo (art. 27 Ley 3918).

### Checklist: responsabilidad del Estado Mendoza

1. No aplicar Ley 26.944 ni CCCN sin verificar criterio de la SCJ Mendoza; aportar fallo de la Sala con Competencia Originaria.
2. La pretensión resarcitoria puede acumularse a la anulatoria en la misma acción (art. 18 Ley 3918): incluirla en la misma presentación.
3. Verificar prescripción: 2 años para acto anulable / 5 años para acto nulo (art. 19 Ley 3918).

### Checklist: empleo público Mendoza

1. Identificar estatuto aplicable: Ley 5892 (general) o sectorial (Ley 4934 docentes / Ley 6721 policial / municipal).
2. Situación de revista del agente.
3. Si hubo sumario con garantías de debido proceso.
4. Si la sanción es cesantía/exoneración: **la suspensión cautelar no procede** (art. 24 inc. b Ley 3918). Informar al cliente antes de iniciar la acción.
5. Si la pretensión involucra retribuciones, jubilaciones o pensiones: impugnable ante la SCJ por Ley 3918 (art. 2 inc. c) salvo relación regida por derecho del trabajo.

### Checklist: contratación pública Mendoza

1. Verificar monto vigente para encuadrar el tipo de procedimiento según Ley 8706 y resolución del organismo rector.
2. Verificar plazos de impugnación de pliegos y preadjudicación.
3. Para obra pública: verificar ley provincial; la Ley 13.064 nacional no aplica al Estado provincial salvo remisión contractual expresa.

---

## Instrucciones operativas específicas - Mendoza

### Alerta crítica - plazo de la acción procesal administrativa Mendoza

**Este es el primer paso en toda consulta que involucre una acción judicial contra el Estado provincial o municipal mendocino. El plazo de 30 días corridos es el más breve del sistema y el más peligroso porque no descuenta fines de semana ni feriados.**

El plazo del art. 20 Ley 3918 es de caducidad, no de prescripción:
- Se cuenta en **días corridos** (fines de semana y feriados incluidos)
- No se suspende ni interrumpe salvo norma expresa
- Vencido el plazo, la acción caduca; la SCJ lo verifica de oficio en la admisión formal
- Si se solicita suspensión del acto antes de la acción y luego no se interpone la acción en plazo, la suspensión caduca automáticamente (art. 27 Ley 3918)

**Plazo:** 30 días **corridos** desde el día siguiente al de la notificación de la decisión que agota la vía (o desde el día siguiente al del vencimiento de los 60 días de denegación tácita).

Antes de analizar cualquier otra cuestión, emitir:
```
[ALERTA PLAZO FATAL: art. 20 Ley 3918 APA Mendoza - 30 días CORRIDOS (incluye fines de semana y feriados) - desde notificación de la decisión que agota la vía - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes (no transpolar):**

| Régimen | Plazo | Tipo | Norma |
|---------|-------|------|-------|
| **Mendoza** | **30 días corridos** | Corridos | Ley 3918 art. 20 |
| Córdoba | 30 días | Hábiles judiciales | Ley 7182 art. 8 |
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

**Mendoza es el más breve en términos reales** porque los 30 días son corridos: fines de semana y feriados no se descuentan.

**Alerta adicional:** verificar que el ente emisor del acto requería alzada obligatoria ante el PE antes de la acción judicial (entes descentralizados, art. 8 Ley 3918). Si no se agotó esa vía, la acción es inadmisible.

---

- Identificar si el acto es del Estado provincial mendocino, de un municipio mendocino o de un organismo federal antes de aplicar este perfil o el nacional.
- La SCJ Mendoza es el único tribunal competente en materia procesal administrativa (única instancia ordinaria). No hay primera instancia separada.
- Verificar agotamiento de la vía (Ley 9003: revocatoria → jerárquico → alzada si es ente descentralizado) antes de analizar la acción.
- Articular en sede administrativa todas las pretensiones; las no planteadas allí no pueden introducirse en la acción ante la SCJ (art. 11 Ley 3918).
- El plazo es de 30 días corridos. Calcular con fines de semana y feriados incluidos.
- En empleo público: la suspensión del acto de cesantía o exoneración no procede (art. 24 inc. b). Informar al cliente antes de iniciar la acción.
- Acumular la pretensión resarcitoria a la anulatoria en la misma acción (art. 18 Ley 3918).
- En responsabilidad del Estado: no aplicar Ley 26.944 ni CCCN sin verificar criterio de la SCJ.
- Verificar intervención preceptiva de la Fiscalía de Estado (recursos ante el PE, proceso judicial).
- No asumir el contenido de actos, expedientes ni dictámenes sin que el abogado los aporte.
- Todo escrito ante la SCJ Mendoza en materia procesal administrativa cierra con "Estado del escrito" estándar más: estado del agotamiento de la vía (incluyendo alzada si corresponde), **plazo art. 20 Ley 3918 (verificado en días corridos / pendiente de verificar / vencido)**, verificación de coincidencia entre pretensiones judiciales y planteadas en sede administrativa (art. 11), pretensión resarcitoria acumulada o no, cautela solicitada (verificar art. 24 si es empleo público), intervención de Fiscalía de Estado (sí / no / a verificar).

---

*Última actualización: mayo 2026*
*Normativa base: Ley 9003 LPA Mendoza (derogó Ley 3909), Ley 3918 (Código Procesal Administrativo de Mendoza), Ley 2589 (amparo Mendoza), Ley 5892 (empleo público), Ley 4934 (estatuto docente), Ley 6721 (policía), Ley 8706 (administración financiera y contrataciones), Constitución de Mendoza arts. 128 inc. 20, 144 inc. 5, 155*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
