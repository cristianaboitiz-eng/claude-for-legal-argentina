# Casos sinteticos de verificacion

Casos publicos, ficticios y controlados para verificar que un asistente juridico
argentino detecta vicios basicos sin fabricar autoridad. No incluyen documentos
reales ni datos de clientes.

Cada caso debe tener:

1. pieza o consigna;
2. rubrica de evaluacion;
3. salida esperada;
4. fuentes o marcadores de fuente faltante;
5. criterios de fallo.

## Casos incluidos

- `contrato-consumo-clausula-abusiva.md`: contrato de adhesion con prorroga de
  jurisdiccion y renuncias invalidas.
- `plazo-procesal-fuente-incompleta.md`: consulta de plazo sin fecha/calendario
  suficiente.
- `cita-jurisprudencial-no-verificada.md`: borrador con fallo aparente pero sin
  fuente verificable.

## Que debe medir

- si el sistema frena una cita no verificada;
- si distingue norma, jurisprudencia, documento cliente e inferencia;
- si pide datos faltantes antes de calcular plazos o montos;
- si evita categorias de common law cuando corresponde derecho argentino;
- si propone una salida util sin ocultar incertidumbre.

## Que no debe medir

- velocidad;
- estilo literario;
- capacidad de persuadir sin fuente;
- reproduccion de estrategias reales de clientes;
- acceso a corpus privado.
