![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)


# Proyecto individual 2
​
¡Bienvenidos al segundo proyecto! Durante estos días estarán poniendo en práctica sus habilidades en el campo de la predicción. Deberán usar cierta métrica para medir la performance del modelo la cual, a su vez, será usada para elegir los mejores modelos.

## Mercado inmobiliario
​
Dentro de la sociedad globalizada e industrializada, es sabido que los precios de los inmuebles han presentado un constante cambio, por lo que quienes deseen invertir o vender una propiedad se enfrentan al fenómeno especulativo existente en la valorización de éstos. Esto, debido a la constante tendencia de las ciudades a crecer demográfica y comercialmente, llegando a un punto en donde no se tiene certeza de la valorización real dentro del sector en donde se desee invertir. 
​
Pese a que el precio depende, en cierta medida, de las tendencias que esté teniendo el mercado inmobiliario en un determinado tiempo, poder estimar adecuadamente el valor de una propiedad es una referencia clave para entender si es una buena oportunidad, ya sea de compra o de venta.
​
## Descripción del problema
​
Usted ha sido contactado de una importante empresa inversora dentro del rubro de la inmobiliaria en Colombia, con el fin de que implemente un modelo de clasificación que permita clasificar el precio de las propiedades en venta, utilizando los datos que se han puesto a su disposición correspondientes al año 2020.
​
Para esto, específicamente, debe predecir la **categorización** de las propiedades entre baratas o caras, considerando como criterio el valor promedio de los precios (la media). 

## Entreta trabajo

Se realizo un scrip en Jupyter Notebook .ipynb, el cual se realizaron los siguientes pasos: 
*carga y visualización de archivos* = Se cargaron los arcvivos de la fuente y los convertimos en un DF (DataFrame).
*Limpieza* = Los valores faltantes los cambiamos por la media de cada columna; limpiamos las columnas que utilizaremos para entrenar nuestro modelo
*Columna target (Objetico)* = Creamos esta columna con la siguiente instrucción 'df_train['target']= np.where(df_train['price'] >= df_train['price'].mean(), 1, 0)' Donde le decimos que si el precio es mayor o igual a la media de precio, le de un valor de 0 si el precio es economico y 1 es caro
*Variables X y Y de Train* = La variable 'X' contendra las Feactures con las cuales trabajaremos nuestro modelo de predicción y la 'Y' será nuestra feacture de target (Objetivo). --Debemos aclarar que con las mismas feactures en la variable X de train, trabajaremos con las de test--.
*Entrenamiento y predición* = Trabajaremos con KNN (K-Vecinos). Predecimos los valores de test en 0 y 1. Entrenamos nuestro modelo, predecimos y verificamos que ande bien nuestro modelo con las metricas *Recall, Acurracy, F1_score y precisión*
*Columna Pred* = Cuando predecimos el test nos dio un arreglo de 0 y 1. Ese arreglo lo convertimos en un DF y luego lon convertimosen un csv con los valores de nuestras prediciones.







