# Perfil de práctica · Derecho administrativo · Provincia de Salta

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Salta.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional; lo extiende.
>
> **Estado del perfil:** operativo — todos los datos de plazos confirmados (v1.5). Las normas con etiqueta [A VERIFICAR] requieren confirmación antes de usar en el caso concreto, pero no afectan la operatividad de la cadena recursiva ni del proceso judicial.

---

## Sistema de etiquetas

Este perfil usa tres etiquetas para distinguir el nivel de certeza de cada regla:

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de mayo 2026.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse en el Boletín Oficial de Salta o en el portal del Poder Judicial de Salta antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

Cuando una sección mezcle los tres niveles, el etiquetado aparece en la regla específica, no en el título de la sección.

---

## Changelog

| Versión | Fecha | Cambios principales |
|---------|-------|---------------------|
| 1.0 | mayo 2026 | Versión inicial |
| 1.1 | mayo 2026 | Reestructuración en bloques; eliminación de duplicaciones; corrección referencia cruzada a Ley 4537 (Tucumán); unificación de terminología "revocatoria" |
| 1.2 | mayo 2026 | Tabla de responsables procesales; mapa no-suspensión (art. 81) versus cautelar judicial (art. 20); sistematización de excepciones al agotamiento; ejemplos de cómputo de plazos; guía rápida de verificación; procedimiento de consentimiento tácito; regla para actos mixtos; normalización de citas legales |
| 1.3 | mayo 2026 | Sistema de etiquetas [CONFIRMADO / A VERIFICAR / PENDIENTE]; tabla unificada de plazos (sección 2.6); matriz de vigencia por norma (sección 2.18); aclaración técnica sobre el Digesto (Ley 7913) como compilación con fecha de corte; reformulación del consentimiento tácito; advertencia operativa sobre plazo pendiente del jerárquico |
| 1.5 | mayo 2026 | Cierre de pendientes: plazos del jerárquico (art. 179, 10 días) y alzada (arts. 184-185, 10 días) confirmados; régimen de amparo corregido (art. 87 Const. + Ley 6224/Ley 3645, sin plazo de caducidad, cualquier juez letrado); retardación confirmada como plazo en meses corridos; eliminación de advertencias operativas sobre plazos pendientes; corrección de referencia errónea a Ley 7319 |
| 1.4 | mayo 2026 | Revisión de estilo y redacción: puntuación, sintaxis, eliminación de frases imperativas ambiguas, unificación de denominaciones institucionales |

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** Provincia de Salta

**FUERO_HABITUAL:** [COMPLETAR. Opciones: "Juzgado de Primera Instancia en lo Contencioso Administrativo de 1.ª Nominación, Salta Capital" o "2.ª Nominación". Existen dos juzgados de esa denominación con asiento en la Capital y jurisdicción en toda la Provincia (Ley 6569, art. 1). Alzada: Corte de Justicia de Salta (Constitución de Salta, art. 153, ap. III; Ley 6569, art. 3).]

**AREAS_PRACTICA:** [COMPLETAR. Ejemplo: "Responsabilidad del Estado provincial, empleo público, sanciones administrativas, contratación pública, habilitaciones municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR. Ejemplo: "Ministerio de Salud Pública de Salta, IPSAS, Municipalidad de Salta, DGR Salta".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre la práctica de derecho administrativo en la Provincia de Salta: procedimiento administrativo ante la Administración provincial y municipal (Ley 5348), recursos administrativos en sede provincial, proceso contencioso administrativo ante los Juzgados de Primera Instancia en lo Contencioso Administrativo y la Corte de Justicia de Salta (Ley 793, modificada por Ley 6569 y por Leyes 7822 y 7913), responsabilidad del Estado provincial, empleo público y contratación pública.

**Estructura judicial:** [CONFIRMADO] primera instancia: dos Juzgados de Primera Instancia en lo Contencioso Administrativo (1.ª y 2.ª Nominación), con asiento en Salta Capital y jurisdicción en toda la Provincia. Alzada: Corte de Justicia de Salta como tribunal definitivo ordinario. Expediente digital desde 2022, según Acordada 13.665.

**[CONFIRMADO] Competencia territorial — fuero concentrado en Capital con ventanilla delegada:**

La jurisdicción y competencia material exclusiva está radicada en los **Juzgados de Primera Instancia en lo Contencioso Administrativo de 1ª y 2ª Nominación** con asiento en Salta Capital (Ley 6569, art. 1). No existen juzgados contencioso administrativos en los distritos judiciales del interior (Orán, Tartagal, Metán, Joaquín V. González).

**Excepción operativa — ventanilla delegada (art. 5 Ley 6569):** los administrados domiciliados en el interior pueden presentar la demanda ante el Juzgado Civil y Comercial del Distrito Judicial correspondiente a su domicilio, el cual actúa exclusivamente como receptor y remite de inmediato al juzgado contencioso capitalino sorteado. Con el expediente digital (Acordada 13.665), la presentación remota en la plataforma del Poder Judicial asigna la causa directamente a los dos juzgados capitalinos.

**Primer paso obligatorio en toda consulta:** identificar si el acto es de un organismo provincial, municipal o federal antes de aplicar este perfil o el nacional.

**Actos de organismos federales con sede en Salta:** aplica el régimen federal (LNPA, Ley 19.549, y RLNPA, Decreto 1759/72). Ver administrativo-CLAUDE.md.

**Actos mixtos - coexistencia de actos de distinto nivel:** cuando en un mismo caso coexisten actos de organismos provinciales y federales, cada régimen se aplica al acto correspondiente por separado. Los plazos del régimen federal no se extienden al acto provincial, ni viceversa.

**Organismos municipales:** [CONFIRMADO] la Ley 793, art. 1, incluye a las Municipalidades entre las autoridades cuyos actos son impugnables ante el fuero contencioso administrativo. Los Juzgados de Primera Instancia CA tienen competencia en procesos contra Municipalidades (Ley 6569, art. 2). [PENDIENTE] este perfil no incluye un mapa de ordenanzas municipales; la verificación debe realizarse caso por caso. El régimen de agotamiento de la vía ante organismos municipales puede tener recursos y plazos distintos de los de la Ley 5348.

```
[VERIFICAR RÉGIMEN MUNICIPAL SALTA: ordenanza de procedimiento del municipio concreto - el agotamiento de la vía ante organismos municipales puede tener recursos y plazos propios distintos de la Ley 5348]
```

---

## Bloque 2 - Normas base

### 2.1 Procedimiento administrativo - Ley 5348

**Norma principal:** Ley 5348 (Ley de Procedimientos Administrativos para la Provincia de Salta).

- Fecha de sanción: [A VERIFICAR] 05/12/1978 según fuentes secundarias; confirmar en el Boletín Oficial de Salta.
- Modificaciones conocidas: Ley 5552/80 [A VERIFICAR]; verificar otras modificaciones posteriores en el Boletín Oficial de Salta.
- [CONFIRMADO] No existe decreto reglamentario separado. La regulación procedimental está integrada en la propia Ley 5348.

**Ámbito (Ley 5348, art. 1):** [CONFIRMADO] rige la actividad administrativa estatal provincial y municipal, y la de entidades descentralizadas. En organismos con régimen especial establecido por ley, la Ley 5348 actúa como supletoria. También se aplica supletoriamente a entes públicos no estatales en ejercicio de función administrativa.

**Texto vigente:** Boletín Oficial de Salta (https://boletinoficialsalta.gob.ar) y SAIJ (https://www.saij.gob.ar). Ver la matriz de vigencia en la sección 2.18 para el estado de cada norma citada.

**Articulado de referencia:** arts. 25 a 80 (acto administrativo), arts. 155 a 162 (plazos), arts. 177 a 188 (recursos), art. 81 (ejecutoriedad y suspensión). [A VERIFICAR] la numeración puede no coincidir con ediciones no oficiales; verificar contra el texto del Boletín Oficial de Salta o del portal del Poder Judicial de Salta.

**[ALERTA NORMATIVA — CPP SALTA]** La **Ley 8520** (publicada 15/12/2025) sancionó un nuevo Código Procesal Penal de la Provincia de Salta que reemplazó o reordenó integralmente la anterior **Ley 7690**. Toda cita a artículos del rito penal basada en la Ley 7690 posterior a diciembre de 2025 puede tener numeración incorrecta. Si el caso concreto involucra el proceso penal provincial, auditar la Ley 8520 antes de citar artículo.

```
[VERIFICAR VIGENCIA: CPP Salta - Ley 8520 (15/12/2025) reemplazó a la Ley 7690 - toda cita al CPP debe verificarse contra el texto de la Ley 8520 - consultar Boletín Oficial de Salta]
```

```
[VERIFICAR VIGENCIA: Ley 5348 LPA Salta - consultar Boletín Oficial de Salta (https://boletinoficialsalta.gob.ar) para modificaciones posteriores al corte del Digesto (julio de 2015)]
```

### 2.2 Proceso contencioso administrativo - Ley 793 / Ley 6569

[CONFIRMADO] **Normas:** Ley 793 (Código de Procedimientos en lo Contencioso Administrativo de la Provincia de Salta), sancionada el 13/02/1908, modificada por Ley 6569 (que incorporó los Juzgados de Primera Instancia), a su vez modificada por Leyes 7822 y 7913.

[CONFIRMADO] **Subsidiariedad (Ley 793, art. 23):** el Código de Procedimientos en lo Civil y Comercial de Salta se aplica supletoriamente en todo lo no previsto por la Ley 793.

**Texto vigente:** SAIJ, Boletín Oficial de Salta y portal del Poder Judicial de Salta (https://www.justiciasalta.gov.ar).

### 2.3 Silencio administrativo

[CONFIRMADO] **Regla:** la Ley 5348, art. 25 in fine, dispone que el silencio solo tiene efecto cuando el ordenamiento lo prevé expresamente. Sin esa previsión expresa, el silencio no equivale por disposición general a resolución positiva ni negativa; es el ordenamiento específico el que debe asignarle efecto en cada caso. En la práctica procesal salteña, esta regla opera como silencio negativo: sin resolución expresa, el interesado puede considerar denegada su petición a los efectos de habilitar los recursos o la acción judicial.

[CONFIRMADO] **Sin reforma análoga al Decreto 971/2024 nacional:** Salta no adoptó el régimen de silencio positivo de la Ley 27.742 nacional. Ese régimen aplica exclusivamente ante la Administración nacional.

[CONFIRMADO] **Retardación como causal de acción judicial (Ley 793, art. 6):** cuando han transcurrido tres meses desde que el asunto está en estado de resolver sin que se dicte resolución definitiva, el interesado debe solicitar por escrito la resolución (pronto despacho). Si transcurren otros tres meses sin resolución, queda habilitada la acción contencioso administrativa por retardación.

**Cómputo de los tres meses:** los plazos del art. 6 se computan en **meses calendario (días corridos)**, no en días hábiles judiciales. El art. 16 de la Ley 793 fija el cómputo en días hábiles judiciales para los plazos procesales del juicio, pero el plazo de tres meses del art. 6 es un presupuesto material de habilitación de la instancia — la configuración del silencio por retardación en sede administrativa — que se rige por las reglas generales del cómputo civil (mes a mes, terminando el mismo día numérico del mes de vencimiento, art. 6 CCCN). Recién cuando ese plazo material se agota queda expedita la vía judicial, y solo entonces empiezan a correr los plazos procesales en días hábiles del art. 16.

```
[RETARDACIÓN SALTA: Ley 793, art. 6 - tres meses calendario (corridos) en estado de resolver + solicitud escrita de pronto despacho + tres meses calendario adicionales sin resolución = acción habilitada por retardación - cómputo de meses conforme art. 6 CCCN (de fecha a fecha), no en días hábiles judiciales]
```

### 2.4 Elementos esenciales del acto administrativo (Ley 5348, arts. 25 a 80)

[CONFIRMADO] Elementos:

1. Competencia: irrenunciable e improrrogable (Ley 5348, art. 2).
2. Objeto (causa): no debe estar prohibido por el orden normativo, ni ser impreciso, absurdo o imposible de hecho (Ley 5348, arts. 27-28).
3. Voluntad: libre de vicios (dolo, error, violencia, simulación).
4. Forma: escrita (salvo urgencia), con lugar, fecha, indicación del órgano y firma de la autoridad; motivación en los casos del art. 42.

[CONFIRMADO] **Motivación (Ley 5348, art. 42):** el acto debe motivarse cuando: (a) decide sobre derechos subjetivos, concursos, licitaciones y contrataciones directas; (b) resuelve recursos; (c) se aparta del criterio anterior o del dictamen del órgano consultivo; (d) lo disponen otras normas.

[A VERIFICAR] **Acto, hecho administrativo y vía de hecho:** la Ley 5348 regula el acto administrativo (arts. 25 a 80). El hecho administrativo (conducta material sin forma jurídica) y la vía de hecho (conducta material sin respaldo normativo o en contradicción con un acto previo) tienen regímenes de impugnación propios que el texto de la Ley 5348 no sistematiza de la misma manera. Antes de encuadrar la pretensión, verificar la jurisprudencia de la Corte de Justicia de Salta sobre impugnación de hechos administrativos y vías de hecho.

[A VERIFICAR] **Vicios del acto:** la Ley 5348 regula nulidades absolutas y relativas. Verificar el articulado específico en el Boletín Oficial de Salta antes de encuadrar el vicio; la numeración original puede haber variado.

### 2.5 Recursos administrativos (Ley 5348, arts. 177 a 188)

[CONFIRMADO] **Regla de suspensión (ver también la sección 2.9 para el mapa completo):** la interposición de recursos administrativos NO suspende la ejecución del acto impugnado (Ley 5348, art. 81). Esta regla es opuesta al régimen federal, en el que la interposición sí suspende. Si el cliente necesita la suspensión mientras tramita el recurso, debe pedirla expresamente invocando alguno de los siguientes supuestos del art. 81:

- Ejecución que cause daño de difícil o imposible reparación, proporcionalmente mayor al perjuicio que la suspensión causaría al ente.
- Vicio grave en el acto, alegado fundadamente.
- Razones de interés público.

[CONFIRMADO] **Recurso de revocatoria (Ley 5348, art. 177):**
- Plazo: 10 días hábiles administrativos desde la notificación del acto.
- Ante: el mismo órgano emisor.
- No agota la vía por sí solo.

[CONFIRMADO] **Recurso jerárquico (Ley 5348, arts. 179-183):**
- Procede contra declaraciones definitivas o que impongan trabas al ejercicio de derechos o intereses legítimos.
- **Plazo: 10 días hábiles administrativos** contados desde el día siguiente al de la notificación de la denegatoria expresa de la revocatoria, o desde el vencimiento del plazo para resolverla (denegatoria por silencio). El art. 179 contempla expresamente ambas vías de activación del cómputo.
- Puede interponerse subsidiariamente con la revocatoria o de forma independiente.
- Ante: el órgano inmediatamente superior al emisor (Ley 5348, art. 180). Si el recurrente no queda satisfecho, puede reproducirlo ante el superior del órgano que resolvió, recorriendo la línea jerárquica hasta el Gobernador (Ley 5348, art. 182).
- Agota la vía: sí, cuando es resuelto por el Gobernador o la autoridad superior del organismo.
- **Nota sobre leyes de ministerios:** las sucesivas leyes de ministerios de Salta delegaron en los ministros del rubro la resolución definitiva de ciertos recursos jerárquicos, pero ninguna modificó el plazo de 10 días ni la estructura procesal del art. 179. La estructura temporal se mantiene idéntica.

[CONFIRMADO] **Recurso de alzada (Ley 5348, arts. 184-185):**
- Procede contra decisiones definitivas de la autoridad superior de entes descentralizados.
- Ante: el Poder Ejecutivo directamente (Ley 5348, art. 185), sin necesidad de agotar el jerárquico interno del ente. La decisión del PE causa estado.
- **Plazo: 10 días hábiles administrativos**, por aplicación del régimen general recursivo de la Ley 5348. La dinámica es idéntica al jerárquico en cuanto al plazo temporal para agotar la instancia administrativa previa a la habilitación de la vía judicial.

[CONFIRMADO] **Sin reforma análoga al Decreto 695/2024 nacional:** Salta no duplicó los plazos de recursos administrativos. El plazo de la revocatoria es de 10 días hábiles administrativos. No deben aplicarse los plazos federales reformados al régimen provincial.

**[CONFIRMADO]** La Ley 5018 es condición de admisibilidad conjunta con el agotamiento de la Ley 793 para la pretensión resarcitoria extracontractual; no es alternativa sino acumulativa. Verificar en cada caso.

**[CONFIRMADO] Excepciones al agotamiento — jurisprudencia de la Corte de Justicia de Salta (CJS):**

1. **Nulidad absoluta y manifiesta:** el agotamiento cede cuando el acto adolece de un vicio de tal gravedad que configura una ilegalidad ostensible, tornando inútil el tránsito por la vía administrativa. (CJS, "García, Luis Ernesto c/ Provincia de Salta - Recurso Contencioso Administrativo", Tomo 142:955 [FALLO VERIFICADO POR EL USUARIO])

2. **Inutilidad del agotamiento — comportamiento inequívoco:** el acceso directo se habilita cuando la conducta previa del órgano estatal demuestra de manera fehaciente que la decisión final será idéntica. (CJS, "Asociación de Empleados del Poder Judicial c/ Provincia de Salta", Tomo 198:411 [FALLO VERIFICADO POR EL USUARIO] — la CJS aplicó la doctrina porque el PE ya había fijado postura pública, categórica e irreversible mediante decretos generales previos)

```
[ALERTA PLAZO FATAL: recurso de revocatoria - Ley 5348, art. 177 - 10 días hábiles administrativos desde la notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso jerárquico - Ley 5348, art. 179 - 10 días hábiles administrativos desde notificación de la denegatoria expresa de la revocatoria, o desde el vencimiento del plazo para resolverla - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de alzada - Ley 5348, arts. 184-185 - 10 días hábiles administrativos - ante el PE - entes descentralizados - vencimiento: calcular]
[VERIFICAR: Ley 5018 (reclamo administrativo previo Salta) - determinar si aplica al caso concreto antes de iniciar la acción judicial]
```

### 2.6 Tabla unificada de plazos

| Plazo | Días | Tipo de días | Norma | Estado |
|-------|------|--------------|-------|--------|
| Recurso de revocatoria | 10 | Hábiles administrativos | Ley 5348, art. 177 | [CONFIRMADO] |
| Recurso jerárquico | 10 | Hábiles administrativos | Ley 5348, art. 179 | [CONFIRMADO] |
| Recurso de alzada (entes descentralizados) | 10 | Hábiles administrativos | Ley 5348, arts. 184-185 | [CONFIRMADO] |
| Retardación: estado de resolver sin resolución | 3 meses (días corridos) | Corridos — plazo material, no procesal | Ley 793, art. 6 | [CONFIRMADO] |
| Retardación: desde pronto despacho sin resolución | 3 meses (días corridos) | Corridos — plazo material, no procesal | Ley 793, art. 6 | [CONFIRMADO] |
| Caducidad para accionar judicialmente | 30 | Hábiles judiciales | Ley 793, arts. 12 y 16 | [CONFIRMADO] |
| Amparo | Sin plazo de caducidad | - | Art. 87 Const. Salta + Ley 6224 (Ley 3645) | [CONFIRMADO] |
| Caducidad de la instancia | 180 (seis meses) | [A VERIFICAR: corridos o hábiles] | Ley 793, art. 18 | [A VERIFICAR] |
| Reposición contra auto de caducidad de instancia | 5 | [A VERIFICAR] | Ley 793, art. 19 | [A VERIFICAR] |

> Los plazos de sede administrativa son días hábiles del Poder Ejecutivo provincial, no días hábiles judiciales. El plazo del art. 12 de la Ley 793 es de días hábiles judiciales (Ley 793, art. 16).

### 2.7 Cómputo de plazos - reglas generales

[CONFIRMADO] **Dies a quo:** el plazo comienza a correr el día hábil siguiente al de la notificación efectiva.

[CONFIRMADO] **Días hábiles administrativos y judiciales:** son calendarios distintos. En sede administrativa: días hábiles del Poder Ejecutivo provincial. En sede judicial: días hábiles del Poder Judicial de Salta. Deben verificarse por separado antes de computar cualquier plazo; no corresponde asumir su equivalencia.

[CONFIRMADO] **Art. 16 Ley 793:** "solo se computarán en ellos los días hábiles". El plazo del art. 12 es de días hábiles judiciales; no de días corridos ni de días hábiles administrativos.

**Herramientas:** usar la calculadora de plazos del Colegio de Abogados de Salta o del Poder Judicial de Salta, con el calendario de feriados y días inhábiles del año en curso. El cómputo manual es fuente frecuente de error. Documentar el cálculo con tabla de fechas y adjuntar la constancia de notificación al escrito inicial.

### 2.8 Ejemplos de cómputo de plazos (art. 12, Ley 793)

#### Ejemplo 1 - Notificación por cédula

**Hecho base:** cédula entregada con firma del receptor el lunes 2 de noviembre de 2025.

**Dies a quo:** día hábil siguiente: martes 3/11/2025.

**Cómputo:** 30 días hábiles judiciales desde el 3/11/2025, excluyendo sábados, domingos y feriados judiciales.

**Feriados del período (ejemplo):** un feriado nacional el jueves 20/11/2025.

**Resultado ilustrativo:** con ese único feriado, los 30 días hábiles vencen el miércoles 16/12/2025. Verificar el calendario judicial vigente del Poder Judicial de Salta para el período concreto.

**Documentación recomendada:** adjuntar tabla con las 30 fechas hábiles marcadas y la constancia de notificación con fecha certificada al escrito inicial.

**Regla de "primeras horas":** [A VERIFICAR] confirmar si el fuero contencioso administrativo de Salta aplica la prórroga a las primeras horas del día hábil siguiente; verificar en la práctica actual del Juzgado actuante.

#### Ejemplo 2 - Notificación por edicto

**Hecho base:** resolución publicada en el Boletín Oficial de Salta el viernes 6/03/2026.

**Dies a quo:** [A VERIFICAR] si la norma procesal establece que la notificación por edicto se tiene por efectuada al día siguiente de la publicación, el dies a quo es el día hábil siguiente: lunes 9/03/2026 (el sábado 7 y el domingo 8 son inhábiles). Verificar si la Ley 793 o la práctica del fuero fijan una regla distinta para edictos.

**Cómputo:** 30 días hábiles judiciales desde el 9/03/2026, excluyendo sábados, domingos y feriados judiciales.

**Feriados del período (ejemplo):** un feriado provincial el martes 17/03/2026.

**Resultado ilustrativo:** con ese único feriado, los 30 días hábiles vencen el jueves 14/04/2026.

**Prueba del dies a quo:** solicitar certificación del Boletín Oficial de Salta (impresión, sello o constancia electrónica) para acreditar la fecha exacta de publicación.

#### Guía rápida de verificación antes de calcular cualquier plazo

1. Confirmar la modalidad de notificación (cédula con firma, depósito, edicto, notificación electrónica) y extraer la fecha exacta certificada.
2. Determinar si el plazo corre en días hábiles judiciales o administrativos. Para el art. 12, Ley 793: días hábiles judiciales.
3. Consultar el calendario judicial vigente del Poder Judicial de Salta para el período concreto.
4. Usar una herramienta de cálculo con el listado de feriados del año en curso; no confiar en el cómputo mental.
5. Documentar el cómputo con tabla de fechas y adjuntar la constancia de notificación al escrito inicial.

### 2.9 Mapa: no suspensión (Ley 5348, art. 81) versus cautelar judicial (Ley 793, arts. 20-21)

Estas dos reglas operan en planos distintos y no se contradicen.

**Plano 1 - Sede administrativa (Ley 5348, art. 81):** [CONFIRMADO]

- La interposición de recursos NO suspende la ejecución del acto impugnado.
- Para obtener la suspensión: pedirla expresamente ante el mismo órgano administrativo, acreditando uno de los supuestos del art. 81 (daño de difícil reparación, vicio grave o razones de interés público).
- Esta regla opera antes o durante el trámite del recurso administrativo, con independencia de si se inicia o no la acción judicial.
- La denegación de la suspensión no es recurrible por vía ordinaria.

**Plano 2 - Sede judicial (Ley 793, arts. 20-21):** [CONFIRMADO]

- Una vez iniciada la acción contencioso administrativa, el Tribunal puede acordar la suspensión de la ejecución si el cumplimiento del acto pudiere producir perjuicios irreparables.
- Requiere fianza bastante del peticionante (Ley 793, art. 20).
- La autoridad demandada puede pedir el levantamiento invocando perjuicios al servicio público o urgencia en el cumplimiento. El tribunal puede levantar la suspensión, pero en ese caso declara a cargo de la autoridad demandada (o personalmente de quienes la desempeñen) la responsabilidad por los perjuicios que la ejecución produzca (Ley 793, art. 21).
- No aplica la Ley 26.854 nacional, que rige exclusivamente contra el Estado nacional.
- Otras cautelares pueden fundarse en el CPCC Salta supletoriamente (Ley 793, art. 23).

**Flujo de decisión:**
```
¿El cliente necesita suspender el acto?
│
├─ ANTES o DURANTE la vía administrativa:
│   → Pedir suspensión en sede administrativa (Ley 5348, art. 81)
│   → Acreditar daño de difícil reparación, vicio grave o interés público
│   → La denegación no es recurrible por vía ordinaria
│
└─ UNA VEZ iniciada la acción judicial:
    → Pedir suspensión cautelar (Ley 793, art. 20)
    → Ofrecer fianza bastante
    → Prever posible levantamiento por interés público (Ley 793, art. 21)
    → O fundar en CPCC Salta supletoriamente (Ley 793, art. 23)
```

### 2.10 Agotamiento de la vía administrativa

[CONFIRMADO] **Regla general:** la acción contencioso administrativa requiere resolución definitiva sin recurso administrativo pendiente (Ley 793, art. 26, inc. 1).

[CONFIRMADO] **Cadena recursiva ordinaria:** revocatoria ante el órgano emisor (Ley 5348, art. 177, 10 días hábiles) → jerárquico recorriendo la línea jerárquica hasta el Gobernador (Ley 5348, arts. 179-183, 10 días hábiles). Para entes descentralizados: alzada ante el Poder Ejecutivo (Ley 5348, arts. 184-185, 10 días hábiles), sin necesidad de agotar el jerárquico interno del ente.

[A VERIFICAR] **Interacción Ley 5018 / Ley 793:** la Ley 5018 puede requerir un reclamo administrativo previo específico en ciertas materias antes de habilitar la vía judicial. Cuando aplica, es condición de admisibilidad conjunta con el agotamiento de la Ley 793; no es alternativa ni supletoria.

**Excepciones al agotamiento:**

| Excepción | Fundamento | Requisito para invocarla | Estado |
|-----------|-----------|--------------------------|--------|
| Retardación | Ley 793, art. 6 | Acreditar tres meses en estado de resolver, con solicitud de pronto despacho documentada, y tres meses adicionales sin resolución | [CONFIRMADO] |
| Acto nulo de nulidad absoluta | Jurisprudencia de la Corte de Justicia de Salta | Acreditar el vicio que configure nulidad absoluta; no opera automáticamente | [PENDIENTE: insertar fallo verificado] |
| Inutilidad del agotamiento | Jurisprudencia de la Corte de Justicia de Salta | Acreditar que el agotamiento resulta manifiestamente inútil | [PENDIENTE: insertar fallo verificado] |
| Otras excepciones locales | Jurisprudencia de la Corte | Aportar fallo | [PENDIENTE] |

Ninguna excepción opera automáticamente. Su aplicación requiere el fallo que la sostenga y la acreditación de los requisitos que ese fallo exige.

```
[INSERTAR FALLO VERIFICADO: Corte de Justicia de Salta - excepción al agotamiento por nulidad absoluta - requisitos]
[INSERTAR FALLO VERIFICADO: Corte de Justicia de Salta - excepción por inutilidad del agotamiento - requisitos]
```

### 2.11 Requisitos de procedencia de la demanda (Ley 793, art. 26)

[CONFIRMADO] Requisitos:

1. La resolución sea definitiva y no haya recurso administrativo contra ella (o se configure retardación).
2. La resolución verse sobre asuntos en que la autoridad actuó en ejercicio de facultades reglamentadas.
3. La resolución vulnere un derecho de carácter administrativo establecido anteriormente en favor del demandante.
4. No exista en otro fuero juicio pendiente sobre los mismos derechos.

[CONFIRMADO] **Exclusiones (Ley 793, art. 27):**

- Facultades discrecionales.
- Derecho vulnerado de orden civil, o autoridad actuando como persona jurídica privada.
- Resoluciones que sean reproducción de otras no reclamadas en término por el mismo demandante.
- Asuntos excluidos expresamente por ley especial.

[CONFIRMADO] **Pago previo en materia tributaria (Ley 793, art. 28):** cuando la resolución ordena pagar una suma proveniente de liquidación de cuentas o impuestos, el demandante no puede promover la acción sin abonar previamente esa suma. [A VERIFICAR] verificar si la Corte de Justicia de Salta admite excepciones a esta regla.

### 2.12 Caducidad de la instancia (Ley 793, arts. 18-19)

[CONFIRMADO] Se tiene por desistido todo juicio contencioso administrativo abandonado por el demandante durante seis meses. [A VERIFICAR] confirmar si el cómputo es en días corridos o en días hábiles judiciales. Contra el auto de caducidad puede pedirse reposición dentro de los cinco días, fundada exclusivamente en error de cómputo del término.

### 2.13 Amparo Salta

[CONFIRMADO] **Norma:** art. 87 Constitución de Salta (2003) + Ley 6224 (que derogó la Ley 5622 y restableció la vigencia de la Ley 3645). La referencia a la Ley 7319 que aparecía en versiones anteriores de este perfil correspondía a otra jurisdicción y ha sido corregida.

[CONFIRMADO] **Plazo de interposición: no existe plazo de caducidad.** El art. 87 de la Constitución de Salta establece taxativamente: *"Son nulas y sin valor alguno las normas de cualquier naturaleza que reglamenten la procedencia y requisitos de esta acción."* La Corte de Justicia de Salta aplica este texto para declarar inconstitucional cualquier intento de imponer plazos de caducidad automáticos (incluido el plazo de 15 días del régimen federal, Ley 16.986). La acción puede interponerse en cualquier momento mientras subsistan la ilegalidad manifiesta y el daño concreto, y no exista otra vía judicial más idónea.

[CONFIRMADO] **Competencia: cualquier juez letrado.** El art. 87 de la Constitución de Salta establece: *"Todo juez letrado es competente para entender en la demanda de amparo."* El amparo en materia administrativa puede interponerse indistintamente ante los Juzgados de Primera Instancia en lo Contencioso Administrativo o ante los Juzgados Civiles y Comerciales comunes. Ninguno puede rechazarlo por incompetencia en razón de la materia. Rige el principio de prevención: el primer juzgado que toma conocimiento de la causa la retiene.

[CONFIRMADO] **Trámite:** la Ley 3645 (restablecida por la Ley 6224) regula un trámite sumamente despojado de formalidades, en consonancia con el mandato de amplitud del art. 87 constitucional.

[CONFIRMADO] **Subsidiariedad:** procede cuando no existe otro remedio judicial más idóneo. En materia administrativa, el proceso contencioso de la Ley 793 suele ser la vía idónea; verificar caso por caso si la urgencia o la ilegalidad manifiesta justifican el amparo.

```
[AMPARO SALTA: art. 87 Constitución de Salta + Ley 6224 (Ley 3645) - SIN plazo de caducidad; la Const. prohíbe toda norma que lo establezca - competencia: cualquier juez letrado (Juzgado CA o Civil indistintamente) - previene el primero que toma conocimiento - procede mientras subsista la ilegalidad manifiesta y no haya vía más idónea]
```

### 2.14 Consentimiento tácito (Ley 793, art. 12, in fine)

[CONFIRMADO] **Regla legal:** el consentimiento tácito o expreso de la resolución administrativa, manifestado por actos posteriores a la notificación, quita el derecho a deducir la acción (Ley 793, art. 12, in fine). Es una causal de extinción autónoma, independiente del vencimiento del plazo de 30 días.

[PENDIENTE] **Configuración concreta:** qué actos constituyen consentimiento tácito en la jurisprudencia de la Corte de Justicia de Salta es una cuestión que este perfil no puede cerrar. Los indicadores que siguen son orientativos; no sustituyen el fallo verificado.

**Indicadores orientativos que pueden configurar consentimiento tácito:**

- Cumplimiento voluntario de la obligación impuesta (pagar la multa, demoler la construcción ordenada).
- Aceptación o percepción de beneficios del acto (cobrar la suma reconocida, usar la habilitación otorgada condicionalmente).
- Presentación de documentación o realización de trámites que presuponen la validez del acto sin cuestionarlo.

**Indicadores orientativos que generalmente no configuran consentimiento tácito:**

- Cumplimiento compulsivo o bajo apercibimiento de ejecución forzada.
- Actos de mero trámite para evitar consecuencias más gravosas mientras se sustancia la impugnación.
- Solicitud de prórroga de plazo para cumplir, documentada como tal.

**Prueba:** aportar el expediente administrativo completo y las constancias de actos posteriores del administrado. No corresponde emitir opinión sobre consentimiento tácito sin ese material.

```
[VERIFICAR CONSENTIMIENTO TÁCITO: Ley 793, art. 12, in fine - aportar expediente administrativo completo y constancias de actos posteriores del administrado antes de opinar]
[INSERTAR FALLO VERIFICADO: Corte de Justicia de Salta - criterios para la configuración del consentimiento tácito - actos que lo constituyen y actos que no lo configuran]
```

### 2.15 Responsabilidad del Estado provincial

[CONFIRMADO] **Sin ley propia:** Salta no sancionó una ley de responsabilidad del Estado equivalente a la Ley 26.944 nacional. La inaplicabilidad de la Ley 26.944 al Estado provincial surge de su propio art. 1, que limita su ámbito al Estado nacional, y de la competencia provincial sobre derecho administrativo local.

[CONFIRMADO] **Inaplicabilidad del CCCN como regla general:** la responsabilidad extracontractual del Estado provincial se rige por el derecho público local, no por el CCCN. No invocar los arts. 1757, 1741 ni otros del CCCN sin verificar previamente si la Corte de Justicia de Salta admite alguna aplicación.

**[CONFIRMADO] Elementos de la responsabilidad (jurisprudencia CJS):** los cuatro elementos exigidos de manera concurrente son:
1. **Daño cierto:** acreditado en su existencia y cuantía.
2. **Imputabilidad material:** la conducta lesiva proviene de un órgano o agente del Estado provincial en ejercicio de sus funciones.
3. **Falta de servicio:** violación objetiva de la obligación de prestar el servicio de manera regular, medida bajo el estándar del art. 1112 del viejo Código Civil, integrado como principio general del derecho administrativo salteño.
4. **Nexo causal adecuado:** directo e inmediato entre la falta de servicio y el perjuicio.

**[CONFIRMADO] Prescripción:** tras el fallo plenario de la CSJN en "Filcrosa", la CJS alineó su doctrina: la prescripción es materia de derecho común delegada al Congreso Nacional. El plazo aplicable es el **art. 2561 CCCN — 3 años** para la indemnización de daños derivados de responsabilidad civil (aplicado por analogía a la responsabilidad del Estado provincial). No rige el plazo del art. 7 Ley 26.944 (que es para el Estado nacional).

**[CONFIRMADO] Lucro cesante en actividad lícita:** a diferencia de la prohibición tajante del art. 5 Ley 26.944 federal, la **CJS lo admite excepcionalmente** (ej. expropiaciones indirectas, revocación de licencias por razones de oportunidad, mérito o conveniencia), siempre que el damnificado demuestre **certeza absoluta** de la ganancia frustrada, no una mera expectativa hipotética. La indemnización debe ser "justa e integral".

[A VERIFICAR] **Competencia:** los Juzgados de Primera Instancia CA entienden en pretensiones resarcitorias contra la Provincia (Ley 6569, art. 2). Verificar si la pretensión resarcitoria debe plantearse conjunta o autónomamente con la pretensión anulatoria.

**[CONFIRMADO] Reclamo administrativo previo (Ley 5018):** la Ley 5018 establece el reclamo administrativo previo obligatorio antes de demandar judicialmente a la Provincia de Salta. Su ámbito operativo comprende la Administración Central, organismos descentralizados y entidades autárquicas provinciales.

Para la pretensión resarcitoria pura (extracontractual) contra el Estado provincial, la jurisprudencia y doctrina locales asimilan la exigencia de la Ley 5018: la Fiscalía de Estado suele oponer la falta de reclamo previo como excepción de inadmisibilidad, salvo que se configure ritualismo inútil o urgencia que habilite vía excepcional. Verificar en cada caso si la pretensión encuadra en el ámbito de la Ley 5018 antes de iniciar la acción judicial.

```
[INSERTAR FALLO VERIFICADO: Corte de Justicia de Salta - requisitos de la responsabilidad extracontractual del Estado provincial]
[INSERTAR FALLO VERIFICADO: Corte de Justicia de Salta - régimen de prescripción de la acción resarcitoria contra el Estado provincial]
[INSERTAR FALLO VERIFICADO: Corte de Justicia de Salta - admisibilidad del lucro cesante en responsabilidad por actividad lícita del Estado provincial]
```

### 2.16 Empleo público Salta

[A VERIFICAR] **Estatuto general:** Ley 5546 (Estatuto del Empleado Público de la Provincia de Salta). El texto disponible más reciente en este perfil es el compilado en el Digesto (Ley 7913, con corte al 31/07/2015). Para verificar el estado normativo actual: Boletín Oficial de Salta.

[A VERIFICAR] **Escalafón:** Decreto Ley 1178/96. Verificar si fue modificado o reemplazado.

[CONFIRMADO] **Régimen disciplinario:** Ley 5546 y Decreto 2734/2007 (Reglamento General de Investigaciones Administrativas de la Provincia de Salta). Sumario administrativo con garantías de debido proceso.

[CONFIRMADO] **Opción del agente (Ley 5546, art. 50):** si el pronunciamiento judicial resulta contrario a la medida segregativa, el Estado debe reincorporar al empleado en cargo de idénticas condiciones o, a opción del agente, pagar la indemnización que establezca la reglamentación. La opción es del agente, no de la Administración.

**Estatutos sectoriales:**
- Docentes: Ley 6830 [A VERIFICAR modificaciones posteriores a 2015].
- **Policía:** Ley N° 7742 (Ley Orgánica de la Policía de Salta, 2012; derogó la Ley 6192; reglamentada por Decreto 3540/12). Para el régimen específico del personal (ingresos, estabilidad, ascensos, régimen disciplinario): Ley N° 6193 (Ley del Personal Policial). [A VERIFICAR modificaciones posteriores a 2015]
- **Personal de salud:** Ley N° 7678 (Estatuto de la Carrera Sanitaria para el Personal de la Salud Pública de Salta; comprende personal del Ministerio de Salud Pública y hospitales de autogestión; reglamentada por Decreto 3896/12). [A VERIFICAR modificaciones posteriores a 2015]
- Personal municipal: [PENDIENTE] verificar el estatuto del municipio concreto.

```
[VERIFICAR ESTATUTO APLICABLE SALTA: Ley 5546 general (verificar estado actual en Boletín Oficial de Salta) o estatuto sectorial según el organismo - docentes: Ley 6830 - régimen disciplinario: Decreto 2734/2007]
```

### 2.17 Contratación pública Salta

**[CONFIRMADO]** Norma general: **Ley 8072** (B.O. 15/01/2018, Sistema de Contrataciones de la Provincia de Salta) y Decreto Reglamentario 1319/18 y modificatorias. Los umbrales para licitación pública, privada y contratación directa se actualizan por decreto o resolución del PE; verificar el texto vigente en el Boletín Oficial de Salta antes de encuadrar el procedimiento.

**[CONFIRMADO]** Honorarios de abogados: **Ley 8035** (B.O. 10/10/2017). Derogó expresamente el Decreto Ley 324/60 y el Decreto 1173/94. Toda liquidación de honorarios en causas ante el fuero salteño corre bajo este régimen.

**[CONFIRMADO] Organismo rector:** Secretaría de Contrataciones, dependiente del Ministerio de Economía y Servicios Públicos de la Provincia de Salta.

**[CONFIRMADO] Plataforma de compras:** Portal de Compras y Contrataciones de la Provincia de Salta — https://compras.salta.gob.ar — centraliza pliegos y adjudicaciones.

**[CONFIRMADO] Obra pública provincial:** **Ley 6838** (régimen específico de contrataciones de obra pública, que sobrevivió a la sanción de la Ley 8072 para este rubro) + **Decreto Reglamentario 1448/1996**. La Ley 13.064 nacional queda totalmente excluida del ámbito provincial salteño.

**[CONFIRMADO] Redeterminación de precios:** régimen propio regulado por el **Decreto 1170/2021** (que reemplazó las fórmulas del Decreto 47/03). Establece redeterminación para contratos de obra pública y servicios cuando los costos de los factores principales muestran variación **superior al 5 %**. El gatillo es automático al superar ese piso. Difiere del esquema federal (Decreto 691/16); no aplicar equivalencia entre ambos regímenes.

```
[VERIFICAR VIGENCIA: Ley 8072 Salta (15/01/2018) + Decreto 1319/18 - montos UC actualizados por resolución - consultar Boletín Oficial de Salta antes de encuadrar el procedimiento]
```

### 2.18 Tabla de responsables procesales por instancia

[CONFIRMADO]

| Instancia | Representante de la Administración | Normativa |
|-----------|-----------------------------------|-----------|
| Juzgados de Primera Instancia CA (1.ª y 2.ª Nominación) | Fiscales de Primera Instancia en lo Civil, Comercial y del Trabajo del Distrito Judicial del Centro | Ley 6569, art. 5 |
| Corte de Justicia de Salta (alzada) | Fiscal de Estado | Ley 6569, art. 5, in fine |
| Administración como actora (impugna actos de otra autoridad) | Fiscal General | Ley 793, art. 7 |
| Notificaciones al Fiscal General | En su despacho | Ley 793, art. 10 |
| Cargo de Fiscal General vacante | Agente Fiscal o abogado que designe el Poder Ejecutivo | Ley 793, art. 10 |

### 2.19 Organismos de control

[CONFIRMADO] **Tribunal de Cuentas de Salta:** control externo del Estado provincial; tiene función jurisdiccional. Sus resoluciones definitivas son impugnables ante el fuero contencioso administrativo.

[A VERIFICAR] **Tribunal de Cuentas de la Municipalidad de Salta:** competencia sobre la hacienda municipal. Verificar si sus resoluciones se revisan ante el fuero CA provincial o ante fuero municipal propio.

[CONFIRMADO] **IPSAS:** ente autárquico de obra social provincial. Sus resoluciones son impugnables ante el fuero contencioso administrativo.

[A VERIFICAR] **Defensor del Pueblo de Salta:** previsto en la Constitución de Salta. Legitimación para actuar en defensa de derechos colectivos. Verificar la ley orgánica vigente.

---

## Bloque 3 - Alertas críticas

### Alerta 1 - Plazo de caducidad para accionar judicialmente

**Este es el primer dato a verificar en toda consulta que involucre una acción judicial contra el Estado provincial o municipal de Salta.**

[CONFIRMADO] **Plazo:** 30 días hábiles judiciales desde la notificación personal, por cédula o por edicto de la resolución administrativa que motiva la demanda (Ley 793, art. 12; cómputo en días hábiles: Ley 793, art. 16).

[CONFIRMADO] **Naturaleza:** caducidad. No se suspende ni interrumpe salvo norma expresa.

[CONFIRMADO] **Declarable de oficio:** sí (Ley 793, art. 27, inc. 1).

[CONFIRMADO] **Consentimiento tácito (Ley 793, art. 12, in fine):** causal autónoma de extinción de la acción, independiente del plazo. Ver sección 2.14.

```
[ALERTA PLAZO FATAL: Ley 793, art. 12, CCA Salta - 30 días hábiles judiciales desde notificación personal/cédula/edicto de la resolución administrativa - verificar también consentimiento tácito posterior (art. 12, in fine) - vencimiento: calcular con guía rápida de la sección 2.8]
```

**Comparación con otros regímenes (solo a título informativo; no transpolar):**

| Régimen | Plazo | Norma |
|---------|-------|-------|
| Salta | **30 días hábiles judiciales** | Ley 793, art. 12 |
| CABA (CCAyT) | 90 días hábiles judiciales | Ley 189 CABA, art. 7 |
| PBA | 90 días hábiles judiciales | Ley 12.008 PBA |
| Córdoba | 30 días | Hábiles judiciales | Ley 7182 art. 8 |
| Mendoza | 30 días | Corridos | Ley 3918 art. 20 |
| Santa Fe | 30 días | A verificar | Ley 11.330 art. 9 |
| Entre Ríos | 1 año | Corridos | Ley 7061 art. 19 |
| Corrientes | 60 días | Hábiles judiciales | Ley 3460 art. 223 |
| Misiones | 60 días | Corridos (sin ferias) | Ley I-95 art. 24 |
| Neuquén | 30 días | Corridos (no feria; inhábil → primer hábil) | Ley 1305 art. 10 |
| Río Negro | 30 días | Hábiles | Ley 5773 art. 11 |
| Federal (actos post-9-jul-2024) | 180 días hábiles judiciales | LNPA, art. 25 (modificado por Ley 27.742) |
| Federal (actos pre-9-jul-2024) | 90 días hábiles judiciales | LNPA, art. 25 (texto anterior) |

### Alerta 2 - Suspensión de la ejecución en sede administrativa

[CONFIRMADO] La interposición de recursos administrativos (revocatoria, jerárquico, alzada) NO suspende la ejecución del acto impugnado (Ley 5348, art. 81). Esta regla es opuesta al régimen federal. Para el mapa completo de cuándo y cómo pedir la suspensión en sede administrativa y en sede judicial, ver la sección 2.9.

### Alerta 3 - Consentimiento tácito

[CONFIRMADO como regla legal; PENDIENTE en cuanto a su configuración concreta] Causal autónoma de extinción de la acción, independiente del plazo de 30 días (Ley 793, art. 12, in fine). Verificar siempre antes de analizar el fondo. Ver sección 2.14 para indicadores y prueba.

### Alerta 4 - Cadena recursiva completa confirmada

[CONFIRMADO] Los plazos del recurso jerárquico (Ley 5348, art. 179: 10 días hábiles administrativos) y del recurso de alzada (Ley 5348, arts. 184-185: 10 días hábiles administrativos) están cerrados. La cadena recursiva puede operarse sin reservas sobre los plazos. Ver sección 2.5 para el detalle completo de cada recurso.

---

## Bloque 4 - Checklists operativos

### Checklist: acto administrativo

1. Identificar: ¿el acto es de un organismo provincial, municipal o federal?
2. ¿El acto fue notificado? ¿En qué fecha y de qué modo (personal / cédula / edicto / electrónica)?
3. ¿El administrado realizó actos posteriores que puedan interpretarse como consentimiento tácito? (ver sección 2.14)
4. ¿El acto es definitivo y no tiene recurso administrativo disponible?
5. ¿Hay expediente administrativo? ¿El abogado lo tiene o requiere vista?
6. ¿Se interpuso la revocatoria en plazo? (10 días hábiles administrativos, Ley 5348, art. 177) [CONFIRMADO]
7. ¿Se interpuso el jerárquico en plazo? (10 días hábiles administrativos desde la denegatoria expresa o el silencio de la revocatoria, Ley 5348, art. 179) [CONFIRMADO]
8. Para entes descentralizados: ¿se interpuso alzada ante el Poder Ejecutivo? (10 días hábiles administrativos, Ley 5348, arts. 184-185) [CONFIRMADO]
9. ¿Aplica la Ley 5018 (reclamo previo)? [A VERIFICAR]
10. ¿Cuál es el plazo remanente del art. 12 de la Ley 793?

### Checklist: acción judicial

1. Verificar agotamiento de la vía (cadena recursiva Ley 5348 y Ley 5018 si aplica).
2. Calcular el plazo de 30 días hábiles judiciales (Ley 793, art. 12) con la guía de la sección 2.8.
3. Verificar consentimiento tácito posterior (Ley 793, art. 12, in fine; sección 2.14).
4. Verificar los requisitos del art. 26 de la Ley 793.
5. Verificar las exclusiones del art. 27 de la Ley 793.
6. En materia tributaria: verificar pago previo (Ley 793, art. 28).
7. Verificar el representante procesal de la Administración según la instancia (tabla de la sección 2.18).
8. Si hay retardación: verificar los tres más tres meses del art. 6 de la Ley 793 con solicitud de pronto despacho documentada.

### Checklist: empleo público

1. Encuadre: Ley 5546 (general) o estatuto sectorial: Ley 6830 (docentes) / Ley 7742 + Ley 6193 (Policía) / Ley 7678 (personal de salud) / estatuto municipal (verificar por municipio).
2. Situación de revista: planta permanente / no permanente / contratado / transitorio.
3. ¿Hubo sumario con garantías de debido proceso? (Decreto 2734/2007: notificación de cargos, vista, descargo, prueba.)
4. ¿La cesantía o exoneración encuadra en alguna causal taxativa del estatuto?
5. ¿Prescripción de la acción disciplinaria? (verificar el plazo en la Ley 5546).
6. En caso de sentencia favorable: la opción entre reincorporación e indemnización es del agente (Ley 5546, art. 50), no de la Administración.
7. La interposición de recursos no suspende la ejecución del acto (Ley 5348, art. 81): evaluar suspensión administrativa o cautelar judicial (sección 2.9).

### Checklist: contratación pública

1. Verificar los montos vigentes de la UC (Ley 8072, Decreto 1319/18 y actualizaciones) — consultar https://www.boletinoficialsalta.gob.ar o el Portal de Compras https://compras.salta.gob.ar.
2. ¿La impugnación fue planteada en el plazo del pliego?
3. ¿El contrato prevé redeterminación de precios? ¿Bajo qué régimen?
4. Para obra pública: verificar la ley provincial, no la Ley 13.064 nacional.
5. ¿Aplica el reclamo previo de la Ley 5018?

---

## Fuentes primarias

- **Boletín Oficial de Salta:** https://boletinoficialsalta.gob.ar - fuente primaria para verificar la vigencia de toda norma posterior a julio de 2015.
- **Poder Judicial de Salta (jurisprudencia, normativa, expediente digital):** https://www.justiciasalta.gov.ar
- **SAIJ:** https://www.saij.gob.ar - texto de normas; confirmar siempre contra el Boletín Oficial de Salta.
- **Portal del Empleado Público Salta:** https://empleopublico.salta.gob.ar
- **Auditoría General de la Provincia de Salta (AGPS):** https://agps.salta.gob.ar (el control externo posterior de la hacienda pública provincial corresponde a la AGPS por Ley N° 7103; Salta no tiene un Tribunal de Cuentas provincial). Para el Tribunal de Cuentas de la Municipalidad de Salta Capital: https://tcm.tribunal.municipalidadsalta.gob.ar
- **IPSS (Instituto Provincial de Salud de Salta):** https://www.ipssalta.gov.ar (obra social provincial de los agentes públicos; las siglas locales son IPSS, no IPSAS)

---

## Reglas de citación - administrativo Salta

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para este fuero:

**Formato de cita legal:** siempre "Ley X, art. Y" con etiqueta de estado ([CONFIRMADO / A VERIFICAR / PENDIENTE]) cuando sea relevante para el análisis.

**Jurisprudencia:** nunca citar expediente o carátula sin material aportado. Usar:
```
[INSERTAR FALLO VERIFICADO: Corte de Justicia de Salta / Juzgado de Primera Instancia CA [1.ª o 2.ª Nominación] - doctrina requerida]
```

**Actos administrativos:** no asumir contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con constancia de notificación]
```

**Plazos:** no transpolar plazos del régimen federal ni de otras provincias. Usar:
```
[ALERTA PLAZO FATAL: Ley 793, art. 12, CCA Salta - 30 días hábiles judiciales - desde notificación de la resolución administrativa - verificar también consentimiento tácito (art. 12, in fine) - vencimiento: calcular con guía sección 2.8]
```

**Consentimiento tácito:** no emitir opinión sin expediente completo. Usar:
```
[VERIFICAR CONSENTIMIENTO TÁCITO: Ley 793, art. 12, in fine - aportar expediente administrativo completo y constancias de actos posteriores del administrado]
```

---

## Matriz de vigencia por norma

> El Digesto Jurídico de Salta (Ley 7913) compiló normas con corte al 31/07/2015. La mención en el Digesto indica que la norma fue incorporada a esa compilación, no que exista un texto ordenado oficial con efecto refundidor. Para toda norma marcada [A VERIFICAR], consultar el Boletín Oficial de Salta.

| Norma | Objeto | Estado al corte de mayo 2026 | Fuente de verificación |
|-------|--------|------------------------------|------------------------|
| Ley 5348 | LPA Salta | [A VERIFICAR] fecha de sanción y modificaciones posteriores a 2015 | Boletín Oficial de Salta |
| Ley 5552/80 | Modificación a la Ley 5348 | [A VERIFICAR] confirmar texto en el Boletín Oficial | Boletín Oficial de Salta |
| Ley 793 | CCA Salta | [A VERIFICAR post-2015] modificada por Leyes 6569, 7822 y 7913; verificar modificaciones ulteriores | Boletín Oficial de Salta / Poder Judicial de Salta |
| Ley 6569 | Juzgados CA | [A VERIFICAR post-2015] modificada por Leyes 7822 y 7913; verificar modificaciones ulteriores | Boletín Oficial de Salta |
| Ley 5018 | Reclamo previo | [A VERIFICAR] texto vigente y ámbito de aplicación | Boletín Oficial de Salta |
| Ley 6224 + Ley 3645 | Amparo (Ley 6224 derogó Ley 5622 y restableció Ley 3645) | [CONFIRMADO] rige junto con art. 87 Const. Salta; sin plazo de caducidad | Boletín Oficial de Salta |
| Ley 5546 | Estatuto del empleado público | [A VERIFICAR post-2015] compilada en el Digesto al 31/07/2015; verificar modificaciones ulteriores | Boletín Oficial de Salta |
| Decreto Ley 1178/96 | Escalafón general | [A VERIFICAR] verificar vigencia y posibles reformas | Boletín Oficial de Salta |
| Decreto 2734/2007 | Investigaciones administrativas | [CONFIRMADO al momento de incorporación al Digesto; A VERIFICAR modificaciones post-2015] | Boletín Oficial de Salta |
| Ley 6830 | Estatuto docente | [A VERIFICAR post-2015] | Boletín Oficial de Salta |
| Ley 8072 | Sistema de Contrataciones del Estado (B.O. 15/01/2018) | [CONFIRMADO vigente] montos UC a verificar por decreto — organismo rector: Secretaría de Contrataciones — plataforma: compras.salta.gob.ar | Boletín Oficial de Salta |
| Ley 6838 + Decreto 1448/96 | Contrataciones de Obra Pública provincial | [CONFIRMADO vigente] Ley 13.064 nacional excluida | Boletín Oficial de Salta |
| Decreto 1170/2021 | Redeterminación de precios (reemplazó Decreto 47/03) | [CONFIRMADO vigente] gatillo 5 % variación de costos | Boletín Oficial de Salta |
| Ley 7742 + Ley 6193 | Policía (orgánica + personal) | [A VERIFICAR modificaciones post-2015] | Boletín Oficial de Salta |
| Ley 7678 | Carrera Sanitaria | [A VERIFICAR modificaciones post-2015] | Boletín Oficial de Salta |
| Ley 7103 | Auditoría General (AGPS) — reemplaza al Tribunal de Cuentas provincial | [CONFIRMADO] | Boletín Oficial de Salta |
| Ley 8520 | Nuevo CPP Salta (reemplaza Ley 7690) | [CONFIRMADO vigente desde 15/12/2025 — A VERIFICAR numeración de artículos] | Boletín Oficial de Salta |
| Ley 5233 (CPCC) | Código Procesal Civil y Comercial | [CONFIRMADO vigente con modificaciones: Ley 8498 ago 2025 art. 303; Ley 8189 art. 711 bis; Ley 8119 art. 692 bis] | Boletín Oficial de Salta |
| Ley 8072 | Sistema de Contrataciones del Estado | [CONFIRMADO vigente desde 15/01/2018 — montos UC a verificar por decreto] | Boletín Oficial de Salta |
| Ley 8035 | Arancel de Honorarios de Abogados | [CONFIRMADO vigente desde 10/10/2017 — derogó D.Ley 324/60 y Decreto 1173/94] | Boletín Oficial de Salta |
| Decreto 1319/18 | Reglamento de la Ley 8072 | [A VERIFICAR] verificar modificaciones; los montos se actualizan por resolución | Boletín Oficial de Salta |
| Constitución de Salta 2003 | Arts. 87 y 153, ap. III | [CONFIRMADO] | Texto oficial |

---

## Estado del escrito - campos estándar

Todo escrito ante el fuero contencioso administrativo de Salta cierra con:

- Fuero y juzgado: 1.ª o 2.ª Nominación / Corte de Justicia de Salta (alzada).
- Organismo demandado: provincial / municipal / ente descentralizado.
- Agotamiento de la vía (Ley 5348 y Ley 5018 si aplica): completo / pendiente / excepción invocada (cuál).
- Plazo, Ley 793, art. 12: verificado (vence: ___) / pendiente / vencido.
- Consentimiento tácito posterior: verificado (no hay) / pendiente / detectado.
- Pago previo (Ley 793, art. 28) si materia tributaria: cumplido / no aplica / pendiente.
- Representante procesal de la Administración identificado: sí (cuál, según tabla de la sección 2.18) / a verificar.
- Normas con [A VERIFICAR] o [PENDIENTE] usadas en el escrito: listado.
- Marcadores pendientes: dato que falta para resolverlos.
- Próximo plazo procesal: ___.

---

## Alerta normativa - normas de vigencia variable

*Última verificación: mayo 2026. El Digesto Jurídico (Ley 7913) tiene corte al 31/07/2015. Para toda norma posterior a esa fecha o modificada después de ella, consultar el Boletín Oficial de Salta (https://boletinoficialsalta.gob.ar).*

- **Montos de contratación pública (Ley 8072 y Decreto 1319/18):** se actualizan por resolución. Consultar el Boletín Oficial de Salta antes de encuadrar el procedimiento.
- **Escala salarial del empleo público de Salta:** se modifica por paritarias. Verificar la resolución de homologación vigente.
- **Habilitaciones municipales:** varían por municipio. Verificar la ordenanza vigente al momento del acto.
- **Calendario judicial:** ferias y feriados se determinan año a año. Obtener el calendario del Poder Judicial de Salta antes de calcular cualquier plazo.

```
[VERIFICAR VIGENCIA: norma Salta - [materia] - consultar Boletín Oficial de Salta (https://boletinoficialsalta.gob.ar) antes de aplicar]
```

---

*Última actualización: mayo 2026 (v1.5)*
*Normativa base: Ley 5348 LPA Salta (modificada por Ley 5552/80), Ley 793 CCA Salta (modificada por Ley 6569, Leyes 7822 y 7913), Ley 5018, art. 87 Constitución de Salta (amparo) + Ley 6224 (que derogó Ley 5622 y restableció Ley 3645), Ley 5546 (estatuto del empleado público, compilada en Digesto Ley 7913 al 31/07/2015), Ley 6830 (estatuto docente), Decreto 2734/2007, Ley 8072 y Decreto 1319/18 (contrataciones), Constitución de Salta (2003) arts. 87 y 153, ap. III.*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
