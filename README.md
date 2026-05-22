# claude-for-legal · Adaptación Argentina

Configuración de Claude para práctica legal argentina. El material está construido
sobre derecho argentino: CCCN, LCT, LDC, LGS, CPCCN/CPCCBA, y normas especiales.
No requiere ningún repositorio externo para funcionar; puede usarse de forma
autónoma desde Claude.ai Projects o Claude Code.

---

## Estructura

```
argentina/
  CLAUDE.md                         # Perfil general - cargar en todo Project
  CHANGELOG.md                      # Historial de cambios normativos y del sistema
  marcadores-GLOSARIO.md            # Glosario canónico de marcadores (fuente de verdad)
  setup-interview.md                # Entrevista de configuración inicial
  setup-output-TEMPLATE.md          # Template de output de la entrevista
  diagnostico-SKILL.md              # Skill de diagnóstico previo (transversal)
  plazos-SKILL.md                   # Skill de cómputo de plazos procesales y administrativos
  diagnostico-casos-prueba.md       # Casos de prueba para verificar el skill
  red-flags-contratos.md            # Alertas para revisión de contratos (activ. automática)
  contratos-CLAUDE.md               # Perfil unificado para revisión y redacción de contratos
  administrativo-CLAUDE.md          # Perfil derecho administrativo
  civil-CLAUDE.md                   # Perfil derecho civil (CCCN)
  concursos-CLAUDE.md               # Perfil concursos y quiebras (LCQ)
  familia-CLAUDE.md                 # Perfil derecho de familia
  laboral-CLAUDE.md                 # Perfil derecho del trabajo (LCT)
  penal-CLAUDE.md                   # Perfil derecho penal
  societario-CLAUDE.md              # Perfil derecho societario (LGS)
  tributario-CLAUDE.md              # Perfil derecho tributario
  ejemplos-civil.md                 # Casos de daños y responsabilidad civil
  ejemplos-laboral.md               # Casos de liquidación con checklist de rubros
  ejemplos-societario.md            # Due diligence y pactos de accionistas
  fuentes.md                        # Conectores MCP y fuentes primarias
  macos-automation.md               # Módulo opcional - automatización de escritorio macOS (Claude Code)
  legal.local.md.template           # Template de configuración local del estudio (por rama del derecho)
  evals/                            # Casos de control para verificar perfiles de área
    README.md                       # Formato estándar y áreas prioritarias
```

---

## Qué hace este sistema

**Opera bajo:**
- CCCN (Ley 26.994) para contratos y obligaciones
- LCT (Ley 20.744) y modificatorias para materia laboral
- Ley 25.326 y disposiciones AAIP para privacidad y datos personales
- CPCCN para fueros nacionales y federales / CPCCBA para PBA
- LDC (Ley 24.240) para contratos de consumo
- LGS para societario

**Reemplaza la lógica de common law en tres áreas críticas:**
- Contratos: análisis bajo CCCN (no bajo consideration ni indemnification caps)
- Laboral: modelo de despido con indemnización obligatoria art. 245 LCT (no at-will)
- Privacidad: habeas data bajo Ley 25.326 (no GDPR/DSAR)

**Agrega:**
- Red flags específicas del derecho argentino para revisión automática de contratos
- Glosario canónico de marcadores estandarizados para señalar vacíos e inconsistencias
- Protocolo de alucinación normativa: el sistema detiene la redacción si detecta que citó una norma sin respaldo
- Routing automático hacia perfiles de área según la rama del derecho de la consulta
- Alertas de normas inestables integradas en cada perfil con fecha de última verificación
- Casos de prueba para verificar que el skill de diagnóstico funciona correctamente
- Skill de cómputo de plazos procesales y administrativos: días hábiles judiciales y administrativos, días corridos, meses y años, con suspensiones por feria judicial, mediación prejudicial y SECLO

---

## Antes de empezar

Necesitás:
- Cuenta de Claude.ai con plan Pro o Team
- Opcionalmente: Claude Code (terminal) o Claude Cowork (escritorio) para flujos más automatizados

No necesitás saber programar para la configuración base en Claude.ai Projects.
Para conectar fuentes normativas locales (fase 2, ver `fuentes.md`), los conectores
marcados "URL directa" se agregan en segundos desde Claude.ai sin instalar nada.

---

## Instalación paso a paso

> Esta guía asume que nunca usaste GitHub. Si ya tenés experiencia, saltá al Paso 2.

### Paso 1: Crear cuenta en GitHub (si no tenés)

1. Entrá a [github.com](https://github.com) y hacé clic en **Sign up**.
2. Completá email, contraseña y nombre de usuario. El plan gratuito es suficiente.
3. Verificá tu email.

### Paso 2: Fork del repositorio

"Fork" significa hacer una copia del repositorio en tu propia cuenta. Eso te permite personalizar el sistema sin afectar el original, y recibir las actualizaciones diarias automáticamente.

1. Entrá a [github.com/cristianaboitiz-eng/claude-for-legal-argentina](https://github.com/cristianaboitiz-eng/claude-for-legal-argentina).
2. Hacé clic en el botón **Fork** (arriba a la derecha).
3. Dejá todo como está y confirmá con **Create fork**.

Ahora tenés tu propia copia en `github.com/TU-USUARIO/claude-for-legal-argentina`.

> **No descargues el ZIP.** El fork es lo que te permite recibir actualizaciones sin pisar tu configuración.

### Paso 3: Activar actualizaciones automáticas diarias

El repositorio se actualiza todos los dias. Para que tu copia reciba esos cambios automáticamente sin que tengas que hacer nada:

1. En tu fork, hacé clic en la pestaña **Settings**.
2. En el menu izquierdo, buscá **Actions** → **General**.
3. Bajá hasta **Workflow permissions** y seleccioná **Read and write permissions**. Guardá.
4. Hacé clic en la pestaña **Actions** de tu fork.
5. Buscá el workflow **Sync upstream** y hacé clic en **Run workflow** para verificar que funciona.

A partir de ese momento, todos los dias a las 03:00 (hora Argentina) el sistema incorpora automaticamente las novedades del repositorio original.

### Paso 4: Perfil de práctica general

Abrí `argentina/CLAUDE.md` y cargá su contenido en las instrucciones del Project de Claude que vas a usar para práctica general.

**Para configuración personalizada:** corre la entrevista de `setup-interview.md`
antes de cargar el CLAUDE.md. La entrevista genera un CLAUDE.md personalizado
con tu jurisdicción, áreas de práctica, CCT habitual y preferencias de formato.
El template de output está en `setup-output-TEMPLATE.md`.

Sin configuración personalizada: el CLAUDE.md genérico funciona pero opera con
supuestos genéricos de jurisdicción y área.

**Configuración local del estudio (`legal.local.md`):** el archivo
`legal.local.md.template` contiene variables específicas del estudio organizadas
por rama del derecho: jurisdicción, fuero, departamento judicial, sistema de
gestión, CCT habitual, tasa de interés, preferencias de formato y notas libres.
Cubre civil, comercial, laboral, penal, familia, administrativo, tributario,
societario, concursal, contratos y privacidad.

Según tu flujo de trabajo, usá uno de estos dos métodos:

**Claude.ai Projects:** completá el template, guardalo como `legal.local.md`
y subilo a las instrucciones del Project junto con el `CLAUDE.md`. Se hace
una sola vez. El sistema lo lee como configuración de contexto y lo prioriza
sobre los valores genéricos del perfil.

**Claude Code:** guardá el archivo completado como `legal.local.md` en el
mismo directorio donde corrés Claude Code. El sistema lo detecta y lo lee
automáticamente en cada sesión, sin ningún paso adicional.

> No subas `legal.local.md` al repositorio. Agregalo a `.gitignore`.
> El template (`legal.local.md.template`) sí forma parte del repo.

### Paso 5: Perfiles por área

Para cada área de práctica que uses, cargá el perfil correspondiente junto con
el CLAUDE.md general en las instrucciones del Project. Cada perfil incluye
instrucciones para activar sus archivos complementarios (ejemplos, red-flags).

Los perfiles disponibles:

| Archivo | Área | Complementos | Alertas |
|---|---|---|---|
| `laboral-CLAUDE.md` | Derecho del trabajo (LCT) | `ejemplos-laboral.md` | DNU 70/2023, topes art. 245, tasas CNAT |
| `administrativo-CLAUDE.md` | Derecho administrativo | - | Plazos de caducidad, contratación pública |
| `civil-CLAUDE.md` | Derecho civil (CCCN) | `ejemplos-civil.md` | Tasas de interés, fórmulas de daños por fuero |
| `penal-CLAUDE.md` | Derecho penal | - | Umbrales penales, código procesal vigente |
| `familia-CLAUDE.md` | Derecho de familia | - | Cuotas alimentarias, régimen de alquileres |
| `societario-CLAUDE.md` | Societario y M&A | `ejemplos-societario.md` | Resoluciones IGJ/DPPJ, capital mínimo |
| `tributario-CLAUDE.md` | Derecho tributario | - | Alícuotas, MNI, umbrales de punibilidad |
| `concursos-CLAUDE.md` | Concursos y quiebras (LCQ) | - | Tasas post-concursales, reformas LCQ |
| `contratos-CLAUDE.md` | Revisión y redacción de contratos | `red-flags-contratos.md` | Régimen cambiario, locaciones, intertemporalidad |

`red-flags-contratos.md` se activa automáticamente desde el CLAUDE.md general
ante cualquier contrato aportado en sesión; no requiere cargarlo por separado
salvo que se use el perfil de contratos dedicado.

### Paso 6: Configuración del skill de diagnóstico

Cargá `diagnostico-SKILL.md` en cualquier Project donde quieras que el sistema
diagnostique escritos antes de modificarlos. Puede cargarse solo o junto con
cualquier perfil de área.

Para verificar que el skill funciona correctamente, usá `diagnostico-casos-prueba.md`:
pegá uno de los tres escritos de prueba y comparás el output del sistema con
el diagnóstico esperado documentado en el archivo.

### Paso 7: Skill de cómputo de plazos

Cargá `plazos-SKILL.md` en cualquier Project donde necesites calcular plazos procesales
o administrativos. Puede cargarse solo o junto con cualquier perfil de área; si el
CLAUDE.md personalizado tiene configurado `FUERO_HABITUAL`, el skill lo usa por defecto
sin preguntar.

El skill cubre plazos en días hábiles judiciales y administrativos, días corridos, meses
y años, con suspensiones por feria judicial, mediación prejudicial y SECLO. No calcula
plazos ante AFIP/ARCA: ante esas consultas emite `[REVISIÓN NORMATIVA REQUERIDA]`.

Interacción con perfiles de área: el skill se activa automáticamente ante consultas de
prescripción o caducidad cuando está cargado junto con `civil-CLAUDE.md`,
`laboral-CLAUDE.md` o `administrativo-CLAUDE.md`. También puede invocarse directamente
con el comando `/argentina:plazos`.

---

## Alertas de normas inestables

Cada perfil de área incluye una sección `## Alerta normativa` con las normas de mayor
volatilidad para esa materia. La sección está ubicada antes de las instrucciones operativas
de cada perfil para que el sistema la procese con prioridad.

| Perfil | Sección de alerta | Normas cubiertas |
|---|---|---|
| `laboral-CLAUDE.md` | `## Alerta normativa - Decreto 70/2023 y modificaciones posteriores` | DNU 70/2023 (período de prueba, art. 245, negociación colectiva) |
| `civil-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Tasas de interés por fuero, fórmulas de cuantificación de daños, art. 52 bis LDC |
| `administrativo-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Plazos de caducidad art. 25 LNPA, contratación pública, normativa provincial |
| `concursos-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Tasas post-concursales, período de sospecha, reformas LCQ |
| `tributario-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Ganancias/MNI, Bienes Personales, umbrales penales Ley 27.430, monto mínimo TFN |
| `familia-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Cuotas alimentarias, locaciones con destino habitacional |
| `penal-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Umbrales de punibilidad, códigos procesales en transición |
| `societario-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Resoluciones IGJ/DPPJ, capital mínimo, sindicatura |



---

## Fuentes normativas (fase 2)

Conectores de la comunidad que apuntan directamente a las fuentes oficiales argentinas:

### Conectores MCP disponibles

| # | Repositorio / Endpoint | Fuente | Función | Requisito |
|---|---|---|---|---|
| 1 | [Ansvar-Systems/argentine-law-mcp](https://github.com/Ansvar-Systems/argentine-law-mcp) | InfoLEG / SAIJ | Texto literal de normas nacionales | Gratuito |
| 2 | [voftec/normativapba-mcp](https://github.com/voftec/normativapba-mcp) · URL directa: `https://normativapba-mcp.vercel.app/api/mcp/sse` | normas.gba.gob.ar | Legislación provincial PBA: búsqueda, vigencia, articulado, árbol de dependencias normativas. Conexión directa vía URL en Claude.ai sin instalación local. Ver nota de limitación abajo. | Gratuito |
| 3 | [voftec/InfoLeg-MCP](https://github.com/voftec/InfoLeg-MCP) · URL directa: `https://infoleg-mcp.vercel.app/api/mcp/sse` | infoleg.gob.ar | Texto oficial de normas nacionales. Complementa o reemplaza el conector 1. Conexión directa vía URL en Claude.ai sin instalación local. | Gratuito |
| 4 | [voftec/juba-mcp](https://github.com/voftec/juba-mcp) · URL directa: `https://juba-mcp.vercel.app/api/mcp/sse` | JUBA / SCBA | Jurisprudencia SCBA y cámaras de apelación PBA. 21 herramientas especializadas por fuero, campo y tipo de voto. Cubre primera instancia desde junio 2025. Conexión directa vía URL en Claude.ai sin instalación local. | Gratuito |
| 5 | `claude mcp add saij-mcp -- uvx saij-mcp` | SAIJ | Jurisprudencia, legislación, doctrina y dictámenes. Más de 330.000 documentos. | Gratuito |
| 6 | `claude mcp add csjn-mcp -- uvx csjn-mcp` | CSJN | Fallos de la Corte Suprema de Justicia de la Nación | Gratuito |
| 7 | `claude mcp add juscaba-mcp -- uvx juscaba-mcp` | Poder Judicial CABA / fueros nacionales | Jurisprudencia de fueros nacionales y locales con sede en CABA | Gratuito |
| 8 | [joaquinescalante23/saij-mcp](https://github.com/joaquinescalante23/saij-mcp) | SAIJ | Investigación profunda: jurisprudencia, legislación, doctrina y dictámenes; grafo legal; OCR para PDFs históricos; resolución de citas textuales. Opera sobre API no oficial de SAIJ - verificar estado antes de usar. | Gratuito |
| 9 | [Psflores/Legal-MCP-Server-](https://github.com/Psflores/Legal-MCP-Server-) | PJN / CABA | Jurisprudencia fueros nacionales. Proyecto de la comunidad - verificar estado antes de usar. | Gratuito |
| 10 | [guidobonomini/argentina-law-mcp-server](https://github.com/guidobonomini/argentina-law-mcp-server) | Praxis local | Análisis semántico, glosario judicial argentino, detección de riesgos calibrada para praxis local | Gratuito |
| 11 | [datos-justicia-argentina/Tesauro-Saij](https://github.com/datos-justicia-argentina/Tesauro-Saij-de-Derecho-Argentino) | SAIJ | Vocabulario controlado para búsqueda jurídica | Gratuito |
| 12 | [voftec/bora-mcp](https://github.com/voftec/bora-mcp) · URL directa: `https://bora-mcp.vercel.app/api/mcp/sse` | Boletín Oficial de la República Argentina | Portada del día, sumario por fecha, texto verbatim de avisos, nuevas sociedades (2da Sección), licitaciones (3ra Sección). Conexión directa en Claude.ai sin instalación local. | Gratuito |

#### Como conectar los servidores MCP por URL en Claude.ai (sin instalacion)

Para los conectores marcados "URL directa" (2, 3, 4 y 12), el proceso es identico para todos:

1. Entrá a [claude.ai/settings/integrations](https://claude.ai/settings/integrations) o desde Claude.ai: **Settings → Integrations → Add integration**.
2. En el campo **URL** pegá la URL del conector (por ejemplo `https://juba-mcp.vercel.app/api/mcp/sse`).
3. Poné un nombre descriptivo (por ejemplo `JUBA - Jurisprudencia PBA`).
4. Guardá. El conector queda disponible en todos tus Projects.

No requiere instalar Node.js, npm ni ningun programa adicional.

#### Nota sobre el conector 2 (voftec/normativapba-mcp) - `verificar_vigencia`

La herramienta `verificar_vigencia` consulta en tiempo real los metadatos de `normas.gba.gob.ar` y reproduce su estado tal como está cargado en el portal. El portal puede contener errores en las relaciones de derogación. Caso conocido: la Ley 11.922 (CPP Bonaerense, 1997) figura en el portal como derogada por la Ley/Decreto-ley 9032 (1978), cuando la relación es inversa: la 11.922 deroga a la 9032 y está plenamente vigente con modificatorias.

Regla de uso: `verificar_vigencia` es un primer filtro, no una fuente definitiva. Ante cualquier resultado de derogación que parezca anómalo, verificar contra el Boletín Oficial PBA o el texto actualizado disponible en el propio portal. El error fue reportado al mantenedor del conector y a la Subsecretaría Legal y Técnica de PBA para corrección en la fuente.

### Tabla de decisión rápida

| Necesidad | Conector recomendado | Fallback manual |
|---|---|---|
| Texto de norma nacional | 3 (voftec/InfoLeg-MCP) o 1 (Ansvar) | infoleg.gob.ar |
| Texto de norma provincial PBA | 2 (voftec/normativapba-mcp) | normas.gba.gob.ar |
| Jurisprudencia PBA (SCBA y cámaras) | 4 (voftec/juba-mcp) | juba.scba.gov.ar |
| Jurisprudencia SAIJ (todas las instancias) | 5 (saij-mcp) | saij.gob.ar |
| Jurisprudencia CSJN | 6 (csjn-mcp) | sj.csjn.gov.ar |
| Jurisprudencia CABA / fueros nacionales | 7 (juscaba-mcp) | jusbaires.gob.ar |
| Grafo legal / navegación de citas / OCR histórico | 8 (joaquinescalante23/saij-mcp) | saij.gob.ar |
| Jurisprudencia PJN alternativa | 9 (Psflores) | pjn.gov.ar |
| Doctrina y dictámenes | 5 (saij-mcp) o 8 (joaquinescalante23) | saij.gob.ar |
| Análisis semántico / terminología | 10 (guidobonomini) | Glosario del CLAUDE.md |
| Mejora de búsquedas jurisprudenciales | 11 (Tesauro SAIJ) | saij.gob.ar |
| Texto de normas publicadas en BORA / nuevas sociedades / licitaciones | 12 (voftec/bora-mcp) | boletinoficial.gob.ar |

### Fuentes primarias sin conector MCP

Acceso directo por el abogado para verificación manual. Son la fuente de verdad ante cualquier discrepancia con un conector.

| Fuente | URL | Uso principal |
|---|---|---|
| InfoLEG | infoleg.gob.ar | Texto oficial de normas nacionales |
| normas.gba.gob.ar | normas.gba.gob.ar | Leyes, decretos, códigos y resoluciones provinciales PBA (sin API pública; acceso por búsqueda o URL directa) |
| SAIJ | saij.gob.ar | Jurisprudencia, doctrina, legislación provincial |
| PJN | pjn.gov.ar | Acordadas y jurisprudencia federal |
| CNACAF | cnacaf.gov.ar | Jurisprudencia contencioso administrativo federal y alzada tributaria |
| SCBA | scba.gov.ar | Jurisprudencia PBA - fuente primaria bonaerense |
| JUBA | juba.scba.gov.ar | Consulta de jurisprudencia PBA (SCBA + cámaras + primera instancia desde 2025) |
| Poder Judicial CABA | buenosaires.gob.ar/jusbaires | Jurisprudencia fuero local CABA |
| PTN | ptn.gov.ar | Dictámenes - responsabilidad del Estado y empleo público |
| AAIP | argentina.gob.ar/aaip | Disposiciones de datos personales |
| IGJ | igj.gob.ar | Resoluciones societarias CABA |
| DPPJ | gba.gob.ar/dppj | Resoluciones societarias PBA |
| TFN | tfnacional.gov.ar | Jurisprudencia tributaria |
| BCRA | bcra.gov.ar | Normativa cambiaria y financiera |

No son necesarios para empezar. Los perfiles funcionan solos como única configuración.
Los conectores son la segunda capa: permiten que el sistema consulte fuentes primarias
automáticamente sin que el abogado tenga que pegar el texto en la sesión. Los conectores
4 a 7 (Caravario) se instalan vía `uvx`; los conectores 2, 3 (voftec) y 12 (BORA Oficial)
tienen conexión directa por URL en Claude.ai sin instalación local. Ver `fuentes.md`
para instrucciones completas de verificación de estado, fallback y combinaciones recomendadas.

### Paso 8 (opcional): Automatización de escritorio macOS

Si usás Claude Code en Mac y tu flujo incluye portales judiciales o sistemas de gestión
de estudio sin API (PJN, MEJ, SCBA, IGJ, AFIP desktop), podés agregar `macos-use`
para automatizar esa capa:

```bash
claude mcp add macos-use -- npx -y mcp-server-macos-use
```

Requiere macOS 13+ y permiso de Accesibilidad en el terminal. Solo aplica a Claude Code;
no funciona en Claude.ai web. Proyecto de [@m13v_](https://x.com/m13v_). Ver `argentina/macos-automation.md` para casos de uso
jurídicos, requisitos y limitaciones.

---

## Lo que podés hacer desde el día uno

**Plazos procesales y administrativos:**
- Calcular plazos en días hábiles judiciales o administrativos, días corridos, meses y años
- Aplicar suspensiones por feria judicial, mediación prejudicial obligatoria y SECLO
- Verificar vencimientos de prescripción y caducidad en materia civil, laboral y administrativa
- Activación automática ante consultas de prescripción o caducidad cuando se usa junto con `civil-CLAUDE.md`, `laboral-CLAUDE.md` o `administrativo-CLAUDE.md`; también invocable directamente con `/argentina:plazos`

**Contratos:**
- Revisar contratos contra la lista de red flags argentina, con referencia a norma aplicable (CCCN, LCT, LDC)
- Redactar borradores de contratos tipo (NDA, prestación de servicios, compraventa) con CCCN como base
- Detectar cláusulas abusivas en contratos de adhesión y consumo

**Societario y M&A:**
- Preparar briefings de due diligence con checklist adaptado a LGS y normativa IGJ/DPPJ
- Armar pactos de accionistas con análisis de ejecutabilidad en Argentina
- Verificar requisitos de notificación a la CNDC en operaciones de concentración

**Laboral:**
- Calcular liquidaciones finales (art. 245 LCT + agravantes Ley 24.013 / Ley 25.323 / art. 80)
- Analizar estrategia desde el trabajador o el empleador con carga probatoria invertida
- Redactar telegramas y cartas documento laborales

**Administrativo:**
- Verificar agotamiento de la vía administrativa y plazos de caducidad (art. 25 LNPA)
- Analizar recursos administrativos y acciones contenciosas en los tres fueros (federal, CABA, PBA)

**Penal:**
- Analizar estrategia de defensa por etapa procesal y código aplicable (CPPN / CPPF / CPPCABA / CPPBA)
- Evaluar procedencia de colaboración eficaz (Ley 27.304) y proceso de flagrancia (Ley 27.272)

**Familia:**
- Armar convenios reguladores de divorcio con todos los institutos del CCCN
- Analizar alimentos, cuidado personal y régimen comunicacional con jurisprudencia del fuero

**Tributario:**
- Analizar recursos ante el TFN y la CNACAF
- Revisar compliance bajo Ley 25.326 (habeas data) con vocabulario argentino nativo

**Concursal:**
- Verificar privilegios de créditos y estrategia de verificación
- Analizar acciones de recomposición patrimonial (período de sospecha, arts. 118-119 LCQ)

---

## Lo que no reemplaza

El criterio del abogado. La responsabilidad profesional. La firma.

Todo output del sistema es un borrador. No sabe qué pasó en la negociación, no conoce la relación con la contraparte, no tiene el expediente completo. Acelera la parte mecánica. Las decisiones son siempre del abogado.

---

## Actualización del sistema

El sistema tiene dos ciclos de actualización con distinta frecuencia:

**Perfiles de área (`*-CLAUDE.md`):** actualizar cuando cambia un instituto central
del área (nueva ley, reforma procesal, cambio de criterio CSJN en un tema estructural)
o cuando cambia una norma listada en la sección `## Alerta normativa` de ese perfil.
Frecuencia orientativa: continua para alertas normativas; semestral para el resto.

Para actualizaciones urgentes (nueva tasa CNAT, cambio de tope art. 245, reforma
procesal): modificar directamente la sección `## Alerta normativa` del perfil
afectado y registrar el cambio en `CHANGELOG.md`. Esa sección tiene el impacto
más inmediato en los marcadores que el sistema emite.

La tabla de normas de alta volatilidad del `CHANGELOG.md` lista los datos con
mayor frecuencia de cambio y la fecha de última verificación de cada uno.



---

## Contribuciones

El proyecto sigue en desarrollo para adaptar completamente Claude for Legal al derecho argentino.

Si hay abogados argentinos interesados en colaborar, la idea es dividir áreas de trabajo para coordinar esfuerzos, evitar duplicar trabajo y avanzar más rápido.

**Para reportar un error normativo**, abrí un issue indicando:
- la norma correcta y la fuente oficial
- el archivo y sección afectada
- el texto actual que considerás incorrecto

**Para proponer mejoras o nuevas áreas**, abrí un issue describiendo qué querés sumar y con qué alcance. Si querés adaptar el perfil para otra jurisdicción (Uruguay, Chile, Colombia), forkéalo y avisame.

**Para contribuir directamente**, editá el archivo en tu fork y abrí un Pull Request describiendo el cambio. Si no sabés cómo, mandame el texto por mensaje y lo incorporo yo con la atribución correspondiente. Los cambios con fuente normativa citada se procesan primero.

**Para aportar un caso de verificación**, el sistema incluye una carpeta `evals/` con casos de prueba que permiten comprobar que los perfiles de área detectan vicios y vulnerabilidades procesales de forma consistente. La idea es la misma que un caso de control en la práctica: una pieza procesal con solución conocida que se usa para verificar que la herramienta funciona antes de usarla en un expediente real. Cada caso tiene tres archivos: la pieza anonimizada, la rúbrica con los puntos que el sistema debe identificar, y la solución esperada. Las áreas prioritarias son nulidades procesales penales, prescripción laboral y vicios formales en contratos. Ver `evals/README.md` para el formato completo.

---

## Autor

Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)  
Abogado (CPACF) · CABA y GBA · Legal tech & IA aplicada a práctica jurídica argentina

*Última actualización: mayo 2026*
