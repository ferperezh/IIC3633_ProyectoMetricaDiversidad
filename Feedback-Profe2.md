# Feedback Segunda Entrega - Proyecto de Sistemas Recomendadores

## Aspectos positivos:
- En esta entrega hay cierta creatividad para proponer una métrica basada en Entropía de una distribución categórica.
- Se nota un esfuerzo por hacer un análisis de datos con varias visualizaciones.

## Aspectos débiles:
- Los métodos *random* y *most popular* están bien como *sanity check*, pero como baselines se esperan modelos más sofisticados.
- Explicar un modelo de recomendación como "método colaborativo" es demasiado general. ¿UKNN, IKNN, funkSVD, ALS, BPR, FM, DeepFM, MultVAE, LightGCN, SLIM, EASE? Se espera que sean más específicos en esta clase.
- Falta un modelo basado en contenido.
- El método híbrido también es extremadamente simple y no ayuda a entender el comportamiento de la métrica en casos como uso de contexto o metadata (ej. LightFM, FastFM).
- El análisis de datos indica la realización de un ANOVA, pero en ninguna parte del reporte aparece el reporte oficial de dicho análisis (si lo llegan a reportar, deben usar el formato *APA style*).
- En el análisis de datos se habla de propiedades de la métrica, pero no se compara con otras métricas que miden diversidad. ¿En qué se parece y en qué se diferencia esta métrica propuesta de las métricas de diversidad ya existentes en la literatura de sistemas de recomendación?

## Comentarios para la versión final:
- Se espera que usen al menos **3 datasets** y que las métricas se puedan ver en los 3. Hay decenas de datasets disponibles, basta con revisar la página de J. MacAuley de UCSD.
- Deben agregar modelos de recomendación más competitivos.
- Falta un modelo basado en contenido.
- Incluir un modelo que use datos de contexto o metadata (ej. LightFM, FastFM, DeepFM).
