# Feedback del Profesor respecto a nuestra Entrega 1
La propuesta de hacer una métrica es factible, pero la formulación actual está demasiado limitada para un proyecto del curso de sistemas de recomendación. Si se propone una nueva métrica, la nueva métrica debe evaluarse en al menos 2 datasets (esto está OK por el momento con las.fm, pero deben tener la metadata para estas canciones). 

Por otro lado, crear una métrica significa demostrar que esa métrica tiene ciertas propiedades que la hacen mejor que otras métricas existentes, por lo cual deben: decir contra qué métrica(s) actuales de diversidad se van a comparar (2 o 3 para comparación al menos), cuáles son las hipótesis de contribución que tendrá la nueva métrica (por ejemplo, esta métrica nueva será más eficiente de calcular que la de Ziegler, más efectiva ante elementos nicho, menos sesgada que otras métricas, etc.)

Por lo tanto la propuesta debe indicar los experimentos que llevarán a cabo para probar sus hipotesis, Deben también proponer análisis y gráficos para la nueva métrica ¿cómo se relaciona esta nueva métrica con la de Ziegler o con otras existentes como inverse propensity score IPS? ¿tienen mayor a menor varianza? ¿tiene una correlación positiva con las métricas de ranking conocidas? 

Les sugiero revisar el articulo hecho previamente por un grupo de este mismo curso del año 2020 "Quantification of the Impact of Popularity Bias in Multi-stakeholder and Time-Aware Environments" Ruiz et al https://link.springer.com/chapter/10.1007/978-3-030-78818-6_8 ellos crearon dos métricas y evaluaron en dos datasets. 

Otro elemento que deben mejorar es que el hecho de calcular diversidad o novedad no significa que deben dejar de calcular las otras métricas como ranking (MAP, nDCG, precision, recall, AUC); Siempre deben calcular esas métricas, de hecho, lo que deben hacer es analizar la relación entre su nueva métrica propuesta y las métricas existentes de rendimiento o ranking. 

Se espera para el avance tomar estos elementos en consideración. Nota: en esta propuesta no hay resultados de ningún tipo sobre los métodos minimos random, most popular y fact. matricial. Se les sugiere revisar metricas de diversidad para compararse en este paper Kunaver, M., & Požrl, T. (2017). Diversity in recommender systems–A survey. Knowledge-based systems, 123, 154-162.
