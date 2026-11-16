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
Estado del estudio

Los magos pueden estudiar varios grimorios y un grimorio puede ser estudiado por varios magos.

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



```mermaid

    MAGO {
        int cod_mago PK
        string nombre
        int edad
        string rango
    }

    AFINIDAD {
        int cod_afinidad PK
        string nombre
    }

    GRIMORIO {
        int cod_grimorio PK
        string nombre
        string rareza
        date fecha_descubrimiento
    }

    HECHIZO {
        int num_hechizo PK
        string nombre
        float coste_mana
        string descripcion
        string estado_estudio
    }

    MISION {
        int cod_mision PK
        string nombre
        string region
        float recompensa
    }

    EQUIPO {
        int cod_equipo PK
        string nombre
    }

    CIUDAD {
        int cod_ciudad PK
        string nombre
        string reino
    }

    %% Relación identificadora (Entidad débil)
    GRIMORIO ||--|{ HECHIZO : contiene

    %% N:M Mago-Afinidad
    MAGO }o--o{AFINIDAD : posee

    %% N:M Mago-Grimorio
    MAGO}o--o{GRIMORIO : estudia

    %% N:M Mago-Misión
    MAGO}o--o{MISION : participa

    %% N:M Equipo-Mago
    EQUIPO}o--o{ MAGO : miembros

    %% Líder del equipo
    MAGO ||--o{EQUIPO : lidera

    %% N:M Equipo-Ciudad
    EQUIPO}o--o{ CIUDAD : visita

    %% Relación recursiva
    MAGO ||--o{ MAGO : entrena

    %% Relación ternaria descompuesta
    MAGO ||--o{ UTILIZA : usa
    MISION ||--o{ UTILIZA : durante
    HECHIZO ||--o{ UTILIZA : ejecuta

    UTILIZA {
        int veces_utilizado
    }

    %% Atributos de relaciones N:M

    ESTUDIA {
        date fecha_inicio
        string nivel_dominio
    }

    PARTICIPACION {
        string rol
        int puntuacion
    }

    VISITA {
        date fecha
        string motivo
    }

    ENTRENAMIENTO {
        date fecha_inicio
    }
    ```