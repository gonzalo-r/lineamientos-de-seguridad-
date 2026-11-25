# lineamientos-de-seguridad-
En el marco de la iniciativa Security by Design, compartimos los lineamientos y buenas prácticas de seguridad que deberán tenerse en cuenta durante el diseño y desarrollo del producto.

El objetivo es incorporar la seguridad desde las primeras etapas del desarrollo, promoviendo la construcción de aplicaciones seguras y reduciendo la introducción de vulnerabilidades en el código y la arquitectura de las soluciones.

Los siguientes lineamientos toman como referencia el estándar OWASP Application Security Verification Standard (ASVS 5.0.0) y buenas prácticas de desarrollo seguro.

1. Arquitectura y diseño seguro

Aplicar principios de seguridad desde el diseño de la solución.

Identificar los componentes, servicios, interfaces e integraciones de la aplicación.

Evitar exponer funcionalidades, servicios o recursos que no sean necesarios.

Diseñar considerando el principio de mínimo privilegio y la reducción de la superficie de ataque.

Evitar dependencias innecesarias entre componentes y servicios.

2. Autenticación y control de acceso

Implementar mecanismos de autenticación seguros.

No desarrollar mecanismos propios de gestión de credenciales cuando existan soluciones corporativas disponibles.

Aplicar el principio de mínimo privilegio.

Validar los permisos del usuario en el servidor para cada operación protegida.

Evitar accesos directos a recursos sin validar previamente los permisos correspondientes.

Implementar controles adecuados para prevenir ataques de fuerza bruta y abuso de autenticación.

3. Validación de entradas y tratamiento de datos

Validar todas las entradas recibidas desde usuarios, APIs y sistemas externos.

No confiar en información proveniente del cliente.

Utilizar consultas parametrizadas para prevenir SQL Injection.

Aplicar mecanismos de codificación y sanitización de salidas para prevenir ataques XSS.

Evitar la ejecución de comandos construidos a partir de entradas no confiables.

Validar tipos, formatos, longitudes y rangos de los datos recibidos.

4. Protección de información

Identificar y proteger los datos procesados y almacenados según su clasificación.

No exponer información sensible en respuestas, mensajes de error o registros de aplicación.

Utilizar mecanismos criptográficos reconocidos para proteger información sensible.

Implementar comunicaciones seguras mediante protocolos cifrados.

Evitar almacenar información sensible cuando no sea estrictamente necesaria.

5. Gestión de credenciales y secretos

No incluir contraseñas, tokens, claves privadas o credenciales dentro del código fuente.

No publicar secretos en repositorios, archivos de configuración o scripts.

Utilizar mecanismos seguros de almacenamiento y administración de secretos.

Evitar credenciales compartidas o embebidas en las aplicaciones.

Implementar mecanismos de rotación de credenciales cuando corresponda.

6. Gestión de sesiones

Utilizar identificadores de sesión seguros y no predecibles.

Implementar expiración de sesiones por inactividad y mecanismos de cierre de sesión.

Proteger las cookies y tokens de sesión.

Evitar exponer identificadores de sesión en URLs o registros.

7. Manejo de errores y registros

Evitar exponer información técnica interna mediante mensajes de error.

No mostrar trazas, consultas, credenciales o detalles de infraestructura al usuario.

Registrar eventos relevantes de seguridad y operaciones sensibles.

Proteger los registros contra modificaciones y accesos no autorizados.

Evitar registrar contraseñas, tokens y datos sensibles.

8. Uso de componentes y dependencias

Utilizar librerías, frameworks y componentes de fuentes confiables.

Mantener las dependencias actualizadas.

Evitar incorporar componentes obsoletos o con vulnerabilidades conocidas.

Utilizar únicamente los componentes necesarios para la funcionalidad de la aplicación.

Verificar la procedencia y confiabilidad de los paquetes incorporados.

9. Configuración segura

Evitar utilizar configuraciones predeterminadas inseguras.

Deshabilitar servicios, puertos y funcionalidades innecesarias.

No habilitar opciones de depuración en ambientes productivos.

Mantener separados los ambientes de desarrollo, testing y producción.

Evitar utilizar información productiva en ambientes no productivos sin las protecciones correspondientes.

10. Desarrollo y gestión del código fuente

Utilizar repositorios corporativos autorizados.

Mantener trazabilidad de los cambios realizados.

Aplicar revisiones de código antes de integrar cambios a las ramas principales.

Evitar incorporar código de origen desconocido o sin validación.

No incluir información confidencial ni secretos en comentarios, documentación o archivos versionados.

11. Protección de APIs y servicios

Implementar mecanismos de autenticación y autorización en los endpoints protegidos.

Validar todas las solicitudes recibidas.

Limitar el acceso a los recursos según los permisos correspondientes.

Implementar controles para prevenir abuso de servicios y solicitudes excesivas.

Evitar exponer información innecesaria en las respuestas de las APIs.

12. Manejo seguro de archivos

Validar el tipo, tamaño y contenido de los archivos recibidos.

Evitar confiar exclusivamente en la extensión del archivo.

Restringir los directorios y ubicaciones de almacenamiento.

Evitar la ejecución de archivos recibidos desde fuentes externas sin validación.

Consideraciones generales

Los lineamientos mencionados constituyen las prácticas mínimas de desarrollo seguro que deberán contemplarse durante la construcción del producto.

Su aplicación deberá adecuarse a las características técnicas, arquitectura y naturaleza de la solución, sin dejar de cumplir los requisitos de seguridad que resulten aplicables.

La seguridad debe ser considerada una responsabilidad compartida durante todo el proceso de desarrollo, y no una validación que se incorpora únicamente antes de la puesta en producción.

Para mayor referencia técnica, se recomienda consultar el estándar OWASP ASVS 5.0.0:
https://asvs.owasp.org/

