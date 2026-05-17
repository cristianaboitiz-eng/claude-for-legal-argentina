# CHANGELOG · claude-for-legal Argentina

> Historial de cambios del repositorio.
> Formato: fecha · archivo(s) afectado(s) · descripción del cambio · motivo.
> Las entradas más recientes van primero.
>
> Cuándo actualizar este archivo:
> - Cambio de norma listada en una sección "## Alerta normativa"
> - Modificación de un marcador o de una regla operativa
> - Agregado o eliminación de un archivo del repositorio
> - Corrección de un error normativo
> - Incorporación de un nuevo perfil de área o archivo de ejemplos
>
> Cuándo NO es necesario actualizar:
> - Correcciones tipográficas menores sin impacto en comportamiento del sistema
> - Actualizaciones de estilo sin cambio de contenido normativo

---

## Instrucción de urgencia

Cuando cambia una norma que afecta a múltiples consultas diarias (un tope indemnizatorio,
una tasa de interés, un umbral de punibilidad), actualizar primero la sección
`## Alerta normativa` del perfil afectado y registrar el cambio aquí.
No esperar a la revisión periódica.

---

## 2026

### Mayo 2026 - Sincronización README con fuentes.md (Etapa 9)

**Archivos modificados:**
- `argentina/README.md` - sección "Fuentes normativas (fase 2)" reescrita para reflejar el estado actual de `fuentes.md`: tabla de conectores expandida de 4 a 6 entradas (agregados FalloBot como conector 5 y SCBA/JUBA como conector 6); agregada tabla de decisión rápida por necesidad; agregada tabla de fuentes primarias sin conector MCP (InfoLEG, normas.gba.gob.ar, SAIJ, PJN, CNACAF, SCBA, JUBA, PTN, AAIP, IGJ, DPPJ, TFN, BCRA); párrafo de cierre actualizado con referencia a `fuentes.md` para instrucciones completas

**Normas afectadas:** ninguna. Cambio de documentación.

**Impacto en conectores:** ninguno. El cambio es de visibilidad: FalloBot y normas.gba.gob.ar ya estaban en `fuentes.md`; ahora también figuran en el README.

---

### Mayo 2026 - Actualización de fuentes y conectores (Etapa 8)

**Archivos modificados:**
- `argentina/fuentes.md` - agregado conector 5 (FalloBot, `https://api.fallobot.com/mcp`): conector MCP disponible con cobertura simultánea de CSJN, SAIJ, JUBA y SCBA en tiempo real; requiere plan Pro; tabla de decisión actualizada para incluirlo como opción principal para jurisprudencia CSJN y PBA; actualizada la entrada SCBA con nota sobre expansión de cobertura JUBA (Acuerdo 4011 / Resolución RP 1651/24: Cámaras PBA desde marzo 2025, primera instancia desde junio 2025); agregado `normas.gba.gob.ar` en tabla de fuentes primarias como equivalente bonaerense de InfoLEG para normativa provincial PBA (leyes, decretos, códigos provinciales - sin API pública, acceso por fallback manual; aclaración: "Malvinas Argentinas" es el nombre del sistema, no la jurisdicción; la fuente es del Gobierno de la Provincia de Buenos Aires); agregado JUBA como entrada independiente en la tabla de fuentes primarias; numeración de conectores actualizada (SCBA pasa a ser conector 6)

**Normas afectadas:** ninguna. Los cambios son de conectores y fuentes de referencia.

**Impacto en conectores:**
- FalloBot: nuevo conector disponible (plan Pro) - cubre CSJN y PBA que antes no tenían conector MCP
- normas.gba.gob.ar: nueva fuente primaria de fallback para normativa provincial PBA
- SCBA/JUBA: cobertura ampliada a partir de 2025 por el Acuerdo 4011

---

### Mayo 2026 - Correcciones segunda auditoría (Etapa 6)

**Archivos modificados:**
- `argentina/ejemplos-civil.md` - marcador `[VERIFICAR CRITERIO VIGENTE DE LA SALA]` reemplazado por `[VERIFICAR CRITERIO DEL FUERO: ratio daño punitivo art. 52 bis LDC - sala actuante]`
- `argentina/ejemplos-laboral.md` - marcador `[VERIFICAR FÓRMULA VIGENTE]` reemplazado por `[VERIFICAR CRITERIO DEL FUERO: fórmula de cuantificación LRT vigente - resolución SRT y jurisprudencia aplicable]`
- `argentina/ejemplos-societario.md` - marcador `[VERIFICAR]` (forma corta) reemplazado por `[VERIFICAR RESOLUCIÓN REGISTRAL VIGENTE: IGJ/DPPJ - parámetros de activación de sindicatura obligatoria]`
- `argentina/tributario-CLAUDE.md` - marcador `[VERIFICAR MONTO ACTUALIZADO]` sin detalle completado: `[VERIFICAR MONTO ACTUALIZADO: multa art. 39 LPT - RG AFIP vigente]`
- `argentina/penal-CLAUDE.md` - instrucción de plazo fatal en instrucciones operativas: agregada referencia explícita al marcador A10 `[ALERTA PLAZO FATAL]` para prescripción de la acción y de la pena
- `argentina/laboral-CLAUDE.md` - instrucción de prescripción en instrucciones operativas: agregada referencia explícita al marcador A10 con ejemplo concreto art. 258 LCT
- `argentina/CLAUDE.md` - tabla de routing: agregada fila `contratos-CLAUDE.md` + `red-flags-contratos.md`; eliminada fila redundante de `red-flags-contratos.md` solo
- `argentina/diagnostico-SKILL.md` - sección 7 "Normas con verificación pendiente": agregada instrucción de emitir `[ALERTA PLAZO FATAL]` cuando el escrito involucra acción sujeta a plazo fatal, con cuatro ejemplos de uso
- `argentina/setup-output-TEMPLATE.md` - sección final: agregada nota con ejemplo de CLAUDE.md personalizado que incluye configuración administrativa

**Normas afectadas:** ninguna. Los cambios son de marcadores y referencias cruzadas.

**Impacto en marcadores:**
- `[VERIFICAR CRITERIO VIGENTE DE LA SALA]`: eliminado del repo; forma no canónica confirmada en tabla de equivalencias del glosario
- `[VERIFICAR FÓRMULA VIGENTE]`: ídem
- `[VERIFICAR]` (forma corta): ídem

---

### Mayo 2026 - Mejoras post-análisis: administrativo y glosario (Etapa 5)

**Archivos modificados:**
- `argentina/administrativo-CLAUDE.md` - sección "Configuración inicial" reescrita: variables `FUERO_HABITUAL` y `AREAS_PRACTICA_ADMINISTRATIVO` ahora usan marcador `[PENDIENTE]` con instrucción explícita y ejemplo, en lugar de texto libre sin valor asignado; marcador no canónico `[ALERTA DE PLAZO]` reemplazado por `[ALERTA PLAZO FATAL]` en sección de reglas de citación, alerta normativa e instrucciones operativas; sección "Identidad y alcance" restaurada como sección independiente
- `argentina/marcadores-GLOSARIO.md` - agregado marcador A10 `[ALERTA PLAZO FATAL]` con sintaxis, cuatro ejemplos de uso (administrativo, amparo federal, prescripción LCT, responsabilidad del Estado) y regla de uso negativa; tabla de equivalencias: agregada entrada `[ALERTA DE PLAZO]` → `[ALERTA PLAZO FATAL]`; versión actualizada a 1.1
- `argentina/CHANGELOG.md` - agregadas dos filas en tabla de normas de alta volatilidad: Decreto 1030/16 + resoluciones ONC (administrativo) y Ley 12.008 PBA (administrativo)
- `argentina/setup-interview.md` - agregado Bloque 2-bis de configuración administrativa (P5-bis a P7-bis): fuero habitual, áreas dentro de administrativo, y rol predominante (actor/demandado)
- `argentina/setup-output-TEMPLATE.md` - agregada variable `[FUERO_ADMINISTRATIVO]`, `[AREAS_ADMINISTRATIVO]` y `[ROL_ADMINISTRATIVO]` en tabla de variables; agregada sección "Configuración administrativa" en el template (análoga a la laboral y societaria); agregado ejemplo en el output mínimo
- `argentina/fuentes.md` - agregadas dos entradas en tabla de fuentes primarias oficiales: CNACAF (`cnacaf.gov.ar`) y PTN (`ptn.gov.ar`)

**Normas afectadas:** ninguna. Los cambios son de estructura, marcadores y referencias cruzadas.

**Impacto en marcadores:**
- `[ALERTA DE PLAZO]`: eliminado del repo; reemplazar por `[ALERTA PLAZO FATAL: norma - plazo - fecha de inicio del cómputo - vencimiento estimado]`
- `[ALERTA PLAZO FATAL]`: nuevo marcador canónico A10; usar en administrativo, amparo, laboral y cualquier plazo fatal

---

### Mayo 2026 - Limpieza final y sincronización (Etapa 4)

**Archivos modificados:**
- `argentina/fuentes.md` - agregada sección "Cómo verificar que un conector está activo" con instrucciones de verificación en Cowork y Claude Code, tabla de fallback por conector con URL y consecuencia, campo "Estado al mayo 2026" en cada entrada; marcador `[DISCREPANCIA ENTRE CONECTORES]` reemplazado por `[DISCREPANCIA ENTRE FUENTES]`
- `argentina/ejemplos-civil.md` - bloque de fórmulas genérico reemplazado por tabla por fuero (CNAC, civil y comercial federal, CABA local, PBA departamental, CNAT) con fórmula predominante, descripción técnica y ejemplo numérico; cuatro marcadores no canónicos corregidos
- `argentina/README.md` - referencia al repositorio base eliminada; estructura de archivos sincronizada con los 22 archivos reales; sección de instalación actualizada con referencias a `setup-output-TEMPLATE.md` y `diagnostico-casos-prueba.md`; tabla de perfiles con columna "Complementos"; referencias a "plugins" corregidas

**Normas afectadas:** ninguna. Los cambios son de estructura y documentación.

---

### Mayo 2026 - Gaps de cobertura (Etapa 3)

**Archivos nuevos:**
- `argentina/contratos-CLAUDE.md` - perfil unificado para revisión y redacción de contratos bajo derecho argentino; cubre flujo de revisión (clasificación + red-flags + análisis por tipo), flujo de redacción con preguntas de diagnóstico previo, y 7 tipos contractuales con lógica específica (servicios profesionales, SaaS, compraventa, locación, NDA, mutuo, agencia/concesión/franquicia)
- `argentina/diagnostico-casos-prueba.md` - tres casos ficticios con diagnóstico esperado completo para verificar el skill: demanda laboral por despido (9 marcadores esperados), demanda civil por mala praxis (14 marcadores), revisión de cláusulas de pacto de accionistas (10 marcadores)

**Normas afectadas:** ninguna. Los archivos nuevos aplican normativa ya incluida en los perfiles de área.

---

### Mayo 2026 - Integración interna (Etapa 2)

**Archivos modificados:**
- `argentina/CLAUDE.md` - agregados bloques "Protocolo ante alucinación normativa" y "Routing hacia perfiles de área"; estructura del repo actualizada con archivos nuevos de Etapa 1
- `argentina/civil-CLAUDE.md` - agregado bloque "Archivos complementarios"; marcadores `[VACÍO CUANTIFICATIVO]` y `[VERIFICAR CRITERIO DE LA SALA]` reemplazados por formas canónicas; fecha de verificación en alertas normativas
- `argentina/societario-CLAUDE.md` - agregado bloque "Archivos complementarios"; marcadores `[VERIFICAR RESOLUCIÓN IGJ/DPPJ VIGENTE]`, `[VACÍO DOCUMENTAL]` y `[VERIFICAR UMBRAL CNDC VIGENTE]` reemplazados; fecha de verificación en alertas normativas
- `argentina/laboral-CLAUDE.md` - agregado bloque "Archivos complementarios"; fecha de verificación en alerta DNU
- `argentina/administrativo-CLAUDE.md`, `argentina/tributario-CLAUDE.md`, `argentina/penal-CLAUDE.md`, `argentina/familia-CLAUDE.md`, `argentina/concursos-CLAUDE.md` - fecha de verificación agregada en cada sección "## Alerta normativa"

**Normas afectadas:** ninguna. Los cambios son de estructura, marcadores y referencias cruzadas.

---

### Mayo 2026 - Reorganización y estandarización inicial (Etapa 1)

**Archivos nuevos:**
- `argentina/marcadores-GLOSARIO.md` - glosario canónico con 15 formas canónicas en 4 categorías; tabla de equivalencias que mapea los 40+ marcadores anteriores a su forma canónica
- `argentina/setup-output-TEMPLATE.md` - template con variables mapeadas a cada pregunta de la entrevista, instrucciones de generación para el sistema, y ejemplo de output completo
- `argentina/CHANGELOG.md` - este archivo; incluye tabla de normas de alta volatilidad con fecha de última verificación

**Archivos modificados:**
- `argentina/setup-interview.md` - agregada referencia a `setup-output-TEMPLATE.md` en el flujo de output
- `argentina/CLAUDE.md` - agregada referencia al glosario de marcadores

**Motivo:** estandarización de marcadores (existían más de 40 variantes equivalentes distribuidas entre archivos); formalización del output de la entrevista; trazabilidad de cambios normativos.

**Normas afectadas:** ninguna. Los cambios son de forma, no de contenido normativo.

---

## Plantilla de entrada

Copiar y completar para cada cambio:

```
### [Mes Año]

**Archivos afectados:**
- `ruta/archivo.md` - sección afectada

**Cambio:**
[descripción del cambio]

**Motivo:**
[norma modificada / error detectado / nueva funcionalidad]

**Normas vigentes actualizadas:**
- [norma]: [cambio concreto]

**Impacto en marcadores:**
- [marcador afectado]: [cambio en comportamiento]

**Fuente:**
- [URL o referencia de la norma que motivó el cambio]
```

---

## Normas de alta volatilidad · estado al momento de la última revisión

Esta tabla recoge las normas con mayor frecuencia de cambio. Verificar antes de aconsejar.
Actualizar la columna "Última verificación" cuando se confirme la vigencia.

| Norma | Área | Dato volátil | Última verificación |
|---|---|---|---|
| Art. 245 LCT - tope indemnizatorio | Laboral | Monto del tope por CCT | Mayo 2026 - verificar por CCT |
| Acta CNAT - tasa de interés | Laboral | Tasa y fecha de vigencia | Mayo 2026 - verificar acta vigente |
| Resolución SRT - prestaciones LRT | Laboral / LRT | Montos de prestaciones | Mayo 2026 - verificar RG vigente |
| DNU 70/2023 - modificaciones LCT | Laboral | Estado judicial de cada modificación | Mayo 2026 - algunas suspendidas, verificar |
| Ley 27.430 art. 1 - umbral penal tributario | Tributario | Monto de punibilidad | Mayo 2026 - verificar si fue actualizado |
| Monto mínimo recurso TFN | Tributario | Monto habilitante | Mayo 2026 - verificar norma vigente |
| Capital mínimo IGJ/DPPJ | Societario | Monto actualizado por resolución | Mayo 2026 - verificar resolución vigente |
| Sindicatura obligatoria SA - parámetros | Societario | Parámetros de activación | Mayo 2026 - verificar resolución IGJ/DPPJ |
| Régimen cambiario BCRA | Contratos / M&A | Restricciones al giro de divisas | Mayo 2026 - verificar comunicaciones BCRA |
| Decreto 1030/16 + resoluciones ONC | Administrativo | Umbrales, procedimientos y formularios de contratación pública | Mayo 2026 - verificar ONC antes de asesorar |
| Ley 12.008 PBA - plazos CCA | Administrativo | Plazos de caducidad contencioso administrativo PBA | Mayo 2026 - verificar norma y jurisprudencia SCBA |
| Ley 27.551 - locaciones urbanas | Familia / Civil | Modalidad de actualización del alquiler | Mayo 2026 - verificar estado de modificaciones |
| Tasas de interés fueros civiles y comerciales | Civil / Comercial | Tasa activa BNA, variantes por sala | Mayo 2026 - verificar actas CNAC / CNACOM |
| Prestaciones alimentarias - fórmulas | Familia | Criterio por fuero | Mayo 2026 - verificar criterio sala actuante |

---

*Última actualización: mayo 2026*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
