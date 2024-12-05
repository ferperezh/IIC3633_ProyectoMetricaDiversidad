# Pitch para la presentación del póster

## Introducción 

Hola, mi nombre es Fernanda Pérez Hargreaves, y junto a mis compañeros les presento nuestro proyecto titulado User Diversity: Una Métrica para Diversidad en Recomendaciones. Este trabajo surge de una motivación clave: los sistemas de recomendación actuales tienden a enfocarse excesivamente en el comportamiento pasado del usuario, dejando de lado áreas menos exploradas pero potencialmente relevantes. Nuestro objetivo fue desarrollar una métrica que equilibrara personalización y diversidad, enriqueciendo la experiencia del usuario.

## Objetivo y propuesta

El objetivo principal fue diseñar la métrica User Diversity, que mide la diversidad en recomendaciones teniendo en cuenta las preferencias del usuario. Para esto, trabajamos con datasets de películas (MovieLens), música (Last.fm y Music-dataset-1950-to-2019) y restaurantes (Yelp). Comparamos nuestra métrica con otras métricas de diversidad, como Shannon Entropy y Long Tail, y evaluamos su desempeño en modelos como iKNN, FastFM, DeepFM y Hybrid.

## Resultados clave

Los resultados destacan tres observaciones importantes:

1. El modelo **Hybrid** alcanzó los valores más altos de User Diversity, pero sacrificó rendimiento en métricas como precisión y recall, lo que limita su utilidad práctica.

2. En contraste, **DeepFM** mostró un mejor equilibrio entre diversidad y rendimiento, lo que lo convierte en un modelo más consistente.

3. **Diversity Coverage** presentó patrones similares a User Diversity, debido a la similitud en sus fórmulas, pero los valores de **User Diversity** fueron consistentemente mayores, destacando su capacidad para capturar diversidad de forma más personalizada. Además, vimos que **User Diversity** supera a métricas tradicionales como **Shannon Entropy** e **Intra-List Diversity (ILD)**, ya que combina personalización y variedad, adaptándose mejor a las preferencias del usuario.


## Conclusiones y Futuro

En conclusión, **User Diversity** es una métrica innovadora que aborda las limitaciones de las métricas tradicionales al equilibrar personalización y diversidad. Sin embargo, su implementación depende de datos detallados del usuario y es más costosa computacionalmente. En trabajos futuros, planeamos:

- Analizar el impacto de diferentes valores de $k$

- Estudiar cómo el tamaño de $top_n$ afecta la precisión y diversidad.

- Incorporar pesos personalizados según las preferencias del usuario.

Creemos que esta métrica tiene un gran potencial para enriquecer sistemas de recomendación en dominios variados.

## Cierre

Gracias por su atención. Estaré encantada de responder preguntas o discutir cómo esta métrica podría aplicarse a otros sistemas de recomendación.


## Preguntas frecuentes


### **Preguntas generales**
1. **¿Por qué desarrollar una nueva métrica en lugar de usar las existentes?**
   - **Respuesta:** Las métricas tradicionales como Long Tail y Shannon Entropy no consideran la relevancia personalizada del usuario. **User Diversity** integra esta dimensión, equilibrando personalización y diversidad, lo que resulta en recomendaciones más relevantes y variadas para el usuario.

2. **¿Cómo se asegura que User Diversity sea útil en sistemas reales?**
   - **Respuesta:** Evaluamos la métrica en múltiples datasets (películas, música, restaurantes) y modelos, mostrando su capacidad para adaptarse a diferentes dominios. Además, su diseño permite ajustar parámetros como \(k\) y \(top_n\), lo que facilita su integración en sistemas existentes.

---

### **Sobre los modelos**
3. **¿Por qué el modelo Hybrid obtuvo alta diversidad pero bajo rendimiento en precisión?**
   - **Respuesta:** Hybrid prioriza la diversidad en las recomendaciones, dejando en segundo plano métricas como precisión y recall. Este enfoque extremo lo hace útil en contextos específicos, pero menos práctico en sistemas generales.

4. **¿Qué hace que DeepFM sea el modelo más balanceado?**
   - **Respuesta:** DeepFM combina redes neuronales profundas y máquinas de factorización, capturando relaciones complejas entre ítems y usuarios. Esto permite un mejor equilibrio entre personalización, precisión y diversidad.

---

### **Sobre la métrica**
5. **¿Cómo se compara User Diversity con métricas tradicionales?**
   - **Respuesta:** A diferencia de métricas como Long Tail o Shannon Entropy, **User Diversity** incorpora relevancia personalizada. Esto permite evaluar la diversidad en función de las categorías más importantes para el usuario, ofreciendo un análisis más completo.

6. **¿Qué limitaciones tiene User Diversity?**
   - **Respuesta:** Sus principales limitaciones son:
     - Depende de datos detallados de las preferencias del usuario.
     - Requiere más recursos computacionales en comparación con métricas tradicionales.
     - Está enfocada en categorías conocidas, lo que podría limitar la exploración de nuevas áreas.

7. **¿Cómo afecta el valor de \(k\) en la métrica?**
   - **Respuesta:** \(k\) define el número de categorías principales que se consideran relevantes para el usuario. Valores altos pueden diluir la personalización, mientras que valores bajos pueden limitar la diversidad. Encontrar el \(k\) óptimo depende del dominio y del comportamiento del usuario.

---

### **Aplicaciones prácticas**
8. **¿En qué otros dominios podría aplicarse User Diversity?**
   - **Respuesta:** Además de películas, música y restaurantes, la métrica puede aplicarse a recomendaciones de libros, productos en e-commerce, o incluso contenidos educativos, donde personalización y diversidad son esenciales.

9. **¿Cómo impacta la métrica en la experiencia del usuario?**
   - **Respuesta:** Mejora la experiencia al ofrecer recomendaciones variadas y relevantes, evitando la monotonía y fomentando el descubrimiento de nuevos intereses. Esto ayuda a mantener el interés del usuario en la plataforma.

---

### **Técnicas y herramientas**
10. **¿Cómo manejaron las limitaciones de memoria en Google Colab?**
    - **Respuesta:** Simplificamos procedimientos y optimizamos los cálculos para datasets grandes. Por ejemplo, procesamos subconjuntos de datos y ajustamos el tamaño de las listas recomendadas (\(top_n\)).

11. **¿Por qué no utilizaron librerías como pyRecLab?**
    - **Respuesta:** PyRecLab no era compatible con algunos de nuestros requisitos específicos, como la implementación de **User Diversity**. Esto nos llevó a desarrollar herramientas desde cero, asegurando la flexibilidad necesaria para nuestro análisis.

---

### **Impacto y futuro**
12. **¿Qué impacto tiene esta métrica en el diseño de sistemas recomendadores?**
    - **Respuesta:** Proporciona una herramienta que equilibra precisión y diversidad, permitiendo sistemas que sean tanto efectivos como enriquecedores para los usuarios. Esto es especialmente importante en aplicaciones donde la monotonía de recomendaciones puede ser perjudicial.

13. **¿Qué esperan lograr en el futuro con esta métrica?**
    - **Respuesta:** Planeamos explorar su impacto con diferentes configuraciones de \(k\) y \(top_n\), e incorporar ponderaciones personalizadas para categorías. También evaluaremos su aplicabilidad en sistemas recomendadores en tiempo real.

---

### **Motivación y Objetivos**

14. **¿Por qué la personalización y la diversidad al mismo tiempo son importantes para el usuario?**
    - **Respuesta:** La personalización garantiza que las recomendaciones sean relevantes para el usuario, basándose en sus intereses y comportamientos previos. Sin embargo, centrarse exclusivamente en la personalización puede generar recomendaciones repetitivas y predecibles, limitando la exploración de nuevas opciones. La diversidad, por otro lado, fomenta el descubrimiento de nuevos intereses, ampliando la experiencia del usuario. Al combinar ambas, un sistema recomendador puede mantener al usuario comprometido y satisfecho, ofreciendo contenido que es tanto relevante como novedoso.


15.  **¿Por qué no centrarse solo en diversidad en lugar de combinarla con personalización?**
        - **Respuesta:** La diversidad sin personalización puede resultar en recomendaciones que no son relevantes para el usuario, lo que disminuye su satisfacción y el interés por interactuar con el sistema. Por ejemplo, mostrar categorías completamente ajenas a las preferencias del usuario podría ser percibido como ruido. Al combinar diversidad con personalización, se logra un equilibrio: se exploran nuevas opciones dentro de las áreas de interés del usuario, manteniendo la relevancia de las recomendaciones y fomentando el descubrimiento sin desconectarse de sus preferencias actuales.

---

