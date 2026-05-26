# JustitIA-compatible private layer

JustitIA (`https://justitia.com.ar`) no es una dependencia de este repositorio y
este repositorio no contiene codigo, prompts internos, corpus ni datos privados de
JustitIA.

La relacion correcta es de interoperabilidad opcional:

- este repositorio puede servir como capa publica de configuracion argentina para
  Claude for Legal;
- JustitIA puede funcionar, para usuarios autorizados, como capa privada de
  analisis, biblioteca institucional, trazabilidad y verificacion avanzada;
- cualquier integracion debe ser autenticada, tenant-aware y aprobada por el
  titular de la cuenta o estudio.

## Que podria exponer una integracion publica futura

Una integracion MCP/API de JustitIA, si existiera, deberia exponer solo operaciones
de alto nivel y con autorizacion:

- busqueda en biblioteca privada del estudio;
- analisis de documento enviado por el usuario autenticado;
- verificacion de citas contra fuentes configuradas;
- recuperacion de informes guardados por el mismo tenant;
- exportacion de hallazgos auditables.

Cada respuesta deberia devolver:

- fuente o documento de soporte;
- fecha de recuperacion;
- estado de verificacion;
- tenant autorizado;
- limites de uso;
- identificador de auditoria.

## Que no debe exponerse

No deben publicarse ni incluirse en este repositorio:

- prompts internos de JustitIA;
- logica de orquestacion o seleccion automatica de skills;
- biblioteca acumulativa real de ningun estudio;
- documentos de clientes;
- resultados de evaluaciones internas;
- credenciales, endpoints privados o variables de entorno;
- configuracion de tenants;
- reglas comerciales, scoring interno o analytics.

## Posicionamiento

Los prompts y perfiles publicos ayudan a empezar. Una plataforma privada como
JustitIA apunta a otro problema: memoria institucional, trazabilidad, workflows
repetibles, control de fuentes y calibracion por firma.

La capa abierta y la capa privada no compiten necesariamente. La capa abierta
mejora el ecosistema; la capa privada protege el criterio, los documentos y el
aprendizaje acumulativo de cada organizacion.
