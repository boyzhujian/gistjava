### quick create maven project 
```
mvn archetype:generate -DgroupId=com.javapapers.sample -DartifactId=first-mavenapp -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false


  <properties>
    <maven.compiler.source>1.8</maven.compiler.source>
    <maven.compiler.target>1.8</maven.compiler.target>
  </properties>
 ```
 
###  run main class 
``` mvn exec:java -Dexec.mainClass="com.javapapers.sample.App"  ```


### show all info 
```mvn help:effective-pom```

### plugin help

```
mvn -Dplugin=<groupId>:<artifactId> help:describe

mvn  -Dplugin=org.springframework.boot:spring-boot-maven-plugin   help:describe 

mvn versions:display-plugin-updates   
```

