# Modelos de Exploración y Operaciones Mineras (Proyectos Demo)

Repositorio con notebooks en Python para simular y analizar
un yacimiento de cobre tipo IOCG/manto, inspirado en faenas 
de la Faja de Hierro chilena (Mantoverde, Costa Fuego, etc.).

*Debo aclarar que estos proyectos utilizan IA Generativa como asistente técnico para acelerar la implementación de código y depuración, logrando crear este repositorio en 4-7 dias con diversas aplicaciones. Lo anterior no quita el hecho de que se reviso linea por linea la sintaxis y logica de cada codigo. Mi pensamiento personal, es que las herramientas que pueden acelerar cosas que se hacen en meses a dias, pueden explotarse responsablemente. Porque no sirve tener los mejores datos si no explotamos todo el potencial tecnológico disponible para revelar su valor.*

## Contenido
###**Están en revisión para mezclar algunos o complejisarlos un poco más, ya que algunos son muy redundantes**###
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

**Prospectividad IOCG (Data Fusion) - ModeloProspectividad_Atacama_ML.ipynb**

Objetivo: Generación de blancos de exploración para depósitos IOCG en la Franja de Atacama.

Metodología:

Data Fusion: Integración de Geofísica Aeromagnética (TMI), Teledetección (ASTER L1T) y Geología Vectorial (Sernageomin).

Ingienería de características: Implementación de Lógica Difusa (Fuzzy Logic) para modelar control estructural y Isolation Forest para detección de anomalías espectrales.

Machine Learning: Random Forest Classifier con balanceo de clases (Undersampling).

Validación: Rigurosa Spatial Cross-Validation (Bloques Espaciales) para evitar sesgos de autocorrelación, logrando un AUC ~0.67 en zonas desconocidas.

*Nota Técnica: Este modelo constituye una Prueba. Los parámetros de influencia geológica son estimaciones teóricas para validar el flujo de trabajo computacional.*
