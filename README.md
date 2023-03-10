# Price-management
**Price management** es un proyecto basado en **Arquitectura Hexagonal** que se encarga de obtener el precio final
(*pvp*) y la tarifa que aplica a un producto de una cadena (**Zara**) entre unas fechas determinadas.

## 馃搵 Caracter铆sticas del proyecto
### Formateo c贸digo (Google-Java-Format)

Con los siguientes comandos formateamos el c贸digo fuente, exceptuando los tests, otorgando legibilidad y consistencia
al c贸digo.
```
mvn com.coveo:fmt-maven-plugin:format
mvn com.coveo:fmt-maven-plugin:check
```

### Gesti贸n de calidad (Checkstyle)

Con el siguiente comando se ejecutar谩 el proceso de an谩lisis de c贸digo Checkstyle que comprobar谩 si el c贸digo fuente
cumple con las reglas de codificaci贸n.
```
mvn checkstyle:checkstyle
```
>**NOTA:** Por problemas de incoherencias que puedan surgir, se recomienda primero aplicar el correspondiente formateo
> de c贸digo antes de ejecutar el proceso de an谩lisis de c贸digo **Checkstyle**.

### Documentaci贸n de la API

Para ver la documentaci贸n referente a la API de una manera m谩s c贸moda necesitaremos copiar el siguiente documento
[api.yaml](src/main/resources/api.yaml) en el [Swagger Editor](https://editor.swagger.io/).

### API Testing
[Colecci贸n de pruebas de Postman]().

### PIT Mutation Testing

Para poder generar el informe de **PITest** referente al proyecto ser谩 necesario hacerlo usando el siguiente comando:
```
mvn org.pitest:pitest-maven:MutationCoverage
```

Esto generar谩 una carpeta (pit-reports) dentro del target del proyecto. Dicha carpeta a su vez tendr谩 un fichero
index.html que se podr谩 abrir en el navegador y explorar el informe de testing generado.

## 锔? 鈿欙笍 Ejecuci贸n 锔弝 configuraci贸n

Para ejecutar la aplicaci贸n bien se puede hacer accediendo a la clase PriceManagementApplication o bien ejecutando
los siguientes comandos.

### Instalaci贸n del artefacto en local.
```
mvn clean install
```

### Empaquetado el proyecto
```
mvn clean package
```

### Ejecuci贸n del proyecto
```
mvn clean spring-boot:run
```

### Ejecuci贸n del proyecto exceptuando tests
```
mvn clean package -DskipTests
```

### Ejecuci贸n de tests
```
mvn test
```

###  Base de datos en memoria h2

La ejecuci贸n de la API habilitar谩 una base de datos en memoria que se puede encontrar en
http://localhost:8080/h2-console.

`JDBC URL:`jdbc:h2:mem:pricesdb

`Username:` sa

`Password:`


