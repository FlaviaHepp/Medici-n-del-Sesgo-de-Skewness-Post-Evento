# Medición del Sesgo de Skewness Post-Evento

Eficiencia y Respuesta del Mercado — Eventos Corporativos

## 📌Descripción General

Este proyecto analiza cómo cambia la asimetría de los retornos (skewness) de una acción antes y después de un evento corporativo, específicamente un Split de acciones.

El objetivo es detectar si el evento altera la distribución del riesgo:
- mayor probabilidad de retornos positivos extremos (skewness positivo),
- o mayor riesgo de caídas abruptas (skewness negativo).

A diferencia del análisis tradicional de precios, este enfoque se centra en la forma estadística de los retornos, una dimensión frecuentemente ignorada por indicadores clásicos.

## 📍Insight Clave

- ¿Cómo cambia el sesgo de los retornos (riesgo de cola) en la semana posterior a un Split?

Un cambio significativo en el skewness sugiere que:
- el mercado re-evalúa el perfil de riesgo del activo,
- el evento no es neutral, aunque el precio no muestre movimientos evidentes.

## 💼Valor de Negocio

- Identifica eventos que alteran la naturaleza del riesgo, no solo el retorno esperado.

Detecta asimetrías ocultas que pueden afectar estrategias de:
- opciones,
- risk parity,
- cobertura de cola.

Útil para evaluar si un Split genera:
- mayor especulación alcista (skewness positivo),
- o mayor fragilidad post-evento (skewness negativo).

Fuentes de Datos:
- eventos_corporativos
- ticker_id
- fecha
- tipo_evento
- indicadores_tecnicos
- ticker_id
- fecha
- skewness

## 🧠Lógica del Análisis

Se filtran eventos corporativos del tipo Split.

Para cada evento:
- Se calcula el skewness promedio de los 5 días previos.
- Se calcula el skewness promedio de los 5 días posteriores.

Se mide el cambio neto de skewness:
- skewness_post − skewness_pre

Los resultados se ordenan para destacar los mayores cambios.

## 📊Interpretación de Resultados

Cambio positivo de skewness
→ Mayor probabilidad de retornos positivos extremos post-evento.
→ Señal de optimismo especulativo o re-pricing alcista del riesgo.

Cambio negativo de skewness
→ Incremento del riesgo de caídas abruptas.
→ El evento puede haber aumentado la fragilidad del activo.

Cambio cercano a cero
→ Evento ampliamente descontado por el mercado.

## 🧩Casos de Uso

- Evaluación de impacto real de Splits más allá del efecto nominal.
- Ajuste de modelos de riesgo basados en colas.
- Filtrado de eventos “cosméticos” vs. eventos que alteran el perfil estadístico.
- Complemento avanzado a estudios de event-driven trading.

## 🚀Posibles Extensiones

- Comparar Splits vs. Dividendos vs. Ganancias.
- Medir skewness a 10 o 20 días post-evento.
- Analizar resultados por sector o país.
- Combinar con kurtosis para medir riesgo extremo total.
- Integrar con precios para detectar divergencias precio-riesgo.

## ✒️Nota Final

- Este análisis revela cómo cambia el riesgo, no solo el precio.
- Es especialmente útil en mercados donde los eventos son frecuentes, pero su impacto real es sutil y no lineal.

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
