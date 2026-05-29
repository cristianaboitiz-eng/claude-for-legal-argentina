# Perfil de práctica · Derecho administrativo · Provincia de San Juan

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de San Juan.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables del Bloque 0 antes de usar.
>
> **Estado del perfil:** operativo - todos los campos estructurales completados y verificados contra la Ley N° 1995-A, la Ley N° 2415-O y el Digesto Jurídico de San Juan. Quedan [PENDIENTE] solo los campos de configuración inicial (AREAS_PRACTICA y ORGANISMO_CONTRALOR_HABITUAL), los estatutos sectoriales de empleo público, el reglamento de la Ley N° 1995-A y los campos de Fiscalía de Estado (domicilio procesal, URL) que dependen del caso concreto.

---

## Sistema de etiquetas

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de la fecha de actualización del perfil.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse en el Boletín Oficial provincial o en el portal del Poder Judicial antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

---

## Changelog

| Versión | Fecha | Cambios principales |
|---------|-------|---------------------|
| 1.0 | Mayo 2025 | Versión inicial - fuente: Ley N° 2415-O, Ley N° 1995-A, Digesto Jurídico de San Juan |
| 1.1 | Mayo 2025 | Completado: articulado Ley N° 1995-A (recursos, elementos, nulidades, silencio + pronto despacho); plazo de caducidad con artículo exacto (30 días corridos acto expreso / 3 meses silencio - arts. 727 y ss. Ley N° 2415-O); Fiscalía de Estado (Ley N° 319-E, art. 263 CP); empleo público (Ley N° 560-E); contrataciones (Ley N° 2000-A + Decreto 1148-MHF-2020); responsabilidad del Estado (sin ley propia - aplicación pretoriana arts. 8 y 43 CP San Juan) |

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** Provincia de San Juan

**FUERO_HABITUAL:** Juzgado Contencioso Administrativo de la Primera Circunscripción Judicial - Ciudad de San Juan (primera instancia, órgano unipersonal especializado). Alzada: Cámara de Apelaciones en lo Civil, Comercial y Minería de San Juan (salas distribuidas, sin cámara exclusiva CA). No existe instancia originaria ante tribunal superior; el STJ de San Juan interviene solo por vía extraordinaria.

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo San Juan. Ej: "Empleo público provincial, responsabilidad del Estado, contratación pública, impugnación de actos del Poder Ejecutivo Provincial".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos provinciales ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Hacienda, OSSE, EPSE, Municipalidad de San Juan".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de San Juan: procedimiento administrativo ante organismos provinciales y municipales (Ley N° 1995-A), recursos administrativos en sede provincial, control judicial contencioso administrativo (Ley N° 2415-O, Título V), responsabilidad del Estado provincial, empleo público provincial y contratación pública provincial.

**Particularidad estructural - reforma 2022:** el proceso contencioso administrativo fue reformado íntegramente por la Ley N° 2415-O (sancionada el 11 de agosto de 2022, publicada el 12 de septiembre de 2022), que reemplazó al anterior código (Ley N° 988-O). El proceso CA no tiene código propio: está integrado en el Título V del Código Procesal Civil, Comercial y Minería. No invocar la Ley N° 988-O ni el régimen anterior sin verificar si la cuestión corresponde a hechos anteriores a la vigencia de la Ley N° 2415-O. [CONFIRMADO]

**Particularidad estructural - gestión de audiencias:** el Juzgado Contencioso Administrativo funciona bajo la coordinación de la Oficina de Gestión de Audiencias (OGA) para los Juzgados Especializados en lo Comercial y Contencioso Administrativo. El juez unipersonal conserva exclusivamente la potestad jurisdiccional (sentencias y dirección de audiencias); la agenda y estructura administrativa quedan en la OGA. Prever esta lógica al coordinar audiencias y presentaciones. [CONFIRMADO]

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en San Juan (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal sanjuanina, aplica este perfil. No transpolar plazos ni institutos.

**Actos mixtos:** cuando en un mismo caso coexisten actos de organismos provinciales y federales, cada régimen se aplica al acto correspondiente por separado.

**Tercer nivel - organismos municipales:** los actos de los municipios y sus entes descentralizados son impugnables ante el Juzgado Contencioso Administrativo. El agotamiento de la vía ante actos municipales es presupuesto de admisibilidad. Verificar si el municipio tiene ordenanza de procedimiento propio antes de encuadrar el agotamiento; a falta de norma municipal, aplica supletoriamente la Ley N° 1995-A. [CONFIRMADO - régimen de agotamiento municipal: A VERIFICAR en cada caso]

```
[VERIFICAR RÉGIMEN MUNICIPAL SAN JUAN: actos de municipios - competencia del Juzgado Contencioso Administrativo - verificar ordenanza de procedimiento del municipio antes de encuadrar el agotamiento de la vía]
```

**Primer paso obligatorio en toda consulta:** identificar si el acto es del Estado provincial, de un municipio o de un organismo federal antes de aplicar este perfil o el nacional.

---

## Bloque 2 - Normativa de procedimiento administrativo provincial

### 2.1 Ley de procedimiento administrativo provincial

- **Norma principal:** Ley N° 1995-A (texto unificado y consolidado por la Ley N° 2504-E en el Digesto Jurídico de San Juan). Ex Ley N° 135-A, históricamente conocida como Ley N° 3756. [CONFIRMADO]
- **Contenido:** regula los elementos del acto administrativo, el régimen general de nulidades, la caducidad del procedimiento por inactividad y los plazos de los recursos de reconsideración y jerárquico de la Administración Central y descentralizada de San Juan. [CONFIRMADO]
- **Reglamento:** la Ley N° 1995-A no tiene decreto reglamentario equivalente al Decreto 1759/72 federal. La norma está redactada de manera integral; las formalidades de escritos, vistas, notificaciones y plazos procesales se regulan de forma directa dentro del propio texto unificado, sin perjuicio de decretos organizativos menores por ministerio. [CONFIRMADO]
- **Texto vigente:** Digesto Jurídico de San Juan - Ley N° 1995-A. Verificar modificaciones posteriores a la consolidación por Ley N° 2504-E en el Boletín Oficial provincial. [CONFIRMADO]
- **Articulado clave:** arts. 85 y ss. (recurso de reconsideración y jerárquico); art. 70 (silencio administrativo y pronto despacho); artículos sobre elementos del acto (ver sección 2.3); artículos sobre nulidades (ver sección 2.3). [CONFIRMADO - numeración exacta de artículos sobre elementos y nulidades: A VERIFICAR en el texto consolidado]

```
[VERIFICAR VIGENCIA: Ley N° 1995-A San Juan - ley de procedimiento administrativo - verificar modificaciones posteriores a la consolidación por Ley N° 2504-E en el Digesto o Boletín Oficial provincial]
```

### 2.2 Régimen de silencio administrativo provincial

- **Regla general:** silencio administrativo negativo. [CONFIRMADO]
- **Plazo general para resolver:** treinta (30) días desde la interposición del recurso o desde la presentación de los alegatos si hubo apertura a prueba. [CONFIRMADO - Ley N° 1995-A]
- **Mecanismo de agotamiento por silencio (art. 70 LPA en concordancia con CPCA):** vencido el plazo de 30 días sin resolución, el interesado debe presentar Pronto Despacho. Si transcurren veinte (20) días hábiles adicionales desde dicha presentación sin pronunciamiento, se configura la denegatoria presunta (silencio negativo), quedando expedita la vía judicial. [CONFIRMADO]
- **Secuencia obligatoria ante silencio:** (1) vencimiento de los 30 días para resolver + (2) presentación de Pronto Despacho + (3) vencimiento de 20 días hábiles adicionales sin resolución = denegatoria tácita habilitante de la vía judicial.
- **Efecto sobre el plazo de caducidad judicial:** si la vía se agota por silencio, el plazo de caducidad para interponer la demanda es de tres (3) meses (no 30 días). Ver sección 3.2. [CONFIRMADO]
- **Sin reforma análoga al Decreto 971/2024 nacional:** verificar si San Juan adoptó régimen de silencio positivo de la Ley 27.742 nacional. Si no lo adoptó, aplica silencio negativo del régimen original. [A VERIFICAR]

```
[VERIFICAR RÉGIMEN DE SILENCIO: Ley N° 1995-A San Juan - plazo para operar la denegatoria tácita - secuencia procedimental para configurar el silencio y habilitar la vía judicial]
```

### 2.3 Elementos esenciales del acto administrativo provincial

Aplicar Ley N° 1995-A. La norma sigue la línea clásica de la doctrina administrativa, replicando los requisitos esenciales de validez. [CONFIRMADO]

Elementos:

1. Competencia: órgano facultado en razón de la materia, territorio, tiempo o grado. Irrenunciable e improrrogable.
2. Causa: antecedentes de hecho y de derecho que justifican el dictado del acto.
3. Objeto: certero, física y jurídicamente posible; debe decidir sobre todo lo peticionado.
4. Procedimiento: cumplimiento de los pasos previos esenciales, en especial el dictamen jurídico obligatorio. [CONFIRMADO]
5. Motivación: explicación sucinta de las razones que llevan a la emisión, incluyendo la valoración de la prueba y el derecho. [CONFIRMADO]
6. Finalidad: cumplir con el fin público específico determinado por la norma habilitante, sin incurrir en desviación de poder.

**Advertencia - dictamen jurídico obligatorio:** el procedimiento exige dictamen jurídico como paso previo esencial. La omisión puede configurar vicio de procedimiento susceptible de anular el acto. [CONFIRMADO]

**Régimen de nulidades provincial:** [CONFIRMADO]
- Nulidad absoluta e incurable: el acto es nulo cuando carece de alguno de sus elementos esenciales (competencia sustancial, objeto imposible, ausencia de motivación, falta de procedimiento esencial) o cuando estos están afectados por vicios graves. La Administración tiene la obligación de anularlo de oficio en sede administrativa si el acto es irregular, siempre que no afecte derechos subjetivos consolidados de buena fe.
- Nulidad relativa: el acto es anulable si el vicio no es sustancial, permitiendo su saneamiento, ratificación o confirmación por la autoridad superior.

**Límite a la revocación de oficio:** la obligación de anular de oficio cede cuando el acto irregular ya afectó derechos subjetivos consolidados de buena fe del particular. En ese caso, la invalidación solo procede judicialmente. [CONFIRMADO]

### 2.4 Recursos administrativos provinciales

**Recurso de reconsideración (art. 85 y ss. Ley N° 1995-A):**
- Plazo: diez (10) días hábiles desde la notificación del acto. [CONFIRMADO]
- Ante: mismo órgano emisor.
- Efecto especial - subsidio implícito: la interposición de la reconsideración lleva implícito el recurso jerárquico en subsidio cuando el acto emana de autoridad inferior. [CONFIRMADO]
- Actos del Gobernador o Ministros: la reconsideración es la vía obligatoria y suficiente para agotar la instancia administrativa. No procede jerárquico posterior. [CONFIRMADO]

**Recurso jerárquico:**
- Plazo: diez (10) días hábiles desde la notificación de la denegatoria expresa de la reconsideración. En ese plazo, el recurrente puede también mejorar los fundamentos del recurso jerárquico. [CONFIRMADO - art. 85 y ss. Ley N° 1995-A]
- Ante: superior jerárquico / ministro / gobernador según el caso.
- Plazo para resolver: treinta (30) días desde la interposición o desde la presentación de alegatos si hubo prueba. [CONFIRMADO]
- Vencido sin resolución: presentar Pronto Despacho (ver sección 2.2).
- ¿Agota la vía?: sí. Para actos de autoridades inferiores, el jerárquico es la instancia definitiva. Para actos del Gobernador o Ministros, la reconsideración agota la vía directamente. [CONFIRMADO]

**Recurso de alzada (entes autárquicos):**
- [PENDIENTE: verificar si la Ley N° 1995-A o norma especial de cada ente regula el alzada. Precisar si es obligatorio u optativo y el efecto sobre el plazo de caducidad judicial.]

**Sin reforma análoga a la Ley 27.742 nacional:** verificar si San Juan duplicó los plazos de recursos administrativos. Si no hubo reforma local, aplican los plazos originales de la Ley N° 1995-A. [A VERIFICAR]

**Días hábiles administrativos San Juan:** son los días hábiles del Poder Ejecutivo provincial. Verificar decreto de asueto vigente al momento del acto.

```
[ALERTA PLAZO FATAL: reconsideración - Ley N° 1995-A San Juan, art. 85 y ss. - 10 días hábiles administrativos desde notificación del acto - vencimiento: calcular]
[ALERTA PLAZO FATAL: jerárquico - Ley N° 1995-A San Juan, art. 85 y ss. - 10 días hábiles administrativos desde notificación de la denegatoria de la reconsideración - vencimiento: calcular]
```

### 2.5 Agotamiento de la vía administrativa provincial

- **Regla general:** es presupuesto procesal de admisibilidad obligatorio para habilitar la demanda judicial impugnatoria contra actos de la Administración Central, entes autárquicos y municipios. [CONFIRMADO]
- **Excepciones:** [CONFIRMADO]
  - Vías de hecho administrativas (acciones materiales lesivas del Estado sin sustento en un acto).
  - Cuando la exigencia configure un ritualismo inútil ante una postura pública irreversible del órgano.
  - Cuando se reclamen daños y perjuicios derivados de la actividad lícita o ilícita estatal, según la naturaleza de la pretensión.
- **Fiscalía de Estado / Asesoría General:** [PENDIENTE: verificar denominación exacta, si tiene dictamen obligatorio previo al acto en determinadas materias, y si es parte necesaria en el proceso contencioso.]
- **Municipios:** el agotamiento ante actos municipales es presupuesto de admisibilidad. Verificar ordenanza de procedimiento del municipio antes de encuadrar la secuencia recursiva.

```
[VERIFICAR AGOTAMIENTO DE VÍA: San Juan - Ley N° 1995-A - verificar si se interpusieron los recursos en plazo y si la resolución que agota la vía fue notificada - determinar si aplica alguna excepción]
```

### 2.6 Tabla unificada de plazos - sede administrativa

| Recurso / instituto | Plazo | Cómputo | Norma | Nivel de certeza |
|---------------------|-------|---------|-------|-----------------|
| Reconsideración | 10 días hábiles adm. | desde notificación del acto | Ley N° 1995-A, art. 85 y ss. | CONFIRMADO |
| Jerárquico | 10 días hábiles adm. | desde notificación de la denegatoria de la reconsideración | Ley N° 1995-A, art. 85 y ss. | CONFIRMADO |
| Plazo para resolver recursos | 30 días | desde interposición / desde alegatos si hubo prueba | Ley N° 1995-A | CONFIRMADO |
| Pronto despacho (paso 1 para silencio) | se presenta al vencer los 30 días sin resolución | desde vencimiento del plazo para resolver | Ley N° 1995-A art. 70 | CONFIRMADO |
| Silencio negativo (denegatoria tácita) | 20 días hábiles adicionales tras el pronto despacho | desde presentación del pronto despacho | Ley N° 1995-A art. 70 | CONFIRMADO |
| Alzada (entes autárquicos) | PENDIENTE | desde notificación | Ley N° 1995-A / norma especial | PENDIENTE |

---

## Bloque 3 - Control judicial contencioso administrativo

### 3.1 Código / ley de proceso contencioso administrativo

- **Norma:** Ley N° 2415-O (Código Procesal Civil, Comercial y Minería de San Juan), Título V "Proceso Contencioso Administrativo". Sancionada el 11 de agosto de 2022, publicada el 12 de septiembre de 2022. [CONFIRMADO]
- **Norma anterior derogada:** Ley N° 988-O (derogada por Ley N° 2415-O). No invocar para hechos posteriores al 12 de septiembre de 2022 sin verificar régimen de derecho transitorio. [CONFIRMADO]
- **Ley Orgánica del Poder Judicial:** Ley N° 2352-O - consolidó la reorganización del fuero y el diseño de juzgados unipersonales especializados. [CONFIRMADO]
- **Subsidiariedad:** para lo no previsto en el Título V, aplican las disposiciones generales del mismo Código (Ley N° 2415-O). [CONFIRMADO - verificar si existe remisión expresa al articulado general]
- **Texto vigente:** Boletín Oficial San Juan, publicación del 12/09/2022. Verificar modificaciones posteriores.

### 3.2 Plazo de caducidad para accionar judicialmente

**Este es el dato más crítico del perfil. San Juan tiene dos plazos distintos según cómo se agotó la vía.**

- **Plazo - acto expreso:** treinta (30) días corridos desde el día siguiente a la notificación de la resolución definitiva que agota la vía administrativa. [CONFIRMADO - arts. 727 y ss., Ley N° 2415-O]
- **Plazo - silencio administrativo:** tres (3) meses desde la configuración de la denegatoria tácita (vencimiento de los 20 días hábiles posteriores al Pronto Despacho). [CONFIRMADO - arts. 727 y ss., Ley N° 2415-O]
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa. El vencimiento produce la caducidad automática de la acción; el acto queda firme y consentido.
- **Advertencia crítica - días corridos vs. hábiles judiciales:** el plazo de 30 días para acto expreso es en días **corridos** (no hábiles judiciales). Incluye sábados, domingos y feriados. Diferencia relevante respecto de otros regímenes provinciales y del federal. [CONFIRMADO]
- **¿Declarable de oficio?:** [A VERIFICAR: confirmar en jurisprudencia del Juzgado CA y Cámara Civil San Juan]
- **Procesos especiales:** [PENDIENTE: verificar si el Título V prevé procesos abreviados con plazo distinto.]

```
[ALERTA PLAZO FATAL: San Juan - Ley N° 2415-O, arts. 727 y ss. - ACTO EXPRESO: 30 días CORRIDOS desde notificación del acto que agota la vía - SILENCIO: 3 meses desde configuración de la denegatoria tácita - vencimiento: calcular según modalidad]
```

**Diferencia crítica con el régimen federal:** el plazo federal es de 180 días hábiles judiciales. El plazo de San Juan para acto expreso es de 30 días corridos. No asumir equivalencia.

**Diferencia con Chubut:** Chubut computa 30 días hábiles (no corridos). San Juan computa 30 días corridos para acto expreso y 3 meses para silencio. Verificar la modalidad de agotamiento antes de calcular el vencimiento.

### 3.3 Órganos jurisdiccionales

**Primera instancia:**
- **Tribunal:** Juzgado Contencioso Administrativo de la Primera Circunscripción Judicial, con asiento en la Ciudad de San Juan. Órgano unipersonal especializado. [CONFIRMADO]
- **Competencia:** actos del Poder Ejecutivo Provincial, entes autárquicos provinciales y municipios. [CONFIRMADO]
- **Gestión:** coordinado por la Oficina de Gestión de Audiencias (OGA) para los Juzgados Especializados en lo Comercial y Contencioso Administrativo. El juez conserva exclusivamente la potestad jurisdiccional; la agenda de audiencias la gestiona la OGA. [CONFIRMADO]
- **Organización territorial:** circunscripción con asiento en la Ciudad de San Juan. [PENDIENTE: verificar si hay juzgados en circunscripciones del interior o si toda la materia CA se concentra en la capital.]

**Segunda instancia (alzada):**
- **Tribunal:** Cámara de Apelaciones en lo Civil, Comercial y Minería de San Juan - salas distribuidas. No existe cámara exclusiva CA. [CONFIRMADO]
- **Modalidad:** cuando la Cámara revisa sentencias del Juzgado CA actúa formalmente en materia contencioso administrativa de alzada. [CONFIRMADO]
- **Advertencia:** las salas de la Cámara pueden tener criterios distintos en cuestiones no unificadas por el STJ. Identificar la sala actuante en cada causa.

**Tribunal superior:**
- **Tribunal:** Superior Tribunal de Justicia de San Juan.
- **Acceso:** recurso extraordinario provincial / inconstitucionalidad. [PENDIENTE: precisar denominación exacta del recurso y requisitos de admisibilidad según la Ley N° 2352-O.]
- **Competencia originaria:** el STJ no tiene competencia originaria en materia CA ordinaria; actúa solo por vía extraordinaria. [CONFIRMADO]

### 3.4 Pretensiones admisibles

[PENDIENTE: verificar si el Título V de la Ley N° 2415-O enumera las pretensiones admisibles (anulación, restablecimiento del derecho, declarativa, prestacional, cautelar autónoma) o sigue un sistema abierto. Indicar artículo.]

### 3.5 Medidas cautelares contra el Estado provincial

- **Régimen:** San Juan no tiene ley especial de cautelares contra el Estado equivalente a la Ley N° 26.854 nacional. Aplica el régimen general de la Ley N° 2415-O. La Ley N° 26.854 rige solo contra el Estado nacional; no aplicarla al Estado provincial. [CONFIRMADO]
- **Requisitos:** verosimilitud del derecho + peligro en la demora + contracautela suficiente + ponderación de que la medida no altere grave e irreversiblemente el interés público ni la prestación de un servicio esencial del Estado provincial. [CONFIRMADO]
- **Contracautela:** exigida. [CONFIRMADO - modalidad (real / juratoria): A VERIFICAR]
- **Informe previo del Estado:** [PENDIENTE: verificar si la Ley N° 2415-O o la práctica del Juzgado CA exige informe previo del organismo demandado antes de resolver la cautelar.]
- **Plazo de vigencia:** [PENDIENTE: verificar si existe límite temporal.]

```
[VERIFICAR RÉGIMEN CAUTELAR: San Juan - Ley N° 2415-O régimen general - no asumir equivalencia con Ley N° 26.854 nacional - verificar requisitos ante el Juzgado CA antes de presentar]
```

### 3.6 Amparo provincial

- **Norma:** art. 40 Constitución de la Provincia de San Juan + Ley N° 2415-O (disposiciones procesales integradas en el Código). No existe ley de amparo general autónoma separada del Código. [CONFIRMADO]
- **Intereses difusos / derechos colectivos:** Ley N° 379-E (texto consolidado de la ex Ley N° 6006) - tutela específica de derechos colectivos, medio ambiente y del consumidor. [CONFIRMADO]
- **Articulación supranacional:** art. 43 CN y estándar de tutela efectiva de la CADH, aplicados operativamente por los tribunales en todos los supuestos de urgencia o lesión manifiesta. [CONFIRMADO]
- **Plazo:** [PENDIENTE: verificar plazo en el art. 40 CP San Juan y en la Ley N° 2415-O. Indicar días hábiles/corridos y norma con artículo.]
- **Subsidiariedad:** [PENDIENTE: verificar si rige el principio de no existencia de otro remedio judicial más idóneo.]

```
[ALERTA PLAZO FATAL - AMPARO: art. 40 CP San Juan + Ley N° 2415-O - plazo pendiente de precisar - verificar artículo antes de presentar - vencimiento: calcular]
```

---

## Bloque 4 - Normativa de referencia provincial

### 4.1 Responsabilidad del Estado provincial

- **Ley propia:** no existe. San Juan no sancionó ley de adhesión ni norma espejo a la Ley N° 26.944 nacional. La Ley N° 26.944 rige solo contra el Estado nacional; no aplicarla al Estado provincial. [CONFIRMADO]
- **Régimen aplicable - aplicación pretoriana:** el marco sustancial se extrae directamente de los arts. 8 y 43 de la Constitución de San Juan (responsabilidad directa y objetiva por la actividad lícita e ilícita de sus agentes). Los tribunales locales (STJ San Juan) aplican los principios clásicos del derecho administrativo. [CONFIRMADO]
- **Factores de atribución y requisitos:** falta de servicio como factor de atribución objetivo; daño cierto y mensurable; relación de causalidad adecuada entre el accionar u omisión estatal y el perjuicio invocado. [CONFIRMADO]
- **Régimen de ejecución de sentencias:** las sentencias que imponen al Estado el pago de sumas líquidas tienen efectos declarativos en su faz de ejecución directa. El Poder Ejecutivo incorpora el crédito en el proyecto de Ley de Presupuesto General del ejercicio siguiente al que el fallo quedó firme. Excepción: si vence ese ejercicio sin que se hayan previsto los fondos o efectuado el pago, cesa la protección y procede la ejecución. [CONFIRMADO]
- **Prescripción:** [A VERIFICAR: verificar plazo en jurisprudencia del STJ San Juan. Tener presente el potencial conflicto con el art. 2561 CCCN si el tribunal aplica el estándar civil ante ausencia de ley propia provincial.]

```
[VERIFICAR VIGENCIA: responsabilidad del Estado San Juan - sin ley propia - aplicar arts. 8 y 43 CP San Juan + principios del derecho administrativo + jurisprudencia STJ San Juan - no aplicar Ley N° 26.944 ni CCCN sin verificar criterio del tribunal]
```

### 4.2 Empleo público provincial

- **Estatuto general:** Ley N° 560-E (Estatuto del Empleado Público de la Provincia de San Juan) y sus decretos reglamentarios. [CONFIRMADO]
- **Estabilidad:** garantizada tras el período de prueba de seis (6) meses, conforme al art. 46 de la Constitución Provincial. [CONFIRMADO]
- **Régimen disciplinario general:** el sumario administrativo previo es requisito obligatorio y parte necesaria para la aplicación de sanciones expulsivas (cesantía o exoneración). La omisión del sumario vicia el acto disciplinario. [CONFIRMADO]
- **Escalafón:** [PENDIENTE: decreto o resolución de escalafón general vigente.]
- **Estatutos sectoriales - fragmentación relevante:** [CONFIRMADO - la Ley N° 560-E es el marco general pero los siguientes sectores tienen régimen propio que desplaza al general en disciplina y agotamiento de vía]
  - Personal docente: Ley N° 64-H (Estatuto Docente). Regula de forma exclusiva los ingresos, ascensos y régimen disciplinario del personal dependiente del Ministerio de Educación. [CONFIRMADO]
  - Personal de la salud: Ley N° 2529-A (Carrera Médico-Asistencial) para el personal médico; convenios colectivos sectoriales aplicables al personal no médico de hospitales públicos. [CONFIRMADO]
  - Personal policial: Ley N° 487-R (Personal Policial). Cuenta con consejo de disciplina propio y plazos de descargo sumarial que desplazan la vía común. [CONFIRMADO]
  - Servicio Penitenciario: Ley N° 1222-R. Ídem - consejo de disciplina propio, plazos diferenciados. [CONFIRMADO]
- **Regla operativa:** en toda consulta de empleo público, identificar el organismo y la categoría del agente antes de aplicar la Ley N° 560-E. Si el agente pertenece a educación, salud, policía o penitenciario, ese estatuto sectorial desplaza al general en disciplina, plazos de descargo y forma de agotar la instancia administrativa previa.
- **Negociación colectiva:** [PENDIENTE: verificar si San Juan adhirió a la Ley N° 24.185 o tiene ley propia.]

```
[VERIFICAR ESTATUTO APLICABLE: San Juan - docente (Ley N° 64-H) / médico-asistencial (Ley N° 2529-A) / policial (Ley N° 487-R) / penitenciario (Ley N° 1222-R) / civil general (Ley N° 560-E) - cada estatuto tiene régimen disciplinario y agotamiento de vía propios]
```

### 4.3 Contratación pública provincial

- **Norma general:** Ley N° 2000-A (Ley de Administración Financiera de San Juan). [CONFIRMADO]
- **Reglamento:** Decreto N° 1148-MHF-2020 (Pliego Único de Bases y Condiciones Generales). [CONFIRMADO]
- **Regla general:** Licitación Pública. Las excepciones (Licitación Privada, Concurso de Precios, Contratación Directa) son de interpretación restrictiva y exigen fundamentación explícita basada en montos máximos o urgencia manifiesta debidamente acreditada. [CONFIRMADO]
- **Organismo rector:** Dirección General de Control de Gastos y Contrataciones, dependiente del Ministerio de Economía, Finanzas y Hacienda de la Provincia. Dicta las circulares aclaratorias y aprueba los registros de proveedores. [CONFIRMADO]
- **Plataforma de compras:** compraspublicas.sanjuan.gob.ar - centraliza toda la actividad contractual de bienes y servicios. Publicación de pliegos y adjudicaciones. [CONFIRMADO]
- **Obra pública provincial:** se rige por la Ley N° 118-A (Ley de Obras Públicas de San Juan) y su Decreto Reglamentario N° 1228-P-1979. La redeterminación de precios y el cómputo de mayores costos se auditan bajo este subsistema normativo, con independencia de la Ley N° 2000-A. [CONFIRMADO]
- **Redeterminación de precios:** regulada bajo la Ley N° 118-A y el Decreto N° 1228-P-1979 para contratos de obra pública. [CONFIRMADO]
- **Impugnación de licitaciones:** [PENDIENTE: precisar plazos para impugnar pliegos y preadjudicación según la Ley N° 2000-A, el Decreto N° 1148-MHF-2020 y las circulares de la Dirección General.]

```
[VERIFICAR VIGENCIA: norma de contrataciones San Juan - los montos de licitación y los plazos se actualizan por decreto o resolución con frecuencia - consultar plataforma provincial antes de encuadrar el procedimiento]
```

### 4.4 Organismo de control externo

- **Tribunal de Cuentas:** regulado por el art. 253 de la Constitución Provincial y la Ley N° 260-E. Dicta fallos definitivos de cuenta y de responsabilidad administrativa sobre funcionarios públicos. Su resolución agota la vía administrativa: no se recurre ante el Poder Ejecutivo, sino que se demanda directamente ante el Juzgado Contencioso Administrativo. [CONFIRMADO]
- **Fiscalía de Estado / Asesoría General:** Fiscalía de Estado de la Provincia de San Juan. Base normativa: art. 263 Constitución Provincial + Ley N° 319-E (Ley Orgánica de Fiscalía de Estado). [CONFIRMADO]
  - Misión: defensa del patrimonio provincial, control de legalidad de los actos administrativos y custodia de los bienes fiscales (dominio público y privado).
  - Parte necesaria: por imperativo del art. 263 CP, es parte legítima y necesaria en todos los juicios contencioso administrativos, amparos en que se involucren actos estatales, y en toda controversia judicial o extrajudicial en que se afecten directa o indirectamente los intereses patrimoniales o económicos del Estado Provincial.
  - **Sanción por omisión:** la falta de citación o intervención de la Fiscalía de Estado acarrea la nulidad insanable de las actuaciones. [CONFIRMADO]
- **Control sobre municipios:** [PENDIENTE: verificar si el Tribunal de Cuentas provincial tiene competencia sobre cuentas municipales.]

### 4.5 Defensor del Pueblo provincial

Previsto en el art. 134 de la Constitución de San Juan y normado por la Ley N° 100-E. [CONFIRMADO]
- **Legitimación procesal:** tiene legitimación activa para interponer amparos colectivos o de intereses difusos. [CONFIRMADO]
- **Límite operativo:** sus recomendaciones, informes y dictámenes no vinculan a la Administración Pública ni suspenden los plazos de caducidad para que el particular interponga recursos o demandas. El particular no puede esperar la intervención del Defensor del Pueblo para preservar sus plazos. [CONFIRMADO]

### 4.6 Tabla de responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| Juzgado CA (primera instancia) | Fiscalía de Estado de la Provincia de San Juan (parte necesaria) | Art. 263 CP San Juan; Ley N° 319-E |
| Cámara Civil CA (alzada) | Fiscalía de Estado (parte necesaria) | Art. 263 CP San Juan; Ley N° 319-E |
| STJ (extraordinario) | Fiscalía de Estado (parte necesaria) | Art. 263 CP San Juan; Ley N° 319-E |
| Notificaciones físicas | Av. Libertador Gral. San Martín 750 (Oeste), Centro Cívico, 5° Piso, Núcleo 1, Ciudad de San Juan | Ley N° 319-E |
| Notificaciones electrónicas | Casillero virtual institucional "Fiscalía de Estado de la Provincia" en el sistema de gestión judicial del Poder Judicial de San Juan | Sistema e-judicial San Juan |

**Sanción por omisión de citación:** la falta de citación o intervención de la Fiscalía de Estado acarrea la nulidad insanable de las actuaciones. Citar antes de la primera presentación en todo proceso donde se afecten intereses del Estado provincial. [CONFIRMADO]

```
[VERIFICAR REPRESENTACIÓN PROCESAL: San Juan - identificar el representante del Estado por instancia antes de radicar - las notificaciones deben cursarse en el domicilio procesal correcto]
```

---

## Bloque 5 - Alerta normativa

*Última verificación de esta sección: Mayo 2025. Actualizar cuando cambie alguna de las normas listadas.*

### Plazos de caducidad

Los plazos para impugnar actos administrativos provinciales son breves y fatales. No asumir equivalencia con el régimen federal.

```
[ALERTA PLAZO FATAL: San Juan - Ley N° 2415-O, arts. 727 y ss. - ACTO EXPRESO: 30 días CORRIDOS desde notificación - SILENCIO: 3 meses desde configuración de denegatoria tácita - vencimiento: calcular según modalidad]
```

### Matriz de vigencia por norma

| Norma | Materia | Estado | Última verificación | Fuente |
|-------|---------|--------|--------------------|----|
| Ley N° 1995-A (ex Ley 135-A / Ley 3756) | Procedimiento administrativo provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico de San Juan |
| Ley N° 2415-O, Título V (arts. 727 y ss.) | Proceso contencioso administrativo | CONFIRMADO | Mayo 2025 | BO San Juan 12/09/2022 |
| Ley N° 2352-O | Ley Orgánica del Poder Judicial - fuero CA | CONFIRMADO | Mayo 2025 | Digesto Jurídico de San Juan |
| Ley N° 379-E (ex Ley 6006) | Intereses difusos / derechos colectivos | CONFIRMADO | Mayo 2025 | Digesto Jurídico de San Juan |
| Ley N° 319-E | Fiscalía de Estado | CONFIRMADO | Mayo 2025 | Digesto Jurídico de San Juan |
| Ley N° 560-E | Empleo público provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico de San Juan |
| Ley N° 2000-A + Dec. 1148-MHF-2020 | Contrataciones del Estado provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico de San Juan |
| Responsabilidad del Estado | Sin ley propia - arts. 8 y 43 CP San Juan | CONFIRMADO | Mayo 2025 | Jurisprudencia STJ San Juan |
| Ley N° 988-O | Código CA - DEROGADO por Ley N° 2415-O | DEROGADO | Mayo 2025 | - |

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública:** se actualizan por decreto o resolución - verificar antes de encuadrar el procedimiento de selección.
- **Escala salarial del empleo público provincial:** se modifica por paritarias - no asumir montos sin verificar.
- **Asuetos administrativos provinciales:** afectan el cómputo de plazos en sede administrativa - verificar decreto de asueto vigente al momento del acto.
- **Feria judicial:** no afecta el plazo de caducidad de 30 días para acto expreso (son días corridos, no hábiles judiciales). Sí puede afectar el cómputo de los 3 meses por silencio si el tribunal los interpreta en días corridos. Verificar criterio del Juzgado CA.

```
[VERIFICAR VIGENCIA: norma provincial San Juan - consultar Digesto Jurídico de San Juan y Boletín Oficial antes de aplicar]
```

---

## Bloque 6 - Fuentes primarias

- **Boletín Oficial:** [PENDIENTE: confirmar URL vigente del Boletín Oficial de San Juan]
- **Digesto / Portal jurídico provincial:** [PENDIENTE: confirmar URL del Digesto Jurídico de San Juan]
- **Poder Judicial provincial:** https://www.jussanjuan.gov.ar [A VERIFICAR: confirmar URL vigente]
- **Fiscalía de Estado:** [PENDIENTE: verificar URL si publica dictámenes]
- **Organismo de compras:** [PENDIENTE: verificar URL de la plataforma de contrataciones]

---

## Bloque 7 - Reglas de citación

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para este fuero:

**Jurisprudencia del Juzgado CA:** nunca citar expediente o carátula sin material aportado. Es juzgado unipersonal; no hay divergencias internas. Usar:
```
[INSERTAR FALLO VERIFICADO: Juzgado Contencioso Administrativo San Juan - Primera Circunscripción Judicial - doctrina requerida]
```

**Jurisprudencia de la Cámara (alzada CA):** identificar la sala actuante. Las salas pueden tener criterios distintos en cuestiones no unificadas por el STJ. Usar:
```
[INSERTAR FALLO VERIFICADO: Cámara de Apelaciones Civil, Comercial y Minería San Juan - sala [X] - en materia CA - doctrina requerida]
```

**Actos administrativos provinciales:** no asumir el contenido de resoluciones, disposiciones o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos provinciales:** no transpolar plazos del régimen federal. En San Juan, el plazo de caducidad difiere según cómo se agotó la vía. Usar:
```
[ALERTA PLAZO FATAL: Ley N° 2415-O, arts. 727 y ss. San Juan - ACTO EXPRESO: 30 días CORRIDOS - SILENCIO: 3 meses - desde el hito que corresponda - vencimiento: calcular según modalidad]
```

**Dictámenes de Fiscalía de Estado:** no asumir su contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: dictamen de Fiscalía de Estado San Juan no aportado - aportar texto del dictamen si fue emitido en el expediente]
```

---

## Bloque 8 - Lógica de análisis por institución

Las instituciones que siguen tienen base en el derecho administrativo general argentino. Donde la ley o jurisprudencia provincial difiera del régimen nacional, prevalece la regla local indicada en los bloques anteriores.

### Acto administrativo - elementos y vicios

Aplicar Ley N° 1995-A. Elementos según sección 2.3.

Preguntas de diagnóstico:
1. ¿Qué acto se impugna? ¿Es definitivo o de mero trámite? ¿Es del Estado provincial, de un municipio o de un organismo federal?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo del plazo de caducidad - 30 días hábiles judiciales)
3. ¿Qué elementos del acto se cuestionan?
4. ¿Hay expediente administrativo que lo respalda? ¿El abogado lo tiene o hay que pedirlo por vista?
5. ¿Se recurrió en sede administrativa? ¿Qué recursos se interpusieron y en qué plazo?
6. ¿Intervino Fiscalía de Estado cuando era obligatorio?

### Recursos administrativos provinciales

Aplicar el esquema de la sección 2.4. Verificar siempre:
- Plazo desde la notificación (hábiles administrativos provinciales, no judiciales)
- Órgano ante el que se interpone
- Si el silencio opera por vencimiento del plazo para resolver y cuándo habilita la vía judicial
- Si el recurso de alzada ante entes autárquicos es obligatorio u optativo

```
[ALERTA PLAZO FATAL: recurso administrativo San Juan - Ley N° 1995-A - plazo a precisar con artículo - días hábiles administrativos desde notificación - vencimiento: calcular]
```

### Agotamiento de la vía administrativa provincial

Antes de analizar cualquier acción judicial:
1. Verificar si la vía está agotada (sección 2.5)
2. Si no lo está, determinar si aplica alguna excepción (vía de hecho, ritualismo inútil, pretensión resarcitoria)
3. Verificar si la Fiscalía de Estado requiere intervención previa
4. Alertar sobre el plazo de caducidad: 30 días hábiles judiciales desde la notificación del acto que agota la vía

### Responsabilidad del Estado provincial

San Juan no tiene ley propia de responsabilidad. Aplicar arts. 8 y 43 CP San Juan + principios del derecho administrativo + jurisprudencia del STJ San Juan. Alertas:
- No aplicar la Ley N° 26.944 nacional ni el CCCN como régimen sustantivo sin verificar criterio del STJ.
- Falta de servicio como factor de atribución objetivo; daño cierto; causalidad adecuada.
- Las sentencias de condena dineraria tienen carácter declarativo. El Estado incorpora el crédito en el presupuesto del ejercicio siguiente. Excepción: si vence ese ejercicio sin pago ni previsión, procede la ejecución.
- Prescripción: sin ley propia, el STJ puede aplicar el estándar del art. 2561 CCCN. Verificar jurisprudencia reciente antes de analizar la viabilidad de la acción.

### Empleo público provincial

Aplicar el estatuto de la sección 4.2. Verificar siempre:
- Identificar el sector antes de aplicar el estatuto general: verificar si existe estatuto sectorial (docente, policial, sanitario, u otro)
- Situación de revista del agente (planta permanente con estabilidad / sin estabilidad / contratado / transitorio / gabinete)
- Si hubo sumario con garantías de debido proceso conforme el régimen disciplinario del estatuto aplicable
- Si la sanción expulsiva encuadra en alguna causal taxativa del estatuto aplicable
- Si el agotamiento de la vía sigue el estatuto general o el régimen del estatuto sectorial

### Contratación pública provincial

Aplicar la normativa de la sección 4.3. Verificar siempre:
- Montos vigentes para encuadrar el tipo de procedimiento
- Plazos de impugnación de pliegos y preadjudicación según norma local
- Si la redeterminación de precios aplica y bajo qué régimen
- Si el contrato es de obra pública: verificar si aplica ley provincial propia o Ley N° 13.064 nacional

---

## Bloque 9 - Instrucciones operativas

### Alerta crítica - plazo de caducidad para accionar judicialmente

**Este es el primer paso en toda consulta que involucre una acción judicial contra el Estado provincial de San Juan.**

El plazo para demandar es un plazo de caducidad, no de prescripción:
- No se suspende ni interrumpe por las mismas causales que la prescripción
- Vencido el plazo, la acción caduca automáticamente; el acto queda firme y consentido
- La caducidad puede declararse de oficio

**Plazo provincial:** dos regímenes según modalidad de agotamiento - [CONFIRMADO - arts. 727 y ss., Ley N° 2415-O]
- Acto expreso: treinta (30) días **corridos** desde notificación del acto que agotó la vía.
- Silencio: tres (3) meses desde la configuración de la denegatoria tácita.

Antes de analizar cualquier otra cuestión en una consulta sobre acción contenciosa provincial, emitir:
```
[ALERTA PLAZO FATAL: San Juan - Ley N° 2415-O, arts. 727 y ss. - ACTO EXPRESO: 30 días CORRIDOS - SILENCIO: 3 meses - verificar modalidad de agotamiento - vencimiento: calcular]
```

**Diferencia con el régimen federal:** el plazo federal es de 180 días hábiles judiciales. El plazo de San Juan para acto expreso es de 30 días corridos (incluye fines de semana y feriados). No asumir equivalencia.

**Diferencia con Chubut:** Chubut computa 30 días hábiles. San Juan computa 30 días corridos para acto expreso. Verificar la modalidad de agotamiento antes de calcular.

---

- Identificar si el acto es del Estado provincial, de un municipio o de un organismo federal antes de aplicar este perfil o el nacional.
- El proceso CA está integrado en el Título V (arts. 727 y ss.) de la Ley N° 2415-O (vigente desde 12/09/2022). No invocar la Ley N° 988-O para hechos posteriores a esa fecha.
- Primera instancia: Juzgado CA unipersonal + OGA. Alzada: Cámara Civil salas distribuidas. STJ solo por vía extraordinaria.
- En actos mixtos: aplicar cada régimen al acto correspondiente por separado.
- Verificar agotamiento de la vía administrativa provincial antes de analizar la acción judicial.
- Plazos de recursos en sede administrativa son hábiles administrativos, no judiciales. Reconsideración: 10 días. Jerárquico: 10 días desde denegatoria.
- Silencio: requiere (1) vencimiento de 30 días para resolver + (2) Pronto Despacho + (3) 20 días hábiles adicionales sin resolución. Secuencia obligatoria.
- Plazo de caducidad: ACTO EXPRESO = 30 días corridos. SILENCIO = 3 meses. Verificar modalidad antes de calcular.
- Fiscalía de Estado es parte necesaria en todo proceso. Su omisión produce nulidad insanable. Citar antes de la primera presentación.
- En responsabilidad del Estado: sin ley propia; aplicar arts. 8 y 43 CP San Juan + principios del derecho administrativo. Sentencias declarativas con excepción por vencimiento de ejercicio sin pago.
- Todo escrito provincial cierra con "Estado del escrito" estándar más: fuero y régimen aplicado (Juzgado CA San Juan + Ley N° 2415-O, arts. 727 y ss.), estado del agotamiento de la vía, **plazo de caducidad provincial (30 días corridos acto expreso / 3 meses silencio - verificado / pendiente / vencido)**, intervención de Fiscalía de Estado (sí - parte necesaria / citada / a citar - omisión: nulidad insanable), sala de Cámara si está en alzada, próximo plazo procesal si lo hay, régimen de responsabilidad (arts. 8 y 43 CP San Juan + jurisprudencia STJ / CCCN solo si es contratista privado), régimen de ejecución (declarativa - presupuesto ejercicio siguiente / excepción por vencimiento sin pago).

---

*Última actualización: Mayo 2025*
*Normativa base: Ley N° 1995-A (ex Ley 135-A / 3756, consolidada por Ley N° 2504-E) - procedimiento administrativo; Ley N° 2415-O, Título V arts. 727 y ss. - proceso CA (vigente desde 12/09/2022, deroga Ley N° 988-O); Ley N° 2352-O - Ley Orgánica del Poder Judicial; Ley N° 319-E + art. 263 CP - Fiscalía de Estado; Ley N° 379-E (ex Ley 6006) - intereses difusos; Ley N° 560-E - empleo público; Ley N° 2000-A + Decreto 1148-MHF-2020 - contrataciones; Constitución Provincial arts. 8, 40, 43 y 263.*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
