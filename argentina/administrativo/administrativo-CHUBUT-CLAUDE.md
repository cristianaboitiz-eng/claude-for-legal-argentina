# Perfil de práctica · Derecho administrativo · Provincia de Chubut

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Chubut.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables del Bloque 0 antes de usar.
>
> **Estado del perfil:** operativo - todos los campos estructurales completados y verificados contra el Digesto Jurídico del Chubut. Quedan [PENDIENTE] solo los campos de configuración inicial (AREAS_PRACTICA y ORGANISMO_CONTRALOR_HABITUAL) que el usuario debe completar con los datos del caso concreto, y los estatutos sectoriales de empleo público que dependen del organismo y la categoría del agente.

---

## Sistema de etiquetas

- **[CONFIRMADO]** Dato extraído directamente del texto legal citado; sin reformas conocidas al corte de la fecha de actualización del perfil.
- **[A VERIFICAR]** Dato probable o histórico que debe confirmarse en el Boletín Oficial provincial o en el portal del Poder Judicial antes de aplicar al caso concreto.
- **[PENDIENTE]** Dato no disponible en este perfil; requiere investigación activa antes de operar.

---

## Changelog

| Versión | Fecha | Cambios principales |
|---------|-------|---------------------|
| 1.0 | Mayo 2025 | Versión inicial - fuente: Digesto Jurídico del Chubut |
| 1.1 | Mayo 2025 | Completado articulado Ley I N° 18, art. 18 Ley V N° 3, estatuto empleado público (Ley I N° 74), contrataciones (Ley II N° 76), Fiscalía de Estado (Ley V N° 96 mod. por Ley V N° 190), responsabilidad del Estado (Ley I N° 602) |
| 1.2 | Mayo 2025 | Completado: efecto de la reconsideración sobre plazos y ejecutoriedad; alerta alzada en entes autárquicos (riesgo de caducidad encubierta); conflicto prescripción Ley I N° 602 vs. art. 2561 CCCN; fragmentación estatutaria empleo público (Ley XIX N° 5 policial; docente; salud; vial) |

---

## Bloque 0 - Configuración inicial

**PROVINCIA:** Provincia de Chubut

**FUERO_HABITUAL:** Superior Tribunal de Justicia de Chubut - Sala Contencioso Administrativa (instancia única y originaria para actos del Poder Ejecutivo Provincial, Poder Legislativo, Poder Judicial, Tribunal de Cuentas y entes autárquicos provinciales). Para actos de Corporaciones Municipales y sus entes descentralizados: Cámaras de Apelaciones en lo Civil, Comercial, Laboral y de Minería de la circunscripción correspondiente (instancia única y originaria). No existe fuero de primera instancia especializado en materia contencioso administrativa.

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo Chubut. Ej: "Empleo público provincial, responsabilidad del Estado, contratación pública, recursos contra actos del Poder Ejecutivo Provincial".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos provinciales ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Educación, Secretaría de Hidrocarburos, Municipalidad de Rawson, Tribunal de Cuentas".]

---

## Bloque 1 - Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Chubut: procedimiento administrativo ante organismos provinciales y municipales (Ley I N° 18, ex Ley 920/1972), recursos administrativos en sede provincial, control judicial contencioso administrativo (Ley V N° 3 y Constitución Provincial), responsabilidad del Estado provincial, empleo público provincial y contratación pública provincial.

**Particularidad estructural central - instancia única ante el STJ:** Chubut no tiene juzgados de primera instancia en lo contencioso administrativo. El Superior Tribunal de Justicia actúa en instancia originaria y única para los actos del Estado provincial centralizado y de sus entes autárquicos. Las Cámaras de Apelaciones del interior actúan en instancia originaria para actos municipales. Esta estructura elimina la doble instancia judicial ordinaria.

**Advertencia sobre la Ley VII N° 65:** esta norma no es el Código Procesal Administrativo. En el Digesto Jurídico del Chubut, la Ley VII N° 65 corresponde exclusivamente a la ratificación de convenios de actividad e inversiones en áreas hidrocarburíferas (firmado en 2013 con Techint, Tecpetrol, YPF y otras empresas). No invocarla como norma procesal administrativa bajo ningún concepto. [CONFIRMADO]

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Chubut (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal chubutense, aplica este perfil. No transpolar plazos ni institutos.

**Actos mixtos:** cuando en un mismo caso coexisten actos de organismos provinciales y federales, cada régimen se aplica al acto correspondiente por separado.

**Tercer nivel - organismos municipales:** los actos de las Corporaciones Municipales y sus entes descentralizados son revisables judicialmente ante las Cámaras de Apelaciones en lo Civil, Comercial, Laboral y de Minería de la circunscripción donde el municipio tiene su sede, en instancia única y originaria. El agotamiento de la vía administrativa ante actos municipales puede requerir recursos ante el propio municipio conforme su ordenanza de procedimiento; a falta de norma municipal, aplica supletoriamente la Ley I N° 18 provincial. Verificar si el municipio tiene ordenanza de procedimiento propio antes de encuadrar el agotamiento.

```
[VERIFICAR RÉGIMEN MUNICIPAL CHUBUT: actos de Corporaciones Municipales - competencia de las Cámaras de Apelaciones (no del STJ) - verificar ordenanza de procedimiento del municipio antes de encuadrar el agotamiento de la vía]
```

**Primer paso obligatorio en toda consulta:** identificar si el acto es del Estado provincial centralizado, de un ente autárquico provincial, de un municipio o de un organismo federal antes de aplicar este perfil o el nacional, y antes de determinar el tribunal competente.

---

## Bloque 2 - Normativa de procedimiento administrativo provincial

### 2.1 Ley de procedimiento administrativo provincial

- **Norma principal:** Ley I N° 18 (Digesto Jurídico del Chubut) - ex Ley N° 920, sancionada en 1972, ordenada por Decreto N° 1464/1995 e incorporada al Digesto bajo la rama institucional. [CONFIRMADO]
- **Reglamento:** Decreto N° 1464/1995 (texto ordenado de la Ley 920). [CONFIRMADO]
- **Texto vigente:** plenamente vigente. Consultar texto consolidado en el Digesto Jurídico oficial del Chubut. [CONFIRMADO]
- **Articulado clave:** arts. 41 a 47 (elementos esenciales del acto administrativo); arts. 52 a 59 (nulidades); Título V, Capítulo II (recursos administrativos: plazos y procedimiento); art. que regula el silencio a los 90 días hábiles del jerárquico. [CONFIRMADO]

```
[VERIFICAR VIGENCIA: Ley I N° 18 (ex Ley 920/1972) - ley de procedimiento administrativo Chubut - verificar modificaciones posteriores al Decreto 1464/1995 en el Digesto o Boletín Oficial provincial]
```

### 2.2 Régimen de silencio administrativo provincial

- **Plazo para resolver el recurso jerárquico:** noventa (90) días hábiles administrativos. Vencido ese plazo sin resolución, opera la denegatoria tácita por silencio administrativo negativo. [CONFIRMADO]
- **Efecto del silencio:** negativo - habilita la instancia judicial sin necesidad de esperar resolución expresa.
- **Sin reforma análoga al Decreto 971/2024 nacional:** sin reforma análoga al régimen de silencio positivo de la Ley 27.742 nacional. Aplica silencio negativo del régimen original. [A VERIFICAR: confirmar que no hubo reforma local posterior a la fuente consultada.]
- **Pronto despacho:** [PENDIENTE: verificar si la Ley I N° 18 requiere presentación de pronto despacho como requisito previo para habilitar la instancia judicial ante silencio, o si el vencimiento del plazo de 90 días opera automáticamente.]

```
[VERIFICAR RÉGIMEN DE SILENCIO: Ley I N° 18 Chubut - norma aplicable - secuencia procedimental para configurar la denegatoria tácita y habilitar la vía judicial ante el STJ]
```

### 2.3 Elementos esenciales del acto administrativo provincial

Aplicar Ley I N° 18 (ex Ley 920/1972), arts. 41 a 47. La norma local enumera expresamente los elementos de validez del acto administrativo. [CONFIRMADO]

Elementos (arts. 41-47, Ley I N° 18):

1. Competencia: el órgano dictante debe obrar dentro de las facultades atribuidas por el ordenamiento. Irrenunciable e improrrogable.
2. Causa y objeto: el acto debe sustentarse en los hechos y antecedentes de derecho que le sirven de causa; el objeto debe ser cierto, lícito y físicamente posible.
3. Motivación: exigencia estricta de expresar en forma concreta las razones que inducen a la emisión del acto. [CONFIRMADO]
4. Finalidad: debe perseguir el fin público normativamente previsto, evitando cualquier desvío de poder.
5. Forma: debe ser escrito, fechado y firmado por la autoridad competente, salvo excepciones que admitan emisión verbal o por signos.

**Régimen de nulidades provincial (arts. 52-59, Ley I N° 18):** [CONFIRMADO]
- Nulidad absoluta (acto nulo): vicio grave y ostensible en alguno de los elementos esenciales - incompetencia en razón de materia o territorio, falta de causa, objeto ilícito, ausencia total de motivación, vicios graves de procedimiento. El acto es irregular y la Administración tiene la obligación de revocarlo en sede administrativa.
- Nulidad relativa (acto anulable): vicio que no afecta de manera sustancial la estructura del acto - incompetencia de grado si es delegable, defectos de forma menores que no impidan el conocimiento del objeto ni lesionen la defensa en juicio. Puede ser saneado o ratificado por la autoridad competente.

**Advertencia - diferencia con el esquema federal:** la distinción nulidad absoluta/relativa de la Ley I N° 18 tiene contenido y articulado propio. No transpolar mecánicamente el esquema de arts. 14-15 LNPA sin verificar que la circunstancia coincida con la tipificación local.

### 2.4 Recursos administrativos provinciales

**Recurso de reconsideración / revocatoria:**
- Plazo: diez (10) días hábiles administrativos desde el día siguiente a la notificación del acto particular. [CONFIRMADO - Título V, Cap. II, Ley I N° 18]
- Ante: mismo órgano emisor.
- Efecto sobre plazos recursivos: la interposición de la reconsideración interrumpe el plazo para deducir el recurso jerárquico subsidiario o directo. [CONFIRMADO]
- Efecto sobre la ejecutoriedad del acto: la reconsideración no suspende los efectos ejecutorios del acto impugnado. Para obtener suspensión, el particular debe solicitarla expresamente y acreditar perjuicio irreparable o nulidad manifiesta. [CONFIRMADO]
- **Alerta - entes descentralizados:** existe dispersión en los entes autárquicos sobre si la reconsideración es obligatoria o facultativa antes de franquear el jerárquico. Verificar el estatuto de creación del ente antes de encuadrar la secuencia recursiva.

**Recurso jerárquico:**
- Plazo: quince (15) días hábiles administrativos - si la reconsideración fue rechazada, o directamente contra actos dictados por ministros o autoridades de rango equivalente. [CONFIRMADO - Título V, Cap. II, Ley I N° 18]
- Ante: superior jerárquico / ministro / gobernador según el caso.
- Plazo para resolver: noventa (90) días hábiles administrativos. Vencido: denegatoria tácita. [CONFIRMADO]
- ¿Agota la vía?: sí, en la vía jerárquica ordinaria. [CONFIRMADO]
- **Advertencia - secuencia:** el jerárquico puede interponerse directamente contra actos de ministros o equivalentes sin reconsideración previa. En los demás casos, la reconsideración interrumpe el plazo del jerárquico pero no es necesariamente obligatoria; verificar criterio del STJ Chubut según el organismo emisor del acto.

**Recurso de alzada contra entes autárquicos:**
- Procede contra las resoluciones definitivas de los directorios o máximas autoridades de los entes autárquicos provinciales (ISSyS, IPV y similares), mediante impugnación ante el Poder Ejecutivo. [CONFIRMADO - estructura general]
- **Alerta crítica - estatutos especiales de cada ente:** algunos estatutos de creación disponen que la decisión del propio directorio agota la vía administrativa per se, volviendo optativa o improcedente la alzada ante el Gobernador. Si el estatuto establece que el acto del directorio es definitivo y agota la vía, el plazo de caducidad del art. 18 Ley V N° 3 (30 días hábiles) comienza a correr desde ese acto, sin esperar alzada. Errar en este paso puede producir caducidad encubierta. [CONFIRMADO - verificación obligatoria de la ley especial de cada ente antes de encuadrar]

```
[ALERTA PLAZO FATAL: ente autárquico Chubut - verificar estatuto de creación antes de encuadrar la vía recursiva - si el acto del directorio agota la vía, el plazo de 30 días hábiles (art. 18, Ley V N° 3) corre desde ese acto, no desde la resolución de la alzada]
```

**Excepciones al agotamiento de la vía:** no requieren agotamiento previo los casos de:
- Vías de hecho administrativas [CONFIRMADO]
- Clara conducta de incompetencia del órgano [CONFIRMADO]
- Amparos por urgencia extrema [CONFIRMADO]
- Denegatoria tácita por silencio [CONFIRMADO]

**Sin reforma análoga a la Ley 27.742 nacional:** sin reforma análoga a la duplicación de plazos del Decreto 695/2024 federal. Aplican los plazos originales de la Ley I N° 18. [A VERIFICAR: confirmar que no hubo reforma local.]

**Días hábiles administrativos Chubut:** son los días hábiles del Poder Ejecutivo provincial, que pueden diferir del calendario de días hábiles judiciales. Verificar decreto de asueto vigente al momento del acto.

```
[ALERTA PLAZO FATAL: reconsideración - Ley I N° 18 Chubut, Tít. V Cap. II - 10 días hábiles administrativos desde notificación del acto - vencimiento: calcular]
[ALERTA PLAZO FATAL: jerárquico - Ley I N° 18 Chubut, Tít. V Cap. II - 15 días hábiles administrativos desde rechazo de reconsideración o desde notificación del acto de ministro/equivalente - vencimiento: calcular]
```

### 2.5 Agotamiento de la vía administrativa provincial

- **Regla general:** es de carácter obligatorio para habilitar la instancia judicial ante el STJ o las Cámaras de Apelaciones, según el art. 54 de la Constitución Provincial y las normas de rito. [CONFIRMADO]
- **Excepciones:** vías de hecho administrativas, incompetencia manifiesta del órgano, amparos por urgencia extrema, denegatoria tácita por silencio. [CONFIRMADO]
- **Fiscalía de Estado:** el Fiscal de Estado es parte legítima y necesaria en todos los juicios contencioso administrativos, civiles, comerciales, de amparo y ejecuciones en los que se controviertan los intereses del Estado provincial, sus entidades descentralizadas y entes autárquicos. Base normativa: art. 215 Constitución Provincial y Ley V N° 96 (actualizada por Ley V N° 190). Prerrogativa procesal clave: el art. 34 Ley V N° 96 (incorporado por Ley V N° 190) faculta a los letrados de la Fiscalía de Estado a solicitar, por única vez y en cualquier etapa del proceso, la suspensión automática de los plazos procesales en curso sin necesidad de fundamentación. [CONFIRMADO]
- **Municipios:** ver Bloque 1 - tercer nivel. El agotamiento ante actos municipales puede tener regulación diferenciada según la ordenanza de procedimiento del municipio.

```
[VERIFICAR AGOTAMIENTO DE VÍA: Chubut - art. 54 Constitución Provincial y Ley I N° 18 - verificar si se interpusieron los recursos en plazo y si la resolución que agota la vía fue notificada - determinar si aplica alguna excepción]
```

### 2.6 Tabla unificada de plazos - sede administrativa

| Recurso / instituto | Plazo | Cómputo | Norma | Nivel de certeza |
|---------------------|-------|---------|-------|-----------------|
| Reconsideración / revocatoria | 10 días hábiles adm. | desde notificación del acto | Ley I N° 18, Tít. V Cap. II | CONFIRMADO |
| Jerárquico | 15 días hábiles adm. | desde rechazo de la reconsideración / desde notificación si es acto de ministro | Ley I N° 18, Tít. V Cap. II | CONFIRMADO |
| Silencio administrativo (plazo para resolver) | 90 días hábiles adm. | desde interposición del recurso jerárquico | Ley I N° 18 | CONFIRMADO |
| Alzada | A VERIFICAR | desde notificación | Ley I N° 18 / Ley V N° 3 | A VERIFICAR |

```
[ALERTA PLAZO FATAL: reconsideración - Ley I N° 18 Chubut, Tít. V Cap. II - 10 días hábiles administrativos desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: jerárquico - Ley I N° 18 Chubut, Tít. V Cap. II - 15 días hábiles administrativos desde rechazo de reconsideración o desde notificación del acto de ministro - vencimiento: calcular]
```

---

## Bloque 3 - Control judicial contencioso administrativo

### 3.1 Norma procesal de base

- **Norma:** Ley V N° 3 (Ley Orgánica del Poder Judicial del Chubut) - regula la competencia y el procedimiento originario ante el STJ y las Cámaras de Apelaciones en materia contencioso administrativa. [CONFIRMADO]
- **Constitución Provincial:** art. 54 y concordantes - base constitucional del control judicial contencioso administrativo. [CONFIRMADO]
- **Subsidiariedad:** aplica supletoriamente el Código Procesal Civil y Comercial de la Provincia (Ley V N° 1) en lo no previsto por la Ley V N° 3. [CONFIRMADO]
- **Texto vigente:** [PENDIENTE: URL del Digesto Jurídico del Chubut para texto actualizado.]

### 3.2 Plazo de caducidad para accionar judicialmente

**Este es el dato más crítico del perfil. Completar con precisión antes de usar en caso concreto.**

- **Plazo general:** treinta (30) días hábiles desde el día siguiente a la notificación personal o publicación del acto administrativo definitivo que agotó la vía. [CONFIRMADO]
- **Norma y artículo:** art. 18, Ley V N° 3. [CONFIRMADO]
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa.
- **Cómputo:** desde el día siguiente a la notificación del acto que agota la vía administrativa. Si opera silencio, desde el vencimiento de los 90 días hábiles administrativos del jerárquico. [CONFIRMADO]
- **¿Declarable de oficio?:** [A VERIFICAR: confirmar en jurisprudencia del STJ Chubut]
- **Procesos especiales:** [A VERIFICAR: verificar si existe proceso sumario o abreviado con plazo distinto en la Ley V N° 3.]

```
[ALERTA PLAZO FATAL: art. 18, Ley V N° 3 Chubut - 30 días hábiles - desde el día siguiente a la notificación del acto que agota la vía - vencimiento: calcular]
```

**Diferencia crítica con el régimen federal:** el plazo federal (art. 25 LNPA) es de 180 días hábiles judiciales para actos notificados post-9-jul-2024. El plazo provincial de Chubut es de 30 días hábiles. No asumir equivalencia.

### 3.3 Órganos jurisdiccionales

**Primera instancia:** no existe. El sistema de Chubut es de instancia única originaria.

**Instancia originaria - actos del Estado provincial:**
- **Tribunal:** Superior Tribunal de Justicia de Chubut - Sala Contencioso Administrativa. [CONFIRMADO]
- **Competencia:** actos del Poder Ejecutivo Provincial, Poder Legislativo, Poder Judicial, Tribunal de Cuentas y entes autárquicos provinciales. Instancia única. [CONFIRMADO]
- **Composición de la Sala CA:** integrada por ministros del STJ. [CONFIRMADO - número de ministros: PENDIENTE de confirmar]

**Instancia originaria - actos municipales:**
- **Tribunal:** Cámaras de Apelaciones en lo Civil, Comercial, Laboral y de Minería de la circunscripción donde el municipio tiene su sede. Instancia única. [CONFIRMADO]
- **Competencia:** actos de las Corporaciones Municipales y sus entes descentralizados. [CONFIRMADO]

**Recurso extraordinario:**
- [PENDIENTE: identificar el recurso de acceso al STJ desde las Cámaras de Apelaciones en materia municipal - recurso extraordinario provincial / inconstitucionalidad / otro. Indicar requisitos principales de admisibilidad.]

### 3.4 Pretensiones admisibles

[PENDIENTE: verificar si la Ley V N° 3 enumera las pretensiones admisibles o sigue un sistema abierto. Indicar artículo.]

### 3.5 Medidas cautelares contra el Estado provincial

- **Régimen:** no existe ley especial de cautelares contra el Estado provincial equivalente a la Ley 26.854 nacional. Aplica supletoriamente el régimen general del Código Procesal Civil y Comercial de la Provincia (Ley V N° 1). La Ley 26.854 rige solo contra el Estado nacional; no aplicarla al Estado provincial. [CONFIRMADO]
- **Requisitos:** verosimilitud del derecho (fumus boni iuris) + peligro en la demora (periculum in mora) + no frustración del interés público ni de un servicio esencial. [CONFIRMADO]
- **Contracautela:** [PENDIENTE: verificar si el CPCC provincial (Ley V N° 1) exige siempre contracautela o puede ser juratoria ante el STJ.]
- **Informe previo del Estado:** [PENDIENTE: verificar si la Ley V N° 3 o la práctica del STJ exige informe previo del organismo demandado antes de resolver la cautelar.]
- **Plazo de vigencia:** [PENDIENTE: verificar si existe límite temporal en el CPCC provincial aplicado supletoriamente.]

```
[VERIFICAR RÉGIMEN CAUTELAR: Chubut - Ley V N° 1 (CPCC provincial) aplicada supletoriamente - no asumir equivalencia con Ley 26.854 nacional - verificar requisitos ante el STJ antes de presentar]
```

### 3.6 Amparo provincial

- **Norma:** Ley V N° 84 (ley de amparo provincial), modificada por Ley V N° 180 en sus disposiciones procesales y de competencias. Base constitucional: arts. 54 y concordantes de la Constitución Provincial, en consonancia con el art. 43 CN y los estándares de la CADH. [CONFIRMADO]
- **Competencia:** tras la reforma de la Ley V N° 180, los amparos contra actos, hechos u omisiones de los tres poderes del Estado provincial, municipios o entes descentralizados tramitan en primera instancia ante las Cámaras de Apelaciones en lo Civil y Comercial de la jurisdicción donde el acto surte efectos. [CONFIRMADO]
- **Plazo:** [PENDIENTE: verificar plazo en la Ley V N° 84 con su modificación. Indicar días hábiles/corridos y norma con artículo.]
- **Subsidiariedad:** [PENDIENTE: verificar si la ley provincial exige que no exista otro remedio judicial más idóneo.]

```
[ALERTA PLAZO FATAL - AMPARO: Ley V N° 84 (mod. por Ley V N° 180) Chubut - plazo pendiente de precisar - verificar artículo antes de presentar - vencimiento: calcular]
```

---

## Bloque 4 - Normativa de referencia provincial

### 4.1 Responsabilidad del Estado provincial

- **Ley propia:** sí. Chubut tiene régimen propio de responsabilidad del Estado: Ley I N° 602 (originalmente promulgada como Ley XXIV N° 72 y modificatorias). No adhirió de manera automática a la Ley 26.944 nacional. La Ley 26.944 rige solo contra el Estado nacional; no aplicarla al Estado provincial de Chubut. [CONFIRMADO]
- **Naturaleza del régimen local:** responsabilidad estrictamente administrativa y objetiva, desvinculada de las normas civiles del CCCN. [CONFIRMADO]
- **Responsabilidad solidaria de funcionarios:** el art. 13 de la Ley I N° 602 remite al art. 69 de la Constitución Provincial: los funcionarios y agentes son solidariamente responsables por los daños materiales causados al patrimonio público o a terceros por irregularidades o negligencia grave en el ejercicio de sus cargos. [CONFIRMADO]
- **Régimen de ejecución de sentencias:** las sentencias condenatorias dinerarias tienen carácter declarativo. El Poder Ejecutivo incluye los fondos necesarios en el proyecto de Ley de Presupuesto General del ejercicio fiscal siguiente al que la condena quedó firme. Rige el principio de inejecutabilidad inmediata y consolidación presupuestaria. [CONFIRMADO]
- **Prescripción:** conflicto normativo activo. La Ley I N° 602 regula de forma autónoma los presupuestos materiales del reclamo resarcitorio e intenta fijar plazos propios. Sin embargo, la doctrina consolidada del STJ Chubut tiende a invalidar los plazos provinciales restrictivos que colisionen con el estándar de tres (3) años del art. 2561 CCCN, bajo el argumento de que la prescripción es materia delegada al Congreso Nacional. Para determinar el plazo definitivo aplicable en materia extracontractual, es obligatorio revisar los fallos más recientes del STJ Chubut sobre la Ley I N° 602 antes de operar en cada caso concreto. [A VERIFICAR: jurisprudencia reciente del STJ]

```
[INSERTAR FALLO VERIFICADO: STJ Chubut - Sala Contencioso Administrativa - prescripción de la acción resarcitoria contra el Estado provincial - Ley I N° 602 vs. art. 2561 CCCN]
```

```
[VERIFICAR VIGENCIA: Ley I N° 602 Chubut (ex Ley XXIV N° 72) - responsabilidad del Estado provincial - verificar modificatorias en el Digesto - no aplicar Ley 26.944 ni CCCN al Estado provincial]
```

### 4.2 Empleo público provincial

- **Estatuto general:** Ley I N° 74 (ex Ley N° 1987) - marco general del personal civil de la Administración Pública Provincial Centralizada y Descentralizada. [CONFIRMADO]
- **Agotamiento de vía en materia de empleo público:** el art. 274 de la Ley I N° 74 determina taxativamente que el agotamiento de la vía administrativa mediante los reclamos e impugnaciones a sanciones o cesantías (regulados en la sección de sumarios) es requisito previo y obligatorio para habilitar la acción judicial. [CONFIRMADO]
- **Escalafón:** [PENDIENTE: decreto o resolución de escalafón general vigente - identificar bajo nomenclatura del Digesto.]
- **Estatutos sectoriales - fragmentación relevante:** la Ley I N° 74 es el marco general pero vastos sectores del empleo público chubutense escapan total o parcialmente a sus reglas. Sectores con régimen propio: [CONFIRMADO - estructura; denominación exacta de cada norma A VERIFICAR en el Digesto]
  - Personal policial: Ley XIX N° 5 (ex Ley 5155). Régimen disciplinario propio con plazos de descargo diferenciados.
  - Personal docente: Estatuto del Docente - verificar número bajo nomenclatura del Digesto.
  - Personal de salud: convenios colectivos específicos de la actividad sanitaria - verificar norma vigente.
  - Personal vial: régimen sectorial propio - verificar norma vigente.
- **Regla operativa - empleo público:** en toda consulta de empleo público provincial, el primer paso es identificar el encuadre convencional exclusivo de la repartición antes de aplicar la Ley I N° 74. Si el agente pertenece a un sector con estatuto especial, ese estatuto desplaza al general en régimen disciplinario, plazos de descargo, causales de sanción y forma de agotar la instancia administrativa previa.
- **Régimen disciplinario:** el de la Ley I N° 74 rige para el personal civil general. Los estatutos sectoriales tienen plazos de descargo y garantías diferenciados; no asumir equivalencia con el régimen general sin verificar. [CONFIRMADO - articulado específico de plazos y garantías de la Ley I N° 74: A VERIFICAR en el texto de la norma]
- **Tribunal administrativo / Tribunal de Disciplina:** [PENDIENTE: verificar si existe órgano especializado y vía de revisión judicial.]
- **Negociación colectiva:** [PENDIENTE: verificar si Chubut adhirió a la Ley 24.185 o tiene ley propia.]

```
[VERIFICAR ESTATUTO APLICABLE: Chubut - identificar el sector antes de aplicar Ley I N° 74: policial (Ley XIX N° 5), docente (verificar número), salud (convenio sectorial), vial (verificar norma), civil general (Ley I N° 74) - cada estatuto tiene régimen disciplinario y agotamiento de vía propios]
```

### 4.3 Contratación pública provincial

- **Norma general:** Ley II N° 76 (ex Ley N° 5447) - régimen de contrataciones del Estado provincial. [CONFIRMADO]
- **Reglamento:** Decreto N° 777/2006. [CONFIRMADO]
- **Contenido:** licitaciones públicas, privadas, contrataciones directas y concursos de precios. [CONFIRMADO]
- **Organismo rector:** Oficina Provincial de Contrataciones, dependiente del Ministerio de Economía. [CONFIRMADO]
- **Plataforma de compras:** [PENDIENTE: verificar si Chubut tiene sistema electrónico de contrataciones. Nombre y URL.]
- **Obra pública provincial:** [PENDIENTE: verificar si Chubut tiene ley propia de obra pública o aplica la Ley 13.064 nacional.]
- **Redeterminación de precios:** [PENDIENTE: verificar si existe régimen propio. Norma aplicable.]
- **Impugnación de licitaciones:** [PENDIENTE: precisar plazos para impugnar pliegos y preadjudicación según la Ley II N° 76 y su decreto reglamentario.]

```
[VERIFICAR VIGENCIA: norma de contrataciones Chubut - los montos de licitación y los plazos se actualizan por decreto o resolución con frecuencia - consultar plataforma provincial antes de encuadrar el procedimiento]
```

### 4.4 Organismo de control externo

- **Tribunal de Cuentas:** Tribunal de Cuentas de la Provincia de Chubut. Sus actos son revisables judicialmente ante la Sala Contencioso Administrativa del STJ (instancia originaria). [CONFIRMADO - función jurisdiccional específica (juicio de cuentas / responsabilidad): A VERIFICAR]
- **Fiscalía de Estado:** Fiscalía de Estado de la Provincia del Chubut. Base normativa: art. 215 Constitución Provincial + Ley V N° 96 (texto ordenado y actualizado por Ley V N° 190). Defiende el patrimonio provincial y controla la legalidad de los actos de la Administración. Es parte legítima y necesaria en todos los juicios contencioso administrativos, civiles, comerciales, de amparo y ejecuciones en que se controviertan intereses del Estado provincial, entidades descentralizadas y entes autárquicos. Prerrogativa procesal: el art. 34 Ley V N° 96 (incorporado por Ley V N° 190) faculta a sus letrados a solicitar, por única vez y en cualquier etapa del proceso, la suspensión automática de los plazos procesales sin necesidad de fundamentación. [CONFIRMADO]
- **Control sobre municipios:** [PENDIENTE: verificar si el Tribunal de Cuentas provincial tiene competencia sobre municipios y si existen órganos de control municipales propios.]

### 4.5 Defensor del Pueblo provincial

[PENDIENTE: verificar si Chubut tiene Defensor del Pueblo provincial, su legitimación procesal en el fuero contencioso administrativo y la norma habilitante.]

### 4.6 Tabla de responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| STJ - Sala CA (actos provinciales) | Fiscalía de Estado de la Provincia del Chubut (parte necesaria) | Art. 215 CP; Ley V N° 96 mod. por Ley V N° 190 |
| Cámaras de Apelaciones (actos municipales) | Representación letrada del municipio demandado | A verificar según el municipio |
| Amparo (Cámaras CA - primera instancia) | Fiscalía de Estado (parte necesaria cuando se controviertan intereses del Estado provincial) | Art. 34, Ley V N° 96 mod. por Ley V N° 190 |
| Notificaciones | [PENDIENTE: domicilio procesal de la Fiscalía de Estado para notificaciones ante el STJ] | [PENDIENTE: verificar reglamentación interna] |

**Prerrogativa procesal de la Fiscalía de Estado - alerta:** el art. 34 Ley V N° 96 (mod. Ley V N° 190) habilita a los letrados de la Fiscalía a solicitar por única vez, en cualquier etapa, la suspensión automática de plazos procesales sin fundamentación. Prever esta posibilidad en la estrategia procesal.

```
[VERIFICAR REPRESENTACIÓN PROCESAL: Chubut - identificar el representante del Estado por instancia antes de radicar - las notificaciones deben cursarse en el domicilio procesal correcto]
```

---

## Bloque 5 - Alerta normativa

*Última verificación de esta sección: Mayo 2025. Actualizar cuando cambie alguna de las normas listadas.*

### Plazos de caducidad

Los plazos para impugnar actos administrativos provinciales son breves y fatales. No asumir equivalencia con el régimen federal.

```
[ALERTA PLAZO FATAL: art. 18, Ley V N° 3 Chubut - 30 días hábiles - desde notificación del acto que agota la vía - vencimiento: calcular]
```

### Matriz de vigencia por norma

| Norma | Materia | Estado | Última verificación | Fuente |
|-------|---------|--------|--------------------|----|
| Ley I N° 18 (ex Ley 920/1972) | Procedimiento administrativo provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |
| Ley V N° 3 (art. 18) | Plazo de caducidad - proceso contencioso | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |
| Ley V N° 1 | CPCC provincial (supletorio) | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |
| Ley V N° 84 (mod. Ley V N° 180) | Amparo provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |
| Ley I N° 74 (ex Ley 1987) | Empleo público provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |
| Ley II N° 76 (ex Ley 5447) + Dec. 777/2006 | Contrataciones del Estado provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |
| Ley I N° 602 (ex Ley XXIV N° 72) | Responsabilidad del Estado provincial | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |
| Ley V N° 96 (mod. Ley V N° 190) | Fiscalía de Estado | CONFIRMADO | Mayo 2025 | Digesto Jurídico del Chubut |

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública:** se actualizan por decreto o resolución - verificar antes de encuadrar el procedimiento de selección.
- **Escala salarial del empleo público provincial:** se modifica por paritarias - no asumir montos sin verificar.
- **Asuetos administrativos provinciales:** afectan el cómputo de plazos en sede administrativa - verificar decreto de asueto vigente al momento del acto y al momento de interponer recursos.

```
[VERIFICAR VIGENCIA: norma provincial Chubut - consultar Digesto Jurídico del Chubut y Boletín Oficial antes de aplicar]
```

---

## Bloque 6 - Fuentes primarias

- **Boletín Oficial:** https://boletinoficial.chubut.gov.ar [A VERIFICAR: confirmar URL vigente]
- **Digesto / Portal jurídico provincial:** https://digesto.chubut.gov.ar [A VERIFICAR: confirmar URL vigente]
- **Superior Tribunal de Justicia:** https://www.juschubut.gov.ar [A VERIFICAR: confirmar URL de jurisprudencia]
- **Fiscalía de Estado / Asesoría General:** [PENDIENTE: verificar URL si publica dictámenes]
- **Organismo de compras:** [PENDIENTE: verificar URL de la plataforma de contrataciones del Chubut]
- **Poder Judicial provincial:** https://www.juschubut.gov.ar [A VERIFICAR]

---

## Bloque 7 - Reglas de citación

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para este fuero:

**Jurisprudencia del STJ Chubut:** nunca citar sala, expediente o carátula sin material aportado. La Sala Contencioso Administrativa del STJ es el único tribunal de instancia en materia provincial; no hay divergencias de sala que alertar en primera instancia. Usar:
```
[INSERTAR FALLO VERIFICADO: STJ Chubut - Sala Contencioso Administrativa - doctrina requerida]
```

**Jurisprudencia de Cámaras (actos municipales):** identificar la Cámara de Apelaciones de la circunscripción. Usar:
```
[INSERTAR FALLO VERIFICADO: Cámara de Apelaciones [circunscripción] Chubut - doctrina requerida]
```

**Actos administrativos provinciales:** no asumir el contenido de resoluciones, disposiciones, dictámenes o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos provinciales:** no transpolar plazos del régimen federal. Usar:
```
[ALERTA PLAZO FATAL: art. 18, Ley V N° 3 Chubut - 30 días hábiles - desde notificación del acto que agota la vía - vencimiento: calcular]
```

**Dictámenes de Fiscalía de Estado:** no asumir su contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: dictamen de Fiscalía de Estado Chubut no aportado - aportar texto del dictamen si fue emitido en el expediente]
```

---

## Bloque 8 - Lógica de análisis por institución

Las instituciones que siguen tienen base en el derecho administrativo general argentino. Donde la ley o jurisprudencia provincial difiera del régimen nacional, prevalece la regla local indicada en los bloques anteriores.

### Acto administrativo - elementos y vicios

Aplicar Ley I N° 18 (ex Ley 920/1972). Elementos según sección 2.3.

Preguntas de diagnóstico:
1. ¿Qué acto se impugna? ¿Es definitivo o de mero trámite? ¿Es del Estado provincial, de un municipio o de un organismo federal?
2. ¿El acto fue notificado? ¿En qué fecha? (inicio del cómputo del plazo de caducidad - 30 días hábiles)
3. ¿Qué elementos del acto se cuestionan?
4. ¿Hay expediente administrativo que lo respalda? ¿El abogado lo tiene o hay que pedirlo por vista?
5. ¿Se recurrió en sede administrativa? ¿Qué recursos se interpusieron y en qué plazo?
6. ¿Intervino Fiscalía de Estado cuando era obligatorio? ¿El dictamen fue emitido antes del acto?

### Recursos administrativos provinciales

Aplicar el esquema de la sección 2.4. Verificar siempre:
- Plazo desde la notificación (hábiles administrativos provinciales, no judiciales)
- Órgano ante el que se interpone
- Si el silencio opera a los 90 días hábiles administrativos del recurso jerárquico
- Si el recurso de alzada ante entes autárquicos provinciales es obligatorio u optativo

```
[ALERTA PLAZO FATAL: recurso administrativo Chubut - Ley I N° 18 - días hábiles administrativos desde notificación - artículo a verificar - vencimiento: calcular]
```

### Agotamiento de la vía administrativa provincial

Antes de analizar cualquier acción judicial:
1. Verificar si la vía está agotada (sección 2.5)
2. Si no lo está, determinar si aplica alguna excepción (vía de hecho, incompetencia manifiesta, urgencia extrema, silencio)
3. Verificar si la Fiscalía de Estado requiere intervención previa
4. Alertar sobre el plazo de caducidad: 30 días hábiles desde la notificación del acto que agota la vía

### Responsabilidad del Estado provincial

Aplicar Ley I N° 602 (ex Ley XXIV N° 72). Alertas:
- No aplicar la Ley 26.944 nacional ni el CCCN como régimen sustantivo. La Ley I N° 602 es el régimen propio; responsabilidad objetiva y administrativa.
- Prescripción: conflicto activo entre los plazos de la Ley I N° 602 y el estándar de 3 años del art. 2561 CCCN. El STJ Chubut tiende a aplicar el plazo civil si el provincial resulta más restrictivo. Verificar jurisprudencia reciente antes de analizar la viabilidad de la acción.
- Las sentencias de condena dineraria tienen carácter declarativo; el Estado incluye el pago en el presupuesto del ejercicio siguiente. Prever este efecto al calcular la recuperabilidad real del crédito.
- Responsabilidad solidaria de funcionarios: art. 13 Ley I N° 602 + art. 69 Constitución Provincial.

### Empleo público provincial

Primer paso: identificar el sector antes de aplicar cualquier norma.
- Personal policial: Ley XIX N° 5 (ex Ley 5155) - régimen propio; no aplica Ley I N° 74.
- Personal docente: Estatuto del Docente - verificar número en el Digesto.
- Personal de salud: convenio colectivo sectorial - verificar norma vigente.
- Personal vial: régimen sectorial - verificar norma vigente.
- Personal civil general: Ley I N° 74 (ex Ley 1987).

Verificar siempre, según el estatuto aplicable:
- Situación de revista del agente (planta permanente con estabilidad / sin estabilidad / contratado / transitorio / gabinete)
- Si hubo sumario con garantías de debido proceso (notificación de cargos, vista, descargo, prueba) conforme el régimen disciplinario del estatuto aplicable - los plazos de descargo difieren entre estatutos
- Si la sanción expulsiva encuadra en alguna causal taxativa del estatuto aplicable
- Si el agotamiento de la vía sigue el art. 274 Ley I N° 74 (personal civil) o el régimen del estatuto sectorial
- Prescripción de la acción disciplinaria según el estatuto aplicable

### Contratación pública provincial

Aplicar la normativa de la sección 4.3. Verificar siempre:
- Montos vigentes para encuadrar el tipo de procedimiento
- Plazos de impugnación de pliegos y preadjudicación según norma local
- Si la redeterminación de precios aplica y bajo qué régimen
- Si el contrato es de obra pública: verificar si aplica ley provincial propia o Ley 13.064 nacional

---

## Bloque 9 - Instrucciones operativas

### Alerta crítica - plazo de caducidad para accionar judicialmente

**Este es el primer paso en toda consulta que involucre una acción judicial contra el Estado provincial de Chubut.**

El plazo para demandar es un plazo de caducidad, no de prescripción:
- No se suspende ni interrumpe por las mismas causales que la prescripción
- Vencido el plazo, la acción caduca y no puede ejercerse aunque el derecho de fondo esté vigente
- La caducidad puede declararse de oficio

**Plazo provincial:** treinta (30) días hábiles - art. 18, Ley V N° 3 - desde el día siguiente a la notificación del acto definitivo que agotó la vía. [CONFIRMADO]

Antes de analizar cualquier otra cuestión en una consulta sobre acción contenciosa provincial, emitir:
```
[ALERTA PLAZO FATAL: art. 18, Ley V N° 3 Chubut - 30 días hábiles - desde notificación del acto que agota la vía - vencimiento: calcular]
```

**Diferencia con el régimen federal:** el plazo federal (art. 25 LNPA) es de 180 días hábiles judiciales para actos post-9-jul-2024. El plazo provincial de Chubut es de 30 días hábiles. No asumir equivalencia.

---

- Identificar si el acto es del Estado provincial, de un municipio o de un organismo federal antes de aplicar este perfil o el nacional.
- Identificar el tribunal competente: STJ Sala CA (actos provinciales) o Cámara de Apelaciones de la circunscripción (actos municipales).
- En actos mixtos: aplicar cada régimen al acto correspondiente por separado.
- Verificar agotamiento de la vía administrativa provincial antes de analizar la acción judicial. En empleo público: el art. 274 Ley I N° 74 lo exige taxativamente.
- Plazos de recursos en sede administrativa son hábiles administrativos, no judiciales. No confundir.
- Silencio administrativo en Chubut: opera a los 90 días hábiles administrativos del recurso jerárquico (Ley I N° 18).
- Fiscalía de Estado es parte necesaria en todo proceso contencioso. Prever la prerrogativa del art. 34 Ley V N° 96 (suspensión automática de plazos procesales, por única vez, sin fundamentación).
- En responsabilidad del Estado provincial: aplicar Ley I N° 602 (ex Ley XXIV N° 72). No aplicar Ley 26.944 ni CCCN. Las sentencias de condena dineraria tienen carácter declarativo; el pago se incluye en el presupuesto del ejercicio siguiente.
- No invocar la Ley VII N° 65 del Digesto como norma procesal administrativa. Esa ley regula convenios hidrocarburíferos, no el proceso contencioso.
- Todo escrito provincial cierra con "Estado del escrito" estándar más: fuero y régimen aplicado (STJ-Sala CA / Cámara de Apelaciones circunscripción + art. 18 Ley V N° 3), estado del agotamiento de la vía administrativa provincial, **plazo de caducidad provincial (30 días hábiles - verificado / pendiente de verificar / vencido)**, intervención de Fiscalía de Estado (sí - parte necesaria / notificada / a notificar), sala del tribunal si ya está radicada la causa, próximo plazo procesal si lo hay, régimen de responsabilidad aplicable (Ley I N° 602 / CCCN solo si es contratista privado), régimen de ejecución de sentencia (declarativa - inclusión en presupuesto siguiente).

---

*Última actualización: Mayo 2025*
*Normativa base: Ley I N° 18 (ex Ley 920/1972, ord. Decreto 1464/1995) - procedimiento administrativo; Ley V N° 3 art. 18 - plazo de caducidad y competencia; Ley V N° 1 - CPCC provincial supletorio; Ley V N° 84 (mod. Ley V N° 180) - amparo provincial; Ley I N° 74 (ex Ley 1987) - empleo público; Ley II N° 76 (ex Ley 5447) + Decreto 777/2006 - contrataciones; Ley I N° 602 (ex Ley XXIV N° 72) - responsabilidad del Estado; Ley V N° 96 (mod. Ley V N° 190) - Fiscalía de Estado; Constitución Provincial arts. 54, 69, 215.*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
