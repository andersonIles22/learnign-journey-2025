# Semana 9
## Meta de Hora: Aproximadamente 20 horas
## Compromiso
- Cumplir con los tiempos de estudio para no estudiar hasta tarde con tal de cumplir las horas.
- No compensar días malos con días intensos
- No estar bloqueado en un tema por mas de 30-45min
- Entregar reporte Cada tercer día
## Tareas Pendientes:
Manteniendo la misma tarea de la anterior semana no completada

- Agregar paginación a los endpoint /posts/:post_id
- Añadir filtración de autor y estado de publicación
- Agregar PATCH y DELETE a las /post/:post_id (Middleware auth y función Middleware isOwnerOrAdmin)
- Testing exhaustivo para que todos los endpoints funcionen.

## Febrero 9, 2026 - Day 1
**Horas Trabajado:** 5.5 Horas
- Añadir paginación al endpoint de /posts/:post_id y /posts/:post_id/comments/

**Completed:**
- Complementar el uso de LIMIT y OFFSET en SQL
- Uso de parametros de query de la ruta req.query
- Usar de {mergeParams:true}
- Añadir validaciones de post_id

**Learning**
- Como establecer los parametros en las rutas y como usarlas usando req.query
- Manejo de paginación, establecimiento de valores page y limit para obtener el valor offset.

**Mañama  Febrero 10:**
- Añadir función de filtración por autor y estado de publicación

## Febrero 10, 2026 - Day 2
**Horas Trabajado:** 2 Horas
**Project:** 
- Agregar filtración por autor y estado de publicación añadiendo mas parametros al query de la ruta.

**Completed:**
- La función de paginación es compatible con la función de filtración por autor y estado de publicación, y en caso de no tener posts se retorna un array vacío.

**Learned:**
- Utilzar la librería matchedData que nos facilita la obtención de los parametros especificos, una alternativa a usar req.query.
- matchedData nos permite obtener aquellos parametros que hayan cuplido las reglas que establecieron en las validaciones de entradas. Y no parametros ramdos.
**Mañama  Enero 13:**
- Agregar que los endpoints PATCH y DELETE solo para el propietario o de roles permitidos

## Febrero 11, 2026 - Day 3
**Horas Trabajado:** 4.5 Horas
**Project:** 
- Agregar un middleware que permita identificar si es propietario o de rol permitido

**Completed:**
- La función middleware permite verificar si es usario propietario o de rol admin, para poder editar o eliminar un post.

**Learned:**
- Complementar como funciona el motor PostgreSQL ante el uso de placeholders en el prepared statement por cuestiones de que primero parsea, luego planea y finalmente sustituye valores. Por lo cual se recomienda interpolación de cadenas.
- Los middlewares son optimos cuando se puede reutilizarlos, por lo que el middleware recibe parametros de roles que pueden ser cambiados y el nombre de la tabla y campo.

**Mañama  Enero 13:**
- Afinar la función middleware

## Febrero 11, 2026 - Day 4
**Horas Trabajado:** 1.5 Horas
**Project:** 
- Evitar que se pueda hacer SQL injection en el middleware

**Completed:**
-  Utilizar recursos centralizados para evitar sql injections, sea mas dinamico el middleware y más legible

**Learned:**
- Establecer recursos que puedan ser reutilizados en otras rutas es optimo para evitar redundacia al validar los parametros que se pasen a la función del middleware.
- Se recomiendo utilizar "listas blancas" para solo permitir ciertos parametros y no tener sql injections por parametros dinamicos o externos. 

**Mañama  Enero 13:**
- Establecer tabla categories y relación N:M
- listar posts por categorias
