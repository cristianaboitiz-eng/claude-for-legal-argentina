# claude-for-legal · Adaptación Argentina

Configuración de Claude para práctica legal argentina. El material está construido
sobre derecho argentino: CCCN, LCT, LDC, LGS, CPCCN/CPCCBA, y normas especiales.
No requiere ningún repositorio externo para funcionar; puede usarse de forma
autónoma desde Claude.ai Projects o Claude Code.

Cada perfil codifica las reglas que cambian el resultado: plazos diferenciados entre días hábiles administrativos y judiciales, alertas automáticas de caducidad con la norma y el artículo exacto, marcadores obligatorios cuando falta el acto notificado o el expediente, lógica de agotamiento de vía antes de analizar cualquier acción judicial, distinción entre regímenes que se confunden habitualmente (Dec 1510/97 vs. Ley 189 CCAyT, LCT vs. estatutos sectoriales, régimen federal pre y post-reforma Ley 27.742). El sistema no inventa fallos, no completa vigencia normativa cuando no tiene fuente verificable, no asume el contenido de actos o expedientes que el abogado no aportó. Cada gap tiene un marcador explícito con lo que falta para resolverlo.

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
  administrativo-CLAUDE.md          # Perfil derecho administrativo (federal)
  administrativo/                    # Perfiles jurisdiccionales (complementan al federal)
    administrativo-CABA-CLAUDE.md      # CABA (CCAyT / TSJBA)
    administrativo-PBA-CLAUDE.md       # Buenos Aires (Cámaras CA / SCBA)
    administrativo-CHUBUT-CLAUDE.md    # Chubut (STJ - Sala CA)
    administrativo-CÓRDOBA-CLAUDE.md   # Córdoba (TSJ - Sala CA)
    administrativo-CORRIENTES-CLAUDE.md # Corrientes (STJ - pleno)
    administrativo-ENTRERIOS-CLAUDE.md  # Entre Ríos (STJ - Sala N° 2 / Sala Constitucional y Electoral)
    administrativo-MENDOZA-CLAUDE.md   # Mendoza (SCJ - Sala Primera)
    administrativo-MISIONES-CLAUDE.md  # Misiones (STJ - pleno)
    administrativo-NEUQUEN-CLAUDE.md   # Neuquén (TSJ - Sala Procesal Administrativa)
    administrativo-RIONEGRO-CLAUDE.md  # Río Negro (STJ - última instancia)
    administrativo-SALTA-CLAUDE.md     # Salta (Corte de Justicia - pleno)
    administrativo-SANJUAN-CLAUDE.md   # San Juan (Corte de Justicia - Sala Segunda)
    administrativo-SANTAFE-CLAUDE.md   # Santa Fe (CSJSF)
    administrativo-TUCUMAN-CLAUDE.md   # Tucumán (CSJ - Sala CA)
    administrativo-_PROVINCIA_-CLAUDE.md # Template para nuevas provincias
  especialidades/
    medicina-legal-CLAUDE.md         # Pericia médica forense (penal / civil / seguridad social)
  civil-CLAUDE.md                   # Perfil derecho civil (CCCN)
  concursos-CLAUDE.md               # Perfil concursos y quiebras (LCQ)
  familia-CLAUDE.md                 # Perfil derecho de familia
  laboral-CLAUDE.md                 # Perfil derecho del trabajo (LCT)
  laboral/
    telegrama/
      telegramas-SKILL.md           # Instrucciones operativas del skill de telegramas
      tipos-de-telegrama.md         # Clasificación por grupo y notas críticas
      reglas-normativas.md          # Reglas de validación normativa post-reforma
      modelos/
        bloque-01-registro.md       # Registro de la relación laboral
        bloque-02-estabilidad-despido.md  # Estabilidad y despido
        bloque-03-salarios.md       # Pago de salarios y remuneraciones
        bloque-04-ius-variandi.md   # Modificaciones contractuales
        bloque-05-renuncia.md       # Renuncia
        bloque-06-vacaciones-licencias.md # Vacaciones y licencias
        bloque-07-salud-hostigamiento.md  # Seguridad, salud, hostigamiento y discriminación
        bloque-08-construccion.md   # Industria de la construcción (Ley 22.250)
  penal-CLAUDE.md                   # Perfil derecho penal
  societario-CLAUDE.md              # Perfil derecho societario (LGS)
  tributario-CLAUDE.md              # Perfil derecho tributario
  ejemplos-civil.md                 # Casos de daños y responsabilidad civil
  ejemplos-societario.md            # Due diligence y pactos de accionistas
  fuentes.md                        # Conectores MCP y fuentes primarias
  macos-automation.md               # Módulo opcional - automatización de escritorio macOS (Claude Code)
  legal.local.md.template           # Template de configuración local del estudio (por rama del derecho)
  evals/                            # Casos de control para verificar perfiles de área
    README.md                       # Formato estándar y áreas prioritarias
    administrativo-caba-recursos-agotamiento-via/  # Recursos Dec 1510/97 + plazo art. 7 CCAyT
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

## Lo que necesitás

Hay dos formas de instalarlo. El plan gratuito es suficiente para evaluar el sistema sin costo. El plan pago agrega automatización, acceso directo a archivos locales y tareas largas sin supervisión.

| Característica | Plan gratuito + Git Bash | Plan pago + Claude Desktop + Cowork |
|---|---|---|
| Costo | $0 | u$s 20/mes (Pro) |
| Activación de perfiles | Manual (copiar y pegar) | Automática según la rama del derecho del caso |
| Actualizaciones del repo | Automática (workflow diario incluido) | Automática (workflow diario incluido) |
| Acceso a archivos locales | No | Sí (directo, sin copiar archivos) |
| Tareas largas sin supervisión | No | Sí |
| Capacidades normativas | Completas | Completas |

---

## Instalación

### Opción A: Plan gratuito + Git Bash

**Lo que necesitás:** cuenta Claude gratuita y Git.

- **Windows:** instalá Git desde [git-scm.com](https://git-scm.com) con las opciones por defecto.
- **Mac:** instalá Git con Homebrew. Si no tenés Homebrew, primero corrés esto en la Terminal:
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
  Después:
  ```bash
  brew install git
  ```

No necesitás cuenta de GitHub para descargar y usar el sistema.

#### Paso 1: Clonar el repositorio

Abrí Git Bash desde el menú inicio y ejecutá:

```bash
git clone https://github.com/cristianaboitiz-eng/claude-for-legal-argentina.git
cd claude-for-legal-argentina
git pull
```

El `git pull` trae los cambios más recientes. Si dice "Already up to date" ya tenés la versión actual.

Una vez ejecutado, todos los archivos del sistema quedan en tu computadora en la carpeta `C:\Users\TU USUARIO\claude-for-legal-argentina\argentina\`. Desde ahí vas a adjuntarlos en Claude cuando el sistema te lo pida.

#### Paso 2: Configurar el perfil del estudio
 
El archivo `argentina/legal.local.md` le dice al sistema quién sos, en qué fueros trabajás y cómo trabajás. Es privado: nunca se sube al repositorio.
 
Creá tu copia:
 
**Windows:**
```bash
cp argentina/legal.local.md.template argentina/legal.local.md
notepad argentina/legal.local.md
```
 
**Mac:**
```bash
cp argentina/legal.local.md.template argentina/legal.local.md
open -e argentina/legal.local.md
```
 
`open -e` abre el archivo en TextEdit. Si no funciona, probá `nano argentina/legal.local.md`.
 
Para completarlo, abrís un chat en [claude.ai](https://claude.ai), adjuntás `argentina/legal.local.md.template` y escribís:
 
> "Completá este archivo con los datos de mi estudio."
 
Copiás el resultado y lo guardás como `C:\Users\[TU USUARIO]\claude-for-legal-argentina\argentina\legal.local.md`. Después lo protegés:
 
```bash
echo "legal.local.md" >> .gitignore
```
 
**Crear tu copia personal:**

En Git Bash ejecutás:

```bash
cp argentina/legal.local.md.template argentina/legal.local.md
```

**Completarlo con ayuda de Claude:**

Abrís un chat nuevo en [Claude.ai](https://claude.ai), adjuntás el archivo `C:\Users\TU USUARIO\claude-for-legal-argentina\argentina\legal.local.md.template` y escribís:

> "Completá este archivo con los datos de mi estudio."

Copiás el resultado y lo guardás como `C:\Users\TU USUARIO\claude-for-legal-argentina\argentina\legal.local.md`.

**Protegerlo para que no se suba al repositorio por error:**

```bash
echo "legal.local.md" >> .gitignore
```

#### Paso 3: Mantener el sistema actualizado

El repositorio no se actualiza solo con el plan gratuito. Cada vez que haya cambios - perfiles de área, alertas normativas, correcciones - los bajás con un solo comando:

```bash
cd claude-for-legal-argentina
git pull
```

Hacelo antes de cada sesión de trabajo, o cuando veas un aviso de actualización en el repositorio. El pull es instantáneo y nunca pisa tu `legal.local.md` porque ese archivo está protegido por el `.gitignore`.

#### Paso 4: Crear el Project en Claude.ai y cargar los perfiles

En un chat nuevo de Claude adjuntás el archivo `C:\Users\TU USUARIO\claude-for-legal-argentina\argentina\CLAUDE.md`, escribís **"Corré la entrevista de configuración"** y completás las preguntas. El sistema te entrega un `CLAUDE.md` personalizado con los datos de tu práctica.

Después:

1. En [Claude.ai](https://claude.ai) entrás a **Projects** (barra lateral izquierda) y creás uno nuevo. Le ponés el nombre de tu práctica.
2. Dentro del Project, hacés clic en el ícono de lápiz (**Project instructions**) y pegás el `CLAUDE.md` personalizado que te generó la entrevista. Queda activo en todas las conversaciones de ese Project.
3. Subís los perfiles de área como **Knowledge** del Project (botón "Add content"). Ejemplos según tu fuero habitual:
   - Laboral: `argentina/laboral-CLAUDE.md`. Para usar skills específicas (telegramas, plazos u otras), subí los archivos de la subcarpeta correspondiente dentro de `argentina/laboral/` cuando las necesites.
   - Civil: `argentina/civil-CLAUDE.md` + `argentina/ejemplos-civil.md`
   - Administrativo CABA: `argentina/administrativo-CLAUDE.md` + `argentina/administrativo-caba-CLAUDE.md`
   - Administrativo PBA: `argentina/administrativo-CLAUDE.md` + `argentina/administrativo-PBA-CLAUDE.md`
   - Administrativo Salta: `argentina/administrativo-CLAUDE.md` + `argentina/administrativo-SALTA-CLAUDE.md`
   - También subís tu `argentina/legal.local.md` con los datos del estudio.
4. Guardás. Cada conversación nueva dentro del Project arranca con todos esos archivos activos.

**Límite del plan gratuito:** el espacio de Knowledge es acotado. Si no entran todos los archivos, priorizá el `CLAUDE.md` personalizado + el perfil de área + tu `legal.local.md`. Los perfiles complementarios los podés pegar manualmente al inicio de la conversación cuando el caso lo requiera.

**Para mantener el Project actualizado:** cada vez que hagas `git pull` y haya cambios en algún perfil cargado en el Project, reemplazás el archivo subiendo la versión nueva desde Knowledge.

---

### Opción B: Plan pago + Claude Desktop + Cowork

**Lo que necesitás:** Plan Pro (u$s 20/mes), Max, Team o Enterprise, y la aplicación de escritorio Claude.

#### Paso 1: Descargá la aplicación de escritorio

Entrá a [claude.ai/download](https://claude.ai/download) y bajá la app para Windows o Mac. Instalala como cualquier otro programa.

#### Paso 2: Abrí Cowork

Una vez abierta la app, vas a ver una barra en la parte superior con distintas pestañas. Hacé clic en "Cowork".

Cowork es el entorno de trabajo avanzado donde viven los plugins. La primera vez te va a pedir que configures acceso a una carpeta de tu computadora - dáselo a una carpeta donde tengas documentos de trabajo (contratos, escritos, lo que sea). Claude va a poder leer los archivos de esa carpeta.

#### Paso 3: Instalá el plugin legal

Dentro de Cowork, hacé clic en "Customize" (Personalizar) en la barra lateral izquierda. Eso abre el menú de plugins, skills y conectores. [Más información](https://support.claude.com/en/articles/13837440-use-plugins-in-claude-cowork)

Desde ahí:

1. Clic en "Browse plugins" (Explorar plugins).
2. Buscá Legal en la lista.
3. Clic en Install.

Después de instalarlo, el plugin ejecuta automáticamente una entrevista inicial. Te pregunta sobre tu práctica: jurisdicción, tipo de trabajo habitual, a quién escalás, etc. Con esas respuestas arma tu perfil de práctica, y de ahí en más todos los flujos de trabajo corren contra ese contexto, no contra una plantilla genérica. Eso es lo que diferencia esta herramienta de un chat común.

#### Paso 4: Configurar el perfil argentino

Dentro de Cowork, cargás el contenido de `C:\Users\TU USUARIO\claude-for-legal-argentina\argentina\CLAUDE.md` como perfil base. Ese archivo reemplaza la lógica norteamericana del plugin original con configuración argentina. La primera vez que usás un plugin de área, el sistema corre la entrevista de configuración; cuando te pida el perfil de práctica, usás el contenido de `argentina/legal.local.md` que ya completaste.

#### Paso 5: Elegí qué plugins instalar

Instalá los que correspondan a tu práctica. Podés instalar varios.

#### Paso 6: Empezar a usarlo

Las skills se activan automáticamente cuando son relevantes. También podés invocarlas manualmente escribiendo "/" para ver la lista de comandos disponibles. Claude accede a tu carpeta de trabajo, lee los archivos directamente y ejecuta tareas largas sin supervisión: liquidaciones sobre varios expedientes, revisión de contratos en lote, matrices de riesgo, cronologías. Las actualizaciones del repositorio se incorporan automáticamente la próxima vez que usás el sistema.

Para activar una skill específica (telegramas, plazos u otras): en Cowork, con acceso habilitado a tu carpeta del repo, indicale a Claude que lea el archivo correspondiente dentro de `argentina/laboral/`. No uses el flujo "Cargar habilidad", ese es para archivos `.skill` de Cowork, no para los `.md` de este repo.

---

## Perfiles por área

Los plugins disponibles corresponden a las áreas de práctica cubiertas por este sistema:

| Archivo de perfil | Área | Complementos | Alertas |
|---|---|---|---|
| `laboral-CLAUDE.md` | Derecho del trabajo (LCT) | `laboral/telegrama/` | DNU 70/2023, Ley 27.742, Ley 27.802, topes art. 245, tasas CNAT |
| `administrativo-CLAUDE.md` | Derecho administrativo (federal) | - | Plazos de caducidad, contratación pública |
| `administrativo-CABA-CLAUDE.md` | Derecho administrativo CABA | `administrativo-CLAUDE.md` (base) | Plazo 90 días art. 7 CCAyT, Dec 1510/97, Ley 2095, Ley 471 |
| `administrativo-PBA-CLAUDE.md` | Derecho administrativo PBA | `administrativo-CLAUDE.md` (base) | Plazos CPCA PBA, Ley 7647, contratación pública PBA |
| `administrativo-SALTA-CLAUDE.md` | Derecho administrativo Salta | `administrativo-CLAUDE.md` (base) | Procedimiento administrativo Salta, fuero contencioso local |
| `civil-CLAUDE.md` | Derecho civil (CCCN) | `ejemplos-civil.md` | Tasas de interés, fórmulas de daños por fuero |
| `penal-CLAUDE.md` | Derecho penal | - | Umbrales penales, código procesal vigente |
| `familia-CLAUDE.md` | Derecho de familia | - | Cuotas alimentarias, régimen de alquileres |
| `societario-CLAUDE.md` | Societario y M&A | `ejemplos-societario.md` | Resoluciones IGJ/DPPJ, capital mínimo |
| `tributario-CLAUDE.md` | Derecho tributario | - | Alícuotas, MNI, umbrales de punibilidad |
| `concursos-CLAUDE.md` | Concursos y quiebras (LCQ) | - | Tasas post-concursales, reformas LCQ |
| `contratos-CLAUDE.md` | Revisión y redacción de contratos | `red-flags-contratos.md` | Régimen cambiario, locaciones, intertemporalidad |
| `especialidades/medicina-legal-CLAUDE.md` | Pericia médica forense (penal / civil / seguridad social) | - | CPPF implementación por distrito, baremos por tribunal |

---

## Alertas de normas inestables

Cada perfil de área incluye una sección `## Alerta normativa` con las normas de mayor
volatilidad para esa materia. La sección está ubicada antes de las instrucciones operativas
de cada perfil para que el sistema la procese con prioridad.

| Perfil | Sección de alerta | Normas cubiertas |
|---|---|---|
| `laboral-CLAUDE.md` | `## Alerta normativa - Reforma laboral 2023-2026 vigente operacionalmente` | DNU 70/2023, Ley 27.742 (derogación agravantes registrales), Ley 27.802 (art. 245, art. 66, art. 80, art. 240) |
| `civil-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Tasas de interés por fuero, fórmulas de cuantificación de daños, art. 52 bis LDC |
| `administrativo-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Plazos de caducidad art. 25 LNPA, contratación pública, normativa provincial |
| `concursos-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Tasas post-concursales, período de sospecha, reformas LCQ |
| `tributario-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Ganancias/MNI, Bienes Personales, umbrales penales Ley 27.430, monto mínimo TFN |
| `familia-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Cuotas alimentarias, locaciones con destino habitacional |
| `penal-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Umbrales de punibilidad, códigos procesales en transición |
| `societario-CLAUDE.md` | `## Alerta normativa - normas de vigencia variable` | Resoluciones IGJ/DPPJ, capital mínimo, sindicatura |
| `especialidades/medicina-legal-CLAUDE.md` | `## Alerta normativa` | Estado de implementación CPPF por distrito, baremos por tribunal requirente |



---

## Conectores MCP - Fuentes oficiales argentinas

Los conectores MCP son una capa opcional que permite que Claude consulte fuentes jurídicas oficiales directamente desde el chat, sin que tengas que copiar y pegar texto manualmente. Claude busca la norma, el fallo o el expediente por vos y lo incorpora a la respuesta.

No son necesarios para empezar. Los perfiles funcionan solos. Los conectores mejoran la experiencia una vez que el sistema ya está funcionando.

**Regla general antes de usar cualquier conector:** hacé una consulta de prueba antes de usarlo en una sesión real. Si el conector no responde, accedé directamente a la fuente primaria (los links están al final de esta sección) y pegá el texto en la sesión.

---

### Cómo instalar los conectores

Hay tres formas de instalar un conector. La más simple para abogados sin experiencia técnica es la primera.

#### Opción 1: Por URL en Claude.ai - sin instalar nada (recomendada)

Funciona para todos los conectores voftec (BOPBA, Normativa PBA, BORA, JUBA, InfoLeg, PJN consulta, PJN jurisprudencia, PTN, TFN). El proceso es idéntico para todos:

1. En [Claude.ai](https://claude.ai) entrás a **Settings → Integrations → Add MCP Server**.
2. En el campo URL pegás la URL del conector (ver tabla abajo).
3. Le ponés un nombre descriptivo, por ejemplo `JUBA - Jurisprudencia PBA`.
4. Guardás. El conector queda disponible en todos tus Projects.

No requiere instalar ningún programa adicional.

#### Opción 2: Por comando (conectores de la comunidad)

Algunos conectores se instalan con un comando en la terminal. Solo aplica si ya tenés Claude Code instalado.

#### Opción 3: Instalación manual desde GitHub

Para usuarios con experiencia técnica. Ver el README de cada repositorio.

---

### Conectores voftec

Todos tienen instalación por URL (Opción 1). Todos son gratuitos.

| Conector | Qué hace | URL para instalar |
|---|---|---|
| **BORA** - Boletín Oficial nacional | Normas nacionales publicadas, nuevas sociedades, licitaciones | `https://bora-mcp.vercel.app` |
| **BOPBA** - Boletín Oficial PBA | Normas publicadas en el BOPBA, búsqueda por fecha y número | `https://bopba-mcp.vercel.app` |
| **InfoLeg** - Legislación nacional | Texto oficial de normas nacionales desde infoleg.gob.ar | `https://infoleg-mcp.vercel.app` |
| **Normativa PBA** | Legislación provincial PBA: texto, vigencia, articulado | `https://normativapba-mcp.vercel.app` |
| **JUBA** - Jurisprudencia PBA | Fallos SCBA y cámaras de apelación PBA | `https://juba-mcp.vercel.app` |
| **PJN** - Expedientes | Consulta de expedientes PJN: estado, movimientos, carátula | `https://pjn-consulta-mcp.vercel.app` |
| **PJN** - Jurisprudencia | Fallos, sentencias y resoluciones de fueros federales PJN | `https://pjn-juris-mcp.vercel.app` |
| **PTN** - Dictámenes | Dictámenes de la Procuración del Tesoro de la Nación | `https://ptn-mcp.vercel.app` |
| **TFN** - Tribunal Fiscal de la Nación | Jurisprudencia y resoluciones TFN: impositivo y aduanero, 16 herramientas, descarga PDF | `https://tfn-mcp.vercel.app` |

**Nota sobre Normativa PBA:** la herramienta de vigencia consulta el portal normas.gba.gob.ar y reproduce su estado tal como está cargado. El portal puede tener errores en relaciones de derogación. Usalo como primer filtro y verificá siempre contra el Boletín Oficial PBA ante cualquier resultado que parezca anómalo.

**Diferencia entre los dos conectores PJN:** PJN-Expedientes consulta el estado procesal de un expediente (movimientos, carátula, fecha de última actuación). PJN-Jurisprudencia devuelve el texto de fallos y sentencias para investigación previa a la redacción de escritos. Son complementarios, no equivalentes.

**Disponibilidad de los conectores:** las URLs de esta tabla fueron verificadas en mayo 2026. Antes de usar cualquier conector en una sesión real, hacé una consulta de prueba. Si no responde, usá la fuente primaria directamente (links al final de esta sección).

---

### Conectores de la comunidad

Requieren instalación por comando o manual. Los conectores con `uvx` requieren Claude Code instalado. Los que se instalan manualmente desde GitHub (como `scba-mcp-server`) funcionan con Claude Desktop sin Claude Code.

| Conector | Fuente | Función | Instalación |
|---|---|---|---|
| saij-mcp | SAIJ | Jurisprudencia, legislación, doctrina y dictámenes | `claude mcp add saij-mcp -- uvx saij-mcp` · [GitHub](https://github.com/hernan-cc/saij-mcp) |
| csjn-mcp | CSJN | Fallos de la Corte Suprema | `claude mcp add csjn-mcp -- uvx csjn-mcp` · [GitHub](https://github.com/hernan-cc/csjn-mcp) |
| juscaba-mcp | JUSCABA | Jurisprudencia fueros nacionales con sede en CABA | `claude mcp add juscaba-mcp -- uvx juscaba-mcp` · [GitHub](https://github.com/hernan-cc/juscaba-mcp) |
| saij-mcp (Escalante) | SAIJ | Investigación profunda: grafo legal, OCR para PDFs históricos | Ver [repositorio](https://github.com/joaquinescalante23/saij-mcp) |
| guidobonomini | Local | Análisis semántico y terminológico de textos jurídicos | Ver [repositorio](https://github.com/guidobonomini/argentina-law-mcp-server) |
| macos-use | Desktop | Automatización de portales sin API (PJN, SCBA, IGJ) - solo Mac, solo Claude Code | Ver [repositorio](https://github.com/mediar-ai/mcp-server-macos-use) |
| scba-mcp-server | SCBA | Sentencias y resoluciones de primera instancia PBA (sentencias.scba.gov.ar): búsqueda por organismo, fecha y texto libre; descarga y guarda documentos en disco. Requiere Chrome + chromedriver instalados localmente. No cubre JUBA (Cámaras / SCBA). | Ver [repositorio](https://github.com/FacundoEmanuel/scba-mcp-server) |

**Ecosistema Hernán Caravario (hernan-cc):** saij-mcp, csjn-mcp y juscaba-mcp son parte del mismo ecosistema. Podés instalar los tres en simultáneo; Claude elige cuál usar según la consulta. Ver todos en [github.com/hernan-cc](https://github.com/hernan-cc) y [hernancc.com/mcp-tools](https://hernancc.com/mcp-tools).

---

### Fuentes primarias

Accedé directamente y pegá el texto en la sesión. Son la fuente de verdad ante cualquier discrepancia.

| Necesidad | URL |
|---|---|
| Normas nacionales | infoleg.gob.ar |
| Boletín Oficial nacional | boletinoficial.gob.ar |
| Normas PBA | normas.gba.gob.ar |
| Boletín Oficial PBA | boletinoficial.gba.gob.ar |
| Jurisprudencia SCBA y cámaras PBA | juba.scba.gov.ar |
| Sentencias y resoluciones primera instancia PBA | sentencias.scba.gov.ar |
| Jurisprudencia CSJN | sj.csjn.gov.ar |
| Jurisprudencia federal PJN (fallos y sentencias) | pjn.gov.ar |
| Jurisprudencia SAIJ | saij.gob.ar |
| Jurisprudencia CABA y fueros nacionales | jusbaires.gob.ar |
| Expedientes PJN | pjn.gov.ar |
| Dictámenes PTN | busquedadictamenes.ptn.gob.ar |
| Jurisprudencia contencioso administrativo federal | cnacaf.gov.ar |
| Resoluciones IGJ | igj.gob.ar |
| Resoluciones DPPJ (societario PBA) | gba.gob.ar/dppj |
| Jurisprudencia tributaria TFN | tfn.gob.ar |
| Normativa BCRA | bcra.gov.ar |
| Disposiciones AAIP (datos personales) | argentina.gob.ar/aaip |

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
- Calcular liquidaciones finales (art. 245 LCT con los tres regímenes según fecha del acto extintivo, certificados art. 80 LCT)
- Analizar estrategia desde el trabajador o el empleador con carga probatoria invertida
- Redactar telegramas y cartas documento laborales con verificación normativa post-reforma (Ley 27.742 + Ley 27.802)

**Administrativo:**
- Verificar agotamiento de la vía administrativa y plazos de caducidad (art. 25 LNPA y equivalentes provinciales)
- Analizar recursos administrativos y acciones contenciosas en fuero federal, CABA (CCAyT / TSJBA) y las provincias con perfil cargado: Buenos Aires (Cámaras CA / SCBA), Chubut (STJ - Sala CA), Córdoba (TSJ - Sala CA), Corrientes (STJ - pleno), Entre Ríos (STJ - Sala N° 2 / Sala Constitucional y Electoral), Mendoza (SCJ - Sala Primera), Misiones (STJ - pleno), Neuquén (TSJ - Sala Procesal Administrativa), Río Negro (STJ), Salta (Corte de Justicia - pleno), San Juan (Corte de Justicia - Sala Segunda), Santa Fe (CSJSF) y Tucumán (CSJ - Sala CA)
- Identificar el régimen procesal aplicable en cada jurisdicción y alertar sobre plazos de caducidad diferenciados entre vía administrativa y acción judicial

**Penal:**
- Analizar estrategia de defensa por etapa procesal y código aplicable (CPPN / CPPF / CPPCABA / CPPBA)
- Evaluar procedencia de colaboración eficaz (Ley 27.304) y proceso de flagrancia (Ley 27.272)

**Medicina legal y pericia médica forense:**
- Redactar y analizar informes médico-legales periciales en los fueros penal, civil y de la seguridad social
- Verificar estructura, completitud de puntos periciales y vacíos probatorios antes de presentar el informe
- Identificar el régimen procesal aplicable (CPPN / CPPF / CPCCN / Ley 24.655) y alertar sobre plazos urgentes en causas con detenidos

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

**Sincronización del fork con el repo original:**

El repositorio incluye un workflow de GitHub Actions que sincroniza tu fork con el original de Anthropic todos los días a las 03:00 (hora Argentina), sin que tengas que hacer nada. Es un robot incluido en el repo: revisa si hubo cambios en el repo original y los incorpora a tu copia automáticamente. Tus archivos propios (carpeta `argentina/` y `legal.local.md`) nunca se pisan. El workflow corre gratis en todos los planes de GitHub, incluido el gratuito.

Si preferís hacerlo a mano, GitHub te avisa cuando tu fork está desactualizado y podés sincronizar con un click desde el botón "Sync fork" en la página del repo.

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

**Para aportar un caso de verificación**, el sistema incluye una carpeta `evals/` con casos de prueba que permiten comprobar que los perfiles de área detectan vicios y vulnerabilidades procesales de forma consistente. La idea es la misma que un caso de control en la práctica: una pieza procesal con solución conocida que se usa para verificar que la herramienta funciona antes de usarla en un expediente real. Cada caso tiene tres archivos: la pieza anonimizada, la rúbrica con los puntos que el sistema debe identificar, y la solución esperada. Las áreas prioritarias son nulidades procesales penales y vicios formales en contratos. Ver `evals/README.md` para el formato completo.

---

## Autor

Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)  
Abogado (CPACF) · CABA y GBA · Legal tech & IA aplicada a práctica jurídica argentina

*Última actualización: mayo 2026*
