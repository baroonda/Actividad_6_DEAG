📊 Actividad 6: Validación de Modelos de Machine Learning - Detección de Fraude

📌 Descripción del Proyecto

Este repositorio contiene la experimentación, evaluación y validación de modelos de clasificación aplicados a un caso de negocio financiero: Detección de fraude en transacciones con tarjetas de crédito.

Como parte de una arquitectura orientada a la nube híbrida, el proyecto evalúa algoritmos de Machine Learning para minimizar las pérdidas financieras (Falsos Negativos) y optimizar la experiencia del cliente reduciendo bloqueos erróneos (Falsos Positivos).

🎯 Objetivo SMART

Evaluar y validar la capacidad de un modelo Random Forest frente a un baseline de Regresión Logística para clasificar transacciones fraudulentas, logrando un Recall mínimo del 85% en la clase minoritaria mediante el ajuste del umbral de decisión, validado con Stratified K-Fold Cross-Validation y una simulación de prueba A/B offline.

🛠️ Tecnologías y Herramientas

Lenguaje: Python 3

Librerías: Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

Entorno: Google Colab

Gestión del Proyecto: Trello (Kanban) / GitHub

🧪 Metodología de Validación

Entrenamiento y Baseline: Se estableció un modelo de Regresión Logística como baseline para contrastar el rendimiento frente al modelo retador (Random Forest).

Validación Cruzada (K-Fold): Se implementó Stratified K-Fold (5 particiones) en el modelo Random Forest para prevenir el sobreajuste (overfitting), obteniendo un ROC AUC promedio de 0.9452 (+/- 0.0202).

Simulación de Prueba A/B (Offline): El tráfico de prueba se dividió 50/50 para medir el impacto operativo de ambos modelos antes de un despliegue total.

Ajuste de Umbral (Threshold Tuning): Se priorizó la sensibilidad frente al fraude. El umbral de decisión se ajustó de 0.50 a 0.10 para garantizar un Recall superior al 85%.

📈 Resultados Destacados

Superación del Baseline: El modelo Random Forest capturó significativamente más transacciones fraudulentas que la Regresión Logística y redujo los Falsos Positivos de 13 a solo 2.

Trade-off Precisión vs Recall: Al ajustar el umbral, se demostró que es posible blindar al banco contra el fraude sin saturar los canales de atención al cliente.

Métrica de Negocio vs Métrica Técnica: Se descartó la "Exactitud" (Accuracy) debido al desbalance extremo de clases, priorizando el AUC ROC y la matriz de confusión para la toma de decisiones.

📂 Contenido del Repositorio

Actividad_6_Validacion_Modelos.ipynb: Notebook de experimentación con el código fuente y las métricas detalladas.

(Nota: El dataset creditcard.csv no se incluye en el repositorio por restricciones de tamaño, pero puede descargarse desde Kaggle).

Autor: baroonda

Módulo: Gestión de Proyectos de Inteligencia Artificial
