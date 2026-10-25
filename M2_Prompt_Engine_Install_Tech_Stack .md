# PROMPT PARA CODEX — INSTALACIÓN Y EJECUCIÓN COMPLETA DEL LABORATORIO JAVA

## ROL

Actuá como un Senior Java Software Engineer, DevOps Engineer y especialista en Spring Boot, JPA, Hibernate, PostgreSQL, Docker, Eclipse IDE y Windows.

Necesito que trabajes como agente autónomo para preparar mi computadora desde cero y ejecutar un proyecto empresarial Java existente.

**Quiero que ejecutes las tareas, no que solamente me entregues instrucciones.**

Soy docente universitaria de Ingeniería de Software y necesito que el entorno quede completamente preparado para una demostración académica de 20 minutos.

## 1. CONTEXTO Y REPOSITORIOS

**Proyecto empresarial original:**

https://github.com/No-Country-simulation/S07-26-Team-26

Nombre: Ghost Load.

Es una aplicación empresarial para evaluar la eficiencia y capacidad no productiva de centros de datos.

Tecnologías identificadas:

- Java 21.
- Spring Boot 4.1.0, según el pom.xml revisado.
- Maven.
- Spring Data JPA.
- Hibernate.
- PostgreSQL 16.
- Flyway.
- Docker Compose.
- React y Next.js.

**Repositorio académico:**

ADE_M2_Aplicaciones_Interactiva

Este repositorio se utilizará para documentar el ejercicio de la materia.

No modifiques ni publiques cambios en el repositorio original. Trabajá sobre una copia local y una rama independiente.

No sobrescribas archivos del repositorio académico sin comprobar primero su contenido.

## 2. OBJETIVO FINAL

Quiero que mi computadora tenga:

1. Java JDK 21 instalado y funcionando.
2. Git instalado.
3. Eclipse IDE instalado y configurado.
4. Docker Desktop funcionando.
5. Docker Compose disponible.
6. Proyecto Ghost Load clonado.
7. Backend Spring Boot compilado y ejecutándose.
8. PostgreSQL 16 funcionando mediante Docker.
9. Frontend accesible desde el navegador.
10. Proyecto Java importado en Eclipse.
11. Un ejercicio real de persistencia de datos probado.
12. Documentación para reproducir la práctica universitaria.

No quiero crear un proyecto nuevo con Spring Initializr porque el proyecto original ya contiene el backend y su archivo pom.xml.

## 3. FASE 1 — DIAGNÓSTICO AUTOMÁTICO

Detectá el sistema operativo y comprobá:

- Versión de Windows.
- Arquitectura del procesador.
- Disponibilidad de PowerShell.
- Disponibilidad de winget.
- Java y javac.
- Git.
- Docker Desktop y Docker Compose.
- Eclipse IDE.
- Maven o Maven Wrapper.
- Virtualización y WSL2.

Mostrame qué herramientas están disponibles y cuáles faltan.

No reinstales programas existentes que funcionen correctamente.

## 4. FASE 2 — INSTALACIÓN DE HERRAMIENTAS

Instalá automáticamente las herramientas faltantes, utilizando fuentes oficiales.

### Java

Instalar JDK 21.

Verificar:

java -version

javac -version

Configurar JAVA_HOME cuando corresponda.

### Git

Instalar Git y comprobar:

git --version

### Eclipse

Instalar Eclipse IDE for Enterprise Java and Web Developers.

Configurar JDK 21.

Verificar soporte Maven y compatibilidad con Spring Boot.

Instalar Spring Tools solamente si resulta necesario.

### Docker Desktop

Instalar Docker Desktop.

Configurar Docker Compose y WSL2 si corresponde.

Verificar:

docker --version

docker compose version

docker info

Si alguna instalación necesita permisos de administrador, aprobación de Windows o reinicio, solicitá mi intervención y continuá después.

No desactives medidas de seguridad del sistema.

## 5. FASE 3 — CLONAR GHOST LOAD

Crear una carpeta local para proyectos académicos.

Clonar:

git clone https://github.com/No-Country-simulation/S07-26-Team-26.git

Entrar en el proyecto.

Crear una rama local:

git switch -c laboratorio-jpa

Analizar:

- README.md.
- backend/pom.xml.
- backend/src/main/java.
- backend/src/main/resources.
- frontend/.
- docker-compose.yml.
- backend/.env.example.

Verificar la versión real de Java y Spring Boot.

No cambiar versiones ni dependencias sin necesidad técnica demostrada.

## 6. FASE 4 — CONFIGURAR POSTGRESQL

Utilizar PostgreSQL mediante Docker Compose.

No instalar otro servidor PostgreSQL directamente en Windows salvo que exista una necesidad justificada.

Revisar la configuración del servicio PostgreSQL.

Crear el archivo:

backend/.env

a partir de:

backend/.env.example

Configurar las variables necesarias utilizando credenciales locales seguras.

No mostrar ni publicar contraseñas.

No incorporar archivos .env al repositorio Git.

Comprobar:

- Contenedor PostgreSQL.
- Puerto 5432.
- Base de datos ghost_load.
- Conectividad desde el backend.
- Persistencia mediante volumen Docker.

No eliminar volúmenes existentes.

## 7. FASE 5 — LEVANTAR LA APLICACIÓN COMPLETA

Desde la raíz del repositorio, una vez configurado el entorno, ejecutar:

docker compose --env-file backend/.env up --build

Verificar los tres servicios:

**PostgreSQL**

Base de datos relacional utilizada para almacenar los datos del negocio.

**Backend**

Aplicación Java con Spring Boot, Spring Data JPA e Hibernate.

**Frontend**

Interfaz web desarrollada con React y Next.js.

Según la documentación original, las direcciones esperadas son:

- Frontend: http://localhost:3001
- Backend: http://localhost:8080
- PostgreSQL: localhost:5432

Comprobar el endpoint:

http://localhost:8080/actuator/health

No afirmar que los servicios están funcionando sin comprobarlo.

Si existe algún error de compilación, conexión o configuración, investigarlo y aplicar una corrección mínima, documentando lo realizado.

## 8. FASE 6 — CONFIGURAR ECLIPSE

Abrir Eclipse.

Seleccionar JDK 21.

Importar el proyecto Maven existente:

File → Import → Maven → Existing Maven Projects.

Seleccionar la carpeta:

S07-26-Team-26/backend

Verificar que Eclipse reconozca:

- pom.xml.
- Dependencias Maven.
- Clases Java.
- Configuración Spring Boot.
- Entidades JPA.
- Repositorios.
- Controladores.
- Servicios.
- Adaptadores de persistencia.

Identificar la clase principal de Spring Boot.

Preparar la ejecución y depuración del backend desde Eclipse.

Si el backend está funcionando en Docker, evitar ejecutar otra instancia en el mismo puerto 8080.

## 9. FASE 7 — IDENTIFICAR EL EJERCICIO REAL

Necesito preparar una demostración de persistencia de datos.

Seleccionar preferentemente este caso empresarial:

**Registrar un operador y crear una evaluación de eficiencia de un centro de datos.**

Buscar en el código real:

- Endpoint HTTP.
- Controller o adaptador de entrada.
- Caso de uso.
- Servicio de aplicación.
- Puerto de persistencia.
- Adaptador de persistencia.
- Entidad JPA.
- Repositorio Spring Data JPA.
- Tabla PostgreSQL.
- Migración Flyway.

Mostrarme las rutas exactas de los archivos encontrados.

No inventar nombres de clases ni endpoints.

Respetar la arquitectura hexagonal existente.

## 10. FASE 8 — EXPLICAR JPA E HIBERNATE

Identificar en el código las anotaciones disponibles:

@Entity

@Table

@Id

@Column

@GeneratedValue

Buscar interfaces que extiendan JpaRepository.

Explicar:

- Qué representa una entidad Java.
- Cómo se relaciona con una tabla PostgreSQL.
- Qué es una clave primaria.
- Qué responsabilidad tiene Spring Data JPA.
- Qué es la especificación JPA.
- Cómo Hibernate implementa el mapeo objeto-relacional.
- Cómo interviene JDBC.
- Cómo se ejecutan las consultas SQL.

Diferenciar los objetos temporales en memoria RAM de los registros persistidos en PostgreSQL.

## 11. FASE 9 — EJECUTAR OPERACIONES REALES

### Operación de escritura

Ejecutar un endpoint existente que permita registrar un operador o crear una evaluación.

Verificar el flujo:

Solicitud HTTP → Spring Boot → caso de uso → adaptador de persistencia → Spring Data JPA → Hibernate → PostgreSQL.

Registrar la respuesta HTTP.

### Operación de lectura

Ejecutar un endpoint existente que permita consultar la evaluación o el operador registrado.

Comprobar que los datos se recuperan de PostgreSQL.

### Verificación SQL

Utilizar psql u otra herramienta apropiada para consultar los registros.

Mostrar una consulta SELECT real, utilizando nombres de tablas y columnas previamente verificados.

No utilizar información personal real.

No modificar datos ajenos al ejercicio.

## 12. FASE 10 — DOCUMENTACIÓN ACADÉMICA

Preparar o actualizar la documentación del laboratorio:

**ADE_M2_Aplicaciones_Interactiva**

El README debe incluir:

- Objetivos de aprendizaje.
- Descripción de Ghost Load.
- Arquitectura de la solución.
- Tecnologías.
- Instalación y configuración.
- Comandos de ejecución.
- Entidades JPA identificadas.
- Repositorios y adaptadores.
- Endpoints utilizados.
- Operación de escritura.
- Operación de lectura.
- Verificación SQL.
- Evidencias de ejecución.
- Guion de demostración de 20 minutos.

Conservar la atribución y la licencia del proyecto original.

No publicar cambios automáticamente en GitHub sin mi aprobación.

## 13. FASE 11 — PREPARAR LA CLASE DE 20 MINUTOS

Diseñar una demostración con esta distribución:

| Tiempo | Actividad |
|---|---|
| 0–3 min | Problema empresarial y caso Ghost Load |
| 3–6 min | Arquitectura de la aplicación |
| 6–10 min | Entidad JPA y Repository |
| 10–14 min | Operación de escritura |
| 14–17 min | Consulta y verificación PostgreSQL |
| 17–20 min | Conclusiones y preguntas |

La instalación completa debe quedar finalizada antes de la clase.

Crear un documento que indique qué archivos abrir en Eclipse, qué comandos ejecutar y qué resultados mostrar.

## 14. CRITERIOS DE FINALIZACIÓN

Antes de terminar, verificar:

- [ ] JDK 21 instalado.
- [ ] Git funcionando.
- [ ] Docker Desktop funcionando.
- [ ] Eclipse configurado.
- [ ] Repositorio clonado.
- [ ] PostgreSQL funcionando.
- [ ] Backend compilado.
- [ ] Backend ejecutándose.
- [ ] Frontend accesible.
- [ ] Entidades JPA identificadas.
- [ ] Repositorios identificados.
- [ ] Operación de escritura comprobada.
- [ ] Operación de lectura comprobada.
- [ ] Consulta SQL verificada.
- [ ] README académico preparado.
- [ ] Guion de clase terminado.

Para cada elemento, informar si está completado, pendiente o bloqueado.

## INSTRUCCIÓN FINAL

Comenzá inmediatamente con el diagnóstico de mi computadora.

Avanzá de forma autónoma con todas las tareas que puedas ejecutar.

No te detengas después de entregar un plan.

Quiero que instales, configures, descargues, compiles, ejecutes y verifiques el proyecto.

Solicitá mi intervención únicamente cuando sea necesaria una autorización, una acción gráfica que no puedas realizar o una decisión que pueda afectar mi computadora o mis repositorios.

Al finalizar, entregame un informe técnico de todo lo realizado y dejá preparado el entorno para la demostración universitaria.
