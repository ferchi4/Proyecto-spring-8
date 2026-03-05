# **Análisis de Movilidad Urbana: Taxis en Chicago y el Impacto del Clima**

Este proyecto explora los patrones del servicio de taxis en Chicago, utilizando datos de viajes desde el Aeropuerto Internacional O'Hare. El objetivo principal es identificar las empresas líderes, los barrios con mayor demanda y, mediante una prueba de hipótesis, determinar si las condiciones climáticas afectan significativamente la duración de los viajes en una ruta clave.

**Objetivo**

El proyecto se centra en probar la siguiente hipótesis:

*   **Hipótesis Nula (H0):** La duración promedio de los viajes desde el barrio Loop al Aeropuerto O'Hare **no** varía entre los sábados con lluvia y los sábados con buen tiempo.
*   **Hipótesis Alternativa (H1):** La duración promedio de los viajes desde el Loop al Aeropuerto O'Hare **sí varía** entre los sábados con lluvia y los sábados con buen tiempo (específicamente, se espera que sea mayor en días lluviosos).

**🛠️ Tecnologías Utilizadas**

*   **Python:** Lenguaje principal para el análisis.
*   **Pandas:** Para la manipulación y limpieza de datos.
*   **Matplotlib y Seaborn:** Para la visualización de datos y creación de gráficos.
*   **SciPy:** Para la realización de la prueba de hipótesis estadística (prueba t de Welch).
*   **Jupyter Notebook:** Entorno interactivo para el desarrollo del análisis.

**Pasos Clave**

1.  **Análisis Exploratorio de Datos (EDA):**
    *   Se evaluó la calidad de los conjuntos de datos, verificando tipos de datos, valores nulos y duplicados.
    *   Se realizó una limpieza básica para asegurar la integridad de la información.

2.  **Visualización de Patrones de Demanda:**
    *   Se identificaron y graficaron los 10 barrios con mayor promedio de viajes finalizados, destacando zonas de alta actividad como Loop y River North.
    *   Se visualizaron las 20 empresas de taxis con mayor número de viajes, revelando una alta concentración del mercado en unas pocas compañías, lideradas por *Flash Cab*.

3.  **Prueba de Hipótesis:**
    *   Se prepararon los datos meteorológicos, filtrando los viajes realizados los sábados y clasificándolos por condición climática ("Bad" para lluvia, "Good" para buen tiempo).
    *   Se aplicó una prueba t de Welch para comparar las medias de dos grupos independientes (sábados lluviosos vs. sábados normales), sin asumir varianzas iguales.
    *   Se visualizó la distribución de la duración de los viajes para ambos grupos mediante gráficos de densidad (KDE).

**Resultados**

El análisis confirma que:

*   **Concentración del Mercado:** Empresas como *Flash Cab* y *Taxi Affiliation Services* dominan el número de viajes, y la mayoría de los viajes terminan en barrios centrales como Loop y River North.
*   **Impacto del Clima en la Duración de Viajes:** La prueba de hipótesis rechaza la hipótesis nula. Se encontró una diferencia estadísticamente significativa en la duración de los viajes.
    *   La duración promedio en sábados lluviosos fue de **40.2 minutos**, mientras que en sábados normales fue de **33.9 minutos**.
*   **Conclusión Estadística:** Con un valor p extremadamente bajo (p < 0.05), se concluye que el mal tiempo (lluvia) aumenta significativamente el tiempo de viaje en la ruta analizada, probablemente debido a una mayor congestión vehicular o condiciones de manejo más lentas.

**Cómo Ejecutar el Proyecto**

1.  Clona este repositorio en tu máquina local.
    ```bash
    git clone (https://github.com/ferchi4/Proyecto-spring-8)
    ```

2.  Asegúrate de tener instaladas las dependencias necesarias:
    ```bash
    pip install pandas numpy matplotlib seaborn scipy jupyter
    ```

3.  Coloca los archivos CSV (`moved_project_sql_result_01.csv`, `moved_project_sql_result_04.csv`, `moved_project_sql_result_07.csv`) en el mismo directorio que el notebook.

4.  Abre y ejecuta el archivo `proyecto8.ipynb` en Jupyter Notebook.
    ```bash
    jupyter notebook proyecto8.ipynb
    ```
