Ejercicio: Sistema de Gestión de Magos de Frieren

La Asociación Continental de Magos desea almacenar información sobre magos, hechizos, misiones y grimorios.

Se dispone de los siguientes datos:

Magos

Para cada mago se almacena:

Código de mago (único).
Nombre.
Edad.
Rango.
Afinidades mágicas (un mago puede tener varias).
Grimorios

Para cada grimorio:

Código de grimorio (único).
Nombre.
Rareza.
Fecha de descubrimiento.

Los grimorios contienen varios hechizos.

Hechizos

Un hechizo solamente existe dentro de un grimorio.

Para cada hechizo:

Número de hechizo dentro del grimorio.
Nombre.
Coste de maná.
Descripción.
Estudio de grimorios

Los magos pueden estudiar varios grimorios.

Para cada estudio se desea almacenar:

Fecha de inicio.
Nivel de dominio alcanzado.
Misiones

Para cada misión:

Código de misión (único).
Nombre.
Región.
Recompensa.

Una misión puede ser realizada por varios magos.

Para cada participación se registrará:

Rol desempeñado.
Puntuación obtenida.
Equipos

Los magos pueden organizarse en equipos.

Para cada equipo:

Código de equipo.
Nombre.

Cada equipo tiene un líder.

Ciudades

Para cada ciudad:

Código de ciudad.
Nombre.
Reino.

Los equipos pueden visitar ciudades.

Para cada visita se registrará:

Fecha.
Motivo.


Maestros y Aprendices
Un mago puede entrenar a varios magos.
Para cada entrenamiento se desea registrar:
Fecha de inicio del entrenamiento.
Relación avanzada

Durante una misión, un mago puede utilizar determinados hechizos.

Se desea almacenar:

Cuántas veces utilizó el hechizo durante la misión.

Este dato relaciona simultáneamente:

MAGO
MISIÓN
HECHIZO

Información derivada

Se desea conocer:

Número total de grimorios estudiados por cada mago.
Número total de hechizos contenidos en cada grimorio.
Ambos datos son derivados y no se almacenarán.