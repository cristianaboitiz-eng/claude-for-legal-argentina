# Matriz argentina de fuentes oficiales

Esta matriz ayuda a decidir donde verificar derecho argentino antes de citar una
norma, fallo, dictamen o criterio administrativo. No reemplaza el criterio del
abogado ni convierte una fuente secundaria en autoridad primaria.

## Regla general

1. Primero buscar fuente oficial o documento aportado por el abogado.
2. Si la fuente no aparece, no inventar la cita.
3. Si el sistema conoce el instituto pero no verifico vigencia o texto literal,
   usar marcador explicito: `[VERIFICAR VIGENCIA: motivo]`.
4. Distinguir siempre: norma vigente, publicacion oficial, jurisprudencia,
   doctrina administrativa, doctrina privada, documento del cliente e inferencia.

## Fuentes nacionales

| Fuente | Materia | Uso correcto | Limite |
|---|---|---|---|
| InfoLEG | Normativa nacional | Texto de leyes, decretos y normas nacionales | No siempre resuelve reglamentacion, vigencia practica o criterios administrativos |
| SAIJ | Normativa, jurisprudencia, doctrina | Busqueda juridica amplia, doctrina y fallos disponibles | No toda jurisprudencia argentina esta completa ni necesariamente consolidada |
| Boletin Oficial de la Republica Argentina | Publicacion oficial | Confirmar publicacion, fechas, resoluciones recientes | Publicacion no equivale siempre a texto consolidado |
| CSJN | Jurisprudencia Corte | Fallos, acordadas y decisiones de maximo tribunal | Exigir identificador y texto verificable |
| PJN | Fueros nacionales/federales | Jurisprudencia y gestion judicial disponible | Cobertura variable por fuero/sala |
| PTN | Dictamenes administrativos | Doctrina administrativa nacional | No es jurisprudencia judicial ni norma general |

## Fuentes provinciales y locales

| Fuente | Materia | Uso correcto | Limite |
|---|---|---|---|
| SCBA / JUBA | Jurisprudencia PBA | Fallos de tribunales bonaerenses | No extrapolar automaticamente a CABA/federal |
| BOPBA | Publicaciones oficiales PBA | Leyes, decretos, resoluciones y actos publicados | Publicacion no sustituye texto consolidado ni vigencia actual |
| Normativa PBA | Legislacion bonaerense | Texto provincial y municipal disponible | Verificar fuente concreta y fecha |
| Justicia CABA | Jurisprudencia CABA | Fallos y resoluciones locales | No confundir con fueros nacionales con asiento en CABA |
| Boletines provinciales/municipales | Normativa local | Ordenanzas, resoluciones, actos administrativos | Cobertura y buscabilidad variables |

## Reguladores y organismos

| Fuente | Materia | Uso correcto | Limite |
|---|---|---|---|
| AAIP | Datos personales | Disposiciones, guias y sanciones Ley 25.326 | No importar vocabulario GDPR sin aclarar regimen |
| IGJ | Sociedades CABA | Resoluciones generales, sociedades, fiscalizacion | No aplica automaticamente a DPPJ/PBA u otras jurisdicciones |
| DPPJ PBA | Sociedades PBA | Sociedades inscriptas en Provincia de Buenos Aires | Reglas y practica distintas a IGJ |
| CNV | Mercado de capitales | Normas CNV, emisoras, oferta publica | Verificar texto ordenado vigente |
| BCRA | Cambios, pagos, bancos | Comunicaciones A, B, circulares y normativa financiera | Alta volatilidad; requiere verificacion de fecha y vigencia |
| UIF | Lavado y sujetos obligados | Resoluciones, guias, sanciones | Verificar categoria de sujeto obligado y fecha |
| AFIP/ARCA | Tributario y seguridad social | Resoluciones generales, aplicativos, criterios | Montos, alicuotas y vencimientos son volatiles |
| CNDC | Defensa de la competencia | Concentraciones, conductas, guias | Verificar umbrales vigentes y acto administrativo aplicable |

## Conectores MCP de comunidad

Los conectores MCP pueden acelerar la recuperacion de fuentes, pero cada resultado
debe conservar procedencia, fecha de recuperacion e identificador citables.

| Conector | Fuente principal | Uso sugerido |
|---|---|---|
| InfoLEG / SAIJ MCP | Normativa nacional y busqueda juridica | Recuperar texto literal antes de analizar |
| SAIJ MCP con OCR | SAIJ y PDFs escaneados | Recuperar documentos cuando la fuente este en PDF no estructurado |
| BOPBA MCP | Boletin Oficial PBA | Verificar publicaciones bonaerenses |
| Normativa PBA MCP | Legislacion PBA | Buscar normativa provincial |
| PTN MCP | Dictamenes PTN | Revisar doctrina administrativa nacional |
| JUBA MCP | Jurisprudencia PBA | Buscar precedentes bonaerenses |
| Tesauro SAIJ | Vocabulario juridico | Expandir busquedas y evitar terminos de common law |

## Taxonomia de procedencia recomendada

- `[Verificado]`: fuente oficial o documento del cliente recuperado en la sesion.
- `[Estable]`: norma estructural de baja volatilidad, identificada con seguridad,
  aunque conviene verificar texto antes de presentar.
- `[documento cliente]`: hecho, clausula, resolucion o prueba aportada por el usuario.
- `[Inferencia razonada]`: conclusion derivada de hechos y normas disponibles.
- `[VERIFICAR FUENTE]`: cita, vigencia, jurisprudencia o criterio no recuperado.
- `[VACIO PROBATORIO]`: hecho relevante no acreditado.

## Criterio de uso

Esta matriz es deliberadamente publica. Lo que no debe incluirse aqui:

- documentos reales de clientes;
- prompts internos de productos comerciales;
- corpus privado;
- claves, endpoints privados o tenants;
- evaluaciones internas de rendimiento;
- reglas de orquestacion propietarias.
