# claude-for-legal · Adaptación Argentina

Fork de [anthropics/claude-for-legal](https://github.com/anthropics/claude-for-legal) configurado para práctica legal argentina.

El repositorio original cubre 12 plugins y más de 80 agentes. Está construido íntegramente sobre derecho norteamericano: Delaware, Nueva York, common law, at-will employment, GDPR. Este fork agrega una capa de configuración argentina sin modificar los plugins originales.

---

## Estructura

```
argentina/
  CLAUDE.md                   # Perfil de práctica general (reemplaza al original)
  administrativo-CLAUDE.md    # Perfil para derecho administrativo
  civil-CLAUDE.md             # Perfil para derecho civil (CCCN)
  concursos-CLAUDE.md         # Perfil para concursos y quiebras (LCQ)
  familia-CLAUDE.md           # Perfil para derecho de familia
  laboral-CLAUDE.md           # Perfil para derecho del trabajo (LCT)
  penal-CLAUDE.md             # Perfil para derecho penal
  societario-CLAUDE.md        # Perfil para derecho societario (LGS)
  tributario-CLAUDE.md        # Perfil para derecho tributario
  red-flags-contratos.md      # Lista de alertas para revisión de contratos
  fuentes.md                  # Conectores a bases de datos normativas locales
  fuentes-oficiales-matrix.md # Matriz de fuentes oficiales y limites de uso
  higiene-citas.md            # Reglas para no fabricar citas ni vigencia normativa
  justitia-compatible.md      # Frontera de interoperabilidad con JustitIA
  casos-verificacion/         # Casos sinteticos para testear comportamiento
```

Los plugins originales quedan intactos. Todo el material argentino vive en la carpeta `argentina/`.

---

## Qué hace este fork

**Configura el sistema para operar bajo:**
- CCCN (Ley 26.994) para contratos y obligaciones
- LCT (Ley 20.744) y modificatorias para materia laboral
- Ley 25.326 y disposiciones AAIP para privacidad y datos personales
- CPCCN para fueros nacionales y federales / CPCCBA para PBA
- LDC (Ley 24.240) para contratos de consumo
- LGS para societario

**Reemplaza la lógica de common law en tres plugins críticos:**
- `commercial-legal` - análisis de contratos bajo CCCN, no bajo consideration/indemnification caps
- `employment-legal` - modelo de despido con indemnización obligatoria (art. 245 LCT), no at-will
- `privacy-legal` - habeas data bajo Ley 25.326, no GDPR/DSAR

**Agrega red flags específicas del derecho argentino** para revisión automática de contratos.

**Agrega una capa publica de verificacion**:
- matriz argentina de fuentes oficiales y conectores;
- reglas de higiene de citas y grounding normativo;
- casos sinteticos de verificacion para probar que el asistente no inventa fallos,
  plazos ni vigencia normativa;
- nota de interoperabilidad con JustitIA sin exponer codigo, prompts internos,
  corpus privado ni datos de clientes.

---

## Antes de empezar

Necesitás:
- Cuenta de Claude.ai con plan Pro
- Claude Cowork (aplicación de escritorio, descargable desde claude.ai)
- Cuenta de GitHub gratuita

No necesitás saber programar para la configuración base. Para conectar fuentes normativas locales (fase 2), vas a necesitar ayuda técnica.

---

## Instalación

### Paso 1: Fork

Hacé click en "Fork" arriba a la derecha. Eso crea una copia en tu cuenta. No descargues el ZIP: el fork te permite incorporar actualizaciones del repositorio original sin pisar tu configuración local.

### Paso 2: Perfil de práctica

Cada plugin tiene un `CLAUDE.md` que el sistema lee antes de hacer cualquier análisis. El archivo `argentina/CLAUDE.md` de este fork reemplaza ese perfil con configuración argentina.

La primera vez que usás un plugin, el sistema corre una entrevista de configuración inicial. Cuando te pida el perfil de práctica, cargá el contenido de `argentina/CLAUDE.md` como punto de partida y completá con los datos de tu firma (fueros habituales, CCT de tus clientes, documentos semilla propios).

### Paso 3: Plugins críticos

Para los tres plugins que requieren reescritura completa de lógica, el `CLAUDE.md` argentino incluye instrucciones específicas por sección. Ver el archivo para el detalle.

---

## Fuentes normativas (fase 2)

Conectores de la comunidad que apuntan directamente a las fuentes oficiales argentinas:

| Repositorio | Fuente | Función |
|---|---|---|
| [Ansvar-Systems/argentine-law-mcp](https://github.com/Ansvar-Systems/argentine-law-mcp) | InfoLEG / SAIJ | Texto literal de normas nacionales |
| [Psflores/Legal-MCP-Server-](https://github.com/Psflores/Legal-MCP-Server-) | PJN / CABA | Jurisprudencia fueros nacionales |
| [guidobonomini/argentina-law-mcp-server](https://github.com/guidobonomini/argentina-law-mcp-server) | Praxis local | Análisis semántico, glosario judicial |
| [datos-justicia-argentina/Tesauro-Saij](https://github.com/datos-justicia-argentina/Tesauro-Saij-de-Derecho-Argentino) | SAIJ | Vocabulario controlado para búsqueda jurídica |
| BOPBA MCP | Boletin Oficial PBA | Publicaciones oficiales bonaerenses |
| Normativa PBA MCP | Normativa provincial | Legislacion bonaerense |
| PTN MCP | Procuracion del Tesoro | Dictamenes administrativos |
| JUBA MCP | Jurisprudencia PBA | Busqueda de precedentes bonaerenses |

No son necesarios para empezar. Los plugins funcionan con el perfil de práctica como única configuración. Los conectores son la segunda capa: permiten que el sistema consulte InfoLEG automáticamente antes de analizar una norma.

Ver tambien `argentina/fuentes-oficiales-matrix.md` para distinguir fuente oficial,
publicacion, doctrina administrativa, jurisprudencia, documento cliente e inferencia.

---

## Lo que podés hacer desde el día uno

- Revisar contratos contra la lista de red flags argentina, con referencia a norma aplicable
- Redactar borradores de contratos tipo (NDA, prestación de servicios, compraventa) con CCCN como base
- Preparar briefings de due diligence para operaciones societarias o M&A, con checklist adaptado a LGS y normativa IGJ/DPPJ
- Monitorear vencimientos de contratos
- Armar matrices de riesgo para compliance bajo Ley 25.326
- Auditar citas dudosas y reemplazar autoridad no verificada por marcadores seguros
- Correr casos sinteticos de verificacion antes de confiar en un perfil o conector

---

## Lo que no reemplaza

El criterio del abogado. La responsabilidad profesional. La firma.

Todo output del sistema es un borrador. No sabe qué pasó en la negociación, no conoce la relación con la contraparte, no tiene el expediente completo. Acelera la parte mecánica. Las decisiones son siempre del abogado.

Este fork tampoco reemplaza una plataforma privada de produccion. Los perfiles,
matrices y casos publicos son una capa abierta de referencia. Bibliotecas
institucionales, documentos reales, trazabilidad por tenant, calibracion por firma,
prompts internos, corpus privados y workflows productivos deben permanecer en
sistemas autenticados.

---

## Contribuciones

Este repositorio es una vitrina de referencia, no un proyecto con mantenimiento activo. Si encontrás un error normativo, abrí un issue con la norma correcta y la fuente. Si querés adaptar el perfil para otra jurisdicción (Uruguay, Chile, Colombia), forkéalo y avisame.

---

## Autor

Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)  
Abogado (CPACF) · CABA y GBA · Legal tech & IA aplicada a práctica jurídica argentina
