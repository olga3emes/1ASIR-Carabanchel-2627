Crear el modelo relacional que represente el organigrama de una empresa, de modo que:
Aparezcan los datos de todos los empleados: DNI, N.º de seguridad social, código de trabajador, nombre, apellidos, dirección, teléfono y departamento en el que trabajan indicado por su código y nombre.
También hay que tener en cuenta que cada trabajador puede tener un responsable (que en realidad es otro trabajador).
Los departamentos poseen un único coordinador.
Necesitamos almacenar la categoría profesional de los trabajadores, teniendo en cuenta que la categoría a veces cambia al cambiar el contrato, de los contratos se almacena la fecha de inicio de éste y la fecha final (un contrato en vigor tendrá como fecha final el valor nulo).
También controlaremos las nóminas que ha recibido el trabajador de las que sabemos la fecha, el salario y a qué trabajador van dirigidas y la categoría de éste.
