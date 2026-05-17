# Fuentes normativas argentinas · Conectores MCP

Repositorios de la comunidad que conectan claude-for-legal directamente
con las fuentes oficiales argentinas. Reemplazan los conectores originales
del repositorio base (Westlaw, CourtListener, Everlaw) para práctica local.

Los conectores son la segunda capa del sistema. Los plugins funcionan
sin ellos usando el perfil de práctica como única configuración.
Con los conectores, el sistema consulta fuentes primarias automáticamente
sin que el abogado tenga que pegar el texto de la norma en la sesión.

---

## Cómo verificar que un conector está activo antes de usarlo

Los conectores de esta lista son proyectos de la comunidad sin mantenimiento
garantizado. Antes de depender de un conector en una sesión de trabajo:

1. En Claude Cowork: ir a Configuración > MCP Servers y verificar que el conector
   figura como activo (ícono verde). Si figura como inactivo o no aparece,
   no está disponible para esa sesión.
2. En Claude Code: ejecutar `mcp list` para ver los conectores activos en el
   contexto actual. Si el conector no aparece, no está disponible.
3. Hacer una consulta de prueba mínima antes de la consulta real:
   "¿Podés consultar el art. 1 de la Ley 26.994?" para el conector 1, por ejemplo.
   Si el conector responde con el texto correcto, está activo. Si devuelve
   error o no responde, aplicar el fallback correspondiente.

**Si un conector no responde:** no intentar la misma consulta dos veces.
Aplicar el fallback de la tabla de abajo y registrar en la sesión que el
conector no estaba disponible.

### Tabla de fallback por conector

| Conector | Función | Fallback si no responde |
|---|---|---|
| 1 - Ansvar (InfoLEG) | Texto de normas nacionales | Acceder directamente a infoleg.gob.ar y pegar el texto en la sesión |
| 2 - Psflores (PJN/CABA) | Jurisprudencia fueros nacionales | Acceder a pjn.gov.ar o buenosaires.gob.ar/jusbaires y pegar el fallo en la sesión |
| 3 - guidobonomini | Análisis semántico / glosario | Operar con el glosario del CLAUDE.md argentino; la calidad terminológica puede bajar |
| 4 - Tesauro SAIJ | Vocabulario jurídico | Usar terminología estándar del CCCN y LCT directamente |
| SCBA | Jurisprudencia PBA | Acceder a scba.gov.ar/jurisprudencia y pegar el fallo en la sesión |

Cuando se usa el fallback manual (pegar texto en sesión), indicar siempre
al inicio del texto pegado: fuente, fecha de consulta, y URL de origen.

---

## Conectores disponibles

### 1. Ansvar-Systems/argentine-law-mcp

**Repositorio:** https://github.com/Ansvar-Systems/argentine-law-mcp
**Fuentes:** InfoLEG · SAIJ
**Función:** Devuelve el texto literal de normas nacionales argentinas sin
pasar por ningún modelo de lenguaje. Consulta directa a InfoLEG.
**Estado al mayo 2026:** activo según última verificación. Confirmar antes de usar.

Casos de uso:
- Verificar el texto actual de un artículo del CCCN, LCT, LDC u otra norma nacional
- Confirmar si una norma fue modificada o derogada
- Obtener el texto de una ley especial sin buscarlo manualmente

Limitaciones:
- Solo normas nacionales (no provinciales)
- No incluye jurisprudencia
- No realiza análisis: devuelve texto literal

**Fallback:** infoleg.gob.ar · acceso directo sin conector.

---

### 2. Psflores/Legal-MCP-Server-

**Repositorio:** https://github.com/Psflores/Legal-MCP-Server-
**Fuentes:** Poder Judicial de la Nación · Justicia CABA
**Función:** Búsqueda de jurisprudencia de fueros nacionales y CABA.
**Estado al mayo 2026:** proyecto de la comunidad sin mantenimiento activo declarado.
Verificar estado antes de usar (ver instrucciones arriba).

Casos de uso:
- Buscar fallos por doctrina antes de citar en un escrito
- Verificar criterio de la sala en una materia específica
- Rastrear evolución jurisprudencial sobre un instituto

Limitaciones:
- No cubre PBA (SCBA ni cámaras de apelación provinciales)
- Los resultados deben verificarse antes de citar: el conector busca,
  no garantiza que el fallo sea el más reciente o representativo

**Fallback:** pjn.gov.ar (fueros federales y nacionales) · buenosaires.gob.ar/jusbaires (fuero local CABA).

---

### 3. guidobonomini/argentina-law-mcp-server

**Repositorio:** https://github.com/guidobonomini/argentina-law-mcp-server
**Función:** Análisis semántico de documentos legales, glosario judicial
argentino, detección de riesgos calibrada para praxis local.
**Estado al mayo 2026:** proyecto de la comunidad sin mantenimiento activo declarado.
Verificar estado antes de usar (ver instrucciones arriba).

Casos de uso:
- Análisis de contratos con terminología jurídica argentina nativa
- Corrección de terminología cuando el sistema genera términos de common law
- Consistencia terminológica en documentos largos

Limitaciones:
- No conecta a fuentes primarias oficiales
- El análisis semántico está basado en praxis documentada, no en texto oficial
- Complementa al conector 1, no lo reemplaza

**Fallback:** operar con el glosario de terminología del CLAUDE.md argentino.
La calidad terminológica puede bajar en documentos con mucho vocabulario específico.

---

### 4. datos-justicia-argentina/Tesauro-Saij-de-Derecho-Argentino

**Repositorio:** https://github.com/datos-justicia-argentina/Tesauro-Saij-de-Derecho-Argentino
**Fuente:** SAIJ
**Función:** Vocabulario controlado para búsqueda jurídica. Mapea sinónimos,
términos preferidos y jerarquías conceptuales del derecho argentino.
**Estado al mayo 2026:** repositorio de datos estático; menor riesgo de caída
que los conectores de consulta en tiempo real. Verificar igualmente antes de usar.

Casos de uso:
- Mejorar la precisión de búsquedas jurisprudenciales
- Evitar que el sistema use términos de common law cuando existe equivalente argentino
- Consistencia terminológica en documentos largos

Limitaciones:
- Es un vocabulario de referencia, no un conector a fuentes primarias
- No devuelve texto normativo ni fallos: solo estructura conceptual

**Fallback:** usar terminología estándar de CCCN, LCT y LDC directamente.

---

### 5. FalloBot - CSJN + SAIJ + JUBA + SCBA

**Endpoint MCP:** `https://api.fallobot.com/mcp`
**Fuentes consultadas en paralelo:** CSJN, SAIJ, JUBA (sistema de jurisprudencia PBA) y SCBA
**Función:** búsqueda en lenguaje natural en todas las fuentes oficiales argentinas simultáneamente. Cada resultado enlaza al fallo original en la fuente oficial. No almacena copias: cada búsqueda va directo a la fuente.
**Requisito:** cuenta en fallobot.com con plan Pro. La integración con Claude se configura en Configuración → Conectores → Agregar conector personalizado → pegar la URL del endpoint.
**Estado al mayo 2026:** activo y documentado en https://fallobot.com

Casos de uso:
- Buscar jurisprudencia de CSJN sin acceso directo a sj.csjn.gov.ar
- Buscar fallos SCBA y de cámaras de apelación PBA (JUBA)
- Consultas cruzadas multifuente en una sola operación
- Verificación de citas jurisprudenciales en escritos aportados

Limitaciones:
- Requiere plan pago (plan Pro)
- No reemplaza la verificación del texto completo del fallo antes de citar
- La cobertura de instancias inferiores PBA está en expansión (ver nota sobre SCBA abajo)

**Fallback:** acceso directo a cada fuente por separado (ver tabla de fuentes primarias al final de este archivo).

---

### 6. SCBA - Jurisprudencia PBA

**Estado:** conector MCP de fuente abierta no disponible. FalloBot (conector 5) cubre SCBA vía JUBA. Ver también fuentes directas abajo.

La Suprema Corte de Justicia de la Provincia de Buenos Aires (SCBA) tiene
jurisprudencia relevante especialmente en materia laboral, civil y administrativo
provincial que no está cubierta por conectores de fuente abierta.

**Expansión de cobertura JUBA (Acuerdo 4011 / Resolución RP 1651/24):**
La SCBA implementó publicidad total de sentencias en etapas:
- Desde marzo 2025: Cámaras de Apelación provinciales y Tribunal de Casación Penal
- Desde junio 2025: juzgados de primera instancia civiles, laborales y contencioso administrativos

Esto aumenta significativamente la cobertura que FalloBot (conector 5) puede acceder vía JUBA en tiempo real.

**Alternativa directa mientras no hay conector MCP de fuente abierta:**
Acceder directamente a https://scba.gov.ar/jurisprudencia/ y pegar el texto
del fallo en la sesión para que el sistema lo procese. Indicar siempre:
sala, fecha, carátula y número de expediente.

**Para quien quiera desarrollar el conector:**
La SCBA tiene acceso programático a JUBA. La contribución de un conector MCP
de fuente abierta sería la de mayor impacto para práctica bonaerense.

---

## Tabla de decisión - qué conector usar

| Necesidad | Conector recomendado | Alternativa |
|---|---|---|
| Verificar texto de una norma nacional | 1 (Ansvar) | InfoLEG directo |
| Verificar texto de una norma provincial PBA | Sin conector MCP | normas.gba.gob.ar directo |
| Buscar jurisprudencia CSJN | 5 (FalloBot, plan Pro) | sj.csjn.gov.ar directo |
| Buscar jurisprudencia CABA / fueros nacionales | 2 (Psflores) | PJN directo |
| Buscar jurisprudencia PBA (SCBA y cámaras) | 5 (FalloBot, plan Pro) | JUBA / SCBA directo |
| Buscar jurisprudencia multifuente simultánea | 5 (FalloBot, plan Pro) | Fuentes por separado |
| Análisis semántico / terminología | 3 (guidobonomini) | - |
| Mejorar búsquedas jurisprudenciales | 4 (Tesauro SAIJ) | SAIJ directo |

**¿Son acumulables?**

Sí, pero con criterio. Las combinaciones útiles son:

- **1 + 2:** para trabajo donde se necesita tanto el texto de la norma como
  jurisprudencia que la interpreta. El flujo recomendado es: primero verificar
  el texto con 1, luego buscar jurisprudencia con 2 usando la terminología
  correcta del texto oficial.

- **4 + 2:** el Tesauro (4) mejora la calidad de las búsquedas de jurisprudencia (2).
  Activar el 4 para normalizar los términos antes de la búsqueda.

- **1 + 3:** el 3 analiza el contrato con glosario argentino; el 1 verifica
  las normas que el 3 cita. El 3 no reemplaza al 1 porque no accede a texto oficial.

**¿Qué pasa si dos conectores dan resultados contradictorios?**

Los conectores 1 y 2 acceden a fuentes primarias oficiales: en caso de contradicción
con cualquier otro conector o con el conocimiento base del sistema, prevalece
la fuente primaria. Los conectores 3 y 4 son instrumentos auxiliares:
si contradicen una fuente primaria, reportar la discrepancia al abogado
con el marcador:

```
[DISCREPANCIA ENTRE FUENTES: el conector [X] indica [A] / la fuente primaria
 indica [B]. Verificar directamente en fuente primaria antes de proceder.]
```

---

## Fuentes primarias oficiales (sin conector MCP)

Estas fuentes no tienen conector MCP disponible actualmente. Acceso directo
por el abogado para verificación manual. Son la fuente de verdad cuando
hay discrepancia con cualquier conector.

| Fuente | URL | Uso principal |
|---|---|---|
| InfoLEG | infoleg.gob.ar | Texto oficial de normas nacionales |
| normas.gba.gob.ar | normas.gba.gob.ar | Texto oficial de normas provinciales PBA: leyes, decretos, decretos-ley, resoluciones, disposiciones, Constitución PBA, códigos provinciales (CPCCBA, CPPBA, CPL PBA, Código Fiscal, etc.). Sistema de Información Normativa y Documental del Gobierno de la Provincia de Buenos Aires. Sin API pública documentada: acceso por búsqueda web o URL directa por número de norma. |
| SAIJ | saij.gob.ar | Jurisprudencia, doctrina, legislación provincial |
| PJN | pjn.gov.ar | Acordadas y jurisprudencia federal |
| CNACAF | cnacaf.gov.ar | Jurisprudencia contencioso administrativo federal y alzada tributaria |
| SCBA | scba.gov.ar | Jurisprudencia PBA - fuente primaria bonaerense |
| JUBA | juba.scba.gov.ar | Sistema de consulta de jurisprudencia PBA (SCBA + cámaras + primera instancia desde 2025) |
| Poder Judicial CABA | buenosaires.gob.ar/jusbaires | Jurisprudencia fuero local CABA |
| PTN | ptn.gov.ar | Dictámenes de la Procuración del Tesoro de la Nación - responsabilidad del Estado y empleo público |
| AAIP | argentina.gob.ar/aaip | Disposiciones de datos personales |
| IGJ | igj.gob.ar | Resoluciones societarias CABA |
| DPPJ | gba.gob.ar/dppj | Resoluciones societarias PBA |
| CNV | cnv.gov.ar | Normas y resoluciones mercado de capitales |
| BCRA | bcra.gov.ar | Normativa cambiaria y financiera |
| COMARB | comarb.gov.ar | Convenio Multilateral - Ingresos Brutos |
| TFN | tfnacional.gov.ar | Jurisprudencia tributaria |

---

## Instalación de conectores MCP

**En Claude Cowork (aplicación de escritorio):**
1. Abrir Claude Cowork
2. Ir a Configuración > MCP Servers
3. Agregar la URL del repositorio del conector
4. Verificar que el conector aparezca activo antes de usarlo

**En Claude Code:**
Agregar la URL del conector al archivo `.mcp.json` del plugin.
Ver instrucciones detalladas en el README del repositorio de cada conector.

Para instrucciones específicas de cada conector, consultar el README
del repositorio correspondiente. Los conectores son proyectos de la comunidad:
si encontrás un error o un conector que dejó de funcionar, reportarlo
en el issue tracker del repositorio correspondiente.

---

## Contribuciones

Si desarrollás un conector para una fuente no cubierta, especialmente SCBA
o jurisprudencia provincial de otras provincias, abrí un PR en este repositorio
para agregar la referencia a esta lista.

---

*Última actualización: mayo 2026*
*Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)*
