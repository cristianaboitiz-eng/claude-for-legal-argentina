# Perfil de práctica · Derecho administrativo · Provincia de Río Negro

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Río Negro.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.
>
> **Estado del perfil:** operativo — nuevo Código Procesal Administrativo (Ley 5773, vigente desde 23/12/2024). Verificar que la jurisprudencia citada corresponda al nuevo régimen.

---

## Sistema de etiquetas

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de mayo 2026.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** Provincia de Río Negro

**FUERO_HABITUAL:** [COMPLETAR: "Juzgado en lo Contencioso Administrativo N° X, [circunscripción judicial]". Río Negro tiene competencia territorial distribuida: el actor puede elegir entre el tribunal de su domicilio (cuando sea en la provincia) o el del demandado. También puede elegir el del lugar de cumplimiento de la prestación (contratos), el del hecho (responsabilidad extracontractual) o el de radicación del inmueble (bienes inmuebles). Verificar la circunscripción judicial correspondiente antes de radicar.]

**AREAS_PRACTICA:** [COMPLETAR: Ej. "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, contratación pública, IPPV, organismos municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: Ej. "Ministerio de Salud Río Negro, IPROSS, Municipalidad de Viedma, Municipalidad de Bariloche, DGR Río Negro".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Río Negro: procedimiento administrativo ante la Administración provincial y municipal (Ley A-2938), recursos administrativos en sede provincial, acción contencioso administrativa ante los Juzgados en lo Contencioso Administrativo (Ley 5773, vigente desde 23/12/2024, que derogó la Ley P-4142), responsabilidad del Estado provincial, empleo público y contratación pública.

**Alerta crítica - NUEVO CÓDIGO [CONFIRMADO]:** la **Ley 5773** (sancionada 18/12/2024, promulgada 23/12/2024, B.O.P. N° 6348 extra, 23/12/2024) derogó la anterior Ley P-4142 y entró en vigor de inmediato. Fue modificada parcialmente por la Ley 5780 (arts. 23 y 26, B.O. 10/03/2025). Todo escrito debe verificar que aplica el régimen de la Ley 5773. La jurisprudencia anterior a diciembre 2024 corresponde al régimen derogado; evaluar su aplicabilidad caso por caso.

**Estructura judicial [CONFIRMADO]:**
- **Juzgados en lo Contencioso Administrativo:** competencia territorial, a elección del actor (domicilio del actor en la provincia o del demandado; y opciones específicas para contratos, responsabilidad extracontractual e inmuebles). Las Cámaras en lo Civil, Comercial, Familia, de Minería y Contencioso Administrativo mantienen transitoriamente la competencia administrativa que detentaban (arts. transitorios Ley 5773).
- **Alzada (régimen transitorio confirmado - art. transitorio Ley 5773):** hasta que funcionen las Cámaras específicas del fuero CA, la revisión de las sentencias de los Juzgados CA corresponde a la Cámara de Apelaciones civil/comercial de cada circunscripción:
  - **1ª Circunscripción (Viedma):** Cámara de Apelaciones en lo Civil, Comercial, Minería y de Familia de Viedma.
  - **2ª Circunscripción (General Roca):** Cámara de Apelaciones en lo Civil, Comercial y de Minería de General Roca.
  - **3ª Circunscripción (Bariloche):** Cámara de Apelaciones en lo Civil, Comercial y de Minería de San Carlos de Bariloche.
  - **4ª Circunscripción (Cipolletti):** Cámara de Apelaciones en lo Civil, Comercial y de Minería de Cipolletti.
- El STJ Río Negro no actúa como instancia ordinaria de apelación; se limita a casación e inconstitucionalidad.
- **Tribunal Superior:** Superior Tribunal de Justicia de Río Negro (STJ Río Negro).

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Río Negro (ARCA/ex AFIP, ANSES), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal rionegrina, aplica este perfil.

**Tercer nivel - organismos municipales [CONFIRMADO]:** son competentes los tribunales contencioso administrativos (art. 1 Ley 5773). El agotamiento de la vía ante actos municipales se rige por "la normativa municipal respectiva" (art. 6 Ley 5773). Verificar si el municipio tiene ordenanza de procedimiento propio.

---

## Bloque 2 - Normas base

### 2.1 Procedimiento administrativo - Ley A-2938

**[CONFIRMADO]** Norma principal: Ley A-2938 (Ley de Procedimiento Administrativo de la Provincia de Río Negro). El agotamiento de la vía se rige por el Título VII de esta ley (art. 6 Ley 5773).

**Texto vigente:** https://www.jusnorionegro.gov.ar o Boletín Oficial de Río Negro. Verificar modificaciones posteriores.

```
[VERIFICAR VIGENCIA: Ley A-2938 LPA Río Negro - consultar Boletín Oficial Río Negro antes de aplicar - verificar Título VII (agotamiento de la vía)]
```

### 2.2 Proceso contencioso administrativo - Ley 5773 (vigente desde 23/12/2024)

**[CONFIRMADO]** Norma: Ley 5773 (Código Procesal Administrativo de la Provincia de Río Negro, sancionada 18/12/2024, promulgada 23/12/2024, B.O.P. N° 6348 extra).

**[CONFIRMADO]** Modificaciones: Ley 5780 (B.O. 10/03/2025) modificó los arts. 23 y 26 de la Ley 5773.

**Derogación:** derogó la Ley P-4142 (anterior código) al entrar en vigor.

**[CONFIRMADO]** Subsidiariedad: el Código Procesal Civil y Comercial de Río Negro aplica supletoriamente en todo lo no previsto.

**Texto vigente:** https://web.legisrn.gov.ar (Ley 5773) y https://servicios-publico.jusrionegro.gov.ar.

### 2.3 Silencio administrativo y denegación tácita

**[CONFIRMADO]** Regla (art. 11 Ley 5773): cuando la vía administrativa se agota por denegatoria por silencio, la acción puede interponerse en cualquier momento antes de la prescripción. No hay plazo de caducidad para la denegación tácita — misma lógica que Neuquén.

Sin reforma análoga al Dec 971/2024 nacional para el Estado provincial: Río Negro no adoptó el régimen de silencio positivo de la Ley 27.742 nacional respecto del Estado provincial. El art. 18 de la Ley A-2938 regula el silencio en sede administrativa.

### 2.4 Plazo de caducidad para accionar judicialmente

**[CONFIRMADO — DATO MÁS CRÍTICO]**

- **Plazo general:** **30 días hábiles** desde que la resolución que agota la instancia administrativa fue notificada al interesado (art. 11 Ley 5773).
- **Resolución tácita (silencio):** la acción puede interponerse en cualquier momento antes de la prescripción (art. 11 in fine Ley 5773).
- **Naturaleza:** la caducidad de la acción procesal administrativa es excepción de previo y especial pronunciamiento (art. 17 inc. d Ley 5773). El archivo del expediente procede ante su procedencia (art. 17 in fine Ley 5773).
- **¿Declarable de oficio?:** sí, verificable de oficio en la admisión del proceso (art. 14 Ley 5773).

```
[ALERTA PLAZO FATAL: art. 11 Ley 5773 CPA Río Negro - 30 días hábiles desde notificación de la resolución que agota la vía - EXCEPCIÓN: si la vía se agotó por silencio, la acción puede interponerse en cualquier momento antes de la prescripción - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes:**

| Régimen | Plazo (vía expresa) | Silencio | Norma |
|---------|---------------------|---------|-------|
| **Río Negro** | **30 días hábiles** | Sin caducidad (antes prescripción) | Ley 5773 art. 11 |
| Neuquén | 30 días corridos (no feria; inhábil → primer hábil) | Sin caducidad (antes prescripción) | Ley 1305 art. 10 |
| Córdoba | 30 días hábiles judiciales | - | Ley 7182 art. 8 |
| Mendoza | 30 días corridos | - | Ley 3918 art. 20 |
| Salta | 30 días hábiles judiciales | - | Ley 793 art. 12 |
| Santa Fe | 30 días (A verificar) | - | Ley 11.330 art. 9 |
| Corrientes | 60 días hábiles judiciales | - | Ley 3460 art. 223 |
| Misiones | 60 días corridos (sin ferias) | - | Ley I-95 art. 24 |
| PBA | 90 días hábiles judiciales | - | Ley 12.008 art. 18 |
| CABA | 90 días hábiles judiciales | - | Ley 189 art. 7 |
| Tucumán | 90 días hábiles judiciales | - | Ley 6205 art. 9 |
| Entre Ríos | 1 año corridos | - | Ley 7061 art. 19 |
| Federal (post-9-jul-2024) | 180 días hábiles judiciales | - | LNPA art. 25 |

### 2.5 Recursos administrativos (Ley A-2938, Título VII)

**[CONFIRMADO] Recurso de reconsideración (art. 114 Ley A-2938):**
- Plazo: **10 días hábiles administrativos** desde el día siguiente a la notificación del acto.
- Lleva implícito el recurso jerárquico en subsidio.

**[CONFIRMADO] Recurso jerárquico autónomo (art. 119 Ley A-2938):**
- Plazo: **15 días hábiles administrativos** si se opta por interponerlo directamente sin reconsideración previa.
- Se presenta ante la misma autoridad que dictó el acto, para que la eleve al superior (Ministro o Gobernador).

**[CONFIRMADO] Recurso de alzada (art. 124 Ley A-2938):**
- Para impugnar actos definitivos de entes autárquicos o descentralizados.
- Plazo: **15 días hábiles administrativos**.

**[CONFIRMADO] Cómputo:** todos los plazos en días se computan como días hábiles administrativos.

**Sin reforma análoga al Decreto 695/2024 nacional:** Río Negro no duplicó los plazos de recursos administrativos.

```
[ALERTA PLAZO FATAL: recurso de reconsideración - Ley A-2938 art. 114 - 10 días hábiles administrativos desde notificación - lleva implícito jerárquico en subsidio - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico autónomo - Ley A-2938 art. 119 - 15 días hábiles administrativos - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de alzada (entes descentralizados) - Ley A-2938 art. 124 - 15 días hábiles administrativos - vencimiento: calcular]
```

### 2.6 Excepciones al agotamiento de la vía

**[CONFIRMADO]** No es necesario el agotamiento en (art. 7 Ley 5773):
- (a) Repetición de lo pagado al Estado (salvo norma especial).
- (b) Desalojo o interdicto posesorio contra el Estado.
- **(c) Nulidad fundada en inconstitucionalidad de la norma que motiva el acto.**
- **(d) Daños y perjuicios por responsabilidad extracontractual o actividad lícita del Estado.**
- (e) Cobro de haberes, tutela sindical, accidentes de trabajo y enfermedades profesionales (Ley P-5631).
- (f) Ejecución de deuda reconocida o documentada en título cambiario o instrumento público.

**Nota relevante:** en los supuestos a, b, c y d, antes del traslado de la demanda, el juez da intervención a la Comisión de Transacciones Judiciales (art. 7 Ley 5773, art. 9 Ley K-3233).

### 2.6 Competencia territorial (art. 3 Ley 5773)

**[CONFIRMADO]** A elección del actor, es competente el tribunal correspondiente a:
- Su domicilio (cuando sea en la provincia) **o** al del demandado.
- Lugar de cumplimiento de la prestación característica (contratos administrativos).
- Lugar del hecho (responsabilidad extracontractual personal).
- Lugar de radicación del bien (controversias sobre inmuebles).

La competencia puede prorrogarse por acuerdo de partes.

### 2.7 Tabla unificada de plazos

| Recurso / instituto | Plazo | Tipo | Norma | Estado |
|---------------------|-------|------|-------|--------|
| Reconsideración (con jerárquico en subsidio) | 10 días | Hábiles administrativos | Ley A-2938 art. 114 | [CONFIRMADO] |
| Jerárquico autónomo | 15 días | Hábiles administrativos | Ley A-2938 art. 119 | [CONFIRMADO] |
| Alzada (entes descentralizados) | 15 días | Hábiles administrativos | Ley A-2938 art. 124 | [CONFIRMADO] |
| Acción (vía agotada por resolución expresa) | 30 días | Hábiles | Ley 5773 art. 11 | [CONFIRMADO] |
| Acción (vía agotada por silencio) | Sin caducidad (antes de la prescripción) | - | Ley 5773 art. 11 | [CONFIRMADO] |
| Recurso directo (leyes especiales) | 30 días desde notificación del acto | - | Ley 5773 art. 9 | [CONFIRMADO] |
| Contestación de demanda | 30 días | - | Ley 5773 art. 14 | [CONFIRMADO] |
| Condena a hacer (Estado) | 60 días hábiles o plazo judicial | - | Ley 5773 art. 23 (mod. Ley 5780) | [CONFIRMADO] |
| Sentencia | 40 días desde estado | - | Ley 5773 art. 21 | [CONFIRMADO] |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial. Los 30 días del art. 11 son días hábiles judiciales.

### 2.8 Agotamiento de la vía administrativa

**[CONFIRMADO]** Regla general (art. 6 Ley 5773): previo a promover la pretensión procesal, debe haberse recorrido las vías previstas en el Título VII de la Ley A-2938, o las normativas especiales o la normativa municipal respectiva, a fin de obtener un acto administrativo definitivo que cause estado.

**[CONFIRMADO]** Congruencia (art. 8 Ley 5773): las acciones deben versar sobre las cuestiones planteadas previamente en las reclamaciones o recursos administrativos.

**[CONFIRMADO]** Reparación por acto ilegítimo (art. 10 Ley 5773): no puede demandarse autónomamente la reparación de daños por actos administrativos que se reputen ilegítimos sin haber impugnado en tiempo y forma el acto lesivo.

```
[VERIFICAR AGOTAMIENTO DE VÍA RÍO NEGRO: Ley A-2938 Título VII + Ley 5773 arts. 6, 7, 8 y 10 - verificar cadena recursiva completa y si la resolución que agota la vía fue notificada - determinar si se agotó por resolución expresa (30 días hábiles) o por silencio (sin plazo de caducidad)]
```

### 2.9 Tutela cautelar

**[CONFIRMADO]** Régimen cautelar (art. 12 Ley 5773): aplican las disposiciones del Código Procesal Civil y Comercial de Río Negro. No aplica la Ley 26.854 nacional (que rige solo contra el Estado nacional).

### 2.10 Ejecución de sentencias contra el Estado (art. 26 Ley 5773, mod. Ley 5780)

**[CONFIRMADO]** Si la sentencia condena al Estado provincial al pago de sumas de dinero:
- Aplica el art. 55 de la Constitución Provincial.
- El presupuesto anual determina el monto para el pago de sentencias firmes.
- Fecha de corte para incluir sentencias en el presupuesto inmediato posterior: **31 de agosto** de cada año.
- Los pagos siguen el orden cronológico de sentencias firmes durante el ejercicio fiscal inmediato.
- Vencido el ejercicio fiscal sin pago: se habilita la ejecución directa.
- No procede el embargo preventivo contra el Sector Público Provincial. El embargo de sentencia ejecutable se hace sobre la cuenta de Rentas Generales Provinciales.

### 2.11 Acción por mora administrativa (arts. 28-29 Ley 5773)

**[CONFIRMADO]** Procede cuando vence el plazo para pronunciarse y el interesado no optó por el silencio negativo (art. 18 Ley A-2938).

Trámite: el juez da intervención al órgano remiso por 5 días hábiles para que informe las causas de la demora. Las resoluciones en el trámite son irrecurribles.

### 2.12 Tabla de responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| Juzgados CA (primera instancia) | Fiscalía de Estado de Río Negro | Ley 5773 arts. 15 y 22 |
| Cámara (alzada) | Fiscalía de Estado de Río Negro | Ley 5773 art. 22 |
| STJ Río Negro | Fiscalía de Estado de Río Negro | - |
| Notificaciones a la Fiscalía de Estado | Domicilio electrónico en sistema de gestión judicial del STJ / sede domicilio legal hasta registro en el sistema | Ley 5773 art. 15 |

**[CONFIRMADO]** La Fiscalía de Estado es **parte necesaria y legítima** en todo proceso en que se controviertan intereses de la Provincia y sus entes descentralizados (art. 15 Ley 5773).

```
[VERIFICAR NOTIFICACIÓN FISCALÍA DE ESTADO RÍO NEGRO: verificar si está registrada en el sistema de gestión judicial del STJ para notificación electrónica; si no, notificar en sede domicilio legal - art. 15 Ley 5773]
```

### 2.13 Responsabilidad del Estado provincial

**[CONFIRMADO]** Sin ley propia equivalente a Ley 26.944 nacional. La Ley 26.944 no aplica al Estado provincial rionegrino.

**[CONFIRMADO]** Excepción al agotamiento: las acciones de daños y perjuicios por responsabilidad extracontractual o actividad lícita del Estado no requieren agotamiento de la vía administrativa (art. 7 inc. d Ley 5773).

**[CONFIRMADO]** Límite: no puede demandarse autónomamente la reparación de daños por actos administrativos ilegítimos sin haber impugnado el acto en tiempo y forma (art. 10 Ley 5773).

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD RÍO NEGRO: sin ley propia - verificar si el daño es extracontractual puro (no requiere agotamiento, art. 7 inc. d) o deriva de acto ilegítimo (requiere impugnar el acto previo, art. 10) - jurisprudencia STJ Río Negro]
```

### 2.14 Empleo público Río Negro

**[CONFIRMADO]** Estatuto general: **Ley L-1844** (Estatuto y Escalafón del Personal de la Administración Pública de Río Negro) y modificatorias (entre ellas Ley L-4541). Regula ingreso por concurso, estabilidad, deberes, prohibiciones y procedimiento sumarial disciplinario del personal del Poder Ejecutivo Provincial.

**[CONFIRMADO]** Los conflictos laborales en el ámbito del art. 1 Ley 5773 (Estado como empleador) son competencia del fuero laboral exclusivamente si corresponden al art. 209 de la Constitución Provincial (art. 4 Ley 5773).

### 2.15 Contratación pública Río Negro

**[CONFIRMADO]** Norma marco: **Ley H-3186** (Ley de Administración Financiera y Control Interno de Río Negro), Capítulo VI (régimen de contrataciones). No existe una ley autónoma de compras: el régimen está integrado en la ley de administración financiera.

**[CONFIRMADO]** Reglamentación operativa: **Decreto H-1737/98** (Reglamento de Contrataciones) y sus actualizaciones, incluyendo el Decreto 123/19 (compras y firmas electrónicas).

```
[VERIFICAR VIGENCIA: Ley H-3186 Capítulo VI + Decreto H-1737/98 Río Negro - los montos de licitación pública/privada/contratación directa se actualizan por decreto - consultar Boletín Oficial de Río Negro antes de encuadrar el procedimiento]
```

---

## Bloque 3 - Alertas críticas

### Alerta 1 - Nuevo código vigente desde 23/12/2024

**[CONFIRMADO]** La Ley 5773 rige desde el 23/12/2024. Toda jurisprudencia anterior a esa fecha corresponde al régimen de la Ley P-4142 (derogada). Evaluar la aplicabilidad de la jurisprudencia previa al nuevo texto antes de citarla. La Ley 5780 (03/2025) modificó los arts. 23 y 26.

### Alerta 2 - Plazo de 30 días hábiles, con excepción por silencio

**[CONFIRMADO]** Dos regímenes coexisten:
- **Resolución expresa:** 30 días hábiles desde la notificación.
- **Silencio:** sin plazo de caducidad; antes de la prescripción.

Determinar cómo se agotó la vía antes de computar cualquier plazo.

```
[ALERTA PLAZO FATAL: art. 11 Ley 5773 CPA Río Negro - si vía agotada por resolución EXPRESA: 30 días hábiles desde notificación - si vía agotada por SILENCIO: sin plazo de caducidad (antes de la prescripción) - determinar primero cómo se agotó la vía]
```

### Alerta 3 - Alzada: Cámaras civiles por circunscripción (transitorio)

**[CONFIRMADO]** Hasta que funcionen las Cámaras CA específicas, la alzada de los Juzgados CA es la Cámara Civil y Comercial de cada circunscripción (Viedma, General Roca, Bariloche, Cipolletti). El STJ actúa solo en casación e inconstitucionalidad. Identificar la circunscripción judicial del juzgado antes de apelar.

### Alerta 4 - Fiscalía de Estado: parte necesaria

**[CONFIRMADO]** La Fiscalía de Estado es parte necesaria y legítima en todo proceso contra la Provincia. Su omisión puede afectar la regularidad del proceso. Verificar notificación (electrónica si está en el sistema; papel en sede si no lo está).

### Alerta 4 - Responsabilidad extracontractual: no requiere agotamiento

**[CONFIRMADO]** Las acciones del art. 7 inc. d (daños por responsabilidad extracontractual o actividad lícita) no requieren agotamiento de la vía administrativa. Pero si el daño proviene de un acto ilegítimo, sí se requirió impugnar el acto en tiempo y forma (art. 10). Distinguir ambos supuestos antes de articular la pretensión.

---

## Bloque 4 - Checklists operativos

### Checklist: acto administrativo

1. ¿El acto es del Estado provincial, de un municipio o de un organismo federal?
2. ¿El acto fue notificado? ¿En qué fecha?
3. ¿La vía se agotó por resolución expresa (30 días hábiles) o por silencio (sin plazo)?
4. ¿Hay expediente administrativo? ¿El abogado lo tiene?
5. ¿Se agotaron los recursos del Título VII Ley A-2938?
6. ¿Las pretensiones coinciden con lo planteado en sede administrativa? (art. 8 Ley 5773)
7. ¿La demanda involucra responsabilidad extracontractual o actividad lícita? (excepción art. 7 inc. d)

### Checklist: acción judicial

1. Determinar cómo se agotó la vía.
2. Si fue por resolución expresa: calcular **30 días hábiles** desde la notificación (art. 11 Ley 5773).
3. Si fue por silencio: la acción puede interponerse en cualquier momento antes de la prescripción.
4. Determinar la circunscripción judicial competente según la opción territorial del art. 3.
5. Verificar que la Fiscalía de Estado sea notificada correctamente (electrónica o papel según el caso).
6. En daños por actividad lícita o responsabilidad extracontractual: verificar si aplica la excepción del art. 7 inc. d.
7. En daños por acto ilegítimo: verificar que el acto fue impugnado en tiempo y forma (art. 10).

### Checklist: responsabilidad del Estado

1. Distinguir: ¿daño extracontractual puro (art. 7 inc. d, sin agotamiento) o daño por acto ilegítimo (art. 10, requiere impugnar el acto)?
2. No aplicar Ley 26.944 ni CCCN sin verificar criterio del STJ Río Negro.
3. Antes del traslado en supuestos del art. 7 incs. a, b, c y d: el juez da intervención a la Comisión de Transacciones Judiciales.

### Checklist: empleo público

1. Verificar si el conflicto es laboral (fuero laboral, art. 209 Const.) o administrativo (fuero CA).
2. Identificar estatuto aplicable.
3. Situación de revista del agente.
4. ¿Hubo sumario con garantías de debido proceso?

### Checklist: ejecución de sentencia contra el Estado

1. ¿Hay condena a pagar suma de dinero? Verificar los plazos y mecanismo del art. 26 Ley 5773 (mod. Ley 5780) y art. 55 Constitución Provincial.
2. ¿Hay condena a hacer? Plazo para el Estado: 60 días hábiles o plazo judicial (art. 23 Ley 5773 mod. Ley 5780).
3. No procede embargo preventivo contra el Sector Público Provincial.

---

## Fuentes primarias

- **Legislatura de Río Negro (leyes):** https://web.legisrn.gov.ar
- **Poder Judicial de Río Negro:** https://jusrionegro.gov.ar
- **Boletín Oficial Río Negro:** https://www.rionegro.gov.ar/boletin-oficial
- **Texto Ley 5773:** https://web.legisrn.gov.ar/legislativa/legislacion/documento?id=10966
- **Fiscalía de Estado Río Negro:** https://www.rionegro.gov.ar/fiscalia-de-estado

---

## Reglas de citación - administrativo Río Negro

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente.

**Jurisprudencia:** toda jurisprudencia anterior al 23/12/2024 corresponde al régimen de la Ley P-4142 (derogada). Evaluar aplicabilidad al nuevo régimen antes de citar. Usar:
```
[INSERTAR FALLO VERIFICADO: STJ Río Negro / Cámara CA [circunscripción] / Juzgado CA [circunscripción] - doctrina requerida - verificar si es bajo Ley P-4142 (derogada) o Ley 5773 (vigente desde 23/12/2024)]
```

**Plazos:** no transpolar plazos de otros regímenes. Usar:
```
[ALERTA PLAZO FATAL: art. 11 Ley 5773 CPA Río Negro - vía agotada por resolución expresa: 30 días hábiles / vía agotada por silencio: sin plazo de caducidad - vencimiento: calcular]
```

---

*Última actualización: mayo 2026*
*Normativa base: Ley A-2938 LPA Río Negro, Ley 5773 (Código Procesal Administrativo, vigente desde 23/12/2024, mod. Ley 5780), Constitución de Río Negro arts. 55 y 209*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
