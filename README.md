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

---

## Antes de empezar

Necesitás:
- Cuenta de Claude.ai con plan Pro o Team
- Opcionalmente: Claude Code (terminal) o Claude Cowork (escritorio) para flujos más automatizados

No necesitás saber programar para la configuración base en Claude.ai Projects.
Para conectar fuentes normativas locales (fase 2, ver `fuentes.md`), vas a necesitar
acceso a Claude Code o ayuda técnica para instalar los conectores MCP.

---

## Instalación

### Paso 1: Fork

Hacé click en "Fork" arriba a la derecha. Eso crea una copia en tu cuenta. No descargues el ZIP: el fork te permite incorporar actualizaciones del repositorio original sin pisar tu configuración local.

### Paso 2: Perfil de práctica general

Abrí `argentina/CLAUDE.md` y cargá su contenido en las instrucciones del Project
de Claude que vas a usar para práctica general.

**Para configuración personalizada:** corrí la entrevista de `setup-interview.md`
antes de cargar el CLAUDE.md. La entrevista genera un CLAUDE.md personalizado
con tu jurisdicción, áreas de práctica, CCT habitual y preferencias de formato.
El template de output está en `setup-output-TEMPLATE.md`.

Sin configuración personalizada: el CLAUDE.md genérico funciona pero opera con
supuestos genéricos de jurisdicción y área.

### Paso 3: Perfiles por área

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

### Paso 4: Configuración del skill de diagnóstico

Cargá `diagnostico-SKILL.md` en cualquier Project donde quieras que el sistema
diagnostique escritos antes de modificarlos. Puede cargarse solo o junto con
cualquier perfil de área.

Para verificar que el skill funciona correctamente, usá `diagnostico-casos-prueba.md`:
pegá uno de los tres escritos de prueba y comparás el output del sistema con
el diagnóstico esperado documentado en el archivo.

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
| 2 | [Psflores/Legal-MCP-Server-](https://github.com/Psflores/Legal-MCP-Server-) | PJN / CABA | Jurisprudencia fueros nacionales | Gratuito |
| 3 | [guidobonomini/argentina-law-mcp-server](https://github.com/guidobonomini/argentina-law-mcp-server) | Praxis local | Análisis semántico, glosario judicial | Gratuito |
| 4 | [datos-justicia-argentina/Tesauro-Saij](https://github.com/datos-justicia-argentina/Tesauro-Saij-de-Derecho-Argentino) | SAIJ | Vocabulario controlado para búsqueda jurídica | Gratuito |
| 5 | [voftec/normativapba-mcp](https://github.com/voftec/normativapba-mcp) · `https://normativapba-mcp.vercel.app` | normas.gba.gob.ar | Legislación provincial PBA: búsqueda, vigencia, articulado, árbol de dependencias normativas. Conexión directa vía URL en Claude.ai (Settings → Integrations) o instalable vía npx. Consulta en tiempo real sobre el portal oficial. Ver nota de limitación abajo. | Gratuito |
| 6 | [joaquinescalante23/saij-mcp](https://github.com/joaquinescalante23/saij-mcp) | SAIJ | Investigación profunda: jurisprudencia, legislación, doctrina y dictámenes; grafo legal; OCR para PDFs históricos; resolución de citas textuales. Opera sobre API no oficial de SAIJ - verificar estado antes de usar. | Gratuito |
| 7 | `https://api.fallobot.com/mcp` | CSJN · SAIJ · JUBA · SCBA | Búsqueda multifuente simultánea en lenguaje natural; enlaza al fallo original en la fuente oficial | Plan Pro (fallobot.com) |
| 8 | SCBA / JUBA | Jurisprudencia PBA | Sin conector MCP de fuente abierta; cubierto por FalloBot (7). Ver instrucciones de acceso directo en `fuentes.md` | — |

#### Nota sobre el conector 5 (voftec/normativapba-mcp) - `verificar_vigencia`

La herramienta `verificar_vigencia` consulta en tiempo real los metadatos de `normas.gba.gob.ar` y reproduce su estado tal como está cargado en el portal. El portal puede contener errores en las relaciones de derogación. Caso conocido: la Ley 11.922 (CPP Bonaerense, 1997) figura en el portal como derogada por la Ley/Decreto-ley 9032 (1978), cuando la relación es inversa: la 11.922 deroga a la 9032 y está plenamente vigente con modificatorias.

Regla de uso: `verificar_vigencia` es un primer filtro, no una fuente definitiva. Ante cualquier resultado de derogación que parezca anómalo, verificar contra el Boletín Oficial PBA o el texto actualizado disponible en el propio portal. El error fue reportado al mantenedor del conector y a la Subsecretaría Legal y Técnica de PBA para corrección en la fuente.

### Tabla de decisión rápida

| Necesidad | Conector recomendado | Fallback manual |
|---|---|---|
| Texto de norma nacional | 1 (Ansvar) | infoleg.gob.ar |
| Texto de norma provincial PBA | 5 (voftec) | normas.gba.gob.ar |
| Jurisprudencia CSJN | 7 (FalloBot, plan Pro) | sj.csjn.gov.ar |
| Jurisprudencia CABA / fueros nacionales | 2 (Psflores) o 6 (saij-mcp) | pjn.gov.ar · jusbaires |
| Jurisprudencia SAIJ (todas las instancias) | 6 (saij-mcp) | saij.gob.ar |
| Doctrina y dictámenes | 6 (saij-mcp) | saij.gob.ar |
| Grafo legal / navegación de citas | 6 (saij-mcp) | Manual en saij.gob.ar |
| Jurisprudencia PBA (SCBA y cámaras) | 7 (FalloBot, plan Pro) | juba.scba.gov.ar |
| Búsqueda multifuente simultánea | 7 (FalloBot, plan Pro) | Fuentes por separado |
| Análisis semántico / terminología | 3 (guidobonomini) | Glosario del CLAUDE.md |
| Mejora de búsquedas jurisprudenciales | 4 (Tesauro SAIJ) | saij.gob.ar |

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
automáticamente sin que el abogado tenga que pegar el texto en la sesión. Ver `fuentes.md`
para instrucciones completas de verificación de estado, fallback y combinaciones recomendadas.

---

## Lo que podés hacer desde el día uno

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

Si hay abogados argentinos interesados en colaborar, la idea es dividir áreas de trabajo para coordinar esfuerzos, evitar duplicar trabajo y avanzar más rápido. Las áreas abiertas incluyen:

| Área | Ejemplos de contribución |
|---|---|
| Perfiles de área | Penal, laboral, compliance, privacidad, procesal |
| Prompts y ejemplos | Casos de prueba, escritos tipo, checklists |
| Validación normativa | Verificación de citas, alertas de normas inestables |
| Fuentes y conectores | Nuevos conectores MCP, cobertura provincial |
| Testing | Validar outputs contra casos reales |

**Para reportar un error normativo**, abrí un issue indicando:
- la norma correcta y la fuente oficial
- el archivo y sección afectada
- el texto actual que considerás incorrecto

**Para proponer mejoras o nuevas áreas**, abrí un issue describiendo qué querés sumar y con qué alcance. Si querés adaptar el perfil para otra jurisdicción (Uruguay, Chile, Colombia), forkéalo y avisame.

**Para contribuir directamente**, editá el archivo en tu fork y abrí un Pull Request describiendo el cambio. Si no sabés cómo, mandame el texto por mensaje y lo incorporo yo con la atribución correspondiente. Los cambios con fuente normativa citada se procesan primero.

---

## Autor

Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)  
Abogado (CPACF) · CABA y GBA · Legal tech & IA aplicada a práctica jurídica argentina

*Última actualización: mayo 2026*
