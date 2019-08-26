# weld-inject-tck
Project to run Weld against the Jakarta Dependency Injection TCK

## Download TCK
```shell script
wget http://download.eclipse.org/ee4j/cdi/jakarta.inject-tck-1.0-bin.zip
unzip jakarta.inject-tck-1.0-bin.zip
```

## Install the TCK jar
```shell script
mvn org.apache.maven.plugins:maven-install-plugin:3.0.0-M1:install-file \
-Dfile=jakarta.inject-tck-1.0.jar
```

## Run the tests
if running with staged api jars use:
```shell script
mvn -Pstaging clean test
```
If running after the Jakarta EE 8 final release use:
```shell script
mvn clean test
```