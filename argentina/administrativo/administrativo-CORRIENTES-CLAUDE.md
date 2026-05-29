# Perfil de práctica · Derecho administrativo · Provincia de Corrientes

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Corrientes.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.
>
> **Estado del perfil:** operativo — datos procesales clave confirmados. Las normas con etiqueta [A VERIFICAR] no afectan la operatividad de la cadena recursiva ni del proceso judicial.

---

## Sistema de etiquetas

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de mayo 2026.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse en el Boletín Oficial de Corrientes o en el portal del Poder Judicial antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** Provincia de Corrientes

**FUERO_HABITUAL:** [COMPLETAR: "Juzgado de Primera Instancia en lo Contencioso Administrativo N° X (Iº o IIº), Corrientes Capital" / "Cámara en lo Contencioso Administrativo y Electoral, Corrientes". Los dos únicos Juzgados CA de la provincia están en Capital (Primera Circunscripción, art. 5 D.Ley 26/00). El fuero NO está descentralizado en el interior. Para causas originadas en el interior, la radicación corresponde a los Juzgados CA de Capital salvo Acordada del STJ o disposición de la Ley 6554 (CPA, si vigente). Ver Alerta 3.]

**AREAS_PRACTICA:** [COMPLETAR: Ej. "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, contratación pública, habilitaciones municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: Ej. "Ministerio de Salud Corrientes, IOSCOR, Municipalidad de Corrientes, DGR Corrientes".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Corrientes: procedimiento administrativo ante la Administración provincial y municipal (Ley 3460), recursos administrativos en sede provincial, acción contencioso administrativa ante los Juzgados de Primera Instancia CA y la Cámara en lo Contencioso Administrativo y Electoral (Ley 4106, modificada por Ley 5846), responsabilidad del Estado provincial, empleo público y contratación pública.

**Estructura judicial [CONFIRMADO]:** desde la Ley 5846 (2008), Corrientes tiene:
- **Primera instancia:** Juzgados de Primera Instancia en lo Contencioso Administrativo — **únicamente en Capital** (Primera Circunscripción). El fuero no está descentralizado en el interior (D.Ley 26/00 art. 5).
- **Alzada:** Cámara en lo Contencioso Administrativo y Electoral (3 jueces, asiento en Corrientes Capital, competencia en todo el territorio provincial).
- **Tribunal superior:** Superior Tribunal de Justicia de Corrientes (casación e inconstitucionalidad).

**[CONFIRMADO] Estado del fuero en el interior — fuero concentrado en Capital:**

El Decreto Ley 26/00 (Ley Orgánica de la Administración de Justicia de Corrientes) distribuye los juzgados por circunscripción sin crear ningún Juzgado CA fuera de la Primera Circunscripción (Capital). El art. 5 asigna únicamente dos (2) Juzgados en lo Contencioso Administrativo, ambos en Capital. Las demás circunscripciones (Goya, Curuzú Cuatiá, Paso de los Libres, Santo Tomé) tienen solo fueros ordinarios: Civil y Comercial, Laboral, Familia, Instrucción.

**Vacío de delegación:** el art. 35 D.Ley 26/00 limita la competencia de los jueces civiles y comerciales del interior a "todos los asuntos que le están asignados por las Leyes Procesales", sin otorgarles competencia contencioso administrativa en subsidio. La cláusula de delegación explícita que existe en otras provincias (ej. Tucumán, Entre Ríos) está ausente en este texto.

**Consecuencia práctica:** la competencia contencioso administrativa está concentrada en los dos Juzgados CA de la Primera Circunscripción (Capital). Si un abogado del interior de la provincia necesita habilitar la instancia judicial, la radicación corresponde en Capital, salvo que exista una Acordada del STJ habilitando competencia delegada en jueces civiles del interior por ejercicio de la superintendencia (art. 23 inc. 27 D.Ley 26/00) o que el nuevo Código Procesal Administrativo provincial (Ley 6554, si estuviere vigente) regule este punto. **Verificar antes de radicar en cualquier circunscripción fuera de Capital.**

**Notificaciones al Estado en el interior:** al no prever el D.Ley 26/00 una estructura de defensores del Estado en el interior, las notificaciones a la Provincia de Corrientes se realizan en el domicilio legal de la Fiscalía de Estado en la Ciudad de Corrientes (Capital), independientemente del lugar donde se originó el acto impugnado.

```
[VERIFICAR COMPETENCIA CORRIENTES INTERIOR: D.Ley 26/00 no descentraliza el fuero CA fuera de Capital - verificar si existe Acordada del STJ de Corrientes habilitando competencia en jueces civiles del interior, o si la Ley 6554 (CPA Corrientes, si vigente) regula este punto - antes de radicar fuera de Capital consultar Mesa de Entradas del STJ o Colegio de Abogados de Corrientes]
```

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Corrientes (ARCA/ex AFIP, ANSES), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal correntina, aplica este perfil.

**Tercer nivel - organismos municipales [CONFIRMADO]:** la Ley 4106 incluye a las Municipalidades entre las autoridades cuyos actos son impugnables (art. 1). La notificación de la demanda cuando el demandado es un municipio se hace al Intendente (Ley 4106, art. 60 inc. c, texto según Ley 5846).

```
[VERIFICAR ESTADO DEL FUERO INTERIOR: Corrientes - confirmar si en la circunscripción correspondiente ya funciona Juzgado CA propio o si la competencia corresponde a la Cámara Civil y Comercial con competencia asignada - antes de radicar en el interior provincial]
```

---

## Bloque 2 - Normas base

### 2.1 Procedimiento administrativo - Ley 3460

**[CONFIRMADO]** Norma principal: Ley 3460 (Código de Procedimientos Administrativos de la Provincia de Corrientes), sancionada el 22/11/1978, modificada por Ley 6250 (principio de celeridad y TIC) y otras.

**Ámbito (art. 1 Ley 3460):** rige la actividad administrativa del Estado provincial, con aplicación supletoria a personas públicas no estatales y privadas que ejerzan función administrativa por delegación estatal.

**Texto vigente:** Boletín Oficial de Corrientes y portal de la H. Cámara de Diputados (https://hcdcorrientes.gov.ar). Verificar modificaciones posteriores a la versión consultada (mayo 2026).

**Articulado clave:** art. 14 (plazos en días hábiles administrativos), arts. 15-16 (vencimiento y pérdida de derechos), art. 91 (recurso de revocatoria), arts. 94 y ss. (recurso jerárquico), arts. 112 y ss. (silencio y denegatoria tácita), art. 223 (prescripción/caducidad de la acción judicial - ver sección 2.4).

```
[VERIFICAR VIGENCIA: Ley 3460 LPA Corrientes (mod. Ley 6250 y otras) - consultar https://hcdcorrientes.gov.ar/digesto para modificaciones posteriores a mayo 2026]
```

### 2.2 Proceso contencioso administrativo - Ley 4106 / Ley 5846

**[CONFIRMADO]** Normas:
- **Ley 4106** (Código Contencioso Administrativo, 1980): regula el proceso. Fue modificado por el Decreto Ley 182/2001 (modifica arts. 36, 59, 61 y otros) y por la **Ley 5846** (2008, que creó la Cámara CA y los Juzgados de Primera Instancia, derogando los arts. 6 y 9 que radicaban todo en el STJ).
- **Ley 5846** (2008): ley orgánica del fuero CA. Crea la Cámara CA y los Juzgados de Primera Instancia CA. Modifica el texto de varios artículos de la Ley 4106 para adaptar las referencias del "Tribunal" (antes STJ) al nuevo fuero.

**Texto vigente:** Ley 4106 actualizada disponible en https://hcdcorrientes.gov.ar/digesto/legislacion/textos-actualizados/Ley4106.pdf. Verificar modificaciones ulteriores.

**Subsidiariedad (art. 41 Ley 4106):** el Código de Procedimientos en lo Civil y Comercial de Corrientes aplica supletoriamente en todo lo no previsto.

### 2.3 Silencio administrativo y denegatoria tácita

**[CONFIRMADO]** La Ley 3460 (art. 112 y ss.) regula la denegatoria tácita. Vencido el plazo para resolver sin pronunciamiento expreso, el interesado puede articular el recurso siguiente o considerar agotada la vía.

**Sin reforma análoga al Dec 971/2024 nacional:** Corrientes no adoptó el régimen de silencio positivo de la Ley 27.742 nacional. El silencio positivo aplica solo ante la Administración nacional.

### 2.4 Plazo de caducidad para accionar judicialmente

**[CONFIRMADO] Plazo:** **60 días hábiles judiciales** para interponer la acción contencioso administrativa (art. 223 Ley 3460, modificado por D.Ley 182/2001).

**[CONFIRMADO] Cómputo:** desde el día siguiente al de la notificación del acto definitivo que agota la vía (resolución del jerárquico), o desde el día siguiente en que opera el silencio administrativo si la autoridad no resolvió el recurso en término.

**[CONFIRMADO] Naturaleza:** caducidad perentoria. Vencidos los 60 días hábiles judiciales, se pierde el derecho a accionar; el acto administrativo queda firme y consentido, sin posibilidad de revisión judicial.

```
[ALERTA PLAZO FATAL: art. 223 Ley 3460 (mod. D.Ley 182/2001) CCA Corrientes - 60 días hábiles judiciales - desde notificación de la decisión que agota la vía (rechazo del jerárquico o silencio) - caducidad perentoria - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes:**

| Régimen | Plazo | Tipo | Norma |
|---------|-------|------|-------|
| **Corrientes** | **60 días** | **Hábiles judiciales** | Ley 3460 art. 223 |
| Misiones | 60 días | Corridos (sin ferias) | Ley I-95 art. 24 |
| PBA | 90 días | Hábiles judiciales | Ley 12.008 art. 18 |
| CABA | 90 días | Hábiles judiciales | Ley 189 art. 7 |
| Tucumán | 90 días | Hábiles judiciales | Ley 6205 art. 9 |
| Federal (post-9-jul-2024) | 180 días | Hábiles judiciales | LNPA art. 25 |
| Neuquén | 30 días | A verificar (hábiles/corridos) | Ley 1305 art. 10 |
| Río Negro | 30 días | Hábiles | Ley 5773 art. 11 |
| Mendoza | 30 días | Corridos | Ley 3918 art. 20 |
| Córdoba | 30 días | Hábiles judiciales | Ley 7182 art. 8 |
| Salta | 30 días | Hábiles judiciales | Ley 793 art. 12 |
| Santa Fe | 30 días | A verificar (jurisprudencia CSJ SF) | Ley 11.330 art. 9 |
| Entre Ríos | 1 año | Corridos | Ley 7061 art. 19 |

### 2.5 Recursos administrativos (Ley 3460)

**[CONFIRMADO] Recurso de revocatoria con jerárquico en subsidio implícito (art. 197 Ley 3460):**

Corrientes adopta el sistema de **revocatoria con jerárquico en subsidio implícito**: al interponer la revocatoria se activa automáticamente el jerárquico como subsidiario, sin necesidad de presentar un escrito autónomo de "recurso jerárquico" separado.

- **Plazo:** **20 días hábiles administrativos** desde la notificación del acto lesivo. Se interpone ante el mismo órgano que dictó el acto.
- **Resolución por el inferior:** el órgano emisor resuelve la revocatoria dentro del plazo legal.
- **Elevación automática al superior:** si el órgano inferior rechaza la revocatoria, o si vence el plazo de un mes sin pronunciamiento (denegatoria tácita), las actuaciones se elevan **de oficio y automáticamente** al superior jerárquico (Poder Ejecutivo o máxima autoridad del ente) para que resuelva el jerárquico en subsidio.
- **Mejora de fundamentos:** el particular tiene la facultad de presentar un escrito para mejorar los fundamentos del jerárquico dentro de los primeros días de recibidas las actuaciones por el superior. No es obligatorio pero es estratégicamente recomendable.
- **Agota la vía:** la resolución del PE o autoridad máxima agota la instancia administrativa.

**Tabla operativa de recursos Corrientes:**

| Recurso | Plazo | Tipo de días | Mecanismo |
|---------|-------|--------------|-----------|
| Revocatoria (con jerárquico en subsidio) | 20 días | Hábiles administrativos | Se interpone ante el órgano emisor; activa jerárquico automáticamente |
| Jerárquico (activado automáticamente) | - | - | Se eleva de oficio al superior tras rechazo o silencio de la revocatoria |
| Acción judicial (art. 223) | 60 días | Hábiles judiciales | Desde notificación del rechazo del jerárquico o desde el silencio |

**[CONFIRMADO] Pérdida del derecho recursivo (art. 15 Ley 3460):** vencido el plazo de 20 días sin interponer la revocatoria, se pierde el derecho. La presentación extemporánea puede considerarse denuncia de ilegitimidad, salvo resolución contraria por seguridad jurídica o abandono voluntario del derecho.

**Sin reforma análoga al Decreto 695/2024 nacional:** Corrientes no duplicó los plazos de recursos administrativos.

```
[ALERTA PLAZO FATAL: recurso de revocatoria con jerárquico en subsidio - Ley 3460 art. 197 - 20 días hábiles administrativos desde notificación del acto - vencimiento: calcular]
[NOTA: el jerárquico se activa automáticamente; no requiere escrito autónomo separado - las actuaciones se elevan de oficio al superior tras rechazo o silencio del inferior]
```

### 2.6 Tabla unificada de plazos

| Recurso / instituto | Plazo | Tipo de días | Norma | Estado |
|---------------------|-------|--------------|-------|--------|
| Revocatoria con jerárquico en subsidio | 20 días | Hábiles administrativos | Ley 3460 art. 197 | [CONFIRMADO] |
| Jerárquico (elevación automática) | Automático tras rechazo/silencio | - | Ley 3460 | [CONFIRMADO] |
| Caducidad para accionar judicialmente | 60 días | Hábiles judiciales | Ley 3460 art. 223 (mod. D.Ley 182/2001) | [CONFIRMADO] |
| Caducidad de instancia | 6 meses | [A VERIFICAR: corridos o hábiles] | Ley 4106 art. 36 (mod. D.Ley 182/2001) | [CONFIRMADO plazo; A VERIFICAR naturaleza] |
| Cautelar previa - caducidad si no hay demanda | 15 días | - | Ley 4106 art. 19 | [CONFIRMADO] |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial, no días hábiles judiciales.

### 2.7 Agotamiento de la vía administrativa

**[CONFIRMADO]** Regla general (art. 10 Ley 4106): antes de iniciar la acción contencioso administrativa, es preciso agotar los recursos previstos en la Ley 3460 o el trámite del art. 112 de dicha ley según el caso.

**[CONFIRMADO] Excepciones al agotamiento (art. 11 Ley 4106):**
- Acto dictado de oficio ejecutable antes de tramitarse el reclamo.
- El administrado presentó su pretensión contraria antes del acto de oficio.
- Repetición de lo pagado al Estado por ejecución o gravamen indebido.
- Daños y perjuicios, desalojo o acciones que no tramiten por vía ordinaria.
- Clara conducta del Estado que haga presumir la ineficacia del procedimiento.
- Se demanda a un ente autárquico, empresa del Estado, sociedad mixta o ente descentralizado con facultad para estar en juicio.

**[CONFIRMADO] Límite de pretensiones (art. 12 Ley 4106):** las pretensiones deben limitarse a las cuestiones debatidas en sede administrativa. Pueden deducirse contra la decisión definitiva originaria, la que resulte de los recursos, o contra ambas conjuntamente.

```
[VERIFICAR AGOTAMIENTO DE VÍA CORRIENTES: Ley 3460 + Ley 4106 art. 10 - verificar cadena recursiva completa y si la resolución que agota la vía fue notificada]
```

### 2.8 Suspensión cautelar (arts. 17-19 y 23-30 Ley 4106)

**[CONFIRMADO] Suspensión de la decisión administrativa (art. 17 Ley 4106):**
Puede solicitarse antes, simultánea o posteriormente a la acción. Requisitos:
- (a) haber solicitado la suspensión a la demandada con resultado negativo (salvo excepciones del art. 11);
- (b) verosimilitud de las irregularidades;
- (c) daño de la ejecución mayor o desproporcionado respecto al perjuicio de la suspensión;
- (d) urgencia notoria (no exigida cuando la irregularidad sea manifiesta).

**[CONFIRMADO] Caducidad de la cautelar (art. 19 in fine Ley 4106):** la suspensión dispuesta antes de la demanda caduca automáticamente y de pleno derecho si ésta no se deduce en el plazo de **15 días**.

```
[ALERTA CAUTELAR CORRIENTES: suspensión ordenada antes de la demanda caduca automáticamente si la acción no se interpone en 15 días (art. 19 in fine Ley 4106)]
```

### 2.9 Tabla de responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| Juzgados CA (primera instancia, Capital) | Fiscalía de Estado de Corrientes | Ley 5846; D.Ley 26/00 art. 75 inc. b |
| Cámara CA y Electoral (alzada) | Fiscalía de Estado de Corrientes | Ley 5846; D.Ley 26/00 art. 75 inc. b |
| STJ (casación / inconstitucionalidad) | Fiscalía de Estado de Corrientes | D.Ley 26/00 art. 75 inc. b |
| Notificaciones a organismos públicos con asiento en Capital | En sus respectivos despachos, por cédula o en el expediente | Ley 4106 art. 35 |
| Demandas desde el interior de la provincia | Notificación en domicilio legal de Fiscalía de Estado en Capital (Corrientes), sin representación territorial descentralizada confirmada | D.Ley 26/00; Ley 4106 art. 35 |

```
[CONFIRMADO: Fiscalía de Estado de Corrientes representa al Estado en todas las instancias (D.Ley 26/00 art. 75 inc. b) - notificaciones en domicilio legal en Capital - sin estructura territorial descentralizada confirmada en el interior]
```

---

## Bloque 3 - Alertas críticas

### Alerta 1 - Plazo para accionar: 60 días hábiles judiciales

**[CONFIRMADO]** El art. 223 Ley 3460 (mod. D.Ley 182/2001) fija **60 días hábiles judiciales** desde la notificación de la resolución que agota la vía (rechazo del jerárquico o silencio). Caducidad perentoria: vencido el plazo, el acto queda firme sin posibilidad de revisión judicial.

```
[ALERTA PLAZO FATAL: art. 223 Ley 3460 (mod. D.Ley 182/2001) CCA Corrientes - 60 días hábiles judiciales - desde notificación de la resolución que agota la vía - caducidad perentoria - vencimiento: calcular]
```

### Alerta 2 - Reforma estructural del fuero (Ley 5846)

**[CONFIRMADO]** La Ley 5846 (2008) transformó el sistema: el STJ dejó de ser tribunal de instancia única en lo CA. Ahora hay primera instancia (Juzgados CA) y alzada (Cámara CA). Verificar que la jurisprudencia que se cite corresponda al fuero actual (post-2008) y no al régimen anterior del STJ en instancia única.

### Alerta 3 - Fuero concentrado en Capital / interior sin competencia delegada confirmada

**[CONFIRMADO]** El D.Ley 26/00 reserva los dos únicos Juzgados CA de la provincia a la Primera Circunscripción (Capital). No hay juzgados CA en Goya, Curuzú Cuatiá, Paso de los Libres ni Santo Tomé. El art. 35 D.Ley 26/00 no otorga competencia contencioso administrativa en subsidio a los jueces civiles del interior.

La competencia territorial para demandar al Estado provincial corresponde a los Juzgados CA de Capital, salvo Acordada del STJ o disposición de la Ley 6554 (CPA, si vigente) que establezca otra cosa. Antes de radicar desde el interior, verificar si existe esa Acordada consultando la Mesa de Entradas del STJ o el Colegio de Abogados de Corrientes.

Notificaciones al Estado: siempre en domicilio de Fiscalía de Estado en Capital.

### Alerta 4 - Sistema de revocatoria con jerárquico en subsidio implícito

**[CONFIRMADO]** Corrientes no tiene un recurso jerárquico autónomo: el jerárquico se activa automáticamente como subsidiario de la revocatoria. El plazo para interponer la revocatoria es de **20 días hábiles administrativos** (art. 197 Ley 3460). Vencido ese plazo sin recurrir, el acto queda firme. El particular puede mejorar los fundamentos del jerárquico una vez elevadas las actuaciones al superior, pero no debe presentar un nuevo escrito de "jerárquico" por separado.

---

## Bloque 4 - Checklists operativos

### Checklist: acto administrativo

1. ¿El acto es del Estado provincial, de un municipio o de un organismo federal?
2. ¿El acto fue notificado? ¿En qué fecha?
3. ¿Es definitivo y sin recurso administrativo disponible?
4. ¿Hay expediente administrativo? ¿El abogado lo tiene o requiere vista?
5. ¿Se interpuso la revocatoria con jerárquico en subsidio en plazo? (**20 días hábiles administrativos**, art. 197 Ley 3460)
6. ¿Se notificó la resolución del jerárquico (o operó el silencio)? Ese hito inicia el plazo de 60 días hábiles judiciales.
7. ¿Las pretensiones coinciden con lo planteado en sede administrativa? (art. 12 Ley 4106)
8. Si el acto proviene del interior de la provincia: radicar en Juzgados CA de Capital (Primera Circunscripción). Verificar si existe Acordada del STJ que delegue competencia en el juez civil de la circunscripción del interior.

### Checklist: acción judicial

1. Verificar agotamiento de la vía (Ley 3460 + Ley 4106 art. 10).
2. Calcular el plazo de **60 días hábiles judiciales** desde la notificación de la resolución que agota la vía (art. 223 Ley 3460 mod. D.Ley 182/2001).
3. Verificar que las pretensiones no superen lo planteado en sede administrativa (art. 12 Ley 4106).
4. En materia tributaria: verificar pago previo (art. 15 Ley 4106).
5. Si se solicitó suspensión cautelar previa: interponer la demanda en **15 días** desde que la suspensión se cumplió (art. 19 in fine Ley 4106).

### Checklist: empleo público

1. Identificar estatuto aplicable: [PENDIENTE: verificar estatuto del empleado público provincial de Corrientes].
2. Situación de revista del agente.
3. ¿Hubo sumario con garantías de debido proceso?
4. ¿La sanción encuadra en causal taxativa del estatuto?

### Checklist: contratación pública

1. Verificar norma de contrataciones vigente de Corrientes y montos actualizados.
2. Verificar plazos de impugnación de pliegos y preadjudicación.
3. Para obra pública: verificar ley provincial; la Ley 13.064 nacional no aplica al Estado provincial salvo remisión contractual expresa.

---

## Fuentes primarias

- **H. Cámara de Diputados Corrientes (digesto de leyes):** https://hcdcorrientes.gov.ar/digesto
- **Poder Judicial de Corrientes:** https://www.juscorrientes.gov.ar
- **Boletín Oficial Corrientes:** https://www.boletinoficialcorrientes.gov.ar
- **SAIJ (normas provinciales):** https://www.saij.gob.ar

---

## Reglas de citación - administrativo Corrientes

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente.

**Jurisprudencia:** la reforma de la Ley 5846 (2008) separó el fuero CA del STJ. Nunca citar jurisprudencia del STJ en rol de tribunal de instancia única sin verificar si es anterior o posterior a 2008 y si sigue siendo aplicable. Usar:
```
[INSERTAR FALLO VERIFICADO: STJ Corrientes / Cámara CA Corrientes / Juzgado CA N° [X] - doctrina requerida - verificar si es pre o post Ley 5846 (2008)]
```

**Actos administrativos:** no asumir contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con constancia de notificación]
```

**Plazos:** no transpolar plazos de otros regímenes. Usar:
```
[ALERTA PLAZO FATAL: art. 223 Ley 3460 (mod. D.Ley 182/2001) CCA Corrientes - 60 días hábiles judiciales - desde notificación de la resolución que agota la vía - caducidad perentoria - vencimiento: calcular]
```

---

## Matriz de vigencia por norma

| Norma | Objeto | Estado | Fuente de verificación |
|-------|--------|--------|------------------------|
| Ley 3460 | LPA Corrientes | [A VERIFICAR post-2008] modificada por Ley 6250 y otras | https://hcdcorrientes.gov.ar/digesto |
| D.Ley 182/2001 | Modifica arts. 36, 59, 61, 66, 68, 69, 80, 97, 98, 101, 106 Ley 4106 y art. 223 Ley 3460 | [CONFIRMADO vigente] | https://hcdcorrientes.gov.ar/digesto |
| Ley 4106 | Código CA Corrientes | [CONFIRMADO vigente; verificar modificaciones post-2008] | https://hcdcorrientes.gov.ar/digesto |
| Ley 5846 | Crea Cámara CA y Juzgados CA | [CONFIRMADO vigente - reforma estructural 2008] | https://hcdcorrientes.gov.ar/digesto |

---

*Última actualización: mayo 2026*
*Normativa base: Ley 3460 LPA Corrientes (mod. Ley 6250 y D.Ley 182/2001), Ley 4106 Código CA (mod. D.Ley 182/2001 y Ley 5846), Ley 5846 (fuero CA), Constitución de Corrientes*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
