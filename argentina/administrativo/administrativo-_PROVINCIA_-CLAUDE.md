# Perfil de práctica · Derecho administrativo · [PROVINCIA]

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de [PROVINCIA].
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables del Bloque 0 antes de usar.
>
> **Estado del perfil:** [COMPLETAR al entregar. Ej: "operativo - todos los campos completados y verificados contra texto legal" / "operativo con campos pendientes (ver etiquetas [PENDIENTE] en el texto)" / "borrador - requiere revisión antes de usar en caso concreto".]

---

## Sistema de etiquetas

Este perfil usa tres etiquetas para distinguir el nivel de certeza de cada regla al completar los campos:

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de la fecha de actualización del perfil.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse en el Boletín Oficial provincial o en el portal del Poder Judicial antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

Cuando una sección mezcle niveles, el etiquetado aparece en la regla específica, no en el título de la sección. Los campos vacíos del template no llevan etiqueta; la etiqueta se incorpora al completar.

---

## Changelog

| Versión | Fecha | Cambios principales |
|---------|-------|---------------------|
| 1.0 | [COMPLETAR] | Versión inicial |

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** [COMPLETAR: nombre de la provincia]

**FUERO_HABITUAL:** [COMPLETAR: denominación exacta del fuero contencioso administrativo provincial. Ej: "Cámara en lo Contencioso Administrativo - Sala I, La Plata" / "Juzgados Civiles y Comerciales con competencia administrativa, Córdoba" / "Juzgados de Primera Instancia en lo Contencioso Administrativo, Mendoza". Incluir ciudad o departamento judicial si corresponde.]

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo provincial. Ej: "Responsabilidad del Estado provincial, empleo público provincial, contratación pública provincial".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos provinciales ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Salud, Fiscalía de Estado, DGR provincial".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la provincia de [PROVINCIA]: procedimiento administrativo ante organismos provinciales y municipales, recursos administrativos en sede provincial, control judicial contencioso administrativo provincial, responsabilidad del Estado provincial, empleo público provincial y contratación pública provincial.

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en [PROVINCIA] (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA) - ver administrativo-CLAUDE.md. Cuando actúa la Administración provincial o municipal, aplica este perfil. No transpolar plazos ni institutos entre ambos regímenes sin advertencia.

**Actos mixtos:** cuando en un mismo caso coexisten actos de organismos provinciales y federales, cada régimen se aplica al acto correspondiente por separado. Los plazos del régimen federal no se extienden al acto provincial, ni viceversa.

**Tercer nivel - organismos municipales:** [COMPLETAR: ¿el fuero contencioso administrativo provincial tiene competencia sobre actos municipales? ¿O existe fuero municipal propio o competencia civil/comercial? El agotamiento de la vía ante organismos municipales puede tener regulación diferenciada: verificar si el municipio tiene ordenanza de procedimiento propio y qué recursos prevé ante el Intendente o el Concejo Deliberante antes de ocurrir al fuero judicial. Si el régimen municipal es idéntico al provincial, consignarlo expresamente.]

```
[VERIFICAR RÉGIMEN MUNICIPAL: [PROVINCIA] - actos de municipios pueden tener fuero, plazos y vía de agotamiento distintos del régimen provincial - verificar antes de encuadrar]
```

**Primer paso obligatorio en toda consulta:** identificar si el acto es de un organismo provincial, municipal o federal antes de aplicar este perfil o el nacional.

---

## Bloque 2 - Normativa de procedimiento administrativo provincial

### 2.1 Ley de procedimiento administrativo provincial

- **Norma principal:** [COMPLETAR: número, nombre oficial y año. Ej: "Ley 5348 (Ley de Procedimientos Administrativos, Salta)" / "Decreto-Ley 7647/70 (LPA PBA)".]
- **Reglamento:** [COMPLETAR: decreto reglamentario si existe, con número y año. Si no existe equivalente al Decreto 1759/72 federal, consignarlo expresamente.]
- **Texto vigente:** [COMPLETAR: indicar si hubo reformas recientes y dónde consultar el texto actualizado. Ej: "Texto consolidado disponible en [URL digesto provincial]".]
- **Articulado clave:** [COMPLETAR: artículos sobre elementos del acto, recursos, silencio, plazos. Ej: "arts. X-Y (acto administrativo), arts. Z-W (recursos), art. N (silencio)".]

```
[VERIFICAR VIGENCIA: ley de procedimiento administrativo [PROVINCIA] - verificar modificaciones posteriores a la fecha de este perfil en el digesto o boletín oficial provincial]
```

### 2.2 Régimen de silencio administrativo provincial

- **Regla general:** [COMPLETAR: ¿la provincia adoptó silencio positivo, negativo, o mixto? ¿Hay norma específica? Precisar el mecanismo: ¿requiere pronto despacho previo? ¿En qué plazo opera la denegatoria tácita?]
- **Sin reforma análoga al Decreto 971/2024 nacional:** [COMPLETAR: verificar si la provincia adoptó el régimen de silencio positivo de la Ley 27.742 nacional. Si no lo adoptó, consignarlo expresamente: "Sin reforma análoga - aplica silencio [positivo/negativo] del régimen original".]
- **Denegatoria tácita:** [COMPLETAR: plazo a partir del cual opera y norma que lo establece. Precisar si requiere presentación de pronto despacho como requisito previo para habilitar la instancia judicial.]

```
[VERIFICAR RÉGIMEN DE SILENCIO: [PROVINCIA] - norma aplicable - secuencia procedimental para configurar la denegatoria tácita y habilitar la vía judicial]
```

### 2.3 Elementos esenciales del acto administrativo provincial

[COMPLETAR: verificar si la ley provincial enumera expresamente los elementos o si el sistema los recoge por vía jurisprudencial. Indicar los artículos relevantes.]

Elementos (estructura general del derecho administrativo argentino; ajustar si la ley provincial difiere):

1. Competencia: irrenunciable e improrrogable
2. Causa: antecedentes de hecho y de derecho que fundamentan el acto
3. Objeto: cierto, lícito, físicamente posible
4. Procedimiento: cumplimiento de trámites esenciales previos
5. Motivación: [COMPLETAR: ¿la ley provincial regula cuándo es obligatoria? Indicar artículo.]
6. Finalidad: adecuada a la causa del acto y al ordenamiento provincial

**Régimen de nulidades provincial:** [COMPLETAR: ¿la ley distingue nulidad absoluta / relativa con los criterios de la LNPA arts. 14-15? ¿Hay regulación propia? Indicar artículos. Si la ley no hace esa distinción, alertar expresamente para no transpolar el esquema federal.]

### 2.4 Recursos administrativos provinciales

**Recurso de reconsideración / revocatoria:**
- Plazo: [COMPLETAR: días hábiles administrativos - norma con artículo]
- Ante: [COMPLETAR: mismo órgano emisor]
- Efecto: [COMPLETAR: ¿suspende el plazo para el recurso jerárquico? ¿Efecto suspensivo sobre la ejecutoriedad del acto?]

**Recurso jerárquico:**
- Plazo: [COMPLETAR: días hábiles administrativos - norma con artículo]
- Ante: [COMPLETAR: superior jerárquico / ministro / gobernador según el caso]
- ¿Agota la vía?: [COMPLETAR: sí / no / depende del organismo. Indicar artículo.]
- **Advertencia - secuencia no necesariamente rígida:** [COMPLETAR: verificar si la reconsideración/revocatoria es siempre obligatoria o si en algunos supuestos el jerárquico puede interponerse directamente sin el recurso previo.]

**Recurso de alzada:**
- [COMPLETAR: ¿procede contra actos de entes autárquicos y descentralizados provinciales? Plazo y ante quién. ¿Es obligatorio u optativo según jurisprudencia del tribunal superior provincial? Si es optativo, precisar: si el particular prescinde de él, ¿el plazo para accionar judicialmente corre desde el acto del ente sin esperar la resolución del alzada?]

**Queja:**
- [COMPLETAR: ¿existe? Si existe: plazo, efectos sobre otros plazos. Consignar si no existe instituto equivalente y cuál es el remedio ante anomalías de trámite.]

**Otros recursos específicos de la provincia:**
- [COMPLETAR: si la provincia tiene recursos especiales no contemplados en el esquema anterior.]

**Sin reforma análoga a la Ley 27.742 nacional:**
- [COMPLETAR: ¿la provincia duplicó los plazos de recursos administrativos como hizo el Decreto 695/2024 federal? Si no hubo reforma local, consignar expresamente: "Sin reforma análoga - aplican plazos originales de la ley provincial". Los plazos federales reformados no se aplican a recursos ante la Administración provincial.]

**Días hábiles administrativos [PROVINCIA]:** son los días hábiles del Poder Ejecutivo provincial, que pueden diferir del calendario de días hábiles judiciales. Verificar decreto de asueto vigente al momento del acto.

```
[ALERTA PLAZO FATAL: recurso de [denominación] - [norma provincial art. X] - [X] días hábiles administrativos desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico - [norma provincial art. X] - [X] días hábiles administrativos desde notificación del acto denegatorio o desde denegatoria tácita - vencimiento: calcular]
```

### 2.5 Agotamiento de la vía administrativa provincial

- **Regla general:** [COMPLETAR: ¿es requisito previo de admisibilidad de la acción judicial? ¿La ley local lo exige expresamente o surge de la jurisprudencia del tribunal superior provincial? Indicar norma o fallo de referencia.]
- **Excepciones:** [COMPLETAR: ¿la ley o jurisprudencia provincial reconoce excepciones al agotamiento? Listar las principales con norma o fallo de referencia. Ej: acto nulo de nulidad absoluta, inutilidad del agotamiento, vía de hecho, acto dictado por la autoridad jerárquica máxima.]
- **Asesoría / Fiscalía de Estado:** [COMPLETAR: ¿interviene con dictamen obligatorio antes del acto? ¿La omisión del dictamen configura vicio de procedimiento? ¿Tiene intervención preceptiva en contrataciones, concesiones, transacciones? ¿Es parte necesaria en el proceso judicial?]
- **Organismos municipales:** [COMPLETAR: ¿el agotamiento ante actos municipales tiene regulación diferenciada? ¿Qué recursos deben interponerse ante el municipio antes de ocurrir al fuero judicial? Si el régimen es idéntico al provincial, consignarlo expresamente.]

```
[VERIFICAR AGOTAMIENTO DE VÍA: [PROVINCIA] - [norma provincial] - verificar si se interpusieron los recursos en plazo y si la resolución que agota la vía fue notificada - determinar si aplica alguna excepción]
```

### 2.6 Tabla unificada de plazos - sede administrativa

| Recurso / instituto | Plazo | Cómputo | Norma | Nivel de certeza |
|---------------------|-------|---------|-------|-----------------|
| Reconsideración / revocatoria | [X] días hábiles adm. | desde notificación | [art. X] | [COMPLETAR] |
| Jerárquico | [X] días hábiles adm. | desde notificación / denegatoria | [art. X] | [COMPLETAR] |
| Alzada | [X] días hábiles adm. | desde notificación | [art. X] | [COMPLETAR] |
| Pronto despacho / silencio | [X] días hábiles adm. | desde [hito] | [art. X] | [COMPLETAR] |

---

## Bloque 3 - Control judicial contencioso administrativo

### 3.1 Código / ley de proceso contencioso administrativo

- **Norma:** [COMPLETAR: número y nombre oficial. Ej: "Ley 793 (Código de Procedimientos en lo Contencioso Administrativo, Salta, mod. por Ley 6569)" / "Ley 12.008 (CCA PBA)".]
- **Modificatorias:** [COMPLETAR: leyes modificatorias relevantes y año.]
- **Texto vigente:** [COMPLETAR: URL donde consultar el texto actualizado.]
- **Subsidiariedad:** [COMPLETAR: ¿el código local remite al CPCC provincial para lo no previsto? ¿En qué materias?]

### 3.2 Plazo de caducidad para accionar judicialmente

**Este es el dato más crítico del perfil. Completar con precisión.**

- **Plazo general:** [COMPLETAR: días hábiles judiciales / corridos - norma exacta con artículo]
- **Cómputo:** [COMPLETAR: desde notificación del acto que agota la vía / desde el vencimiento del plazo para resolver el recurso / otro. Indicar si la jurisprudencia del tribunal superior provincial ha interpretado que son días hábiles judiciales aunque la norma diga "días".]
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa.
- **Advertencia - recursos optativos:** [COMPLETAR: si el alzada u otro recurso es optativo, precisar si su interposición suspende o no el plazo de caducidad para accionar. Indicar el criterio del tribunal superior provincial.]
- **Inicio del cómputo según tipo de pretensión:** [COMPLETAR: si el código prevé incisos diferenciados por tipo de pretensión (anulatoria, resarcitoria acumulada, vía de hecho, etc.), listarlos con el inicio del cómputo para cada uno.]
- **Procesos especiales o sumarios:** [COMPLETAR: ¿existe un proceso sumario o abreviado con plazo distinto? Indicar plazo y norma.]
- **¿Declarable de oficio?:** [COMPLETAR: sí / verificar jurisprudencia del tribunal superior provincial]

```
[ALERTA PLAZO FATAL: [norma provincial art. X] - [X] días hábiles [judiciales/corridos] - desde notificación del acto que agota la vía - verificar inicio del cómputo según tipo de pretensión - vencimiento: calcular]
```

**Diferencia crítica con el régimen federal:** el plazo federal (art. 25 LNPA) es de 180 días hábiles judiciales para actos notificados post-9-jul-2024. El plazo provincial de [PROVINCIA] es de [COMPLETAR]. No asumir equivalencia con ninguno de los dos regímenes federales.

### 3.3 Órganos jurisdiccionales

**Primera instancia:**
- **Juzgados:** [COMPLETAR: denominación exacta. Indicar si hay fuero especializado o si la competencia está distribuida entre juzgados civiles/comerciales.]
- **Organización territorial:** [COMPLETAR: ¿hay juzgados en el interior o solo en la capital? ¿Cómo se distribuye la competencia territorial? Indicar regla de competencia por domicilio del demandado o lugar del acto.]
- **Competencia por materia:** [COMPLETAR: ¿el fuero tiene competencia exclusiva sobre materia administrativa o comparte con juzgados civiles?]

**Alzada:**
- **Tribunal:** [COMPLETAR: denominación exacta.]
- **Salas:** [COMPLETAR: número de salas si corresponde. Advertir si las salas pueden tener criterios distintos en cuestiones no unificadas por el tribunal superior.]
- **Jurisprudencia:** [COMPLETAR: URL de acceso.]

**Tribunal superior:**
- **Tribunal:** [COMPLETAR: denominación exacta. Ej: "Suprema Corte de Justicia de [PROVINCIA]" / "Superior Tribunal de Justicia" / "Corte de Justicia de [PROVINCIA]".]
- **Recurso de acceso:** [COMPLETAR: recurso extraordinario provincial / recurso de inconstitucionalidad / inaplicabilidad de ley / casación / otro. Indicar requisitos principales de admisibilidad.]
- **Competencia originaria:** [COMPLETAR: ¿el tribunal superior tiene competencia originaria en materia contencioso administrativa? ¿En qué casos?]

### 3.4 Pretensiones admisibles

[COMPLETAR: ¿el código provincial enumera las pretensiones admisibles (anulación, restablecimiento del derecho, declarativa, prestacional, cautelar autónoma)? ¿O sigue un sistema abierto? Indicar artículo y enumerar las principales.]

### 3.5 Medidas cautelares contra el Estado provincial

- **Régimen:** [COMPLETAR: ¿la provincia tiene ley especial de cautelares contra el Estado equivalente a la Ley 26.854 nacional? ¿O aplica el régimen general del CPCC provincial? La Ley 26.854 rige solo contra el Estado nacional; no aplicarla al Estado provincial sin verificar norma local equivalente.]
- **Requisitos:** [COMPLETAR: verosimilitud del derecho + peligro en la demora + otros si la ley local los agrega]
- **Informe previo del Estado:** [COMPLETAR: ¿el código local exige informe previo del organismo demandado antes de resolver la cautelar? ¿En qué plazo?]
- **Plazo de vigencia de la cautelar:** [COMPLETAR: ¿existe límite temporal? ¿Cuál?]
- **Contracautela:** [COMPLETAR: ¿se exige siempre? ¿Puede ser juratoria?]

```
[VERIFICAR RÉGIMEN CAUTELAR: [PROVINCIA] - norma aplicable - no asumir equivalencia con Ley 26.854 nacional]
```

### 3.6 Amparo provincial

- **Norma:** [COMPLETAR: constitución provincial + ley de amparo provincial si existe.]
- **Plazo:** [COMPLETAR: días hábiles / corridos desde que el acto fue conocido o debió conocerse. Indicar artículo.]
- **Subsidiariedad:** [COMPLETAR: ¿procede solo si no hay otro remedio judicial más idóneo?]
- **Particularidades:** [COMPLETAR: habeas data integrado / amparo colectivo / otros.]

```
[ALERTA PLAZO FATAL - AMPARO: [norma provincial art. X] - [X] días [hábiles/corridos] - desde [inicio del cómputo] - vencimiento: calcular]
```

---

## Bloque 4 - Normativa de referencia provincial

### 4.1 Responsabilidad del Estado provincial

- **Ley propia:** [COMPLETAR: ¿la provincia sancionó una ley de responsabilidad del Estado equivalente a la Ley 26.944 nacional? Si existe, indicar número. Si no existe, consignar: "Sin ley propia - aplican principios generales del derecho administrativo y jurisprudencia del [tribunal superior provincial]". La Ley 26.944 rige solo contra el Estado nacional; no aplicarla al Estado provincial sin verificar norma local.]
- **Exclusión del CCCN:** [COMPLETAR: ¿la constitución o ley provincial excluye la aplicación del CCCN a la responsabilidad extracontractual del Estado provincial? ¿O rige por jurisprudencia local?]
- **Requisitos según jurisprudencia local:** [COMPLETAR: si no hay ley propia, indicar los requisitos que el tribunal superior provincial exige para la procedencia de la responsabilidad extracontractual del Estado (daño cierto, imputabilidad, nexo causal, falta de servicio). Aportar fallo de referencia.]
- **Pretensión resarcitoria y proceso sumario:** [COMPLETAR si la provincia tiene proceso sumario o abreviado: verificar si la pretensión resarcitoria puede acumularse al proceso sumario de ilegitimidad o debe plantearse en proceso autónomo posterior.]
- **Prescripción de la acción:** [COMPLETAR: plazo y norma. ¿Coincide con los 3 años del art. 7 Ley 26.944 o es distinto?]
- **Lucro cesante en responsabilidad por actividad lícita:** [COMPLETAR: ¿la jurisprudencia local lo admite o lo excluye?]

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD: [PROVINCIA] - ley propia o principios generales - no aplicar Ley 26.944 ni CCCN sin verificar criterio del fuero provincial]
```

### 4.2 Empleo público provincial

- **Estatuto general:** [COMPLETAR: ley del estatuto del empleado público provincial. Número y nombre.]
- **Escalafón:** [COMPLETAR: decreto o resolución de escalafón general. Indicar si hay escalafones sectoriales relevantes.]
- **Estatutos sectoriales:** [COMPLETAR: listar los principales estatutos especiales vigentes. Ej: estatuto docente (Ley XXXX), personal de salud (Ley XXXX), policía provincial (Ley XXXX).]
- **Régimen disciplinario:** [COMPLETAR: norma que regula el sumario administrativo provincial. Plazos, garantías, recursos internos.]
- **Tribunal administrativo / Tribunal de Disciplina:** [COMPLETAR: ¿existe órgano especializado? ¿Sus resoluciones son revisables judicialmente y por qué vía?]
- **Negociación colectiva:** [COMPLETAR: ¿la provincia adhirió a la Ley 24.185? ¿Tiene ley propia?]

```
[VERIFICAR ESTATUTO APLICABLE: [PROVINCIA] - estatuto general o sectorial según el organismo y la categoría del agente]
```

### 4.3 Contratación pública provincial

- **Norma general:** [COMPLETAR: ley o decreto de compras y contrataciones del Estado provincial. Número y nombre.]
- **Reglamento:** [COMPLETAR: decreto reglamentario.]
- **Plataforma de compras:** [COMPLETAR: ¿la provincia tiene sistema electrónico de contrataciones? Nombre y URL.]
- **Organismo rector:** [COMPLETAR: denominación del organismo equivalente a la ONC nacional.]
- **Obra pública provincial:** [COMPLETAR: ¿la provincia tiene ley propia de obra pública o aplica la Ley 13.064 nacional?]
- **Redeterminación de precios:** [COMPLETAR: ¿la provincia tiene régimen propio? Norma aplicable.]
- **Impugnación de licitaciones:** [COMPLETAR: plazos para impugnar pliegos y preadjudicación según la norma local.]

```
[VERIFICAR VIGENCIA: norma de contrataciones [PROVINCIA] - los montos de licitación y los plazos se actualizan por decreto o resolución con frecuencia - consultar plataforma provincial antes de encuadrar el procedimiento]
```

### 4.4 Organismo de control externo

- **Tribunal de Cuentas / Contaduría General:** [COMPLETAR: denominación exacta. ¿Tiene función jurisdiccional (juicio de cuentas, juicio de responsabilidad)? ¿Sus resoluciones son revisables judicialmente y por qué vía?]
- **Fiscalía de Estado / Asesoría General de Gobierno:** [COMPLETAR: denominación exacta. Funciones: ¿representa al Estado en juicio? ¿Dictamina en sede administrativa? ¿Interviene en contrataciones? ¿Es parte necesaria en el proceso contencioso?]
- **Control sobre municipios:** [COMPLETAR: ¿el Tribunal de Cuentas provincial tiene competencia sobre municipios? ¿Existen órganos de control municipales propios?]

### 4.5 Defensor del Pueblo provincial

[COMPLETAR: ¿existe Defensor del Pueblo provincial? ¿Tiene legitimación procesal en el fuero contencioso administrativo? Norma y artículo.]

### 4.6 Tabla de responsables procesales por instancia

[COMPLETAR: identificar quién representa al Estado provincial en cada instancia del proceso contencioso administrativo. Esta tabla es obligatoria para evitar errores de notificación y de legitimación pasiva.]

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| Primera instancia (juzgados) | [COMPLETAR] | [COMPLETAR: norma y artículo] |
| Alzada (cámara) | [COMPLETAR] | [COMPLETAR: norma y artículo] |
| Tribunal superior | [COMPLETAR] | [COMPLETAR: norma y artículo] |
| Estado como actor (impugna acto propio) | [COMPLETAR: ¿actúa la Fiscalía de Estado, la Asesoría General u otro órgano?] | [COMPLETAR] |
| Notificaciones | [COMPLETAR: domicilio procesal del representante del Estado para notificaciones] | [COMPLETAR] |

**Nota:** el representante del Estado puede variar según si el demandado es la Administración centralizada o un ente autárquico. [COMPLETAR: aclarar si el régimen difiere para entes descentralizados.]

```
[VERIFICAR REPRESENTACIÓN PROCESAL: [PROVINCIA] - identificar el representante del Estado por instancia antes de radicar - las notificaciones deben cursarse en el domicilio procesal correcto]
```

---

## Bloque 5 - Alerta normativa

*Última verificación de esta sección: [COMPLETAR: fecha]. Actualizar cuando cambie alguna de las normas listadas.*

### Plazos de caducidad

Los plazos para impugnar actos administrativos provinciales son breves y fatales. No asumir equivalencia con el régimen federal.

```
[ALERTA PLAZO FATAL: [norma provincial art. X] - [X] días hábiles [judiciales/corridos] - desde notificación del acto que agota la vía - vencimiento: calcular]
```

### Matriz de vigencia por norma

| Norma | Materia | Estado | Última verificación | Fuente |
|-------|---------|--------|--------------------|----|
| [Ley/Decreto X] | Procedimiento administrativo | [CONFIRMADO / A VERIFICAR] | [fecha] | [URL] |
| [Ley/Decreto X] | Proceso contencioso | [CONFIRMADO / A VERIFICAR] | [fecha] | [URL] |
| [Ley/Decreto X] | Empleo público | [CONFIRMADO / A VERIFICAR] | [fecha] | [URL] |
| [Ley/Decreto X] | Contrataciones | [CONFIRMADO / A VERIFICAR] | [fecha] | [URL] |
| [Ley/Decreto X] | Responsabilidad del Estado | [CONFIRMADO / A VERIFICAR] | [fecha] | [URL] |

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública:** se actualizan por decreto o resolución - verificar antes de encuadrar el procedimiento de selección.
- **Escala salarial del empleo público provincial:** se modifica por paritarias - no asumir montos sin verificar.
- [COMPLETAR: otras normas de vigencia variable específicas de la provincia.]

```
[VERIFICAR VIGENCIA: [norma provincial] - [materia] - consultar boletín oficial provincial antes de aplicar]
```

---

## Bloque 6 - Fuentes primarias

- **Boletín Oficial:** [COMPLETAR: URL del boletín oficial provincial]
- **Digesto / Portal jurídico provincial:** [COMPLETAR: URL donde consultar textos normativos consolidados]
- **Tribunal superior provincial:** [COMPLETAR: URL de jurisprudencia]
- **Fiscalía de Estado / Asesoría General:** [COMPLETAR: URL si publica dictámenes]
- **Organismo de compras:** [COMPLETAR: URL de la plataforma de contrataciones]
- **Poder Judicial provincial:** [COMPLETAR: URL portal general]

---

## Bloque 7 - Reglas de citación

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para este fuero provincial:

**Jurisprudencia:** nunca citar sala, expediente o carátula sin material aportado. El criterio de la sala actuante es determinante; salas distintas pueden tener posiciones diferentes en cuestiones no unificadas por el tribunal superior. Usar:
```
[INSERTAR FALLO VERIFICADO: [tribunal provincial] - sala/fuero - doctrina requerida]
```

**Actos administrativos provinciales:** no asumir el contenido de resoluciones, disposiciones, dictámenes o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos provinciales:** no transpolar plazos del régimen federal. Usar:
```
[ALERTA PLAZO FATAL: [norma provincial art. X] - [X] días [hábiles/corridos] - desde [inicio del cómputo] - vencimiento: calcular]
```

**Dictámenes de Fiscalía de Estado / Asesoría General:** no asumir su contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: dictamen de [Fiscalía de Estado / Asesoría General] no aportado - aportar texto del dictamen si fue emitido en el expediente]
```

---

## Bloque 8 - Lógica de análisis por institución

Las instituciones que siguen tienen base en el derecho administrativo general argentino. Donde la ley o jurisprudencia provincial difiera del régimen nacional, prevalece la regla local indicada en los bloques anteriores.

### Acto administrativo - elementos y vicios

Aplicar [norma LPA provincial]. Elementos según sección 2.3.

Preguntas de diagnóstico:
1. ¿Qué acto se impugna? ¿Es definitivo o de mero trámite? ¿Es del Estado provincial o de un municipio?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo del plazo de caducidad)
3. ¿Qué elementos del acto se cuestionan?
4. ¿Hay expediente administrativo que lo respalda? ¿El abogado lo tiene o hay que pedirlo por vista?
5. ¿Se recurrió en sede administrativa? ¿Qué recursos se interpusieron y en qué plazo?
6. ¿Intervino Fiscalía de Estado / Asesoría General cuando era obligatorio? ¿El dictamen fue emitido antes del acto?

### Recursos administrativos provinciales

Aplicar el esquema de la sección 2.4. Verificar siempre:
- Plazo desde la notificación (hábiles administrativos provinciales, no judiciales)
- Órgano ante el que se interpone
- Si la reconsideración/revocatoria es obligatoria o el jerárquico puede interponerse directamente
- Si el recurso de alzada ante entes descentralizados es obligatorio u optativo
- Si el recurso agota la vía o hay que interponer el jerárquico

```
[ALERTA PLAZO FATAL: recurso [denominación] - [norma provincial art. X] - [X] días hábiles administrativos desde notificación - vencimiento: calcular]
```

### Agotamiento de la vía administrativa provincial

Antes de analizar cualquier acción judicial:
1. Verificar si la vía está agotada (sección 2.5)
2. Si no lo está, determinar si aplica alguna excepción local
3. Verificar si la Fiscalía de Estado / Asesoría General requiere intervención previa
4. Alertar sobre el plazo de caducidad para accionar una vez agotada la vía

### Responsabilidad del Estado provincial

Aplicar el régimen de la sección 4.1. Alertas:
- No aplicar la Ley 26.944 nacional a demandas contra el Estado provincial sin verificar si la provincia tiene ley propia
- No aplicar el CCCN sin verificar el régimen local
- Si existe proceso sumario: verificar si la pretensión resarcitoria puede acumularse o debe plantearse en proceso autónomo posterior
- Verificar el plazo de prescripción provincial antes de analizar el fondo

### Empleo público provincial

Aplicar el estatuto de la sección 4.2. Verificar siempre:
- Situación de revista del agente (planta permanente con estabilidad / sin estabilidad / contratado / transitorio / gabinete)
- Estatuto aplicable (general o sectorial)
- Si hubo sumario con garantías de debido proceso (notificación de cargos, vista, descargo, prueba)
- Si la sanción expulsiva encuadra en alguna causal taxativa del estatuto
- [COMPLETAR si hay proceso sumario de impugnación de sanciones: verificar si el código provincial prevé un proceso abreviado con plazo distinto del ordinario]
- Prescripción de la acción disciplinaria según el estatuto provincial

### Contratación pública provincial

Aplicar la normativa de la sección 4.3. Verificar siempre:
- Montos vigentes para encuadrar el tipo de procedimiento (licitación pública / privada / directa)
- Plazos de impugnación de pliegos y preadjudicación según la norma local
- Si la redeterminación de precios aplica y bajo qué régimen
- Si el contrato es de obra pública: verificar si aplica ley provincial propia o Ley 13.064 nacional

---

## Bloque 9 - Instrucciones operativas

### Alerta crítica - plazo de caducidad para accionar judicialmente

**Este es el primer paso en toda consulta que involucre una acción judicial contra el Estado provincial de [PROVINCIA].**

El plazo para demandar es un plazo de caducidad, no de prescripción:
- No se suspende ni interrumpe por las mismas causales que la prescripción
- Vencido el plazo, la acción caduca y no puede ejercerse aunque el derecho de fondo esté vigente
- La caducidad puede declararse de oficio

**Plazo provincial:** [COMPLETAR: X días hábiles judiciales / corridos - norma con artículo]

Antes de analizar cualquier otra cuestión en una consulta sobre acción contenciosa provincial, emitir:
```
[ALERTA PLAZO FATAL: [norma provincial art. X] - [X] días hábiles [judiciales/corridos] - desde notificación del acto que agota la vía - vencimiento: calcular]
```

**Diferencia con el régimen federal:** el plazo federal (art. 25 LNPA) es de 180 días hábiles judiciales para actos post-9-jul-2024. El plazo provincial de [PROVINCIA] es de [COMPLETAR]. No asumir equivalencia con ninguno de los dos regímenes federales.

---

- Identificar si el acto es del Estado provincial, de un municipio o de un organismo federal antes de aplicar este perfil o el nacional.
- En actos mixtos: aplicar cada régimen al acto correspondiente por separado.
- Verificar agotamiento de la vía administrativa provincial antes de analizar la acción judicial.
- Plazos de recursos en sede administrativa son hábiles administrativos, no judiciales. No confundir.
- En responsabilidad del Estado provincial: verificar primero si existe ley propia antes de aplicar principios generales. No aplicar Ley 26.944 ni CCCN sin verificar criterio del fuero.
- En empleo público: identificar el estatuto aplicable (general o sectorial) antes de analizar los derechos del agente.
- En contratación pública: verificar montos vigentes antes de encuadrar el tipo de procedimiento.
- No asumir el contenido de actos, expedientes, pliegos ni dictámenes de Fiscalía de Estado / Asesoría General sin que el abogado los aporte.
- Todo escrito provincial cierra con "Estado del escrito" estándar más: fuero y régimen aplicado, estado del agotamiento de la vía administrativa provincial, **plazo de caducidad provincial (verificado / pendiente de verificar / vencido)**, intervención de Fiscalía de Estado / Asesoría General (sí / no / a verificar), sala del tribunal si ya está radicada la causa, próximo plazo procesal si lo hay, régimen de responsabilidad aplicable (ley provincial propia / principios generales / CCCN solo si es contratista privado).

---

*Última actualización: [COMPLETAR: fecha]*
*Normativa base: [COMPLETAR: listar las normas provinciales principales incorporadas al completar el template]*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
