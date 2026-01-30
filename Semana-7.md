# Semana 7
## Meta de Hora: Aproximadamente 25 horas
## Compromiso
- Completar minimo 20 horas de estudio a la semana
- No estar bloqueado en un tema por mas de 30-45min
- Entregar reporte Cada domingo

## Enero 26, 2025 - Day 1
**Horas Trabajado:** 4.5 Horas
**Project:** 
- API Blog con crud basico
**Completed:**
- Solo establer el endpoint /api/auth/login y /api/auth/register.
- Creación de base de datos para registrar usuarios y almacenar los posts que se realizarán
- Comprobar que hacer POST a /login y /register funcionen. 

**Learned:**
- Puedo hacer estos endpoints funcionales sin mucha ayuda 
**Mañama  Enero 27:**
- Endepoint /api/posts/


## Enero 27, 2025 - Day 2
**Horas Trabajado:** 4 Horas
**Project:** 
- Añadir Endpoints /api/posts/
- Realizar post y get a /api/posts/  y que funcionen como deben.
**Completed:**
- Hacer request POST para postear y almacenar en la base de datos.  Estos necesitan el token que se obtiene al hacer login para realizar un posteo.
- Hacer request GET para obtener los post por ID y todos a la vez


**Learned:**
- Se debe definir muy bien y de manera cuidadosa las validaciones para no tener problemas al momento de hacer las requests a las rutas.

**Mañama  Enero 28:**
- Añadir endpoints para comentar y ver los comentarios

## Enero 28, 2025 - Day 3
**Horas Trabajado:**  0 Horas
**Justificación:**
Nada que mencionar, me dormí hasta tarde, y toda la tarde no hice nada. Pasé la tarde procrastinando. A las 6pm empecé a emsamblar un amplifcador hasta las 11 pm


## Enero 29, 2025 - Day 4
**Horas Trabajado:** 7.5 Horas
**Project:** 
- Añadir los endpoint /api/posts/:id  y /api/posts/:id/comments y que sean funcionales para realizar peticiones GET y POST. 
- Añadir PATCH a cada endpoint disponible /api/posts/:id
- Añadir validación de entrada para los posts y comentarios
**Completed:**

- Se añadió endpoints /api/posts/:id, /api/posts/:id/comments, para poder realizar GET Y POSTS para hacer publicaciones, realizar comentarios. Y PATCH para actualizar los posts existentes.
- Validación de las entradas al momento de postear, comentar y actualizar, como que el campo tittle y content no esten vacios al momento de postear. También se añadieron middleware para hacer posts, comentar y para actualizar, y asi no pueda cualquier usuario logeado actualizar publicaciones que no les pertenece.
- Se agregaron mensajes y valores nuevos de validación.
- Se cambio como los endpoints son usados para hacer publicaciones.


**Learned:**
 Establecer routes de forma jerarquica utilizando MergeParams, que al estar en true nos permite conectar un router dentro de otro.  Así permitiendonos reflejar la relación de datos en estructura de carpetas y rutas.
**Mañama  Enero 30:**
- Solo el autor puede editar y borrar sus posts y comentarios.
- Testing exhaustivo para que todos los endpoints funcionen.
- Actualizar README.
