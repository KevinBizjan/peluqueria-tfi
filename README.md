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
GitHub
Java 21
Persistencia en JSON mediante clases propias (sin bases de datos)
POO: herencia, polimorfismo, composición
Colecciones Java
Validaciones y excepciones personalizadas
VS Code + extensiones de Java


Persistencia
Todo el sistema se guarda en archivos JSON ubicados en la carpeta /data.
La carga y el guardado son automáticos cada vez que se inicia o cierra la aplicación. Esto permite que toda la información permanezca disponible entre ejecuciones.

El sistema implementa distintas excepciones para mejorar la robustez.

Todas son manejadas desde los menús para evitar caídas del programa y mostrar mensajes claros al usuario.

Manual de Usuario – Sistema de Gestión de Peluquería Fullstack (LEER PDF)
Este sistema funciona íntegramente por consola y permite gestionar clientes, empleados, servicios y turnos de una peluquería.

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


El trabajo fue realizado de forma colaborativa mediante control de versiones y ramas individuales.

Conclusión
El sistema cumple con todos los requisitos del Trabajo Final Integrador, utilizando conceptos fundamentales de programación en Java.
La aplicación es estable, modular y escalable, y la persistencia en JSON permite su uso real sin necesidad de bases de datos externas.
