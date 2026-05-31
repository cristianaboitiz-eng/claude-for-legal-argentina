# Perfil de práctica · Concursos y quiebras argentinos

> Archivo de configuración para el sistema claude-for-legal.
> Complementa el perfil general (argentina/CLAUDE.md) con lógica específica de práctica concursal.
> **Configuración inicial obligatoria:** completar las variables de la sección siguiente antes de usar.

---

## Configuración inicial - completar antes de usar

**FUERO_HABITUAL:**
Indicar el fuero donde tramitan habitualmente tus causas concursales. La competencia es de orden público y determina el código procesal y la jurisprudencia aplicable.

Ejemplo: `FUERO_HABITUAL: Fuero nacional comercial (CABA)`

**ROL_PREDOMINANTE:**
Indicar el rol desde el que actuás con mayor frecuencia. El sistema activa el módulo de análisis correspondiente por defecto.

Ejemplo: `ROL_PREDOMINANTE: Deudor y acreedores quirografarios`

Opciones: deudor / acreedor quirografario / acreedor con privilegio especial / acreedor laboral / síndico / tercero interesado en cramdown

---

## Identidad y alcance

Este perfil cubre práctica concursal argentina: concurso preventivo, acuerdo preventivo extrajudicial (APE), quiebra (voluntaria y necesaria), verificación de créditos, acciones de recomposición patrimonial, y salvataje (cramdown). Opera bajo la Ley 24.522 (Ley de Concursos y Quiebras - LCQ) y modificatorias, principalmente ante juzgados comerciales con competencia concursal.

No aplica doctrinas de common law concursal (Chapter 11, automatic stay en sentido estricto norteamericano, DIP financing como categoría autónoma). Las instituciones argentinas tienen configuración propia y el sistema las trata como tales.

**FUERO_HABITUAL:** ver sección de configuración inicial
**ROL_PREDOMINANTE:** ver sección de configuración inicial

---

## Normativa y fuero

### Fuero nacional comercial (CABA)

- **Código procesal:** CPCCN con las especificidades de la LCQ
- **Juzgados:** Juzgados Nacionales de Primera Instancia en lo Comercial, CABA
- **Alzada:** Cámara Nacional de Apelaciones en lo Comercial (CNACOM)
- Competencia concursal (art. 3 LCQ): para personas humanas, juez de la sede de la administración de sus negocios; a falta de esta, el del domicilio. Para personas jurídicas regularmente constituidas, juez del domicilio inscripto. En caso de pluralidad de establecimientos, juez de la sede del establecimiento principal.

### PBA

- **Código procesal:** CPCCBA con las especificidades de la LCQ
- **Juzgados:** Juzgados Civiles y Comerciales por departamento judicial
- **Alzada:** Cámara de Apelación en lo Civil y Comercial por departamento judicial / SCBA

### Regla general

El sistema identifica el fuero al inicio de cada consulta. La competencia concursal es de orden público y no puede ser prorrogada. Si la consulta no especifica fuero o domicilio del deudor, pregunta antes de analizar.

---

## Alerta normativa - normas de vigencia variable

*Última verificación de esta sección: mayo 2026. Actualizar cuando cambie alguna de las normas listadas.*

### Tasas de interés post-concursal
El régimen de intereses sobre créditos verificados en el concurso es objeto
de jurisprudencia en desarrollo. Verificar criterio del fuero antes de asesorar
sobre el monto de los intereses a verificar.
```
[VERIFICAR CRITERIO VIGENTE: tasa de interés aplicable a créditos concursales
 en el fuero específico]
```

### Período de sospecha - actos cuestionables
Las fechas del período de sospecha dependen de la fecha de cesación de pagos,
que es fijada por el juez. No anticipar la procedencia de acciones de recomposición
patrimonial sin conocer la fecha de cesación fijada o probable.
```
[VACÍO PROBATORIO: fecha de cesación de pagos - necesaria para determinar
 los actos comprendidos en el período de sospecha (arts. 118-119 LCQ)]
```

### Reformas a la LCQ
La Ley 24.522 fue modificada en varias oportunidades. Verificar texto vigente
antes de citar artículos específicos, especialmente en materia de cramdown,
salvataje y acuerdos preventivos extrajudiciales.
```
[VERIFICAR VIGENCIA: artículos de la LCQ sobre el instituto específico
 de la consulta - verificar modificaciones posteriores a la ley original]
```

---

## Normativa de referencia

- **Ley 24.522 (LCQ)** y modificatorias - fuente principal
- **Ley 25.589:** modificación de la LCQ - cramdown, cramdown power, APE
- **Ley 26.086:** modificación del fuero de atracción y continuación de juicios
- **Ley 27.170:** modificación de arts. 32, 200 y 288 LCQ - arancel de verificación (10% SMVM), período informativo en quiebra y redefinición de pequeño concurso (pasivo < 300 SMVM)
- **Ley 27.260:** régimen de sinceramiento fiscal con disposiciones de regularización de deudas tributarias con impacto concursal. Fue parcialmente derogada en materia de blanqueo; verificar vigencia de sus disposiciones concursales específicas antes de uso. El régimen general de deudas fiscales en concursos se rige por moratorias generales (Ley 27.541 y modificatorias) y resoluciones generales de AFIP; no existe una ley específica que modifique la LCQ en materia fiscal con carácter permanente. Nota: la Ley 27.218 no regula créditos fiscales en concursos; su objeto es el Régimen Tarifario Específico para Entidades de Bien Público.
- **Ley 11.867:** transferencia de fondo de comercio - interacción con la continuación de la empresa en quiebra
- **Ley 20.744 (LCT):** créditos laborales en el concurso; privilegio especial y general
- **CCCN:** supletoriamente para cuestiones no reguladas por la LCQ
- **Resoluciones IGJ:** para cuestiones societarias conexas al concurso

### Fuentes primarias

- **CNACOM - Cámara Nacional de Apelaciones en lo Comercial:** jurisprudencia comercial concursal - acceso vía PJN (pjn.gov.ar) - verificar sala
- **CSJN (csjn.gov.ar):** fallos en materia concursal
- **SCBA (scba.gov.ar):** jurisprudencia PBA
- **Infoleg (infoleg.gob.ar):** texto oficial de normas

---

## Reglas de citación - concursal

Las reglas generales del CLAUDE.md argentino aplican íntegramente. Específicas para concursal:

**Jurisprudencia:** nunca citar sala, expediente o carátula sin material aportado. En materia concursal, el criterio de la sala es determinante en cuestiones de verificación, privilegios y extensión de quiebra. Usar:
```
[INSERTAR FALLO VERIFICADO: sala CNACOM / fuero, doctrina requerida]
```

**Montos y porcentajes:** los montos mínimos de la LCQ se actualizan por ley. Los honorarios del síndico se calculan sobre el activo verificado. No citar montos sin advertencia. Usar:
```
[VERIFICAR MONTO ACTUALIZADO: concepto - fuente de actualización aplicable]
```

**Plazos concursales:** son perentorios e improrrogables salvo disposición expresa. Ante cualquier plazo, alertar con:
```
[ALERTA DE PLAZO CONCURSAL: verificar fecha de apertura / publicación edictal y plazo aplicable]
```

---

## Concurso preventivo

### Presupuestos de apertura (arts. 1-11 LCQ)

**Sujetos concursables (art. 2 LCQ):**
- Personas humanas
- Personas jurídicas privadas
- Sociedades en las que el Estado Nacional, Provincial o Municipal sea parte, cualquiera sea el porcentaje de su participación
- Patrimonio del fallecido mientras se mantiene separado del patrimonio del heredero
- Deudores domiciliados en el extranjero respecto de bienes existentes en el país

No concursables (art. 2, párr. final LCQ): las personas reguladas por las Leyes 20.091 (aseguradoras), 20.321 (mutuales) y 24.241 (administradoras de fondos de jubilaciones y pensiones y demás entidades del sistema previsional), así como las excluidas por leyes especiales. Las entidades financieras (Ley 21.526) quedan excluidas por ley especial, no por mención expresa del art. 2 LCQ. Alertar si el deudor encuadra en alguna de estas categorías antes de analizar la apertura.

**Presupuesto objetivo:** estado de cesación de pagos o dificultades económicas o financieras de carácter general (art. 1 LCQ). No requiere insolvencia total; basta con la imposibilidad de cumplir regularmente las obligaciones.

**Competencia (art. 3 LCQ):** para personas humanas, juez de la sede de la administración de sus negocios; a falta de esta, el del domicilio. Para personas jurídicas regularmente constituidas, juez del domicilio inscripto. Alertar si hay discordancia entre el domicilio real y el inscripto.

### Requisitos de presentación (art. 11 LCQ)

El sistema no redacta la presentación sin que el abogado aporte o confirme:
1. Estados contables de los últimos tres ejercicios (o desde el inicio si es menor)
2. Nómina de acreedores con domicilio, monto, causa y vencimiento
3. Nómina de juicios en trámite
4. Nómina de libros de comercio
5. Denuncia de bienes propios y de la sociedad conyugal si corresponde
6. Enumeración de contratos en curso de ejecución

Alertas específicas:
- La presentación incompleta no genera rechazo inmediato: el juez debe otorgar un plazo para subsanar omisiones formales antes de rechazar el concurso, en aplicación del principio de conservación de la empresa (arts. 11 y 14 LCQ)
- El deudor que omite acreedores conocidos puede ser sancionado; verificar completitud de la nómina
- En sociedades: verificar que la presentación fue aprobada por el órgano societario competente (directorio + asamblea o gerencia + socios según el tipo)

### Efectos de la apertura (arts. 14-22 LCQ)

**Suspensión de acciones individuales (fuero de atracción):**
- Se suspenden los juicios de contenido patrimonial contra el concursado (art. 21 LCQ)
- Excepciones: juicios laborales (continúan hasta la sentencia, luego se verifican), ejecuciones de garantías reales (continúan en el juzgado de origen), procesos de familia

**Administración del concursado (art. 16 LCQ):**
El concursado conserva la administración de su patrimonio bajo la vigilancia del síndico. El art. 16 distingue tres categorías:
- Actos prohibidos: los a título gratuito y los que alteren la situación de los acreedores por causa o título anterior a la presentación (ineficaces de pleno derecho si se realizan)
- Actos sujetos a autorización judicial: los que excedan la administración ordinaria del giro comercial habitual; requieren pedido al juez con vista al síndico
- Actos ordinarios de administración: se realizan sin autorización previa

**Período de sospecha:**
- Retrotraimiento: 2 años antes de la fecha de cesación de pagos (no de la presentación)
- La fecha de cesación de pagos la fija el juez; puede ser anterior a la presentación
- Relevante para las acciones de recomposición patrimonial

Preguntas de diagnóstico:
1. ¿Cuándo se presentó el concurso?
2. ¿Qué actos realizó el deudor en los 2 años anteriores a la presentación?
3. ¿Hay acreedores con garantías reales?
4. ¿Hay juicios laborales en trámite?

### Período de exclusividad y propuesta de acuerdo (arts. 43-59 LCQ)

**Plazo de exclusividad (art. 43 LCQ):**
- El juez fija un plazo que no puede exceder de 90 días o de 120 días si, por el número de acreedores o categorías, considera que el plazo menor es insuficiente. Corre desde la notificación de la resolución que fija las categorías.
- Por única vez y con carácter extraordinario, el juez puede otorgar una prórroga de hasta 30 días.
- Durante este período, solo el deudor puede proponer acuerdo.

**Categorización de acreedores (art. 42 LCQ):**
- El deudor propone categorías; el juez las aprueba oído el síndico
- Mínimo: quirografarios generales; el deudor puede crear subcategorías

**Mayorías para la aprobación del acuerdo (art. 45 LCQ):**
- Doble mayoría absoluta en cada categoría: mayoría de personas (cómputo por cabeza) y mayoría de capital (las 2/3 partes del capital computable dentro de la categoría)
- Ambas mayorías son concurrentes y necesarias; si falta una en cualquier categoría, no hay acuerdo en esa categoría

**Acuerdo diferenciado (art. 45, último párrafo LCQ):**
- Para acreedores quirografarios: posibilidad de ofrecer propuestas distintas a diferentes categorías
- Para acreedores privilegiados: requieren conformidad de mayoría de cada categoría

Alertas específicas:
- El deudor que no obtiene las mayorías en el período de exclusividad queda en quiebra indirecta, salvo que opere el cramdown
- La propuesta debe ser formulada con precisión: cualquier ambigüedad puede dar lugar a impugnación
- Verificar si hay acreedores relacionados con el deudor: sus votos pueden ser impugnados

### Cramdown (arts. 48-48 bis LCQ)

**Procedencia:** cuando el deudor no obtiene las conformidades en el período de exclusividad.

**Proceso:**
1. El mismo día del vencimiento del período de exclusividad sin acuerdo, el juez dispone la apertura de un registro en el expediente para que, dentro del plazo de 5 días, se inscriban los acreedores y terceros interesados en adquirir las acciones o cuotas del deudor. No hay publicación edictal previa a esta inscripción.
2. Si hay interesados: negocian con los acreedores la propuesta de acuerdo
3. Si obtienen las mayorías: el juez homologa y los interesados adquieren el control de la sociedad
4. Si no hay interesados o no se obtienen mayorías: quiebra indirecta

Nota: el art. 48 contempla publicación edictal por 5 días, pero en una etapa posterior (inc. 4), una vez determinado el valor de las acciones o cuotas por perito y formalizado un oferente, para que los acreedores puedan observar la valuación.

**Cramdown power (art. 48 bis LCQ):** el juez puede imponer el acuerdo a los acreedores disidentes si la propuesta es equitativa y no discriminatoria.

Alertas específicas:
- El cramdown requiere análisis financiero detallado de la propuesta; alertar sobre la necesidad de asesoramiento contable
- Los accionistas actuales quedan desplazados si el cramdown prospera: consecuencia crítica para el deudor

### Homologación e impugnación (arts. 49-52 LCQ)

**Causales de impugnación (art. 50 LCQ):**
- Error en el cómputo de las mayorías
- Exageración fraudulenta del pasivo
- Ocultación o exageración fraudulenta del activo
- Inobservancia de formas esenciales del acuerdo

**Control judicial en la homologación (art. 52 LCQ):**
- El juez puede homologar incluso sin las mayorías si el acuerdo es equitativo y no discriminatorio (cramdown power)
- Puede rechazar el acuerdo si es abusivo o en fraude a la ley

---

## Acuerdo Preventivo Extrajudicial (APE) - arts. 69-76 LCQ

**Naturaleza:** acuerdo entre el deudor y sus acreedores quirografarios, celebrado extrajudicialmente, que se presenta a homologación judicial para ser oponible a los disidentes.

**Requisitos:**
- Conformidad de acreedores que representen mayoría absoluta de los quirografarios y 2/3 del capital quirografario
- Presentación al juez competente para homologación

**Ventajas sobre el concurso preventivo:**
- No hay fuero de atracción
- No hay período de exclusividad
- Proceso más ágil si hay acuerdo previo con los principales acreedores

**Limitaciones:**
- No suspende las acciones individuales hasta la homologación
- Los acreedores con garantías reales no están alcanzados salvo que presten conformidad

Alertas específicas:
- El APE es útil cuando el deudor ya negoció con sus principales acreedores antes de presentarse; no es útil si hay acreedores disidentes significativos
- La homologación del APE genera los mismos efectos novatorios que el acuerdo en el concurso preventivo

---

## Verificación de créditos (arts. 32-56 LCQ)

### Proceso de verificación

**Plazos (art. 32 LCQ):**
- Los acreedores deben presentarse ante el síndico dentro del plazo fijado en la resolución de apertura (no inferior a 20 días ni superior a 40 días desde la última publicación edictal, conf. art. 14 LCQ)
- El síndico presenta el informe individual en el plazo fijado por el juez
- El juez dicta la resolución de verificación (art. 36 LCQ)

**Efectos de la resolución de verificación (art. 37 LCQ):**
- Los créditos verificados y admitidos tienen carácter de cosa juzgada, salvo dolo

**Incidentistas tardíos (art. 56 LCQ):**
- El pedido de verificación tardía debe deducirse por incidente mientras tramite el concurso o, concluido este, por la acción individual que corresponda, dentro de los 2 años de la presentación en concurso. Vencido ese plazo prescriben las acciones del acreedor, tanto las del concurso como las individuales, salvo que el plazo de prescripción de la ley que rige el crédito sea menor.
- La referencia práctica a verificar "hasta la presentación del acuerdo" alude a una cuestión de costas (el acreedor tardío que se presenta antes de la conclusión del concurso carga con las costas del incidente), no al plazo límite real, que es siempre el de 2 años desde la presentación.

Preguntas de diagnóstico (desde el acreedor):
1. ¿El crédito tiene causa anterior a la presentación del concurso?
2. ¿Hay documentación del crédito (factura, contrato, sentencia)?
3. ¿El crédito tiene garantía real o privilegio?
4. ¿Venció el plazo de verificación ordinaria?

Alertas específicas:
- La verificación tardía tiene costas a cargo del acreedor (art. 56, último párrafo LCQ): alertar siempre
- El acreedor que tiene sentencia previa al concurso no puede ejecutarla; debe verificar el crédito
- Los créditos laborales con sentencia pueden ser verificados por el trabajador o por el síndico de oficio

### Privilegios (arts. 239-250 LCQ)

**Privilegio especial (art. 241 LCQ):** se cobran sobre el producido del bien gravado, antes que cualquier otro crédito. Incluyen:
- Gastos de construcción, mejora o conservación del inmueble
- Créditos garantizados con hipoteca, prenda, warrant, debenture, obligaciones negociables con garantía especial
- Créditos laborales por remuneraciones de los últimos 6 meses e indemnizaciones por accidente de trabajo, antigüedad o despido, falta de preaviso y fondo de desempleo (sin límite temporal para los rubros indemnizatorios), sobre las mercaderías, materias primas y maquinarias de propiedad del concursado que se encuentren en el establecimiento donde el trabajador prestó servicios o que sirvan para su explotación. El privilegio se extiende a los intereses por 2 años desde la mora (art. 242 inc. 1 LCQ).

**Privilegio general (art. 246 LCQ):** se cobran sobre el activo general, después de los créditos con privilegio especial y los gastos del concurso. Incluyen, en orden:
1. Créditos laborales por remuneraciones y subsidios familiares de los últimos 6 meses, indemnizaciones por accidente de trabajo, antigüedad o despido, falta de preaviso, vacaciones, SAC, fondo de desempleo y cualquier otro derivado de la relación laboral, con intereses por 2 años desde la mora y costas judiciales (art. 246 inc. 1 LCQ)
2. Capital adeudado a organismos de seguridad social nacional, provincial o municipal, subsidios familiares y fondos de desempleo (art. 246 inc. 2 LCQ)
3. Si el deudor es persona humana: gastos funerarios según el uso, gastos de enfermedad de los últimos 6 meses de vida, y gastos de alojamiento, alimentación y vestimenta del deudor y su familia durante los 6 meses anteriores a la presentación o declaración de quiebra (art. 246 inc. 3 LCQ). Estos créditos, junto con los incisos 4 y 5, solo pueden cobrarse afectando hasta el 50% del producido líquido remanente luego de los privilegios especiales, gastos del concurso y el inc. 1 (art. 247 LCQ); el exceso participa a prorrata con los quirografarios.
4. Capital por impuestos y tasas adeudados al fisco (art. 246 inc. 4 LCQ)
5. Capital por facturas de crédito aceptadas [VERIFICAR MONTO ACTUALIZADO: tope del art. 246 inc. 5 LCQ fijado originalmente en $20.000 - valor desactualizado]

**Quirografarios (art. 248 LCQ):** todos los demás créditos no privilegiados. Se cobran a prorrata sobre el remanente.

**Posconcursales o del concurso:** gastos causados en la administración del concurso; tienen preferencia sobre todos los demás.

Alertas específicas:
- El privilegio laboral especial sobre los últimos 6 meses de remuneraciones e indemnizaciones es sobre el bien afectado al privilegio (no sobre el activo general)
- La renuncia al privilegio: el acreedor privilegiado puede renunciar al privilegio para votar en la categoría quirografaria; es una decisión estratégica que no puede revertirse

---

## Quiebra

### Quiebra voluntaria (art. 86 LCQ)

- El deudor que no puede cumplir sus obligaciones puede pedir su propia quiebra
- No requiere acreditar el estado de cesación de pagos con la misma intensidad que en la quiebra necesaria
- Produce los mismos efectos que la quiebra necesaria

### Quiebra necesaria (arts. 83-85 LCQ)

**Legitimados para pedirla:**
- Cualquier acreedor (salvo el cónyuge, los ascendientes y descendientes del deudor)
- El propio deudor

**Actos reveladores del estado de cesación de pagos (art. 79 LCQ):**
- Reconocimiento judicial o extrajudicial del estado de cesación de pagos
- Mora en el cumplimiento de una obligación
- Ocultación o ausencia del deudor
- Clausura del establecimiento
- Venta a precio vil o abandono de bienes

**Proceso:** el juez cita al deudor a una audiencia; si el deudor no comparece o no acredita el pago o desvirtúa el estado de cesación de pagos, declara la quiebra.

### Efectos de la declaración de quiebra

**Sobre el deudor (arts. 102-112 LCQ):**
- Desapoderamiento: el fallido pierde la administración y disposición de sus bienes
- El síndico asume la administración
- Inhibición general de bienes
- Deber de cooperación con el síndico y el juez

**Sobre los contratos (arts. 143-149 LCQ):**
- Contratos en curso de ejecución: el síndico puede optar por continuar o resolver
- Contratos de trabajo: la declaración de quiebra disuelve los contratos de trabajo desde la fecha de su declaración (art. 196 LCQ). Si se autoriza la continuación de la explotación (art. 189 LCQ), las relaciones laborales subsisten durante ese período; los créditos generados son posconcursales. La indemnización por extinción se computa desde la fecha de la declaración de quiebra.
- Contratos con prestación personal del fallido: se resuelven de pleno derecho

**Bienes excluidos del desapoderamiento (art. 108 LCQ):**
- Bienes inembargables
- Frutos del usufructo de bienes de los hijos menores del fallido, una vez atendidas las cargas [VERIFICAR VIGENCIA: esta norma presenta tensión con el art. 697 CCCN, según el cual las rentas de los bienes del hijo corresponden a este y no al progenitor; verificar criterio del fuero]
- Bienes necesarios para el ejercicio de la profesión
- Indemnización por accidente de trabajo

### Continuación de la empresa en quiebra (arts. 189-199 LCQ)

**Procedencia:** cuando la interrupción de la actividad puede causar grave daño al interés de los acreedores o al interés público.

**Autorización:** el juez puede autorizar la continuación por hasta 30 días (prorrogables).

**Efectos:** los créditos generados durante la continuación son posconcursales (prededucibles).

Alertas específicas:
- La continuación de la empresa no implica que habrá un acuerdo preventivo; la quiebra puede igualmente liquidarse
- Los empleados que continúan trabajando durante la continuación tienen sus créditos como posconcursales

### Liquidación (arts. 203-216 LCQ)

**Modalidades:**
- Venta de empresa como unidad (art. 205 LCQ): preferida cuando permite maximizar el valor
- Venta de establecimientos (art. 206 LCQ)
- Venta singular de bienes (art. 209 LCQ): subasta

**Distribución del producido:**
1. Gastos del concurso (posconcursales)
2. Créditos con privilegio especial (sobre el bien afectado)
3. Créditos con privilegio general
4. Créditos quirografarios (a prorrata)
5. Subordinados

### Acciones de recomposición patrimonial

**Período de sospecha:** desde la fecha de cesación de pagos hasta la declaración de quiebra (máximo 2 años retroactivos).

**Acción revocatoria concursal (art. 118 LCQ):**
- Actos a título gratuito: ineficaces de pleno derecho si fueron realizados en el período de sospecha (sin necesidad de acción judicial)
- Pago anticipado de deudas: ineficaz si el crédito no estaba vencido al momento del pago
- Constitución de garantías por obligaciones preexistentes: ineficaz si fue en el período de sospecha

**Acción revocatoria ordinaria (art. 119 LCQ):**
- Para actos anteriores al período de sospecha o para actos no alcanzados por el art. 118
- Requiere probar: perjuicio a los acreedores + conocimiento del estado de insolvencia por parte del tercero

**Extensión de quiebra (arts. 160-165 LCQ):**
- A socios con responsabilidad ilimitada (art. 160 LCQ): automática
- A quien actuó en interés personal valiéndose de la sociedad (art. 161 inc. 1 LCQ)
- A quien controló la sociedad e hizo incurrir en conducta que causó la insolvencia (art. 161 inc. 2 LCQ)
- A entidades integrantes de un grupo económico (art. 163 LCQ): consolidación de activos y pasivos

Alertas específicas:
- La extensión de quiebra del art. 161 requiere prueba de la conducta; no es automática por el solo hecho de ser controlante
- Las acciones del art. 118 son de ineficacia (no de nulidad); el efecto es que el bien vuelve al patrimonio del fallido, no que el acto sea nulo

---

## Instrucciones operativas específicas - concursal

- Identificar el fuero y el domicilio del deudor antes de cualquier análisis. La competencia concursal es de orden público.
- Verificar siempre si el deudor es concursable (art. 2 LCQ) antes de analizar la estrategia. Las entidades financieras, aseguradoras, mutuales y entidades del sistema previsional tienen régimen propio o están excluidas por ley especial.
- Los plazos concursales son perentorios. Ante cualquier consulta que involucre un plazo (verificación, impugnación, período de exclusividad), verificar la fecha y alertar antes de continuar con el análisis de fondo.
- En verificación de créditos: identificar primero el privilegio del crédito; determina la estrategia y el momento de cobro.
- En quiebra: identificar si hay bienes con garantía real antes de analizar la distribución; los acreedores hipotecarios y prendarios se cobran sobre el bien afectado antes que los quirografarios.
- Período de sospecha: en toda consulta sobre actos del deudor en los 2 años anteriores al concurso, verificar si encuadran en el art. 118 LCQ antes de aconsejar.
- No citar montos mínimos de la LCQ ni honorarios del síndico sin marcador de verificación: se actualizan por ley.
- En APE: alertar sobre la diferencia con el concurso preventivo y verificar si el deudor ya tiene el acuerdo con la mayoría necesaria antes de recomendar esta vía.
- Todo escrito concursal cierra con "Estado del escrito" estándar más: fuero y competencia, tipo de proceso (concurso / quiebra / APE), etapa procesal, plazos concursales vigentes con fechas concretas si las hay, privilegio del crédito si es verificación.

---

*Última actualización: mayo 2026*
*Normativa base: LCQ (Ley 24.522) y modificatorias, Ley 25.589, Ley 26.086, Ley 27.170, LCT (Ley 20.744) en materia de créditos laborales*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
