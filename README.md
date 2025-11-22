# Sistema de Gestor Peluqueria Fullstack-tfi
El sistema permite administrar una peluquería gestionando clientes, empleados, servicios y turnos. Se podrán registrar clientes, dar de alta empleados (barberos y estilistas), definir los servicios ofrecidos y agendar turnos entre clientes y empleados.
El sistema ofrece operaciones de búsqueda, modificación, eliminación y listado para cada tipo de entidad. También incluye funcionalidades adicionales como calcular los ingresos diarios, listar turnos por empleado, y mostrar los servicios más solicitados.
El programa utiliza programación estructurada, arrays, manejo de Strings, colecciones del Java Collections Framework, herencia, polimorfismo, interfaces, lambdas, Comparator, métodos de referencia y un TAD propio para guardar el historial de acciones, generacion de reportes y persistencia en archivos JSON.
Se implementan validaciones, manejo de excepciones con try–catch–finally y una excepción personalizada. El menú se ejecuta de forma recursiva hasta que el usuario decida salir.
Toda la interacción se realiza mediante consola, cumpliendo con todos los requisitos especificados en el Trabajo Práctico Integrador.

Este proyecto corresponde al Trabajo Final Integrador de la materia Programación, realizado por el grupo compuesto por Kevin Bizjan, Sebastián Flores y Thomas Borchichi.
El objetivo fue desarrollar un sistema completo para la administración de una peluquería, aplicando conceptos de programación orientada a objetos, colecciones, manejo de excepciones, persistencia y diseño modular.

El diseño se enfocó en lograr código claro, modular y fácil de mantener, respetando buenas prácticas de programación vistas en la cursada.

Tecnologías utilizadas:
Java 21
Persistencia en JSON mediante clases propias (sin bases de datos)
POO: herencia, polimorfismo, composición
Colecciones Java
Validaciones y excepciones personalizadas
VS Code + extensiones de Java

Estructura del proyecto:
peluqueria-tfi/
│
├── src/
│   ├── app/               # Menús y clase Main
│   ├── model/             # Clases del dominio (Cliente, Empleado, Servicio, Turno...)
│   ├── services/          # Lógica del negocio
│   ├── exceptions/        # Excepciones personalizadas
│   ├── repo/              # Persistencia en archivos JSON
│   └── util/              # Utilidades generales
│
├── data/                  # Archivos JSON generados automáticamente
│
└── README.md

Persistencia
Todo el sistema se guarda en archivos JSON ubicados en la carpeta /data, incluyendo:
clientes.json
empleados.json
servicios.json
turnos.json
La carga y el guardado son automáticos cada vez que se inicia o cierra la aplicación. Esto permite que toda la información permanezca disponible entre ejecuciones.

El sistema implementa distintas excepciones para mejorar la robustez:
ClienteDuplicadoException
ServicioInvalidoException
EmpleadoNoEncontradoException
TurnoNoDisponibleException
ElementoNoEncontradoException

Todas son manejadas desde los menús para evitar caídas del programa y mostrar mensajes claros al usuario.

Manual de Usuario – Sistema de Gestión de Peluquería Fullstack
Este sistema funciona íntegramente por consola y permite gestionar clientes, empleados, servicios y turnos de una peluquería.
A continuación se detallan los pasos para utilizarlo correctamente.

Inicio del programa
Al ejecutar el sistema aparece el menú principal:

PELUQUERÍA FULLSTACK – MENÚ PRINCIPAL
1. Gestión de clientes
2. Gestión de servicios
3. Gestión de empleados
4. Gestión de turnos
5. Reportes
0. Salir
El usuario debe ingresar un número del 0 al 5.

 1. Gestión de Clientes
Permite:
Agregar un cliente
Buscar por DNI
Buscar por nombre
Modificar datos
Eliminar
Listar todos

Validaciones:
DNI numérico
Teléfono numérico
Campos obligatorios

2. Gestión de Servicios
Incluye:
Crear servicios (nombre, precio, duración)
Editar
Buscar
Eliminar
Listar

Validaciones:
Precio mayor a 0
Duración mayor a 0 minutos

3. Gestión de Empleados
Permite:
Crear empleado (Barbero / Estilista)
Buscar por ID
Listar todos
Validaciones:
El tipo debe ser “Barbero” o “Estilista”
Nombre obligatorio

4. Gestión de Turnos
Funciones:
Crear turno
Cancelar
Finalizar
Listar por fecha
Listar por empleado
Listar todos

Validaciones:
Fecha futura
Cliente existente
Servicio existente
Empleado existente
Empleado disponible en ese horario
Uso de excepciones personalizadas

5. Reportes
Disponible:
Ingresos del día
Turnos pendientes
Turnos realizados
Ranking de servicios más vendidos
Ingresos por empleado
Horas trabajadas

Incluye persistencia automática.
Al cerrar o cambiar de menú, el sistema guarda la información en archivos JSON:
clientes.json
empleados.json
servicios.json
turnos.json
Y al iniciar, los vuelve a cargar automáticamente.

Consejos de uso:
Usar formato: dd/MM/yyyy HH:mm para turnos
Si se ingresa un dato inválido, el sistema mostrará un mensaje claro
Se puede usar sin perder datos gracias a la persistencia

Fin del Manual de Usuario

El trabajo fue realizado de forma colaborativa mediante control de versiones y ramas individuales.

Conclusión
El sistema cumple con todos los requisitos del Trabajo Final Integrador, utilizando conceptos fundamentales de programación en Java.
La aplicación es estable, modular y escalable, y la persistencia en JSON permite su uso real sin necesidad de bases de datos externas.
