# Fuentes normativas argentinas · Conectores MCP

Repositorios de la comunidad que conectan claude-for-legal directamente con las fuentes oficiales argentinas. Reemplazan los conectores originales del repositorio (Westlaw, CourtListener, Everlaw) para práctica local.

No son necesarios para empezar. Los plugins funcionan con el perfil de práctica (`CLAUDE.md`) como única configuración. Los conectores son la segunda capa: permiten que el sistema consulte fuentes primarias automáticamente sin que el abogado tenga que pegar el texto de la norma en la sesión.

---

## Conectores disponibles

### 1. Ansvar-Systems/argentine-law-mcp

**Repositorio:** https://github.com/Ansvar-Systems/argentine-law-mcp
**Fuentes:** InfoLEG · SAIJ
**Función:** Devuelve el texto literal de normas nacionales argentinas sin pasar por ningún modelo de lenguaje. Ideal para verificación de vigencia y texto oficial de artículos específicos.

Casos de uso:
- Verificar texto actual de un artículo del CCCN o la LCT
- Confirmar si una norma fue modificada o derogada
- Obtener el texto de una ley especial sin buscarlo manualmente

### 2. Psflores/Legal-MCP-Server-

**Repositorio:** https://github.com/Psflores/Legal-MCP-Server-
**Fuentes:** Poder Judicial de la Nación · Justicia CABA
**Función:** Búsqueda de jurisprudencia de CABA y fueros nacionales.

Casos de uso:
- Buscar fallos por doctrina antes de citar en un escrito
- Verificar criterio de la sala en una materia específica
- Rastrear evolución jurisprudencial sobre un instituto

### 3. guidobonomini/argentina-law-mcp-server

**Repositorio:** https://github.com/guidobonomini/argentina-law-mcp-server
**Función:** Análisis semántico de documentos legales, glosario judicial argentino, módulos de detección de riesgos según praxis local.

Casos de uso:
- Análisis de contratos con terminología jurídica argentina nativa
- Detección de riesgos calibrada para jurisprudencia local
- Consulta de glosario cuando el sistema genera términos de common law

### 4. datos-justicia-argentina/Tesauro-Saij-de-Derecho-Argentino

**Repositorio:** https://github.com/datos-justicia-argentina/Tesauro-Saij-de-Derecho-Argentino
**Fuente:** SAIJ
**Función:** Vocabulario controlado para búsqueda jurídica. Mapea sinónimos, términos preferidos y jerarquías conceptuales del derecho argentino.

Casos de uso:
- Mejorar la precisión de búsquedas jurisprudenciales
- Evitar que el sistema use términos de common law cuando existe equivalente argentino
- Consistencia terminológica en documentos largos

### 5. BOPBA MCP

**Fuente:** Boletin Oficial de la Provincia de Buenos Aires
**Funcion:** Verificacion de publicaciones oficiales bonaerenses.

Casos de uso:
- Confirmar publicacion de leyes, decretos, resoluciones y actos provinciales
- Verificar fecha de publicacion antes de analizar vigencia
- Buscar actos administrativos provinciales recientes

Limite: publicacion oficial no equivale necesariamente a texto consolidado vigente.

### 6. Normativa PBA MCP

**Fuente:** Legislacion y normativa de Provincia de Buenos Aires
**Funcion:** Busqueda de normativa provincial.

Casos de uso:
- Verificar normativa PBA por tema
- Cruzar una publicacion BOPBA con texto normativo disponible
- Evitar aplicar CPCCN o normativa nacional cuando corresponde PBA

### 7. PTN MCP

**Fuente:** Procuracion del Tesoro de la Nacion
**Funcion:** Recuperacion de dictamenes administrativos.

Casos de uso:
- Buscar doctrina administrativa nacional sobre procedimiento, contrataciones,
  empleo publico o responsabilidad estatal
- Separar criterio administrativo de jurisprudencia judicial
- Ubicar lineas doctrinarias utiles para escritos administrativos

Limite: un dictamen PTN no es una sentencia ni reemplaza la norma aplicable.

### 8. JUBA MCP

**Fuente:** Jurisprudencia bonaerense
**Funcion:** Busqueda de precedentes de tribunales PBA.

Casos de uso:
- Verificar doctrina SCBA o camaras provinciales
- Evitar extrapolar CNCom/CNAT a Provincia de Buenos Aires
- Preparar busquedas por departamento judicial o materia

---

## Fuentes primarias oficiales (sin conector MCP)

Estas fuentes no tienen conector MCP disponible actualmente. Se acceden directamente por el abogado para verificación manual.

| Fuente | URL | Uso |
|---|---|---|
| InfoLEG | infoleg.gob.ar | Texto oficial de normas nacionales |
| SAIJ | saij.gob.ar | Jurisprudencia, doctrina, legislación provincial |
| PJN | pjn.gov.ar | Acordadas, jurisprudencia federal |
| SCBA | scba.gov.ar | Jurisprudencia PBA |
| AAIP | argentina.gob.ar/aaip | Disposiciones de datos personales |
| IGJ | igj.gob.ar | Resoluciones societarias CABA |
| CNV | cnv.gov.ar | Normas y resoluciones mercado de capitales |
| BCRA | bcra.gob.ar | Comunicaciones y normativa financiera/cambiaria |
| UIF | argentina.gob.ar/uif | Resoluciones y criterios PLA/FT |
| PTN | ptn.gob.ar | Dictamenes administrativos nacionales |
| BOPBA | gba.gob.ar/boletin_oficial | Publicaciones oficiales PBA |
| JUBA | juba.scba.gov.ar | Jurisprudencia bonaerense |

---

## Instalación de conectores MCP

Los conectores se instalan en Claude Cowork (aplicación de escritorio). El proceso general:

1. Abrir Claude Cowork
2. Ir a Configuración > MCP Servers
3. Agregar el repositorio del conector
4. Verificar que el conector aparezca activo antes de usarlo

Para instrucciones específicas de cada conector, consultar el README del repositorio correspondiente.

Ver `fuentes-oficiales-matrix.md` para la matriz completa de procedencia,
volatilidad y limites de uso.

---

*Última actualización: mayo 2026*
