# weld-inject-tck
Project to run Weld against the Jakarta Dependency Injection TCK

## Download TCK
```shell script
wget http://download.eclipse.org/ee4j/cdi/jakarta.inject-tck-1.0-bin.zip
unzip jakarta.inject-tck-1.0-bin.zip
cd jakarta.inject-tck-1.0
```

## Install the TCK jar
```shell script
mvn org.apache.maven.plugins:maven-install-plugin:3.0.0-M1:install-file \
-Dfile=jakarta.inject-tck-1.0.jar
```

# Clone the weld-inject-tck running
```shell script
git clone https://github.com/jakartaredhat/weld-inject-tck
cd weld-inject-tck
```

## Run the tests
if running prior to Jakarta EE 8 release with staged api jars use:
```shell script
mvn -Pstaging clean test
```
If running after the Jakarta EE 8 final release use:
```shell script
mvn clean test
```