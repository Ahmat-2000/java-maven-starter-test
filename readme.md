# Project Name

## Overview
This is a Java project managed with Maven.

## Project Structure
```
├── pom.xml
└── src
    ├── main
    │   └── java
    │       └── com
    │           └── ahmat
    │               └── App.java
    └── test
        └── java
            └── com
                └── ahmat
                    └── AppTest.java
```

## Prerequisites
Ensure you have the following installed on your system:
- Java Development Kit (JDK) 8 or later
- Apache Maven 3.6 or later

## Build and Run

### Compile the project
```sh
mvn compile
```

### Package the project
```sh
mvn package
```

This will generate a JAR file inside the `target/` directory.

### Run the application
```sh
java -cp target/your-app-name.jar com.ahmat.App
```
Replace `your-app-name.jar` with the actual generated JAR file name.

### Run tests
```sh
mvn test
```

### Clean the project
```sh
mvn clean
```

### Format the code
```sh
mvn fmt:format
```

### Check for dependency updates
```sh
mvn versions:display-dependency-updates
```

## Creating the Maven Project
Run the following command to generate a new Maven project:
```sh
mvn archetype:generate -DgroupId=com.yourname.poker -DartifactId=poker-game -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

## `pom.xml` Configuration
Include the following `pom.xml` file configuration:
```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.yourname.poker</groupId>
  <artifactId>poker-game</artifactId>
  <packaging>jar</packaging>
  <version>1.0-SNAPSHOT</version>
  <name>poker-game-test</name>
  <url>http://maven.apache.org</url>

  <properties>
    <maven.compiler.source>21</maven.compiler.source>
    <maven.compiler.target>21</maven.compiler.target>
  </properties>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.13.2</version>
      <scope>test</scope>
    </dependency>
  </dependencies>

  <build>
  <plugins>
    <!-- Shade Plugin to create an executable JAR -->
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-shade-plugin</artifactId>
      <version>3.2.4</version>
      <executions>
        <execution>
          <phase>package</phase>
          <goals>
            <goal>shade</goal>
          </goals>
        </execution>
      </executions>
      <configuration>
        <transformers>
          <transformer implementation="org.apache.maven.plugins.shade.resource.ManifestResourceTransformer">
            <mainClass>com.yourname.poker.App</mainClass>
          </transformer>
        </transformers>
      </configuration>
    </plugin>
  </plugins>
  </build>
</project>
```

## Contributing
1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Make your changes and commit (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Create a Pull Request

## License
This project is licensed under the MIT License. See `LICENSE` file for details.


