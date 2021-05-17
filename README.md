# microservicilities-quarkus project

Este proyecto utiliza Quarkus, el marco Java subatómico supersónico.

Si desea obtener más información sobre Quarkus, visite su sitio web: https://quarkus.io/ .

## Ejecutando la aplicación en modo dev

Puede ejecutar su aplicación en modo dev que habilita la codificación en vivo usando:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTA:_**  Quarkus ahora se envía con una interfaz de usuario de desarrollo, que está disponible en modo de desarrollo solo en http://localhost:8080/q/dev/.

## Empaquetando y ejecutando la aplicación

La aplicación se puede empaquetar usando:
```shell script
./mvnw package
```

Produce el archivo `quarkus-run.jar` en el directorio `target/quarkus-app/`.
Tenga en cuenta que no es un _über-jar_ ya que las dependencias se copian en el directorio `target/quarkus-app/lib/`.

Si desea construir un _über-jar_, ejecute el siguiente comando:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

La aplicación ahora se puede ejecutar usando `java -jar target/quarkus-app/quarkus-run.jar`.

## Creando un ejecutable nativo

Puede crear un ejecutable nativo usando: 
```shell script
./mvnw package -Pnative
```

O, si no tiene GraalVM instalado, puede ejecutar la compilación ejecutable nativa en un contenedor usando: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

Luego puede ejecutar su ejecutable nativo con: `./target/microservicilities-quarkus-1.0.0-SNAPSHOT-runner`

Si desea obtener más información sobre la creación de ejecutables nativos, consulte https://quarkus.io/guides/maven-tooling.html.

## Guías relacionadas

- RESTEasy JAX-RS ([guide](https://quarkus.io/guides/rest-json)): REST endpoint framework implementing JAX-RS and more

## Ejemplos proporcionados

### RESTEasy JAX-RS Ejemplos

REST es fácil con este recurso RESTEasy de Hello World.

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)

## Guia ejercicio

[Related guide section...](https://www.infoq.com/articles/microservicilities-quarkus/)
