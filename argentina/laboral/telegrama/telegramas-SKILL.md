---
name: telegramas-laborales
description: Redacta telegramas laborales y cartas documento en el marco del derecho laboral argentino, con verificación normativa post-reforma (Ley 27.742 + Ley 27.802). Activar ante cualquier mención de telegrama, carta documento, CD, despido, intimación, rechazo, renuncia, certificados art. 80, ius variandi, o cualquier pedido de redacción de pieza postal laboral. No requiere que el usuario mencione "telegrama" explícitamente.
---

# Telegramas laborales

> Parte del repositorio [claude-for-legal-argentina](https://github.com/cristianaboitiz-eng/claude-for-legal-argentina/).  
> Autor: Dr. Cristian Aboitiz · [@abogadoaboitiz](https://x.com/abogadoaboitiz)

---

## Descripción

Redacta telegramas laborales y cartas documento para abogados matriculados en ejercicio de la práctica laboral argentina. El abogado firma y asume responsabilidad profesional por cada pieza. Este skill redacta; el abogado revisa y decide.

---

## Cuándo usar

Activar cuando el usuario pida redactar o preparar:

- Telegramas de despido, rechazo, intimación, notificación o renuncia
- Cartas documento laborales de cualquier tipo
- Cualquier pieza fehaciente laboral, aunque no use la palabra "telegrama"

No activar para análisis estratégico, liquidaciones o escritos judiciales — esos corresponden a otros skills del plugin laboral.

---

## Proceso

### Paso 1 - Recolección de datos

Antes de redactar, presentar al usuario:

---
Para redactar el telegrama necesito algunos datos. Tiene dos opciones:

OPCION A: Me proporciona todos los datos ahora y redacto el borrador completo.

OPCION B: Me indica solo el tipo de telegrama y redacto con espacios en blanco marcados como [DATO A COMPLETAR] para que el abogado los complete antes del envío.

Antes de elegir, indíqueme: ¿el telegrama lo envía el trabajador o el empleador? Eso condiciona la estrategia y el tono desde el inicio.

Si elige la Opción A, necesito:
- Quién envía: trabajador o empleador (y nombre completo con su carácter)
- Tipo de telegrama (despido, intimación, rechazo, renuncia, notificación, etc.)
- Nombre completo y domicilio del destinatario
- Fecha exacta del telegrama
- Fecha de ingreso del trabajador
- **Fecha del acto extintivo o del hecho generador** (determina el régimen normativo aplicable)
- Categoría laboral y CCT aplicable, si corresponde
- Remuneración mensual efectivamente percibida y remuneración registrada, si difieren
- Hechos concretos a narrar, afirmar o negar, con fechas
- Número de telegrama anterior, si este es una respuesta o continuación
- Cualquier otro dato relevante según el tipo de telegrama

---

### Paso 2 - Verificación normativa

Antes de incluir cualquier cita legal, leer `reglas-normativas.md` y aplicar las reglas en orden.

- ¿La norma está en las Reglas 1 a 10? Aplicar esa regla directamente.
- ¿La norma no está listada? Aplicar Regla 11: buscar en InfoLeg, luego en Boletín Oficial. Incluir alerta si no se confirma vigencia.

Este paso no es opcional. Si se omite, el telegrama puede citar normas derogadas.

### Paso 3 - Consultar tipos de telegrama y modelos

Antes de redactar, leer `tipos-de-telegrama.md` y ubicar el grupo correspondiente. Luego leer el bloque de modelos que corresponda:

| Materia | Archivo |
|---|---|
| Registro de la relación laboral | `modelos/bloque-01-registro.md` |
| Estabilidad y despido | `modelos/bloque-02-estabilidad-despido.md` |
| Pago de salarios y remuneraciones | `modelos/bloque-03-salarios.md` |
| Modificaciones contractuales / ius variandi | `modelos/bloque-04-ius-variandi.md` |
| Renuncia | `modelos/bloque-05-renuncia.md` |
| Vacaciones y licencias | `modelos/bloque-06-vacaciones-licencias.md` |
| Seguridad y salud laboral / hostigamiento y discriminación | `modelos/bloque-07-salud-hostigamiento.md` |
| Industria de la construcción | `modelos/bloque-08-construccion.md` |

---

## Formato del telegrama

**Encabezado:** solo lugar y fecha. El nombre del remitente y el destinatario se consignan en el formulario postal del correo, no en el cuerpo del texto.

**Cuerpo:** comienza inmediatamente con el acto jurídico principal.
- Intimaciones: la primera palabra es "Intimo" - sin excepción.
- Rechazos, renuncias, notificaciones: comenzar con la fórmula que corresponda al acto.

Sin negritas, cursivas, asteriscos, bullets, hashtags, corchetes decorativos, barras ni emojis. Solo texto plano. Punto, coma, punto y coma, dos puntos y paréntesis para referencias normativas.

Las normas se citan exclusivamente por número y denominación. Prohibido transcribir o parafrasear el contenido de artículos en el cuerpo del telegrama.

Cerrar siempre con: Queda Ud. debidamente notificado/a.

---

## Formato de salida: dos bloques

### Bloque 1. Texto del telegrama
Texto completo en prosa continua, listo para copiar y enviar.

### Bloque 2. Referencias legales para verificación

Tabla con cuatro columnas:

| Norma citada | Artículo | Materia | Link oficial |
|---|---|---|---|

Links a usar:
- LCT (Ley 20.744): https://servicios.infoleg.gob.ar/infolegInternet/buscar.do
- Otras leyes: link directo obtenido durante verificación, o buscador general si no se obtuvo.
- CCT: https://www.argentina.gob.ar/trabajo/relacioneslaborales/negociacioncolectiva
- Normas sin vigencia confirmada: escribir "Ver alerta en este Bloque."

Al pie del Bloque 2, incluir siempre:

> ADVERTENCIA: Verificar vigencia antes del envío. La LCT y sus normas complementarias han sido modificadas por la Ley de Bases N° 27.742 (julio 2024) y la Ley de Modernización Laboral N° 27.802 (marzo 2026). Los links dirigen a fuentes oficiales. Algunas disposiciones tienen vigencia diferida. El abogado firmante asume responsabilidad profesional por el contenido y la vigencia de las normas citadas.

---

## Restricciones absolutas

- No inventar hechos no proporcionados por el usuario.
- No citar artículos sin verificar que correspondan al tipo de telegrama y a la fecha del hecho generador.
- No aplicar normas derogadas a hechos ocurridos con posterioridad a su derogación.
- No prometer remedios procesales que no existan en el texto legal vigente.
- No usar formato enriquecido en el Bloque 1.

---

## Racionalizaciones comunes

Atajos que este skill tiende a tomar. Cada uno tiene un rebuttal explícito.

| Racionalización | Realidad |
|---|---|
| "El CCT no está disponible pero la norma es estándar" | Sin CCT aportado el tope del art. 245 no puede calcularse. Emitir `[VERIFICAR CCT APLICABLE]` siempre. El tope no es estándar: varía por actividad. |
| "El abogado pidió citar el art. 8 Ley 24.013" | La instrucción del abogado no deroga la norma. Si el acto extintivo es post-9/7/2024, informar la derogación y no citar. El abogado decide; el skill informa. |
| "La fecha del hecho generador no fue indicada, pero parece reciente" | Asumir régimen sin fecha verificada es el error más frecuente en este skill. Solicitar la fecha antes de redactar; el tramo temporal del art. 245 y los agravantes derogados dependen de ella. |
| "El modelo del bloque cubre el caso, no hace falta leer reglas-normativas.md" | Los modelos tienen notas de revisión, no verificación normativa automática. El Paso 2 es obligatorio siempre. Los modelos y las reglas son complementarios. |
| "La retención de tareas siempre protege al trabajador" | El art. 1031 CCCN puede ser interpretado como abandono por el empleador. Evaluar el caso concreto antes de incluirla; no es una fórmula automática. |
| "El despido indirecto es siempre viable como siguiente paso" | Requiere injuria grave y contemporánea. Invocar despido indirecto por causa antigua sin intimación previa reciente es improcedente. |
| "Art. 216 LCT permite pedir la reinstalación cautelar" | Art. 216 LCT fue derogado por Ley 27.802 con vigencia desde el 6/3/2026. No existe esa vía para hechos posteriores a esa fecha. |

---

## Señales de alerta

Indicadores de que el borrador está mal antes de entregarlo:

- Citar arts. 8, 9, 10 o 15 de la Ley 24.013 sin haber verificado que el acto extintivo es anterior al 9/7/2024
- Citar arts. 1 o 2 de la Ley 25.323 sin haber verificado que el acto extintivo es anterior al 9/7/2024
- Prometer acción sumarísima de restablecimiento para hechos posteriores al 6/3/2026 (suprimida, art. 66 LCT)
- Mencionar "libro especial del art. 52" en cualquier pieza
- Calcular o mencionar base del art. 245 sin haber identificado el tramo temporal del acto extintivo
- Entregar el Bloque 1 sin haber leído el bloque de modelos correspondiente
- Incluir apercibimiento de multas derogadas aunque el abogado lo haya pedido
- Usar "AFIP" en lugar de "ARCA" en cualquier referencia administrativa

---

## Correcciones

Si el usuario señala errores:
1. Reconocer el error con precisión. Sin frases genéricas.
2. Entregar solo el párrafo o sección corregida, no el telegrama entero salvo error estructural.
3. Indicar al pie: "REGLA INCORPORADA PARA ESTA SESION: [descripción de la regla nueva]."
4. Preguntar si la corrección resuelve el problema antes de dar el borrador por cerrado.

---

## Verificación al cierre

Antes de entregar el borrador final:

- [ ] Fecha del acto extintivo o hecho generador identificada
- [ ] Régimen normativo determinado según el tramo temporal (pre-30/12/2023 / 30/12/2023-5/3/2026 / desde 6/3/2026)
- [ ] `reglas-normativas.md` consultado (Paso 2 ejecutado)
- [ ] Bloque de modelos correspondiente consultado (Paso 3 ejecutado)
- [ ] Ninguna norma derogada citada en el cuerpo del telegrama
- [ ] Ningún remedio procesal inexistente prometido
- [ ] Bloque 1 en texto plano sin formato enriquecido
- [ ] Bloque 2 con tabla de referencias completa y advertencia al pie
- [ ] CCT indicado o marcador `[VERIFICAR CCT APLICABLE]` presente donde corresponde

---

*Ultima actualizacion: mayo 2026*  
*Normativa base: LCT (Ley 20.744 reformada por DNU 70/2023 + Ley 27.742 + Ley 27.802), Ley 24.013, Ley 25.323, Ley 25.345*
