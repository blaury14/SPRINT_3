# Proyecto: Sprint 3

## Descripción del Proyecto

¡Felicidades! Has terminado el sprint sobre análisis exploratorio de datos. Es momento de aplicar el conocimiento y las habilidades que adquiriste en un estudio de caso de análisis.

Para este proyecto, trabajarás con datos de Instacart, una plataforma de entregas de comestibles. Este conjunto de datos fue modificado del original lanzado por Instacart en 2017 para una competición en Kaggle. Redujimos el tamaño del conjunto para que tus cálculos se hicieran más rápido e introdujimos valores ausentes y duplicados.

Tu misión es limpiar los datos y preparar un informe que brinde información sobre los hábitos de compra de los clientes de Instacart. Después de responder a cada pregunta, escribe una breve explicación de tus resultados en una celda markdown de tu Jupyter notebook.

Este proyecto requerirá que hagas gráficos que comuniquen tus resultados. Asegúrate de que cualquier gráfico que vayas a crear tenga un título, ejes etiquetados y una leyenda si es necesario; e incluye `plt.show()` al final de cada celda con un gráfico.

## Diccionario de Datos

Hay cinco tablas en el conjunto de datos que tendrás que usar para el preprocesamiento y el análisis exploratorio de datos:

1. **instacart_orders.csv**: cada fila corresponde a un pedido en la aplicación Instacart.
   - `order_id`: número de ID que identifica de manera única cada pedido.
   - `user_id`: número de ID que identifica de manera única la cuenta de cada cliente.
   - `order_number`: el número de veces que este cliente ha hecho un pedido.
   - `order_dow`: día de la semana en que se hizo un pedido (0 si es domingo).
   - `order_hour_of_day`: hora del día en que se hizo el pedido.
   - `days_since_prior_order`: número de días transcurridos desde que este cliente hizo su pedido anterior.

2. **products.csv**: cada fila corresponde a un producto único que pueden comprar los clientes.
   - `product_id`: número ID que identifica de manera única cada producto.
   - `product_name`: nombre del producto.
   - `aisle_id`: número ID que identifica de manera única cada categoría de pasillo de víveres.
   - `department_id`: número ID que identifica de manera única cada departamento de víveres.

3. **order_products.csv**: cada fila corresponde a un artículo pedido en un pedido.
   - `order_id`: número de ID que identifica de manera única cada pedido.
   - `product_id`: número ID que identifica de manera única cada producto.
   - `add_to_cart_order`: el orden secuencial en el que se añadió cada artículo en el carrito.
   - `reordered`: 0 si el cliente nunca ha pedido este producto antes, 1 si lo ha pedido.

4. **aisles.csv**
   - `aisle_id`: número ID que identifica de manera única cada categoría de pasillo de víveres.
   - `aisle`: nombre del pasillo.

5. **departments.csv**
   - `department_id`: número ID que identifica de manera única cada departamento de víveres.
   - `department`: nombre del departamento.

## Instrucciones para Completar el Proyecto

### Paso 1: Abre los Archivos de Datos

- Abre los archivos de datos (`/datasets/instacart_orders.csv`, `/datasets/products.csv`, `/datasets/aisles.csv`, `/datasets/departments.csv` y `/datasets/order_products.csv`) y echa un vistazo al contenido general de cada tabla.
- Observa que los archivos tienen un formato no estándar, así que vas a necesitar establecer ciertos argumentos en `pd.read_csv()` para leer los datos correctamente.

### Paso 2: Preprocesa los Datos

- Verifica y corrige los tipos de datos (por ejemplo, asegúrate de que las columnas de ID sean números enteros).
- Identifica y completa los valores ausentes.
- Identifica y elimina los valores duplicados.
- Explica qué tipos de valores ausentes y duplicados encontraste, cómo los completaste o eliminaste y por qué usaste esos métodos.

### Paso 3: Análisis de Datos

#### [A] (deben completarse todos para aprobar)
1. Verifica que los valores en las columnas `order_hour_of_day` y `order_dow` de la tabla orders sean razonables.
2. Crea un gráfico que muestre el número de personas que hacen pedidos dependiendo de la hora del día.
3. Crea un gráfico que muestre qué día de la semana la gente hace sus compras.
4. Crea un gráfico que muestre el tiempo que la gente espera hasta hacer su próximo pedido, y comenta los valores mínimos y máximos.

#### [B] (deben completarse todos para aprobar)
1. ¿Hay alguna diferencia en las distribuciones de `order_hour_of_day` en miércoles y sábados? Traza los histogramas de ambos días en el mismo gráfico y describe las diferencias que observes.
2. Traza la distribución del número de pedidos que hacen los clientes y las clientas.
3. ¿Cuáles son los 20 principales productos que se piden con más frecuencia?

#### [C] (deben completarse todos para aprobar)
1. ¿Cuántos artículos compra la gente por lo general en un pedido? ¿Cómo es la distribución?
2. ¿Cuáles son los 20 principales artículos que se vuelven a pedir con más frecuencia?
3. Para cada producto, ¿qué proporción de sus pedidos se vuelven a pedir?
4. ¿Cuál es la proporción de productos pedidos que se vuelven a pedir para cada cliente?
5. ¿Cuáles son los 20 principales artículos que la gente pone en sus carritos primero?

## Contribución

Si deseas contribuir a este proyecto, por favor realiza un fork del repositorio y crea una pull request con tus mejoras. Asegúrate de que tu código sigue los lineamientos del proyecto y está bien comentado.

## Licencia

Este proyecto está bajo la licencia MIT. Para más detalles, consulta el archivo LICENSE.
