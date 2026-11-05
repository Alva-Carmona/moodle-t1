- Crear el rol

1.	Ir a Administración del sitio → Usuarios → Permisos → Definir roles
2.	Haz clic en "Agregar un nuevo rol"
3.	Configuración:

Nombre corto: revisor_calidad

Nombre completo: Revisor de calidad

Descripción: Rol con acceso solo lectura para revisar cursos sin capacidad de edición.

Arquetipo base: "Estudiante" (Student) — porque ya tiene capacidades de lectura básicas y lo modificamos en base a la petición.

Tipos de contexto habilitados: Marca al menos: 

Sistema
Categoría de curso
Curso
Actividad/recursos

- Ajustar capacidades

Con el estudiante ya tiene los permisos de edición y calificación limitados. Nos aseguramos de que en la lista de capacidades del rol se ha modificado para permitir o prohibir los siguientes permisos para completar el rol según la petición:

moodle/course:view - Permitir -	Para poder ver los cursos

mod/forum:viewdiscussion - Permitir	- Leer foros (sin publicar)

mod/forum:startdiscussion - Prohibido - No debe publicar en foros

moodle/course:manageactivities - Prohibido	Sin edición de actividades

moodle/grade:view
moodle/grade:viewall - Permitir - Para poder ver las calificaciones

moodle/course:viewparticipants - Permitir - Puede ver lista de participantes

moodle/site:viewreports
report/log:view - Permitir - Acceso a informes de logs

- Asignar el rol a un usuario de prueba en categoría

1.	Se va a Administración del sitio → Cursos → Administrar cursos y categorías
2.	Entra en una categoría existente o crea una nueva
3.	En la página de la categoría, ir a Más → Permisos → Asignar roles
4.	En el apartado "Revisor de calidad", busca y selecciona el usuario de prueba.
5.	Hacer clic en "Añadir"

- Añadir una sobrescritura local

1.	Se accede a un curso o actividad.
2.	Hay que ir a Permisos → Anulación de rol avanzada
3.	Hacer clic en el rol, en este caso "Revisor de calidad" en la lista
4.	Selecciona una capacidad para sobrescribir, por ejemplo: 
o	mod/forum:viewdiscussion → Cambia a "Prevenir"
5.	Guarda los cambios

Explicación: La sobrescritura a nivel de curso anula lo definido a nivel de categoría. Aunque el rol permite ver foros por defecto, en este curso concreto el revisor NO podrá acceder a ellos. Esto es útil para casos específicos donde necesitas restringir aún más el acceso

