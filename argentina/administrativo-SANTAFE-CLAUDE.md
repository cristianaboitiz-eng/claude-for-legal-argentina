# Perfil de práctica · Derecho administrativo · Provincia de Santa Fe

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) y el perfil administrativo nacional (administrativo-CLAUDE.md) con lógica específica del fuero contencioso administrativo de Santa Fe.
> Cargar junto con administrativo-CLAUDE.md en el Project. Este archivo no reemplaza al nacional - lo extiende.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.

---

## Configuración inicial - completar antes de usar

**PROVINCIA:** Provincia de Santa Fe

**FUERO_HABITUAL:** [COMPLETAR: denominación exacta del tribunal y circunscripción. Ej: "Cámara de lo Contencioso Administrativo N° 1, Santa Fe" / "Cámara de lo Contencioso Administrativo N° 2, Rosario" / "Corte Suprema de Justicia de Santa Fe (competencia originaria - municipios/comunas)". Las Cámaras de lo Contencioso Administrativo tienen competencia en 1ª instancia originaria. La CSJ Santa Fe tiene competencia especial cuando el recurrente es un Municipio o Comuna (art. 35 Ley 11.330).]

**AREAS_PRACTICA:** [COMPLETAR: áreas de mayor volumen dentro de administrativo Santa Fe. Ej: "Responsabilidad del Estado provincial, empleo público, contratación pública, sanciones administrativas, habilitaciones municipales".]

**ORGANISMO_CONTRALOR_HABITUAL:** [COMPLETAR: organismos provinciales o municipales ante los que se tramitan habitualmente los expedientes. Ej: "Ministerio de Salud Santa Fe, IAPOS, Municipalidad de Rosario, Municipalidad de Santa Fe".]

---

## Identidad y alcance

Este perfil cubre práctica de derecho administrativo en la Provincia de Santa Fe: procedimiento administrativo ante la Administración provincial (Decreto 4174/15) y municipal, recursos administrativos en sede provincial, recurso contencioso administrativo (Ley 11.330), responsabilidad del Estado provincial, empleo público provincial y contratación pública provincial.

**Particularidad estructural del sistema santafesino:** el control judicial de la actividad administrativa se articula como **recurso** (no como demanda ordinaria), y el tribunal que lo resuelve (Cámara de lo Contencioso Administrativo) actúa en instancia originaria e improrrogable. La Corte Suprema de Justicia de Santa Fe conoce en segunda instancia (salvo cuando el recurrente es un Municipio o Comuna, en cuyo caso la CSJ actúa en instancia originaria exclusiva).

**Articulación con el perfil nacional:** cuando actúa un organismo federal con sede en Santa Fe (ARCA/ex AFIP, ANSES, organismos desconcentrados nacionales), aplica el régimen federal (LNPA + RLNPA). Cuando actúa la Administración provincial o municipal santafesina, aplica este perfil. No transpolar plazos ni institutos.

**Tercer nivel - organismos municipales:** los actos de los Intendentes, Concejos Municipales y Comisiones Comunales son impugnables por la Ley 11.330 (art. 5). Cuando el recurrente es un **Municipio o Comuna** impugnando actos del Poder Ejecutivo provincial, la competencia es exclusiva de la **Corte Suprema de Justicia de Santa Fe** (art. 2 y art. 35 Ley 11.330). Verificar antes de radicar si la causa involucra a un municipio o una comuna como actor.

---

## Normativa de procedimiento administrativo provincial

### Reglamento para el trámite de actuaciones administrativas Santa Fe

- **Norma principal:** Decreto 4174/15 (Reglamento para el Trámite de Actuaciones Administrativas de la Provincia de Santa Fe), vigente desde el 1° de abril de 2016. Derogó el Decreto 10204/58 que era el anterior código de procedimiento.
- **Sin ley de procedimiento separada:** a diferencia de PBA (Dec-Ley 7647/70) y Córdoba (Ley 5350), en Santa Fe el procedimiento administrativo se rige por un decreto del Poder Ejecutivo, no por una ley de la Legislatura. El Dec 4174/15 es la norma de procedimiento vigente para la Administración centralizada.
- **Norma complementaria:** el Estatuto del Personal de la Administración Pública Provincial (Ley 8525) contiene normas específicas sobre recursos en materia de empleo público y régimen disciplinario.
- **Texto vigente:** consultar el portal oficial de Santa Fe: https://www.santafe.gov.ar o el digesto de ATE Santa Fe: https://documentos.atesantafe.com.ar/digesto
- **Articulado clave del Decreto 4174/15:** art. 42 (recurso de revocatoria), arts. 54-58 (recurso de apelación y jerárquico), arts. 29-50 (régimen de notificaciones), principios generales del procedimiento.

```
[VERIFICAR VIGENCIA: Decreto 4174/15 (Reglamento para el Trámite de Actuaciones Administrativas de Santa Fe) - consultar https://www.santafe.gov.ar antes de aplicar - verificar modificaciones posteriores a mayo 2026]
```

### Régimen de silencio administrativo Santa Fe

- **Regla general:** silencio negativo (denegatoria tácita). El Decreto 4174/15 prevé que si la autoridad no resuelve el recurso de revocatoria en el plazo fijado, el interesado puede articular el recurso jerárquico previo pedido de pronto despacho (art. del Decreto 4174/15).
- **Silencio en la Ley 11.330:** existe denegación presunta a efectos del recurso contencioso administrativo cuando la autoridad administrativa no se expide dentro de los 60 días de hallarse en condiciones de resolver en definitiva, o si paraliza injustificadamente el trámite durante más de 30 días (art. 9 Ley 11.330). Agotados los recursos que la dilación acordase, queda expedita la vía jurisdiccional desde la expiración del plazo.
- **Sin reforma análoga al Dec 971/2024 nacional:** Santa Fe no adoptó el régimen de silencio positivo de la Ley 27.742 nacional. El silencio positivo para autorizaciones regladas aplica solo ante la Administración nacional. No transpolar ese régimen al Estado provincial santafesino sin verificar.

```
[VERIFICAR RÉGIMEN DE SILENCIO SANTA FE: Dec 4174/15 + art. 9 Ley 11.330 - silencio negativo por regla general - denegación presunta a los 60 días sin resolución o 30 días de paralización + pronto despacho previo]
```

### Elementos esenciales del acto administrativo Santa Fe

El Decreto 4174/15 regula los elementos esenciales del acto administrativo con estructura análoga a los sistemas administrativos argentinos:

1. Competencia: atribución del órgano provincial o municipal
2. Causa: antecedentes de hecho y de derecho
3. Objeto: cierto, lícito, físicamente posible
4. Procedimiento: trámites esenciales previos (incluye intervención de Fiscalía de Estado cuando corresponde)
5. Motivación: expresión concreta de las razones del dictado del acto
6. Finalidad: adecuada al ordenamiento provincial

**Vicios del acto:** el Decreto 4174/15 recoge la doctrina de nulidad absoluta/relativa con estructura análoga al régimen federal. Verificar artículos específicos en el texto consolidado.

### Recursos administrativos Santa Fe (Decreto 4174/15)

**Recurso de revocatoria (art. 42 Decreto 4174/15):**
- Plazo: 10 días hábiles administrativos desde la notificación del acto
- Ante: la misma autoridad que dictó el acto
- Fundamento: puede fundarse en razones de ilegitimidad y también en razones de oportunidad, mérito o conveniencia
- La autoridad dispone de 30 días para resolver, prorrogables por 10 días adicionales
- La resolución queda firme a los 10 días de notificada, salvo que dentro de ese término se interponga recurso de apelación ante el PE (si fue dictada por autoridad inferior)
- Si el acto fue dictado por el PE: la resolución del recurso de revocatoria agota la vía (previa vista a Fiscalía de Estado)
- Si no se resuelve en plazo: el interesado puede articular el recurso jerárquico previo pronto despacho

**Recurso de apelación (arts. 54-57 Decreto 4174/15):**
- Plazo: 10 días hábiles desde la notificación de la resolución que resuelve el recurso de revocatoria
- Ante: el Poder Ejecutivo (actúa como segunda instancia administrativa)
- Puede interponerse subsidiariamente con el recurso de revocatoria
- Fundamento: puede fundarse en ilegitimidad y también en oportunidad, mérito o conveniencia
- El PE resuelve con dictamen previo de la Fiscalía de Estado; su resolución agota la vía administrativa

**Recurso jerárquico (art. 58 Decreto 4174/15):**
- Procede ante el Poder Ejecutivo cuando los órganos de la Administración Centralizada o los entes descentralizados han denegado tácitamente un derecho o incurrido en retardación indebida
- Requiere pedido de pronto despacho previo
- Agota la vía: sí, cuando es resuelto por el PE

**Estructura de la cadena recursiva:**
La cadena típica en Santa Fe es: **revocatoria ante el órgano emisor → apelación ante el PE**. Es diferente a la cadena federal (reconsideración → jerárquico) y a la de PBA (revocatoria → jerárquico). No confundir las denominaciones ni la lógica de cada sistema.

**Sin reforma análoga al Decreto 695/2024 nacional:** Santa Fe no duplicó los plazos de recursos administrativos. El plazo del Dec 4174/15 para la revocatoria es de 10 días hábiles administrativos. No aplicar los plazos federales reformados.

```
[ALERTA PLAZO FATAL: recurso de revocatoria - Dec 4174/15 art. 42 - 10 días hábiles administrativos desde notificación del acto - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de apelación - Dec 4174/15 arts. 54-57 - 10 días hábiles desde notificación de la resolución de la revocatoria - ante el PE - vencimiento: calcular]
```

### Agotamiento de la vía administrativa Santa Fe

- **Regla general:** el agotamiento de la vía administrativa mediante los recursos reglamentados en sede administrativa es requisito previo e ineludible para ejercer el recurso contencioso administrativo de la Ley 11.330 (art. 7 Ley 11.330). No se puede ejercer el recurso sin agotar previamente la vía administrativa.
- **Solo se pueden juzgar pretensiones propuestas y resueltas en la reclamación previa:** esta es una particularidad crítica del sistema santafesino. El objeto del recurso contencioso administrativo está delimitado por lo planteado en sede administrativa. Pretensiones no articuladas en sede administrativa no pueden introducirse en el recurso judicial.
- **Vía de agotamiento:** revocatoria ante el órgano emisor + apelación ante el PE (en la cadena normal de la Administración centralizada).
- **Entes autárquicos:** la revocatoria ante el propio ente + la posible alzada o apelación ante el PE, según la normativa específica del ente.
- **Denegatoria tácita:** si la autoridad no se expide en los plazos del Dec 4174/15, el interesado puede articular el recurso siguiente previo pronto despacho, y eventualmente considerar agotada la vía por silencio (art. 9 Ley 11.330).
- **Intervención de Fiscalía de Estado:** previa al dictado del acto que resuelve el recurso de revocatoria contra un decreto del PE, y en el recurso de apelación ante el PE. La omisión del dictamen cuando es preceptivo puede configurar vicio de procedimiento.

```
[VERIFICAR AGOTAMIENTO DE VÍA SANTA FE: Dec 4174/15 - verificar cadena recursiva completa (revocatoria + apelación ante PE) - verificar que las pretensiones del recurso judicial coincidan con las articuladas en sede administrativa (art. 7 Ley 11.330)]
```

---

## Control judicial contencioso administrativo

### Ley del recurso contencioso administrativo Santa Fe

- **Norma:** Ley 11.330 (Ley del Recurso Contencioso Administrativo de la Provincia de Santa Fe), sancionada en 1995, reglamentaria del art. 93 inc. 2 de la Constitución Provincial
- **Texto vigente:** https://www.santafe.gov.ar/normativa (buscar Ley 11.330) y portal del Poder Judicial de Santa Fe: https://www.justiciasantafe.gov.ar
- **Subsidiariedad:** se rige supletoriamente por el Código Procesal Civil y Comercial de Santa Fe en lo aplicable (art. 1 Ley 11.330)
- **Naturaleza:** el proceso se denomina y articula como **recurso**, no como demanda. Esta terminología es propia del sistema santafesino y tiene consecuencias prácticas: el objeto del proceso está acotado por lo resuelto en sede administrativa (art. 7 Ley 11.330).

### Plazo del recurso contencioso administrativo

**Este es el dato más crítico del perfil.**

- **Plazo general:** 30 días contados desde la notificación o publicación oficial de la resolución denegatoria del derecho o interés legítimo postulado, o desde el conocimiento pleno de la resolución que el interesado exteriorizara en el expediente administrativo (art. 9 Ley 11.330)
- **Cómputo:** días hábiles judiciales [VERIFICAR: el art. 9 dice "días" sin calificación; la jurisprudencia de la CSJ Santa Fe ha interpretado que son días hábiles judiciales - verificar criterio vigente antes de computar]
- **Denegación presunta:** si la autoridad no se expide dentro de los 60 días de hallarse en condiciones de resolver, o paraliza el trámite más de 30 días, queda expedita la vía jurisdiccional desde la expiración del plazo respectivo (art. 9 in fine Ley 11.330)
- **Naturaleza:** caducidad - no se suspende ni interrumpe salvo norma expresa
- **¿Declarable de oficio?:** sí, la CSJ Santa Fe verifica la admisibilidad incluyendo el plazo antes de dar curso al recurso (art. 12 Ley 11.330)

```
[ALERTA PLAZO FATAL: art. 9 Ley 11.330 RCA Santa Fe - 30 días - desde notificación/publicación de la resolución denegatoria que agota la vía - vencimiento: calcular]
```

**Diferencia crítica con otros regímenes:**
- Federal: 180 días hábiles judiciales (actos post-9-jul-2024)
- PBA: 90 días hábiles judiciales
- Córdoba: 30 días hábiles judiciales
- **Santa Fe: 30 días** (verificar si son hábiles judiciales o corridos según jurisprudencia CSJ Santa Fe)

**Requisito de pago previo en materia tributaria (art. 8 Ley 11.330):** cuando la resolución ordena el pago de contribuciones fiscales, no puede promoverse el recurso sin satisfacerlas previamente (excluida la parte correspondiente a recargos, multas e intereses).

```
[ALERTA ADMISIBILIDAD - PAGO PREVIO: art. 8 Ley 11.330 Santa Fe - en materia tributaria, verificar si la resolución ordena pago de contribuciones fiscales - el recurso contencioso administrativo no puede promoverse sin satisfacer ese pago previo (excluidos recargos, multas e intereses) - verificar cumplimiento antes de radicar]
```

### Actos impugnables (art. 3 Ley 11.330)

El recurso procede contra actos de la Administración Pública regidos por el ordenamiento jurídico administrativo que sean lesivos de un modo directo y actual de un **derecho subjetivo o un interés legítimo**, ya sean:
- Actos definitivos
- Actos de trámite que decidan directa o indirectamente el fondo del asunto o pongan término al proceso

**No corresponde a la jurisdicción contencioso administrativa (art. 6 Ley 11.330):**
- Actos del poder político del Estado
- Actos relacionados con derechos o intereses que tutela el derecho privado
- Actos discrecionales (en cuanto deban reputarse tales)
- Actos que resuelvan reclamos de agentes en materia de accidentes de trabajo
- Actos que sean reproducción, confirmación o ejecución de otros anteriores ya consentidos

**Actos reglamentarios:** no son impugnables, excepto que por sí mismos y sin necesidad de aplicación individual produzcan efectos en relación al recurrente.

**Alcance del recurso:** se funda en un vicio de **ilegitimidad** del acto, y se propone la anulación total o parcial y la reintegración del recurrente en la situación jurídica vulnerada (art. 4 Ley 11.330). La pretensión resarcitoria por daños puede acumularse.

### Órganos jurisdiccionales

**Primera instancia - instancia originaria:**
- **Cámaras de lo Contencioso Administrativo:** son los tribunales de instancia originaria e improrrogable. Hay Cámara de lo Contencioso Administrativo en Santa Fe y en Rosario (las dos circunscripciones principales). La competencia es improrrogable aún entre las propias Cámaras.
- Las Cámaras actúan como primera y única instancia ordinaria; no hay juzgados de primera instancia en lo contencioso administrativo (a diferencia de PBA y del fuero contencioso federal).

**Instancia especial - Municipios y Comunas:**
- Cuando el **recurrente es un Municipio o Comuna** impugnando actos del Poder Ejecutivo Provincial, la competencia es exclusiva e improrrogable de la **Corte Suprema de Justicia de Santa Fe** (art. 2 y art. 35 Ley 11.330). La CSJ actúa en instancia originaria en esos casos.

**Alzada:**
- **Corte Suprema de Justicia de Santa Fe:** es la segunda instancia de las Cámaras de lo Contencioso Administrativo. Conoce por vía de los recursos de inconstitucionalidad y de casación (art. 37 Ley 11.330). El recurso de casación procede por inobservancia o grave error en la aplicación de normas de derecho o doctrina legal, y en caso de sentencias contradictorias entre las Cámaras.
- **Avocación de la CSJ:** dentro de los 5 días de notificado el llamamiento de autos para sentencia por la Cámara, cualquier parte puede solicitar a la CSJ que se avoque al conocimiento del recurso por existir interés institucional suficiente (art. 36 Ley 11.330).

```
[ALERTA PLAZO FATAL: avocación CSJ Santa Fe - art. 36 Ley 11.330 - 5 días desde la notificación del llamamiento de autos para sentencia por la Cámara - vencido el plazo, la solicitud es inadmisible - vencimiento: calcular]
```

**Procurador General / Fiscal de Cámara:**
- El Procurador General de Santa Fe y los Fiscales de Cámara intervienen en el proceso contencioso administrativo. Antes de declarar admisible o inadmisible el recurso, el Presidente de la Cámara o de la CSJ oye al Procurador General o Fiscal de Cámara (art. 12 Ley 11.330).

### Tutela cautelar (arts. 14-15 Ley 11.330)

- **Requisitos:** que el recurso parezca fundado de tal modo que en principio pueda considerarse jurídicamente aceptable la posición del recurrente + peligro por la demora del proceso + ponderación de los intereses en juego.
- **Alcance:** el Tribunal puede adoptar medidas urgentes idóneas para asegurar provisionalmente los efectos de la sentencia, incluyendo mandamientos a la autoridad administrativa para conservar o restablecer una situación o hacer cesar un trastorno manifiestamente ilegal. También puede ordenar una provisión justa y razonable ante obligación pública no seriamente cuestionable.
- **Suspensión del acto:** procede si "prima facie" resulta verosímil la ilegitimidad del acto o si su cumplimiento causaría perjuicios graves o de reparación difícil.
- **Trámite cautelar:** vista previa por 5 días a la recurrida; el Tribunal resuelve en 5 días.
- **Caución:** puede exigirse para responder por daños al interés público o de terceros. No se exige a funcionarios, empleados, jubilados y pensionados en causas vinculadas a sus derechos como tales.
- **Levantamiento por interés público:** la autoridad administrativa puede solicitar el cese de la cautelar si produce grave daño al interés público; el Tribunal corre traslado por 5 días al recurrente y resuelve. La decisión es apelable ante la CSJ.
- **No aplica Ley 26.854 nacional:** ese régimen rige solo contra el Estado nacional.

```
[VERIFICAR RÉGIMEN CAUTELAR SANTA FE: Ley 11.330 arts. 14-15 - verosimilitud + peligro + ponderación de intereses - vista previa 5 días a la recurrida - no aplica Ley 26.854]
```

### Amparo Santa Fe

- **Norma:** art. 17 Constitución Santa Fe + Ley 10.456 (Ley de Amparo de Santa Fe, 1989) y modificatorias
- **Plazo:** verificar plazo de caducidad de la Ley 10.456. La ley establece un plazo específico desde que el afectado conoció o pudo conocer el acto lesivo [VERIFICAR VIGENCIA: Ley 10.456 plazo de caducidad - consultar texto actualizado]
- **Competencia:** cuando la demandada es el Estado provincial, los Juzgados de Primera Instancia de Distrito tienen aptitud para entender en amparos (art. 4 Ley 10.456); sin embargo, si la materia es contencioso administrativa, existe jurisprudencia de la CSJ Santa Fe que atribuye competencia a la Cámara de lo Contencioso Administrativo (verificar jurisprudencia vigente).
- **Subsidiariedad:** procede cuando no existe otra vía judicial más idónea. Dado que la Ley 11.330 prevé tutela cautelar amplia, el amparo tiene aplicación más restringida en materia administrativa.
- **Amparo por mora:** procede ante la inactividad de la Administración. Verificar regulación específica en la Ley 10.456.

```
[VERIFICAR AMPARO SANTA FE: Ley 10.456 - plazo de caducidad - competencia (Juzgado de Distrito o Cámara CA según materia) - consultar jurisprudencia CSJ Santa Fe vigente]
```

---

## Normativa de referencia Santa Fe

### Responsabilidad del Estado provincial

- **Sin ley propia equivalente a Ley 26.944 nacional:** Santa Fe no sancionó una ley de responsabilidad del Estado equivalente a la Ley 26.944. Ésta no aplica a demandas contra el Estado provincial santafesino.
- **Régimen aplicable:** principios generales del derecho administrativo y jurisprudencia de la CSJ Santa Fe. La Fiscalía de Estado publica dictámenes sobre responsabilidad que son referencia doctrinal relevante en la práctica local.
- **Reclamo administrativo previo:** en materia de responsabilidad del Estado provincial, la Fiscalía de Estado ha elaborado criterios sobre el reclamo administrativo previo del Decreto 4174/15 como paso previo a la acción judicial por daños y perjuicios. Verificar dictámenes de la Fiscalía de Estado antes de articular la pretensión.
- **No aplicar CCCN:** no invocar arts. 1757, 1741 ni otros del CCCN en demandas contra el Estado provincial sin verificar criterio de la CSJ Santa Fe.
- **Prescripción:** verificar criterio de la CSJ Santa Fe; puede diferir del plazo de 3 años del art. 7 Ley 26.944 federal.

```
[VERIFICAR RÉGIMEN DE RESPONSABILIDAD SANTA FE: sin ley propia equivalente a Ley 26.944 - principios generales + jurisprudencia CSJ Santa Fe + dictámenes Fiscalía de Estado - verificar reclamo administrativo previo del Dec 4174/15 como paso previo]
```

### Empleo público Santa Fe

- **Estatuto general:** Ley 8525 (Estatuto del Personal de la Administración Pública Provincial de Santa Fe, 1979) y modificatorias. Rige las relaciones laborales del personal dependiente del Poder Ejecutivo provincial.
- **Escalafón:** Decreto 2695/83 (Escalafón del Personal Civil de la Administración Pública de Santa Fe) y modificatorias.
- **Régimen disciplinario (arts. 64-75 Ley 8525):** sumario administrativo con garantías de debido proceso. Los plazos del procedimiento disciplinario son días hábiles administrativos (art. 75 Ley 8525).
- **Estatutos sectoriales principales:**
  - Docentes: verificar norma sectorial vigente (Ley 10.296 Estatuto del Docente y sus modificatorias)
  - Policía: Ley 7395 (Ley Orgánica de la Policía de la Provincia de Santa Fe) y modificatorias
  - Personal de salud: verificar norma sectorial vigente
  - Personal municipal: verificar si el municipio tiene estatuto propio o remite a la Ley 8525 supletoriamente
  - [COMPLETAR: otros estatutos sectoriales según las áreas de práctica habituales]
- **Obra social:** IAPOS (Instituto Autárquico Provincial de Obra Social de Santa Fe). Sus resoluciones son impugnables ante el fuero contencioso administrativo.

```
[VERIFICAR ESTATUTO APLICABLE SANTA FE: Ley 8525 general o estatuto sectorial según el organismo y la categoría del agente - Escalafón: Decreto 2695/83]
```

### Contratación pública Santa Fe

- **Norma general:** Ley 12.510 (Ley de Administración, Eficiencia y Control del Estado de Santa Fe, 2005) y modificatorias. Regula el sistema de contrataciones del Estado provincial.
- **Reglamento:** verificar decretos reglamentarios vigentes de la Ley 12.510 sobre contrataciones. Los umbrales y procedimientos se actualizan por decreto o resolución.
- **Organismo rector:** verificar denominación actual del organismo rector de contrataciones en Santa Fe (históricamente bajo la órbita del Ministerio de Economía).
- **Plataforma de compras:** verificar sistema electrónico de contrataciones vigente en Santa Fe. El uso de medios informáticos está previsto en la Ley 12.510.
- **Obra pública provincial:** verificar ley de obras públicas provincial vigente. La Ley 13.064 (obra pública nacional) no aplica supletoriamente a obra pública provincial salvo remisión contractual expresa.
- **Impugnación de licitaciones:** los plazos para impugnar pliegos y preadjudicación están fijados en la Ley 12.510 y en cada pliego. Verificar antes de analizar la admisibilidad.

```
[VERIFICAR VIGENCIA: Ley 12.510 Santa Fe y decretos reglamentarios - los montos de licitación pública/privada/contratación directa se actualizan - verificar antes de encuadrar el procedimiento]
```

### Organismos de control Santa Fe

**Tribunal de Cuentas de Santa Fe:**
- Control externo de la hacienda pública provincial. Tiene función jurisdiccional. Sus resoluciones definitivas son impugnables ante el fuero contencioso administrativo (Ley 11.330).

**Fiscalía de Estado de Santa Fe:**
- Representante legal del Estado provincial en juicio. Interviene con dictamen obligatorio en los recursos de revocatoria interpuestos contra decretos del PE y en los recursos de apelación ante el PE.
- En el proceso contencioso administrativo: la Fiscalía de Estado representa al Estado provincial como parte recurrida (art. 20 Ley 11.330; los representantes del Estado no pueden desistir ni transigir sin autorización especial).
- La Fiscalía de Estado publica dictámenes que son referencia doctrinal relevante para la práctica local. Consultar: https://www.santafe.gob.ar (Fiscalía de Estado).
- Las notificaciones a la Fiscalía de Estado se hacen en su despacho oficial.

**Procurador General / Fiscales de Cámara:**
- El Procurador General y los Fiscales de Cámara de lo Contencioso Administrativo tienen intervención en el proceso judicial (art. 12 Ley 11.330). El Tribunal los oye antes de declarar admisible o inadmisible el recurso.

**Defensor del Pueblo de Santa Fe:**
- Art. 86 Constitución Santa Fe. Legitimación para actuar en defensa de derechos colectivos.

---

## Alerta normativa - normas de vigencia variable

*Última verificación de esta sección: mayo 2026. Actualizar cuando cambie alguna de las normas listadas.*

### Plazo del RCA Santa Fe

```
[ALERTA PLAZO FATAL: art. 9 Ley 11.330 RCA Santa Fe - 30 días - desde notificación/publicación de la resolución denegatoria que agota la vía - verificar si son hábiles judiciales o corridos según jurisprudencia CSJ Santa Fe - vencimiento: calcular]
```

### Normas de vigencia variable a verificar en cada consulta

- **Montos de contratación pública (Ley 12.510):** los umbrales para licitación pública, privada y contratación directa se actualizan por decreto o resolución. Verificar antes de encuadrar el procedimiento.
- **Escala salarial empleo público Santa Fe:** se modifica por paritarias. No asumir montos sin verificar la resolución de homologación vigente.
- **Habilitaciones municipales:** el régimen varía por municipio (Rosario y Santa Fe tienen ordenanzas propias). Ante cualquier habilitación o sanción municipal, verificar norma vigente al momento del acto.
- **Competencia en amparo:** la jurisprudencia de la CSJ Santa Fe sobre competencia en amparos contra el Estado puede cambiar. Verificar antes de radicar.

```
[VERIFICAR VIGENCIA: norma Santa Fe - [materia] - consultar Boletín Oficial Santa Fe (https://www.santafe.gov.ar/boletinoficial) antes de aplicar]
```

---

## Responsables procesales por instancia

| Instancia | Representante del Estado | Normativa |
|-----------|--------------------------|-----------|
| Cámara de lo Contencioso Administrativo N° 1 (Santa Fe) | Fiscalía de Estado de Santa Fe | Art. 20 Ley 11.330 |
| Cámara de lo Contencioso Administrativo N° 2 (Rosario) | Fiscalía de Estado de Santa Fe | Art. 20 Ley 11.330 |
| Corte Suprema de Justicia de Santa Fe (alzada y competencia originaria Municipios/Comunas) | Fiscalía de Estado de Santa Fe | Art. 20 Ley 11.330 |
| Intervención del Procurador General / Fiscal de Cámara | Antes de declarar admisible o inadmisible el recurso, el Presidente oye al Procurador General o Fiscal de Cámara | Art. 12 Ley 11.330 |
| Estado como recurrente (impugna acto propio) | [A VERIFICAR: verificar si la Fiscalía de Estado actúa también cuando la Provincia es recurrente o si interviene otro órgano] | Art. 20 Ley 11.330 |

**Nota operativa:** la Fiscalía de Estado representa al Estado provincial como parte recurrida; los representantes no pueden desistir ni transigir sin autorización especial (art. 20 Ley 11.330). Las notificaciones a la Fiscalía de Estado se hacen en su despacho oficial.

```
[VERIFICAR REPRESENTACIÓN PROCESAL SANTA FE: art. 20 Ley 11.330 - Fiscalía de Estado como representante del Estado recurrido - notificaciones en despacho oficial - sin autorización especial para desistir o transigir]
```

---

## Fuentes primarias

- **Boletín Oficial Santa Fe:** https://www.santafe.gov.ar/boletinoficial
- **Portal de normativa Santa Fe:** https://www.santafe.gov.ar/normativa
- **Poder Judicial Santa Fe (jurisprudencia):** https://www.justiciasantafe.gov.ar
- **Fiscalía de Estado Santa Fe:** https://www.santafe.gob.ar (Fiscalía de Estado)
- **IAPOS:** https://www.iapos.gov.ar
- **ATE Santa Fe - Digesto normativo:** https://documentos.atesantafe.com.ar/digesto

---

## Reglas de citación - administrativo Santa Fe

Las reglas generales del CLAUDE.md argentino y del administrativo-CLAUDE.md nacional aplican íntegramente. Específicas para el fuero contencioso administrativo Santa Fe:

**Jurisprudencia:** nunca citar sala, expediente o carátula sin material aportado. La CSJ Santa Fe y las Cámaras de lo Contencioso Administrativo pueden tener criterios distintos en cuestiones no resueltas uniformemente. Usar:
```
[INSERTAR FALLO VERIFICADO: CSJ Santa Fe / Cámara CA [Santa Fe / Rosario] - doctrina requerida]
```

**Actos administrativos Santa Fe:** no asumir el contenido de resoluciones, dictámenes de la Fiscalía de Estado o actos impugnados sin que el abogado los aporte. Usar:
```
[VACÍO PROBATORIO: texto del acto administrativo provincial/municipal no aportado - aportar copia del acto impugnado con sello de notificación]
```

**Plazos RCA Santa Fe:** no transpolar plazos del régimen federal ni de PBA ni de Córdoba. Usar:
```
[ALERTA PLAZO FATAL: art. 9 Ley 11.330 RCA Santa Fe - 30 días desde notificación de la resolución denegatoria - verificar si son hábiles judiciales o corridos - vencimiento: calcular]
```

**Dictámenes de Fiscalía de Estado:** no asumir su contenido sin material aportado. Usar:
```
[VACÍO PROBATORIO: dictamen de Fiscalía de Estado Santa Fe no aportado - verificar intervención en el expediente administrativo]
```

---

## Lógica de análisis por institución

### Checklist: acto administrativo provincial/municipal

Aplicar Decreto 4174/15. Elementos: competencia, causa, objeto, procedimiento, motivación, finalidad.

1. ¿Qué acto se impugna? ¿Es del Estado provincial (Administración centralizada o ente autárquico) o de un municipio/comuna? ¿Es definitivo o de trámite que decide el fondo?
2. ¿El acto fue notificado fehacientemente? ¿En qué fecha? (inicio del cómputo del art. 9 Ley 11.330)
3. ¿Qué elementos del acto se cuestionan? ¿Es un vicio de ilegitimidad? (requisito del art. 4 Ley 11.330)
4. ¿Hay expediente administrativo que lo respalda? ¿El abogado lo tiene o hay que pedirlo por vista?
5. ¿Se interpuso recurso de revocatoria en plazo? ¿Fue resuelto? ¿Se apeló ante el PE?
6. ¿Las pretensiones que se quieren plantear en el recurso judicial coinciden con las articuladas en sede administrativa? (art. 7 Ley 11.330 - límite crítico)
7. ¿Intervino la Fiscalía de Estado cuando era preceptivo? ¿El dictamen fue emitido antes del acto?

### Checklist: recursos administrativos Santa Fe

Aplicar Dec 4174/15. En cada recurso verificar:

1. Plazo desde la notificación en días hábiles administrativos: revocatoria 10 días (art. 42) / apelación ante PE 10 días (arts. 54-57).
2. Cadena: revocatoria → apelación ante PE. No confundir con la cadena federal (reconsideración → jerárquico) ni con la de PBA (revocatoria → jerárquico).
3. Si la autoridad emisora es el PE directamente: la revocatoria ante el PE agota la vía (previa vista a Fiscalía de Estado); no hay apelación posterior.
4. Articular en sede administrativa todas las pretensiones que se quieran plantear en el recurso judicial. Las no articuladas no pueden introducirse después (art. 7 Ley 11.330).
5. Los recursos no suspenden la ejecutoriedad del acto salvo petición expresa con fundamento. Evaluar si el cliente necesita suspensión y por qué vía solicitarla.

```
[ALERTA PLAZO FATAL: recurso de revocatoria - Dec 4174/15 art. 42 - 10 días hábiles administrativos desde notificación - vencimiento: calcular]
[ALERTA PLAZO FATAL: recurso de apelación ante PE - Dec 4174/15 arts. 54-57 - 10 días hábiles desde notificación de la resolución de la revocatoria - vencimiento: calcular]
```

### Checklist: agotamiento de la vía y acción judicial

Antes de analizar cualquier acción ante las Cámaras de lo Contencioso Administrativo:

1. Verificar si se interpusieron revocatoria + apelación ante el PE en plazo (Dec 4174/15).
2. Verificar que las pretensiones del recurso judicial no superen lo planteado en sede administrativa (art. 7 Ley 11.330).
3. Verificar intervención preceptiva de la Fiscalía de Estado en el trámite administrativo.
4. Verificar si la vía quedó agotada por silencio (art. 9 Ley 11.330: 60 días sin resolver en condiciones de hacerlo, o 30 días de paralización injustificada).
5. Calcular el plazo del art. 9 Ley 11.330 (30 días; verificar si son hábiles judiciales o corridos según jurisprudencia CSJ Santa Fe).
6. Verificar tribunal competente: Cámara CA Santa Fe / Cámara CA Rosario / CSJ Santa Fe (competencia originaria si el recurrente es un Municipio o Comuna, art. 35 Ley 11.330).
7. En materia tributaria: verificar si aplica el pago previo del art. 8 Ley 11.330.

### Checklist: responsabilidad del Estado Santa Fe

1. Verificar reclamo administrativo previo del Dec 4174/15 como paso previo a la acción resarcitoria.
2. No aplicar Ley 26.944 ni CCCN sin verificar criterio de la CSJ Santa Fe; aportar fallo del tribunal.
3. Consultar dictámenes de la Fiscalía de Estado sobre responsabilidad publicados en https://www.santafe.gob.ar.
4. Verificar prescripción según criterio local; puede diferir del plazo de 3 años del art. 7 Ley 26.944.
5. Si la pretensión resarcitoria se acumula al recurso de ilegitimidad: verificar si la Cámara lo admite o exige proceso autónomo posterior.

```
[INSERTAR FALLO VERIFICADO: CSJ Santa Fe / Cámara CA - requisitos de la responsabilidad extracontractual del Estado provincial]
[INSERTAR FALLO VERIFICADO: CSJ Santa Fe / Cámara CA - régimen de prescripción de la acción resarcitoria contra el Estado provincial]
```

### Checklist: empleo público Santa Fe

1. Identificar el estatuto aplicable: Ley 8525 (general) o sectorial (Ley 10.296 docentes / Ley 7395 policía / personal municipal: verificar si el municipio tiene estatuto propio o aplica Ley 8525 supletoriamente / otro).
2. Situación de revista del agente: planta permanente con estabilidad / sin estabilidad / contratado / transitorio / gabinete.
3. ¿Hubo sumario con garantías de debido proceso? (Ley 8525 arts. 64-75: vista por 10 días, prueba en 15 días, resolución.)
4. ¿La sanción expulsiva encuadra en alguna causal taxativa del estatuto?
5. Verificar si la sanción fue impugnada por la cadena recursiva del Dec 4174/15 antes de ir al recurso judicial; si no se impugnó en sede administrativa, puede no estar agotada la vía.
6. Verificar prescripción de la acción disciplinaria según la Ley 8525.

```
[VERIFICAR ESTATUTO APLICABLE SANTA FE: Ley 8525 general o estatuto sectorial según el organismo y la categoría del agente - Escalafón: Decreto 2695/83]
```

### Checklist: contratación pública Santa Fe

1. Verificar montos vigentes según Ley 12.510 y resoluciones del organismo rector para encuadrar el tipo de procedimiento (licitación pública / privada / contratación directa).
2. Verificar plazos de impugnación de pliegos y preadjudicación en la Ley 12.510 y en el pliego específico.
3. Para obra pública: verificar ley provincial aplicable; la Ley 13.064 nacional no rige para obra pública provincial salvo remisión contractual expresa.
4. Verificar si el contrato prevé redeterminación de precios y bajo qué régimen provincial.

```
[VERIFICAR VIGENCIA: Ley 12.510 Santa Fe y decretos reglamentarios - montos actualizados por resolución - consultar plataforma provincial antes de encuadrar el procedimiento]
```

---

## Instrucciones operativas específicas - Santa Fe

### Alerta crítica - plazo del recurso contencioso administrativo Santa Fe

**Este es el primer paso en toda consulta que involucre la impugnación de un acto del Estado provincial o municipal santafesino.**

El plazo del art. 9 Ley 11.330 es de caducidad, no de prescripción:
- No se suspende ni interrumpe salvo norma expresa
- Vencido el plazo, el recurso es inadmisible (el Tribunal lo verifica de oficio, art. 12 Ley 11.330)
- La caducidad opera de pleno derecho

**Plazo:** 30 días desde la notificación o publicación oficial de la resolución denegatoria (o desde el conocimiento pleno exteriorizado en el expediente). Verificar si son hábiles judiciales o corridos según jurisprudencia CSJ Santa Fe vigente.

Antes de analizar cualquier otra cuestión, emitir:
```
[ALERTA PLAZO FATAL: art. 9 Ley 11.330 RCA Santa Fe - 30 días desde notificación/publicación de la resolución denegatoria que agota la vía - verificar naturaleza del plazo (hábiles o corridos) en jurisprudencia CSJ Santa Fe - vencimiento: calcular]
```

**Diferencia crítica:** federal 180 días / PBA 90 días / Córdoba 30 días hábiles judiciales / **Santa Fe 30 días** (verificar naturaleza). No aplicar bajo ningún concepto plazos de otros regímenes.

**Alerta adicional - límite de pretensiones:** verificar que lo que se quiere plantear en el recurso judicial haya sido planteado en sede administrativa (art. 7 Ley 11.330). Este es un error frecuente y fatal.

---

- Identificar si el acto es del Estado provincial santafesino, de un municipio/comuna santafesino o de un organismo federal antes de aplicar este perfil o el nacional.
- Si el recurrente es un Municipio o Comuna impugnando actos del PE provincial: competencia exclusiva de la CSJ Santa Fe (art. 35 Ley 11.330).
- Verificar agotamiento de la vía (Dec 4174/15: revocatoria + apelación ante PE) antes de analizar el recurso judicial.
- Articular en sede administrativa todas las pretensiones que se quieran sostener en el recurso judicial; las no articuladas en sede no pueden introducirse después (art. 7 Ley 11.330).
- Plazos en sede administrativa: 10 días hábiles administrativos para revocatoria y para apelación. No confundir con plazos judiciales.
- En responsabilidad del Estado: no aplicar Ley 26.944 ni CCCN sin verificar criterio de la CSJ Santa Fe; verificar necesidad de reclamo previo.
- En empleo público: verificar Ley 8525 o estatuto sectorial antes de analizar los derechos del agente.
- En contratación pública: verificar Ley 12.510 y montos vigentes.
- Verificar intervención preceptiva de la Fiscalía de Estado (recursos ante el PE, proceso judicial).
- No asumir el contenido de actos, expedientes ni dictámenes sin que el abogado los aporte.
- Todo escrito ante el fuero contencioso administrativo santafesino cierra con "Estado del escrito" estándar más: tribunal competente (Cámara CA Santa Fe / Cámara CA Rosario / CSJ Santa Fe), estado del agotamiento de la vía, **plazo art. 9 Ley 11.330 (verificado / pendiente de verificar / vencido)**, verificación de coincidencia entre pretensiones judiciales y planteadas en sede administrativa (art. 7 Ley 11.330), intervención de Fiscalía de Estado (sí / no / a verificar), próximo plazo procesal.

---

*Última actualización: mayo 2026*
*Normativa base: Decreto 4174/15 (Reglamento para el Trámite de Actuaciones Administrativas), Ley 11.330 (RCA Santa Fe), Ley 10.456 (amparo Santa Fe), Ley 8525 (empleo público), Decreto 2695/83 (escalafón), Ley 10.296 (estatuto docente), Ley 7395 (policía), Ley 12.510 (Ley de Administración, Eficiencia y Control del Estado), Constitución de Santa Fe arts. 17, 86, 93*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
