El Ministerio de Magia británico quiere desarrollar una base de datos para gestionar toda la actividad relacionada con las escuelas de magia, los estudiantes, profesores, asignaturas, criaturas mágicas, hechizos, torneos y eventos mágicos que se celebran cada año.

Dado el gran volumen de información que se maneja, se necesita diseñar una base de datos que permita almacenar y gestionar todos estos datos de forma eficiente.

Información a almacenar
Escuelas de magia

De cada escuela de magia se conoce:

Código de escuela (único).
Nombre.
País.
Fecha de fundación.
Director actual.
Número máximo de estudiantes.

Una escuela puede tener varias casas mágicas.

Casas mágicas

Cada casa estará identificada mediante un código único.

Además se almacenará:

Nombre.
Color representativo.
Emblema.
Escuela a la que pertenece.

Ejemplos de casas son Gryffindor, Slytherin, Ravenclaw o Hufflepuff.

Personas

Se desea almacenar información de todas las personas relacionadas con el mundo mágico.

De cada persona se conoce:

DNI mágico.
Nombre.
Apellidos.
Fecha de nacimiento.
Nacionalidad.
Dirección mágica.
Correo de lechuza.
Número de varita.

Una misma persona puede desempeñar distintos roles simultáneamente:

Estudiante.
Profesor.
Auror.
Investigador mágico.
Estudiantes

De los estudiantes interesa conocer además:

Curso actual.
Año de ingreso.
Casa a la que pertenecen.
Nivel académico.
Profesores

De los profesores se almacenan:

Especialidad.
Fecha de contratación.
Salario.
Años de experiencia.

Un profesor puede impartir varias asignaturas.

Asignaturas

Cada asignatura estará identificada mediante un código.

También se almacena:

Nombre.
Número de créditos mágicos.
Curso recomendado.
Departamento responsable.

Ejemplos de asignaturas:

Pociones.
Defensa Contra las Artes Oscuras.
Herbología.
Transformaciones.
Encantamientos.
Historia de la Magia.
Departamentos

De cada departamento se conoce:

Código.
Nombre.
Presupuesto anual.
Profesor jefe.

Un departamento puede gestionar varias asignaturas.

Hechizos

De cada hechizo interesa almacenar:

Código.
Nombre.
Tipo.
Nivel de dificultad.
Efecto principal.
Consumo de energía mágica.

El atributo tipo solo podrá tomar uno de los siguientes valores:

Encantamiento
Maldición
Contrahechizo
Transformación
Invocación
Curación
Defensa
Varitas mágicas

De cada varita se conoce:

Número de serie.
Tipo de madera.
Núcleo mágico.
Longitud.
Flexibilidad.
Fecha de fabricación.

Cada varita pertenece a una única persona.

Criaturas mágicas

De cada criatura mágica se almacena:

Código.
Nombre.
Especie.
Nivel de peligrosidad.
Hábitat.
Estado de conservación.
Pociones

Cada poción estará identificada por un código.

Además se conocerá:

Nombre.
Nivel de dificultad.
Tiempo de preparación.
Efecto producido.
Ingredientes mágicos

De cada ingrediente se conoce:

Código.
Nombre.
Rareza.
Procedencia.
Precio de mercado.

Una poción puede necesitar varios ingredientes y un ingrediente puede usarse en varias pociones.

Torneos mágicos

De cada torneo se almacena:

Código.
Nombre.
Fecha de inicio.
Fecha de finalización.
Premio.
Escuela organizadora.

En un torneo pueden participar varios estudiantes.

Pruebas del torneo

Cada torneo está compuesto por diferentes pruebas.

De cada prueba se conoce:

Número de prueba.
Nombre.
Descripción.
Puntuación máxima.
Nivel de dificultad.
Eventos mágicos

Cuando se celebra un evento mágico se registra:

Código de evento.
Nombre.
Fecha.
Hora de inicio.
Hora de finalización.
Escuela organizadora.
Profesor responsable.
Lugar de celebración.

Además es necesario conocer:

Los estudiantes participantes.
Los profesores asistentes.
Los hechizos utilizados.
Las criaturas mágicas involucradas.
Las pociones empleadas.

Las fechas se almacenarán en formato DD/MM/AAAA.

Lugares mágicos

De cada lugar mágico se almacenan:

Código.
Nombre.
Tipo de lugar.
Capacidad máxima.
Ubicación.

El atributo tipo de lugar solo podrá tomar los valores:

Castillo
Bosque
Lago
Mazmorra
Aula
Estadio
Ministerio
Restricciones semánticas
Cada escuela debe tener al menos una casa mágica.

Un estudiante solo puede pertenecer a una casa al mismo tiempo.

Un estudiante solo puede estar matriculado en una escuela.

Cada departamento debe estar dirigido por un único profesor.

Un profesor puede pertenecer a varios departamentos, pero solamente dirigir uno.

Los códigos de las asignaturas son únicos dentro de cada departamento.

Ninguna criatura mágica con peligrosidad superior a 8 podrá participar en eventos donde intervengan estudiantes de primer curso.

Un estudiante no podrá participar en un torneo si no pertenece a alguna escuela.

Un profesor responsable de un evento debe tener como mínimo 5 años de experiencia.

Un hechizo clasificado como "Maldición" no podrá ser utilizado en eventos académicos.

Una varita únicamente puede estar asociada a una persona.

Una persona no podrá poseer más de dos varitas registradas.

Una prueba pertenece a un único torneo.

Un torneo debe contener al menos tres pruebas.

Una poción debe estar compuesta, como mínimo, por un ingrediente.

Un estudiante no podrá matricularse en una asignatura de cuarto curso sin haber superado las asignaturas equivalentes de cursos anteriores.

Ningún evento podrá celebrarse simultáneamente en el mismo lugar.

Un profesor no podrá ser responsable de dos eventos que se desarrollen en la misma fecha y hora.

Un estudiante no podrá participar en más de dos torneos durante el mismo curso académico.

Las criaturas clasificadas como "en peligro de extinción" solo podrán participar en eventos autorizados por el Ministerio de Magia.

Los hechizos serán identificados mediante un código secuencial independiente para cada tipo de hechizo.

Un ingrediente de rareza "Legendaria" únicamente podrá utilizarse en pociones de dificultad alta.

El director de una escuela debe ser un profesor perteneciente a dicha escuela.

Una asignatura puede requerir otras asignaturas como prerrequisitos.

Una persona puede ser simultáneamente estudiante, profesor, auror e investigador mágico.