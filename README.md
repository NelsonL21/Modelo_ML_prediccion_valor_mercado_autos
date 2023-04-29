# Modelo_ML_prediccion_valor_mercado_autos
Empleando métodos numéricos el servicio de venta de autos usados Rusty Bargain requiere  desarrollar una aplicación para atraer nuevos clientes. Gracias a esa app, puedes averiguar rápidamente el valor de mercado de tu coche.

## **Conclusión general**

Primeramente, al realizar el análisis de los datos, se observa que la cantidad de nulos es considerble y al tratarse de observaciones categóricas, en este caso, no sería correcto que sean sutituidas por los valores más communes como la moda, o por alguna distribución aleatoria, ya que entrenaríamos al modelo con modelos de autos innexistentes, lo cual puede que a futuro ocacione algun error que conlleve a una mala predicción. Es por ello que se opta por borrarlos, ya que el porcentaje de perdedia oscila en el 20% de los datos, y aunque esto representa un 1/5 de los mismos, es un mal necesario para garantizar que el modelo funciona adecuadamente.

### **Resultado de los modelos**

#### **Regresión lineal**

Tarda 4us segundos es casi instantaneo, sin embargo su RMSE es de 67.32% lo cual habla de una calidad de modelo bastante baja

#### LGBMRegressor

Este código tiene una RMSE de 34.72% casi la mitad del anterior, siendo bastante eficiente, y al mismo tiempo solo tarda 8 us en ejecutarse, un poco superior sin embargo bastante rápido.

#### CatBoost

Así mismo,revisando el algoritmo de CatBoost, podemos observar que en 200 iteraciones logró un RMSE de 35.2 % en tan solo 4 us, siendo bastante rapido, y con una diferencia de solo 1.18% entre el modelo de LGBM y el de CatBoost

#### Arbol de decisión aleatorio

Se obtuvo un RMSE del 30.94% el más bajo hasta ahora, obteniendo incluso un timepo de ejecución de 4 us. Siendo el que mejor calidad aporta hasta ahora, y el más rápido.

Se puede concluir que luego de realizar un análisis de los datos, eliminar aquellos que no servian para el análisis y porbar 4 modelos diferentes, se llega a la conclusión general que el modelo que aporta un menor RMSE es el arbol de desición el cual empleó un método de validación cruzada, y con ello se llegó al mejor resultado posible. 
