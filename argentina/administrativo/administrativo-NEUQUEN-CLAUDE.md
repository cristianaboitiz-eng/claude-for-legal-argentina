# Perfil de práctica · Derecho administrativo · Provincia de Neuquén

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Neuquén.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.
>
> **Estado del perfil:** operativo — datos procesales clave confirmados. Fuero con Colegios de Jueces operativo (Ley 2979).

---

## Sistema de etiquetas

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de mayo 2026.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** Provincia de Neuquén

**FUERO_HABITUAL:** [COMPLETAR: Ej. "Juzgado del Fuero Procesal Administrativo N° X, Neuquén Capital" / "Colegio de Jueces del Fuero Procesal Administrativo, Neuquén Capital". La Ley 2979 creó el Fuero Procesal Administrativo con Colegios de Jueces. La Sala Procesal Administrativa del TSJ actúa como alzada y como tribunal de instancia única en causas con decreto de autos firme anterior a la puesta en funcionamiento de los Colegios. Verificar el Juzgado/Colegio competente territorialmente antes de radicar.]

**AREAS_PRACTICA:** [COMPLETAR: Ej. "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, contratación pública, EPEN, organismos municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: Ej. "Ministerio de Salud Neuquén, IPROSS, Municipalidad de Neuquén, DPR Neuquén, EPEN".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Neuquén: procedimiento administrativo ante la Administración provincial y municipal (Ley 1284), recursos administrativos en sede provincial, acción procesal administrativa ante el Fuero Procesal Administrativo con Colegios de Jueces (Ley 2979) y la Sala Procesal Administrativa del TSJ como alzada (Ley 1305 con modificaciones de la Ley 2979), responsabilidad del Estado, empleo público y contratación pública.

**Estructura judicial [CONFIRMADO]:**
- **Primera instancia:** Colegios de Jueces del Fuero Procesal Administrativo (Ley 2979, operativos). Entienden en las causas iniciadas desde su puesta en funcionamiento y en las que tramitaban ante la Sala Procesal Administrativa del TSJ sin decreto de autos firme.
- **Alzada:** Sala Procesal Administrativa del Tribunal Superior de Justicia de Neuquén (TSJ Neuquén). También mantiene competencia de instancia única en causas con decreto de autos firme anterior a la Ley 2979.
- **Recursos contra sentencia:** TSJ Neuquén (casación/inconstitucionalidad, recurso extraordinario federal para la CSJN).

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Neuquén (ARCA/ex AFIP, ANSES), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal neuquina, aplica este perfil.

**Tercer nivel - organismos municipales [CONFIRMADO]:** los actos municipales son impugnables ante el Fuero Procesal Administrativo. La constitución provincial (art. 238) exige la previa denegación o retardo de la autoridad administrativa. Verificar si el municipio tiene ordenanza de procedimiento propio.

---

## Bloque 2 - Normas base

### 2.1 Procedimiento administrativo - Ley 1284

**[CONFIRMADO]** Norma principal: Ley 1284 (Ley de Procedimiento Administrativo de la Provincia de Neuquén). Regula la actividad administrativa provincial y municipal.

**[CONFIRMADO]** La Ley 1284 establece la estructura de recursos administrativos, los elementos del acto, la ejecutoriedad y el silencio.

**Texto vigente:** https://dprneuquen.gob.ar/wp-content/uploads/2019/05/Ley-de-Procedimiento-Adm.-Nqn-1284.pdf — verificar modificaciones posteriores.

**Articulado clave:** arts. 171 y ss. (agotamiento de la vía, denegación tácita), arts. 188 y ss. (recursos).

```
[VERIFICAR VIGENCIA: Ley 1284 LPA Neuquén - consultar portal oficial de Neuquén antes de aplicar - verificar modificaciones posteriores a mayo 2026]
```

### 2.2 Proceso administrativo - Ley 1305 (mod. Ley 2979)

**[CONFIRMADO]** Norma principal: Ley 1305 (Código de Procedimiento Procesal Administrativo de Neuquén), modificada parcialmente por Ley 2979 (que derogó los arts. 62 y 79 y el Capítulo VII del Título Cuarto de la Ley 1305, y creó el nuevo fuero).

**[CONFIRMADO]** Subsidiariedad (art. 20 Ley 1305): en materia de intervención de terceros, plazos y notificaciones, aplica el Código de Procedimientos en lo Civil y Comercial supletoriamente.

**Texto vigente:** Ley 1305 disponible en https://docs.argentina.justia.com/provinciales/neuquen/codigos/ley-1305.pdf — verificar modificaciones de la Ley 2979.

### 2.3 Silencio administrativo y denegación tácita

**[CONFIRMADO]** El agotamiento de la vía por denegación tácita se rige por los arts. 171 y 188-190 de la Ley 1284. Cuando la vía se agota por resolución tácita, la acción puede interponerse **en cualquier momento antes de la prescripción** (art. 10 in fine Ley 1305).

Sin reforma análoga al Dec 971/2024 nacional: Neuquén no adoptó el régimen de silencio positivo de la Ley 27.742 nacional.

### 2.4 Plazo de caducidad para accionar judicialmente

**[CONFIRMADO — DATO MÁS CRÍTICO]**

- **Plazo general:** **30 días corridos** desde el día siguiente al de la notificación de la decisión que agota la vía (art. 10 Ley 1305).
- **Naturaleza:** caducidad — perentoria. No se suspende por feria judicial.
- **Inhábil al vencimiento:** si el día 30 cae en día inhábil, el plazo se prorroga al primer día hábil subsiguiente (jurisprudencia pacífica del TSJ Neuquén).
- **Resolución tácita (silencio):** la acción puede interponerse en cualquier momento antes de la prescripción (art. 10 Ley 1305). No hay plazo de caducidad.
- **¿Declarable de oficio?:** sí.

```
[ALERTA PLAZO FATAL: art. 10 Ley 1305 CPA Neuquén - 30 días CORRIDOS - desde notificación de la decisión que agota la vía - no se suspende por feria judicial - si vence en inhábil: prorroga al primer hábil subsiguiente - EXCEPCIÓN: vía agotada por silencio → sin plazo de caducidad (antes de la prescripción) - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes:**

| Régimen | Plazo | Tipo | Excepción por silencio |
|---------|-------|------|----------------------|
| **Neuquén** | **30 días** | **Corridos** (sin suspensión por feria; si vence en inhábil: prorroga al primer hábil) | Sin plazo de caducidad si vía agotada por silencio |
| **Río Negro** | **30 días** | Hábiles | Sin caducidad si silencio (antes prescripción) |
| PBA | 90 días | Hábiles judiciales | No análoga |
| CABA | 90 días | Hábiles judiciales | No análoga |
| Tucumán | 90 días | Hábiles judiciales | No análoga |
| Corrientes | 60 días | Hábiles judiciales | No análoga |
| Misiones | 60 días | Corridos (sin ferias) | No análoga |
| Mendoza | 30 días | Corridos | No análoga |
| Salta | 30 días | Hábiles judiciales | No análoga |
| Córdoba | 30 días | Hábiles judiciales | No análoga |
| Santa Fe | 30 días | A verificar | No análoga |
| Entre Ríos | 1 año | Corridos | No análoga |
| Federal (post-9-jul-2024) | 180 días | Hábiles judiciales | No análoga |

```
[CONFIRMADO: art. 10 Ley 1305 Neuquén - 30 días corridos - jurisprudencia pacífica de la Sala Procesal Administrativa del TSJ Neuquén - no se suspende por feria - si vence en inhábil prorroga al primer hábil subsiguiente]
```

### 2.5 Recursos administrativos (Ley 1284)

**[A VERIFICAR en cuanto a plazos específicos]** La Ley 1284 regula los recursos administrativos. La cadena recursiva sigue la estructura general del derecho administrativo argentino: recurso ante el órgano emisor → jerárquico ante el superior hasta el Gobernador o autoridad máxima.

**[CONFIRMADO]** Cuando la vía se agota por decisión expresa, hay plazo de caducidad (30 días, art. 10 Ley 1305). Cuando se agota por silencio, no hay plazo de caducidad.

```
[VERIFICAR PLAZOS RECURSOS ADMINISTRATIVOS NEUQUÉN: Ley 1284 arts. 188 y ss. - identificar plazos de revocatoria y jerárquico antes de operar la cadena recursiva]
```

### 2.6 Tabla unificada de plazos

| Recurso / instituto | Plazo | Tipo | Norma | Estado |
|---------------------|-------|------|-------|--------|
| Recursos administrativos | [A VERIFICAR] | Hábiles administrativos | Ley 1284 arts. 188 y ss. | [A VERIFICAR] |
| Acción (vía agotada por resolución expresa) | 30 días | **Corridos** (sin feria; si vence en inhábil prorroga al primer hábil) | Ley 1305 art. 10 | [CONFIRMADO] |
| Acción (vía agotada por silencio) | Sin plazo de caducidad (antes de la prescripción) | - | Ley 1305 art. 10 | [CONFIRMADO] |
| Traslado de demanda (trámite ordinario) | 15 días | - | Ley 1305 art. 46 | [CONFIRMADO] |
| Caducidad de instancia | 6 meses | - | Ley 1305 art. 31 | [CONFIRMADO] |
| Caducidad instancia (recursos contra sentencia) | 3 meses | - | Ley 1305 art. 32 | [CONFIRMADO] |
| Suspensión previa: caducidad si no hay acción | En plazo del art. 10 (automáticamente) | - | Ley 1305 art. 26 | [CONFIRMADO] |
| Cautelar (traslado a demandada) | 5 días | - | Ley 1305 art. 21 | [CONFIRMADO] |

### 2.7 Agotamiento de la vía administrativa

**[CONFIRMADO]** Requisito previo: resolución expresa o tácita que agote la vía administrativa conforme a los arts. 171, 188, 189 y 190 de la Ley 1284 (art. 6 Ley 1305).

**[CONFIRMADO]** Límite de pretensiones (art. 8 Ley 1305): las acciones deben limitarse a las cuestiones previamente debatidas en las reclamaciones o recursos administrativos.

```
[VERIFICAR AGOTAMIENTO DE VÍA NEUQUÉN: Ley 1284 arts. 171, 188-190 + Ley 1305 art. 6 - verificar cadena recursiva completa y notificación de la decisión que agota la vía - determinar si se agotó por resolución expresa (plazo 30 días) o por silencio (sin plazo de caducidad)]
```

### 2.8 Suspensión cautelar (arts. 21-26 Ley 1305)

**[CONFIRMADO]** Puede solicitarse antes, simultánea o posteriormente a la acción (art. 21).

**[CONFIRMADO]** Trámite (art. 21): traslado por 5 días a la demandada; el tribunal resuelve en 5 días. Por cuerda separada.

**[CONFIRMADO]** Procede cuando "prima facie" la disposición es nula o puede producir daño grave si aparece como anulable (art. 22).

**[CONFIRMADO]** No procede (art. 23):**
- (a) Demolición/clausura por seguridad/moralidad/higiene pública con dictamen técnico y jurídico.
- **(b) Cesantías o exoneraciones de agentes públicos.**

**[CONFIRMADO]** Caducidad de la cautelar (art. 26): la suspensión dispuesta antes de la acción caduca automáticamente si ésta no se deduce en plazo (en el plazo del art. 10).

```
[ALERTA CAUTELAR NEUQUÉN: suspensión solicitada antes de la acción caduca si la acción no se interpone en el plazo del art. 10 (30 días desde notificación o antes de la prescripción si fue por silencio)]
[ATENCIÓN: no procede la suspensión en cesantías/exoneraciones de agentes públicos - art. 23 inc. b Ley 1305]
```

### 2.9 Tabla de responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| Colegios de Jueces del Fuero Procesal Administrativo | Fiscal de Estado de Neuquén | Constitución Neuquén art. 252 |
| Sala Procesal Administrativa del TSJ (alzada) | Fiscal de Estado de Neuquén | Constitución Neuquén art. 252 |
| Conflictos de competencia | Fiscal del TSJ (previo dictamen) | Ley 1305 art. 4 |

**[CONFIRMADO]** La Fiscalía de Estado es **parte necesaria y legítima** en todo proceso en el que se controviertan intereses de la Provincia y sus entes descentralizados (art. 252 Constitución Neuquén).

**[CONFIRMADO] Notificación — régimen digital:**
- **Domicilio físico de reserva:** Fiscalía de Estado de la Provincia de Neuquén, Santiago del Estero 666, Ciudad de Neuquén. Válido para actos que requieran formalidad en papel.
- **Regla vigente:** el traslado de las demandas contencioso administrativas contra la Provincia se realiza de forma automatizada al domicilio electrónico institucional de la Fiscalía de Estado en el **Sistema Alberdi** (sistema de gestión de causas del TSJ Neuquén). La Fiscalía se considera formalmente notificada cuando la cédula digital ingresa a su casillero institucional.
- **Nulidad por omisión:** omitir la notificación al domicilio electrónico validado de la Fiscalía de Estado, o dirigirla únicamente al ministerio u organismo descentralizado que dictó el acto, provoca la **nulidad absoluta** de la notificación por violación del art. 252 Constitución Neuquén.

```
[CONFIRMADO: Fiscalía de Estado Neuquén — parte necesaria en todo proceso contra la Provincia (art. 252 Const. Neuquén) — sede física de reserva: Santiago del Estero 666, Neuquén Capital — notificación digital en Sistema Alberdi / casillero institucional del TSJ — omisión genera nulidad absoluta de la notificación]
```

### 2.10 Responsabilidad del Estado provincial

**[CONFIRMADO]** Sin ley propia equivalente a Ley 26.944 nacional. La Ley 26.944 no aplica al Estado provincial neuquino.

**[CONFIRMADO]** La pretensión resarcitoria es admisible ante el Fuero Procesal Administrativo cuando el daño deriva de incumplimiento o vinculación especial de derecho público contractual o reglamentaria (art. 2 inc. a.4 Ley 1305).

**[CONFIRMADO]** La Administración puede deducir acción procesal administrativa para la ejecución de actos firmes o el ejercicio de prerrogativas (art. 2 inc. b Ley 1305).

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD NEUQUÉN: sin ley propia - principios generales + jurisprudencia TSJ Neuquén Sala Procesal Administrativa - no aplicar Ley 26.944 ni CCCN sin verificar criterio del fuero]
```

### 2.11 Empleo público Neuquén

**[CONFIRMADO]** Estatuto general: **Ley 2265** (Estatuto del Personal de la Administración Pública Provincial de Neuquén). Rige la Administración centralizada y descentralizada.

**Nota operativa:** la provincia tiene alta tasa de sindicalización con Convenios Colectivos de Trabajo (CCT) sectoriales ratificados por leyes específicas (Salud, Educación, Escalafón General, viales). En la práctica judicial neuquina, las demandas por empleo público (sanciones, encuadramientos, licencias) se fundan primero en el CCT sectorial aplicable y, supletoriamente, en la Ley 2265. Identificar el CCT antes de encuadrar la pretensión.

**Nota procesal:** el plazo para impugnar judicialmente un acto de cesantía o sanción corre bajo los términos de la Ley 1284 (LPA Neuquén): 30 días corridos desde la notificación del acto que agota la vía (art. 10 Ley 1305).

**[CONFIRMADO]** Los actos sobre retribuciones, jubilaciones y pensiones de agentes estatales son impugnables ante el Fuero Procesal Administrativo (art. 2 inc. a.3 Ley 1305), salvo relaciones de derecho del trabajo.

**[CONFIRMADO]** No procede la suspensión cautelar en cesantías/exoneraciones (art. 23 inc. b Ley 1305). Informar al cliente antes de iniciar la acción.

### 2.12 Contratación pública Neuquén

**[CONFIRMADO]** Norma marco: **Ley 2141** (Ley de Administración Financiera y Control de la Provincia de Neuquén), Capítulo de Contrataciones. Decreto reglamentario principal: **Decreto 2758/95** (Reglamento de Contrataciones) con sucesivas modificaciones en sus anexos de escalas.

**[CONFIRMADO]** Sistema de montos: Neuquén opera mediante **Unidades de Compra (UC)** actualizables. Los topes para Licitación Pública, Licitación Privada, Concurso de Precios y Contratación Directa se expresan en UC. Las escalas no se modifican por ley sino por Decreto del PE (a propuesta del Ministerio de Economía, Producción e Industria) o Resolución de la Contaduría General de la Provincia. Para buscar la actualización vigente en el Boletín Oficial: «actualización de montos artículo 64 Ley 2141» o «valor de la unidad de compra Contaduría General».

```
[VERIFICAR MONTOS UC: Ley 2141 Neuquén + Decreto 2758/95 - los topes de contratación se actualizan por Decreto del PE o Resolución de la Contaduría General - consultar https://boficial.neuquen.gov.ar con los términos indicados]
```

---

## Bloque 3 - Alertas críticas

### Alerta 1 - Plazo: 30 días, con excepción crucial por silencio

**[CONFIRMADO]** Dos regímenes coexisten según cómo se agotó la vía:
- **Resolución expresa:** **30 días corridos** desde el día siguiente a la notificación. Caducidad perentoria. No se suspende por feria judicial. Si el día 30 cae en inhábil, prorroga al primer hábil subsiguiente. (Jurisprudencia pacífica de la Sala Procesal Administrativa del TSJ Neuquén.)
- **Silencio (denegación tácita):** sin plazo de caducidad; la acción puede interponerse en cualquier momento antes de la prescripción.

Esta dualidad es característica del sistema neuquino y no tiene equivalente exacto en PBA, Córdoba ni Santa Fe. Determinar cómo se agotó la vía antes de computar cualquier plazo.

```
[ALERTA PLAZO FATAL: art. 10 Ley 1305 CPA Neuquén - vía agotada por resolución EXPRESA: 30 días CORRIDOS desde notificación - no se suspende por feria - si vence en inhábil: prorroga al primer hábil - vía agotada por SILENCIO: sin plazo de caducidad (antes de la prescripción) - determinar primero cómo se agotó la vía]
```

### Alerta 2 - Fuero con Colegios de Jueces (Ley 2979) en funcionamiento

**[CONFIRMADO]** La Ley 2979 creó el Fuero Procesal Administrativo con Colegios de Jueces. El presupuesto 2024 y los concursos activos en 2026 confirman que el fuero está en pleno funcionamiento. Antes de radicar, identificar el Colegio de Jueces competente territorialmente.

### Alerta 3 - No procede cautelar en cesantías/exoneraciones

**[CONFIRMADO]** Art. 23 inc. b Ley 1305. Informar al cliente antes de iniciar la acción en empleo público.

---

## Bloque 4 - Checklists operativos

### Checklist: acto administrativo

1. ¿El acto es del Estado provincial, de un municipio o de un organismo federal?
2. ¿El acto fue notificado? ¿En qué fecha?
3. ¿La vía se agotó por resolución expresa (plazo 30 días) o por silencio (sin plazo de caducidad)?
4. ¿Hay expediente administrativo? ¿El abogado lo tiene?
5. ¿Se agotaron los recursos de la Ley 1284?
6. ¿Las pretensiones coinciden con lo planteado en sede administrativa? (art. 8 Ley 1305)
7. ¿La pretensión resarcitoria deriva de vinculación especial de derecho público? (verificar competencia del Fuero)

### Checklist: acción judicial

1. Determinar cómo se agotó la vía (resolución expresa vs. silencio).
2. Si fue por resolución expresa: calcular **30 días corridos** desde el día siguiente a la notificación (no se suspende por feria; si vence en inhábil: primer hábil subsiguiente).
3. Si fue por silencio: la acción puede interponerse en cualquier momento antes de la prescripción.
4. Identificar el Colegio de Jueces competente territorialmente.
5. Si se solicitó cautelar previa: recordar que caduca si la acción no se interpone en plazo (art. 26).
6. Si involucra cesantía/exoneración: no pedir cautelar (art. 23 inc. b).
7. En materia tributaria: verificar pago previo (art. 7 Ley 1305).

### Checklist: responsabilidad del Estado

1. Verificar si el daño deriva de vinculación especial de derecho público (competencia del Fuero).
2. No aplicar Ley 26.944 ni CCCN sin verificar criterio del TSJ Neuquén.
3. La pretensión resarcitoria puede acumularse a la anulatoria.

### Checklist: empleo público

1. Identificar estatuto aplicable (general o sectorial).
2. Situación de revista del agente.
3. ¿Hubo sumario con garantías de debido proceso?
4. Si la sanción es cesantía/exoneración: **no procede cautelar** (art. 23 inc. b). Informar al cliente.

---

## Fuentes primarias

- **Boletín Oficial Neuquén:** https://boficial.neuquen.gov.ar
- **Poder Judicial de Neuquén:** https://www.jusneuquen.gov.ar
- **Legislatura de Neuquén (leyes):** https://www.legislaturaneuquen.gob.ar
- **DPR Neuquén (Ley 1284):** https://dprneuquen.gob.ar

---

## Reglas de citación - administrativo Neuquén

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente.

**Jurisprudencia:** verificar si el fallo es de la Sala Procesal Administrativa del TSJ en instancia única (pre-Ley 2979) o del Colegio de Jueces / Sala como alzada (post-Ley 2979). Usar:
```
[INSERTAR FALLO VERIFICADO: TSJ Neuquén Sala Procesal Administrativa / Colegio de Jueces Fuero Procesal Administrativo - doctrina requerida - verificar si es pre o post Ley 2979]
```

**Plazos:** no transpolar plazos de otros regímenes. Usar:
```
[ALERTA PLAZO FATAL: art. 10 Ley 1305 CPA Neuquén - vía agotada por resolución expresa: 30 días / vía agotada por silencio: sin plazo de caducidad - vencimiento: calcular]
```

---

*Última actualización: mayo 2026*
*Normativa base: Ley 1284 LPA Neuquén, Ley 1305 CPA Neuquén (mod. por Ley 2979), Ley 2979 (Fuero Procesal Administrativo - Colegios de Jueces), Constitución de Neuquén arts. 238 y 252*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
