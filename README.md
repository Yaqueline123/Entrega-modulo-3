---------------- ✨ CONSULTAS Y FILTROS EN SQL 

/* ✎ Actividad práctica: consultas, filtros y expresiones en SQL Server

En este bloque vamos a trabajar con consultas sobre la tabla de RetailPro_Base para comprender cómo seleccionar columnas, filtrar registros, interpretar valores NULL y construir nuevas salidas a partir de operadores y funciones. El objetivo es que practiquen cómo recuperar información útil, aplicando distintos criterios de búsqueda, comparación y transformación de datos.

Durante la actividad veremos cómo:
✅ seleccionar columnas específicas,
✅ usar alias para mejorar la lectura,
✅ filtrar filas con WHERE,
✅ consultar valores NULL correctamente,
✅ aplicar operadores relacionales y lógicos,
✅ construir filtros avanzados con LIKE, IN y BETWEEN,
✅ realizar cálculos aritméticos,
✅ y dar formato a resultados numéricos.
*/

/*======================= EXPLORACIÓN Y SELECCIÓN DE COLUMNAS ==============================*/

------


-- Una lista de países sin repetir.


/*======================= OPERADORES RELACIONALES ==============================*/

/* MENOR QUE (<)
Filtrar registros cuyo valor sea menor al indicado en la condición. 
En este caso, mostrar ventas cuyo precio unitario sea inferior a 50. */



/* DISTINTO DE (!=) (otro modo <>)
Filtrar registros cuyo valor sea diferente al especificado. 
En este ejemplo, mostrar todos los países registrados excepto Argentina. */




/*======================= OPERADORES LÓGICOS ==================================*/

/* AND
Mostrar únicamente los registros que cumplen ambas condiciones al mismo tiempo. 
En este caso, ventas con un monto total elevado y realizadas en el segmento Premium. */




/* OR
Mostrar registros que cumplan al menos una de las condiciones indicadas. 
En este ejemplo, transacciones pagadas con Tarjeta de Crédito o Tarjeta de Débito. */



/* NOT
Excluir del resultado los registros que cumplan una condición específica. 
En este caso, mostrar todas las ventas excepto las de la categoría 'Tecnología'. */




/*======================= FILTROS AVANZADOS: LIKE, IN, BETWEEN ================*/

/* LIKE 'L%'
Filtrar registros de texto que comienzan con una letra o patrón específico. 
En este ejemplo, mostrar productos cuyo nombre empieza con la letra L (ej: Laptop). */



/* LIKE 'PRD-_07'
Filtrar valores que sigan una estructura específica usando comodines. 
En este caso, códigos de producto que empiezan con PRD-, tienen un carácter variable y terminan en 07. */



/* LIKE '%Mesa%'
Buscar textos que contengan una palabra o fragmento en cualquier posición. 
En este ejemplo, correos electrónicos corporativos o personales que contengan la palabra 'medina'. */



/* LIKE '[A-M]%'
Filtrar registros cuyo texto comience dentro de un rango de caracteres. 
En este caso, ciudades que empiezan con letras entre la A y la M. */



/* IN
Filtrar registros cuyos valores pertenezcan a una lista específica. 
En este ejemplo, mostrar ventas realizadas en Brasil, Chile o Uruguay. */



/* BETWEEN
Filtrar registros que se encuentren dentro de un rango numérico o de fechas. 
En este caso, transacciones con un MontoTotal entre 200 y 500 inclusive. */





/*======================= MANEJO DE VALORES NULL ==============================*/

/* IS NULL
Filtrar registros donde la columna especificada no contenga ningún dato almacenado.
En este caso, buscar transacciones donde la Cantidad quedó vacía o nula. */




/* IS NOT NULL
Filtrar registros para asegurar que la columna indicada contenga un valor válido.
En este ejemplo, listar las ventas que sí tienen el cálculo del MontoTotal registrado. */





/*======================= OPERADORES ARITMÉTICOS ===============================*/

/* MULTIPLICACIÓN (*)
Crear una nueva columna calculada multiplicando dos valores numéricos fila por fila. 
En este ejemplo, recalculamos el monto total multiplicando el precio unitario por la cantidad. */




/* DIVISIÓN (/) Y NULLIF
Realizar un cálculo entre columnas evitando errores de división por cero. 
Para este escenario simulado, calculamos un "Precio Promedio Ajustado" dividiendo el monto total por la cantidad, 
reemplazando temporalmente el valor 0 por NULL mediante NULLIF para evitar que la consulta falle. */






/*======================= FORMATEO NUMÉRICO ===================================*/

/* ROUND
Redondear un valor numérico a una cantidad específica de decimales. 
En este ejemplo,redondea a 1 decimal. */





/* CAST
Convertir un valor de un tipo de dato a otro. 
En este caso, transformar de decimal en un número entero para simplificar la vista. */





/* FORMAT
Convertir un número en texto con un formato visual específico. 
En este ejemplo, dar formato monetario con signo de pesos y separador de miles a la columna MontoTotal. */






/*======================= ORDENAMIENTO Y SELECCIÓN =============================*/

/* ORDER BY
Ordenar los resultados de una consulta según una columna específica. 
En este caso, mostrar las ventas del segmento Premium ordenadas por MontoTotal de mayor a menor. */





/* TOP
Limitar la cantidad de registros devueltos por la consulta. 
En este ejemplo, mostrar solo las 5 transacciones con mayor cantidad de productos comprados. */





/*======================= AGRUPACIÓN Y FILTROS SOBRE AGREGADOS ================*/

/* GROUP BY & AGREGACIÓN
Agrupar los registros que comparten un mismo valor para resumir la información por categoría. 
En este caso, reunir los datos por Categoría para calcular el dinero total recaudado (SUM) y cuántas ventas se hicieron (COUNT). */




/* HAVING
Filtrar los resultados después de haber realizado la agrupación. 
A diferencia de WHERE, HAVING evalúa las funciones de agregado. 
Aquí mostraremos únicamente los medios de pago cuyo total acumulado supere los 10000. */
