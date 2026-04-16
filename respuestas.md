# Respuestas — Práctica Final: Análisis y Modelado de Datos

> Rellena cada pregunta con tu respuesta. Cuando se pida un valor numérico, incluye también una breve explicación de lo que significa.

---

## Ejercicio 1 — Análisis Estadístico Descriptivo
---
Añade aqui tu descripción y analisis:

--- 

**Pregunta 1.1** — ¿De qué fuente proviene el dataset y cuál es la variable objetivo (target)? ¿Por qué tiene sentido hacer regresión sobre ella?

> El dataset utilizado es de un sistema ERP de gestión de ventas, recoge informacion sobre perdido, clientes, productos y envios.
La variable objetivo es MARGEN_DOLARES, representando el beneficio obtenido en cada venta.

Tiene sentido aplicar regresion a esta variable por que es numerica continmua y depende de multiples factores como el precio del producto, 
lso descuentos aplicados, la cantidad vendidad o el tipo de transaccion. Esto permite analizar que variables influyen en el margen y predecir su valor en futuras transacciones

**Pregunta 1.2** — ¿Qué distribución tienen las principales variables numéricas y has encontrado outliers? Indica en qué variables y qué has decidido hacer con ellos.

> Las variables numericas presentan distribuciones asimetricas, en particular la variable objetivo MARGEN_DOLARES muestra la asimetria fuerte hacia la izquierda(asimetria negativa), 
con una concentracion de valores cercanos a cero y una cola larga hacia valores negativos, que indica numerosas ventas con perdidas significativas.
![alt text](image.png)

> En cuanto a los outliers, se detectaron principalmente en variables relacionadas con el margen y los descuentos
> - MARGEN_DOLARES (~10.5% de outliers)
> - MARGEN_PORCENTAJE (~9.6%)
> - DESCUENTO (~4.38%)
Se identificaron mediante el metodo del rango intercuartilico -> IQR
![alt text](image-1.png)

> No se eliminaron los valores atípicos, ya que representan situaciones reales del negocio (por ejemplo, ventas con grandes descuentos o pérdidas), 
por lo que forman parte de la variabilidad natural del dataset.



**Pregunta 1.3** — ¿Qué tres variables numéricas tienen mayor correlación (en valor absoluto) con la variable objetivo? Indica los coeficientes.

> Las tres variable snuméricas con mayor correlación (en valor absoluto) respecto a la variable objetivo MARGEN_DOLARES son:
> - MARGEN_PORCENTAJE → 0.865
> - PRECIO_TOTAL_CON_DESCUENTO → 0.118
> - PRECIO_TOTAL_SIN_DESCUENTO → 0.116
![alt text](image-2.png)

> La alta correlación con el margen porcentual indica que el beneficio en terminos absolutos esta fuertemente relacionado con el porcentaje de margen aplicado en cada venta.
> Las otras dos variables presentan correlaciones más bajas, lo que sugiere una relación más débil con el margen.

**Pregunta 1.4** — ¿Hay valores nulos en el dataset? ¿Qué porcentaje representan y cómo los has tratado?

> No se han detectado valores nulos en el dataset, ya que todas las variables presentan un 0% de valores faltantes.
Por lo tanto, no ha sido necesario aplicar técnicas de imputación ni eliminación de datos, lo que facilita el análisis y garantiza la integridad de la información.

---

## Ejercicio 2 — Inferencia con Scikit-Learn

---
Añade aqui tu descripción y analisis:

---

**Pregunta 2.1** — Indica los valores de MAE, RMSE y R² de la regresión lineal sobre el test set. ¿El modelo funciona bien? ¿Por qué?

> _Escribe aquí tu respuesta_


---

## Ejercicio 3 — Regresión Lineal Múltiple en NumPy

---
Añade aqui tu descripción y analisis:

---

**Pregunta 3.1** — Explica en tus propias palabras qué hace la fórmula β = (XᵀX)⁻¹ Xᵀy y por qué es necesario añadir una columna de unos a la matriz X.

> _Escribe aquí tu respuesta_

**Pregunta 3.2** — Copia aquí los cuatro coeficientes ajustados por tu función y compáralos con los valores de referencia del enunciado.

| Parametro | Valor real | Valor ajustado |
|-----------|-----------|----------------|
| β₀        | 5.0       |                |
| β₁        | 2.0       |                |
| β₂        | -1.0      |                |
| β₃        | 0.5       |                |

> _Escribe aquí tu respuesta_

**Pregunta 3.3** — ¿Qué valores de MAE, RMSE y R² has obtenido? ¿Se aproximan a los de referencia?

> _Escribe aquí tu respuesta_

**Pregunta 3.4* — Compara los resultados con la reacción logística anterior para tu dataset y comprueba si el resultado es parecido. Explica qué ha sucedido. 

> _Escribe aquí tu respuesta_

---

## Ejercicio 4 — Series Temporales
---
Añade aqui tu descripción y analisis:

---

**Pregunta 4.1** — ¿La serie presenta tendencia? Descríbela brevemente (tipo, dirección, magnitud aproximada).

> _Escribe aquí tu respuesta_

**Pregunta 4.2** — ¿Hay estacionalidad? Indica el periodo aproximado en días y la amplitud del patrón estacional.

> _Escribe aquí tu respuesta_

**Pregunta 4.3** — ¿Se aprecian ciclos de largo plazo en la serie? ¿Cómo los diferencias de la tendencia?

> _Escribe aquí tu respuesta_

**Pregunta 4.4** — ¿El residuo se ajusta a un ruido ideal? Indica la media, la desviación típica y el resultado del test de normalidad (p-value) para justificar tu respuesta.

> _Escribe aquí tu respuesta_

---

*Fin del documento de respuestas*