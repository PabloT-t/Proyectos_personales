# Modelos de Exploración y Operaciones Mineras (Proyecto Demo)

Repositorio con notebooks en Python para simular y analizar
un yacimiento de cobre tipo IOCG/manto, inspirado en faenas 
de la Faja de Hierro chilena (Mantoverde, Costa Fuego, etc.).

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
