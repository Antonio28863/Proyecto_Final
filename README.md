# Proyecto_Final
EDA y Dashboard de global_superstore.

# Descripción:
Partimos de un archivo csv y dos archivos de excel (Datos_Brutos).  

En python, utilizando la librería pandas, limpiamos los datos (Limpieza_Datos). Comenzamos cargando los archivos y haciendo una vista previa de lo que tenemos. Unimos en un único dataframe, ponemos gerente Canadá ya que no tenemos el nombre de este gerente. Traducimos el nombre de las columnas para trabajar con más claridad. Ponemos el id_venta como indice. Cambiamos de formato las fechas. Eliminamos la columna código postal, solo tenemos 9994 y trabajaremos con ciudad, país, etc. Se cambia ventas y beneficio de str a float. Creamos una función para quitar $ y comas. Cambiamos la columna devueltos a booleano. Guardamos los datos limpios (Datos_Limpios) 

Creamos un dashboard en Power Bi (Dashboard_Ventas). Cargamos el archivo de excel dataset_limpio. Hacemos unas pequeñas correcciones en las fechas y los números decimales. Cambiamos el booleano a devuelto si o no. Creamos una tabla con los datos por pedido con las columnas valor descuento y coste, la tabla sin devueltos y la tabla devoluciones. Creamos la medidas. Hacemos las relaciones entre las tablas. Creamos las tarjetas con los big numbers y algunos Kpis secundarios. El mapa con la facturación en el tamaño de la burbuja y la tasa de pedidos sin beneficio en el color. Se pone la leyenda en el mapa. Un gráfico histórico con la facturación y el beneficio. Colocamos filtros por producto y categoría, por tipo de cliente y por gerente. Se ponen colores en formato condicional, beneficio cambiará a rojo si es negativo, margen de beneficio verde por encima del 12% y rojo por debajo del 10%, el ticket medio rojo por debajo de 300 $, tasa de pedidos sin beneficio rojo por encima del 25% y verde por debajo del 15% y la tasa de devoluciones verde por debajo del 4% y rojo por encima del 8%.  

Con el archivo dataset_limpio.pkl hacemos el EDA en python utilizando pandas (EDA.ipynb). Separamos el dataframe en devueltos y no devueltos. Calculamos el beneficio dependiendo del descuento, los paises con más y menos beneficio, los pruductos con mas y menos beneficios. Creamos los dataframes pedidos y pedidos sin beneficio. Calculamos la tasa de pedidos sin beneficio por país. Creamos una tabla con la tasa de pedidos sin beneficio y el total de pedidos por cada país. Con estos datos y los obtenidos en el dashboard hacemos el análisis. 

# Análisis:
En rasgos generales las ventas aparentan buenos números con un margen de beneficio del 11%. El mayor problema es que hay casi un 25% de los pedidos que no dejan beneficios y generan pérdidas. Turquía con unas pérdidas de 93.000$ y un 100% de pedidos sin beneficio en 649 pedidos está a la cabeza de estos malos datos. Nigeria 78.000$ y Países Bajos 40.000$ de pérdias le siguen. En Argentina un 90% de los 183 pedidos y en Honduras un 88% de 327 dan pérdidas. Hay una lista de más de 20 países con una cantidad de pedidos reseñable con más de la mitad de los pedidos con pérdidas. Algo que se puede comprobar en el mapa del dashboard.  
En beneficios destaca Estados Unidos con 250.000$ aún teniendo un 20% de pedidos sin beneficio, consiguiendo un margen de beneficio del 12.2%. Le siguen China, India y Reino Unido.
El mayor problema para estos pedidos son los descuentos, a partir del 20% de descuento los beneficios caen dando lugar en algunos casos a estas pérdidas.  
Por producto, Canon imageCLASS 2200 Advanced Copier tiene unos beneficios de 25.200$, por otro lado, Cubify CubeX 3D Printer Double Head Print es el producto que más pérdidas deja (9.240$).

# Archivos adjuntos:
- Datos_Brutos
- Datos_Limpios
- Notebook (Limpieza_datos y EDA)
- Dashboard_Ventas

# Autor:
Antonio Fernández
@antonio28863
