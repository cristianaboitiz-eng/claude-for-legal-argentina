# Higiene de citas y grounding normativo argentino

El objetivo no es que el modelo "suene juridico". El objetivo es que el borrador
no fabrique autoridad. Cuando falte respaldo, debe detener la cita, marcar el
problema y permitir que el abogado decida.

## Principios

1. No citar fallos, expedientes, salas, fechas ni caratulas sin fuente verificable.
2. No completar articulos, incisos o numeros de ley desde memoria si la vigencia es
   material para la conclusion.
3. No convertir doctrina administrativa en jurisprudencia.
4. No convertir publicaciones de boletin oficial en texto consolidado sin verificar.
5. No importar institutos de common law si hay categoria argentina especifica.
6. No ocultar incertidumbre: marcarla con motivo concreto.

## Marcadores obligatorios

Usar estos marcadores cuando corresponda:

```text
[VERIFICAR VIGENCIA: norma o articulo no recuperado en fuente oficial]
[VERIFICAR FUENTE: jurisprudencia no recuperada]
[INSERTAR FALLO VERIFICADO: doctrina requerida]
[VACIO PROBATORIO: hecho relevante no acreditado]
[documento cliente: fuente aportada por el usuario]
[Inferencia razonada: conclusion a partir de hechos disponibles]
```

## Normas

Antes de usar una norma como soporte fuerte:

- identificar numero, nombre, articulo e inciso;
- verificar si es nacional, provincial, municipal o regulatoria;
- verificar fecha, modificaciones y autoridad emisora;
- indicar si la fuente es InfoLEG, SAIJ, BO, organismo regulador o documento cliente.

Si se trata de BCRA, AFIP/ARCA, CNV, UIF, tasas, umbrales, salarios, montos,
plazos administrativos o valores actualizables, tratarla como fuente volatil.

## Jurisprudencia

Una cita jurisprudencial usable debe tener, segun disponibilidad:

- tribunal;
- sala o composicion cuando sea relevante;
- fecha;
- caratula;
- identificador oficial o base verificable;
- fuente;
- doctrina efectivamente vinculada al issue.

Si la cita no esta recuperada, no redactar como si existiera. Usar:

```text
[INSERTAR FALLO VERIFICADO: doctrina requerida sobre ...]
```

## Contratos y documentos del cliente

Cuando el soporte proviene del documento aportado:

- citar clausula, pagina, seccion o fragmento;
- separar hecho documental de conclusion juridica;
- no asumir anexos, firmas, poderes, aprobaciones o vigencia si no fueron aportados.

## Respuesta ante falta de fuente

En lugar de completar silenciosamente, devolver:

1. conclusion preliminar;
2. fuente faltante;
3. por que importa;
4. como verificarla;
5. redaccion segura mientras tanto.

## Redaccion segura

Preferir:

```text
Con la informacion disponible, el argumento es plausible, pero requiere verificar
el texto vigente de [norma] y al menos un precedente aplicable de [tribunal].
```

Evitar:

```text
La jurisprudencia ha dicho reiteradamente...
```

salvo que la jurisprudencia haya sido efectivamente recuperada o aportada.

## Frontera publica / privada

Estas reglas pueden compartirse publicamente. No contienen corpus, estrategia de
cliente ni logica propietaria. Los datasets reales, criterios de calibracion por
firma, flujos internos y resultados de evaluacion pertenecen a cada organizacion
o producto que los opere.
