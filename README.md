# **Auditor de Logs y Guardrails para Prompts de IA Generativa**
Nivel: Intermedio
## **OBJETIVO DE NEGOCIO**
Supervisar el funcionamiento de un asistente de IA en producción para garantizar respuestas rápidas,
satisfactorias y libres de fugas de información confidencial.
## QUÉ DEBE HACER TU CÓDIGO (GUÍA DE TRABAJO)

**1- Detectar riesgos de seguridad (Guardrails): Revisar el texto de cada respuesta buscando si contiene alguna
de las palabras_prohibidas (sin importar si están en mayúsculas o minúsculas) y marcar esos
registros como alerta de seguridad.**

Cómo se procedio:

1. Crear una lista que ingresará las entradas con riesgo de seguridad*<br>
2. Crear un for que recorra la lista de entradas totales*<br>
3. Dentro de este for, usar condicionales para ingresar a nuestra lista estos que cumplen la condicion*<br>

**2- Evaluar rendimiento técnico: Identificar qué interacciones superaron el tiempo máximo de respuesta
permitido (3.0 segundos) y calcular el consumo total y promedio de tokens.**

Como se procedio:

1. Crear una lista que guardará las entradas que superen los 3 segundos*
2. Crear una variable numerica que calcula los tokens usados*
3. Sumar los tokens de cada entrada que recorre el for.* 
4. Similar al caso anterior usar un condicional para ingresar en la lista los elementos que duren más de 3 segundos
5. Calcular una media de los tokens usando el tamaño de la lista recorrida como numero por el que se divide la suma


**3-Medir satisfacción: Calcular el porcentaje de feedback positivo por categoría de consulta, ignorando los
casos donde el usuario no dejó valoración (None)**

Como se procedio:

1. Creamos un diccionario que guardará las categorías, y almacenará dentro dos variables, la primera será el feedback positivo, la segunda todo feedback que no sea none
2. Creamos multiples variables entradas con feedback valido y feedback positivo. Esto es un subapartado extra que hago como ampliacion, que calcula el porcentaje de manera general en vez de por categoria
3. Recorremos nuestra lista completa con un for. Por cada entrada obtenemos su feedback y categoría, y las guardamos en una variable
4. Si el feedback no es válido se pasa al siguiente, en caso de que si que sea un feedback valido (positivo o negativo) se procede
5. Si la categoria no existe aun en nuestro diccionario de categorias, se crea
6. A toda categoria se le suma una en sus feedbacks recibidos de manera predeterminada, en caso de que además de esto la critica sea positiva, se suma uno a su cantidad de feedbacks positivos
7. Se calcula la media de cada categoria y los generales, y se muestran en pantalla*

