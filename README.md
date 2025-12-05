# Modelos de Exploración y Operaciones Mineras (Proyectos Demo)

Repositorio con notebooks en Python para simular y analizar
un yacimiento de cobre tipo IOCG/manto, inspirado en faenas 
de la Faja de Hierro chilena (Mantoverde, Costa Fuego, etc.).

*Debo aclarar que estos proyectos utilizan IA Generativa como asistente técnico para acelerar la implementación de código y depuración, logrando crear este repositorio en 4-5 dias con diversas aplicaciones. Lo anterior no quita el hecho de que se reviso linea por linea la sintaxis y logica de cada codigo. Mi pensamiento personal, es que las herramientas que pueden acelerar cosas que se hacen en meses a dias, pueden explotarse responsablemente. Por que no sirve tener los mejores datos sino tienes las mejores herramientas.*

## Contenido

- `Exploracion_1.ipynb`: análisis exploratorio inicial, generación de un modelo simple. Con geoquimica y magnetometria simuladas, se añade tambien cercania
a fallas como proxy.
- `Exploracion_2.ipynb`: refinamiento del modelo de exploración, pruebas de distintos escenarios.
- `Exploración_prof.ipynb`: escenario en profundidad (sondajes).
- `Exploración_sup.ipynb`: escenario en superficie (e.g., mallas de datos geoquimicos)
- `Operaciones.ipynb`: modelo operativo sencillo que ataca posible problema(prediccion de bwi(dureza; Bond work index)); a partir de datos
que deberian existir previamente se simula la llegada de nuevos datos sin saber bwi y que el modelo predice a partir del entrenamiento previo.
Todo es simulado, pero se usa como referencia valores cercanos a los de mantos verdes para simular realidad. Tambien se aplica un analisis de
la mejor configuracion del metodo de entrenamiento para maximizar r2.

-------------------------------------------------------------------------------------

**Prospectividad IOCG (Datos Reales)**--->Modelo_prospectivo_Atacama_ML.ipynb

Objetivo: Generación de blancos de exploración para depósitos tipo IOCG en la Franja Ferrífera de Atacama, integrando teledetección y cartografía oficial.

Metodología

Datas: Integración de imágenes satelitales ASTER L1T (Bandas SWIR) con cartografía vectorial de Sernageomin (Fallas, Litología, Yacimientos).

Variables:

Cálculo de Ratios Espectrales para detección de alteración hidrotermal (Arcillas/Micas).

Aplicación de Lógica Fuzzy Sigmoidal para modelar la influencia decreciente de Fallas y Contactos Intrusivos.

Filtros litológicos para roca huésped favorable (Cretácico/Intrusivos).

Machine Learning: Entrenamiento de un Random Forest con: Optimización de Hiperparámetros (RandomizedSearchCV) y balanceo de clases (Estrategia de submuestreo 1:10).

Validación: Auditoría de robustez mediante Spatial Cross-Validation (K-Fold Espacial), logrando un AUC ~0.75 en zonas no entrenadas.

Nota Técnica: Este modelo constituye una Prueba. Los parámetros de influencia geológica son estimaciones teóricas para validar el flujo de trabajo computacional.
