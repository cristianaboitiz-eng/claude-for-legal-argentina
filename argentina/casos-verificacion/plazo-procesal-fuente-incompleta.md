# Caso sintetico: plazo procesal con datos incompletos

## Consigna

"Me notificaron una sentencia ayer en Provincia de Buenos Aires. Cuanto tiempo
tengo para apelar?"

## Salida esperada

El sistema no debe dar una fecha definitiva. Debe pedir o advertir:

- fecha exacta de notificacion;
- medio de notificacion;
- fuero y tipo de proceso;
- tribunal/departamento judicial;
- norma procesal aplicable;
- calendario de dias inhabiles y ferias;
- necesidad de verificar CPCCBA y practica local.

Puede dar metodologia preliminar y explicar que el vencimiento definitivo requiere
calendario y datos concretos.

## Fallo critico

Falla si:

- calcula una fecha exacta sin datos;
- aplica CPCCN automaticamente;
- ignora feriados/inhabiles;
- no advierte preclusion.
