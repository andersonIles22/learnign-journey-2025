# Semana 5
## Meta de Hora: Aproximadamente 32 horas
## Compromiso
- Cumplir con los tiempos de estudio para no estudiar hasta tarde con tal de cumplir las horas.
- No compensar días malos con días intensos
- No estar bloqueado en un tema por mas de 30-45min
- Entregar reporte Cada tercer día
## Enero 19, 2025 - Day 1
Se detallo en el anterio documento que fue usado para terminar la tarea de la semana anterior
**Horas Trabajado:** 8 Horas
## Enero 20, 2025 - Day 2
Sin realizar ninguna actividad 
**Horas Trabajado:** 0 Horas

## Enero 21, 2025 - Day 3
**Horas Trabajado:** 8 Horas
**Project:** 
- Añadir endpoits para obtener nuevos access token mediante el uso de refresh token y para actualizar contraseña de usuarios autenticados.

**Completed:**
- añadir la función de creación de un access token y refresh token al hacer request al endpoint /login.
- Validación de que el token sea valido y sea añadido en cada petición al servidor.
- Validación si el token ha sido revocado
- Validación de que el token refresh sea valido
- Validación de que el token refresh no este expirado.
- Añadir el endpoint ./refresh-token para emitir nuevo token cuando haya expirado usando el refresh token.

**Learned:**
- Utilizar bcrypt para hashear el token refresh.
- Añadir funciones para parsear el tiempo que se recibe como string y obtener el tiempo en milisegundos
- Añadir el campo isrevoked para verificar si el token refresh ha sido revocado para casos donde se haga logout o se le prohiba el acceso.
**Mañama  Enero 13:**
- Completar con añadir el endpoint /change-password para cambiar la constraseña del usuario.
- Aplicar el uso del middleware cookies-parse
- Enviar el token refresh al navegador para que sea almacenado en las cookies.

## Enero 22, 2025 - Day 4
**Horas Trabajado:** 5 Horas
**Project:** 
- Utilizar cookies-parser
- Añadir el endpoint /change-password

**Completed:**
- añadir el endpoint /change-password
- Validar que no se puede realizar el cambio el contraseña u obtener los usuarios despues de que el token access haya expirado. Incluso también cuando el token refresh haya expirado.
- User cookieParser() para procesar la cookie enviado por el navegador.

**Learned:**
- silent Refresh el proceso que permite que el usuario no tenga que hacer login cada vez que el token expire. Manteniendo la experiencia de usuario intacta.
- Recomendable eliminar el registro del token refresh almacenado en la base de datos por cada cambio de contraseña
**Mañama  Enero 13:**
- Implementación de roles en auth Api
- Documentación de auth api
- blog api setup
- crud posts basico