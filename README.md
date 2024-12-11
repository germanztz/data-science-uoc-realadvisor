<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/79/Logotipo_UOC.svg/480px-Logotipo_UOC.svg.png" alt="UOC" width="100"/>

<img src="images/logo.png" alt="Real Advisor" width="300"/>

# Real Advisor
         
Descubre las mejores oportunidades inmobiliarias en Barcelona con nuestro sistema de recomendación. Analiza datos clave, estima rentabilidad y riesgos, y recibe informes detallados para decisiones inteligentes.

## Objeto

El objetivo principal del trabajo es desarrollar un sistema **recomendador de inversiones** en el sector inmobiliario. En el ámbito terrorial de la **provincia de Barcelona**.

El sistema solicitará al usuario una serie de datos para realizar el análisis, como:
- Datos o URL del imnueble (precio de compra, m2, ubicación)
- Otras características del inmueble (número de habitaciones, superficie, etc.) **(fuera del alcance)**

El sistema podrá estimar el importe de alquiler de esa vivienda teniendo en cuenta el municipio, la superficie y demás características del inmueble
Como resultado, el sistema devolverá un informe comercial del inmuebles analizado según el riesgo y la rentabilidad estimada y otros factores.

## Detalles

```Python

real_advisor = {
   'Autor': 'Germán Zeitz Lalanne'
   'Fecha':'dic/2024'
   'Lenguaje': 'Python'
   'Licencia': 'MIT'
   'Repositorio': {
      'GitHub': 'https://github.com/germanztz/data-science-uoc-realadvisor'
   }
   'Planificacion':{
      'Projects': 'https://github.com/users/germanztz/projects/2'
   }

}
```

## Alcance

1. **Investigación**: Se llevará a cabo una investigación exploratoria para comprender el mercado inmobiliario y las tendencias actuales, precios del mercado inmobiliario de Barcelona.

   - Listado de Entidades gubernamentales para obtención datos sobre el mercado inmobiliario
   - Listado de portales inmobiliarios para obtención de datos de oferta de venta

1. **Analisis**: Se analizarán los datos de oferta de venta de inmuebles y alquileres


   1. **Análisis de Series de Tiempo**: Realizar un análisis exhaustivo de las tendencias y patrones temporales presentes en los datos.
   2. **Análisis Exploratorio de Datos (EDA)**: Identificar patrones, anomalías y relaciones entre las variables mediante visualizaciones y estadísticas descriptivas.
   3. **Análisis de Calidad de los Datos**: Evaluar la calidad de los datos, identificando problemas como valores faltantes, inconsistencias, errores o duplicados.
   4. **Análisis Gráfico de los Datos**: Representar gráficamente las variables mediante gráficos como histogramas, diagramas de dispersión, boxplots, entre otros, para facilitar la comprensión visual de los datos.
   5. **Segmentación Inteligente de los Datos**: Implementar técnicas de segmentación avanzadas que aporten valor al análisis y la extracción de insights relevantes.
   6. **Análisis de Correlación**: Evaluar las relaciones y asociaciones entre las variables mediante matrices de correlación y análisis de dependencias.
   7. **Análisis de Outliers**: Detectar y tratar los valores atípicos (outliers) presentes en los datos para mejorar la precisión de los modelos.
   8. **Análisis de Cohortes Avanzados**: Realizar segmentación y análisis del comportamiento de los usuarios a lo largo del tiempo, con el objetivo de identificar patrones de retención, uso y otros comportamientos clave.

1. **Modelamiento**: Se desarrollarán modelos de aprendizaje automático (ML) para predecir la rentabilidad futura de una inversión inmobiliaria y el retorno sobre la inversión (ROI).

   9. **Modelos de Regresión Regularizados**: Implementar modelos de regresión regularizados (como Ridge, Lasso, ElasticNet), utilizando técnicas de búsqueda de hiperparámetros para optimizar el rendimiento del modelo.
   10. **Modelos de Clasificación**: Desarrollar y optimizar modelos de clasificación (como árboles de decisión, SVM, k-NN), utilizando los métodos adecuados de validación y evaluación.
   11. **Validación de Modelos**: Seleccionar los mejores modelos mediante validación cruzada con k-fold, para asegurar la robustez y generalización de los modelos creados.
         - Modelo de regresión para interpolación para rellenado de precios faltantes
         - Modelo de clasificación para predecir la ocupación del inmueble
         - Modelo de extrapolación para predicción de precios actuales y futuros
         - Uso de Modelos generativos DDL para interpretar las propiedades

1. **Desarrollo**: Se desarrollarán un sistema de recuperación de información y recomendación de inversiones inmobiliarias basado en los modelos desarrollados.

   12. **Uso de Scraping para Variables Exógenas**: El proyecto debe incluir el uso de técnicas de web scraping para obtener variables adicionales de fuentes externas que aporten valor a los datos originales del proyecto.
         - Scrapping de una web para extraer datos del inmueble necesarios para realizar la valoración de la inversión
   - Generación del informe de valoración de la inversión del inmueble

## Planificación

### Metodología ágil

Para abordar este análisis mediante una metodología ágil, vamos a estructurar el trabajo en iteraciones cortas o "sprints". Cada sprint tendrá una duración de 1 semana, con entregas de valor al final de cada uno para mantener el progreso continuo y asegurar que el equipo se adapta rápidamente a cualquier cambio o mejora que se necesite.

Aquí está el desglose de la metodología ágil aplicada a este proyecto de análisis: fichero adjunto: [planificación](planificación.md)

![alt text](images/image.png)

## Metodología

Para el proyecto del recomendador de inversiones inmobiliarias, el tipo de modelo de machine learning (ML) a utilizar depende de los objetivos específicos de predicción y análisis de riesgo y rentabilidad.

### Tipo de modelo de ML

1. **Regresión**:
   Dado que el objetivo principal es predecir la rentabilidad futura de una inversión inmobiliaria y el retorno sobre la inversión (ROI), el tipo de modelo de ML más adecuado sería un **modelo de regresión**. Este tipo de modelo es utilizado para predecir valores numéricos continuos, como el precio futuro de una propiedad o la tasa de retorno esperada.

   - **Regresión lineal múltiple** podría ser un modelo inicial simple, en el que se utilicen múltiples variables como el precio de compraventa, la localización, el tamaño, el estado del inmueble, y otros factores para predecir la rentabilidad o el precio futuro del inmueble.
   - **Modelos de regresión más avanzados** como **Random Forest Regressor** o **XGBoost Regressor** podrían ser implementados para mejorar la precisión, ya que son modelos no lineales que capturan mejor las interacciones complejas entre las variables.

2. **Clasificación**:
   Además, en ciertos aspectos como la clasificación del nivel de riesgo de una inversión, se podrían usar **modelos de clasificación**. Este tipo de modelo clasifica los inmuebles en categorías de riesgo (por ejemplo, bajo, medio, alto). Modelos como **árboles de decisión** o **logistic regression** serían útiles aquí.

### Métrica de evaluación del modelo

1. **Error cuadrático medio (Mean Squared Error, MSE)**:
   Para los modelos de regresión, una métrica adecuada para medir el rendimiento sería el **MSE**. Esta métrica mide el promedio del cuadrado de los errores (diferencia entre el valor real y el valor predicho). Se prefiere minimizar el MSE para obtener predicciones más precisas.

2. **Error absoluto medio (Mean Absolute Error, MAE)**:
   Otra métrica útil es el **MAE**, que calcula la media de las diferencias absolutas entre las predicciones y los valores reales. Es más interpretativa en ciertos contextos, ya que expresa los errores en las mismas unidades que la variable de interés (precio de inmueble o rentabilidad).

3. **R² (Coeficiente de determinación)**:
   Esta métrica indica qué porcentaje de la variabilidad en los datos se explica por el modelo. Un valor cercano a 1 indica que el modelo es capaz de explicar la mayor parte de la variabilidad en los precios o rentabilidades predichos.

4. **Precisión, Recall y F1-Score** (para clasificación):
   En los modelos de clasificación (para riesgo de inversión), se utilizarían métricas como la **precisión** (qué tan bien el modelo predice correctamente los inmuebles de alto riesgo), **recall** (qué proporción de inmuebles de alto riesgo fueron correctamente clasificados), y **F1-score**, que combina ambas métricas en un solo valor.

### Conclusión
- Para la **predicción de rentabilidad y precios**, un **modelo de regresión** con **MSE** o **MAE** como métrica de evaluación sería adecuado.
- Para la **clasificación de inmuebles por nivel de riesgo**, un modelo de clasificación con métricas como **precisión**, **recall** y **F1-score** proporcionaría información útil para los usuarios interesados en inversiones de bajo o alto riesgo.

Se considerarán las tendencias observadas en los datos históricos y se compararán con los datos actuales extraídos de los portales inmobiliarios. La información será filtrada por municipio y otras características clave de los inmuebles. Además, se analizarán las descripciones de los inmuebles para identificar propiedades ocupadas, alquiladas o con otras condiciones especiales.

Los datos a analizar en el sistema incluirán:
- Precio de compraventa
- Fecha de compraventa
- Municipio
- Código postal
- Tipo de inmueble
- Superficie
- Número de habitaciones
- Número de baños
- Descripción del inmueble
- Estado del inmueble
- Precio de alquiler

## Requisitos

1. Datos estadísticos de compraventa de inmuebles en Cataluña de los últimos años (descargables en archivo)
2. Datos estadísticos de alquiler de viviendas en Cataluña de los últimos años (descargables en archivo)
3. Datos de las ofertas actuales de compraventa de inmuebles en Cataluña extraídos de portales online (web scraping)
4. Datos de las ofertas actuales de alquiler de viviendas en Cataluña (web scraping)
5. Modelo de ML entrenado con los datos de compraventa, alquiler y oferta de inmuebles

## Tareas

1. Estudio de portales y páginas estadísticas gubernamentales de Cataluña y España:
   - Listado de portales candidatos para la obtención de datos
1. Obtención de datos estadísticos de compraventa y alquiler de los últimos años en Cataluña:
   - Múltiples tablas con datos históricos de compraventa
   - Múltiples tablas con datos históricos de alquiler
1. Filtrado y limpieza de los datos:
   - Una única tabla con datos de compraventa optimizados
   - Una única tabla con datos de alquiler optimizados
1. Estudio de datos complementarios (por ejemplo, datos geográficos):
   - Tabla con datos de compraventa completos y optimizados
   - Tabla con datos de alquiler completos y optimizados
1. Identificación de portales inmobiliarios con oferta de venta y alquiler:
   - Listado de portales candidatos para la obtención de datos
1. Web scraping de la oferta actual de inmuebles y alquileres:
   - Scripts de web scraping de oferta de venta de inmueble
   - Scripts de web scraping para diferentes portales **(fuera del alcance)**
   - Múltiples tablas con datos de oferta de venta de inmuebles **(fuera del alcance)**
   - Múltiples tablas con datos de oferta de alquiler de viviendas **(fuera del alcance)**
1. Filtrado, limpieza y completado (por ejemplo, con datos geográficos) de la oferta:
   - Una única tabla con datos de oferta de venta optimizados **(fuera del alcance)**
   - Una única tabla con datos de oferta de alquiler optimizados **(fuera del alcance)**
1. Entrenamiento del modelo de ML con datos de compraventa, alquiler y oferta actual:
   - Modelo de regresión pa interpolación para rellenado de precios faltantes
   - Modelo de clasificación para predecir la ocupación del inmueble
   - Modelo de extrapolación para predicción de precios actuales y futuros
   - Uso de Modelos generativos DDL para interpretar las propiedades1. Realización de predicciones y valoraciones sobre las ofertas
1. Evaluación del modelo
1. Creación del portal web para la recomendación de inversiones inmobiliarias **(fuera del alcance)**


### 1. Listado de portales candidatos para la obtención de datos

- [Sistema estatal de referencia del precio del alquiler de vivienda (SERPAVI)](https://www.mivau.gob.es/vivienda/alquila-bien-es-tu-derecho/serpavi) 

   El SERPAVI ofrece el resultado de la explotación de fuentes tributarias de los datos sobre arrendamientos de vivienda habitual.

- [Barcelona Dades](https://portaldades.ajuntament.barcelona.cat/ca/report/habitatge)

   Anàlisi de l’evolució de la construcció d’habitatges a la ciutat, les compravendes registrades i els preus dels habitatges nous i de segona mà, així com els contractes de lloguer i els preus de lloguers per districtes i barris.

   Ejemplo de uso de la api

   ```bash
   curl -H "X-IBM-Client-Id: ${bcndades_client_id}" -o file.csv "https://portaldades.ajuntament.barcelona.cat/services/backend/rest/statistic/export?id=5ibudgqbrb&fileformat=CSV"
   ```

- [Servei de dades obertes de l'Ajuntament de Barcelona](https://opendata-ajuntament.barcelona.cat/data/es/organization/habitatge)
- [Iniciativa de datos abiertos del Gobierno de España](https://datos.gob.es/es/catalogo?theme_es=Vivienda)
- [Portal de dades obertes de la Generalitat](https://analisi.transparenciacatalunya.cat/browse?category=Habitatge)


---
# 1. Investigación


   ## 1.1 Listado de Entidades gubernamentales para obtención datos sobre el mercado inmobiliario

   ### 1.1.1 Alquiler

- [Sistema Estatal de Referencia del Precio del Alquiler de Vivienda](http://cdn.mivau.gob.es/portal-web-mivau/vivienda/serpavi/2024-05-07_bd_sistema-indices-alquiler-vivienda_2011-2022.xlsx)

      Precio medio de alquiler entre 2015-2022, por m2 e inmueble completo, separado en dos cuartiles y mediana, y en vivienda unifamiliar y colectiva, por sección censal, municipio, provincia y comunidad autónoma.

- [Precio medio por superficie (€/m²) del alquiler de viviendas](https://portaldades.ajuntament.barcelona.cat/es/estad%C3%ADsticas/5ibudgqbrb)

      Renta media mensual por superficie (€/m²) de alquiler de viviendas procedente de la estadística de fianzas del INCASOL. Se puede considerar que esta estadística tiene un carácter censal ya que se basa en el recuento de todos los contratos de alquiler que han depositado la fianza en el Incasòl en el período considerado.


### 1.1.2 Compraventa

- [Precio medio por superficie (€/m²) de las viviendas transmitidas por compraventa](https://portaldades.ajuntament.barcelona.cat/es/estad%C3%ADsticas/bxtvnxvukh?view=table)

      Precio medio por superficie (€/m²) de las viviendas transmitidas por compraventa entre 2015 y 2024. Solo se consideran propiedades de tipo horizontal. El número mostrado representa la media aritmética calculada a nivel territorial, basada en un mínimo de 5 muestras. Se excluyen las transacciones con un precio por metro cuadrado superior a 30.000 €/m² o inferior a 100 €/m². En el contexto de este análisis, es importante destacar que los valores límite seleccionados han sido elegidos para alinearse y reflejar las dinámicas del mercado inmobiliario actual de la ciudad. De acuerdo con el Decreto 141/2012 sobre las condiciones mínimas de habitabilidad de las viviendas y el certificado de habitabilidad (Generalitat de Catalunya - Departamento de Territorio y Sostenibilidad - Secretaría de Vivienda y Mejora Urbana), se excluyen las viviendas con una superficie inferior a 15 m².

- [Precio medio por superficie (€/m²) de las viviendas transmitidas por compraventa por tipo de propiedad](https://portaldades.ajuntament.barcelona.cat/es/estad%C3%ADsticas/mrslyp5pcq)

      Precio medio por superficie (€/m²) de las viviendas transmitidas por compraventa por tipo de propiedad. El número mostrado representa la media aritmética calculada a nivel territorial, basada en un mínimo de 5 muestras. Se excluyen las transacciones con un precio por metro cuadrado superior a 30.000 €/m² o inferior a 100 €/m². En el contexto de este análisis, es importante destacar que los valores límite seleccionados han sido elegidos para alinearse y reflejar las dinámicas del mercado inmobiliario actual de la ciudad. De acuerdo con el Decreto 141/2012 sobre las condiciones mínimas de habitabilidad de las viviendas y el certificado de habitabilidad (Generalitat de Catalunya - Departamento de Territorio y Sostenibilidad - Secretaría de Vivienda y Mejora Urbana), se excluyen las viviendas con una superficie inferior a 15 m².

- [Precio medio por superficie (€/m²) de las viviendas transmitidas por compraventa por año de construcción del edificio](https://portaldades.ajuntament.barcelona.cat/es/estad%C3%ADsticas/idjhkx1ruj)

      Precio medio por superficie (€/m²) de las viviendas transmitidas por compraventa por año de construcción del edificio. Solo se consideran propiedades de tipo horizontal. El número mostrado representa la media aritmética calculada a nivel territorial, basada en un mínimo de 5 muestras. Se excluyen las transacciones con un precio por metro cuadrado superior a 30.000 €/m² o inferior a 100 €/m². En el contexto de este análisis, es importante destacar que los valores límite seleccionados han sido elegidos para alinearse y reflejar las dinámicas del mercado inmobiliario actual de la ciudad. De acuerdo con el Decreto 141/2012 sobre las condiciones mínimas de habitabilidad de las viviendas y el certificado de habitabilidad (Generalitat de Catalunya - Departamento de Territorio y Sostenibilidad - Secretaría de Vivienda y Mejora Urbana), se excluyen las viviendas con una superficie inferior a 15 m².

- [Precio medio por superficie (€/m²) de las compraventas de vivienda registradas](https://portaldades.ajuntament.barcelona.cat/es/estad%C3%ADsticas/u25rr7oxh6)

      Compraventas de viviendas inscritas en el Registro de la Propiedad con transmisión del 100% de la propiedad.


- [Precio medio por superficie (€/m²) de oferta de viviendas de segunda mano en venta](https://portaldades.ajuntament.barcelona.cat/es/estad%C3%ADsticas/bhl3ulphi5)

      Media del precio de venta de las viviendas en oferta del portal inmobiliario Idealista.com


- https://datos.gob.es/es/catalogo/a09002970-registro-de-las-fianzas-de-alquiler-de-viviendas-por-municipio
- https://datos.gob.es/es/catalogo/a09002970-registro-de-las-fianzas-de-alquiler-de-viviendas-para-diferentes-ambitos-territoriales
- https://opendata-ajuntament.barcelona.cat/data/es/organization/habitatge?q=&sort=fecha_publicacion+desc
- https://opendata-ajuntament.barcelona.cat/data/es/dataset/est-cadastre-locals-prop/resource/78cbada1-f5e5-4ef3-a00a-9cbdb98d78f0

## 1.1.3 Listado de portales inmobiliarios con oferta de venta y alquiler

- [idealista](https://www.idealista.com)
   - https://github.com/paezha/idealista18
- [habitaclia](https://www.habitaclia.com)

# 2. Análisis exploratorio

   1. **Análisis de Series de Tiempo**: Realizar un análisis exhaustivo de las tendencias y patrones temporales presentes en los datos.

      ![alt text](images/image-1.png)![alt text](images/image-2.png)![alt text](images/image-3.png)

      - El mercado de alquiler sigue una tendencia de crecimiento a largo plazo, con fluctuaciones estacionales bien definidas.
      - Las ligeras irregularidades en los residuos sugieren que hay factores adicionales que podrían influir en los precios pero que no siguen patrones sistemáticos.
      - El precio de venta muestra un crecimiento sostenido a largo plazo, con patrones estacionales bien definidos.
      - Los residuos y puntos atípicos pueden estar vinculados a cambios en políticas económicas, fluctuaciones de mercado, o eventos globales, como la pandemia en 2020.
---

   2. **Análisis Exploratorio de Datos (EDA)**: Identificar patrones, anomalías y relaciones entre las variables mediante visualizaciones y estadísticas descriptivas.

      ![alt text](images/image-15.png)
---

   3. **Análisis de Calidad de los Datos**: Evaluar la calidad de los datos, identificando problemas como valores faltantes, inconsistencias, errores o duplicados.

      ![alt text](images/image-11.png)

      1. **Columnas con Mayor Cantidad de Datos Nulos:**
         * **precio_alquiler:** Presenta una gran cantidad de datos faltantes, lo que sugiere que muchos registros no tienen información sobre el precio de alquiler.
         * **precio_venta:** También muestra una cantidad significativa de datos nulos, indicando que el precio de venta no está registrado en muchos casos.
         * **superficie_venta:** Al igual que las anteriores, esta columna presenta muchos valores faltantes, lo que podría indicar que no se dispone de información sobre la superficie de venta en muchos inmuebles.

---

   4. **Análisis Gráfico de los Datos**: Representar gráficamente las variables mediante gráficos como histogramas, diagramas de dispersión, boxplots, entre otros, para facilitar la comprensión visual de los datos.

      ![alt text](images/image-5.png)

      ![alt text](images/image-7.png)

      ![alt text](images/image-6.png)

      ![alt text](images/image-8.png)

      ![alt text](images/image-9.png)

---
   5. **Segmentación Inteligente de los Datos**: Implementar técnicas de segmentación avanzadas que aporten valor al análisis y la extracción de insights relevantes.

      ![alt text](images/image-24.png) ![alt text](images/image-25.png)
      
      ![alt text](images/image-26.png) ![alt text](images/image-27.png) ![alt text](images/image-28.png) ![alt text](images/image-29.png)

---
   6. **Análisis de Correlación**: Evaluar las relaciones y asociaciones entre las variables mediante matrices de correlación y análisis de dependencias.

      ![alt text](images/image-10.png)

      1. **Relación fuerte entre `precio_alquiler` y `precio_venta`**:
         - Existe una correlación positiva alta (0.80), lo que indica que cuando el precio de alquiler aumenta, también tiende a aumentar el precio de venta. Esto sugiere una relación directa entre estos dos mercados.

      2. **Baja correlación entre `superficie_venta` y las demás variables**:
         - `superficie_venta` no muestra una correlación significativa con ninguna de las otras variables (valores cercanos a 0). Esto podría implicar que el tamaño no es un factor determinante en las variaciones de precio o que otros factores influyen más.

      3. **Relaciones negativas con `codi_districte` y `codi_barri`**:
         - Las variables `codi_districte` y `codi_barri` tienen correlaciones negativas con los precios (`precio_alquiler` y `precio_venta`), lo que podría reflejar diferencias geográficas: en ciertos distritos o barrios, los precios tienden a ser más bajos.

      4. **Alta correlación entre `codi_districte` y `codi_barri` (0.86)**:
         - Esto es lógico, ya que ambos códigos están relacionados jerárquicamente (barrios están dentro de distritos).

      ### Interpretación
      - La relación entre precios de alquiler y venta es clave para entender cómo se comportan estos mercados de forma conjunta.
      - La superficie parece no ser tan determinante, pero podría ser útil segmentar el análisis para evaluar relaciones específicas en ciertos barrios o distritos.
      - Las correlaciones con los códigos geográficos reflejan posibles patrones espaciales, que podrían analizarse más a fondo para identificar zonas con características particulares en los precios.


      ![alt text](images/image-12.png)

---

   7. **Análisis de Outliers**: Detectar y tratar los valores atípicos (outliers) presentes en los datos para mejorar la precisión de los modelos.

      ![alt text](images/image-4.png)

      ![alt text](images/image-13.png)

      ![alt text](images/image-14.png)

---
   8. **Análisis de Cohortes Avanzados**: Realizar segmentación y análisis del comportamiento de los usuarios a lo largo del tiempo, con el objetivo de identificar patrones de retención, uso y otros comportamientos clave.

      ### **Definición de las cohortes por métricas financieras**

      #### **1. Cohorte: Clase de Elasticidad del precio de compra medio en los últimos 10 años (`elasticidad_10y_stars`)**
      - **Definición**: 
      Esta cohorte clasifica los barrios en 5 clases según el cuartil de elasticidad del precio de compra medio. La elasticidad mide cómo responde el precio de compra de las viviendas a cambios en factores externos, como el nivel de ingresos, la oferta y demanda, o los cambios económicos. 
      - Barrios con elasticidad alta: Responden significativamente a las fluctuaciones del mercado.
      - Barrios con elasticidad baja: Presentan precios más estables.

      ![alt text](images/image-30.png)

      - **Utilidad**: 
      - Identificar barrios con mayor volatilidad para inversores con mayor tolerancia al riesgo.
      - Detectar zonas con precios estables para inversiones conservadoras.
      - Analizar la sensibilidad de los barrios a cambios macroeconómicos, ayudando a prever posibles riesgos o ventajas en futuros escenarios.

      ---

      #### **2. Cohorte: Clase de Rentabilidad de inversión media en los últimos 10 años (`rentabilidad_10y_stars`)**
      - **Definición**: 
      Clasifica los barrios en 5 clases basándose en el cuartil de rentabilidad media (bruta o neta) generada por la inversión en propiedades en los últimos 10 años. La rentabilidad mide el retorno económico generado, comparando ingresos por alquiler o revalorización con el coste inicial de la inversión.

      ![alt text](images/image-21.png)

      - **Utilidad**:
      - Identificar los barrios más rentables para maximizar el retorno económico.
      - Comparar la relación entre rentabilidad y riesgo (elasticidad o estabilidad de precios).
      - Evaluar la sostenibilidad de rentabilidades pasadas en el contexto actual del mercado inmobiliario.
      - Segmentar inversores según su enfoque (rentabilidad a corto plazo vs. revalorización a largo plazo).

      ---

      #### **3. Cohorte: Clase de Crecimiento acumulado del precio de alquiler medio en los últimos 10 años (`grow_acu_alquiler_10y_stars`)**
      - **Definición**: 
      Esta cohorte clasifica los barrios en 5 clases según el cuartil de crecimiento acumulado en el precio medio del m² de alquiler en la última década. El crecimiento acumulado refleja la capacidad del barrio para atraer demanda y adaptarse a cambios en el mercado de alquiler.

      ![alt text](images/image-22.png)

      - **Utilidad**:
      - Identificar barrios con alta demanda de alquiler (zonas emergentes o consolidadas).
      - Evaluar oportunidades para inversión en alquiler basándose en tendencias históricas.
      - Analizar la relación entre el crecimiento del alquiler y otros indicadores (ingresos de la población, nuevas infraestructuras, etc.).
      - Diseñar estrategias de marketing o posicionamiento para propiedades en zonas de rápido crecimiento.

      ---

      #### **4. Cohorte: Clase de Crecimiento acumulado del precio de compra medio en los últimos 10 años (`grow_acu_venta_10y_stars`)**
      - **Definición**: 
      Clasifica los barrios en 5 clases basándose en el cuartil de crecimiento acumulado en el precio medio del m² de venta en los últimos 10 años. Representa la capacidad de revalorización de las propiedades en cada barrio.

      ![alt text](images/image-23.png)

      - **Utilidad**:
      - Identificar barrios con alta revalorización para inversiones a largo plazo.
      - Detectar áreas en declive o con crecimiento moderado, que puedan representar oportunidades de compra a precios reducidos.
      - Evaluar la correlación entre el crecimiento del precio de venta y factores como la calidad de vida, inversiones en infraestructuras o evolución socioeconómica de la zona.
      - Prever el impacto de nuevas normativas o cambios en la dinámica del mercado en el crecimiento futuro.

      ---

      ### **Insights relevantes que se pueden extraer**
      1. **Análisis de rentabilidad vs. riesgo**: 
         Comparando `elasticidad_10y_stars` con `rentabilidad_10y_stars`, es posible identificar barrios con rentabilidad alta pero riesgo bajo (ideal para inversiones conservadoras) o barrios de alta elasticidad y alta rentabilidad (para inversores agresivos).

      2. **Oportunidades de crecimiento**: 
         Relacionando `grow_acu_alquiler_10y_stars` y `grow_acu_venta_10y_stars`, se pueden identificar áreas con alta demanda de alquiler y revalorización de propiedades, óptimas para inversiones mixtas (compra para alquilar y reventa).

      3. **Estrategias específicas por perfil de inversor**: 
         - **Inversores a corto plazo**: Priorizar barrios con alta rentabilidad y elasticidad moderada.
         - **Inversores a largo plazo**: Enfocarse en zonas con alto crecimiento acumulado en venta y estabilidad de precios.

      4. **Identificación de zonas emergentes**:
         Comparando `grow_acu_alquiler_10y_stars` y `elasticidad_10y_stars`, se pueden detectar barrios con demanda creciente y precios aún moderados, indicando potencial para revalorización futura.

      5. **Impacto de factores externos**:
         Analizando cómo la elasticidad varía entre barrios, es posible prever qué áreas serán más sensibles a cambios en normativas, tasas de interés o dinámica de oferta/demanda.

      6. **Clasificación competitiva de barrios**: 
         Usando las cohortes como base, es posible elaborar rankings de barrios para orientar a inversores o agentes inmobiliarios.

      ### **Conclusión**
      Estas cohortes permiten segmentar el mercado inmobiliario de forma avanzada, ofreciendo insights útiles para optimizar decisiones de inversión, diseño de políticas públicas o estrategias comerciales. Su combinación potencia el análisis multidimensional, ajustado a distintos perfiles y objetivos. 

      ---

      ### **Descripción de la cohorte `cohortes_distrito`**

      ![alt text](images/image-19.png)

      La cohorte `cohortes_distrito` se genera a partir de los datos del dataset agrupados por **distrito** (`codi_districte`) y **año** (`año`), con el objetivo de analizar las tendencias de los precios de alquiler y venta en diferentes distritos de Barcelona a lo largo del tiempo.

      #### **Estructura de la cohorte `cohortes_distrito`**

      1. **Identificador de cohorte**: La cohorte se define como la combinación del `codi_districte` (que representa el distrito de la ciudad) y el `año` de la fecha del dato (`mes` transformado en año). Así, cada fila del DataFrame representa un distrito y el año de las mediciones de precios, lo que permite observar cómo han evolucionado los precios de alquiler y venta en ese distrito a lo largo del tiempo.
         
         - **Cohorte**: `cohorte_distrito = codi_districte + '-' + año`

      2. **Variables principales**:
         - **`alquiler_medio`**: Precio medio de alquiler en ese distrito y año.
         - **`venta_media`**: Precio medio de venta en ese distrito y año.
         - **`codi_districte`**: Código del distrito, que se usa para identificar el área específica de Barcelona.
         - **`año`**: El año de la medición, extraído de la columna `mes`.

      ### **Insights relevantes que se pueden extraer de la cohorte `cohortes_distrito`**

      1. **Análisis geográfico a nivel distrital**:
         - **Diferencias regionales**: Los distritos de Barcelona suelen presentar características socioeconómicas distintas. Algunos pueden ser más turísticos, otros más residenciales o comerciales, lo que afecta tanto a la oferta como a la demanda de propiedades. Al crear una cohorte basada en el distrito y año, se puede observar cómo evoluciona el mercado de precios en diferentes áreas de la ciudad.
         - **Estabilidad local**: El análisis de los precios por distrito permite observar si ciertas zonas experimentan una estabilidad o fluctuaciones a lo largo del tiempo, lo que puede ser valioso para inversores, planificadores urbanos y ciudadanos interesados en las tendencias inmobiliarias.

      ![alt text](images/image-17.png)
      
      2. **Evolución temporal de los precios**:
         - Al agrupar los datos por año, es posible identificar si los precios de alquiler y venta en un distrito aumentan, disminuyen o permanecen estables a lo largo del tiempo. Esto puede reflejar factores como la gentrificación, cambios en la infraestructura, o políticas urbanísticas locales.
         - **Estacionalidad**: Además de observar las tendencias anuales, esta cohorte podría ser útil para detectar patrones estacionales si se desglosara aún más en base a meses o trimestres.


      ![alt text](images/image-18.png)


      3. **Impacto de factores externos**:
         - Las variaciones de los precios en los distritos podrían estar influenciadas por eventos o decisiones fuera del control de los individuos, como el desarrollo de infraestructuras, cambios en las leyes de arrendamiento, o proyectos urbanísticos. Esta cohorte ayuda a estudiar cómo esos factores afectan a cada distrito de manera distinta.

      4. **Segmentación para análisis detallados**:
         - La cohorte por distrito permite realizar un análisis más granular, lo que facilita la toma de decisiones específicas para cada zona. Por ejemplo, si un distrito muestra un aumento considerable en los precios, podría ser un indicativo de que la zona está siendo más demandada o que está pasando por un proceso de renovación o desarrollo.
         - Las políticas urbanísticas o el desarrollo económico podrían ser analizados en función de cómo afectan a los diferentes distritos. Si el distrito con un alto índice de precios sube significativamente, se podría investigar si el área está siendo renovada o si tiene un crecimiento económico.

      ![alt text](images/image-16.png)

      ### **Conclusión**
      La cohorte `cohortes_distrito` es valiosa porque permite hacer un análisis detallado de la evolución de los precios inmobiliarios en Barcelona, proporcionando información útil tanto para analistas de datos como para los responsables de la toma de decisiones en planificación urbana, inversión inmobiliaria y desarrollo económico.




---

1. **Modelamiento**: Se desarrollarán modelos de aprendizaje automático (ML) para predecir la rentabilidad futura de una inversión inmobiliaria y el retorno sobre la inversión (ROI).

   9. **Modelos de Regresión Regularizados**: Implementar modelos de regresión regularizados (como Ridge, Lasso, ElasticNet), utilizando técnicas de búsqueda de hiperparámetros para optimizar el rendimiento del modelo.

      ![alt text](images/image-20.png)

---

   10. **Modelos de Clasificación**: Desarrollar y optimizar modelos de clasificación (como árboles de decisión, SVM, k-NN), utilizando los métodos adecuados de validación y evaluación.
---
   11. **Validación de Modelos**: Seleccionar los mejores modelos mediante validación cruzada con k-fold, para asegurar la robustez y generalización de los modelos creados.
         - Modelo de regresión para interpolación para rellenado de precios faltantes
         - Modelo de clasificación para predecir la ocupación del inmueble
         - Modelo de extrapolación para predicción de precios actuales y futuros
         - Uso de Modelos generativos DDL para interpretar las propiedades
---

1. **Desarrollo**: Se desarrollarán un sistema de recuperación de información y recomendación de inversiones inmobiliarias basado en los modelos desarrollados.

   12. **Uso de Scraping para Variables Exógenas**: El proyecto debe incluir el uso de técnicas de web scraping para obtener variables adicionales de fuentes externas que aporten valor a los datos originales del proyecto.
         - Scrapping de una web para extraer datos del inmueble necesarios para realizar la valoración de la inversión
   - Generación del informe de valoración de la inversión del inmueble

### **2.1. Definición del objetivo**
- **Objetivo general**: Analizar la evolución y las diferencias en los precios por metro cuadrado de alquiler y venta en los distritos y barrios de Barcelona para identificar tendencias, disparidades y posibles oportunidades de mercado.
- **Preguntas clave**:
  - ¿Qué distritos tienen los precios más altos/bajos de alquiler y venta?
  - ¿Qué relación existe entre los precios de alquiler y venta?
  - ¿Cómo han evolucionado los precios en los últimos años?
  - ¿Hay distritos con mayor estabilidad o volatilidad en los precios?


### **2.2. Preparación de los datos**
1. **Exploración inicial**:
   - Revisión de las columnas: tipo, nombre, orden, mes, precio_alquiler, precio_venta, codi_districte, nom_districte, codi_barri.
   - Identificación de valores nulos (e.g., "NaN" en precio_venta) y duplicados.
   - Validación de consistencia entre las fechas y las ubicaciones (mes y codi_districte).

2. **Limpieza**:
   - Rellenar o eliminar valores faltantes según el análisis (e.g., imputación con la media, mediana o interpolación temporal para precios faltantes).
   - Transformar las fechas (columna "mes") al formato datetime para facilitar el análisis temporal.

3. **Enriquecimiento**:
   - Calcular indicadores adicionales como:
     - Relación alquiler/venta (\( \text{precio\_alquiler} / \text{precio\_venta} \)).
     - Tasa de crecimiento trimestral/anual de precios.

---

### **2.3. Análisis exploratorio**
1. **Análisis descriptivo**:
   - Calcular medias, medianas, y rangos intercuartílicos para alquiler y venta.
   - Comparar precios entre distritos y barrios.

2. **Visualización de datos**:
   - Gráficos de líneas: evolución temporal de los precios por distrito.
   - Mapas de calor: distribución geográfica de precios.
   - Gráficos de dispersión: relación entre alquiler y venta.

3. **Segmentación**:
   - Clasificar distritos/barrios en rangos de precios (e.g., bajo, medio, alto).
   - Identificar distritos con mayor volatilidad.

---

### **2.4. Análisis avanzado**
1. **Correlaciones**:
   - Evaluar la relación entre precios de alquiler y venta.
   - Explorar posibles factores externos (e.g., desarrollo económico, densidad poblacional).

2. **Tendencias temporales**:
   - Identificar picos o caídas significativas en precios.
   - Evaluar estacionalidad y patrones anuales.

3. **Comparación de rentabilidad**:
   - Estimar la rentabilidad bruta de inversión en cada barrio (\( \frac{\text{precio\_alquiler} \times 12}{\text{precio\_venta}} \)).

---

### **2.5. Interpretación de resultados**
- Elaborar un ranking de distritos según:
  - Precio medio de alquiler y venta.
  - Relación entre alquiler y venta.
  - Rentabilidad de inversión.
- Identificar áreas con oportunidades de mercado (e.g., alta rentabilidad o precios estables).

---

### **2.6. Presentación del análisis**
1. **Informe estructurado**:
   - Introducción: contexto y objetivo del análisis.
   - Metodología: pasos seguidos para limpiar, analizar y visualizar los datos.
   - Resultados clave: patrones, tendencias y rankings destacados.
   - Conclusiones: insights sobre el mercado inmobiliario.
   - Recomendaciones: áreas para inversión o acciones específicas.

