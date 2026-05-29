# Perfil de práctica · Derecho administrativo · Provincia de Misiones

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Misiones.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.
>
> **Estado del perfil:** operativo — datos procesales clave confirmados. Las normas con etiqueta [A VERIFICAR] requieren confirmación antes de usar en el caso concreto.

---

## Sistema de etiquetas

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de mayo 2026.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse en el Boletín Oficial de Misiones antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** Provincia de Misiones

**FUERO_HABITUAL:** Superior Tribunal de Justicia de Misiones (STJM) — competencia originaria, exclusiva y en instancia única para todas las acciones contencioso administrativas (Ley I-95, art. 1 y 2). No hay juzgados de primera instancia ni cámaras CA: el STJM es el único tribunal, en única instancia ordinaria.

**AREAS_PRACTICA:** [COMPLETAR: Ej. "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, contratación pública, PAMI, organismos municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: Ej. "Ministerio de Salud Pública Misiones, Dirección General de Educación, IPRODHA, Municipalidad de Posadas".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Misiones: procedimiento administrativo ante la Administración provincial y municipal (Ley I-89, ex Ley 2970), recursos administrativos en sede provincial, acción contencioso administrativa ante el Superior Tribunal de Justicia en instancia única (Ley I-95, ex Ley 3064, texto consolidado por Ley IV-70 - Digesto 2015), responsabilidad del Estado provincial, empleo público y contratación pública.

**Particularidad estructural central — única instancia en el STJM [CONFIRMADO]:** al igual que Mendoza (antes de su reforma), en Misiones no existe un fuero CA de primera instancia. El **STJ de Misiones (STJM)** actúa en competencia originaria, exclusiva y en instancia única para todas las acciones CA (Ley I-95, arts. 1 y 2). No hay apelación ordinaria local de la sentencia definitiva.

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Misiones (ARCA/ex AFIP, ANSES), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal misionera, aplica este perfil.

**Tercer nivel - organismos municipales [CONFIRMADO]:** los Juzgados de Primera Instancia CA (cuando existan) tienen competencia en procesos contra Municipalidades (Ley I-95). El agotamiento de la vía ante organismos municipales puede tener regulación diferenciada: verificar si el municipio tiene ordenanza de procedimiento propia.

---

## Bloque 2 - Normas base

### 2.1 Procedimiento administrativo - Ley I-89 (ex Ley 2970)

**[CONFIRMADO]** Norma principal: Ley I-89 (ex Ley 2970, Ley de Procedimiento Administrativo de la Provincia de Misiones). Texto consolidado en el Digesto Jurídico de Misiones (Ley IV-70, B.O. 13-06-2016).

**Texto vigente:** https://digestomisiones.gob.ar — consultar texto actualizado.

```
[VERIFICAR VIGENCIA: Ley I-89 (ex Ley 2970) LPA Misiones - consultar https://digestomisiones.gob.ar para modificaciones posteriores a mayo 2026]
```

### 2.2 Proceso contencioso administrativo - Ley I-95 (ex Ley 3064)

**[CONFIRMADO]** Norma: Ley I-95 (ex Ley 3064, Código de Procedimiento Contencioso Administrativo de la Provincia de Misiones). Texto consolidado por Ley IV-70 (Digesto Jurídico Misiones, B.O. 13-06-2016).

**[CONFIRMADO]** Subsidiariedad (art. 23 Ley I-95): el Código Procesal Civil, Comercial, de Familia y Violencia Familiar se aplica supletoriamente en materia de plazos y notificaciones, y en todo lo no previsto.

**Texto vigente:** https://digestomisiones.gob.ar/archivospdf/1688644878_LEY%20I%20-%20N%2095.pdf

### 2.3 Silencio administrativo y denegación tácita

**[CONFIRMADO]** La denegación tácita opera conforme a la Ley I-89. La Ley I-95 (art. 10) remite a la Ley I-89 para los supuestos de denegación tácita del reclamo o derecho sustentado.

Sin reforma análoga al Dec 971/2024 nacional: Misiones no adoptó el régimen de silencio positivo de la Ley 27.742 nacional.

### 2.4 Plazo de caducidad para accionar judicialmente

**[CONFIRMADO — DATO MÁS CRÍTICO]**

- **Plazo general:** **60 días** desde el día siguiente al de la notificación de la decisión administrativa (art. 24 Ley I-95).
- **Cómputo:** conforme al art. 6 del CCCN (días corridos), pero **no se computan los días comprendidos en las ferias judiciales** (art. 25 Ley I-95). En la práctica esto se asemeja a un cómputo en días hábiles con la particularidad de excluir solo las ferias, no todos los inhábiles.
- **Naturaleza:** caducidad — en ningún caso puede suspenderse o interrumpirse el plazo (art. 26 Ley I-95).
- **Denegación tácita:** desde el día siguiente al vencimiento del plazo establecido en el art. 10 (art. 24 Ley I-95).
- **Lesividad:** 180 días desde la emisión del acto que declara la lesividad (art. 24 Ley I-95).
- **¿Declarable de oficio?:** sí — el STJM declara inadmisible el proceso cuando la presentación es extemporánea (art. 54 inc. c Ley I-95).

```
[ALERTA PLAZO FATAL: art. 24 Ley I-95 CCA Misiones - 60 días - cómputo conforme art. 6 CCCN SIN computar días de ferias judiciales - desde día siguiente a la notificación de la decisión que agota la vía - NO se suspende ni interrumpe (art. 26) - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes:**

| Régimen | Plazo | Tipo | Norma |
|---------|-------|------|-------|
| **Misiones** | **60 días** | Corridos (sin ferias) | Ley I-95 art. 24 |
| PBA | 90 días | Hábiles judiciales | Ley 12.008 art. 18 |
| CABA | 90 días | Hábiles judiciales | Ley 189 art. 7 |
| Tucumán | 90 días | Hábiles judiciales | Ley 6205 art. 9 |
| Federal (post-9-jul-2024) | 180 días | Hábiles judiciales | LNPA art. 25 |
| Mendoza | 30 días | Corridos | Ley 3918 art. 20 |
| Corrientes | 60 días | Hábiles judiciales | Ley 3460 art. 223 |
| Salta | 30 días | Hábiles judiciales | Ley 793 art. 12 |
| Córdoba | 30 días | Hábiles judiciales | Ley 7182 art. 8 |
| Santa Fe | 30 días | A verificar (jurisprudencia CSJ SF) | Ley 11.330 art. 9 |
| Neuquén | 30 días | A verificar (hábiles/corridos) | Ley 1305 art. 10 |
| Río Negro | 30 días | Hábiles | Ley 5773 art. 11 |
| Entre Ríos | 1 año | Corridos | Ley 7061 art. 19 |

### 2.5 Recursos administrativos (Ley I-89)

**[CONFIRMADO] Recurso de revocatoria (art. 85 Ley I-89):**
- Plazo: **10 días hábiles administrativos** desde el día siguiente a la notificación del acto.
- Ante: la misma autoridad que dictó la resolución.

**[CONFIRMADO] Recurso jerárquico:**
- Plazo: **15 días hábiles administrativos** desde la notificación del rechazo de la revocatoria, o desde la configuración del silencio denegatorio.
- Ante: la máxima autoridad del poder o ente descentralizado (Gobernador o Directorio según el caso).

**[CONFIRMADO] Cómputo general (art. 89 Ley I-89):** todos los plazos del procedimiento se cuentan exclusivamente por días hábiles administrativos.

**Sin reforma análoga al Decreto 695/2024 nacional:** Misiones no duplicó los plazos de recursos administrativos.

```
[ALERTA PLAZO FATAL: recurso de revocatoria - Ley I-89 art. 85 - 10 días hábiles administrativos desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico - Ley I-89 - 15 días hábiles administrativos desde notificación del rechazo de la revocatoria o desde el silencio - vencimiento: calcular]
```

### 2.6 Tabla unificada de plazos

| Recurso / instituto | Plazo | Tipo de días | Norma | Estado |
|---------------------|-------|--------------|-------|--------|
| Revocatoria | 10 días | Hábiles administrativos | Ley I-89 art. 85 | [CONFIRMADO] |
| Jerárquico | 15 días | Hábiles administrativos | Ley I-89 | [CONFIRMADO] |
| Caducidad para accionar | 60 días | Corridos (sin ferias judiciales) | Ley I-95 art. 24 | [CONFIRMADO] |
| Lesividad | 180 días | Corridos (sin ferias) | Ley I-95 art. 24 | [CONFIRMADO] |
| Caducidad de instancia | 6 meses | - | Ley I-95 art. 45 | [CONFIRMADO] |
| Caducidad instancia (sumario/recursos) | 3 meses | - | Ley I-95 art. 46 | [CONFIRMADO] |
| Cautelar previa - caducidad si no hay acción | 10 días desde el auto | - | Ley I-95 art. 33 | [CONFIRMADO] |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial. El plazo del art. 24 es en días corridos excluyendo ferias judiciales.

### 2.7 Agotamiento de la vía administrativa

**[CONFIRMADO]** Regla general (art. 8 Ley I-95): el acto debe ser definitivo y causar estado.

**[CONFIRMADO]** Excepción: cuando los actos que fundan la demanda son resueltos por la más alta autoridad competente (de oficio o a petición de parte), queda expedita la vía judicial. La interposición de recursos contra esas resoluciones **no interrumpe** el plazo para la acción (art. 9 Ley I-95).

**[CONFIRMADO]** Entes autárquicos (art. 12 Ley I-95): no puede promoverse la acción sin haberse interpuesto recurso administrativo ante el PE cuando se trate de decisiones de entidades autárquicas.

**[CONFIRMADO]** Límite de pretensiones (art. 16 Ley I-95): la acción debe versar sobre las cuestiones previamente objeto de reclamo o recurso administrativo. Excepción: los fundamentos de hecho y de derecho que no sean esenciales o no hayan influido directamente en la resolución impugnada.

```
[VERIFICAR AGOTAMIENTO DE VÍA MISIONES: Ley I-89 + Ley I-95 arts. 8, 9 y 12 - para entes autárquicos: recurso ante el PE obligatorio - límite de pretensiones art. 16]
```

### 2.8 Suspensión cautelar (arts. 27-33 Ley I-95)

**[CONFIRMADO]** Puede solicitarse antes, simultánea o posteriormente a la acción (art. 27).

**[CONFIRMADO]** Trámite (art. 28): vista a la demandada por 3 días; el STJM resuelve en 5 días.

**[CONFIRMADO]** Requisitos (art. 29): que "prima facie" el acto sea nulo por incompetencia o violación manifiesta de la ley, o que su ejecución pueda causar daño irreparable y aparezca verosímil el derecho invocado.

**[CONFIRMADO]** No procede la suspensión (art. 30):**
- (a) demolición/clausura por seguridad/moralidad/higiene o resguardo de la salud/medioambiente con dictamen técnico y jurídico fundado;
- **(b) medidas disciplinarias de agentes estatales (cualquiera sea su especie)**;
- (c) actos que sean prima facie ejercicio de facultades discrecionales.

**[CONFIRMADO]** Caducidad de la cautelar (art. 33): la suspensión dispuesta antes de la acción caduca automáticamente si la acción no se deduce en **10 días** desde el auto que ordena la suspensión.

```
[ALERTA CAUTELAR MISIONES: suspensión ordenada antes de la acción caduca si la demanda no se interpone en 10 días desde el auto (art. 33 Ley I-95)]
[ATENCIÓN: no procede suspensión en medidas disciplinarias de agentes estatales de cualquier especie - art. 30 inc. b Ley I-95]
```

### 2.9 Actos impugnables y pretensiones (Ley I-95)

**[CONFIRMADO]** Materia incluida (art. 6):
- Actos discrecionales por razones de ilegitimidad.
- Actos separables de contratos administrativos.
- Actos sobre reclamos de retribuciones, jubilaciones o pensiones de agentes estatales (excepto relaciones regidas por convenios colectivos).
- Restricciones administrativas al dominio (art. 1970 CCCN).
- Ejecución judicial de actos firmes cuando la ley requiere intervención judicial.

**[CONFIRMADO]** Materia excluida (art. 7):
- Expropiaciones; ejecutivos, apremio, desalojos, interdictos, acciones posesorias y reales.
- Acciones fundadas exclusivamente en derecho privado.
- Daños cuando no derivan de vinculación especial de derecho público contractual o reglamentaria.

**[CONFIRMADO]** Pretensiones admisibles (art. 22):
- Anulación total o parcial del acto.
- Restablecimiento o reconocimiento del derecho.
- Reparación de daños y perjuicios consecuencia de incumplimiento de normas de derecho público o contratos administrativos.
- Interpretación declarativa.
- Lesividad (anulación de actos irrevocables lesivos al interés público).

**[CONFIRMADO]** Pago previo en materia tributaria (art. 15): se exige el pago previo de las obligaciones tributarias vencidas; no se aplican multas, recargos ni accesorios.

### 2.10 Tabla de responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| STJM (única instancia) | Fiscalía de Estado de Misiones | Ley I-95 art. 64 (notificación) |
| Tribunal de Cuentas | Su presidente | Ley I-95 art. 64 inc. a.2 |
| Consejo General de Educación | Director General de Educación | Ley I-95 art. 64 inc. a.3 |
| Ente autárquico | Presidente del Directorio o equivalente | Ley I-95 art. 64 inc. b |
| Municipalidad | Intendente o equivalente | Ley I-95 art. 64 inc. c |

```
[VERIFICAR REPRESENTACIÓN PROCESAL MISIONES: Fiscalía de Estado como representante del Estado provincial en el STJM - notificaciones conforme art. 64 Ley I-95 según el organismo demandado]
```

### 2.11 Responsabilidad del Estado provincial

**[CONFIRMADO]** Sin ley propia equivalente a Ley 26.944 nacional. La Ley 26.944 no aplica al Estado provincial misionero.

**[CONFIRMADO]** La pretensión resarcitoria es admisible ante el STJM cuando el daño deriva de incumplimiento o vinculación especial de derecho público contractual o reglamentaria (art. 22 inc. c y art. 7 inc. d Ley I-95). Si el daño es extracontractual puro (sin vinculación especial de derecho público), puede no corresponder al STJM: verificar jurisprudencia.

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD MISIONES: sin ley propia - verificar si el daño corresponde al STJM (vinculación especial de derecho público) o al fuero civil (daño extracontractual puro) - jurisprudencia STJM sobre art. 7 inc. d Ley I-95]
```

### 2.12 Empleo público Misiones

**[CONFIRMADO]** Estatuto general: **Ley I-37** (ex Decreto Ley N° 560/73, Estatuto y Escalafón del Personal de la Administración Pública de Misiones). Texto consolidado en el Digesto Jurídico provincial (Ley IV-70). Regula derechos (estabilidad, carrera), deberes y régimen disciplinario de los agentes públicos provinciales.

**[CONFIRMADO]** Los actos sobre retribuciones, jubilaciones y pensiones de agentes estatales son expresamente impugnables ante el STJM (art. 6 inc. c Ley I-95), salvo relaciones regidas por convenios colectivos de trabajo.

**[CONFIRMADO]** No procede la suspensión cautelar en medidas disciplinarias de agentes estatales (art. 30 inc. b Ley I-95).

```
[VERIFICAR VIGENCIA: Ley I-37 (ex D.Ley 560/73) estatuto del empleado público Misiones - consultar https://digestomisiones.gob.ar para modificaciones posteriores al texto consolidado]
```

### 2.13 Contratación pública Misiones

**[CONFIRMADO]** Norma marco: **Ley VII-11** (ex Ley 2303, Ley de Contabilidad de Misiones, Capítulo VII). Texto consolidado en el Digesto Jurídico provincial.

**[CONFIRMADO]** Montos vigentes (actualizados periódicamente por decreto del PE):
- Contratación directa: hasta $7.209.000
- Licitación privada: desde el límite de la contratación directa hasta $55.984.000
- Licitación pública obligatoria (art. 84): todo monto que supere $55.984.000

```
[VERIFICAR MONTOS: Ley VII-11 Misiones - los topes de contratación directa, licitación privada y pública se actualizan por decreto del Poder Ejecutivo - verificar decreto vigente antes de encuadrar el procedimiento - consultar https://boletin.misiones.gov.ar]
```

---

## Bloque 3 - Alertas críticas

### Alerta 1 - Plazo de caducidad: 60 días corridos sin ferias

**[CONFIRMADO]** El plazo del art. 24 Ley I-95 es de 60 días, computados conforme al art. 6 CCCN (corridos), excluyendo solo los días de ferias judiciales. Esta mecánica es diferente de PBA (90 días hábiles), Mendoza (30 días corridos) y Santa Fe (30 días). No transpolar plazos.

Antes de analizar cualquier otra cuestión, emitir:
```
[ALERTA PLAZO FATAL: art. 24 Ley I-95 CCA Misiones - 60 días corridos (sin ferias judiciales) - desde día siguiente a la notificación de la decisión que agota la vía - NO se suspende ni interrumpe (art. 26) - vencimiento: calcular]
```

### Alerta 2 - Cautelar caduca en 10 días

**[CONFIRMADO]** Si se solicita la suspensión antes de interponer la acción, la cautelar caduca si la acción no se deduce dentro de los **10 días** del auto que la ordena (art. 33). Es el plazo más corto de los sistemas analizados para este supuesto.

### Alerta 3 - No procede cautelar en medidas disciplinarias

**[CONFIRMADO]** El art. 30 inc. b veda la suspensión en "medidas disciplinarias de agentes estatales, cualquiera sea su especie". Informar al cliente en todo caso de empleo público antes de pedir cautelar.

---

## Bloque 4 - Checklists operativos

### Checklist: acto administrativo

1. ¿El acto es del Estado provincial, de un municipio, de un ente autárquico o de un organismo federal?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo de 60 días del art. 24)
3. ¿El acto es definitivo y causa estado?
4. ¿Hay expediente administrativo? ¿El abogado lo tiene o requiere vista?
5. ¿Se agotaron los recursos administrativos de la Ley I-89?
6. Para entes autárquicos: ¿se interpuso recurso ante el PE? (art. 12 Ley I-95 — obligatorio)
7. ¿Las pretensiones coinciden con lo planteado en sede administrativa? (art. 16 Ley I-95)
8. ¿La pretensión resarcitoria deriva de vinculación especial de derecho público? (verificar competencia STJM)

### Checklist: acción judicial

1. Verificar agotamiento de la vía (Ley I-89 + Ley I-95 arts. 8, 9, 12).
2. Calcular el plazo de **60 días corridos sin ferias** desde la notificación (art. 24 Ley I-95).
3. Verificar que el plazo no se haya interrumpido (art. 26: no puede suspenderse ni interrumpirse).
4. En materia tributaria: verificar pago previo de obligaciones vencidas (art. 15 Ley I-95).
5. Si se solicitó cautelar previa: interponer la demanda en **10 días** desde el auto que ordena la suspensión (art. 33).
6. Si la pretensión involucra medidas disciplinarias: no pedir cautelar (art. 30 inc. b).

### Checklist: responsabilidad del Estado

1. Verificar si el daño deriva de vinculación especial de derecho público (competencia STJM) o es extracontractual puro (posible fuero civil).
2. No aplicar Ley 26.944 ni CCCN sin verificar criterio del STJM.
3. La pretensión resarcitoria puede acumularse a la anulatoria (art. 22 inc. c).

### Checklist: empleo público

1. Identificar estatuto aplicable (general o sectorial).
2. Situación de revista del agente.
3. ¿Hubo sumario con garantías de debido proceso?
4. ¿La sanción encuadra en causal taxativa del estatuto?
5. No pedir cautelar en medidas disciplinarias (art. 30 inc. b Ley I-95).

### Checklist: contratación pública

1. Verificar norma provincial de contrataciones vigente y montos actualizados.
2. Verificar plazos de impugnación de pliegos y preadjudicación.
3. Para obra pública: verificar ley provincial; la Ley 13.064 nacional no aplica salvo remisión contractual expresa.

---

## Fuentes primarias

- **Digesto Jurídico de Misiones:** https://digestomisiones.gob.ar
- **Boletín Oficial de Misiones:** https://boletin.misiones.gov.ar
- **Poder Judicial de Misiones (STJM):** https://www.jusmisiones.gov.ar
- **SAIJ:** https://www.saij.gob.ar

---

## Reglas de citación - administrativo Misiones

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente.

**Jurisprudencia:** el STJM actúa en pleno en materia CA. Verificar la composición al momento del fallo. Usar:
```
[INSERTAR FALLO VERIFICADO: STJM En Pleno - doctrina requerida]
```

**Actos administrativos:** usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con constancia de notificación]
```

**Plazos:** no transpolar plazos de otros regímenes. Usar:
```
[ALERTA PLAZO FATAL: art. 24 Ley I-95 CCA Misiones - 60 días corridos (sin ferias judiciales) - desde notificación de la decisión que agota la vía - vencimiento: calcular]
```

---

*Última actualización: mayo 2026*
*Normativa base: Ley I-89 (ex Ley 2970) LPA Misiones, Ley I-95 (ex Ley 3064) Código CA Misiones (texto consolidado Ley IV-70, Digesto 2015)*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
