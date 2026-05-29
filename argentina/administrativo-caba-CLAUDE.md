# Perfil de práctica · Derecho administrativo · CABA

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo y tributario de CABA.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.

---

## Configuración inicial - completar antes de usar

**PROVINCIA:** Ciudad Autónoma de Buenos Aires (CABA)

**FUERO_HABITUAL:** Fuero Contencioso Administrativo y Tributario CABA (CCAyT). Juzgados de Primera Instancia en lo Contencioso Administrativo y Tributario CABA / Cámara de Apelaciones en lo Contencioso Administrativo y Tributario CABA.

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo CABA. Ej: "Responsabilidad del Estado CABA, empleo público GCBA, contratación pública CABA, habilitaciones comerciales, sanciones administrativas GCBA".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos del GCBA ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Salud GCBA, AGC, DGR, SSPLAN".]

---

## Identidad y alcance

Este perfil cubre práctica de derecho administrativo ante el Gobierno de la Ciudad Autónoma de Buenos Aires (GCBA): procedimiento administrativo en sede GCBA, recursos administrativos, control judicial contencioso administrativo y tributario CABA, responsabilidad del Estado CABA, empleo público GCBA y contratación pública CABA.

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en CABA (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA) - ver administrativo-CLAUDE.md. Cuando actúa el GCBA o sus entes, aplica este perfil. La distinción es crítica: CABA tiene régimen propio que difiere sustancialmente del federal en plazos, recursos y estructura de control judicial.

**Distinción crítica - dos cuerpos normativos distintos:**
- **Procedimiento administrativo CABA (en sede administrativa):** Decreto N° 1510/97 (LPA CABA) - t.o. Ley N° 6764/24 (5ta actualización del Digesto Jurídico CABA, B.O. CABA 18/12/2024). Cubre el trámite ante el GCBA antes de agotar la vía.
- **Control judicial contencioso administrativo CABA:** Ley N° 189 CABA (Código Contencioso Administrativo y Tributario - CCAyT). Cubre la acción judicial una vez agotada la vía administrativa.

No confundir el Decreto N° 1510/97 (procedimiento en sede administrativa) con la Ley N° 189 CCAyT (control judicial): son cuerpos legales distintos que cubren etapas distintas del conflicto.

---

## Normativa de procedimiento administrativo provincial

### Ley de procedimiento administrativo CABA

- **Norma principal:** Decreto N° 1510/97 (Ley de Procedimientos Administrativos CABA - LPA CABA)
- **Texto vigente:** t.o. Ley N° 6764/24 (5ta actualización del Digesto Jurídico CABA, B.O. CABA 18/12/2024). Consultar texto en JURISTECA: https://juristeca.jusbaires.gob.ar/compilacion-normativa-juristeca/decreto-1510/
- **Reglamento:** el propio Decreto N° 1510/97 contiene la regulación procedimental; no tiene decreto reglamentario separado equivalente al Decreto N° 1759/72 nacional.
- **Articulado clave:** art. 7 (elementos esenciales del acto), arts. 14-17 (vicios y nulidades), arts. 84 y ss. (recursos), art. 10 (silencio administrativo).

```
[VERIFICAR VIGENCIA: Decreto N° 1510/97 LPA CABA (t.o. Ley N° 6764/24) - consultar JURISTECA para modificaciones posteriores a mayo 2026]
```

### Régimen de silencio administrativo CABA

- **Regla general:** silencio negativo por regla general (art. 10 Decreto N° 1510/97). Vencido el plazo para resolver sin resolución expresa, se tiene por denegado y corre el plazo para recurrir o accionar judicialmente.
- **Silencio positivo:** el Decreto N° 1510/97 no adoptó el régimen de silencio positivo de la Ley N° 27.742 nacional (Decreto N° 971/2024). El silencio positivo del art. 10 LNPA reformado y su reglamentación (Anexo I y II del Decreto N° 971/2024) aplican solo a procedimientos ante la Administración nacional. No transpolar ese régimen al GCBA sin verificar si CABA sancionó normativa equivalente.
- **Plazo subsidiario:** [VERIFICAR: el Decreto N° 1510/97 fija plazos máximos para resolver según el tipo de acto. Verificar artículo aplicable al procedimiento específico.]
- **Denegatoria tácita:** opera vencido el plazo legal para resolver. A partir de ese momento corre el plazo para interponer el recurso correspondiente o accionar judicialmente.

```
[VERIFICAR EFECTO DEL SILENCIO CABA: Decreto N° 1510/97 art. 10 - regla general: silencio negativo - verificar si CABA adoptó norma equivalente al Decreto N° 971/2024 nacional antes de aplicar otro criterio]
```

### Elementos esenciales del acto administrativo CABA

El art. 7 del Decreto N° 1510/97 establece los elementos esenciales del acto administrativo, con estructura paralela al art. 7 LNPA federal:

1. Competencia: atribución del órgano del GCBA para dictar el acto
2. Causa: antecedentes de hecho y de derecho que fundamentan el acto
3. Objeto: cierto, lícito, físicamente posible
4. Procedimiento: cumplimiento de trámites esenciales previos
5. Motivación: expresión concreta de las razones que llevan al dictado del acto
6. Finalidad: adecuada a la causa del acto y al ordenamiento

**Régimen de nulidades CABA:** arts. 14-17 Decreto N° 1510/97, paralelos a los arts. 14-17 LNPA federal. Distingue nulidad absoluta (vicio en elementos esenciales, imprescriptible, declarable de oficio) de nulidad relativa (vicios que admiten saneamiento).

### Recursos administrativos CABA

**Recurso de reconsideración (art. 119 Decreto N° 1510/97):**
- Plazo: 10 días hábiles administrativos GCBA desde la notificación del acto
- Ante: el mismo órgano que dictó el acto
- Efecto: suspende el plazo para interponer el recurso jerárquico
- Resultado: si es denegado o no hay resolución en 30 días hábiles administrativos, el particular puede alzarse en jerárquico

**Recurso jerárquico (arts. 108-119 Decreto N° 1510/97):**
- Plazo: 15 días hábiles administrativos GCBA desde la notificación del acto denegatorio o desde la denegatoria tácita de la reconsideración
- Ante: el superior jerárquico del órgano emisor; sube hasta el Jefe de Gobierno o ministro competente según el caso
- Agota la vía: sí, cuando es resuelto por el ministro o el Jefe de Gobierno

**Recurso de alzada (arts. 120-122 Decreto N° 1510/97):**
- Procede contra actos de entes autárquicos y descentralizados del GCBA
- Ante: el ministerio con tutela sobre el ente
- Opcional en algunos casos: el particular puede prescindir del recurso de alzada y ocurrir directamente al CCAyT

**Queja (art. 71 Decreto N° 1510/97):**
- Por defectos de tramitación o incumplimiento de plazos
- No interrumpe plazos de recursos

**Días hábiles administrativos CABA:** son los días hábiles del GCBA, que pueden diferir del calendario de días hábiles judiciales. Verificar calendario administrativo vigente al momento del acto.

```
[ALERTA PLAZO FATAL: recurso [denominación] - Decreto N° 1510/97 art. [X] - [X] días hábiles administrativos GCBA desde notificación - vencimiento: calcular]
```

### Agotamiento de la vía administrativa CABA

- **Regla general:** el agotamiento de la vía administrativa es requisito previo a la acción judicial ante el CCAyT, salvo excepciones (art. 3 y ss. Ley N° 189 CCAyT).
- **Excepciones:** acto nulo de nulidad absoluta, cuando el agotamiento resulta inútil (jurisprudencia TSJ CABA), vías de hecho del GCBA, cuando el particular es ajeno a la iniciación del procedimiento.
- **Procuración General CABA:** emite dictámenes obligatorios en las materias previstas por el art. 134 Constitución CABA y la ley orgánica de la PG. Verificar si el expediente requirió dictamen de la PG y si fue cumplido; su omisión puede configurar vicio de procedimiento.

```
[VERIFICAR AGOTAMIENTO DE VÍA CABA: Decreto N° 1510/97 + Ley N° 189 CCAyT - verificar si se interpusieron los recursos correspondientes en plazo y si la resolución que agota la vía fue notificada]
```

---

## Control judicial contencioso administrativo

### Código de proceso contencioso administrativo CABA

- **Norma:** Ley N° 189 CABA (Código Contencioso Administrativo y Tributario - CCAyT) y modificatorias
- **Texto vigente:** consultar JURISTECA: https://juristeca.jusbaires.gob.ar/compilacion-normativa-juristeca/ley-189/
- **Subsidiariedad:** el CCAyT es autónomo. Para lo no previsto, remite al Código Procesal Civil y Comercial de la Nación (CPCCN) en forma supletoria según criterio jurisprudencial de la Cámara CCAyT.

### Plazo de caducidad para accionar judicialmente

**Este es el dato más crítico del perfil. Diferencia sustancial con el régimen federal.**

- **Plazo general:** 90 días hábiles judiciales desde que el acto fue ejecutado o debió serlo, o desde que el particular tomó conocimiento fehaciente del acto (art. 7 Ley N° 189 CCAyT)
- **Cómputo:** días hábiles judiciales CABA
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa
- **¿Declarable de oficio?:** sí, según jurisprudencia uniforme de la Cámara CCAyT y TSJ CABA

```
[ALERTA PLAZO FATAL: art. 7 CCAyT (Ley N° 189 CABA) - 90 días hábiles judiciales - desde notificación fehaciente del acto que agota la vía o desde que debió conocerse - vencimiento: calcular]
```

**Diferencia crítica con el régimen federal:** el plazo federal (art. 25 LNPA) es de 180 días hábiles judiciales para actos post-9-jul-2024. El plazo CABA es de 90 días hábiles judiciales. No aplicar el plazo federal a actos del GCBA.

**Supuestos especiales:** el CCAyT puede prever plazos distintos para pretensiones específicas (ej. materia tributaria CABA, habilitaciones, sanciones). La Cámara CCAyT tiene jurisprudencia sobre el inicio del cómputo según el tipo de acto - en particular, cuándo comienza a correr ante actos de ejecución continuada, actos complejos o notificaciones defectuosas. En esos supuestos, el plazo de 90 días hábiles judiciales sigue siendo la regla; lo que varía es el momento de inicio del cómputo. Aportar el fallo aplicable cuando el caso no encuadre en el supuesto estándar de notificación fehaciente de acto definitivo.

```
[INSERTAR FALLO VERIFICADO: Cámara CCAyT / TSJ CABA - doctrina sobre inicio del cómputo del plazo art. 7 en supuesto específico del caso]
```

### Órganos jurisdiccionales

**Primera instancia:**
- **Juzgados:** Juzgados de Primera Instancia en lo Contencioso Administrativo y Tributario CABA
- **Sede:** CABA
- **Competencia por materia:** exclusiva para causas en que el GCBA o sus entes sean parte en materia administrativa y tributaria. Para organismos federales con sede en CABA: fuero contencioso administrativo federal.

**Alzada:**
- **Tribunal:** Cámara de Apelaciones en lo Contencioso Administrativo y Tributario CABA
- **Salas:** tres salas (Sala I, Sala II, Sala III)
- **Jurisprudencia:** acceso vía PJN (pjn.gov.ar) y TSJ CABA (tsjcaba.gov.ar). Verificar sala actuante antes de citar criterio de la Cámara - las tres salas pueden tener criterios distintos en cuestiones no unificadas.

**Tribunal Superior:**
- **Tribunal:** Tribunal Superior de Justicia CABA (TSJ CABA)
- **Recurso de acceso:** recurso de inconstitucionalidad (art. 113 inc. 3 Constitución CABA). Requisitos: cuestión constitucional, agotamiento de instancias ordinarias, resolución definitiva o equiparable.
- **Competencia originaria:** el TSJ CABA tiene competencia originaria en conflictos entre poderes del GCBA y en otras materias específicas de la Constitución CABA. Verificar art. 113 Constitución CABA.

### Pretensiones admisibles (CCAyT)

El CCAyT prevé un catálogo abierto de pretensiones. Las principales:
- Anulación de actos administrativos del GCBA (pretensión anulatoria)
- Reconocimiento o restablecimiento de derechos (pretensión de plena jurisdicción)
- Declarativa de certeza en materia administrativa
- Pretensión prestacional (condena al GCBA a hacer, no hacer o dar)
- Cautelar autónoma

Verificar si la pretensión encuadra en la materia contencioso administrativa del CCAyT antes de radicar en este fuero; algunas materias tienen reglas propias de competencia.

### Medidas cautelares contra el GCBA

- **Régimen:** el CCAyT regula las medidas cautelares contra el GCBA con reglas propias (arts. 177 y ss. CCAyT). No aplica la Ley N° 26.854 nacional (que rige solo contra el Estado nacional).
- **Requisitos:** verosimilitud del derecho + peligro en la demora + no afectación grave del interés público
- **Informe previo del GCBA:** el CCAyT puede requerir informe previo del organismo demandado antes de resolver la cautelar. Verificar práctica actual de la sala actuante.
- **Contracautela:** exigida como regla; puede ser juratoria según el caso y el criterio de la sala.
- **Plazo de vigencia:** sin límite temporal fijo en el CCAyT; la cautelar subsiste hasta la sentencia salvo levantamiento o modificación.

```
[VERIFICAR RÉGIMEN CAUTELAR CABA: CCAyT arts. 177 y ss. - no aplica Ley N° 26.854 nacional - verificar criterio de la sala actuante sobre informe previo y contracautela]
```

### Amparo CABA

- **Norma:** art. 14 Constitución CABA + Ley N° 2145 CABA (amparo)
- **Plazo:** 90 días desde que el afectado conoció o pudo conocer el acto lesivo (art. 6 Ley N° 2145 CABA). La norma no califica si son días hábiles o corridos; la jurisprudencia de la Cámara CCAyT no tiene regla uniforme sobre el punto. No computar como "90 días hábiles judiciales" sin verificar el criterio de la sala actuante al momento del caso concreto.
- **Legitimación activa:** amplia; incluye legitimación colectiva
- **Subsidiariedad:** procede cuando no existe otro medio judicial más idóneo; el CCAyT tiene acción ordinaria más amplia
- **Habeas data:** integrado en el régimen de la Ley N° 2145 CABA
- **Competencia:** Juzgados CCAyT en primera instancia; Cámara CCAyT en alzada

```
[ALERTA PLAZO FATAL - AMPARO CABA: art. 6 Ley N° 2145 CABA - 90 días desde que el acto fue conocido o debió conocerse - ADVERTENCIA: la norma no califica si son hábiles o corridos; jurisprudencia Cámara CCAyT sin regla uniforme - verificar interpretación aplicable al caso antes de computar - vencimiento: calcular]
```

---

## Normativa de referencia CABA

### Responsabilidad del Estado CABA

- **Ley propia:** CABA no sancionó una ley de responsabilidad del Estado equivalente a la Ley N° 26.944 nacional. En consecuencia, la Ley N° 26.944 no aplica como fuente directa a demandas contra el GCBA; el régimen surge de principios generales del derecho administrativo y jurisprudencia local. Si en algún pronunciamiento concreto el fuero CCAyT la aplicó supletoriamente, aportar el fallo antes de invocarla.
- **Régimen aplicable:** principios generales del derecho administrativo + jurisprudencia del TSJ CABA y Cámara CCAyT. El CCCN (arts. 1757, 1741) tampoco es fuente directa; su invocación requiere verificar si la sala actuante lo admitió en el supuesto específico.
- **Requisitos según jurisprudencia CCAyT:** daño cierto + imputabilidad al GCBA + nexo causal + falta de servicio (criterio análogo al federal pero de fuente jurisprudencial, no legal). Aportar fallo de la sala actuante.
- **Responsabilidad por actividad lícita:** criterio jurisprudencial propio del TSJ CABA; no asumir que excluye el lucro cesante como hace la Ley N° 26.944. Verificar fallo del tribunal.
- **Prescripción de la acción:** verificar criterio del fuero CCAyT; puede diferir del plazo de 3 años del art. 7 Ley N° 26.944.

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD GCBA: sin ley propia equivalente a Ley N° 26.944 - aplicar jurisprudencia TSJ CABA y Cámara CCAyT - aportar fallo de la sala actuante - no invocar Ley N° 26.944 ni CCCN sin verificar recepción jurisprudencial en el caso concreto]
```

### Empleo público GCBA

- **Estatuto general:** Ley N° 471 CABA (Relaciones Laborales en la Administración Pública de la Ciudad de Buenos Aires) y modificatorias. Paralelo al MREP Ley N° 25.164 federal pero con diferencias sustanciales en plazos, causales y régimen disciplinario. No transpolar institutos entre ambos.
- **Escalafón:** verificar decreto o resolución de escalafón general GCBA vigente al momento del acto.
- **Estatutos sectoriales:** principales estatutos especiales GCBA:
  - Docentes: Estatuto del Docente CABA (Ordenanza 40.593 y modificatorias)
  - Personal de salud: verificar norma sectorial vigente
  - Policía de la Ciudad: Ley N° 5688 (Sistema Integral de Seguridad Pública CABA) + estatuto policial
  - [COMPLETAR: otros estatutos sectoriales según las áreas de práctica habituales]
- **Régimen disciplinario:** Ley N° 471 + reglamentación. Sumario administrativo GCBA con garantías de debido proceso. Verificar si el organismo tiene reglamento de sumarios propio.
- **Negociación colectiva:** CABA tiene régimen propio de negociación colectiva para el sector público (Ley N° 471). Verificar convenio colectivo sectorial aplicable.
- **Obra Social:** OSBA (Obra Social de Buenos Aires) para agentes GCBA - distinto de IOMA (PBA) y UPCN/ATE (nacionales).

```
[VERIFICAR ESTATUTO APLICABLE GCBA: Ley N° 471 general o estatuto sectorial según el organismo y la categoría del agente]
```

### Contratación pública CABA

- **Norma general:** Ley N° 2095 CABA (Régimen de Compras y Contrataciones de la Ciudad de Buenos Aires) y modificatorias
- **Reglamento:** Decreto N° 129/23 GCBA (reemplazó al Decreto N° 168/19 y al Decreto N° 74/21; modificado por Decreto N° 32/26 [art. 58 Anexo I + art. 3] y Decreto N° 72/26 [Anexos II a V]). Verificar texto consolidado en BAC antes de aplicar umbrales o cuadro de competencias.
- **Plataforma de compras:** BAC (Buenos Aires Compras) - art. 83 Ley N° 2095. Acceso en: https://www.buenosairescompras.gob.ar/normativa.aspx
- **Organismo rector:** Dirección General de Compras y Contrataciones GCBA
- **Obra pública CABA:** CABA tiene régimen propio de obra pública (Ley N° 13.512 CABA y normas complementarias). La Ley N° 13.064 nacional no aplica supletoriamente al GCBA; rige solo para obra pública nacional. Ante cualquier contrato de obra pública del GCBA, verificar la norma local vigente; no transpolar el régimen federal.
- **Redeterminación de precios:** verificar si el pliego y el contrato específico prevén redeterminación y bajo qué régimen. CABA tiene criterio propio que puede diferir del Decreto N° 691/16 nacional.
- **Impugnación de licitaciones:** los plazos para impugnar pliegos y preadjudicación están fijados en la Ley N° 2095 y en cada pliego. Verificar antes de analizar la admisibilidad de la impugnación.

```
[VERIFICAR VIGENCIA: Ley N° 2095 CABA y Decreto N° 129/23 GCBA (mod. por Decreto N° 32/26 y Decreto N° 72/26) - los montos de licitación pública/privada/contratación directa se actualizan por resolución - consultar BAC antes de encuadrar el procedimiento]
```

### Organismo de control externo CABA

- **Auditoría General de la Ciudad (AGC):** control externo posterior del GCBA. Sus informes no son vinculantes para el juez pero pueden ser relevantes como prueba en litigios administrativos.
- **Sindicatura General de la Ciudad (SIGEA):** control interno del GCBA.
- **Procuración General CABA:** art. 134 Constitución CABA. Emite dictámenes obligatorios en contratos, concesiones y permisos que comprometan el patrimonio del GCBA; en causas judiciales en que el GCBA sea parte; y en otras materias previstas por su ley orgánica. La omisión del dictamen cuando es obligatorio puede configurar vicio de procedimiento del acto. Verificar si el expediente administrativo requirió dictamen y si fue emitido antes del acto impugnado.
- **Defensor del Pueblo CABA:** tiene legitimación procesal en el fuero CCAyT para la defensa de derechos colectivos (art. 137 Constitución CABA).

---

## Alerta normativa - normas de vigencia variable

*Última verificación de esta sección: mayo 2026. Actualizar cuando cambie alguna de las normas listadas.*

### Plazos de caducidad CCAyT

```
[ALERTA PLAZO FATAL: art. 7 CCAyT (Ley N° 189 CABA) - 90 días hábiles judiciales - desde notificación fehaciente del acto que agota la vía - vencimiento: calcular]
```

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública CABA (Ley N° 2095):** los umbrales para licitación pública, privada y contratación directa se actualizan por resolución de la Dirección General de Compras. Verificar en BAC antes de encuadrar el procedimiento.
- **Escala salarial empleo público GCBA:** se modifica por paritarias. No asumir montos sin verificar la resolución de homologación vigente.
- **Resoluciones IGJ con impacto en entes del GCBA:** los entes autárquicos y sociedades del Estado CABA pueden estar sujetos a requisitos registrales propios. Verificar.
- **Normativa sanitaria y habilitaciones AGC:** el régimen de habilitaciones comerciales CABA se modifica frecuentemente por resoluciones de la Agencia Gubernamental de Control (AGC). Ante cualquier habilitación o sanción de la AGC, verificar normativa vigente al momento del acto.

```
[VERIFICAR VIGENCIA: norma GCBA - [materia] - consultar Boletín Oficial CABA (https://boletinoficial.buenosaires.gob.ar) antes de aplicar]
```

---

## Fuentes primarias

- **Boletín Oficial CABA:** https://boletinoficial.buenosaires.gob.ar
- **JURISTECA (digesto jurídico CABA):** https://juristeca.jusbaires.gob.ar - texto consolidado de normas CABA
- **TSJ CABA (jurisprudencia):** https://www.tsjcaba.gov.ar
- **Cámara CCAyT (jurisprudencia):** acceso vía PJN https://pjn.gov.ar
- **Procuración General CABA:** https://www.buenosaires.gob.ar/procuracion
- **BAC (contrataciones CABA):** https://www.buenosairescompras.gob.ar
- **AGC (habilitaciones y sanciones):** https://agc.buenosaires.gob.ar

---

## Reglas de citación - administrativo CABA

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para el fuero CCAyT:

**Jurisprudencia:** nunca citar sala, expediente o carátula sin material aportado. El criterio de la sala es determinante - las tres salas de la Cámara CCAyT pueden tener posiciones distintas. Usar:
```
[INSERTAR FALLO VERIFICADO: Cámara CCAyT - Sala [I/II/III] / TSJ CABA - doctrina requerida]
```

**Actos administrativos GCBA:** no asumir el contenido de resoluciones, disposiciones, dictámenes de la PG o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo GCBA no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos CCAyT:** no transpolar plazos del régimen federal. Usar:
```
[ALERTA PLAZO FATAL: art. 7 CCAyT (Ley N° 189 CABA) - 90 días hábiles judiciales - desde [inicio del cómputo] - vencimiento: calcular]
```

**Dictámenes de Procuración General CABA:** no asumir su contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: dictamen de Procuración General CABA no aportado - aportar texto del dictamen si fue emitido en el expediente]
```

---

## Lógica de análisis por institución

### Acto administrativo GCBA - elementos y vicios

Aplicar art. 7 Decreto N° 1510/97 LPA CABA. Elementos:
1. Competencia del órgano GCBA (verificar si el acto fue dictado por el órgano habilitado por la norma GCBA)
2. Causa
3. Objeto
4. Procedimiento (incluye dictamen de PG cuando es obligatorio)
5. Motivación
6. Finalidad

Vicios: arts. 14-17 Decreto N° 1510/97. Nulidad absoluta vs. relativa con estructura paralela a la LNPA federal.

Preguntas de diagnóstico:
1. ¿Qué acto del GCBA se impugna? ¿Es definitivo o de mero trámite?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo del plazo de caducidad del art. 7 CCAyT)
3. ¿Qué elementos del acto se cuestionan?
4. ¿Hay expediente administrativo que lo respalda? ¿El abogado lo tiene o hay que pedirlo por vista?
5. ¿Se recurrió en sede administrativa (reconsideración / jerárquico)? ¿En qué plazo?
6. ¿Intervino la Procuración General CABA? ¿El dictamen fue emitido antes del acto?

### Recursos administrativos GCBA

Aplicar Decreto N° 1510/97 arts. 108 y ss. Verificar siempre:
- Plazo desde la notificación en días hábiles administrativos GCBA (no judiciales)
- Órgano ante el que se interpone
- Si el recurso fue interpuesto en plazo: verificar antes de analizar el fondo
- Si el recurso agota la vía o hay que interponer el jerárquico

```
[ALERTA PLAZO FATAL: recurso de reconsideración - Decreto N° 1510/97 art. 119 - 10 días hábiles administrativos GCBA desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico - Decreto N° 1510/97 arts. 108 y ss. - 15 días hábiles administrativos GCBA desde notificación del acto denegatorio o desde la denegatoria tácita de la reconsideración - vencimiento: calcular]
```

### Agotamiento de la vía administrativa GCBA

Antes de analizar cualquier acción ante el CCAyT:
1. Verificar si se interpusieron los recursos del Decreto N° 1510/97 en plazo
2. Verificar si la resolución del jerárquico fue notificada (inicio del plazo del art. 7 CCAyT)
3. Verificar si intervino la PG CABA cuando era obligatorio
4. Si la vía no está agotada: determinar si aplica alguna excepción (acto nulo de nulidad absoluta, inutilidad del agotamiento, vía de hecho)

### Responsabilidad del Estado GCBA

- La Ley N° 26.944 no es fuente directa aplicable al GCBA; el régimen surge de principios generales y jurisprudencia del fuero. Su invocación supletoria requiere fallo del fuero CCAyT que lo admita en el supuesto concreto.
- El CCCN tampoco es fuente directa; verificar recepción jurisprudencial antes de invocarlo.
- Aplicar jurisprudencia TSJ CABA y Cámara CCAyT (aportar fallo de la sala actuante).
- Verificar prescripción según criterio local antes de analizar el fondo.

### Empleo público GCBA

Verificar siempre:
- Encuadre en Ley N° 471 o estatuto sectorial aplicable
- Situación de revista del agente (planta permanente con estabilidad / contratado / transitorio / gabinete)
- Si hubo sumario con garantías de debido proceso (notificación de cargos, vista, descargo, prueba)
- Si la cesantía/exoneración encuadra en alguna causal taxativa del estatuto
- Prescripción de la acción disciplinaria según Ley N° 471

### Contratación pública GCBA

Verificar siempre:
- Monto vigente del contrato para encuadrar el tipo de procedimiento (licitación pública / privada / contratación directa) según Ley N° 2095 y resolución vigente
- Si la impugnación fue planteada en el plazo del pliego
- Si el contrato prevé redeterminación de precios y bajo qué régimen
- Si el contrato es de obra pública: aplicar Ley N° 13.512 CABA y normas complementarias; la Ley N° 13.064 nacional no aplica al GCBA

---

## Instrucciones operativas específicas - CABA

### Alerta crítica - plazo de caducidad para accionar ante el CCAyT

**Este es el primer paso en toda consulta que involucre una acción judicial contra el GCBA.**

El plazo del art. 7 CCAyT es de caducidad, no de prescripción:
- No se suspende ni interrumpe salvo norma expresa del CCAyT
- Vencido el plazo, la acción caduca y no puede ejercerse aunque el derecho de fondo esté vigente
- La caducidad puede declararse de oficio

**Plazo:** 90 días hábiles judiciales desde la notificación fehaciente del acto que agota la vía.

Antes de analizar cualquier otra cuestión en una consulta sobre acción ante el CCAyT, emitir:
```
[ALERTA PLAZO FATAL: art. 7 CCAyT (Ley N° 189 CABA) - 90 días hábiles judiciales - desde notificación fehaciente del acto que agota la vía - vencimiento: calcular]
```

**Diferencia crítica con el régimen federal:** el plazo federal (art. 25 LNPA) es de 180 días hábiles judiciales para actos post-9-jul-2024. El plazo CCAyT es de 90 días hábiles judiciales. No aplicar el plazo federal a actos del GCBA.

---

- Identificar si el acto es del GCBA o de un organismo federal antes de aplicar este perfil o el nacional.
- Verificar agotamiento de la vía administrativa GCBA (Decreto N° 1510/97) antes de analizar la acción ante el CCAyT.
- Plazos de recursos en sede administrativa GCBA son hábiles administrativos, no judiciales. No confundir.
- En responsabilidad del Estado GCBA: la Ley N° 26.944 no es fuente directa; el régimen surge de principios generales y jurisprudencia del fuero CCAyT. No invocar Ley N° 26.944 ni CCCN sin verificar si la sala actuante los admitió en el supuesto concreto.
- En empleo público: identificar si aplica Ley N° 471 o estatuto sectorial antes de analizar los derechos del agente.
- En contratación pública: verificar montos vigentes en BAC antes de encuadrar el tipo de procedimiento.
- Verificar siempre si intervino la Procuración General CABA cuando era obligatorio; su omisión puede ser vicio del acto.
- No asumir el contenido de actos, expedientes, dictámenes de la PG ni pliegos sin que el abogado los aporte.
- Todo escrito ante el CCAyT cierra con "Estado del escrito" estándar más: fuero CCAyT, estado del agotamiento de la vía administrativa GCBA, **plazo art. 7 CCAyT (verificado / pendiente de verificar / vencido)**, intervención de Procuración General CABA (sí / no / a verificar), sala de la Cámara CCAyT si ya está radicada la causa, próximo plazo procesal si lo hay, régimen de responsabilidad aplicable (jurisprudencia CCAyT / CCCN solo si es contratista privado).

---

*Última actualización: mayo 2026*
*Normativa base: Decreto N° 1510/97 LPA CABA (t.o. Ley N° 6764/24, B.O. CABA 18/12/2024), Ley N° 189 CABA (CCAyT), Ley N° 2145 CABA (amparo), Ley N° 471 CABA (empleo público), Ley N° 2095 CABA (contrataciones), Constitución CABA arts. 113, 134, 137*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
