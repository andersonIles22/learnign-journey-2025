## Diciembre 16, 2025 - Day 1
** Horas código:** 1h
**Project:** notes-api setup
**Completed:**
Creé un miniproyecto node.js desde cero
Instale los paquetes necesarios como pg y dotenv
condiguré estructura de carpetas
escribí databas.js y copié un codigo que utiliza el modulo pg
Primier commit en Git, aunque no se que es un commit1
Subí a github con mi pana el chatgpt

**Mañama Dec 17:**
-Instalar PostgreSQL localmente
- Crear base de datos notes_db
- Probar conexión desde node.js
- Comenzar endpoint GET api/notes
**Project:** Conexión funcional entre Node.js y PostgreSQL, mas primeras queries exitosas
**Completed:**
Establecer un archivo .env con la URL de PostgreSQL
Establecer que el archivo .env no se suba al gitHub
Crear una base de datos y una tabla "notes"
Escribir un script para verificar si existe una conexión exitosa con Node.js y PostgreSQL
Escribir un script para insertar 3 filas a la tabla "notes"
Escribir un script para leer todas las filas de la tabla "notes"
Escribir un script para actualizar cierta fila especifica
Escribir un script para eliminar cierta fila especifica
**Learned:**
- Instale PostgreSQL, luego me dí cuenta que ya tenía instalado xd. Dado que utilizaba pgadmin4 e instale PostgreSQL
- Mediante la terminal PowerShell logré acceder a mi base de datos ya creada, adicionalmente creé otra base para práctica con Node.js
- Establecí el archivo ".env" que supongo que almacena las credenciales para conectarse al mi Base de datos, pues ahí establecí una LLAVE=VALOR donde usé formato URL de PostgreSQL. Lo que me dí cuenta que mi constraseña se guaradaba en texto plano.
- Establecí el archivo ".env" en el archivo ".gitignore" para no permitir que se suba a la nube, en este caso gitHub el archivo ".env" con información delicada.
- Con la guía de gemini logré escribir un test_connection.js para confirmar si establecí conexión con la base de datos ejecutando el script. Donde conocí el constructor new Pool, para utilizarlo para crear instancias con el URL de PostgreSQL guardado en el archivo ".env". Luego utilice "pool.query" para ejecutar ciertas consultas o ejecutar comandos en la base de datos mediantes scripts escritos, estos script fueron para insertar, recuperar, actualizar y eliminar filas. Y siempre establecer "pool.end()" para finalizar la conexión por cada ejecución de comandos en la base de datos, sea exitosa o no para que Node.js no se quede "colgado" debido a las conexiones a la DB siguen abiertas hasta no cerrarlas. Esto es necesario cuando solo se realiza scripts con una sola ejecución, si en ejecuta en aplicaciones web como Express se terminará todas la conexiones, y en producción no es recomendado al menos que de apaques el servidor PostgreSQL.

- En cada script creado se utilizó asycn/await. Se utilizó "await promise.all" para las insercciones y "finally" para finalizar la conexión entre Node.js y PostgreSQL con "await pool.end()". Se utiliza await en estas ejecuciones dado que se esta utilizando async/await.
- Comprender como gestionar el "resultado" devuelto por "pool.query" Para mostrar resultado en la consola y como funciona el RETURNING *
**Tiempo trabajado:**
Mé tomo 10 horas en finalizar estas tareas, waos 
y eso que tomé las horas del 18 de Diciembre. 
**Temas que tomó tiempo entender:**
- No conocía nada el modulo "pg" y peor de su constructor "Pool" 
- No le comprendía bien sobre que hacía "pool.query"
- No recordaba bien como funcioná async/await, promise.all(), finally() 
- Tuve que comprender algo por lo menos sobre lo que devuelve el "pool.query" para poder gestionar el objeto con metadatos.
**Mañama Dec 19:**
-Instalar PostgreSQL localmente
- Crear base de datos notes_db
- Probar conexión desde node.js
- Comenzar endpoint GET api/notes
